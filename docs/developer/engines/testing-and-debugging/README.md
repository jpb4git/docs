# Testing your Engine

Before submitting your build, use the following information to test it thoroughly.

## Testing a Segment or Stream Engine

### Testing Locally

The recommended way to test these types of engines locally is by simulating and verifying locally that your engine can consume and produce the messages documented in the construction guidelines listed below.

* [Segment Engine Construction Guidelines](/developer/engines/processing-modes/segment-processing/)
* [Stream Engine Construction Guidelines](/developer/engines/processing-modes/stream-processing/)

### Testing in aiWARE

You can test your uploaded build in CMS by following the steps below.


1\. Click on the `New` button and then select `Ingestion Job`

![cms ingestion job 1](images/cms-ingestion-job-1.png)


2\. Select an adapter. For this example we're going to select the Web Stream Adapter.


![select an adapter](images/select-an-adapter.png)

3\. If you don't have any existing sources, click on the `Select a Source` dropdown and then click on `Create New Source`


![create new source](images/create-new-source.png)

4\. On the new source page, fill out the `Source Name` and the `Stream URL` fields and then click `Create`.


![new source page](images/new-source-page.png)

5\. Select the newly created source from the `Select a Source` dropdown and click `Next`.


![select new source](images/select-new-source.png)


6\. On the schedule page, choose immediate and then click `Next`.


![schedule page](images/schedule-page.png)


7\. The default view of the processing step displays the Simple Cognitive Workflow which allows users to select a category in which Veritone chooses the best engine of that given category to process their media with. As the intention is to test your own engine, you need to click on `Show Advanced Congnitive Workflow` at the upper right corner.

![advanced workflow](images/advanced-workflow.png)


8\. On the Advanced Cognitive Workflow page, click on the dropdown under Available Engines and choose the category that corresponds to your engine. You will then see your engine in the engine list. Click on the green plus icon to select your engine and move it to the Selected Engines panel. If your engine requires either engine parameters or a library you will now be asked to input these. After configuring your engine parameters, click `Next`.

![select engine](images/select-engine.png)

9\. Click `Next` on the Content Templates step which will take you to the final step `Customize`. Fill out the `Customize` step with any information you'd like, and finally click `Save` to finish.  That will redirect you to the CMS main page.


![customize step](images/customize-step.png)


10\. You have now successfully created an ingestion job, which your engine build will be asked to process. You can click on the `Processing Status` button in the left navigation panel to view the processing list, which gives an overview of all of the recently processed files and their status. You can also click on a file in the processing list to view its media details page where you can view the output of a successfully processed file, as well as make additional actions against the file such as reprocessing.

If your ingestion job results in an error, please read the section below on debugging to get a better understanding of how to debug your engine in the Veritone Platform.

## Testing a Legacy (Batch) Engine

!> Legacy batch engines are deprecated.
If you have developed a legacy batch engine, we highly recommend you upgrade it to a [segment engine](/developer/engines/processing-modes/segment-processing/).

Information on testing legacy engines is available [here](/developer/engines/testing-and-debugging/batch-engines/). 

## Debugging

Any time your engine is asked to process a task which belongs to you, it will be displayed as a new task row under the tasks page of your engine in VDA. This is the best starting point for debugging.

By expanding the task row, you will be able to view additional information about your task in the tabs provided which are detailed below.

##### Payload

The payload tab displays the JSON payload that your engine will receive at runtime. You should verify that you are handling the payload correctly in your engine and also that the correct parameters (custom fields) are being passed to your engine inside of the payload.

You can view your task payload via graphql by using the snippet below:

```graphql
query {
  task(id: "replaceMe") {
    payload
  }
}
```

##### Task Log

The task log tab displays your engines task log in JSON format.
The task log is the primary way for you to debug as it allows you to view the standard output (stdout) of your engine.
The only exception to this is for Segment engines, for which we do not attach stdout as part of the task log.
For both Stream and Segment engines you will also be able to view kafka events here if they are related to your task.

> We only return the task log for completed or failed tasks so it is vital that your engine correctly updates the task status in response to both success/errors in order for you to view your logs.


You can view your task log via graphql by using the snippet below:

```graphql
query {
  task(id: "replaceMe") {
    log {
      uri
      text
      jsondata
    }
  }
}
```


##### Task Output
The task output tab displays your engine results. Take a look [here](apis/tutorials/engine-results?id=uploading-engine-results) for more information about engine results.

You can view your task output via graphql by using the snippet below:

```graphql
query {
  task(id: "replaceMe") {
    output # JSON
    outputString # stringified
  }
}
```

##### Assets
The assets tab displays all of the assets that were produced by your engine for that particular task. This allows you to view the type of asset that was produced, and also allows you to view the source by clicking on the asset ID. This is useful for verifying that the assets produced have been processed by your engine correctly.

You can also view the assets created by your engine by using the graphql query below.  Replace the ID `replaceMe` with the `recordingId` from your task payload.

```graphql
query{
  temporalDataObject(id:"replaceMe"){
    assets(orderBy:createdDateTime) {
      records  {
        id
        assetType
        contentType
        createdDateTime
        jsondata
        signedUri
      }
    }
  }
}
```

This query orders the assets by when they were created, with the most recent asset first. Use the `signedUri` value to view the asset in your browser.

You can also filter by specific types of assets by including the `type` filter. This filters against the `assetType` of the asset. See the query below for an example.

```graphql
query{
  temporalDataObject(id:"replaceMe"){
    assets(type: "vtn-standard" orderBy:createdDateTime) {
      records  {
        id
        assetType
        contentType
        createdDateTime
        jsondata
        signedUri
      }
    }
  }
}
```