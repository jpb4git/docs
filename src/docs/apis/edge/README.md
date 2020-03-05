<!-- markdownlint-disable -->

# Veritone aiWARE Edge API

This is the aiWARE Edge API

More information: [https://aiware.com](https://aiware.com)

Contact Info: [api@aiware.com](api@aiware.com)

Version: 1.0.3

<!-- Apache 2.0

http://www.apache.org/licenses/LICENSE-2.0.html -->

## Access

    APIKey KeyParamName:api\_key KeyInQuery:false KeyInHeader:true

## Methods

\[ Jump to [Models](#__Models) \]

#### [Admin](#Admin)

These are the Admin methods.

*   [`post /admin/server_type/{ServerTypeID}/add`](#addserversServerType)
*   [`post /admin/terminate`](#adminTerminateCluster)
*   [`post /admin/licenses/apply`](#applyLicense)
*   [`post /admin/cores/create`](#createAdminCore)
*   [`post /admin/organizations/create`](#createAdminOrganization)
*   [`post /admin/server_types/create`](#createServerType)
*   [`post /admin/tokens/create`](#createToken)
*   [`post /admin/users/create`](#createUser)
*   [`delete /admin/licenses/{LicenseID}/delete`](#deleteLicense)
*   [`delete /admin/server_type/{ServerTypeID}/delete`](#deleteServerType)
*   [`post /admin/server_type/{ServerTypeID}/delete`](#deleteServerTypePost)
*   [`post /admin/server_type/{ServerTypeID}/desired`](#desiredserversServerType)
*   [`get /admin/core/{CoreID}/detail`](#getAdminCoreDetail)
*   [`get /admin/cores`](#getAdminCores)
*   [`get /admin/organization/{OrganizationID}/detail`](#getAdminOrganizationDetail)
*   [`get /admin/organization/{OrganizationID}/tokens`](#getAdminOrganizationTokens)
*   [`get /admin/organizations`](#getAdminOrganizations)
*   [`get /admin/status`](#getAdminStatus)
*   [`get /admin/user/{UserID}/detail`](#getAdminUserDetail)
*   [`get /admin/user/{UserID}/tokens`](#getAdminUserTokens)
*   [`get /admin/users`](#getAdminUsers)
*   [`get /admin/config`](#getConfig)
*   [`get /admin/config/{ConfigSection}`](#getConfigSection)
*   [`get /admin/config/{ConfigSection}/{ConfigKey}`](#getConfigSectionKey)
*   [`get /admin/licenses/{LicenseID}/detail`](#getLicenseDetail)
*   [`get /admin/licenses`](#getLicenses)
*   [`get /admin/server_type/{ServerTypeID}/detail`](#getServerType)
*   [`get /admin/server_types`](#getServerTypes)
*   [`post /admin/users/login`](#loginUser)
*   [`post /admin/server_type/{ServerTypeID}/remove`](#removeserversServerType)
*   [`post /admin/config`](#updateConfigAll)
*   [`post /admin/config/{ConfigSection}`](#updateConfigSection)
*   [`post /admin/config/{ConfigSection}/{ConfigKey}`](#updateConfigSectionKey)
*   [`post /admin/server_type/{ServerTypeID}/update`](#updateServerType)

#### [Engine](#Engine)

*   [`post /engine/create`](#createEngine)
*   [`post /engine/category/create`](#createEngineCategory)
*   [`post /engine/{EngineID}/build/{BuildID}/delete`](#deleteBuildPost)
*   [`post /engine/{EngineID}/delete`](#deleteEnginePost)
*   [`get /engine/{EngineID}/build/{BuildID}`](#getEngineBuild)
*   [`get /engine/{EngineID}/builds`](#getEngineBuilds)
*   [`get /engine/categories`](#getEngineCategories)
*   [`get /engine/category/{EngineCategoryID}/detail`](#getEngineCategoryDetail)
*   [`get /engine/{EngineID}/detail`](#getEngineDetail)
*   [`get /engine/instance/{EngineInstanceID}/detail`](#getEngineInstanceDetail)
*   [`get /engine/instance/{EngineInstanceID}/logs`](#getEngineInstanceLogs)
*   [`get /engine/instance/{EngineInstanceID}/status`](#getEngineInstanceStatus)
*   [`post /engine/{EngineInstanceID}/getwork`](#getEngineInstanceWork)
*   [`get /engine/instance/{EngineInstanceID}/workdetail`](#getEngineInstanceWorkDetail)
*   [`get /engine/{EngineID}/launch/{LaunchID}/detail`](#getEngineLaunchDetail)
*   [`get /engine/{EngineID}/launches`](#getEngineLaunches)
*   [`get /engines`](#getEngines)
*   [`post /engine/{EngineID}/build/{BuildID}/pause`](#pauseBuild)
*   [`post /engine/{EngineID}/pause`](#pauseEngine)
*   [`post /engine/register`](#registerEngineInstanceNoAuth)
*   [`post /engine/{EngineID}/replace`](#replaceEngine)
*   [`post /engine/{EngineID}/build/{BuildID}/resume`](#resumeBuild)
*   [`post /engine/{EngineID}/resume`](#resumeEngine)
*   [`post /engine/{EngineInstanceID}/terminate`](#terminateEngineInstance)
*   [`post /engine/{EngineID}/update`](#updateEngine)
*   [`post /engine/{EngineID}/build/{BuildID}/update`](#updateEngineBuild)
*   [`post /engine/category/{EngineCategoryID}/update`](#updateEngineCategory)
*   [`post /engine/{EngineInstanceID}/updatestatus`](#updateEngineInstanceStatus)

#### [Flow](#Flow)

*   [`post /flow/nrcontainer/create`](#createNodeRedContainerInfo)
*   [`post /flow/delete/{ContainerID}`](#deleteAutomateContainer)
*   [`post /flow/request/update/{UserID}/{Status}`](#updateAutomateRequestStatus)
*   [`post /flow/{HostID}/updatestatus`](#updateAutomateStatus)

#### [Host](#Host)

*   [`post /host/{HostID}/drain`](#drainHost)
*   [`get /host/{HostID}/detail`](#getHostDetail)
*   [`get /host/{HostID}/status`](#getHostStatus)
*   [`get /hosts`](#getHosts)
*   [`get /host/{HostID}/launch`](#getHostsLaunch)
*   [`post /host/{HostID}/pause`](#pauseHost)
*   [`post /host/{HostID}/engine/register`](#registerEngineInstance)
*   [`post /host/register`](#registerHost)
*   [`post /host/{HostID}/resume`](#resumeHost)
*   [`post /host/{HostID}/terminate`](#terminateHost)
*   [`post /host/{HostID}/updatestatus`](#updateHostStatus)

#### [Process](#Process)

*   [`post /proc/job/create`](#createJob)
*   [`post /proc/job/{JobID}/createnext`](#createNextJob)
*   [`post /proc/job/{JobID}/delete`](#deleteJob)
*   [`get /proc/job/{JobID}/detail`](#getJobDetail)
*   [`get /proc/job/{JobID}/output/{JobOutputName}`](#getJobOutput)
*   [`get /proc/job/{JobID}/outputs`](#getJobOutputs)
*   [`get /proc/job/{JobID}/status`](#getJobStatus)
*   [`get /proc/job/{JobID}/workrequests`](#getJobWorkRequests)
*   [`get /proc/jobs`](#getJobs)
*   [`get /proc/jobs/stats/organization`](#getJobsOrganizationStats)
*   [`get /proc/jobs/performance`](#getJobsPerformance)
*   [`get /proc/jobs/stats`](#getJobsStats)
*   [`get /proc/jobs/stats/time_ranges`](#getJobsTimeRangesStats)
*   [`get /proc/task/{TaskID}/detail`](#getTaskDetail)
*   [`get /proc/task/{TaskID}/logs`](#getTaskLogs)
*   [`get /proc/task/{TaskID}/output/{TaskOutputName}`](#getTaskOutput)
*   [`get /proc/task/{TaskID}/outputs`](#getTaskOutputs)
*   [`get /proc/tasks`](#getTasks)
*   [`get /proc/tasks/stats`](#getTasksStats)
*   [`get /proc/tasks/stats/engines`](#getTasksStatsEngines)
*   [`get /proc/tasks/stats/hosts`](#getTasksStatsHosts)
*   [`get /proc/tasks/stats/time_ranges`](#getTasksStatsTimeRanges)
*   [`post /proc/template/{TemplateID}/launch`](#launchJobTemplate)
*   [`post /proc/endpoint/{Endpoint}`](#pushContentToEndpoint)
*   [`get /proc/job/{JobID}/recheck_status`](#recheckJobStatus)

# <a name="Admin" id="Admin">Admin</a>

#### addserversServerType

<div class="method"><a id="addserversServerType"></a>

[Up](#__Methods)

    post /admin/server_type/{ServerTypeID}/add

</div>

<div class="method-summary">This API add servers to the specified server type (<span class="nickname">addserversServerType</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">ServerTypeID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Server Type format: uuid</div>

</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [AddServersToServerTypeRequest](#AddServersToServerTypeRequest) (optional)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — Add Servers Server Type</div>

</div>

### Request headers

### Return type

<div class="return-type">[AdminOperationResponse](#AdminOperationResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

List of engines [AdminOperationResponse](#AdminOperationResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="adminTerminateCluster" id="adminTerminateCluster"></a>

<div class="method-path">[Up](#__Methods)

    post /admin/terminate

</div>

<div class="method-summary">This terminates the cluster (<span class="nickname">adminTerminateCluster</span>)</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [AdminOperationRequest](#AdminOperationRequest) (optional)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — ClusterID</div>

</div>

### Request headers

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="applyLicense" id="applyLicense"></a>

<div class="method-path">[Up](#__Methods)

    post /admin/licenses/apply

</div>

<div class="method-summary">This applies a license to aiWARE (<span class="nickname">applyLicense</span>)</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [CreateLicenseDetail](#CreateLicenseDetail) (optional)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> —</div>

</div>

### Request headers

### Return type

<div class="return-type">[LicenseDetail](#LicenseDetail)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "licenseKey" : "licenseKey",
      "licenseExpiration" : "2018-03-20T09:12:28Z",
      "currentBytes" : 6,
      "maxTasks" : 7,
      "currentAPI" : 0,
      "maxAPI" : 5,
      "maxBytes" : 5,
      "maxHosts" : 2,
      "licenseID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
      "licenseValidation" : "licenseValidation",
      "currentTasks" : 1
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [LicenseDetail](#LicenseDetail)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="createAdminCore" id="createAdminCore"></a>

<div class="method-path">[Up](#__Methods)

    post /admin/cores/create

</div>

<div class="method-summary">This creates a new core (<span class="nickname">createAdminCore</span>)</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [AdminCoreCreateRequest](#AdminCoreCreateRequest) (required)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — The input for createCor</div>

</div>

### Request headers

### Return type

<div class="return-type">[AdminCoreCreateResponse](#AdminCoreCreateResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : {
        "baseUrl" : "http://example.com/aeiou",
        "endpoint" : "/v3/graphql",
        "scheduled" : true,
        "isEnabled" : true,
        "coreUrl" : "http://example.com/aeiou",
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "clusterID" : "clusterID",
        "coreID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "adhoc" : true,
        "token" : "token"
      },
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [AdminCoreCreateResponse](#AdminCoreCreateResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="createAdminOrganization" id="createAdminOrganization"></a>

<div class="method-path">[Up](#__Methods)

    post /admin/organizations/create

</div>

<div class="method-summary">This updates the config for the cluster for a given key (<span class="nickname">createAdminOrganization</span>)</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [AdminOrganizationCreateRequest](#AdminOrganizationCreateRequest) (required)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — The input for createOrganization</div>

</div>

### Request headers

### Return type

<div class="return-type">[AdminOrganizationCreateResponse](#AdminOrganizationCreateResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : {
        "organizationID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "coreOrganizationID" : 6,
        "name" : "name",
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "defaultRetries" : 1,
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "coreID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "applicationID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "basePriority" : 0,
        "defaultSLASeconds" : 5,
        "taskPriorityAdjustmentStarted" : 5,
        "kvpJSON" : "kvpJSON"
      },
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [AdminOrganizationCreateResponse](#AdminOrganizationCreateResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="createServerType" id="createServerType"></a>

<div class="method-path">[Up](#__Methods)

    post /admin/server_types/create

</div>

<div class="method-summary">This creates a new server type (<span class="nickname">createServerType</span>)</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [CreateServerTypeRequest](#CreateServerTypeRequest) (required)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — The input for createServerType</div>

</div>

### Request headers

### Return type

<div class="return-type">[CreateServerTypeResponse](#CreateServerTypeResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : {
        "awsSecurityGroups" : [ "awsSecurityGroups", "awsSecurityGroups" ],
        "runModes" : [ "engine", "engine" ],
        "serverConfigJSON" : "serverConfigJSON",
        "awsAmi" : "awsAmi",
        "awsUserData" : "awsUserData",
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "minServers" : 5,
        "awsInstanceProfile" : "awsInstanceProfile",
        "memoryBytes" : 1,
        "awsSpot" : true,
        "awsSubnets" : [ "awsSubnets", "awsSubnets" ],
        "agentStartupScript" : "agentStartupScript",
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "numGPU" : 5,
        "serverProvider" : "aws_ec2",
        "gpuType" : "none",
        "serverTypeID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "awsInstanceType" : "awsInstanceType",
        "awsKeyName" : "awsKeyName",
        "awsSpotPersistent" : true,
        "vcpus" : 2,
        "maxServers" : 6,
        "awsSpotMaxPrice" : 0.8008282,
        "hasGPU" : true,
        "onlyOrganizationId" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "isAutoScaleActive" : true,
        "awsTagsJSON" : "awsTagsJSON"
      },
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [CreateServerTypeResponse](#CreateServerTypeResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="createToken" id="createToken"></a>

<div class="method-path">[Up](#__Methods)

    post /admin/tokens/create

</div>

<div class="method-summary">This creates a new token (<span class="nickname">createToken</span>)</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [AdminTokenCreateRequest](#AdminTokenCreateRequest) (required)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — The input for createToken</div>

</div>

### Request headers

### Return type

<div class="return-type">[AdminTokenCreateResponse](#AdminTokenCreateResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : {
        "bytesRateLimitHour" : 6,
        "engineInstanceID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "tokenID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "maxTasks" : 5,
        "apiRateLimitHour" : 0,
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "hostID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "totalCountAPI" : 7,
        "totalCountBytes" : 9,
        "type" : "engine_instance",
        "kvpJSON" : "kvpJSON",
        "taskRateLimitHour" : 2,
        "organizationIDs" : [ "046b6c7f-0b8a-43b9-b35d-6489e6daee91", "046b6c7f-0b8a-43b9-b35d-6489e6daee91" ],
        "maxAPI" : 1,
        "totalCountTasks" : 3,
        "expiration" : "2018-03-20T09:12:28Z",
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "maxBytes" : 5
      },
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [AdminTokenCreateResponse](#AdminTokenCreateResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="createUser" id="createUser"></a>

<div class="method-path">[Up](#__Methods)

    post /admin/users/create

</div>

<div class="method-summary">This creates a new user (<span class="nickname">createUser</span>)</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [AdminUserCreateRequest](#AdminUserCreateRequest) (required)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — The input for createUser</div>

</div>

### Request headers

### Return type

<div class="return-type">[AdminUserCreateResponse](#AdminUserCreateResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : {
        "passwordChangeRequired" : true,
        "userSettingsJSON" : "userSettingsJSON",
        "internalOrganizationID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "displayName" : "displayName",
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "userName" : "userName",
        "userID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "kvpJSON" : "kvpJSON",
        "datePasswordLastUpdated" : "2018-03-20T09:12:28Z",
        "createdBy" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "lastLoggedIn" : "2018-03-20T09:12:28Z",
        "modifiedBy" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "email" : "",
        "status" : "active"
      },
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [AdminUserCreateResponse](#AdminUserCreateResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="deleteLicense" id="deleteLicense"></a>

<div class="method-path">[Up](#__Methods)

    delete /admin/licenses/{LicenseID}/delete

</div>

<div class="method-summary">This deletes a license from aiWARE (<span class="nickname">deleteLicense</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">LicenseID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — License ID</div>

</div>

### Request headers

### Return type

<div class="return-type">[AdminOperationResponse](#AdminOperationResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [AdminOperationResponse](#AdminOperationResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="deleteServerType" id="deleteServerType"></a>

<div class="method-path">[Up](#__Methods)

    delete /admin/server_type/{ServerTypeID}/delete

</div>

<div class="method-summary">This API deletes the specified server type (<span class="nickname">deleteServerType</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">ServerTypeID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Server Type format: uuid</div>

</div>

### Request headers

### Return type

<div class="return-type">[AdminOperationResponse](#AdminOperationResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Delete a particular server type [AdminOperationResponse](#AdminOperationResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="deleteServerTypePost" id="deleteServerTypePost"></a>

<div class="method-path">[Up](#__Methods)

    post /admin/server_type/{ServerTypeID}/delete

</div>

<div class="method-summary">This API deletes the specified server type (<span class="nickname">deleteServerTypePost</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">ServerTypeID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Server Type format: uuid</div>

</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [DeleteServerTypeRequest](#DeleteServerTypeRequest) (optional)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — Engine Instance Info</div>

</div>

### Request headers

### Return type

<div class="return-type">[AdminOperationResponse](#AdminOperationResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 204

Delete a particular engine [AdminOperationResponse](#AdminOperationResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="desiredserversServerType" id="desiredserversServerType"></a>

<div class="method-path">[Up](#__Methods)

    post /admin/server_type/{ServerTypeID}/desired

</div>

<div class="method-summary">This API add servers to the specified server type (<span class="nickname">desiredserversServerType</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">ServerTypeID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Server Type format: uuid</div>

</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [DesiredServersToServerTypeRequest](#DesiredServersToServerTypeRequest) (optional)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — Set Servers for Server Type</div>

</div>

### Request headers

### Return type

<div class="return-type">[AdminOperationResponse](#AdminOperationResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Response to operation [AdminOperationResponse](#AdminOperationResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getAdminCoreDetail" id="getAdminCoreDetail"></a>

<div class="method-path">[Up](#__Methods)

    get /admin/core/{CoreID}/detail

</div>

<div class="method-summary">This provides information on the given core. (<span class="nickname">getAdminCoreDetail</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">CoreID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Core format: uuid</div>

</div>

### Request headers

### Return type

<div class="return-type">[AdminCoreGetDetailResponse](#AdminCoreGetDetailResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : {
        "baseUrl" : "http://example.com/aeiou",
        "endpoint" : "/v3/graphql",
        "scheduled" : true,
        "isEnabled" : true,
        "coreUrl" : "http://example.com/aeiou",
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "clusterID" : "clusterID",
        "coreID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "adhoc" : true,
        "token" : "token"
      },
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [AdminCoreGetDetailResponse](#AdminCoreGetDetailResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getAdminCores" id="getAdminCores"></a>

<div class="method-path">[Up](#__Methods)

    get /admin/cores

</div>

<div class="method-summary">This provides a list of core systems (<span class="nickname">getAdminCores</span>)</div>

### Request headers

### Return type

<div class="return-type">[GetCoresResponse](#GetCoresResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : [ {
        "baseUrl" : "http://example.com/aeiou",
        "endpoint" : "/v3/graphql",
        "scheduled" : true,
        "isEnabled" : true,
        "coreUrl" : "http://example.com/aeiou",
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "clusterID" : "clusterID",
        "coreID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "adhoc" : true,
        "token" : "token"
      }, {
        "baseUrl" : "http://example.com/aeiou",
        "endpoint" : "/v3/graphql",
        "scheduled" : true,
        "isEnabled" : true,
        "coreUrl" : "http://example.com/aeiou",
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "clusterID" : "clusterID",
        "coreID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "adhoc" : true,
        "token" : "token"
      } ],
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [GetCoresResponse](#GetCoresResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getAdminOrganizationDetail" id="getAdminOrganizationDetail"></a>

<div class="method-path">[Up](#__Methods)

    get /admin/organization/{OrganizationID}/detail

</div>

<div class="method-summary">This updates the config for the cluster for a given key (<span class="nickname">getAdminOrganizationDetail</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">OrganizationID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Organization format: uuid</div>

</div>

### Request headers

### Return type

<div class="return-type">[AdminOrganizationGetDetailResponse](#AdminOrganizationGetDetailResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : {
        "organizationID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "coreOrganizationID" : 6,
        "name" : "name",
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "defaultRetries" : 1,
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "coreID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "applicationID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "basePriority" : 0,
        "defaultSLASeconds" : 5,
        "taskPriorityAdjustmentStarted" : 5,
        "kvpJSON" : "kvpJSON"
      },
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [AdminOrganizationGetDetailResponse](#AdminOrganizationGetDetailResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getAdminOrganizationTokens" id="getAdminOrganizationTokens"></a>

<div class="method-path">[Up](#__Methods)

    get /admin/organization/{OrganizationID}/tokens

</div>

<div class="method-summary">This provides information on the given organization tokens. (<span class="nickname">getAdminOrganizationTokens</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">OrganizationID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Organization format: uuid</div>

</div>

### Request headers

### Return type

<div class="return-type">[AdminOrganizationGetTokensResponse](#AdminOrganizationGetTokensResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : [ {
        "bytesRateLimitHour" : 6,
        "engineInstanceID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "tokenID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "maxTasks" : 5,
        "apiRateLimitHour" : 0,
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "hostID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "totalCountAPI" : 7,
        "totalCountBytes" : 9,
        "type" : "engine_instance",
        "kvpJSON" : "kvpJSON",
        "taskRateLimitHour" : 2,
        "organizationIDs" : [ "046b6c7f-0b8a-43b9-b35d-6489e6daee91", "046b6c7f-0b8a-43b9-b35d-6489e6daee91" ],
        "maxAPI" : 1,
        "totalCountTasks" : 3,
        "expiration" : "2018-03-20T09:12:28Z",
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "maxBytes" : 5
      }, {
        "bytesRateLimitHour" : 6,
        "engineInstanceID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "tokenID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "maxTasks" : 5,
        "apiRateLimitHour" : 0,
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "hostID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "totalCountAPI" : 7,
        "totalCountBytes" : 9,
        "type" : "engine_instance",
        "kvpJSON" : "kvpJSON",
        "taskRateLimitHour" : 2,
        "organizationIDs" : [ "046b6c7f-0b8a-43b9-b35d-6489e6daee91", "046b6c7f-0b8a-43b9-b35d-6489e6daee91" ],
        "maxAPI" : 1,
        "totalCountTasks" : 3,
        "expiration" : "2018-03-20T09:12:28Z",
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "maxBytes" : 5
      } ],
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [AdminOrganizationGetTokensResponse](#AdminOrganizationGetTokensResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getAdminOrganizations" id="getAdminOrganizations"></a>

<div class="method-path">[Up](#__Methods)

    get /admin/organizations

</div>

<div class="method-summary">This provides a list of organizations (<span class="nickname">getAdminOrganizations</span>)</div>

### Request headers

### Return type

<div class="return-type">[AdminOrganizationsGetResponse](#AdminOrganizationsGetResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : [ {
        "organizationID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "coreOrganizationID" : 6,
        "name" : "name",
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "defaultRetries" : 1,
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "coreID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "applicationID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "basePriority" : 0,
        "defaultSLASeconds" : 5,
        "taskPriorityAdjustmentStarted" : 5,
        "kvpJSON" : "kvpJSON"
      }, {
        "organizationID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "coreOrganizationID" : 6,
        "name" : "name",
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "defaultRetries" : 1,
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "coreID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "applicationID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "basePriority" : 0,
        "defaultSLASeconds" : 5,
        "taskPriorityAdjustmentStarted" : 5,
        "kvpJSON" : "kvpJSON"
      } ],
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [AdminOrganizationsGetResponse](#AdminOrganizationsGetResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getAdminStatus" id="getAdminStatus"></a>

<div class="method-path">[Up](#__Methods)

    get /admin/status

</div>

<div class="method-summary">This provides information on the status of the aiWARE edge (<span class="nickname">getAdminStatus</span>)</div>

### Request headers

### Query parameters

<div class="field-items">

<div class="param">format (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — If specified, this limits the jobs or tasks to follow status</div>

</div>

### Return type

<div class="return-type">[EngineInstanceInfo](#EngineInstanceInfo)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "runtimeExpirationSeconds" : 6,
      "engineInstanceID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
      "engineToolkitVersion" : "engineToolkitVersion",
      "dockerContainerID" : "dockerContainerID",
      "licenseExpirationSeconds" : 0,
      "launchStatus" : "pending",
      "warnings" : [ null, null ],
      "hostID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
      "additionalEngineIDs" : [ "additionalEngineIDs", "additionalEngineIDs" ],
      "buildID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
      "startupTimestamp" : 1,
      "launchID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
      "launchStatusInfo" : "launchStatusInfo",
      "errors" : [ {
        "errorDescription" : "errorDescription",
        "errorDetail" : "errorDetail",
        "errorId" : "errorId"
      }, {
        "errorDescription" : "errorDescription",
        "errorDetail" : "errorDetail",
        "errorId" : "errorId"
      } ],
      "engineID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
      "launchEnvVariables" : { },
      "status" : "active"
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`
*   `text/csv`
*   `text/html`
*   `text/plain`

### Responses

#### 200

Successful operation [EngineInstanceInfo](#EngineInstanceInfo)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getAdminUserDetail" id="getAdminUserDetail"></a>

<div class="method-path">[Up](#__Methods)

    get /admin/user/{UserID}/detail

</div>

<div class="method-summary">This provides information on the given user. (<span class="nickname">getAdminUserDetail</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">UserID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of User format: uuid</div>

</div>

### Request headers

### Return type

<div class="return-type">[AdminUserGetDetailResponse](#AdminUserGetDetailResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : {
        "passwordChangeRequired" : true,
        "userSettingsJSON" : "userSettingsJSON",
        "internalOrganizationID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "displayName" : "displayName",
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "userName" : "userName",
        "userID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "kvpJSON" : "kvpJSON",
        "datePasswordLastUpdated" : "2018-03-20T09:12:28Z",
        "createdBy" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "lastLoggedIn" : "2018-03-20T09:12:28Z",
        "modifiedBy" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "email" : "",
        "status" : "active"
      },
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [AdminUserGetDetailResponse](#AdminUserGetDetailResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method-path">

<div class="method"><a name="getAdminUserTokens" id="getAdminUserTokens"></a>[Up](#__Methods)

    get /admin/user/{UserID}/tokens

</div>

<div class="method-summary">This provides information on the given user. (<span class="nickname">getAdminUserTokens</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">UserID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of User format: uuid</div>

</div>

### Request headers

### Return type

<div class="return-type">[AdminUserGetTokensResponse](#AdminUserGetTokensResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : [ {
        "bytesRateLimitHour" : 6,
        "engineInstanceID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "tokenID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "maxTasks" : 5,
        "apiRateLimitHour" : 0,
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "hostID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "totalCountAPI" : 7,
        "totalCountBytes" : 9,
        "type" : "engine_instance",
        "kvpJSON" : "kvpJSON",
        "taskRateLimitHour" : 2,
        "organizationIDs" : [ "046b6c7f-0b8a-43b9-b35d-6489e6daee91", "046b6c7f-0b8a-43b9-b35d-6489e6daee91" ],
        "maxAPI" : 1,
        "totalCountTasks" : 3,
        "expiration" : "2018-03-20T09:12:28Z",
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "maxBytes" : 5
      }, {
        "bytesRateLimitHour" : 6,
        "engineInstanceID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "tokenID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "maxTasks" : 5,
        "apiRateLimitHour" : 0,
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "hostID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "totalCountAPI" : 7,
        "totalCountBytes" : 9,
        "type" : "engine_instance",
        "kvpJSON" : "kvpJSON",
        "taskRateLimitHour" : 2,
        "organizationIDs" : [ "046b6c7f-0b8a-43b9-b35d-6489e6daee91", "046b6c7f-0b8a-43b9-b35d-6489e6daee91" ],
        "maxAPI" : 1,
        "totalCountTasks" : 3,
        "expiration" : "2018-03-20T09:12:28Z",
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "maxBytes" : 5
      } ],
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [AdminUserGetTokensResponse](#AdminUserGetTokensResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getAdminUsers" id="getAdminUsers"></a>

<div class="method-path">[Up](#__Methods)

    get /admin/users

</div>

<div class="method-summary">This provides a list of users in the system (<span class="nickname">getAdminUsers</span>)</div>

### Request headers

### Query parameters

<div class="field-items">

<div class="param">offset (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — the number of users to skip before getting the result set</div>

<div class="param">limit (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — the number of users to return.</div>

<div class="param">orderBy (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — the field to sort</div>

<div class="param">direction (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — the sort order</div>

<div class="param">status (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — the value should be in [active, trial, inactive, deleted]</div>

<div class="param">name (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — Name of user</div>

<div class="param">userName (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — userName of user</div>

<div class="param">email (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — email of user</div>

</div>

### Return type

<div class="return-type">[AdminUsersGetResponse](#AdminUsersGetResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : [ {
        "passwordChangeRequired" : true,
        "userSettingsJSON" : "userSettingsJSON",
        "internalOrganizationID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "displayName" : "displayName",
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "userName" : "userName",
        "userID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "kvpJSON" : "kvpJSON",
        "datePasswordLastUpdated" : "2018-03-20T09:12:28Z",
        "createdBy" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "lastLoggedIn" : "2018-03-20T09:12:28Z",
        "modifiedBy" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "email" : "",
        "status" : "active"
      }, {
        "passwordChangeRequired" : true,
        "userSettingsJSON" : "userSettingsJSON",
        "internalOrganizationID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "displayName" : "displayName",
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "userName" : "userName",
        "userID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "kvpJSON" : "kvpJSON",
        "datePasswordLastUpdated" : "2018-03-20T09:12:28Z",
        "createdBy" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "lastLoggedIn" : "2018-03-20T09:12:28Z",
        "modifiedBy" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "email" : "",
        "status" : "active"
      } ],
      "offset" : 1,
      "success" : true,
      "count" : 0,
      "limit" : 6
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [AdminUsersGetResponse](#AdminUsersGetResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getConfig" id="getConfig"></a>

<div class="method-path">[Up](#__Methods)

    get /admin/config

</div>

<div class="method-summary">This provides all the config for the cluster (<span class="nickname">getConfig</span>)</div>

### Request headers

### Return type

<div class="return-type">[AdminConfigResponse](#AdminConfigResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : [ {
        "keys" : [ {
          "createdDateTime" : "2018-03-20T09:12:28Z",
          "modifiedDateTime" : "2018-03-20T09:12:28Z",
          "section" : "section",
          "value" : "value",
          "key" : "key",
          "kvpJSON" : "kvpJSON"
        }, {
          "createdDateTime" : "2018-03-20T09:12:28Z",
          "modifiedDateTime" : "2018-03-20T09:12:28Z",
          "section" : "section",
          "value" : "value",
          "key" : "key",
          "kvpJSON" : "kvpJSON"
        } ],
        "section" : "section"
      }, {
        "keys" : [ {
          "createdDateTime" : "2018-03-20T09:12:28Z",
          "modifiedDateTime" : "2018-03-20T09:12:28Z",
          "section" : "section",
          "value" : "value",
          "key" : "key",
          "kvpJSON" : "kvpJSON"
        }, {
          "createdDateTime" : "2018-03-20T09:12:28Z",
          "modifiedDateTime" : "2018-03-20T09:12:28Z",
          "section" : "section",
          "value" : "value",
          "key" : "key",
          "kvpJSON" : "kvpJSON"
        } ],
        "section" : "section"
      } ],
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [AdminConfigResponse](#AdminConfigResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getConfigSection" id="getConfigSection"></a>

<div class="method-path">[Up](#__Methods)

    get /admin/config/{ConfigSection}

</div>

<div class="method-summary">This provides all the config for the cluster (<span class="nickname">getConfigSection</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">ConfigSection (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — Config Section Entry</div>

</div>

### Request headers

### Return type

<div class="return-type">[AdminConfigSectionResponse](#AdminConfigSectionResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : {
        "keys" : [ {
          "createdDateTime" : "2018-03-20T09:12:28Z",
          "modifiedDateTime" : "2018-03-20T09:12:28Z",
          "section" : "section",
          "value" : "value",
          "key" : "key",
          "kvpJSON" : "kvpJSON"
        }, {
          "createdDateTime" : "2018-03-20T09:12:28Z",
          "modifiedDateTime" : "2018-03-20T09:12:28Z",
          "section" : "section",
          "value" : "value",
          "key" : "key",
          "kvpJSON" : "kvpJSON"
        } ],
        "section" : "section"
      },
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [AdminConfigSectionResponse](#AdminConfigSectionResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getConfigSectionKey" id="getConfigSectionKey"></a>

<div class="method-path">[Up](#__Methods)

    get /admin/config/{ConfigSection}/{ConfigKey}

</div>

<div class="method-summary">This provides a config section key for the cluster (<span class="nickname">getConfigSectionKey</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">ConfigSection (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — Config Section Entry</div>

<div class="param">ConfigKey (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — Config Key</div>

</div>

### Request headers

### Return type

<div class="return-type">[AdminConfigSectionKeyResponse](#AdminConfigSectionKeyResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : "result",
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`
*   `text/csv`
*   `text/html`
*   `text/plain`

### Responses

#### 200

Successful operation [AdminConfigSectionKeyResponse](#AdminConfigSectionKeyResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getLicenseDetail" id="getLicenseDetail"></a>

<div class="method-path">[Up](#__Methods)

    get /admin/licenses/{LicenseID}/detail

</div>

<div class="method-summary">This gets detail on a license key (<span class="nickname">getLicenseDetail</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">LicenseID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — License ID</div>

</div>

### Request headers

### Return type

<div class="return-type">[LicenseDetail](#LicenseDetail)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "licenseKey" : "licenseKey",
      "licenseExpiration" : "2018-03-20T09:12:28Z",
      "currentBytes" : 6,
      "maxTasks" : 7,
      "currentAPI" : 0,
      "maxAPI" : 5,
      "maxBytes" : 5,
      "maxHosts" : 2,
      "licenseID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
      "licenseValidation" : "licenseValidation",
      "currentTasks" : 1
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [LicenseDetail](#LicenseDetail)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getLicenses" id="getLicenses"></a>

<div class="method-path">[Up](#__Methods)

    get /admin/licenses

</div>

<div class="method-summary">This provides a licenses on the system (<span class="nickname">getLicenses</span>)</div>

### Request headers

### Return type

<div class="return-type">[GetLicensesResponse](#GetLicensesResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : [ {
        "licenseKey" : "licenseKey",
        "licenseExpiration" : "2018-03-20T09:12:28Z",
        "currentBytes" : 6,
        "maxTasks" : 7,
        "currentAPI" : 0,
        "maxAPI" : 5,
        "maxBytes" : 5,
        "maxHosts" : 2,
        "licenseID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "licenseValidation" : "licenseValidation",
        "currentTasks" : 1
      }, {
        "licenseKey" : "licenseKey",
        "licenseExpiration" : "2018-03-20T09:12:28Z",
        "currentBytes" : 6,
        "maxTasks" : 7,
        "currentAPI" : 0,
        "maxAPI" : 5,
        "maxBytes" : 5,
        "maxHosts" : 2,
        "licenseID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "licenseValidation" : "licenseValidation",
        "currentTasks" : 1
      } ],
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [GetLicensesResponse](#GetLicensesResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getServerType" id="getServerType"></a>

<div class="method-path">[Up](#__Methods)

    get /admin/server_type/{ServerTypeID}/detail

</div>

<div class="method-summary">This provides detail on the server type (<span class="nickname">getServerType</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">ServerTypeID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Server Type format: uuid</div>

</div>

### Request headers

### Return type

<div class="return-type">[GetServerTypeResponse](#GetServerTypeResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : {
        "awsSecurityGroups" : [ "awsSecurityGroups", "awsSecurityGroups" ],
        "runModes" : [ "engine", "engine" ],
        "serverConfigJSON" : "serverConfigJSON",
        "awsAmi" : "awsAmi",
        "awsUserData" : "awsUserData",
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "minServers" : 5,
        "awsInstanceProfile" : "awsInstanceProfile",
        "memoryBytes" : 1,
        "awsSpot" : true,
        "awsSubnets" : [ "awsSubnets", "awsSubnets" ],
        "agentStartupScript" : "agentStartupScript",
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "numGPU" : 5,
        "serverProvider" : "aws_ec2",
        "gpuType" : "none",
        "serverTypeID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "awsInstanceType" : "awsInstanceType",
        "awsKeyName" : "awsKeyName",
        "awsSpotPersistent" : true,
        "vcpus" : 2,
        "maxServers" : 6,
        "awsSpotMaxPrice" : 0.8008282,
        "hasGPU" : true,
        "onlyOrganizationId" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "isAutoScaleActive" : true,
        "awsTagsJSON" : "awsTagsJSON"
      },
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [GetServerTypeResponse](#GetServerTypeResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getServerTypes" id="getServerTypes"></a>

<div class="method-path">[Up](#__Methods)

    get /admin/server_types

</div>

<div class="method-summary">This lists the server types available on the system (<span class="nickname">getServerTypes</span>)</div>

### Request headers

### Return type

<div class="return-type">[GetServerTypesResponse](#GetServerTypesResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : [ {
        "awsSecurityGroups" : [ "awsSecurityGroups", "awsSecurityGroups" ],
        "runModes" : [ "engine", "engine" ],
        "serverConfigJSON" : "serverConfigJSON",
        "awsAmi" : "awsAmi",
        "awsUserData" : "awsUserData",
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "minServers" : 5,
        "awsInstanceProfile" : "awsInstanceProfile",
        "memoryBytes" : 1,
        "awsSpot" : true,
        "awsSubnets" : [ "awsSubnets", "awsSubnets" ],
        "agentStartupScript" : "agentStartupScript",
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "numGPU" : 5,
        "serverProvider" : "aws_ec2",
        "gpuType" : "none",
        "serverTypeID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "awsInstanceType" : "awsInstanceType",
        "awsKeyName" : "awsKeyName",
        "awsSpotPersistent" : true,
        "vcpus" : 2,
        "maxServers" : 6,
        "awsSpotMaxPrice" : 0.8008282,
        "hasGPU" : true,
        "onlyOrganizationId" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "isAutoScaleActive" : true,
        "awsTagsJSON" : "awsTagsJSON"
      }, {
        "awsSecurityGroups" : [ "awsSecurityGroups", "awsSecurityGroups" ],
        "runModes" : [ "engine", "engine" ],
        "serverConfigJSON" : "serverConfigJSON",
        "awsAmi" : "awsAmi",
        "awsUserData" : "awsUserData",
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "minServers" : 5,
        "awsInstanceProfile" : "awsInstanceProfile",
        "memoryBytes" : 1,
        "awsSpot" : true,
        "awsSubnets" : [ "awsSubnets", "awsSubnets" ],
        "agentStartupScript" : "agentStartupScript",
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "numGPU" : 5,
        "serverProvider" : "aws_ec2",
        "gpuType" : "none",
        "serverTypeID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "awsInstanceType" : "awsInstanceType",
        "awsKeyName" : "awsKeyName",
        "awsSpotPersistent" : true,
        "vcpus" : 2,
        "maxServers" : 6,
        "awsSpotMaxPrice" : 0.8008282,
        "hasGPU" : true,
        "onlyOrganizationId" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "isAutoScaleActive" : true,
        "awsTagsJSON" : "awsTagsJSON"
      } ],
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [GetServerTypesResponse](#GetServerTypesResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="loginUser" id="loginUser"></a>

<div class="method-path">[Up](#__Methods)

    post /admin/users/login

</div>

<div class="method-summary">This logs a user in if successful (<span class="nickname">loginUser</span>)</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [AdminUserLoginRequest](#AdminUserLoginRequest) (optional)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — This logs in the user</div>

</div>

### Request headers

### Return type

<div class="return-type">[AdminUserLoginResponse](#AdminUserLoginResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : {
        "passwordChangeRequired" : true,
        "userSettingsJSON" : "userSettingsJSON",
        "internalOrganizationID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "displayName" : "displayName",
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "userName" : "userName",
        "userID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "kvpJSON" : "kvpJSON",
        "datePasswordLastUpdated" : "2018-03-20T09:12:28Z",
        "createdBy" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "lastLoggedIn" : "2018-03-20T09:12:28Z",
        "modifiedBy" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "email" : "",
        "status" : "active"
      },
      "success" : true,
      "token" : "token"
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [AdminUserLoginResponse](#AdminUserLoginResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="removeserversServerType" id="removeserversServerType"></a>

<div class="method-path">[Up](#__Methods)

    post /admin/server_type/{ServerTypeID}/remove

</div>

<div class="method-summary">This API removes servers from the specified server type (<span class="nickname">removeserversServerType</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">ServerTypeID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Server Type format: uuid</div>

</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [RemoveServersToServerTypeRequest](#RemoveServersToServerTypeRequest) (optional)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — Update Server Type</div>

</div>

### Request headers

### Return type

<div class="return-type">[AdminOperationResponse](#AdminOperationResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

List of engines [AdminOperationResponse](#AdminOperationResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="updateConfigAll" id="updateConfigAll"></a>

<div class="method-path">[Up](#__Methods)

    post /admin/config

</div>

<div class="method-summary">This gets the config for the cluster (<span class="nickname">updateConfigAll</span>)</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [AdminConfigUpdateRequest](#AdminConfigUpdateRequest) (required)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — Config Update for core</div>

</div>

### Request headers

### Return type

<div class="return-type">[AdminConfigUpdateResponse](#AdminConfigUpdateResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : [ {
        "keys" : [ {
          "createdDateTime" : "2018-03-20T09:12:28Z",
          "modifiedDateTime" : "2018-03-20T09:12:28Z",
          "section" : "section",
          "value" : "value",
          "key" : "key",
          "kvpJSON" : "kvpJSON"
        }, {
          "createdDateTime" : "2018-03-20T09:12:28Z",
          "modifiedDateTime" : "2018-03-20T09:12:28Z",
          "section" : "section",
          "value" : "value",
          "key" : "key",
          "kvpJSON" : "kvpJSON"
        } ],
        "section" : "section"
      }, {
        "keys" : [ {
          "createdDateTime" : "2018-03-20T09:12:28Z",
          "modifiedDateTime" : "2018-03-20T09:12:28Z",
          "section" : "section",
          "value" : "value",
          "key" : "key",
          "kvpJSON" : "kvpJSON"
        }, {
          "createdDateTime" : "2018-03-20T09:12:28Z",
          "modifiedDateTime" : "2018-03-20T09:12:28Z",
          "section" : "section",
          "value" : "value",
          "key" : "key",
          "kvpJSON" : "kvpJSON"
        } ],
        "section" : "section"
      } ],
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [AdminConfigUpdateResponse](#AdminConfigUpdateResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="updateConfigSection" id="updateConfigSection"></a>

<div class="method-path">[Up](#__Methods)

    post /admin/config/{ConfigSection}

</div>

<div class="method-summary">This gets the config for the cluster (<span class="nickname">updateConfigSection</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">ConfigSection (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — Config Section Entry</div>

</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [AdminConfigUpdateSectionRequest](#AdminConfigUpdateSectionRequest) (required)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — The input for createConfigSection</div>

</div>

### Request headers

### Return type

<div class="return-type">[AdminConfigUpdateSectionResponse](#AdminConfigUpdateSectionResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : {
        "keys" : [ {
          "createdDateTime" : "2018-03-20T09:12:28Z",
          "modifiedDateTime" : "2018-03-20T09:12:28Z",
          "section" : "section",
          "value" : "value",
          "key" : "key",
          "kvpJSON" : "kvpJSON"
        }, {
          "createdDateTime" : "2018-03-20T09:12:28Z",
          "modifiedDateTime" : "2018-03-20T09:12:28Z",
          "section" : "section",
          "value" : "value",
          "key" : "key",
          "kvpJSON" : "kvpJSON"
        } ],
        "section" : "section"
      },
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`
*   `text/csv`
*   `text/html`
*   `text/plain`

### Responses

#### 200

Successful operation [AdminConfigUpdateSectionResponse](#AdminConfigUpdateSectionResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="updateConfigSectionKey" id="updateConfigSectionKey"></a>

<div class="method-path">[Up](#__Methods)

    post /admin/config/{ConfigSection}/{ConfigKey}

</div>

<div class="method-summary">This updates the config for the cluster for a given key (<span class="nickname">updateConfigSectionKey</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">ConfigSection (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — Config Section Entry</div>

<div class="param">ConfigKey (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — Config Key</div>

</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [AdminConfigUpdateSectionKeyRequest](#AdminConfigUpdateSectionKeyRequest) (required)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — The input for createSectionKey</div>

</div>

### Request headers

### Return type

<div class="return-type">[AdminConfigUpdateSectionKeyResponse](#AdminConfigUpdateSectionKeyResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : {
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "section" : "section",
        "value" : "value",
        "key" : "key",
        "kvpJSON" : "kvpJSON"
      },
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`
*   `text/csv`
*   `text/html`
*   `text/plain`

### Responses

#### 200

Successful operation [AdminConfigUpdateSectionKeyResponse](#AdminConfigUpdateSectionKeyResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="updateServerType" id="updateServerType"></a>

<div class="method-path">[Up](#__Methods)

    post /admin/server_type/{ServerTypeID}/update

</div>

<div class="method-summary">This API updates the specified server type (<span class="nickname">updateServerType</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">ServerTypeID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Server Type format: uuid</div>

</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [ServerTypeDetail](#ServerTypeDetail) (optional)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — Update Server Type</div>

</div>

### Request headers

### Return type

<div class="return-type">[UpdateServerTypeResponse](#UpdateServerTypeResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : {
        "awsSecurityGroups" : [ "awsSecurityGroups", "awsSecurityGroups" ],
        "runModes" : [ "engine", "engine" ],
        "serverConfigJSON" : "serverConfigJSON",
        "awsAmi" : "awsAmi",
        "awsUserData" : "awsUserData",
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "minServers" : 5,
        "awsInstanceProfile" : "awsInstanceProfile",
        "memoryBytes" : 1,
        "awsSpot" : true,
        "awsSubnets" : [ "awsSubnets", "awsSubnets" ],
        "agentStartupScript" : "agentStartupScript",
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "numGPU" : 5,
        "serverProvider" : "aws_ec2",
        "gpuType" : "none",
        "serverTypeID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "awsInstanceType" : "awsInstanceType",
        "awsKeyName" : "awsKeyName",
        "awsSpotPersistent" : true,
        "vcpus" : 2,
        "maxServers" : 6,
        "awsSpotMaxPrice" : 0.8008282,
        "hasGPU" : true,
        "onlyOrganizationId" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "isAutoScaleActive" : true,
        "awsTagsJSON" : "awsTagsJSON"
      },
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

List of engines [UpdateServerTypeResponse](#UpdateServerTypeResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

# <a name="Engine" id="Engine">Engine</a>

<div class="method"><a name="createEngine" id="createEngine"></a>

<div class="method-path">[Up](#__Methods)

    post /engine/create

</div>

<div class="method-summary">This API creates a new engine (<span class="nickname">createEngine</span>)</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [CreateEngineRequest](#CreateEngineRequest) (required)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — The fields for an engine</div>

</div>

### Request headers

### Return type

<div class="return-type">[CreateEngineResponse](#CreateEngineResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : {
        "dependencyJSON" : "dependencyJSON",
        "parentCompleteBeforeStart" : true,
        "replacementEngineID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "internalOrganizationID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "dontrunComplete" : true,
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "fieldsJSON" : "fieldsJSON",
        "edge_version" : 6,
        "engineCategoryID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "priority_adjustment" : 1,
        "validationJSON" : "validationJSON",
        "applicationIDsJSON" : "applicationIDsJSON",
        "child_priority_adjustment_on_complete" : 0,
        "engineState" : "active",
        "parallelProcessing" : true,
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "engineName" : "engineName",
        "jwtRightsJSON" : "jwtRightsJSON",
        "engineID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "engineOutputType" : "chunk"
      },
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Result of the Create Engine API [CreateEngineResponse](#CreateEngineResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="createEngineCategory" id="createEngineCategory"></a>

<div class="method-path">[Up](#__Methods)

    post /engine/category/create

</div>

<div class="method-summary">This API creates a new engine category (<span class="nickname">createEngineCategory</span>)</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [CreateEngineCategoryDetail](#CreateEngineCategoryDetail) (required)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — The fields for an engine category</div>

</div>

### Request headers

### Return type

<div class="return-type">[CreateEngineCategoryResponse](#CreateEngineCategoryResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : {
        "engineCategoryName" : "engineCategoryName",
        "engineCategoryType" : "engineCategoryType",
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "engineCategoryID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91"
      },
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Result of the Create Engine Category API [CreateEngineCategoryResponse](#CreateEngineCategoryResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="deleteBuildPost" id="deleteBuildPost"></a>

<div class="method-path">[Up](#__Methods)

    post /engine/{EngineID}/build/{BuildID}/delete

</div>

<div class="method-summary">This API provides the engine detail result (<span class="nickname">deleteBuildPost</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">EngineID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Engine format: uuid</div>

<div class="param">BuildID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Build format: uuid</div>

</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [DeleteBuildRequest](#DeleteBuildRequest) (optional)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — This deleted a particular build</div>

</div>

### Request headers

### Return type

<div class="return-type">[AdminOperationResponse](#AdminOperationResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 204

Delete a particular engine [AdminOperationResponse](#AdminOperationResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="deleteEnginePost" id="deleteEnginePost"></a>

<div class="method-path">[Up](#__Methods)

    post /engine/{EngineID}/delete

</div>

<div class="method-summary">This API provides the engine detail result (<span class="nickname">deleteEnginePost</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">EngineID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Engine format: uuid</div>

</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [DeleteEngineRequest](#DeleteEngineRequest) (optional)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — Engine Instance Info</div>

</div>

### Request headers

### Return type

<div class="return-type">[AdminOperationResponse](#AdminOperationResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 204

Delete a particular engine [AdminOperationResponse](#AdminOperationResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getEngineBuild" id="getEngineBuild"></a>

<div class="method-path">[Up](#__Methods)

    get /engine/{EngineID}/build/{BuildID}

</div>

<div class="method-summary">This gets a particular build (<span class="nickname">getEngineBuild</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">EngineID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Engine format: uuid</div>

<div class="param">BuildID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Build format: uuid</div>

</div>

### Request headers

### Return type

<div class="return-type">[GetEngineBuildResponse](#GetEngineBuildResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : {
        "dockerImage" : "dockerImage",
        "manifestClusterSize" : "manifestClusterSize",
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "softMemoryBytesLimit" : 5,
        "buildID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "softVCPULimit" : 2,
        "version" : 7,
        "buildState" : "buildState",
        "manifestCustomProfile" : "manifestCustomProfile",
        "manifestEngineName" : "manifestEngineName",
        "manifestGPUSupported" : "none",
        "manifestRequireEC2" : true,
        "licenseExpirationTimestamp" : 1,
        "softGPULimit" : 5,
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "manifestEngineMode" : "manifestEngineMode",
        "diskFreeBytes" : 6,
        "buildDefaultTTL" : 0,
        "engineID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91"
      },
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Specific build [GetEngineBuildResponse](#GetEngineBuildResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getEngineBuilds" id="getEngineBuilds"></a>

<div class="method-path">[Up](#__Methods)

    get /engine/{EngineID}/builds

</div>

<div class="method-summary">Get the list of builds deployed and available on aiWARE for a particular engine (<span class="nickname">getEngineBuilds</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">EngineID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Engine format: uuid</div>

</div>

### Request headers

### Query parameters

<div class="field-items">

<div class="param">BuildState (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — Filter builds by the build state</div>

</div>

### Return type

<div class="return-type">[GetEngineBuildsResponse](#GetEngineBuildsResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : [ {
        "dockerImage" : "dockerImage",
        "manifestClusterSize" : "manifestClusterSize",
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "softMemoryBytesLimit" : 5,
        "buildID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "softVCPULimit" : 2,
        "version" : 7,
        "buildState" : "buildState",
        "manifestCustomProfile" : "manifestCustomProfile",
        "manifestEngineName" : "manifestEngineName",
        "manifestGPUSupported" : "none",
        "manifestRequireEC2" : true,
        "licenseExpirationTimestamp" : 1,
        "softGPULimit" : 5,
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "manifestEngineMode" : "manifestEngineMode",
        "diskFreeBytes" : 6,
        "buildDefaultTTL" : 0,
        "engineID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91"
      }, {
        "dockerImage" : "dockerImage",
        "manifestClusterSize" : "manifestClusterSize",
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "softMemoryBytesLimit" : 5,
        "buildID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "softVCPULimit" : 2,
        "version" : 7,
        "buildState" : "buildState",
        "manifestCustomProfile" : "manifestCustomProfile",
        "manifestEngineName" : "manifestEngineName",
        "manifestGPUSupported" : "none",
        "manifestRequireEC2" : true,
        "licenseExpirationTimestamp" : 1,
        "softGPULimit" : 5,
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "manifestEngineMode" : "manifestEngineMode",
        "diskFreeBytes" : 6,
        "buildDefaultTTL" : 0,
        "engineID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91"
      } ],
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

List of engines [GetEngineBuildsResponse](#GetEngineBuildsResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getEngineCategories" id="getEngineCategories"></a>

<div class="method-path">[Up](#__Methods)

    get /engine/categories

</div>

<div class="method-summary">This provides a list of engine categories (<span class="nickname">getEngineCategories</span>)</div>

### Request headers

### Return type

<div class="return-type">[GetEngineCategoriesResponse](#GetEngineCategoriesResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : [ {
        "engineCategoryName" : "engineCategoryName",
        "engineCategoryType" : "engineCategoryType",
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "engineCategoryID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91"
      }, {
        "engineCategoryName" : "engineCategoryName",
        "engineCategoryType" : "engineCategoryType",
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "engineCategoryID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91"
      } ],
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Result of get_engine_categories [GetEngineCategoriesResponse](#GetEngineCategoriesResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getEngineCategoryDetail" id="getEngineCategoryDetail"></a>

<div class="method-path">[Up](#__Methods)

    get /engine/category/{EngineCategoryID}/detail

</div>

<div class="method-summary">This provides detail for an engine category (<span class="nickname">getEngineCategoryDetail</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">EngineCategoryID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Engine Category format: uuid</div>

</div>

### Request headers

### Return type

<div class="return-type">[GetEngineCategoryDetailResponse](#GetEngineCategoryDetailResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : {
        "engineCategoryName" : "engineCategoryName",
        "engineCategoryType" : "engineCategoryType",
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "engineCategoryID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91"
      },
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Result of get_engine_category_detail [GetEngineCategoryDetailResponse](#GetEngineCategoryDetailResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getEngineDetail" id="getEngineDetail"></a>

<div class="method-path">[Up](#__Methods)

    get /engine/{EngineID}/detail

</div>

<div class="method-summary">This API provides the engine detail result (<span class="nickname">getEngineDetail</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">EngineID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Engine format: uuid</div>

</div>

### Return type

<div class="return-type">[GetEngineDetailResponse](#GetEngineDetailResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : {
        "dependencyJSON" : "dependencyJSON",
        "parentCompleteBeforeStart" : true,
        "replacementEngineID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "internalOrganizationID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "dontrunComplete" : true,
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "fieldsJSON" : "fieldsJSON",
        "edge_version" : 6,
        "engineCategoryID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "priority_adjustment" : 1,
        "validationJSON" : "validationJSON",
        "applicationIDsJSON" : "applicationIDsJSON",
        "child_priority_adjustment_on_complete" : 0,
        "engineState" : "active",
        "parallelProcessing" : true,
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "engineName" : "engineName",
        "jwtRightsJSON" : "jwtRightsJSON",
        "engineID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "engineOutputType" : "chunk"
      },
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

List of engines [GetEngineDetailResponse](#GetEngineDetailResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getEngineInstanceDetail" id="getEngineInstanceDetail"></a>

<div class="method-path">[Up](#__Methods)

    get /engine/instance/{EngineInstanceID}/detail

</div>

<div class="method-summary">Get information about an engine Instance (<span class="nickname">getEngineInstanceDetail</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">EngineInstanceID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Engine Instance format: uuid</div>

</div>

### Request headers

### Return type

<div class="return-type">[EngineInstanceInfo](#EngineInstanceInfo)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "runtimeExpirationSeconds" : 6,
      "engineInstanceID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
      "engineToolkitVersion" : "engineToolkitVersion",
      "dockerContainerID" : "dockerContainerID",
      "licenseExpirationSeconds" : 0,
      "launchStatus" : "pending",
      "warnings" : [ null, null ],
      "hostID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
      "additionalEngineIDs" : [ "additionalEngineIDs", "additionalEngineIDs" ],
      "buildID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
      "startupTimestamp" : 1,
      "launchID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
      "launchStatusInfo" : "launchStatusInfo",
      "errors" : [ {
        "errorDescription" : "errorDescription",
        "errorDetail" : "errorDetail",
        "errorId" : "errorId"
      }, {
        "errorDescription" : "errorDescription",
        "errorDetail" : "errorDetail",
        "errorId" : "errorId"
      } ],
      "engineID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
      "launchEnvVariables" : { },
      "status" : "active"
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [EngineInstanceInfo](#EngineInstanceInfo)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getEngineInstanceLogs" id="getEngineInstanceLogs"></a>

<div class="method-path">[Up](#__Methods)

    get /engine/instance/{EngineInstanceID}/logs

</div>

<div class="method-summary">Get engine instance logs as a zip file (<span class="nickname">getEngineInstanceLogs</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">EngineInstanceID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Engine Instance format: uuid</div>

</div>

### Request headers

### Return type

<div class="return-type">byte[]</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    ""

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/zip`
*   `application/json`

### Responses

#### 200

Successful operation [byte[]](#byte[])

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getEngineInstanceStatus" id="getEngineInstanceStatus"></a>

<div class="method-path">[Up](#__Methods)

    get /engine/instance/{EngineInstanceID}/status

</div>

<div class="method-summary">Get the latest status of the engine instance (<span class="nickname">getEngineInstanceStatus</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">EngineInstanceID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Engine Instance format: uuid</div>

</div>

### Request headers

### Return type

<div class="return-type">[EngineInstanceStatus](#EngineInstanceStatus)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "mode" : "idle",
      "taskStatuses" : [ {
        "outputs" : [ null, null ],
        "inputs" : [ {
          "processedCount" : 3,
          "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "processedTotalCount" : 2
        }, {
          "processedCount" : 3,
          "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "processedTotalCount" : 2
        } ],
        "retryCount" : 7,
        "taskOutput" : { },
        "internalJobID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "internalTaskID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "failureReason" : "internal_error",
        "priorTimestamp" : 4,
        "errorCount" : 9,
        "taskStatus" : "scheduled",
        "workRequestID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "engineID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "errorDetails" : "errorDetails",
        "taskRouteID" : "taskRouteID",
        "timestamp" : 1
      }, {
        "outputs" : [ null, null ],
        "inputs" : [ {
          "processedCount" : 3,
          "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "processedTotalCount" : 2
        }, {
          "processedCount" : 3,
          "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "processedTotalCount" : 2
        } ],
        "retryCount" : 7,
        "taskOutput" : { },
        "internalJobID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "internalTaskID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "failureReason" : "internal_error",
        "priorTimestamp" : 4,
        "errorCount" : 9,
        "taskStatus" : "scheduled",
        "workRequestID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "engineID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "errorDetails" : "errorDetails",
        "taskRouteID" : "taskRouteID",
        "timestamp" : 1
      } ],
      "hostID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
      "secondsToTTL" : 7,
      "workRequestDetails" : "workRequestDetails",
      "priorTimestamp" : 2,
      "workRequestStatus" : "complete",
      "containerStatus" : {
        "launchTimestamp" : 1,
        "CPUUtilization" : 0.8008282,
        "memoryAvailable" : 5,
        "diskAvailableRoot" : 6,
        "containerID" : "containerID",
        "memoryUsed" : 5
      },
      "workRequestID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
      "timestamp" : 1
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [EngineInstanceStatus](#EngineInstanceStatus)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getEngineInstanceWork" id="getEngineInstanceWork"></a>

<div class="method-path">[Up](#__Methods)

    post /engine/{EngineInstanceID}/getwork

</div>

<div class="method-summary">Get a work request (<span class="nickname">getEngineInstanceWork</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">EngineInstanceID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Engine Instance format: uuid</div>

</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [EngineInstanceWorkRequest](#EngineInstanceWorkRequest) (required)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — Engine Instance Info</div>

</div>

### Request headers

### Return type

<div class="return-type">[EngineInstanceWorkRequestResponse](#EngineInstanceWorkRequestResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : {
        "action" : "process",
        "workItem" : [ {
          "isRetry" : true,
          "internalOrganizationID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "engineType" : "chunk",
          "internalJobID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "internalTaskID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "taskPayload" : { },
          "organizationID" : 0,
          "jobID" : "jobID",
          "taskIOs" : [ {
            "ioType" : "input",
            "ioMode" : "stream",
            "options" : { },
            "inputFolders" : [ {
              "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
              "taskId" : "taskId"
            }, {
              "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
              "taskId" : "taskId"
            } ],
            "id" : "id"
          }, {
            "ioType" : "input",
            "ioMode" : "stream",
            "options" : { },
            "inputFolders" : [ {
              "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
              "taskId" : "taskId"
            }, {
              "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
              "taskId" : "taskId"
            } ],
            "id" : "id"
          } ],
          "unitCountToProcess" : 6,
          "taskID" : "taskID",
          "engineID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "taskRouteID" : "taskRouteID"
        }, {
          "isRetry" : true,
          "internalOrganizationID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "engineType" : "chunk",
          "internalJobID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "internalTaskID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "taskPayload" : { },
          "organizationID" : 0,
          "jobID" : "jobID",
          "taskIOs" : [ {
            "ioType" : "input",
            "ioMode" : "stream",
            "options" : { },
            "inputFolders" : [ {
              "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
              "taskId" : "taskId"
            }, {
              "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
              "taskId" : "taskId"
            } ],
            "id" : "id"
          }, {
            "ioType" : "input",
            "ioMode" : "stream",
            "options" : { },
            "inputFolders" : [ {
              "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
              "taskId" : "taskId"
            }, {
              "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
              "taskId" : "taskId"
            } ],
            "id" : "id"
          } ],
          "unitCountToProcess" : 6,
          "taskID" : "taskID",
          "engineID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "taskRouteID" : "taskRouteID"
        } ],
        "workRequestID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91"
      },
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Valid work response [EngineInstanceWorkRequestResponse](#EngineInstanceWorkRequestResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getEngineInstanceWorkDetail" id="getEngineInstanceWorkDetail"></a>

<div class="method-path">[Up](#__Methods)

    get /engine/instance/{EngineInstanceID}/workdetail

</div>

<div class="method-summary">Get detail of the work being done by the engine instance (<span class="nickname">getEngineInstanceWorkDetail</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">EngineInstanceID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Engine Instance format: uuid</div>

</div>

### Request headers

### Return type

<div class="return-type">[EngineInstanceWorkDetailsResponse](#EngineInstanceWorkDetailsResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : {
        "workItem" : [ {
          "isRetry" : true,
          "internalOrganizationID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "engineType" : "chunk",
          "internalJobID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "internalTaskID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "taskPayload" : { },
          "organizationID" : 0,
          "jobID" : "jobID",
          "taskIOs" : [ {
            "ioType" : "input",
            "ioMode" : "stream",
            "options" : { },
            "inputFolders" : [ {
              "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
              "taskId" : "taskId"
            }, {
              "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
              "taskId" : "taskId"
            } ],
            "id" : "id"
          }, {
            "ioType" : "input",
            "ioMode" : "stream",
            "options" : { },
            "inputFolders" : [ {
              "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
              "taskId" : "taskId"
            }, {
              "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
              "taskId" : "taskId"
            } ],
            "id" : "id"
          } ],
          "unitCountToProcess" : 6,
          "taskID" : "taskID",
          "engineID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "taskRouteID" : "taskRouteID"
        }, {
          "isRetry" : true,
          "internalOrganizationID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "engineType" : "chunk",
          "internalJobID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "internalTaskID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "taskPayload" : { },
          "organizationID" : 0,
          "jobID" : "jobID",
          "taskIOs" : [ {
            "ioType" : "input",
            "ioMode" : "stream",
            "options" : { },
            "inputFolders" : [ {
              "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
              "taskId" : "taskId"
            }, {
              "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
              "taskId" : "taskId"
            } ],
            "id" : "id"
          }, {
            "ioType" : "input",
            "ioMode" : "stream",
            "options" : { },
            "inputFolders" : [ {
              "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
              "taskId" : "taskId"
            }, {
              "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
              "taskId" : "taskId"
            } ],
            "id" : "id"
          } ],
          "unitCountToProcess" : 6,
          "taskID" : "taskID",
          "engineID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "taskRouteID" : "taskRouteID"
        } ],
        "workRequestDetails" : "workRequestDetails",
        "workRequestStatus" : "complete",
        "workRequestID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91"
      },
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [EngineInstanceWorkDetailsResponse](#EngineInstanceWorkDetailsResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getEngineLaunchDetail" id="getEngineLaunchDetail"></a>

<div class="method-path">[Up](#__Methods)

    get /engine/{EngineID}/launch/{LaunchID}/detail

</div>

<div class="method-summary">This API returns the list of launches for this engine (<span class="nickname">getEngineLaunchDetail</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">EngineID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Engine format: uuid</div>

<div class="param">LaunchID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Launch format: uuid</div>

</div>

### Query parameters

<div class="field-items">

<div class="param">CreatedBefore (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — Filter items where created date is before this date</div>

<div class="param">CreatedAfter (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — Filter items where created date is after this date</div>

<div class="param">limit (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — limit page size to this set</div>

<div class="param">skip (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — skip this many items</div>

<div class="param">sort (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — field to sort on</div>

<div class="param">sortorder (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — sort order</div>

</div>

### Return type

<div class="return-type">[GetEngineLaunchResponse](#GetEngineLaunchResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : {
        "launchID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "launchStatus" : "pending",
        "launchSuccessful" : true,
        "completedTimestamp" : 0,
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "hostID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "launchAction" : "launch"
      },
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Returns detail on a specific launch [GetEngineLaunchResponse](#GetEngineLaunchResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getEngineLaunches" id="getEngineLaunches"></a>

<div class="method-path">[Up](#__Methods)

    get /engine/{EngineID}/launches

</div>

<div class="method-summary">This API returns the list of launches for this engine (<span class="nickname">getEngineLaunches</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">EngineID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Engine format: uuid</div>

</div>

### Query parameters

<div class="field-items">

<div class="param">LaunchStatus (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — Field to match the current launch status</div>

<div class="param">LaunchAction (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — Field to match the current launch action</div>

<div class="param">CreatedBefore (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — Filter items where created date is before this date</div>

<div class="param">CreatedAfter (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — Filter items where created date is after this date</div>

<div class="param">limit (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — limit page size to this set</div>

<div class="param">skip (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — skip this many items</div>

<div class="param">sort (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — field to sort on</div>

<div class="param">sortorder (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — sort order</div>

</div>

### Return type

<div class="return-type">[GetEngineLaunchResponse](#GetEngineLaunchResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : {
        "launchID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "launchStatus" : "pending",
        "launchSuccessful" : true,
        "completedTimestamp" : 0,
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "hostID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "launchAction" : "launch"
      },
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

List of launches for specified engine [GetEngineLaunchResponse](#GetEngineLaunchResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getEngines" id="getEngines"></a>

<div class="method-path">[Up](#__Methods)

    get /engines

</div>

<div class="method-summary">Get the list of engines deployed and available on aiWARE (<span class="nickname">getEngines</span>)</div>

### Request headers

### Query parameters

<div class="field-items">

<div class="param">InternalOrganizationID (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — ID of Organization. UUID. This ID is unique to this aiWARE installation. format: uuid</div>

<div class="param">EngineName (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — Field to string match against the engine names</div>

<div class="param">EngineState (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — Field to match the current state</div>

<div class="param">EngineType (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — Field to match the current type</div>

<div class="param">EngineOutputType (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — Field to match the current type</div>

<div class="param">EngineCategoryID (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — Filter to the particular engine category ID</div>

<div class="param">limit (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — limit page size to this set</div>

<div class="param">skip (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — skip this many items</div>

<div class="param">sort (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — field to sort on</div>

<div class="param">sortorder (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — sort order</div>

<div class="param">EngineIDs (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — Field to provide the input to get engines by Engine ID list. Separated by commas</div>

</div>

### Return type

<div class="return-type">[GetEnginesResponse](#GetEnginesResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : [ {
        "dependencyJSON" : "dependencyJSON",
        "parentCompleteBeforeStart" : true,
        "replacementEngineID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "internalOrganizationID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "dontrunComplete" : true,
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "fieldsJSON" : "fieldsJSON",
        "edge_version" : 6,
        "engineCategoryID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "priority_adjustment" : 1,
        "validationJSON" : "validationJSON",
        "applicationIDsJSON" : "applicationIDsJSON",
        "child_priority_adjustment_on_complete" : 0,
        "engineState" : "active",
        "parallelProcessing" : true,
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "engineName" : "engineName",
        "jwtRightsJSON" : "jwtRightsJSON",
        "engineID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "engineOutputType" : "chunk"
      }, {
        "dependencyJSON" : "dependencyJSON",
        "parentCompleteBeforeStart" : true,
        "replacementEngineID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "internalOrganizationID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "dontrunComplete" : true,
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "fieldsJSON" : "fieldsJSON",
        "edge_version" : 6,
        "engineCategoryID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "priority_adjustment" : 1,
        "validationJSON" : "validationJSON",
        "applicationIDsJSON" : "applicationIDsJSON",
        "child_priority_adjustment_on_complete" : 0,
        "engineState" : "active",
        "parallelProcessing" : true,
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "engineName" : "engineName",
        "jwtRightsJSON" : "jwtRightsJSON",
        "engineID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "engineOutputType" : "chunk"
      } ],
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

List of engines [GetEnginesResponse](#GetEnginesResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="pauseBuild" id="pauseBuild"></a>

<div class="method-path">[Up](#__Methods)

    post /engine/{EngineID}/build/{BuildID}/pause

</div>

<div class="method-summary">This API pauses a build so that tasks based on this engine build will not run. (<span class="nickname">pauseBuild</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">EngineID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Engine format: uuid</div>

<div class="param">BuildID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Build format: uuid</div>

</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [PauseBuildRequest](#PauseBuildRequest) (optional)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — The fields for an engine</div>

</div>

### Request headers

### Query parameters

<div class="field-items">

<div class="param">BuildState (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — Filter builds by the build state</div>

</div>

### Return type

<div class="return-type">[AdminOperationResponse](#AdminOperationResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 204

Pause a particular build [AdminOperationResponse](#AdminOperationResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="pauseEngine" id="pauseEngine"></a>

<div class="method-path">[Up](#__Methods)

    post /engine/{EngineID}/pause

</div>

<div class="method-summary">This API pauses an engine so that tasks based on this engine will not run. (<span class="nickname">pauseEngine</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">EngineID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Engine format: uuid</div>

</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [PauseEngineRequest](#PauseEngineRequest) (optional)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — Engine Instance Info</div>

</div>

### Request headers

### Return type

<div class="return-type">[AdminOperationResponse](#AdminOperationResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 204

Pause a particular engine [AdminOperationResponse](#AdminOperationResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="registerEngineInstanceNoAuth" id="registerEngineInstanceNoAuth"></a>

<div class="method-path">[Up](#__Methods)

    post /engine/register

</div>

<div class="method-summary">Register a new engine instance without authorization (<span class="nickname">registerEngineInstanceNoAuth</span>)</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [EngineInstanceInfo](#EngineInstanceInfo) (required)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — Engine Instance Info</div>

</div>

### Request headers

### Return type

<div class="return-type">[EngineInstanceRegistrationInfo](#EngineInstanceRegistrationInfo)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "runtimeExpirationSeconds" : 0,
      "engineInstanceID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
      "engineInstanceToken" : "engineInstanceToken",
      "action" : "launch"
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful registration of Engine Instance [EngineInstanceRegistrationInfo](#EngineInstanceRegistrationInfo)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="replaceEngine" id="replaceEngine"></a>

<div class="method-path">[Up](#__Methods)

    post /engine/{EngineID}/replace

</div>

<div class="method-summary">This API replaced an engine so that tasks based on this engine will not run. (<span class="nickname">replaceEngine</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">EngineID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Engine format: uuid</div>

</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [ReplaceEngineRequest](#ReplaceEngineRequest) (optional)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — Engine Instance Info</div>

</div>

### Return type

<div class="return-type">[AdminOperationResponse](#AdminOperationResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 204

Pause a particular engine [AdminOperationResponse](#AdminOperationResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="resumeBuild" id="resumeBuild"></a>

<div class="method-path">[Up](#__Methods)

    post /engine/{EngineID}/build/{BuildID}/resume

</div>

<div class="method-summary">This API resumes a build so that tasks based on this engine build will start running. (<span class="nickname">resumeBuild</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">EngineID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Engine format: uuid</div>

<div class="param">BuildID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Build format: uuid</div>

</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [ResumeBuildRequest](#ResumeBuildRequest) (optional)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — Resume Build</div>

</div>

### Request headers

### Return type

<div class="return-type">[AdminOperationResponse](#AdminOperationResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 204

Resume a particular build [AdminOperationResponse](#AdminOperationResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="resumeEngine" id="resumeEngine"></a>

<div class="method-path">[Up](#__Methods)

    post /engine/{EngineID}/resume

</div>

<div class="method-summary">This API resumes a build so that tasks based on this engine build will start running. (<span class="nickname">resumeEngine</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">EngineID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Engine format: uuid</div>

</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [ResumeEngineRequest](#ResumeEngineRequest) (optional)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — Engine Instance Info</div>

</div>

### Request headers

### Return type

<div class="return-type">[AdminOperationResponse](#AdminOperationResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 204

Resume a particular build [AdminOperationResponse](#AdminOperationResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="terminateEngineInstance" id="terminateEngineInstance"></a>

<div class="method-path">[Up](#__Methods)

    post /engine/{EngineInstanceID}/terminate

</div>

<div class="method-summary">Delete the engine instance record (<span class="nickname">terminateEngineInstance</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">EngineInstanceID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Engine Instance format: uuid</div>

</div>

### Request headers

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 204

Successful operation[](#)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="updateEngine" id="updateEngine"></a>

<div class="method-path">[Up](#__Methods)

    post /engine/{EngineID}/update

</div>

<div class="method-summary">This API updates the specified engine (<span class="nickname">updateEngine</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">EngineID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Engine format: uuid</div>

</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [EngineDetail](#EngineDetail) (required)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — Update Engine</div>

</div>

### Request headers

### Return type

<div class="return-type">[UpdateEngineResponse](#UpdateEngineResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : {
        "dependencyJSON" : "dependencyJSON",
        "parentCompleteBeforeStart" : true,
        "replacementEngineID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "internalOrganizationID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "dontrunComplete" : true,
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "fieldsJSON" : "fieldsJSON",
        "edge_version" : 6,
        "engineCategoryID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "priority_adjustment" : 1,
        "validationJSON" : "validationJSON",
        "applicationIDsJSON" : "applicationIDsJSON",
        "child_priority_adjustment_on_complete" : 0,
        "engineState" : "active",
        "parallelProcessing" : true,
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "engineName" : "engineName",
        "jwtRightsJSON" : "jwtRightsJSON",
        "engineID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "engineOutputType" : "chunk"
      },
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

List of engines [UpdateEngineResponse](#UpdateEngineResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="updateEngineBuild" id="updateEngineBuild"></a>

<div class="method-path">[Up](#__Methods)

    post /engine/{EngineID}/build/{BuildID}/update

</div>

<div class="method-summary">This API updates the specified engine (<span class="nickname">updateEngineBuild</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">EngineID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Engine format: uuid</div>

<div class="param">BuildID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Build format: uuid</div>

</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [BuildDetail](#BuildDetail) (required)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — Update Engine BUild</div>

</div>

### Request headers

### Return type

<div class="return-type">[UpdateBuildResponse](#UpdateBuildResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : {
        "dockerImage" : "dockerImage",
        "manifestClusterSize" : "manifestClusterSize",
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "softMemoryBytesLimit" : 5,
        "buildID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "softVCPULimit" : 2,
        "version" : 7,
        "buildState" : "buildState",
        "manifestCustomProfile" : "manifestCustomProfile",
        "manifestEngineName" : "manifestEngineName",
        "manifestGPUSupported" : "none",
        "manifestRequireEC2" : true,
        "licenseExpirationTimestamp" : 1,
        "softGPULimit" : 5,
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "manifestEngineMode" : "manifestEngineMode",
        "diskFreeBytes" : 6,
        "buildDefaultTTL" : 0,
        "engineID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91"
      },
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

List of engines [UpdateBuildResponse](#UpdateBuildResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="updateEngineCategory" id="updateEngineCategory"></a>

<div class="method-path">[Up](#__Methods)

    post /engine/category/{EngineCategoryID}/update

</div>

<div class="method-summary">This updates the specified engine category (<span class="nickname">updateEngineCategory</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">EngineCategoryID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Engine Category format: uuid</div>

</div>

### Request headers

### Return type

<div class="return-type">[UpdateEngineCategoryResponse](#UpdateEngineCategoryResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : {
        "engineCategoryName" : "engineCategoryName",
        "engineCategoryType" : "engineCategoryType",
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "engineCategoryID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91"
      },
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

This updates the specified engine category [UpdateEngineCategoryResponse](#UpdateEngineCategoryResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="updateEngineInstanceStatus" id="updateEngineInstanceStatus"></a>

<div class="method-path">[Up](#__Methods)

    post /engine/{EngineInstanceID}/updatestatus

</div>

<div class="method-summary">Update the Engine Instance Status. Heartbeat to communicate back to controller both aggregated work and delta work from last heartbeat (<span class="nickname">updateEngineInstanceStatus</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">EngineInstanceID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Engine Instance format: uuid</div>

</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [EngineInstanceStatus](#EngineInstanceStatus) (required)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — Engine Instance Status</div>

</div>

### Request headers

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 201

Item created[](#)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

# <a name="Flow" id="Flow">Flow</a>

<div class="method"><a name="createNodeRedContainerInfo" id="createNodeRedContainerInfo"></a>

<div class="method-path">[Up](#__Methods)

    post /flow/nrcontainer/create

</div>

<div class="method-summary">Create node-red container infomation (<span class="nickname">createNodeRedContainerInfo</span>)</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [CreateNodRedContainerInfo](#CreateNodRedContainerInfo) (required)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — Node-RED container info</div>

</div>

### Request headers

### Return type

<div class="return-type">[AdminOperationResponse](#AdminOperationResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [AdminOperationResponse](#AdminOperationResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)</div>

* * *

<div class="method"><a name="deleteAutomateContainer" id="deleteAutomateContainer"></a>

<div class="method-path">[Up](#__Methods)

    post /flow/delete/{ContainerID}

</div>

<div class="method-summary">Delete automate container. (<span class="nickname">deleteAutomateContainer</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">ContainerID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ContainerID of node-red container</div>

</div>

### Return type

<div class="return-type">[AdminOperationResponse](#AdminOperationResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [AdminOperationResponse](#AdminOperationResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)</div>

* * *

<div class="method"><a name="updateAutomateRequestStatus" id="updateAutomateRequestStatus"></a>

<div class="method-path">[Up](#__Methods)

    post /flow/request/update/{UserID}/{Status}

</div>

<div class="method-summary">Put this automate request into update status mode. This automate request will be updated to new status. (<span class="nickname">updateAutomateRequestStatus</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">UserID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of User format: uuid</div>

<div class="param">Status (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — Automate request status</div>

</div>

### Return type

<div class="return-type">[AdminOperationResponse](#AdminOperationResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [AdminOperationResponse](#AdminOperationResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)</div>

* * *

<div class="method"><a name="updateAutomateStatus" id="updateAutomateStatus"></a>

<div class="method-path">[Up](#__Methods)

    post /flow/{HostID}/updatestatus

</div>

<div class="method-summary">Get updated information to launch node-red container, terminate node-red container. (<span class="nickname">updateAutomateStatus</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">HostID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Host format: uuid</div>

</div>

### Return type

<div class="return-type">[HostAction](#HostAction)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "mode" : "continue",
      "launchNodeRedContainer" : [ {
        "dockerImage" : "dockerImage",
        "softMinMemory" : 5,
        "softMinvCPU" : 2,
        "dockerContainerName" : "dockerContainerName",
        "hostId" : "hostId",
        "buildId" : "buildId",
        "env" : [ null, null ],
        "userId" : "userId",
        "launchId" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "port" : "port",
        "name" : "name",
        "engineId" : "engineId",
        "runtimeTTL" : 5
      }, {
        "dockerImage" : "dockerImage",
        "softMinMemory" : 5,
        "softMinvCPU" : 2,
        "dockerContainerName" : "dockerContainerName",
        "hostId" : "hostId",
        "buildId" : "buildId",
        "env" : [ null, null ],
        "userId" : "userId",
        "launchId" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "port" : "port",
        "name" : "name",
        "engineId" : "engineId",
        "runtimeTTL" : 5
      } ],
      "terminateContainer" : [ {
        "dockerContainerId" : "dockerContainerId"
      }, {
        "dockerContainerId" : "dockerContainerId"
      } ],
      "nfsServers" : [ {
        "port" : 9,
        "server_path" : "server_path",
        "cache_number" : 7,
        "options" : "options",
        "local_path" : "local_path",
        "priority" : 3,
        "ips" : [ "ips", "ips" ],
        "mountType" : "nfs"
      }, {
        "port" : 9,
        "server_path" : "server_path",
        "cache_number" : 7,
        "options" : "options",
        "local_path" : "local_path",
        "priority" : 3,
        "ips" : [ "ips", "ips" ],
        "mountType" : "nfs"
      } ],
      "launchContainer" : [ {
        "launchId" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "containerConfig" : {
          "commandLine" : [ "commandLine", "commandLine" ]
        },
        "dockerImage" : "dockerImage",
        "containerType" : "engine",
        "softMinMemory" : 6,
        "name" : "name",
        "softMinvCPU" : 1,
        "runtime" : "runtime",
        "buildId" : "buildId",
        "env" : [ {
          "value" : "value",
          "key" : "key"
        }, {
          "value" : "value",
          "key" : "key"
        } ],
        "engineId" : "engineId",
        "runtimeTTL" : 0
      }, {
        "launchId" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "containerConfig" : {
          "commandLine" : [ "commandLine", "commandLine" ]
        },
        "dockerImage" : "dockerImage",
        "containerType" : "engine",
        "softMinMemory" : 6,
        "name" : "name",
        "softMinvCPU" : 1,
        "runtime" : "runtime",
        "buildId" : "buildId",
        "env" : [ {
          "value" : "value",
          "key" : "key"
        }, {
          "value" : "value",
          "key" : "key"
        } ],
        "engineId" : "engineId",
        "runtimeTTL" : 0
      } ],
      "registries" : [ {
        "dockerRegistryURL" : "dockerRegistryURL",
        "dockerUsername" : "dockerUsername",
        "dockerPassword" : "dockerPassword",
        "name" : "name",
        "isAIWareRegistry" : true,
        "token" : "token"
      }, {
        "dockerRegistryURL" : "dockerRegistryURL",
        "dockerUsername" : "dockerUsername",
        "dockerPassword" : "dockerPassword",
        "name" : "name",
        "isAIWareRegistry" : true,
        "token" : "token"
      } ]
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Valid status request [HostAction](#HostAction)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

# <a name="Host" id="Host">Host</a>

<div class="method"><a name="drainHost" id="drainHost"></a>

<div class="method-path">[Up](#__Methods)

    post /host/{HostID}/drain

</div>

<div class="method-summary">Put this host into drain mode. A host in drain mode will not have work assigned to engines on the host. (<span class="nickname">drainHost</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">HostID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Host format: uuid</div>

</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [DrainHostRequest](#DrainHostRequest) (required)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — The Request to Drain a Host</div>

</div>

### Request headers

### Return type

<div class="return-type">[AdminOperationResponse](#AdminOperationResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [AdminOperationResponse](#AdminOperationResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getHostDetail" id="getHostDetail"></a>

<div class="method-path">[Up](#__Methods)

    get /host/{HostID}/detail

</div>

<div class="method-summary">Get the latest info of the host (<span class="nickname">getHostDetail</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">HostID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Host format: uuid</div>

</div>

### Request headers

### Return type

<div class="return-type">[HostDetail](#HostDetail)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "agentLabel" : "agentLabel",
      "dockerInfo" : "dockerInfo",
      "serverTypeID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
      "shouldExpire" : true,
      "agentCommitID" : "agentCommitID",
      "hostID" : "hostID",
      "ips" : [ "ips", "ips" ],
      "cloudProviderInstanceId" : "cloudProviderInstanceId",
      "suggestedRuntimeTTL" : 0,
      "terminationDetail" : "terminationDetail",
      "drainReason" : "none",
      "dockerHostID" : "dockerHostID",
      "drainDetail" : "drainDetail",
      "agentVersionNumber" : "agentVersionNumber",
      "terminationReason" : "none"
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [HostDetail](#HostDetail)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getHostStatus" id="getHostStatus"></a>

<div class="method-path">[Up](#__Methods)

    get /host/{HostID}/status

</div>

<div class="method-summary">Get the latest status of the host (<span class="nickname">getHostStatus</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">HostID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Host format: uuid</div>

</div>

### Request headers

### Return type

<div class="return-type">[HostStatus](#HostStatus)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "CPUUtilized" : 0.8008282,
      "diskAvailableOptAiware" : 7,
      "memoryAvailable" : 3,
      "vCPUAvailable" : 1,
      "numEngineInstances" : 1,
      "hostID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
      "numCPU" : 4,
      "diskAvailableRoot" : 9,
      "memoryUsed" : 2,
      "containerStatus" : [ {
        "CPUUtilization" : 6.0274563,
        "engineInstanceID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "launchID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "dockerContainerId" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "memoryAvailable" : 5,
        "diskAvailableRoot" : 1,
        "memoryUsed" : 5,
        "numGPU" : 2,
        "engineID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91"
      }, {
        "CPUUtilization" : 6.0274563,
        "engineInstanceID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "launchID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "dockerContainerId" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "memoryAvailable" : 5,
        "diskAvailableRoot" : 1,
        "memoryUsed" : 5,
        "numGPU" : 2,
        "engineID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91"
      } ],
      "numGPU" : 1,
      "numContainers" : 7
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [HostStatus](#HostStatus)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getHosts" id="getHosts"></a>

<div class="method-path">[Up](#__Methods)

    get /hosts

</div>

<div class="method-summary">This provides a list of hosts in the system (<span class="nickname">getHosts</span>)</div>

### Request headers

### Return type

<div class="return-type">[AdminHostsGetResponse](#AdminHostsGetResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : [ {
        "agentLabel" : "agentLabel",
        "dockerInfo" : "dockerInfo",
        "serverTypeID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "shouldExpire" : true,
        "agentCommitID" : "agentCommitID",
        "hostID" : "hostID",
        "ips" : [ "ips", "ips" ],
        "cloudProviderInstanceId" : "cloudProviderInstanceId",
        "suggestedRuntimeTTL" : 0,
        "terminationDetail" : "terminationDetail",
        "drainReason" : "none",
        "dockerHostID" : "dockerHostID",
        "drainDetail" : "drainDetail",
        "agentVersionNumber" : "agentVersionNumber",
        "terminationReason" : "none"
      }, {
        "agentLabel" : "agentLabel",
        "dockerInfo" : "dockerInfo",
        "serverTypeID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "shouldExpire" : true,
        "agentCommitID" : "agentCommitID",
        "hostID" : "hostID",
        "ips" : [ "ips", "ips" ],
        "cloudProviderInstanceId" : "cloudProviderInstanceId",
        "suggestedRuntimeTTL" : 0,
        "terminationDetail" : "terminationDetail",
        "drainReason" : "none",
        "dockerHostID" : "dockerHostID",
        "drainDetail" : "drainDetail",
        "agentVersionNumber" : "agentVersionNumber",
        "terminationReason" : "none"
      } ],
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [AdminHostsGetResponse](#AdminHostsGetResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getHostsLaunch" id="getHostsLaunch"></a>

<div class="method-path">[Up](#__Methods)

    get /host/{HostID}/launch

</div>

<div class="method-summary">This provides a list of host launches in the system (<span class="nickname">getHostsLaunch</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">HostID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Host format: uuid</div>

</div>

### Request headers

### Return type

<div class="return-type">[GetHostLaunchResponse](#GetHostLaunchResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : {
        "launchID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "serverTypeID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "launchStatus" : "pending",
        "launchSuccessful" : true,
        "completedTimestamp" : 0,
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "hostID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "launchAction" : "launch"
      },
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [GetHostLaunchResponse](#GetHostLaunchResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="pauseHost" id="pauseHost"></a>

<div class="method-path">[Up](#__Methods)

    post /host/{HostID}/pause

</div>

<div class="method-summary">Pause all engines on this host. (<span class="nickname">pauseHost</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">HostID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Host format: uuid</div>

</div>

### Request headers

### Return type

<div class="return-type">[AdminOperationResponse](#AdminOperationResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [AdminOperationResponse](#AdminOperationResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="registerEngineInstance" id="registerEngineInstance"></a>

<div class="method-path">[Up](#__Methods)

    post /host/{HostID}/engine/register

</div>

<div class="method-summary">Register a new engine instance (<span class="nickname">registerEngineInstance</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">HostID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Host format: uuid</div>

</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [EngineInstanceInfo](#EngineInstanceInfo) (required)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — Engine Instance Info</div>

</div>

### Request headers

### Return type

<div class="return-type">[EngineInstanceRegistrationInfo](#EngineInstanceRegistrationInfo)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "runtimeExpirationSeconds" : 0,
      "engineInstanceID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
      "engineInstanceToken" : "engineInstanceToken",
      "action" : "launch"
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful registration of Engine Instance [EngineInstanceRegistrationInfo](#EngineInstanceRegistrationInfo)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="registerHost" id="registerHost"></a>

<div class="method-path">[Up](#__Methods)

    post /host/register

</div>

<div class="method-summary">Update the Host Status (<span class="nickname">registerHost</span>)</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [HostRegisterRequest](#HostRegisterRequest) (required)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — Engine Instance Info</div>

</div>

### Request headers

### Return type

<div class="return-type">[HostRegisterResponse](#HostRegisterResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "hostToken" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
      "configProperties" : {
        "veritoneDockerRegistries" : [ {
          "dockerRegistryURL" : "dockerRegistryURL",
          "dockerUsername" : "dockerUsername",
          "dockerPassword" : "dockerPassword",
          "name" : "name",
          "isAIWareRegistry" : true,
          "token" : "token"
        }, {
          "dockerRegistryURL" : "dockerRegistryURL",
          "dockerUsername" : "dockerUsername",
          "dockerPassword" : "dockerPassword",
          "name" : "name",
          "isAIWareRegistry" : true,
          "token" : "token"
        } ],
        "localCacheDirectory" : "localCacheDirectory"
      },
      "hostID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
      "mount" : [ {
        "port" : 9,
        "server_path" : "server_path",
        "cache_number" : 7,
        "options" : "options",
        "local_path" : "local_path",
        "priority" : 3,
        "ips" : [ "ips", "ips" ],
        "mountType" : "nfs"
      }, {
        "port" : 9,
        "server_path" : "server_path",
        "cache_number" : 7,
        "options" : "options",
        "local_path" : "local_path",
        "priority" : 3,
        "ips" : [ "ips", "ips" ],
        "mountType" : "nfs"
      } ],
      "status" : {
        "mode" : "continue",
        "launchNodeRedContainer" : [ {
          "dockerImage" : "dockerImage",
          "softMinMemory" : 5,
          "softMinvCPU" : 2,
          "dockerContainerName" : "dockerContainerName",
          "hostId" : "hostId",
          "buildId" : "buildId",
          "env" : [ null, null ],
          "userId" : "userId",
          "launchId" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "port" : "port",
          "name" : "name",
          "engineId" : "engineId",
          "runtimeTTL" : 5
        }, {
          "dockerImage" : "dockerImage",
          "softMinMemory" : 5,
          "softMinvCPU" : 2,
          "dockerContainerName" : "dockerContainerName",
          "hostId" : "hostId",
          "buildId" : "buildId",
          "env" : [ null, null ],
          "userId" : "userId",
          "launchId" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "port" : "port",
          "name" : "name",
          "engineId" : "engineId",
          "runtimeTTL" : 5
        } ],
        "terminateContainer" : [ {
          "dockerContainerId" : "dockerContainerId"
        }, {
          "dockerContainerId" : "dockerContainerId"
        } ],
        "nfsServers" : [ {
          "port" : 9,
          "server_path" : "server_path",
          "cache_number" : 7,
          "options" : "options",
          "local_path" : "local_path",
          "priority" : 3,
          "ips" : [ "ips", "ips" ],
          "mountType" : "nfs"
        }, {
          "port" : 9,
          "server_path" : "server_path",
          "cache_number" : 7,
          "options" : "options",
          "local_path" : "local_path",
          "priority" : 3,
          "ips" : [ "ips", "ips" ],
          "mountType" : "nfs"
        } ],
        "launchContainer" : [ {
          "launchId" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "containerConfig" : {
            "commandLine" : [ "commandLine", "commandLine" ]
          },
          "dockerImage" : "dockerImage",
          "containerType" : "engine",
          "softMinMemory" : 6,
          "name" : "name",
          "softMinvCPU" : 1,
          "runtime" : "runtime",
          "buildId" : "buildId",
          "env" : [ {
            "value" : "value",
            "key" : "key"
          }, {
            "value" : "value",
            "key" : "key"
          } ],
          "engineId" : "engineId",
          "runtimeTTL" : 0
        }, {
          "launchId" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "containerConfig" : {
            "commandLine" : [ "commandLine", "commandLine" ]
          },
          "dockerImage" : "dockerImage",
          "containerType" : "engine",
          "softMinMemory" : 6,
          "name" : "name",
          "softMinvCPU" : 1,
          "runtime" : "runtime",
          "buildId" : "buildId",
          "env" : [ {
            "value" : "value",
            "key" : "key"
          }, {
            "value" : "value",
            "key" : "key"
          } ],
          "engineId" : "engineId",
          "runtimeTTL" : 0
        } ],
        "registries" : [ {
          "dockerRegistryURL" : "dockerRegistryURL",
          "dockerUsername" : "dockerUsername",
          "dockerPassword" : "dockerPassword",
          "name" : "name",
          "isAIWareRegistry" : true,
          "token" : "token"
        }, {
          "dockerRegistryURL" : "dockerRegistryURL",
          "dockerUsername" : "dockerUsername",
          "dockerPassword" : "dockerPassword",
          "name" : "name",
          "isAIWareRegistry" : true,
          "token" : "token"
        } ]
      }
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Valid status request [HostRegisterResponse](#HostRegisterResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="resumeHost" id="resumeHost"></a>

<div class="method-path">[Up](#__Methods)

    post /host/{HostID}/resume

</div>

<div class="method-summary">Resume all engines on this host. (<span class="nickname">resumeHost</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">HostID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Host format: uuid</div>

</div>

### Request headers

### Return type

<div class="return-type">[AdminOperationResponse](#AdminOperationResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [AdminOperationResponse](#AdminOperationResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="terminateHost" id="terminateHost"></a>

<div class="method-path">[Up](#__Methods)

    post /host/{HostID}/terminate

</div>

<div class="method-summary">Delete the host/agent record. Any work still running on this host will be restarted on other hosts. (<span class="nickname">terminateHost</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">HostID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Host format: uuid</div>

</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [TerminateHostRequest](#TerminateHostRequest) (required)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — The request to terminate the host</div>

</div>

### Request headers

### Return type

<div class="return-type">[AdminOperationResponse](#AdminOperationResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [AdminOperationResponse](#AdminOperationResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="updateHostStatus" id="updateHostStatus"></a>

<div class="method-path">[Up](#__Methods)

    post /host/{HostID}/updatestatus

</div>

<div class="method-summary">Update the Host Status (<span class="nickname">updateHostStatus</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">HostID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Host format: uuid</div>

</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [HostStatus](#HostStatus) (required)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — Host Status</div>

</div>

### Request headers

### Return type

<div class="return-type">[HostAction](#HostAction)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "mode" : "continue",
      "launchNodeRedContainer" : [ {
        "dockerImage" : "dockerImage",
        "softMinMemory" : 5,
        "softMinvCPU" : 2,
        "dockerContainerName" : "dockerContainerName",
        "hostId" : "hostId",
        "buildId" : "buildId",
        "env" : [ null, null ],
        "userId" : "userId",
        "launchId" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "port" : "port",
        "name" : "name",
        "engineId" : "engineId",
        "runtimeTTL" : 5
      }, {
        "dockerImage" : "dockerImage",
        "softMinMemory" : 5,
        "softMinvCPU" : 2,
        "dockerContainerName" : "dockerContainerName",
        "hostId" : "hostId",
        "buildId" : "buildId",
        "env" : [ null, null ],
        "userId" : "userId",
        "launchId" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "port" : "port",
        "name" : "name",
        "engineId" : "engineId",
        "runtimeTTL" : 5
      } ],
      "terminateContainer" : [ {
        "dockerContainerId" : "dockerContainerId"
      }, {
        "dockerContainerId" : "dockerContainerId"
      } ],
      "nfsServers" : [ {
        "port" : 9,
        "server_path" : "server_path",
        "cache_number" : 7,
        "options" : "options",
        "local_path" : "local_path",
        "priority" : 3,
        "ips" : [ "ips", "ips" ],
        "mountType" : "nfs"
      }, {
        "port" : 9,
        "server_path" : "server_path",
        "cache_number" : 7,
        "options" : "options",
        "local_path" : "local_path",
        "priority" : 3,
        "ips" : [ "ips", "ips" ],
        "mountType" : "nfs"
      } ],
      "launchContainer" : [ {
        "launchId" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "containerConfig" : {
          "commandLine" : [ "commandLine", "commandLine" ]
        },
        "dockerImage" : "dockerImage",
        "containerType" : "engine",
        "softMinMemory" : 6,
        "name" : "name",
        "softMinvCPU" : 1,
        "runtime" : "runtime",
        "buildId" : "buildId",
        "env" : [ {
          "value" : "value",
          "key" : "key"
        }, {
          "value" : "value",
          "key" : "key"
        } ],
        "engineId" : "engineId",
        "runtimeTTL" : 0
      }, {
        "launchId" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "containerConfig" : {
          "commandLine" : [ "commandLine", "commandLine" ]
        },
        "dockerImage" : "dockerImage",
        "containerType" : "engine",
        "softMinMemory" : 6,
        "name" : "name",
        "softMinvCPU" : 1,
        "runtime" : "runtime",
        "buildId" : "buildId",
        "env" : [ {
          "value" : "value",
          "key" : "key"
        }, {
          "value" : "value",
          "key" : "key"
        } ],
        "engineId" : "engineId",
        "runtimeTTL" : 0
      } ],
      "registries" : [ {
        "dockerRegistryURL" : "dockerRegistryURL",
        "dockerUsername" : "dockerUsername",
        "dockerPassword" : "dockerPassword",
        "name" : "name",
        "isAIWareRegistry" : true,
        "token" : "token"
      }, {
        "dockerRegistryURL" : "dockerRegistryURL",
        "dockerUsername" : "dockerUsername",
        "dockerPassword" : "dockerPassword",
        "name" : "name",
        "isAIWareRegistry" : true,
        "token" : "token"
      } ]
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Valid status request [HostAction](#HostAction)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

# <a name="Process" id="Process">Process</a>

<div class="method"><a name="createJob" id="createJob"></a>

<div class="method-path">[Up](#__Methods)

    post /proc/job/create

</div>

<div class="method-summary">This creates a new Job (<span class="nickname">createJob</span>)</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [CreateJobRequest](#CreateJobRequest) (required)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — Create Job API</div>

</div>

### Request headers

### Return type

<div class="return-type">[CreateJobResponse](#CreateJobResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "internalJobIds" : [ "internalJobIds", "internalJobIds" ]
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Valid status request [CreateJobResponse](#CreateJobResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="createNextJob" id="createNextJob"></a>

<div class="method-path">[Up](#__Methods)

    post /proc/job/{JobID}/createnext

</div>

<div class="method-summary">This leverages the job template to create a new job based on the next job template in the pipeline. (<span class="nickname">createNextJob</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">JobID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Job format: uuid</div>

</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [CreateNextJobRequest](#CreateNextJobRequest) (required)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — Create Job Next API</div>

</div>

### Request headers

### Return type

<div class="return-type">[CreateNextJobResponse](#CreateNextJobResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "operation" : {
        "success" : true
      }
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Valid status request [CreateNextJobResponse](#CreateNextJobResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="deleteJob" id="deleteJob"></a>

<div class="method-path">[Up](#__Methods)

    post /proc/job/{JobID}/delete

</div>

<div class="method-summary">This API deletes the specified job (<span class="nickname">deleteJob</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">JobID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Job format: uuid</div>

</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [DeleteJobRequest](#DeleteJobRequest) (optional)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — Request information to delete the specified job</div>

</div>

### Request headers

### Return type

<div class="return-type">[AdminOperationResponse](#AdminOperationResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "success" : true
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 204

Delete a particular job [AdminOperationResponse](#AdminOperationResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getJobDetail" id="getJobDetail"></a>

<div class="method-path">[Up](#__Methods)

    get /proc/job/{JobID}/detail

</div>

<div class="method-summary">Gets Job Detail (<span class="nickname">getJobDetail</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">JobID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Job format: uuid</div>

</div>

### Request headers

### Return type

<div class="return-type">[GetJobDetailResponse](#GetJobDetailResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "job" : {
        "jobStatus" : "scheduled",
        "internalOrganizationID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "coreJobID" : "coreJobID",
        "scheduledDateTime" : "2018-03-20T09:12:28Z",
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "abortedDateTime" : "2018-03-20T09:12:28Z",
        "completedDateTime" : "2018-03-20T09:12:28Z",
        "coreScheduledJobId" : 6,
        "jobTemplateId" : "jobTemplateId",
        "stopDateTime" : "2018-03-20T09:12:28Z",
        "coreSourceId" : 1,
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "tasks" : [ {
          "payloadJSON" : "payloadJSON",
          "coreRecordingID" : 4,
          "taskPayloadJSON" : "taskPayloadJSON",
          "internalOrganizationID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "failureDetail" : "failureDetail",
          "coreJobID" : "coreJobID",
          "scheduledDateTime" : "2018-03-20T09:12:28Z",
          "createdDateTime" : "2018-03-20T09:12:28Z",
          "buildID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "abortedDateTime" : "2018-03-20T09:12:28Z",
          "completedDateTime" : "2018-03-20T09:12:28Z",
          "ioFolders" : [ {
            "mode" : "stream",
            "createdDateTime" : "2018-03-20T09:12:28Z",
            "correlationId" : "correlationId",
            "modifiedDateTime" : "2018-03-20T09:12:28Z",
            "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
            "type" : "input",
            "optionsJSON" : "optionsJSON"
          }, {
            "mode" : "stream",
            "createdDateTime" : "2018-03-20T09:12:28Z",
            "correlationId" : "correlationId",
            "modifiedDateTime" : "2018-03-20T09:12:28Z",
            "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
            "type" : "input",
            "optionsJSON" : "optionsJSON"
          } ],
          "coreTaskID" : "coreTaskID",
          "engineCategoryID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "internalTaskID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "maxEngines" : 1,
          "parentMustBeCompleteBeforeStarting" : true,
          "stopDateTime" : "2018-03-20T09:12:28Z",
          "parallelProcessing" : true,
          "modifiedDateTime" : "2018-03-20T09:12:28Z",
          "errorCount" : 1,
          "engineID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "startedDateTime" : "2018-03-20T09:12:28Z",
          "engineCategoryName" : "Transcription",
          "parentTaskID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "internalJobID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "taskTemplateID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "childTaskIDs" : [ "046b6c7f-0b8a-43b9-b35d-6489e6daee91", "046b6c7f-0b8a-43b9-b35d-6489e6daee91" ],
          "taskOutputSON" : "taskOutputSON",
          "maxRetries" : 1,
          "startDateTime" : "2018-03-20T09:12:28Z",
          "dueDateTime" : "2018-03-20T09:12:28Z",
          "isTemplate" : true,
          "failureReason" : "internal_error",
          "currentRetries" : 7,
          "engineName" : "Speechmatic en - V3F"
        }, {
          "payloadJSON" : "payloadJSON",
          "coreRecordingID" : 4,
          "taskPayloadJSON" : "taskPayloadJSON",
          "internalOrganizationID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "failureDetail" : "failureDetail",
          "coreJobID" : "coreJobID",
          "scheduledDateTime" : "2018-03-20T09:12:28Z",
          "createdDateTime" : "2018-03-20T09:12:28Z",
          "buildID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "abortedDateTime" : "2018-03-20T09:12:28Z",
          "completedDateTime" : "2018-03-20T09:12:28Z",
          "ioFolders" : [ {
            "mode" : "stream",
            "createdDateTime" : "2018-03-20T09:12:28Z",
            "correlationId" : "correlationId",
            "modifiedDateTime" : "2018-03-20T09:12:28Z",
            "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
            "type" : "input",
            "optionsJSON" : "optionsJSON"
          }, {
            "mode" : "stream",
            "createdDateTime" : "2018-03-20T09:12:28Z",
            "correlationId" : "correlationId",
            "modifiedDateTime" : "2018-03-20T09:12:28Z",
            "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
            "type" : "input",
            "optionsJSON" : "optionsJSON"
          } ],
          "coreTaskID" : "coreTaskID",
          "engineCategoryID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "internalTaskID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "maxEngines" : 1,
          "parentMustBeCompleteBeforeStarting" : true,
          "stopDateTime" : "2018-03-20T09:12:28Z",
          "parallelProcessing" : true,
          "modifiedDateTime" : "2018-03-20T09:12:28Z",
          "errorCount" : 1,
          "engineID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "startedDateTime" : "2018-03-20T09:12:28Z",
          "engineCategoryName" : "Transcription",
          "parentTaskID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "internalJobID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "taskTemplateID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "childTaskIDs" : [ "046b6c7f-0b8a-43b9-b35d-6489e6daee91", "046b6c7f-0b8a-43b9-b35d-6489e6daee91" ],
          "taskOutputSON" : "taskOutputSON",
          "maxRetries" : 1,
          "startDateTime" : "2018-03-20T09:12:28Z",
          "dueDateTime" : "2018-03-20T09:12:28Z",
          "isTemplate" : true,
          "failureReason" : "internal_error",
          "currentRetries" : 7,
          "engineName" : "Speechmatic en - V3F"
        } ],
        "startedDateTime" : "2018-03-20T09:12:28Z",
        "coreRecordingId" : 0,
        "priority" : 2,
        "internalJobID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "internalScheduledJobId" : "internalScheduledJobId",
        "maxRetries" : 5,
        "startDateTime" : "2018-03-20T09:12:28Z",
        "dueDateTime" : "2018-03-20T09:12:28Z",
        "isTemplate" : true,
        "jobConfigJSON" : "jobConfigJSON",
        "taskRoutes" : [ {
          "endpoint" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "taskParentOutputId" : "taskParentOutputId",
          "taskChildInputCount" : 7,
          "taskParentOutputCount" : 2,
          "taskChildId" : "taskChildId",
          "taskChildInputId" : "taskChildInputId",
          "taskChildNumEngines" : 3,
          "firstWriteDateTime" : "2018-03-20T09:12:28Z",
          "taskChildInputRemainingCount" : 9,
          "taskParentId" : "taskParentId",
          "lastWriteDateTime" : "2018-03-20T09:12:28Z"
        }, {
          "endpoint" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "taskParentOutputId" : "taskParentOutputId",
          "taskChildInputCount" : 7,
          "taskParentOutputCount" : 2,
          "taskChildId" : "taskChildId",
          "taskChildInputId" : "taskChildInputId",
          "taskChildNumEngines" : 3,
          "firstWriteDateTime" : "2018-03-20T09:12:28Z",
          "taskChildInputRemainingCount" : 9,
          "taskParentId" : "taskParentId",
          "lastWriteDateTime" : "2018-03-20T09:12:28Z"
        } ],
        "currentRetries" : 5,
        "coreID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91"
      }
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Valid status request [GetJobDetailResponse](#GetJobDetailResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getJobOutput" id="getJobOutput"></a>

<div class="method-path">[Up](#__Methods)

    get /proc/job/{JobID}/output/{JobOutputName}

</div>

<div class="method-summary">Returns the contents of the job's output (<span class="nickname">getJobOutput</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">JobID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Job format: uuid</div>

<div class="param">JobOutputName (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — Name of the job output, e.g. vtn-standard.json</div>

</div>

### Request headers

### Return type

<div class="return-type">[GetJobOutputResponse](#GetJobOutputResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "output" : {
        "size" : 6,
        "contents" : "contents",
        "created" : 0,
        "name" : "name",
        "contentsValid" : true
      }
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Valid status request [GetJobOutputResponse](#GetJobOutputResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getJobOutputs" id="getJobOutputs"></a>

<div class="method-path">[Up](#__Methods)

    get /proc/job/{JobID}/outputs

</div>

<div class="method-summary">Returns a list of output information about this job (<span class="nickname">getJobOutputs</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">JobID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Job format: uuid</div>

</div>

### Request headers

### Return type

<div class="return-type">[GetJobOutputsResponse](#GetJobOutputsResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "outputs" : {
        "outputs" : [ {
          "size" : 6,
          "contents" : "contents",
          "created" : 0,
          "name" : "name",
          "contentsValid" : true
        }, {
          "size" : 6,
          "contents" : "contents",
          "created" : 0,
          "name" : "name",
          "contentsValid" : true
        } ],
        "internalJobID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91"
      }
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Valid status request [GetJobOutputsResponse](#GetJobOutputsResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getJobStatus" id="getJobStatus"></a>

<div class="method-path">[Up](#__Methods)

    get /proc/job/{JobID}/status

</div>

<div class="method-summary">Gets Job Status (<span class="nickname">getJobStatus</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">JobID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Job format: uuid</div>

</div>

### Request headers

### Return type

<div class="return-type">[GetJobStatusResponse](#GetJobStatusResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "job" : {
        "jobStatus" : "scheduled",
        "internalJobID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91"
      }
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Valid status request [GetJobStatusResponse](#GetJobStatusResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getJobWorkRequests" id="getJobWorkRequests"></a>

<div class="method-path">[Up](#__Methods)

    get /proc/job/{JobID}/workrequests

</div>

<div class="method-summary">This provides a list of workrequests of a job (<span class="nickname">getJobWorkRequests</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">JobID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Job format: uuid</div>

</div>

### Request headers

### Query parameters

<div class="field-items">

<div class="param">offset (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — the number of records to skip before getting the result set</div>

<div class="param">limit (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — the number of records to return.</div>

<div class="param">orderBy (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — the field to sort. It should be in [start_date_time, completed_date_time]</div>

<div class="param">direction (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — the sort order</div>

<div class="param">status (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — the value should be in [active, trial, inactive, deleted]</div>

<div class="param">taskID (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — This is an internal task ID to get work request</div>

</div>

### Return type

<div class="return-type">[GetJobWorkRequestResponse](#GetJobWorkRequestResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : [ {
        "engineInstanceID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "startDateTime" : "2018-03-20T09:12:28Z",
        "buildID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "completedDateTime" : "2018-03-20T09:15:28Z",
        "engineName" : "engineName",
        "engineCategoryID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "internalJobID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "internalTaskID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "errorCount" : 5,
        "workRequestID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "engineID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "status" : "status"
      }, {
        "engineInstanceID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "startDateTime" : "2018-03-20T09:12:28Z",
        "buildID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "completedDateTime" : "2018-03-20T09:15:28Z",
        "engineName" : "engineName",
        "engineCategoryID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "internalJobID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "internalTaskID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "errorCount" : 5,
        "workRequestID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "engineID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "status" : "status"
      } ],
      "offset" : 1,
      "success" : true,
      "count" : 0,
      "limit" : 6
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Successful operation [GetJobWorkRequestResponse](#GetJobWorkRequestResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getJobs" id="getJobs"></a>

<div class="method-path">[Up](#__Methods)

    get /proc/jobs

</div>

<div class="method-summary">This gets a list of jobs (<span class="nickname">getJobs</span>)</div>

### Request headers

### Query parameters

<div class="field-items">

<div class="param">startTime (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — The unix timestamp, describing the start time for the stats format: int64</div>

<div class="param">endTime (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — The unix timestamp, describing the end time for the stats format: int64</div>

<div class="param">offset (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — the number of jobs to skip before getting the result set</div>

<div class="param">limit (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — the number of jobs to return.</div>

<div class="param">orderBy (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — the field to sort</div>

<div class="param">direction (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — the sort order</div>

</div>

### Return type

<div class="return-type">[GetJobListResponse](#GetJobListResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : [ {
        "jobStatus" : "scheduled",
        "internalOrganizationID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "coreJobID" : "coreJobID",
        "scheduledDateTime" : "2018-03-20T09:12:28Z",
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "abortedDateTime" : "2018-03-20T09:12:28Z",
        "completedDateTime" : "2018-03-20T09:12:28Z",
        "coreScheduledJobId" : 6,
        "jobTemplateId" : "jobTemplateId",
        "stopDateTime" : "2018-03-20T09:12:28Z",
        "coreSourceId" : 1,
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "tasks" : [ {
          "payloadJSON" : "payloadJSON",
          "coreRecordingID" : 4,
          "taskPayloadJSON" : "taskPayloadJSON",
          "internalOrganizationID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "failureDetail" : "failureDetail",
          "coreJobID" : "coreJobID",
          "scheduledDateTime" : "2018-03-20T09:12:28Z",
          "createdDateTime" : "2018-03-20T09:12:28Z",
          "buildID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "abortedDateTime" : "2018-03-20T09:12:28Z",
          "completedDateTime" : "2018-03-20T09:12:28Z",
          "ioFolders" : [ {
            "mode" : "stream",
            "createdDateTime" : "2018-03-20T09:12:28Z",
            "correlationId" : "correlationId",
            "modifiedDateTime" : "2018-03-20T09:12:28Z",
            "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
            "type" : "input",
            "optionsJSON" : "optionsJSON"
          }, {
            "mode" : "stream",
            "createdDateTime" : "2018-03-20T09:12:28Z",
            "correlationId" : "correlationId",
            "modifiedDateTime" : "2018-03-20T09:12:28Z",
            "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
            "type" : "input",
            "optionsJSON" : "optionsJSON"
          } ],
          "coreTaskID" : "coreTaskID",
          "engineCategoryID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "internalTaskID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "maxEngines" : 1,
          "parentMustBeCompleteBeforeStarting" : true,
          "stopDateTime" : "2018-03-20T09:12:28Z",
          "parallelProcessing" : true,
          "modifiedDateTime" : "2018-03-20T09:12:28Z",
          "errorCount" : 1,
          "engineID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "startedDateTime" : "2018-03-20T09:12:28Z",
          "engineCategoryName" : "Transcription",
          "parentTaskID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "internalJobID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "taskTemplateID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "childTaskIDs" : [ "046b6c7f-0b8a-43b9-b35d-6489e6daee91", "046b6c7f-0b8a-43b9-b35d-6489e6daee91" ],
          "taskOutputSON" : "taskOutputSON",
          "maxRetries" : 1,
          "startDateTime" : "2018-03-20T09:12:28Z",
          "dueDateTime" : "2018-03-20T09:12:28Z",
          "isTemplate" : true,
          "failureReason" : "internal_error",
          "currentRetries" : 7,
          "engineName" : "Speechmatic en - V3F"
        }, {
          "payloadJSON" : "payloadJSON",
          "coreRecordingID" : 4,
          "taskPayloadJSON" : "taskPayloadJSON",
          "internalOrganizationID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "failureDetail" : "failureDetail",
          "coreJobID" : "coreJobID",
          "scheduledDateTime" : "2018-03-20T09:12:28Z",
          "createdDateTime" : "2018-03-20T09:12:28Z",
          "buildID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "abortedDateTime" : "2018-03-20T09:12:28Z",
          "completedDateTime" : "2018-03-20T09:12:28Z",
          "ioFolders" : [ {
            "mode" : "stream",
            "createdDateTime" : "2018-03-20T09:12:28Z",
            "correlationId" : "correlationId",
            "modifiedDateTime" : "2018-03-20T09:12:28Z",
            "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
            "type" : "input",
            "optionsJSON" : "optionsJSON"
          }, {
            "mode" : "stream",
            "createdDateTime" : "2018-03-20T09:12:28Z",
            "correlationId" : "correlationId",
            "modifiedDateTime" : "2018-03-20T09:12:28Z",
            "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
            "type" : "input",
            "optionsJSON" : "optionsJSON"
          } ],
          "coreTaskID" : "coreTaskID",
          "engineCategoryID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "internalTaskID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "maxEngines" : 1,
          "parentMustBeCompleteBeforeStarting" : true,
          "stopDateTime" : "2018-03-20T09:12:28Z",
          "parallelProcessing" : true,
          "modifiedDateTime" : "2018-03-20T09:12:28Z",
          "errorCount" : 1,
          "engineID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "startedDateTime" : "2018-03-20T09:12:28Z",
          "engineCategoryName" : "Transcription",
          "parentTaskID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "internalJobID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "taskTemplateID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "childTaskIDs" : [ "046b6c7f-0b8a-43b9-b35d-6489e6daee91", "046b6c7f-0b8a-43b9-b35d-6489e6daee91" ],
          "taskOutputSON" : "taskOutputSON",
          "maxRetries" : 1,
          "startDateTime" : "2018-03-20T09:12:28Z",
          "dueDateTime" : "2018-03-20T09:12:28Z",
          "isTemplate" : true,
          "failureReason" : "internal_error",
          "currentRetries" : 7,
          "engineName" : "Speechmatic en - V3F"
        } ],
        "startedDateTime" : "2018-03-20T09:12:28Z",
        "coreRecordingId" : 0,
        "priority" : 2,
        "internalJobID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "internalScheduledJobId" : "internalScheduledJobId",
        "maxRetries" : 5,
        "startDateTime" : "2018-03-20T09:12:28Z",
        "dueDateTime" : "2018-03-20T09:12:28Z",
        "isTemplate" : true,
        "jobConfigJSON" : "jobConfigJSON",
        "taskRoutes" : [ {
          "endpoint" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "taskParentOutputId" : "taskParentOutputId",
          "taskChildInputCount" : 7,
          "taskParentOutputCount" : 2,
          "taskChildId" : "taskChildId",
          "taskChildInputId" : "taskChildInputId",
          "taskChildNumEngines" : 3,
          "firstWriteDateTime" : "2018-03-20T09:12:28Z",
          "taskChildInputRemainingCount" : 9,
          "taskParentId" : "taskParentId",
          "lastWriteDateTime" : "2018-03-20T09:12:28Z"
        }, {
          "endpoint" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "taskParentOutputId" : "taskParentOutputId",
          "taskChildInputCount" : 7,
          "taskParentOutputCount" : 2,
          "taskChildId" : "taskChildId",
          "taskChildInputId" : "taskChildInputId",
          "taskChildNumEngines" : 3,
          "firstWriteDateTime" : "2018-03-20T09:12:28Z",
          "taskChildInputRemainingCount" : 9,
          "taskParentId" : "taskParentId",
          "lastWriteDateTime" : "2018-03-20T09:12:28Z"
        } ],
        "currentRetries" : 5,
        "coreID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91"
      }, {
        "jobStatus" : "scheduled",
        "internalOrganizationID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "coreJobID" : "coreJobID",
        "scheduledDateTime" : "2018-03-20T09:12:28Z",
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "abortedDateTime" : "2018-03-20T09:12:28Z",
        "completedDateTime" : "2018-03-20T09:12:28Z",
        "coreScheduledJobId" : 6,
        "jobTemplateId" : "jobTemplateId",
        "stopDateTime" : "2018-03-20T09:12:28Z",
        "coreSourceId" : 1,
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "tasks" : [ {
          "payloadJSON" : "payloadJSON",
          "coreRecordingID" : 4,
          "taskPayloadJSON" : "taskPayloadJSON",
          "internalOrganizationID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "failureDetail" : "failureDetail",
          "coreJobID" : "coreJobID",
          "scheduledDateTime" : "2018-03-20T09:12:28Z",
          "createdDateTime" : "2018-03-20T09:12:28Z",
          "buildID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "abortedDateTime" : "2018-03-20T09:12:28Z",
          "completedDateTime" : "2018-03-20T09:12:28Z",
          "ioFolders" : [ {
            "mode" : "stream",
            "createdDateTime" : "2018-03-20T09:12:28Z",
            "correlationId" : "correlationId",
            "modifiedDateTime" : "2018-03-20T09:12:28Z",
            "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
            "type" : "input",
            "optionsJSON" : "optionsJSON"
          }, {
            "mode" : "stream",
            "createdDateTime" : "2018-03-20T09:12:28Z",
            "correlationId" : "correlationId",
            "modifiedDateTime" : "2018-03-20T09:12:28Z",
            "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
            "type" : "input",
            "optionsJSON" : "optionsJSON"
          } ],
          "coreTaskID" : "coreTaskID",
          "engineCategoryID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "internalTaskID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "maxEngines" : 1,
          "parentMustBeCompleteBeforeStarting" : true,
          "stopDateTime" : "2018-03-20T09:12:28Z",
          "parallelProcessing" : true,
          "modifiedDateTime" : "2018-03-20T09:12:28Z",
          "errorCount" : 1,
          "engineID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "startedDateTime" : "2018-03-20T09:12:28Z",
          "engineCategoryName" : "Transcription",
          "parentTaskID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "internalJobID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "taskTemplateID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "childTaskIDs" : [ "046b6c7f-0b8a-43b9-b35d-6489e6daee91", "046b6c7f-0b8a-43b9-b35d-6489e6daee91" ],
          "taskOutputSON" : "taskOutputSON",
          "maxRetries" : 1,
          "startDateTime" : "2018-03-20T09:12:28Z",
          "dueDateTime" : "2018-03-20T09:12:28Z",
          "isTemplate" : true,
          "failureReason" : "internal_error",
          "currentRetries" : 7,
          "engineName" : "Speechmatic en - V3F"
        }, {
          "payloadJSON" : "payloadJSON",
          "coreRecordingID" : 4,
          "taskPayloadJSON" : "taskPayloadJSON",
          "internalOrganizationID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "failureDetail" : "failureDetail",
          "coreJobID" : "coreJobID",
          "scheduledDateTime" : "2018-03-20T09:12:28Z",
          "createdDateTime" : "2018-03-20T09:12:28Z",
          "buildID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "abortedDateTime" : "2018-03-20T09:12:28Z",
          "completedDateTime" : "2018-03-20T09:12:28Z",
          "ioFolders" : [ {
            "mode" : "stream",
            "createdDateTime" : "2018-03-20T09:12:28Z",
            "correlationId" : "correlationId",
            "modifiedDateTime" : "2018-03-20T09:12:28Z",
            "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
            "type" : "input",
            "optionsJSON" : "optionsJSON"
          }, {
            "mode" : "stream",
            "createdDateTime" : "2018-03-20T09:12:28Z",
            "correlationId" : "correlationId",
            "modifiedDateTime" : "2018-03-20T09:12:28Z",
            "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
            "type" : "input",
            "optionsJSON" : "optionsJSON"
          } ],
          "coreTaskID" : "coreTaskID",
          "engineCategoryID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "internalTaskID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "maxEngines" : 1,
          "parentMustBeCompleteBeforeStarting" : true,
          "stopDateTime" : "2018-03-20T09:12:28Z",
          "parallelProcessing" : true,
          "modifiedDateTime" : "2018-03-20T09:12:28Z",
          "errorCount" : 1,
          "engineID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "startedDateTime" : "2018-03-20T09:12:28Z",
          "engineCategoryName" : "Transcription",
          "parentTaskID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "internalJobID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "taskTemplateID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "childTaskIDs" : [ "046b6c7f-0b8a-43b9-b35d-6489e6daee91", "046b6c7f-0b8a-43b9-b35d-6489e6daee91" ],
          "taskOutputSON" : "taskOutputSON",
          "maxRetries" : 1,
          "startDateTime" : "2018-03-20T09:12:28Z",
          "dueDateTime" : "2018-03-20T09:12:28Z",
          "isTemplate" : true,
          "failureReason" : "internal_error",
          "currentRetries" : 7,
          "engineName" : "Speechmatic en - V3F"
        } ],
        "startedDateTime" : "2018-03-20T09:12:28Z",
        "coreRecordingId" : 0,
        "priority" : 2,
        "internalJobID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "internalScheduledJobId" : "internalScheduledJobId",
        "maxRetries" : 5,
        "startDateTime" : "2018-03-20T09:12:28Z",
        "dueDateTime" : "2018-03-20T09:12:28Z",
        "isTemplate" : true,
        "jobConfigJSON" : "jobConfigJSON",
        "taskRoutes" : [ {
          "endpoint" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "taskParentOutputId" : "taskParentOutputId",
          "taskChildInputCount" : 7,
          "taskParentOutputCount" : 2,
          "taskChildId" : "taskChildId",
          "taskChildInputId" : "taskChildInputId",
          "taskChildNumEngines" : 3,
          "firstWriteDateTime" : "2018-03-20T09:12:28Z",
          "taskChildInputRemainingCount" : 9,
          "taskParentId" : "taskParentId",
          "lastWriteDateTime" : "2018-03-20T09:12:28Z"
        }, {
          "endpoint" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "taskParentOutputId" : "taskParentOutputId",
          "taskChildInputCount" : 7,
          "taskParentOutputCount" : 2,
          "taskChildId" : "taskChildId",
          "taskChildInputId" : "taskChildInputId",
          "taskChildNumEngines" : 3,
          "firstWriteDateTime" : "2018-03-20T09:12:28Z",
          "taskChildInputRemainingCount" : 9,
          "taskParentId" : "taskParentId",
          "lastWriteDateTime" : "2018-03-20T09:12:28Z"
        } ],
        "currentRetries" : 5,
        "coreID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91"
      } ],
      "offset" : 1,
      "success" : true,
      "count" : 0,
      "limit" : 6
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Valid status request [GetJobListResponse](#GetJobListResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getJobsOrganizationStats" id="getJobsOrganizationStats"></a>

<div class="method-path">[Up](#__Methods)

    get /proc/jobs/stats/organization

</div>

<div class="method-summary">This gets processing stats of the jobs by organization (<span class="nickname">getJobsOrganizationStats</span>)</div>

### Request headers

### Query parameters

<div class="field-items">

<div class="param">startTime (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — The unix timestamp, describing the start time for the stats format: int64</div>

<div class="param">endTime (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — The unix timestamp, describing the end time for the stats format: int64</div>

</div>

### Return type

<div class="return-type">[GetJobsOrganizationStatsResponse](#GetJobsOrganizationStatsResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "counts" : [ {
        "count" : 1,
        "organizationId" : 7682,
        "organizationName" : "Veritone Inc",
        "status" : "pending"
      }, {
        "count" : 2,
        "organizationId" : 7682,
        "organizationName" : "Veritone Inc",
        "status" : "running"
      } ],
      "endDateTime" : "2018-03-20T10:12:58.000Z",
      "startDateTime" : "2018-03-20T09:12:28.000Z"
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Valid status request [GetJobsOrganizationStatsResponse](#GetJobsOrganizationStatsResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getJobsPerformance" id="getJobsPerformance"></a>

<div class="method-path">[Up](#__Methods)

    get /proc/jobs/performance

</div>

<div class="method-summary">This gets cpu/gpu, memory state of the hosts grouped by time ranges and sorted by a range start time (<span class="nickname">getJobsPerformance</span>)</div>

### Request headers

### Query parameters

<div class="field-items">

<div class="param">startTime (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — The unix timestamp, describing the start time for the stats format: int64</div>

<div class="param">endTime (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — The unix timestamp, describing the end time for the stats format: int64</div>

<div class="param">interval (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — Interval in seconds for output time ranges format: int64</div>

</div>

### Return type

<div class="return-type">[GetJobsPerformanceResponse](#GetJobsPerformanceResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "data" : [ {
        "cpu" : 10,
        "dateTime" : "2018-03-20T08:00:00.000Z",
        "gpu" : 0,
        "memory" : 20
      }, {
        "cpu" : 0,
        "dateTime" : "2018-03-20T09:00:00.000Z",
        "gpu" : 20,
        "memory" : 40
      } ],
      "endDateTime" : "2018-03-20T10:12:28.000Z",
      "startDateTime" : "2018-03-20T09:12:28.000Z"
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Valid status request [GetJobsPerformanceResponse](#GetJobsPerformanceResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getJobsStats" id="getJobsStats"></a>

<div class="method-path">[Up](#__Methods)

    get /proc/jobs/stats

</div>

<div class="method-summary">This gets processing stats of the jobs (<span class="nickname">getJobsStats</span>)</div>

### Request headers

### Query parameters

<div class="field-items">

<div class="param">startTime (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — The unix timestamp, describing the start time for the stats format: int64</div>

<div class="param">endTime (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — The unix timestamp, describing the end time for the stats format: int64</div>

</div>

### Return type

<div class="return-type">[GetJobsStatsResponse](#GetJobsStatsResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "counts" : [ {
        "count" : 0
      }, {
        "count" : 0
      } ],
      "endDateTime" : "2018-03-20T10:12:28.000Z",
      "startDateTime" : "2018-03-20T09:12:28.000Z"
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Valid status request [GetJobsStatsResponse](#GetJobsStatsResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getJobsTimeRangesStats" id="getJobsTimeRangesStats"></a>

<div class="method-path">[Up](#__Methods)

    get /proc/jobs/stats/time_ranges

</div>

<div class="method-summary">This gets processing stats of the jobs grouped by time ranges and sorted by a range start time (<span class="nickname">getJobsTimeRangesStats</span>)</div>

### Request headers

### Query parameters

<div class="field-items">

<div class="param">startTime (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — The unix timestamp, describing the start time for the stats format: int64</div>

<div class="param">endTime (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — The unix timestamp, describing the end time for the stats format: int64</div>

<div class="param">interval (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — Interval in seconds for output time ranges format: int64</div>

</div>

### Return type

<div class="return-type">[GetJobsTimeRangesStatsResponse](#GetJobsTimeRangesStatsResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "counts" : [ {
        "count" : 0,
        "endDateTime" : "2018-03-20T10:12:28.000Z",
        "startDateTime" : "2018-03-20T09:12:28.000Z"
      }, {
        "count" : 0,
        "endDateTime" : "2018-03-20T10:12:28.000Z",
        "startDateTime" : "2018-03-20T09:12:28.000Z"
      } ],
      "endDateTime" : "2018-03-20T10:12:28.000Z",
      "startDateTime" : "2018-03-20T09:12:28.000Z"
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Valid status request [GetJobsTimeRangesStatsResponse](#GetJobsTimeRangesStatsResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getTaskDetail" id="getTaskDetail"></a>

<div class="method-path">[Up](#__Methods)

    get /proc/task/{TaskID}/detail

</div>

<div class="method-summary">Gets Task Detail (<span class="nickname">getTaskDetail</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">TaskID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Task format: uuid</div>

</div>

### Request headers

### Return type

<div class="return-type">[GetTaskDetailResponse](#GetTaskDetailResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "task" : {
        "payloadJSON" : "payloadJSON",
        "coreRecordingID" : 4,
        "taskPayloadJSON" : "taskPayloadJSON",
        "internalOrganizationID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "failureDetail" : "failureDetail",
        "coreJobID" : "coreJobID",
        "scheduledDateTime" : "2018-03-20T09:12:28Z",
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "buildID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "abortedDateTime" : "2018-03-20T09:12:28Z",
        "completedDateTime" : "2018-03-20T09:12:28Z",
        "ioFolders" : [ {
          "mode" : "stream",
          "createdDateTime" : "2018-03-20T09:12:28Z",
          "correlationId" : "correlationId",
          "modifiedDateTime" : "2018-03-20T09:12:28Z",
          "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "type" : "input",
          "optionsJSON" : "optionsJSON"
        }, {
          "mode" : "stream",
          "createdDateTime" : "2018-03-20T09:12:28Z",
          "correlationId" : "correlationId",
          "modifiedDateTime" : "2018-03-20T09:12:28Z",
          "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "type" : "input",
          "optionsJSON" : "optionsJSON"
        } ],
        "coreTaskID" : "coreTaskID",
        "engineCategoryID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "internalTaskID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "maxEngines" : 1,
        "parentMustBeCompleteBeforeStarting" : true,
        "stopDateTime" : "2018-03-20T09:12:28Z",
        "parallelProcessing" : true,
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "errorCount" : 1,
        "engineID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "startedDateTime" : "2018-03-20T09:12:28Z",
        "engineCategoryName" : "Transcription",
        "parentTaskID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "internalJobID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "taskTemplateID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "childTaskIDs" : [ "046b6c7f-0b8a-43b9-b35d-6489e6daee91", "046b6c7f-0b8a-43b9-b35d-6489e6daee91" ],
        "taskOutputSON" : "taskOutputSON",
        "maxRetries" : 1,
        "startDateTime" : "2018-03-20T09:12:28Z",
        "dueDateTime" : "2018-03-20T09:12:28Z",
        "isTemplate" : true,
        "failureReason" : "internal_error",
        "currentRetries" : 7,
        "engineName" : "Speechmatic en - V3F"
      }
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Valid status request [GetTaskDetailResponse](#GetTaskDetailResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getTaskLogs" id="getTaskLogs"></a>

<div class="method-path">[Up](#__Methods)

    get /proc/task/{TaskID}/logs

</div>

<div class="method-summary">Gets logs associated with a task (<span class="nickname">getTaskLogs</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">TaskID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Task format: uuid</div>

</div>

### Request headers

### Return type

<div class="return-type">byte[]</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    ""

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/zip`
*   `application/json`

### Responses

#### 200

Successful operation [byte[]](#byte[])

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getTaskOutput" id="getTaskOutput"></a>

<div class="method-path">[Up](#__Methods)

    get /proc/task/{TaskID}/output/{TaskOutputName}

</div>

<div class="method-summary">Returns the contents of the task's output (<span class="nickname">getTaskOutput</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">TaskID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Task format: uuid</div>

<div class="param">TaskOutputName (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — Name of the task output, e.g. vtn-standard.json</div>

</div>

### Request headers

### Return type

<div class="return-type">[GetTaskOutputResponse](#GetTaskOutputResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "output" : {
        "size" : 6,
        "contents" : "contents",
        "created" : 0,
        "name" : "name",
        "contentsValid" : true
      }
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Valid status request [GetTaskOutputResponse](#GetTaskOutputResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getTaskOutputs" id="getTaskOutputs"></a>

<div class="method-path">[Up](#__Methods)

    get /proc/task/{TaskID}/outputs

</div>

<div class="method-summary">Gets Task Output (<span class="nickname">getTaskOutputs</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">TaskID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Task format: uuid</div>

</div>

### Request headers

### Return type

<div class="return-type">[GetTaskOutputsResponse](#GetTaskOutputsResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "outputs" : {
        "outputs" : [ {
          "size" : 6,
          "contents" : "contents",
          "created" : 0,
          "name" : "name",
          "contentsValid" : true
        }, {
          "size" : 6,
          "contents" : "contents",
          "created" : 0,
          "name" : "name",
          "contentsValid" : true
        } ],
        "internalTaskID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91"
      }
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Valid status request [GetTaskOutputsResponse](#GetTaskOutputsResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getTasks" id="getTasks"></a>

<div class="method-path">[Up](#__Methods)

    get /proc/tasks

</div>

<div class="method-summary">This gets a list of tasks based on the provided criteria (<span class="nickname">getTasks</span>)</div>

### Request headers

### Query parameters

<div class="field-items">

<div class="param">startTime (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — The unix timestamp, describing the start time for the stats format: int64</div>

<div class="param">endTime (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — The unix timestamp, describing the end time for the stats format: int64</div>

<div class="param">offset (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — the number of jobs to skip before getting the result set format: int64</div>

<div class="param">limit (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — the number of jobs to return. format: int64</div>

<div class="param">orderBy (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — the field to sort</div>

<div class="param">direction (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — the sort order</div>

<div class="param">status (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — If specified, this limits the jobs or tasks to follow status</div>

<div class="param">organizationID (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — Filter by organization id</div>

<div class="param">jobID (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — Filter by job id</div>

<div class="param">engineID (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — Filter by engine id</div>

<div class="param">mediaSourceID (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — Filter by media source id</div>

<div class="param">recordingID (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — Filter tasks by the recording id format: int64</div>

<div class="param">modifiedBefore (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — Filter by tasks modified before expressed as timestamp format: int64</div>

<div class="param">modifiedAfter (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — Filter by tasks modified after expressed as timestamp format: int64</div>

</div>

### Return type

<div class="return-type">[GetTasksResponse](#GetTasksResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "result" : [ {
        "payloadJSON" : "payloadJSON",
        "coreRecordingID" : 4,
        "taskPayloadJSON" : "taskPayloadJSON",
        "internalOrganizationID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "failureDetail" : "failureDetail",
        "coreJobID" : "coreJobID",
        "scheduledDateTime" : "2018-03-20T09:12:28Z",
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "buildID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "abortedDateTime" : "2018-03-20T09:12:28Z",
        "completedDateTime" : "2018-03-20T09:12:28Z",
        "ioFolders" : [ {
          "mode" : "stream",
          "createdDateTime" : "2018-03-20T09:12:28Z",
          "correlationId" : "correlationId",
          "modifiedDateTime" : "2018-03-20T09:12:28Z",
          "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "type" : "input",
          "optionsJSON" : "optionsJSON"
        }, {
          "mode" : "stream",
          "createdDateTime" : "2018-03-20T09:12:28Z",
          "correlationId" : "correlationId",
          "modifiedDateTime" : "2018-03-20T09:12:28Z",
          "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "type" : "input",
          "optionsJSON" : "optionsJSON"
        } ],
        "coreTaskID" : "coreTaskID",
        "engineCategoryID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "internalTaskID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "maxEngines" : 1,
        "parentMustBeCompleteBeforeStarting" : true,
        "stopDateTime" : "2018-03-20T09:12:28Z",
        "parallelProcessing" : true,
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "errorCount" : 1,
        "engineID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "startedDateTime" : "2018-03-20T09:12:28Z",
        "engineCategoryName" : "Transcription",
        "parentTaskID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "internalJobID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "taskTemplateID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "childTaskIDs" : [ "046b6c7f-0b8a-43b9-b35d-6489e6daee91", "046b6c7f-0b8a-43b9-b35d-6489e6daee91" ],
        "taskOutputSON" : "taskOutputSON",
        "maxRetries" : 1,
        "startDateTime" : "2018-03-20T09:12:28Z",
        "dueDateTime" : "2018-03-20T09:12:28Z",
        "isTemplate" : true,
        "failureReason" : "internal_error",
        "currentRetries" : 7,
        "engineName" : "Speechmatic en - V3F"
      }, {
        "payloadJSON" : "payloadJSON",
        "coreRecordingID" : 4,
        "taskPayloadJSON" : "taskPayloadJSON",
        "internalOrganizationID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "failureDetail" : "failureDetail",
        "coreJobID" : "coreJobID",
        "scheduledDateTime" : "2018-03-20T09:12:28Z",
        "createdDateTime" : "2018-03-20T09:12:28Z",
        "buildID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "abortedDateTime" : "2018-03-20T09:12:28Z",
        "completedDateTime" : "2018-03-20T09:12:28Z",
        "ioFolders" : [ {
          "mode" : "stream",
          "createdDateTime" : "2018-03-20T09:12:28Z",
          "correlationId" : "correlationId",
          "modifiedDateTime" : "2018-03-20T09:12:28Z",
          "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "type" : "input",
          "optionsJSON" : "optionsJSON"
        }, {
          "mode" : "stream",
          "createdDateTime" : "2018-03-20T09:12:28Z",
          "correlationId" : "correlationId",
          "modifiedDateTime" : "2018-03-20T09:12:28Z",
          "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "type" : "input",
          "optionsJSON" : "optionsJSON"
        } ],
        "coreTaskID" : "coreTaskID",
        "engineCategoryID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "internalTaskID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "maxEngines" : 1,
        "parentMustBeCompleteBeforeStarting" : true,
        "stopDateTime" : "2018-03-20T09:12:28Z",
        "parallelProcessing" : true,
        "modifiedDateTime" : "2018-03-20T09:12:28Z",
        "errorCount" : 1,
        "engineID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "startedDateTime" : "2018-03-20T09:12:28Z",
        "engineCategoryName" : "Transcription",
        "parentTaskID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "internalJobID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "taskTemplateID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "childTaskIDs" : [ "046b6c7f-0b8a-43b9-b35d-6489e6daee91", "046b6c7f-0b8a-43b9-b35d-6489e6daee91" ],
        "taskOutputSON" : "taskOutputSON",
        "maxRetries" : 1,
        "startDateTime" : "2018-03-20T09:12:28Z",
        "dueDateTime" : "2018-03-20T09:12:28Z",
        "isTemplate" : true,
        "failureReason" : "internal_error",
        "currentRetries" : 7,
        "engineName" : "Speechmatic en - V3F"
      } ],
      "offset" : 1,
      "success" : true,
      "count" : 0,
      "limit" : 6
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Valid status request [GetTasksResponse](#GetTasksResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getTasksStats" id="getTasksStats"></a>

<div class="method-path">[Up](#__Methods)

    get /proc/tasks/stats

</div>

<div class="method-summary">This gets processing stats of the tasks (<span class="nickname">getTasksStats</span>)</div>

### Request headers

### Query parameters

<div class="field-items">

<div class="param">startTime (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — The unix timestamp, describing the start time for the stats format: int64</div>

<div class="param">endTime (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — The unix timestamp, describing the end time for the stats format: int64</div>

</div>

### Return type

<div class="return-type">[GetTasksStatsResponse](#GetTasksStatsResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "counts" : [ {
        "count" : 0
      }, {
        "count" : 0
      } ],
      "endDateTime" : "2018-03-20T10:12:28.000Z",
      "startDateTime" : "2018-03-20T09:12:28.000Z"
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

This provides the output for the tasks stats call. Rows that do not have data will be omitted. [GetTasksStatsResponse](#GetTasksStatsResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getTasksStatsEngines" id="getTasksStatsEngines"></a>

<div class="method-path">[Up](#__Methods)

    get /proc/tasks/stats/engines

</div>

<div class="method-summary">This gets processing stats of the tasks grouped by engine categories (<span class="nickname">getTasksStatsEngines</span>)</div>

### Request headers

### Query parameters

<div class="field-items">

<div class="param">startTime (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — The unix timestamp, describing the start time for the stats format: int64</div>

<div class="param">endTime (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — The unix timestamp, describing the end time for the stats format: int64</div>

</div>

### Return type

<div class="return-type">[GetTasksEnginesStatsResponse](#GetTasksEnginesStatsResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "counts" : [ {
        "count" : 0,
        "engineCategoryName" : "Logo Recognition"
      }, {
        "count" : 0,
        "engineCategoryName" : "Logo Recognition"
      } ],
      "endDateTime" : "2018-03-20T10:12:28.000Z",
      "startDateTime" : "2018-03-20T09:12:28.000Z"
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Valid status request [GetTasksEnginesStatsResponse](#GetTasksEnginesStatsResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getTasksStatsHosts" id="getTasksStatsHosts"></a>

<div class="method-path">[Up](#__Methods)

    get /proc/tasks/stats/hosts

</div>

<div class="method-summary">This gets processing stats of the tasks grouped by hosts (<span class="nickname">getTasksStatsHosts</span>)</div>

### Request headers

### Query parameters

<div class="field-items">

<div class="param">startTime (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — The unix timestamp, describing the start time for the stats format: int64</div>

<div class="param">endTime (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — The unix timestamp, describing the end time for the stats format: int64</div>

</div>

### Return type

<div class="return-type">[GetTasksHostsStatsResponse](#GetTasksHostsStatsResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "counts" : [ {
        "count" : 0,
        "engineCategoryName" : "Translation",
        "hostName" : "Host1"
      }, {
        "count" : 0,
        "engineCategoryName" : "Translation",
        "hostName" : "Host1"
      } ],
      "endDateTime" : "2018-03-20T10:12:28.000Z",
      "startDateTime" : "2018-03-20T09:12:28.000Z"
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Valid status request [GetTasksHostsStatsResponse](#GetTasksHostsStatsResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="getTasksStatsTimeRanges" id="getTasksStatsTimeRanges"></a>

<div class="method-path">[Up](#__Methods)

    get /proc/tasks/stats/time_ranges

</div>

<div class="method-summary">This gets processing stats of the tasks grouped by time ranges and sorted by a range start time (<span class="nickname">getTasksStatsTimeRanges</span>)</div>

### Request headers

### Query parameters

<div class="field-items">

<div class="param">startTime (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — The unix timestamp, describing the start time for the stats format: int64</div>

<div class="param">endTime (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — The unix timestamp, describing the end time for the stats format: int64</div>

<div class="param">interval (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> — Interval in seconds for output time ranges format: int64</div>

</div>

### Return type

<div class="return-type">[GetTasksTimeRangesStatsResponse](#GetTasksTimeRangesStatsResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "counts" : [ {
        "count" : 0,
        "endDateTime" : "2018-03-20T10:12:28.000Z",
        "startDateTime" : "2018-03-20T09:12:28.000Z"
      }, {
        "count" : 0,
        "endDateTime" : "2018-03-20T10:12:28.000Z",
        "startDateTime" : "2018-03-20T09:12:28.000Z"
      } ],
      "endDateTime" : "2018-03-20T10:12:28.000Z",
      "startDateTime" : "2018-03-20T09:12:28.000Z"
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Valid status request [GetTasksTimeRangesStatsResponse](#GetTasksTimeRangesStatsResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="launchJobTemplate" id="launchJobTemplate"></a>

<div class="method-path">[Up](#__Methods)

    post /proc/template/{TemplateID}/launch

</div>

<div class="method-summary">This launch a job based on the given job template (<span class="nickname">launchJobTemplate</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">TemplateID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Job</div>

</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`

### Request body

<div class="field-items">

<div class="param">body [LaunchJobTemplateRequest](#LaunchJobTemplateRequest) (required)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — Launch Job Template API</div>

</div>

### Request headers

### Return type

<div class="return-type">[LaunchJobTemplateResponse](#LaunchJobTemplateResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "operation" : {
        "success" : true
      }
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Valid status request [LaunchJobTemplateResponse](#LaunchJobTemplateResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="pushContentToEndpoint" id="pushContentToEndpoint"></a>

<div class="method-path">[Up](#__Methods)

    post /proc/endpoint/{Endpoint}

</div>

<div class="method-summary">Whatever is posted to this endpoint will be added to the child input folder(s) for the task_routes that have this endpoint. If more than one task_routes have this endpoint, it will be added to all child input folders. (<span class="nickname">pushContentToEndpoint</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">Endpoint (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — Endpoint UUID to push this chunk towards format: uuid</div>

</div>

### Consumes

This API call consumes the following media types via the <span class="header">Content-Type</span> request header:

*   `application/json`
*   `application/octet-stream`
*   `audio/*`
*   `image/*`
*   `text/html`
*   `text/plain`
*   `text/xml`
*   `video/*`

### Request body

<div class="field-items">

<div class="param">body [string](#string) (required)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — How to push content into a child input folder(s).</div>

</div>

### Request headers

### Return type

<div class="return-type">[CreateJobResponse](#CreateJobResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "internalJobIds" : [ "internalJobIds", "internalJobIds" ]
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Valid status request [CreateJobResponse](#CreateJobResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

<div class="method"><a name="recheckJobStatus" id="recheckJobStatus"></a>

<div class="method-path">[Up](#__Methods)

    get /proc/job/{JobID}/recheck_status

</div>

<div class="method-summary">Recheck Job Status (<span class="nickname">recheckJobStatus</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">JobID (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — ID of Job format: uuid</div>

</div>

### Request headers

### Return type

<div class="return-type">[RecheckJobStatusResponse](#RecheckJobStatusResponse)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

    {
      "job" : {
        "jobStatus" : "scheduled",
        "internalJobID" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91"
      }
    }

### Produces

This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header.

*   `application/json`

### Responses

#### 200

Valid status request [RecheckJobStatusResponse](#RecheckJobStatusResponse)

#### 400

Invalid argument. Please see the error response for more information. [Error](#Error)

#### 401

Not authorized [Error](#Error)

#### 403

Forbidden [Error](#Error)

#### 404

Not Found [Error](#Error)

#### 405

The request is not allowed. [Error](#Error)

#### 429

Too Many Requests [Error](#Error)

#### 501

Not Implemented [Error](#Error)

#### 503

System Unavailable [Error](#Error)</div>

* * *

## <a name="__Models" id="__Models">Models</a>

[ Jump to [Methods](#__Methods) ]

### Table of Contents

1.  [`AddServersToServerTypeRequest`](#AddServersToServerTypeRequest)
2.  [`AdminConfigResponse`](#AdminConfigResponse)
3.  [`AdminConfigSectionKeyResponse`](#AdminConfigSectionKeyResponse)
4.  [`AdminConfigSectionResponse`](#AdminConfigSectionResponse)
5.  [`AdminConfigUpdateRequest`](#AdminConfigUpdateRequest)
6.  [`AdminConfigUpdateResponse`](#AdminConfigUpdateResponse)
7.  [`AdminConfigUpdateSectionKeyRequest`](#AdminConfigUpdateSectionKeyRequest)
8.  [`AdminConfigUpdateSectionKeyResponse`](#AdminConfigUpdateSectionKeyResponse)
9.  [`AdminConfigUpdateSectionRequest`](#AdminConfigUpdateSectionRequest)
10.  [`AdminConfigUpdateSectionResponse`](#AdminConfigUpdateSectionResponse)
11.  [`AdminCoreCreateRequest`](#AdminCoreCreateRequest)
12.  [`AdminCoreCreateResponse`](#AdminCoreCreateResponse)
13.  [`AdminCoreGetDetailResponse`](#AdminCoreGetDetailResponse)
14.  [`AdminHostsGetResponse`](#AdminHostsGetResponse)
15.  [`AdminOperationRequest`](#AdminOperationRequest)
16.  [`AdminOperationResponse`](#AdminOperationResponse)
17.  [`AdminOrganizationCreateRequest`](#AdminOrganizationCreateRequest)
18.  [`AdminOrganizationCreateResponse`](#AdminOrganizationCreateResponse)
19.  [`AdminOrganizationGetDetailResponse`](#AdminOrganizationGetDetailResponse)
20.  [`AdminOrganizationGetTokensResponse`](#AdminOrganizationGetTokensResponse)
21.  [`AdminOrganizationsGetResponse`](#AdminOrganizationsGetResponse)
22.  [`AdminStatusDetail`](#AdminStatusDetail)
23.  [`AdminTokenCreateRequest`](#AdminTokenCreateRequest)
24.  [`AdminTokenCreateResponse`](#AdminTokenCreateResponse)
25.  [`AdminUserCreateRequest`](#AdminUserCreateRequest)
26.  [`AdminUserCreateResponse`](#AdminUserCreateResponse)
27.  [`AdminUserGetDetailResponse`](#AdminUserGetDetailResponse)
28.  [`AdminUserGetTokensResponse`](#AdminUserGetTokensResponse)
29.  [`AdminUserLoginRequest`](#AdminUserLoginRequest)
30.  [`AdminUserLoginResponse`](#AdminUserLoginResponse)
31.  [`AdminUsersGetResponse`](#AdminUsersGetResponse)
32.  [`ArrayOfEngineCategories`](#ArrayOfEngineCategories)
33.  [`ArrayOfEngineInstanceWorkItem`](#ArrayOfEngineInstanceWorkItem)
34.  [`BuildDetail`](#BuildDetail)
35.  [`ConfigKey`](#ConfigKey)
36.  [`ConfigSection`](#ConfigSection)
37.  [`ConfigSectionKey`](#ConfigSectionKey)
38.  [`ContainerStatus`](#ContainerStatus)
39.  [`ContainerTypeEnum`](#ContainerTypeEnum)
40.  [`CoreDetail`](#CoreDetail)
41.  [`CreateCoreDetail`](#CreateCoreDetail)
42.  [`CreateEngineCategoryDetail`](#CreateEngineCategoryDetail)
43.  [`CreateEngineCategoryResponse`](#CreateEngineCategoryResponse)
44.  [`CreateEngineDetail`](#CreateEngineDetail)
45.  [`CreateEngineRequest`](#CreateEngineRequest)
46.  [`CreateEngineResponse`](#CreateEngineResponse)
47.  [`CreateJobDetail`](#CreateJobDetail)
48.  [`CreateJobRequest`](#CreateJobRequest)
49.  [`CreateJobResponse`](#CreateJobResponse)
50.  [`CreateLicenseDetail`](#CreateLicenseDetail)
51.  [`CreateNextJobRequest`](#CreateNextJobRequest)
52.  [`CreateNextJobRequest_jobInfo`](#CreateNextJobRequest_jobInfo)
53.  [`CreateNextJobResponse`](#CreateNextJobResponse)
54.  [`CreateNodRedContainerInfo`](#CreateNodRedContainerInfo)
55.  [`CreateOrganizationDetail`](#CreateOrganizationDetail)
56.  [`CreateServerTypeDetail`](#CreateServerTypeDetail)
57.  [`CreateServerTypeRequest`](#CreateServerTypeRequest)
58.  [`CreateServerTypeResponse`](#CreateServerTypeResponse)
59.  [`CreateTaskDetail`](#CreateTaskDetail)
60.  [`CreateTaskIOInfo`](#CreateTaskIOInfo)
61.  [`CreateTokenDetail`](#CreateTokenDetail)
62.  [`CreateUserDetail`](#CreateUserDetail)
63.  [`DeleteBuildRequest`](#DeleteBuildRequest)
64.  [`DeleteEngineRequest`](#DeleteEngineRequest)
65.  [`DeleteJobRequest`](#DeleteJobRequest)
66.  [`DeleteServerTypeRequest`](#DeleteServerTypeRequest)
67.  [`DesiredServersToServerTypeRequest`](#DesiredServersToServerTypeRequest)
68.  [`DockerRegistry`](#DockerRegistry)
69.  [`DrainHostRequest`](#DrainHostRequest)
70.  [`EngineCategoryDetail`](#EngineCategoryDetail)
71.  [`EngineDetail`](#EngineDetail)
72.  [`EngineInstanceActionEnum`](#EngineInstanceActionEnum)
73.  [`EngineInstanceInfo`](#EngineInstanceInfo)
74.  [`EngineInstanceRegistrationInfo`](#EngineInstanceRegistrationInfo)
75.  [`EngineInstanceStatus`](#EngineInstanceStatus)
76.  [`EngineInstanceStatusModeEnum`](#EngineInstanceStatusModeEnum)
77.  [`EngineInstanceWorkDetailsResponse`](#EngineInstanceWorkDetailsResponse)
78.  [`EngineInstanceWorkDetailsResponse_result`](#EngineInstanceWorkDetailsResponse_result)
79.  [`EngineInstanceWorkItem`](#EngineInstanceWorkItem)
80.  [`EngineInstanceWorkRequest`](#EngineInstanceWorkRequest)
81.  [`EngineInstanceWorkRequestResponse`](#EngineInstanceWorkRequestResponse)
82.  [`EngineInstanceWorkRequestResponse_result`](#EngineInstanceWorkRequestResponse_result)
83.  [`EngineLaunchDetail`](#EngineLaunchDetail)
84.  [`EngineRegistrationActionEnum`](#EngineRegistrationActionEnum)
85.  [`EngineStateEnum`](#EngineStateEnum)
86.  [`EngineStatusEnum`](#EngineStatusEnum)
87.  [`EngineTypeEnum`](#EngineTypeEnum)
88.  [`EnvKeyValue`](#EnvKeyValue)
89.  [`Error`](#Error)
90.  [`FailureReasonEnum`](#FailureReasonEnum)
91.  [`GPUEnum`](#GPUEnum)
92.  [`GetCoresResponse`](#GetCoresResponse)
93.  [`GetEngineBuildResponse`](#GetEngineBuildResponse)
94.  [`GetEngineBuildsResponse`](#GetEngineBuildsResponse)
95.  [`GetEngineCategoriesResponse`](#GetEngineCategoriesResponse)
96.  [`GetEngineCategoryDetailResponse`](#GetEngineCategoryDetailResponse)
97.  [`GetEngineDetailResponse`](#GetEngineDetailResponse)
98.  [`GetEngineLaunchResponse`](#GetEngineLaunchResponse)
99.  [`GetEngineLaunchesResponse`](#GetEngineLaunchesResponse)
100.  [`GetEnginesResponse`](#GetEnginesResponse)
101.  [`GetHostLaunchResponse`](#GetHostLaunchResponse)
102.  [`GetJobDetailResponse`](#GetJobDetailResponse)
103.  [`GetJobListResponse`](#GetJobListResponse)
104.  [`GetJobOutputResponse`](#GetJobOutputResponse)
105.  [`GetJobOutputsResponse`](#GetJobOutputsResponse)
106.  [`GetJobStatusResponse`](#GetJobStatusResponse)
107.  [`GetJobWorkRequestResponse`](#GetJobWorkRequestResponse)
108.  [`GetJobsOrganizationStatsResponse`](#GetJobsOrganizationStatsResponse)
109.  [`GetJobsPerformanceResponse`](#GetJobsPerformanceResponse)
110.  [`GetJobsStatsResponse`](#GetJobsStatsResponse)
111.  [`GetJobsTimeRangesStatsResponse`](#GetJobsTimeRangesStatsResponse)
112.  [`GetLicensesResponse`](#GetLicensesResponse)
113.  [`GetServerTypeResponse`](#GetServerTypeResponse)
114.  [`GetServerTypesResponse`](#GetServerTypesResponse)
115.  [`GetTaskDetailResponse`](#GetTaskDetailResponse)
116.  [`GetTaskOutputResponse`](#GetTaskOutputResponse)
117.  [`GetTaskOutputsResponse`](#GetTaskOutputsResponse)
118.  [`GetTasksEnginesStatsResponse`](#GetTasksEnginesStatsResponse)
119.  [`GetTasksHostsStatsResponse`](#GetTasksHostsStatsResponse)
120.  [`GetTasksResponse`](#GetTasksResponse)
121.  [`GetTasksStatsResponse`](#GetTasksStatsResponse)
122.  [`GetTasksTimeRangesStatsResponse`](#GetTasksTimeRangesStatsResponse)
123.  [`HostAction`](#HostAction)
124.  [`HostActionEnum`](#HostActionEnum)
125.  [`HostActionLaunch`](#HostActionLaunch)
126.  [`HostActionLaunch_containerConfig`](#HostActionLaunch_containerConfig)
127.  [`HostActionModeEnum`](#HostActionModeEnum)
128.  [`HostActionNodeRedLaunch`](#HostActionNodeRedLaunch)
129.  [`HostActionTerminate`](#HostActionTerminate)
130.  [`HostDetail`](#HostDetail)
131.  [`HostDrainReasonEnum`](#HostDrainReasonEnum)
132.  [`HostLaunchConfig`](#HostLaunchConfig)
133.  [`HostLaunchControllerConfig`](#HostLaunchControllerConfig)
134.  [`HostLaunchDetail`](#HostLaunchDetail)
135.  [`HostLaunchNFSConfig`](#HostLaunchNFSConfig)
136.  [`HostLaunchPostgresConfig`](#HostLaunchPostgresConfig)
137.  [`HostLaunchRegistryConfig`](#HostLaunchRegistryConfig)
138.  [`HostMountInfo`](#HostMountInfo)
139.  [`HostMountTypeEnum`](#HostMountTypeEnum)
140.  [`HostRegisterRequest`](#HostRegisterRequest)
141.  [`HostRegisterResponse`](#HostRegisterResponse)
142.  [`HostRegisterResponse_configProperties`](#HostRegisterResponse_configProperties)
143.  [`HostStatus`](#HostStatus)
144.  [`HostStatusContainer`](#HostStatusContainer)
145.  [`HostTerminationReasonEnum`](#HostTerminationReasonEnum)
146.  [`JobDetail`](#JobDetail)
147.  [`JobOutput`](#JobOutput)
148.  [`JobOutputs`](#JobOutputs)
149.  [`JobPerformanceInfo`](#JobPerformanceInfo)
150.  [`JobStatus`](#JobStatus)
151.  [`JobStatusEnum`](#JobStatusEnum)
152.  [`JobWorkRequest`](#JobWorkRequest)
153.  [`JobsCountsInfo`](#JobsCountsInfo)
154.  [`JobsEnginesCountsInfo`](#JobsEnginesCountsInfo)
155.  [`JobsHostsCountsInfo`](#JobsHostsCountsInfo)
156.  [`JobsOrganizationCountsInfo`](#JobsOrganizationCountsInfo)
157.  [`JobsTimeRangesCountsInfo`](#JobsTimeRangesCountsInfo)
158.  [`LaunchActionEnum`](#LaunchActionEnum)
159.  [`LaunchJobTemplateRequest`](#LaunchJobTemplateRequest)
160.  [`LaunchJobTemplateResponse`](#LaunchJobTemplateResponse)
161.  [`LaunchStatusEnum`](#LaunchStatusEnum)
162.  [`LicenseDetail`](#LicenseDetail)
163.  [`OperationSuccess`](#OperationSuccess)
164.  [`OrganizationDetail`](#OrganizationDetail)
165.  [`OrganizationID`](#OrganizationID)
166.  [`PauseBuildRequest`](#PauseBuildRequest)
167.  [`PauseEngineRequest`](#PauseEngineRequest)
168.  [`RecheckJobStatusResponse`](#RecheckJobStatusResponse)
169.  [`RemoveServersToServerTypeRequest`](#RemoveServersToServerTypeRequest)
170.  [`ReplaceEngineRequest`](#ReplaceEngineRequest)
171.  [`ResumeBuildRequest`](#ResumeBuildRequest)
172.  [`ResumeEngineRequest`](#ResumeEngineRequest)
173.  [`RunModeEnum`](#RunModeEnum)
174.  [`ServerProviderEnum`](#ServerProviderEnum)
175.  [`ServerTypeDetail`](#ServerTypeDetail)
176.  [`SortOrderEnum`](#SortOrderEnum)
177.  [`StatusFormatEnum`](#StatusFormatEnum)
178.  [`TaskDetail`](#TaskDetail)
179.  [`TaskIO`](#TaskIO)
180.  [`TaskIOFolder`](#TaskIOFolder)
181.  [`TaskIOInfo`](#TaskIOInfo)
182.  [`TaskIOModeEnum`](#TaskIOModeEnum)
183.  [`TaskIOStatus`](#TaskIOStatus)
184.  [`TaskIOTypeEnum`](#TaskIOTypeEnum)
185.  [`TaskOutput`](#TaskOutput)
186.  [`TaskOutputs`](#TaskOutputs)
187.  [`TaskRouteDetail`](#TaskRouteDetail)
188.  [`TaskStatusDetail`](#TaskStatusDetail)
189.  [`TaskStatusEnum`](#TaskStatusEnum)
190.  [`TasksCountsInfo`](#TasksCountsInfo)
191.  [`TasksEnginesCountsInfo`](#TasksEnginesCountsInfo)
192.  [`TasksHostsCountsInfo`](#TasksHostsCountsInfo)
193.  [`TasksTimeRangesCountsInfo`](#TasksTimeRangesCountsInfo)
194.  [`TerminateHostRequest`](#TerminateHostRequest)
195.  [`TokenDetail`](#TokenDetail)
196.  [`TokenTypeEnum`](#TokenTypeEnum)
197.  [`UpdateBuildResponse`](#UpdateBuildResponse)
198.  [`UpdateEngineCategoryResponse`](#UpdateEngineCategoryResponse)
199.  [`UpdateEngineResponse`](#UpdateEngineResponse)
200.  [`UpdateServerTypeResponse`](#UpdateServerTypeResponse)
201.  [`UserDetail`](#UserDetail)
202.  [`UserStatusEnum`](#UserStatusEnum)
203.  [`WorkRequestStatusEnum`](#WorkRequestStatusEnum)

<div class="model">

### <a name="AddServersToServerTypeRequest" id="AddServersToServerTypeRequest">`AddServersToServerTypeRequest`</a> [Up](#__Models)

<div class="field-items">

<div class="param">serversToAdd (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> The number of servers to add format: int32</div>

</div>

</div>

<div class="model">

### <a name="AdminConfigResponse" id="AdminConfigResponse">`AdminConfigResponse`</a> [Up](#__Models)

<div class="model-description">Response for config request</div>

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[array[ConfigSection]](#ConfigSection)</span> Config sections</div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="AdminConfigSectionKeyResponse" id="AdminConfigSectionKeyResponse">`AdminConfigSectionKeyResponse`</a> [Up](#__Models)

<div class="model-description">Response for config request</div>

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[ConfigKey](#ConfigKey)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="AdminConfigSectionResponse" id="AdminConfigSectionResponse">`AdminConfigSectionResponse`</a> [Up](#__Models)

<div class="model-description">Response for config request</div>

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[ConfigSection](#ConfigSection)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="AdminConfigUpdateRequest" id="AdminConfigUpdateRequest">`AdminConfigUpdateRequest`</a> [Up](#__Models)

<div class="model-description">Request for update config</div>

<div class="field-items">

<div class="param">sections (optional)</div>

<div class="param-desc"><span class="param-type">[array[ConfigSection]](#ConfigSection)</span> Config sections</div>

</div>

</div>

<div class="model">

### <a name="AdminConfigUpdateResponse" id="AdminConfigUpdateResponse">`AdminConfigUpdateResponse`</a> [Up](#__Models)

<div class="model-description">Response for config request</div>

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[array[ConfigSection]](#ConfigSection)</span> Config sections</div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="AdminConfigUpdateSectionKeyRequest" id="AdminConfigUpdateSectionKeyRequest">`AdminConfigUpdateSectionKeyRequest`</a> [Up](#__Models)

<div class="model-description">Request for update config section for a key</div>

<div class="field-items">

<div class="param">key (optional)</div>

<div class="param-desc"><span class="param-type">[ConfigSectionKey](#ConfigSectionKey)</span></div>

</div>

</div>

<div class="model">

### <a name="AdminConfigUpdateSectionKeyResponse" id="AdminConfigUpdateSectionKeyResponse">`AdminConfigUpdateSectionKeyResponse`</a> [Up](#__Models)

<div class="model-description">Response for config request</div>

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[ConfigSectionKey](#ConfigSectionKey)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="AdminConfigUpdateSectionRequest" id="AdminConfigUpdateSectionRequest">`AdminConfigUpdateSectionRequest`</a> [Up](#__Models)

<div class="model-description">Request for update config</div>

<div class="field-items">

<div class="param">section (optional)</div>

<div class="param-desc"><span class="param-type">[ConfigSection](#ConfigSection)</span></div>

</div>

</div>

<div class="model">

### <a name="AdminConfigUpdateSectionResponse" id="AdminConfigUpdateSectionResponse">`AdminConfigUpdateSectionResponse`</a> [Up](#__Models)

<div class="model-description">Response for config request</div>

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[ConfigSection](#ConfigSection)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="AdminCoreCreateRequest" id="AdminCoreCreateRequest">`AdminCoreCreateRequest`</a> [Up](#__Models)

<div class="model-description">This is the request for Create Core</div>

<div class="field-items">

<div class="param">core (optional)</div>

<div class="param-desc"><span class="param-type">[CreateCoreDetail](#CreateCoreDetail)</span></div>

</div>

</div>

<div class="model">

### <a name="AdminCoreCreateResponse" id="AdminCoreCreateResponse">`AdminCoreCreateResponse`</a> [Up](#__Models)

<div class="model-description">This is the response for Create Core Request</div>

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[CoreDetail](#CoreDetail)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="AdminCoreGetDetailResponse" id="AdminCoreGetDetailResponse">`AdminCoreGetDetailResponse`</a> [Up](#__Models)

<div class="model-description">This is the response for get Core Detail Request</div>

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[CoreDetail](#CoreDetail)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="AdminHostsGetResponse" id="AdminHostsGetResponse">`AdminHostsGetResponse`</a> [Up](#__Models)

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[array[HostDetail]](#HostDetail)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="AdminOperationRequest" id="AdminOperationRequest">`AdminOperationRequest`</a> [Up](#__Models)

<div class="model-description">Request to terminate the cluster</div>

<div class="field-items">

<div class="param">clusterID (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> Cluster ID</div>

</div>

</div>

<div class="model">

### <a name="AdminOperationResponse" id="AdminOperationResponse">`AdminOperationResponse`</a> [Up](#__Models)

<div class="model-description">Response from operation</div>

<div class="field-items">

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="AdminOrganizationCreateRequest" id="AdminOrganizationCreateRequest">`AdminOrganizationCreateRequest`</a> [Up](#__Models)

<div class="model-description">This is the request for Create Organization</div>

<div class="field-items">

<div class="param">organization (optional)</div>

<div class="param-desc"><span class="param-type">[CreateOrganizationDetail](#CreateOrganizationDetail)</span></div>

</div>

</div>

<div class="model">

### <a name="AdminOrganizationCreateResponse" id="AdminOrganizationCreateResponse">`AdminOrganizationCreateResponse`</a> [Up](#__Models)

<div class="model-description">This is the response for Create Organization Request</div>

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[OrganizationDetail](#OrganizationDetail)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="AdminOrganizationGetDetailResponse" id="AdminOrganizationGetDetailResponse">`AdminOrganizationGetDetailResponse`</a> [Up](#__Models)

<div class="model-description">This is the response for get Organization Detail Request</div>

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[OrganizationDetail](#OrganizationDetail)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="AdminOrganizationGetTokensResponse" id="AdminOrganizationGetTokensResponse">`AdminOrganizationGetTokensResponse`</a> [Up](#__Models)

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[array[TokenDetail]](#TokenDetail)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="AdminOrganizationsGetResponse" id="AdminOrganizationsGetResponse">`AdminOrganizationsGetResponse`</a> [Up](#__Models)

<div class="model-description">This is the response for get Organization Detail Request</div>

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[array[OrganizationDetail]](#OrganizationDetail)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="AdminStatusDetail" id="AdminStatusDetail">`AdminStatusDetail`</a> [Up](#__Models)

<div class="model-description">Information about the edge cluster</div>

<div class="field-items">

<div class="param">clusterID (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> Cluster ID</div>

</div>

</div>

<div class="model">

### <a name="AdminTokenCreateRequest" id="AdminTokenCreateRequest">`AdminTokenCreateRequest`</a> [Up](#__Models)

<div class="model-description">This is the request for Create Token</div>

<div class="field-items">

<div class="param">token (optional)</div>

<div class="param-desc"><span class="param-type">[CreateTokenDetail](#CreateTokenDetail)</span></div>

</div>

</div>

<div class="model">

### <a name="AdminTokenCreateResponse" id="AdminTokenCreateResponse">`AdminTokenCreateResponse`</a> [Up](#__Models)

<div class="model-description">This is the response for Create Token Request</div>

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[TokenDetail](#TokenDetail)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="AdminUserCreateRequest" id="AdminUserCreateRequest">`AdminUserCreateRequest`</a> [Up](#__Models)

<div class="model-description">This is the request for Create User</div>

<div class="field-items">

<div class="param">user (optional)</div>

<div class="param-desc"><span class="param-type">[CreateUserDetail](#CreateUserDetail)</span></div>

</div>

</div>

<div class="model">

### <a name="AdminUserCreateResponse" id="AdminUserCreateResponse">`AdminUserCreateResponse`</a> [Up](#__Models)

<div class="model-description">This is the response for Create User Request</div>

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[UserDetail](#UserDetail)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="AdminUserGetDetailResponse" id="AdminUserGetDetailResponse">`AdminUserGetDetailResponse`</a> [Up](#__Models)

<div class="model-description">This is the response for get User Detail Request</div>

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[UserDetail](#UserDetail)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="AdminUserGetTokensResponse" id="AdminUserGetTokensResponse">`AdminUserGetTokensResponse`</a> [Up](#__Models)

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[array[TokenDetail]](#TokenDetail)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="AdminUserLoginRequest" id="AdminUserLoginRequest">`AdminUserLoginRequest`</a> [Up](#__Models)

<div class="field-items">

<div class="param">password (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">username (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

</div>

</div>

<div class="model">

### <a name="AdminUserLoginResponse" id="AdminUserLoginResponse">`AdminUserLoginResponse`</a> [Up](#__Models)

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[UserDetail](#UserDetail)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

<div class="param">token (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

</div>

</div>

<div class="model">

### <a name="AdminUsersGetResponse" id="AdminUsersGetResponse">`AdminUsersGetResponse`</a> [Up](#__Models)

<div class="model-description">This is the response for get User Detail Request</div>

<div class="field-items">

<div class="param">count (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> Total records for the query</div>

<div class="param">limit (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> the number of jobs to return.</div>

<div class="param">offset (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> the number of jobs to skip before getting the result set</div>

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[array[UserDetail]](#UserDetail)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="ArrayOfEngineCategories" id="ArrayOfEngineCategories">`ArrayOfEngineCategories`</a> [Up](#__Models)

</div>

<div class="model">

### <a name="ArrayOfEngineInstanceWorkItem" id="ArrayOfEngineInstanceWorkItem">`ArrayOfEngineInstanceWorkItem`</a> [Up](#__Models)

</div>

<div class="model">

### <a name="BuildDetail" id="BuildDetail">`BuildDetail`</a> [Up](#__Models)

<div class="field-items">

<div class="param">buildDefaultTTL (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> The seconds on average a build should live if utilized format: int32</div>

<div class="param">buildID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">buildState (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> Build State</div>

<div class="param">createdDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the core was created format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">diskFreeBytes (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> The number of free bytes required to launch engine format: int32</div>

<div class="param">dockerImage (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> docker image</div>

<div class="param">engineID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">licenseExpirationTimestamp (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> The unix timestamp on when the license for the engine expires. If 0, then it does not expire format: int64</div>

<div class="param">manifestClusterSize (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> Engine Size from the Manifest</div>

<div class="param">manifestCustomProfile (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> Engine Custom Profile from the Manifest</div>

<div class="param">manifestEngineMode (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> Engine Mode from the Manifest</div>

<div class="param">manifestEngineName (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> Name of the Engine from the Manifest</div>

<div class="param">manifestGPUSupported (optional)</div>

<div class="param-desc"><span class="param-type">[GPUEnum](#GPUEnum)</span></div>

<div class="param">manifestRequireEC2 (optional)</div>

<div class="param-desc"><span class="param-type">[Boolean](#boolean)</span> Does the engine require EC2</div>

<div class="param">modifiedDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the core was last modified. format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">softGPULimit (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> The number of GPU required to launch engine format: int32</div>

<div class="param">softMemoryBytesLimit (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> The number of bytes required to launch this engine format: int32</div>

<div class="param">softVCPULimit (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> The number of VCPU based on 1024 required to launch engine format: int32</div>

<div class="param">version (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> version of the engine format: int32</div>

</div>

</div>

<div class="model">

### <a name="ConfigKey" id="ConfigKey">`ConfigKey`</a> [Up](#__Models)

</div>

<div class="model">

### <a name="ConfigSection" id="ConfigSection">`ConfigSection`</a> [Up](#__Models)

<div class="model-description">This contains the keys in a particular config section</div>

<div class="field-items">

<div class="param">keys (optional)</div>

<div class="param-desc"><span class="param-type">[array[ConfigSectionKey]](#ConfigSectionKey)</span> Config Keys</div>

<div class="param">section (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> The section for the config key</div>

</div>

</div>

<div class="model">

### <a name="ConfigSectionKey" id="ConfigSectionKey">`ConfigSectionKey`</a> [Up](#__Models)

<div class="model-description">Config Key Object</div>

<div class="field-items">

<div class="param">createdDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the core was created format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">key (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> The Key</div>

<div class="param">kvpJSON (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> The KVP as JSON format format: json</div>

<div class="param">modifiedDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the core was last modified. format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">section (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> The section for the config key</div>

<div class="param">value (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> The value for the Key</div>

</div>

</div>

<div class="model">

### <a name="ContainerStatus" id="ContainerStatus">`ContainerStatus`</a> [Up](#__Models)

</div>

<div class="model">

### <a name="ContainerTypeEnum" id="ContainerTypeEnum">`ContainerTypeEnum`</a> [Up](#__Models)

</div>

<div class="model">

### <a name="CoreDetail" id="CoreDetail">`CoreDetail`</a> [Up](#__Models)

<div class="field-items">

<div class="param">adhoc (optional)</div>

<div class="param-desc"><span class="param-type">[Boolean](#boolean)</span> Download adhoc jobs</div>

<div class="param">baseUrl (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> format: url</div>

<div class="param">clusterID (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> Cluster ID</div>

<div class="param">coreID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">coreUrl (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> format: url</div>

<div class="param">createdDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the core was created format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">endpoint (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param-desc"><span class="param-type">example: /v3/graphql</span></div>

<div class="param">isEnabled (optional)</div>

<div class="param-desc"><span class="param-type">[Boolean](#boolean)</span> Is the core enabled</div>

<div class="param">modifiedDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the core was last modified. format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">scheduled (optional)</div>

<div class="param-desc"><span class="param-type">[Boolean](#boolean)</span> Download scheduled jobs</div>

<div class="param">token (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

</div>

</div>

<div class="model">

### <a name="CreateCoreDetail" id="CreateCoreDetail">`CreateCoreDetail`</a> [Up](#__Models)

<div class="field-items">

<div class="param">adhoc (optional)</div>

<div class="param-desc"><span class="param-type">[Boolean](#boolean)</span> Download adhoc jobs</div>

<div class="param">baseUrl (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> format: url</div>

<div class="param">clusterID (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> Cluster ID</div>

<div class="param">coreUrl (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> format: url</div>

<div class="param">endpoint (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param-desc"><span class="param-type">example: /v3/graphql</span></div>

<div class="param">isEnabled (optional)</div>

<div class="param-desc"><span class="param-type">[Boolean](#boolean)</span> Is the core enabled</div>

<div class="param">scheduled (optional)</div>

<div class="param-desc"><span class="param-type">[Boolean](#boolean)</span> Download scheduled jobs</div>

<div class="param">token (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

</div>

</div>

<div class="model">

### <a name="CreateEngineCategoryDetail" id="CreateEngineCategoryDetail">`CreateEngineCategoryDetail`</a> [Up](#__Models)

<div class="model-description">These are the fields required to create an engine category.</div>

<div class="field-items">

<div class="param">engineCategoryName (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> The name of the engine category</div>

<div class="param">engineCategoryType (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> The type of the category</div>

</div>

</div>

<div class="model">

### <a name="CreateEngineCategoryResponse" id="CreateEngineCategoryResponse">`CreateEngineCategoryResponse`</a> [Up](#__Models)

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[EngineCategoryDetail](#EngineCategoryDetail)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="CreateEngineDetail" id="CreateEngineDetail">`CreateEngineDetail`</a> [Up](#__Models)

<div class="field-items">

<div class="param">applicationIDsJSON (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> JSON Data for application_id format: json</div>

<div class="param">child_priority_adjustment_on_complete (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> When this task completes, adjust the priority of child tasks by this value format: int32</div>

<div class="param">dependencyJSON (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> JSON Data for dependency format: json</div>

<div class="param">dontrunComplete (optional)</div>

<div class="param-desc"><span class="param-type">[Boolean](#boolean)</span> If true, do not run this engine. Complete as soon as possible and do not assign work.</div>

<div class="param">edge_version (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> edge version of the engine format: int32</div>

<div class="param">engineCategoryID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> The UUID of the Engine Category format: uuid</div>

<div class="param">engineID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">engineName (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> Name of the Engine</div>

<div class="param">engineOutputType (optional)</div>

<div class="param-desc"><span class="param-type">[EngineTypeEnum](#EngineTypeEnum)</span></div>

<div class="param">engineState (optional)</div>

<div class="param-desc"><span class="param-type">[EngineStateEnum](#EngineStateEnum)</span></div>

<div class="param">engineType (optional)</div>

<div class="param-desc"><span class="param-type">[EngineTypeEnum](#EngineTypeEnum)</span></div>

<div class="param">fieldsJSON (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> JSON Data for fields format: json</div>

<div class="param">internalOrganizationID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">jwtRightsJSON (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> JSON Data for jwt_rights format: json</div>

<div class="param">parallelProcessing (optional)</div>

<div class="param-desc"><span class="param-type">[Boolean](#boolean)</span> If true, the engine can handle multiple instances working against the same chunk task.</div>

<div class="param">parentCompleteBeforeStart (optional)</div>

<div class="param-desc"><span class="param-type">[Boolean](#boolean)</span> If true, the engine waits for the parent(s) to be complete before starting</div>

<div class="param">priority_adjustment (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> On new tasks with this engine, add this value to the priority of that task format: int32</div>

<div class="param">replacementEngineID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">validationJSON (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> JSON Data for validation format: json</div>

</div>

</div>

<div class="model">

### <a name="CreateEngineRequest" id="CreateEngineRequest">`CreateEngineRequest`</a> [Up](#__Models)

<div class="field-items">

<div class="param">engine (optional)</div>

<div class="param-desc"><span class="param-type">[CreateEngineDetail](#CreateEngineDetail)</span></div>

</div>

</div>

<div class="model">

### <a name="CreateEngineResponse" id="CreateEngineResponse">`CreateEngineResponse`</a> [Up](#__Models)

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[EngineDetail](#EngineDetail)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="CreateJobDetail" id="CreateJobDetail">`CreateJobDetail`</a> [Up](#__Models)

<div class="field-items">

<div class="param">coreID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">coreJobID (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> This is the core job id associated with this job</div>

<div class="param">coreRecordingID (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> This is the recording id in the core of the content for this job format: int64</div>

<div class="param">coreSourceID (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> This is the Core Source Id format: int64</div>

<div class="param">currentRetries (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> This is the current retries for the job</div>

<div class="param">dueDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the time the job is due to be complete. This is used by edge to set the priorities. format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">internalOrganizationID</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">jobConfigJSON (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> This is the job config expressed as JSON format: JSON</div>

<div class="param">jobStatus (optional)</div>

<div class="param-desc"><span class="param-type">[JobStatusEnum](#JobStatusEnum)</span></div>

<div class="param">taskRoutes (optional)</div>

<div class="param-desc"><span class="param-type">[array[TaskRouteDetail]](#TaskRouteDetail)</span></div>

<div class="param">tasks (optional)</div>

<div class="param-desc"><span class="param-type">[array[CreateTaskDetail]](#CreateTaskDetail)</span></div>

</div>

</div>

<div class="model">

### <a name="CreateJobRequest" id="CreateJobRequest">`CreateJobRequest`</a> [Up](#__Models)

<div class="field-items">

<div class="param">jobs (optional)</div>

<div class="param-desc"><span class="param-type">[array[CreateJobDetail]](#CreateJobDetail)</span></div>

</div>

</div>

<div class="model">

### <a name="CreateJobResponse" id="CreateJobResponse">`CreateJobResponse`</a> [Up](#__Models)

<div class="field-items">

<div class="param">internalJobIds (optional)</div>

<div class="param-desc"><span class="param-type">[array[String]](#string)</span></div>

</div>

</div>

<div class="model">

### <a name="CreateLicenseDetail" id="CreateLicenseDetail">`CreateLicenseDetail`</a> [Up](#__Models)

<div class="model-description">This provides the detailed information about the license.</div>

<div class="field-items">

<div class="param">licenseKey (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> This is the encoded license string</div>

</div>

</div>

<div class="model">

### <a name="CreateNextJobRequest" id="CreateNextJobRequest">`CreateNextJobRequest`</a> [Up](#__Models)

<div class="field-items">

<div class="param">jobInfo (optional)</div>

<div class="param-desc"><span class="param-type">[CreateNextJobRequest_jobInfo](#CreateNextJobRequest_jobInfo)</span></div>

</div>

</div>

<div class="model">

### <a name="CreateNextJobRequest_jobInfo" id="CreateNextJobRequest_jobInfo">`CreateNextJobRequest_jobInfo`</a> [Up](#__Models)

<div class="model-description">Configuration for the first task in the next job template in the pipeline</div>

<div class="field-items">

<div class="param">payloadJSON (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> Payload to use for first task in the next job template in the pipeline format: json</div>

</div>

</div>

<div class="model">

### <a name="CreateNextJobResponse" id="CreateNextJobResponse">`CreateNextJobResponse`</a> [Up](#__Models)

<div class="field-items">

<div class="param">operation (optional)</div>

<div class="param-desc"><span class="param-type">[AdminOperationResponse](#AdminOperationResponse)</span></div>

</div>

</div>

<div class="model">

### <a name="CreateNodRedContainerInfo" id="CreateNodRedContainerInfo">`CreateNodRedContainerInfo`</a> [Up](#__Models)

<div class="field-items">

<div class="param">automateContainerID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> The UUID of the Automate Container format: uuid</div>

<div class="param">buildID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">containerID (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> This is the docker container id the engine instance</div>

<div class="param">createdDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the core was created format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">engineID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">hostID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">hostIP (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> IP of the host which include NR container</div>

<div class="param">modifiedDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the core was last modified. format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">port (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> Port of the NR container</div>

<div class="param">userID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

</div>

</div>

<div class="model">

### <a name="CreateOrganizationDetail" id="CreateOrganizationDetail">`CreateOrganizationDetail`</a> [Up](#__Models)

<div class="field-items">

<div class="param">applicationID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">basePriority (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span></div>

<div class="param">coreOrganizationID (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span></div>

<div class="param">createdDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the core was created format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">defaultRetries (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span></div>

<div class="param">defaultSLASeconds (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span></div>

<div class="param">kvpJSON (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> format: json</div>

<div class="param">modifiedDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the core was last modified. format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">name (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">taskPriorityAdjustmentStarted (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span></div>

</div>

</div>

<div class="model">

### <a name="CreateServerTypeDetail" id="CreateServerTypeDetail">`CreateServerTypeDetail`</a> [Up](#__Models)

<div class="field-items">

<div class="param">agentStartupScript (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">awsAmi (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">awsInstanceProfile (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">awsInstanceType (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">awsKeyName (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">awsSecurityGroups (optional)</div>

<div class="param-desc"><span class="param-type">[array[String]](#string)</span> aws subnets</div>

<div class="param">awsSpot (optional)</div>

<div class="param-desc"><span class="param-type">[Boolean](#boolean)</span></div>

<div class="param">awsSpotMaxPrice (optional)</div>

<div class="param-desc"><span class="param-type">[Float](#float)</span> format: float</div>

<div class="param">awsSpotPersistent (optional)</div>

<div class="param-desc"><span class="param-type">[Boolean](#boolean)</span></div>

<div class="param">awsSubnets (optional)</div>

<div class="param-desc"><span class="param-type">[array[String]](#string)</span> aws subnets</div>

<div class="param">awsTagsJSON (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> format: json</div>

<div class="param">awsUserData (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">gpuType (optional)</div>

<div class="param-desc"><span class="param-type">[GPUEnum](#GPUEnum)</span></div>

<div class="param">hasGPU (optional)</div>

<div class="param-desc"><span class="param-type">[Boolean](#boolean)</span></div>

<div class="param">isAutoScaleActive (optional)</div>

<div class="param-desc"><span class="param-type">[Boolean](#boolean)</span></div>

<div class="param">maxServers (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> format: int64</div>

<div class="param">memoryBytes (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> format: int64</div>

<div class="param">minServers (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> format: int64</div>

<div class="param">numGPU (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> format: int64</div>

<div class="param">onlyOrganizationId (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">runModes (optional)</div>

<div class="param-desc"><span class="param-type">[array[RunModeEnum]](#RunModeEnum)</span> run modes</div>

<div class="param">serverConfigJSON (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> format: json</div>

<div class="param">serverProvider (optional)</div>

<div class="param-desc"><span class="param-type">[ServerProviderEnum](#ServerProviderEnum)</span></div>

<div class="param">serverTypeID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">vcpus (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> format: int64</div>

</div>

</div>

<div class="model">

### <a name="CreateServerTypeRequest" id="CreateServerTypeRequest">`CreateServerTypeRequest`</a> [Up](#__Models)

<div class="model-description">This is the request for Create Server Type</div>

<div class="field-items">

<div class="param">serverType (optional)</div>

<div class="param-desc"><span class="param-type">[CreateServerTypeDetail](#CreateServerTypeDetail)</span></div>

</div>

</div>

<div class="model">

### <a name="CreateServerTypeResponse" id="CreateServerTypeResponse">`CreateServerTypeResponse`</a> [Up](#__Models)

<div class="model-description">This is the response for Create Server Type</div>

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[ServerTypeDetail](#ServerTypeDetail)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="CreateTaskDetail" id="CreateTaskDetail">`CreateTaskDetail`</a> [Up](#__Models)

<div class="field-items">

<div class="param">coreTaskId (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> This is the core task id associated with this job</div>

<div class="param">correlationTaskId (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> Correlation Task Id. On create, this will be used instead of internalTaskId or coreTaskId on routes</div>

<div class="param">dueDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the time the task is due to be complete. This is used by edge to set the priorities. format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">engineId</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> The engineId to use. If the engine is not available on edge, this will return an exception format: uuid</div>

<div class="param">ioFolders (optional)</div>

<div class="param-desc"><span class="param-type">[array[CreateTaskIOInfo]](#CreateTaskIOInfo)</span></div>

<div class="param">maxEngines (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> The maximum number of engine instances to run against this task. Defaults to 1 if parallelProcessing is false, or 2 otherwise.</div>

<div class="param">maxRetries (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> This is the max retries for the task</div>

<div class="param">parallelProcessing (optional)</div>

<div class="param-desc"><span class="param-type">[Boolean](#boolean)</span> If true, multiple engine instances can process this task in parallel. If false, maxEngines will be 1\.</div>

<div class="param">parentMustBeCompleteBeforeStarting (optional)</div>

<div class="param-desc"><span class="param-type">[Boolean](#boolean)</span> If true, this task won't start until the parent is complete</div>

<div class="param">payloadJSON (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> This is the payload encoded as a JSON string format: json</div>

<div class="param">priority (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> The priority for the task. Default is 0\. format: int32</div>

<div class="param">taskPayloadJSON (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> This is the taskPayload as a JSON string format: json</div>

<div class="param">taskStatus (optional)</div>

<div class="param-desc"><span class="param-type">[JobStatusEnum](#JobStatusEnum)</span></div>

</div>

</div>

<div class="model">

### <a name="CreateTaskIOInfo" id="CreateTaskIOInfo">`CreateTaskIOInfo`</a> [Up](#__Models)

<div class="model-description">This is the task IO Object that provides paramenters for the input and output</div>

<div class="field-items">

<div class="param">correlationID (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> On create, this field will be used to look up task routes for binding.</div>

<div class="param">mode (optional)</div>

<div class="param-desc"><span class="param-type">[TaskIOModeEnum](#TaskIOModeEnum)</span></div>

<div class="param">optionsJSON (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> Any options for this input or output folder for the task to use on processing format: json</div>

<div class="param">type (optional)</div>

<div class="param-desc"><span class="param-type">[TaskIOTypeEnum](#TaskIOTypeEnum)</span></div>

</div>

</div>

<div class="model">

### <a name="CreateTokenDetail" id="CreateTokenDetail">`CreateTokenDetail`</a> [Up](#__Models)

<div class="field-items">

<div class="param">apiRateLimitHour (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> format: int64</div>

<div class="param">bytesRateLimitHour (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> format: int64</div>

<div class="param">engineInstanceID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">expiration (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the core was created format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">hostID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">kvpJSON (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> format: json</div>

<div class="param">maxAPI (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> format: int64</div>

<div class="param">maxBytes (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> format: int64</div>

<div class="param">maxTasks (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> format: int64</div>

<div class="param">organizationIDs (optional)</div>

<div class="param-desc"><span class="param-type">[array[OrganizationID]](#OrganizationID)</span></div>

<div class="param">taskRateLimitHour (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> format: int64</div>

<div class="param">type (optional)</div>

<div class="param-desc"><span class="param-type">[TokenTypeEnum](#TokenTypeEnum)</span></div>

</div>

</div>

<div class="model">

### <a name="CreateUserDetail" id="CreateUserDetail">`CreateUserDetail`</a> [Up](#__Models)

<div class="field-items">

<div class="param">displayName (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">email (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> format: email</div>

<div class="param">internalOrganizationID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">kvpJSON (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> format: json</div>

<div class="param">password (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">passwordChangeRequired (optional)</div>

<div class="param-desc"><span class="param-type">[Boolean](#boolean)</span></div>

<div class="param">status (optional)</div>

<div class="param-desc"><span class="param-type">[UserStatusEnum](#UserStatusEnum)</span></div>

<div class="param">userID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">userName (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">userSettingsJSON (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> format: json</div>

</div>

</div>

<div class="model">

### <a name="DeleteBuildRequest" id="DeleteBuildRequest">`DeleteBuildRequest`</a> [Up](#__Models)

<div class="field-items">

<div class="param">buildID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">engineID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

</div>

</div>

<div class="model">

### <a name="DeleteEngineRequest" id="DeleteEngineRequest">`DeleteEngineRequest`</a> [Up](#__Models)

<div class="field-items">

<div class="param">engineID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

</div>

</div>

<div class="model">

### <a name="DeleteJobRequest" id="DeleteJobRequest">`DeleteJobRequest`</a> [Up](#__Models)

<div class="field-items">

<div class="param">jobID (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> Core Job ID format: string</div>

</div>

</div>

<div class="model">

### <a name="DeleteServerTypeRequest" id="DeleteServerTypeRequest">`DeleteServerTypeRequest`</a> [Up](#__Models)

<div class="field-items">

<div class="param">serverTypeID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

</div>

</div>

<div class="model">

### <a name="DesiredServersToServerTypeRequest" id="DesiredServersToServerTypeRequest">`DesiredServersToServerTypeRequest`</a> [Up](#__Models)

<div class="field-items">

<div class="param">desiredServers (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> The number of servers for this server type format: int32</div>

</div>

</div>

<div class="model">

### <a name="DockerRegistry" id="DockerRegistry">`DockerRegistry`</a> [Up](#__Models)

<div class="field-items">

<div class="param">dockerPassword (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> This is the password for the docker username</div>

<div class="param">dockerRegistryURL (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">dockerUsername (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> This is the username that provides access to the docker registry to pull images</div>

<div class="param">isAIWareRegistry (optional)</div>

<div class="param-desc"><span class="param-type">[Boolean](#boolean)</span></div>

<div class="param">name (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> This is the name for the Repo</div>

<div class="param">token (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> This is a token to use for authentication</div>

</div>

</div>

<div class="model">

### <a name="DrainHostRequest" id="DrainHostRequest">`DrainHostRequest`</a> [Up](#__Models)

<div class="field-items">

<div class="param">detail (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">reason (optional)</div>

<div class="param-desc"><span class="param-type">[HostDrainReasonEnum](#HostDrainReasonEnum)</span></div>

</div>

</div>

<div class="model">

### <a name="EngineCategoryDetail" id="EngineCategoryDetail">`EngineCategoryDetail`</a> [Up](#__Models)

<div class="field-items">

<div class="param">createdDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the core was created format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">engineCategoryID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> The engine category ID. format: uuid</div>

<div class="param">engineCategoryName (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> The name of the engine category</div>

<div class="param">engineCategoryType (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> The type of the category</div>

<div class="param">modifiedDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the core was last modified. format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

</div>

</div>

<div class="model">

### <a name="EngineDetail" id="EngineDetail">`EngineDetail`</a> [Up](#__Models)

<div class="field-items">

<div class="param">applicationIDsJSON (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> JSON Data for application_id format: json</div>

<div class="param">child_priority_adjustment_on_complete (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> When this task completes, adjust the priority of child tasks by this value format: int32</div>

<div class="param">createdDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the core was created format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">dependencyJSON (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> JSON Data for dependency format: json</div>

<div class="param">dontrunComplete (optional)</div>

<div class="param-desc"><span class="param-type">[Boolean](#boolean)</span> If true, do not run this engine. Complete as soon as possible and do not assign work.</div>

<div class="param">edge_version (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> edge version of the engine format: int32</div>

<div class="param">engineCategoryID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> The UUID of the Engine Category format: uuid</div>

<div class="param">engineID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">engineName (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> Name of the Engine</div>

<div class="param">engineOutputType (optional)</div>

<div class="param-desc"><span class="param-type">[EngineTypeEnum](#EngineTypeEnum)</span></div>

<div class="param">engineState (optional)</div>

<div class="param-desc"><span class="param-type">[EngineStateEnum](#EngineStateEnum)</span></div>

<div class="param">engineType (optional)</div>

<div class="param-desc"><span class="param-type">[EngineTypeEnum](#EngineTypeEnum)</span></div>

<div class="param">fieldsJSON (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> JSON Data for fields format: json</div>

<div class="param">internalOrganizationID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">jwtRightsJSON (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> JSON Data for jwt_rights format: json</div>

<div class="param">modifiedDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the core was last modified. format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">parallelProcessing (optional)</div>

<div class="param-desc"><span class="param-type">[Boolean](#boolean)</span> If true, the engine can handle multiple instances working against the same chunk task.</div>

<div class="param">parentCompleteBeforeStart (optional)</div>

<div class="param-desc"><span class="param-type">[Boolean](#boolean)</span> If true, the engine waits for the parent(s) to be complete before starting</div>

<div class="param">priority_adjustment (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> On new tasks with this engine, add this value to the priority of that task format: int32</div>

<div class="param">replacementEngineID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">validationJSON (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> JSON Data for validation format: json</div>

</div>

</div>

<div class="model">

### <a name="EngineInstanceActionEnum" id="EngineInstanceActionEnum">`EngineInstanceActionEnum`</a> [Up](#__Models)

</div>

<div class="model">

### <a name="EngineInstanceInfo" id="EngineInstanceInfo">`EngineInstanceInfo`</a> [Up](#__Models)

<div class="model-description">EngineInstance Information</div>

<div class="field-items">

<div class="param">additionalEngineIDs (optional)</div>

<div class="param-desc"><span class="param-type">[array[String]](#string)</span> This is a list of additional engines this instance can handle</div>

<div class="param">buildID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">dockerContainerID (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> The docker container PID</div>

<div class="param">engineID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">engineInstanceID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">engineToolkitVersion (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> The engine toolkit version</div>

<div class="param">errors (optional)</div>

<div class="param-desc"><span class="param-type">[array[Error]](#Error)</span></div>

<div class="param">hostID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">launchEnvVariables (optional)</div>

<div class="param-desc"><span class="param-type">[Object](#object)</span></div>

<div class="param">launchID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">launchStatus (optional)</div>

<div class="param-desc"><span class="param-type">[LaunchStatusEnum](#LaunchStatusEnum)</span></div>

<div class="param">launchStatusInfo (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> Additional to log about launch status</div>

<div class="param">licenseExpirationSeconds (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> Seconds till the license expires</div>

<div class="param">runtimeExpirationSeconds (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> Seconds till runtime should expire</div>

<div class="param">startupTimestamp (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> Timestamp of engine instance startup in UTC format: int64</div>

<div class="param">status (optional)</div>

<div class="param-desc"><span class="param-type">[EngineStatusEnum](#EngineStatusEnum)</span></div>

<div class="param">warnings (optional)</div>

<div class="param-desc"><span class="param-type">[array[Error]](#Error)</span></div>

</div>

</div>

<div class="model">

### <a name="EngineInstanceRegistrationInfo" id="EngineInstanceRegistrationInfo">`EngineInstanceRegistrationInfo`</a> [Up](#__Models)

<div class="field-items">

<div class="param">action (optional)</div>

<div class="param-desc"><span class="param-type">[EngineRegistrationActionEnum](#EngineRegistrationActionEnum)</span></div>

<div class="param">engineInstanceID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">engineInstanceToken (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> This is the security token the engine must use on other calls</div>

<div class="param">runtimeExpirationSeconds (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span></div>

</div>

</div>

<div class="model">

### <a name="EngineInstanceStatus" id="EngineInstanceStatus">`EngineInstanceStatus`</a> [Up](#__Models)

<div class="model-description">payload for updateEngineInstanceStatus API -</div>

<div class="field-items">

<div class="param">containerStatus (optional)</div>

<div class="param-desc"><span class="param-type">[ContainerStatus](#ContainerStatus)</span></div>

<div class="param">hostID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">mode (optional)</div>

<div class="param-desc"><span class="param-type">[EngineInstanceStatusModeEnum](#EngineInstanceStatusModeEnum)</span></div>

<div class="param">priorTimestamp (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> UTC Timestamp of last status update or start of new task format: int64</div>

<div class="param">secondsToTTL (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span></div>

<div class="param">taskStatuses (optional)</div>

<div class="param-desc"><span class="param-type">[array[TaskStatusDetail]](#TaskStatusDetail)</span></div>

<div class="param">timestamp (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> UTC Timestamp of NOW() format: int64</div>

<div class="param">workRequestDetails (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">workRequestID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">workRequestStatus (optional)</div>

<div class="param-desc"><span class="param-type">[WorkRequestStatusEnum](#WorkRequestStatusEnum)</span></div>

</div>

</div>

<div class="model">

### <a name="EngineInstanceStatusModeEnum" id="EngineInstanceStatusModeEnum">`EngineInstanceStatusModeEnum`</a> [Up](#__Models)

</div>

<div class="model">

### <a name="EngineInstanceWorkDetailsResponse" id="EngineInstanceWorkDetailsResponse">`EngineInstanceWorkDetailsResponse`</a> [Up](#__Models)

<div class="model-description">response payload for workdetail</div>

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[EngineInstanceWorkDetailsResponse_result](#EngineInstanceWorkDetailsResponse_result)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="EngineInstanceWorkDetailsResponse_result" id="EngineInstanceWorkDetailsResponse_result">`EngineInstanceWorkDetailsResponse_result`</a> [Up](#__Models)

<div class="field-items">

<div class="param">workItem (optional)</div>

<div class="param-desc"><span class="param-type">[ArrayOfEngineInstanceWorkItem](#ArrayOfEngineInstanceWorkItem)</span></div>

<div class="param">workRequestDetails (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">workRequestID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">workRequestStatus (optional)</div>

<div class="param-desc"><span class="param-type">[WorkRequestStatusEnum](#WorkRequestStatusEnum)</span></div>

</div>

</div>

<div class="model">

### <a name="EngineInstanceWorkItem" id="EngineInstanceWorkItem">`EngineInstanceWorkItem`</a> [Up](#__Models)

</div>

<div class="model">

### <a name="EngineInstanceWorkRequest" id="EngineInstanceWorkRequest">`EngineInstanceWorkRequest`</a> [Up](#__Models)

<div class="field-items">

<div class="param">containerStatus (optional)</div>

<div class="param-desc"><span class="param-type">[ContainerStatus](#ContainerStatus)</span></div>

<div class="param">hostAction (optional)</div>

<div class="param-desc"><span class="param-type">[HostActionEnum](#HostActionEnum)</span></div>

<div class="param">hostID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">requestWorkForEngineIds (optional)</div>

<div class="param-desc"><span class="param-type">[array[String]](#string)</span> This is the set of engine ids that this instance will get work for. Controller will return the highest priority task across the set of engine ids</div>

<div class="param">taskStatuses (optional)</div>

<div class="param-desc"><span class="param-type">[array[TaskStatusDetail]](#TaskStatusDetail)</span></div>

<div class="param">workRequestDetails (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">workRequestID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">workRequestStatus (optional)</div>

<div class="param-desc"><span class="param-type">[WorkRequestStatusEnum](#WorkRequestStatusEnum)</span></div>

</div>

</div>

<div class="model">

### <a name="EngineInstanceWorkRequestResponse" id="EngineInstanceWorkRequestResponse">`EngineInstanceWorkRequestResponse`</a> [Up](#__Models)

</div>

<div class="model">

### <a name="EngineInstanceWorkRequestResponse_result" id="EngineInstanceWorkRequestResponse_result">`EngineInstanceWorkRequestResponse_result`</a> [Up](#__Models)

<div class="field-items">

<div class="param">action (optional)</div>

<div class="param-desc"><span class="param-type">[EngineInstanceActionEnum](#EngineInstanceActionEnum)</span></div>

<div class="param">workItem (optional)</div>

<div class="param-desc"><span class="param-type">[ArrayOfEngineInstanceWorkItem](#ArrayOfEngineInstanceWorkItem)</span></div>

<div class="param">workRequestID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

</div>

</div>

<div class="model">

### <a name="EngineLaunchDetail" id="EngineLaunchDetail">`EngineLaunchDetail`</a> [Up](#__Models)

<div class="field-items">

<div class="param">completedTimestamp (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> UTC Timestamp of NOW() when launch was completed format: int64</div>

<div class="param">createdDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the core was created format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">hostID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">launchAction (optional)</div>

<div class="param-desc"><span class="param-type">[LaunchActionEnum](#LaunchActionEnum)</span></div>

<div class="param">launchID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">launchStatus (optional)</div>

<div class="param-desc"><span class="param-type">[LaunchStatusEnum](#LaunchStatusEnum)</span></div>

<div class="param">launchSuccessful (optional)</div>

<div class="param-desc"><span class="param-type">[Boolean](#boolean)</span> If true, the launch was successful</div>

<div class="param">modifiedDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the core was last modified. format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

</div>

</div>

<div class="model">

### <a name="EngineRegistrationActionEnum" id="EngineRegistrationActionEnum">`EngineRegistrationActionEnum`</a> [Up](#__Models)

</div>

<div class="model">

### <a name="EngineStateEnum" id="EngineStateEnum">`EngineStateEnum`</a> [Up](#__Models)

<div class="model-description">This describes the different states of the engine. If paused, the tasks for this engine will not run. If replace, then a different engine as specified in the table will be used.</div>

</div>

<div class="model">

### <a name="EngineStatusEnum" id="EngineStatusEnum">`EngineStatusEnum`</a> [Up](#__Models)

</div>

<div class="model">

### <a name="EngineTypeEnum" id="EngineTypeEnum">`EngineTypeEnum`</a> [Up](#__Models)

<div class="model-description">These are the different types of engines on what they can consume. Chunk engines can consumes messages. Stream engines consume bytes. Batch does not consume anything.</div>

</div>

<div class="model">

### <a name="EnvKeyValue" id="EnvKeyValue">`EnvKeyValue`</a> [Up](#__Models)

<div class="model-description">Environment variable</div>

<div class="field-items">

<div class="param">key (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">value (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

</div>

</div>

<div class="model">

### <a name="Error" id="Error">`Error`</a> [Up](#__Models)

</div>

<div class="model">

### <a name="FailureReasonEnum" id="FailureReasonEnum">`FailureReasonEnum`</a> [Up](#__Models)

<div class="model-description">Task Failure Reason if taskStatus=<code>failed</code>. Available at the end of a batch, when getting the next batch to work, or last heartbeat before exiting. May not present in heartbeat update</div>

</div>

<div class="model">

### <a name="GPUEnum" id="GPUEnum">`GPUEnum`</a> [Up](#__Models)

</div>

<div class="model">

### <a name="GetCoresResponse" id="GetCoresResponse">`GetCoresResponse`</a> [Up](#__Models)

<div class="model-description">This is the response for get_cores Request</div>

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[array[CoreDetail]](#CoreDetail)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="GetEngineBuildResponse" id="GetEngineBuildResponse">`GetEngineBuildResponse`</a> [Up](#__Models)

<div class="model-description">This is the response for get_engine_build Request</div>

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[BuildDetail](#BuildDetail)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="GetEngineBuildsResponse" id="GetEngineBuildsResponse">`GetEngineBuildsResponse`</a> [Up](#__Models)

<div class="model-description">This is the response for get_engine_builds Request</div>

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[array[BuildDetail]](#BuildDetail)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="GetEngineCategoriesResponse" id="GetEngineCategoriesResponse">`GetEngineCategoriesResponse`</a> [Up](#__Models)

<div class="model-description">This is the response object for get engine categories.</div>

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[ArrayOfEngineCategories](#ArrayOfEngineCategories)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="GetEngineCategoryDetailResponse" id="GetEngineCategoryDetailResponse">`GetEngineCategoryDetailResponse`</a> [Up](#__Models)

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[EngineCategoryDetail](#EngineCategoryDetail)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="GetEngineDetailResponse" id="GetEngineDetailResponse">`GetEngineDetailResponse`</a> [Up](#__Models)

<div class="model-description">This is the response for get_engine_detail</div>

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[EngineDetail](#EngineDetail)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="GetEngineLaunchResponse" id="GetEngineLaunchResponse">`GetEngineLaunchResponse`</a> [Up](#__Models)

<div class="model-description">This is the response for get_engine_detail</div>

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[EngineLaunchDetail](#EngineLaunchDetail)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="GetEngineLaunchesResponse" id="GetEngineLaunchesResponse">`GetEngineLaunchesResponse`</a> [Up](#__Models)

<div class="model-description">This is the response for get_engine_launches</div>

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[array[EngineLaunchDetail]](#EngineLaunchDetail)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="GetEnginesResponse" id="GetEnginesResponse">`GetEnginesResponse`</a> [Up](#__Models)

<div class="model-description">This is the response for get_engines Request</div>

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[array[EngineDetail]](#EngineDetail)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="GetHostLaunchResponse" id="GetHostLaunchResponse">`GetHostLaunchResponse`</a> [Up](#__Models)

<div class="model-description">This is the response for get_host_detail</div>

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[HostLaunchDetail](#HostLaunchDetail)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="GetJobDetailResponse" id="GetJobDetailResponse">`GetJobDetailResponse`</a> [Up](#__Models)

<div class="field-items">

<div class="param">job (optional)</div>

<div class="param-desc"><span class="param-type">[JobDetail](#JobDetail)</span></div>

</div>

</div>

<div class="model">

### <a name="GetJobListResponse" id="GetJobListResponse">`GetJobListResponse`</a> [Up](#__Models)

<div class="field-items">

<div class="param">count (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> Total records for the query</div>

<div class="param">limit (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> the number of jobs to return.</div>

<div class="param">offset (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> the number of jobs to skip before getting the result set</div>

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[array[JobDetail]](#JobDetail)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="GetJobOutputResponse" id="GetJobOutputResponse">`GetJobOutputResponse`</a> [Up](#__Models)

<div class="field-items">

<div class="param">output (optional)</div>

<div class="param-desc"><span class="param-type">[JobOutput](#JobOutput)</span></div>

</div>

</div>

<div class="model">

### <a name="GetJobOutputsResponse" id="GetJobOutputsResponse">`GetJobOutputsResponse`</a> [Up](#__Models)

<div class="field-items">

<div class="param">outputs (optional)</div>

<div class="param-desc"><span class="param-type">[JobOutputs](#JobOutputs)</span></div>

</div>

</div>

<div class="model">

### <a name="GetJobStatusResponse" id="GetJobStatusResponse">`GetJobStatusResponse`</a> [Up](#__Models)

<div class="field-items">

<div class="param">job (optional)</div>

<div class="param-desc"><span class="param-type">[JobStatus](#JobStatus)</span></div>

</div>

</div>

<div class="model">

### <a name="GetJobWorkRequestResponse" id="GetJobWorkRequestResponse">`GetJobWorkRequestResponse`</a> [Up](#__Models)

<div class="model-description">This is the response for get Job Work-request Request</div>

<div class="field-items">

<div class="param">count (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> Total records for the query</div>

<div class="param">limit (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> the number of records to return.</div>

<div class="param">offset (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> the number of records to skip before getting the result set</div>

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[array[JobWorkRequest]](#JobWorkRequest)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="GetJobsOrganizationStatsResponse" id="GetJobsOrganizationStatsResponse">`GetJobsOrganizationStatsResponse`</a> [Up](#__Models)

<div class="field-items">

<div class="param">counts (optional)</div>

<div class="param-desc"><span class="param-type">[array[JobsOrganizationCountsInfo]](#JobsOrganizationCountsInfo)</span></div>

<div class="param">endDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime of the end of the stats period format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T10:12:28Z</span></div>

<div class="param">startDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime of the beginning of the stats period format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

</div>

</div>

<div class="model">

### <a name="GetJobsPerformanceResponse" id="GetJobsPerformanceResponse">`GetJobsPerformanceResponse`</a> [Up](#__Models)

<div class="field-items">

<div class="param">data (optional)</div>

<div class="param-desc"><span class="param-type">[array[JobPerformanceInfo]](#JobPerformanceInfo)</span></div>

<div class="param">endDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime of the end of the stats period format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T10:12:28Z</span></div>

<div class="param">startDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime of the beginning of the stats period format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

</div>

</div>

<div class="model">

### <a name="GetJobsStatsResponse" id="GetJobsStatsResponse">`GetJobsStatsResponse`</a> [Up](#__Models)

<div class="field-items">

<div class="param">counts (optional)</div>

<div class="param-desc"><span class="param-type">[array[JobsCountsInfo]](#JobsCountsInfo)</span></div>

<div class="param">endDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime of the end of the stats period format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T10:12:28Z</span></div>

<div class="param">startDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime of the beginning of the stats period format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

</div>

</div>

<div class="model">

### <a name="GetJobsTimeRangesStatsResponse" id="GetJobsTimeRangesStatsResponse">`GetJobsTimeRangesStatsResponse`</a> [Up](#__Models)

<div class="field-items">

<div class="param">counts (optional)</div>

<div class="param-desc"><span class="param-type">[array[JobsTimeRangesCountsInfo]](#JobsTimeRangesCountsInfo)</span></div>

<div class="param">endDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime of the end of the stats period format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T10:12:28Z</span></div>

<div class="param">startDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime of the beginning of the stats period format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

</div>

</div>

<div class="model">

### <a name="GetLicensesResponse" id="GetLicensesResponse">`GetLicensesResponse`</a> [Up](#__Models)

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[array[LicenseDetail]](#LicenseDetail)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="GetServerTypeResponse" id="GetServerTypeResponse">`GetServerTypeResponse`</a> [Up](#__Models)

<div class="model-description">This is the response for get Server Type Request</div>

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[ServerTypeDetail](#ServerTypeDetail)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="GetServerTypesResponse" id="GetServerTypesResponse">`GetServerTypesResponse`</a> [Up](#__Models)

<div class="model-description">This is the response for get Server Type Request</div>

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[array[ServerTypeDetail]](#ServerTypeDetail)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="GetTaskDetailResponse" id="GetTaskDetailResponse">`GetTaskDetailResponse`</a> [Up](#__Models)

<div class="field-items">

<div class="param">task (optional)</div>

<div class="param-desc"><span class="param-type">[TaskDetail](#TaskDetail)</span></div>

</div>

</div>

<div class="model">

### <a name="GetTaskOutputResponse" id="GetTaskOutputResponse">`GetTaskOutputResponse`</a> [Up](#__Models)

<div class="field-items">

<div class="param">output (optional)</div>

<div class="param-desc"><span class="param-type">[TaskOutput](#TaskOutput)</span></div>

</div>

</div>

<div class="model">

### <a name="GetTaskOutputsResponse" id="GetTaskOutputsResponse">`GetTaskOutputsResponse`</a> [Up](#__Models)

<div class="field-items">

<div class="param">outputs (optional)</div>

<div class="param-desc"><span class="param-type">[TaskOutputs](#TaskOutputs)</span></div>

</div>

</div>

<div class="model">

### <a name="GetTasksEnginesStatsResponse" id="GetTasksEnginesStatsResponse">`GetTasksEnginesStatsResponse`</a> [Up](#__Models)

<div class="field-items">

<div class="param">counts (optional)</div>

<div class="param-desc"><span class="param-type">[array[TasksEnginesCountsInfo]](#TasksEnginesCountsInfo)</span></div>

<div class="param">endDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime of the end of the stats period format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T10:12:28Z</span></div>

<div class="param">startDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime of the beginning of the stats period format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

</div>

</div>

<div class="model">

### <a name="GetTasksHostsStatsResponse" id="GetTasksHostsStatsResponse">`GetTasksHostsStatsResponse`</a> [Up](#__Models)

<div class="field-items">

<div class="param">counts (optional)</div>

<div class="param-desc"><span class="param-type">[array[TasksHostsCountsInfo]](#TasksHostsCountsInfo)</span></div>

<div class="param">endDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime of the end of the stats period format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T10:12:28Z</span></div>

<div class="param">startDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime of the beginning of the stats period format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

</div>

</div>

<div class="model">

### <a name="GetTasksResponse" id="GetTasksResponse">`GetTasksResponse`</a> [Up](#__Models)

<div class="field-items">

<div class="param">count (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> Total records for the query</div>

<div class="param">limit (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> the number of tasks to return.</div>

<div class="param">offset (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> the number of tasks to skip before getting the result set</div>

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[array[TaskDetail]](#TaskDetail)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="GetTasksStatsResponse" id="GetTasksStatsResponse">`GetTasksStatsResponse`</a> [Up](#__Models)

<div class="field-items">

<div class="param">counts (optional)</div>

<div class="param-desc"><span class="param-type">[array[TasksCountsInfo]](#TasksCountsInfo)</span></div>

<div class="param">endDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime of the end of the stats period format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T10:12:28Z</span></div>

<div class="param">startDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime of the beginning of the stats period format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="GetTasksTimeRangesStatsResponse" id="GetTasksTimeRangesStatsResponse">`GetTasksTimeRangesStatsResponse`</a> [Up](#__Models)

<div class="field-items">

<div class="param">counts (optional)</div>

<div class="param-desc"><span class="param-type">[array[TasksTimeRangesCountsInfo]](#TasksTimeRangesCountsInfo)</span></div>

<div class="param">endDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime of the end of the stats period format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T10:12:28Z</span></div>

<div class="param">startDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime of the beginning of the stats period format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

</div>

</div>

<div class="model">

### <a name="HostAction" id="HostAction">`HostAction`</a> [Up](#__Models)

<div class="field-items">

<div class="param">launchContainer (optional)</div>

<div class="param-desc"><span class="param-type">[array[HostActionLaunch]](#HostActionLaunch)</span></div>

<div class="param">launchNodeRedContainer (optional)</div>

<div class="param-desc"><span class="param-type">[array[HostActionNodeRedLaunch]](#HostActionNodeRedLaunch)</span></div>

<div class="param">mode (optional)</div>

<div class="param-desc"><span class="param-type">[HostActionModeEnum](#HostActionModeEnum)</span></div>

<div class="param">nfsServers (optional)</div>

<div class="param-desc"><span class="param-type">[array[HostMountInfo]](#HostMountInfo)</span></div>

<div class="param">registries (optional)</div>

<div class="param-desc"><span class="param-type">[array[DockerRegistry]](#DockerRegistry)</span></div>

<div class="param">terminateContainer (optional)</div>

<div class="param-desc"><span class="param-type">[array[HostActionTerminate]](#HostActionTerminate)</span></div>

</div>

</div>

<div class="model">

### <a name="HostActionEnum" id="HostActionEnum">`HostActionEnum`</a> [Up](#__Models)

</div>

<div class="model">

### <a name="HostActionLaunch" id="HostActionLaunch">`HostActionLaunch`</a> [Up](#__Models)

<div class="model-description">Launch request</div>

<div class="field-items">

<div class="param">buildId (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> the buildId for the engine</div>

<div class="param">containerConfig (optional)</div>

<div class="param-desc"><span class="param-type">[HostActionLaunch_containerConfig](#HostActionLaunch_containerConfig)</span></div>

<div class="param">containerType (optional)</div>

<div class="param-desc"><span class="param-type">[ContainerTypeEnum](#ContainerTypeEnum)</span></div>

<div class="param">dockerImage (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> Docker image to launch</div>

<div class="param">engineId (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> The id of the engine to launch</div>

<div class="param">env (optional)</div>

<div class="param-desc"><span class="param-type">[array[EnvKeyValue]](#EnvKeyValue)</span></div>

<div class="param">launchId (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> The Launch ID to use for the launch format: uuid</div>

<div class="param">name (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> The name of the engine or process to launch. This is informational only.</div>

<div class="param">runtime (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> the runtime for the build</div>

<div class="param">runtimeTTL (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> Seconds to run</div>

<div class="param">softMinMemory (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> format: int64</div>

<div class="param">softMinvCPU (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span></div>

</div>

</div>

<div class="model">

### <a name="HostActionLaunch_containerConfig" id="HostActionLaunch_containerConfig">`HostActionLaunch_containerConfig`</a> [Up](#__Models)

<div class="field-items">

<div class="param">commandLine (optional)</div>

<div class="param-desc"><span class="param-type">[array[String]](#string)</span></div>

</div>

</div>

<div class="model">

### <a name="HostActionModeEnum" id="HostActionModeEnum">`HostActionModeEnum`</a> [Up](#__Models)

<div class="model-description">Runtime mode for Host. Continue is for normal processing. Drain puts the agent into drain mode. Terminate is shutdown</div>

</div>

<div class="model">

### <a name="HostActionNodeRedLaunch" id="HostActionNodeRedLaunch">`HostActionNodeRedLaunch`</a> [Up](#__Models)

<div class="model-description">Launch request</div>

<div class="field-items">

<div class="param">buildId (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> the buildId for the engine</div>

<div class="param">containerConfig (optional)</div>

<div class="param-desc"><span class="param-type">[HostActionLaunch_containerConfig](#HostActionLaunch_containerConfig)</span></div>

<div class="param">containerType (optional)</div>

<div class="param-desc"><span class="param-type">[ContainerTypeEnum](#ContainerTypeEnum)</span></div>

<div class="param">dockerContainerName (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> Docker container name to launch</div>

<div class="param">dockerImage (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> Docker image to launch</div>

<div class="param">engineId (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> The id of the engine to launch</div>

<div class="param">env (optional)</div>

<div class="param-desc"><span class="param-type">[array[EnvKeyValue]](#EnvKeyValue)</span></div>

<div class="param">hostId (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> HostID of the node-red container</div>

<div class="param">launchId (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> The Launch ID to use for the launch format: uuid</div>

<div class="param">name (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> The name of the engine or process to launch. This is informational only.</div>

<div class="param">port (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> Port of the node-red container</div>

<div class="param">runtimeTTL (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> Seconds to run</div>

<div class="param">softMinMemory (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> format: int64</div>

<div class="param">softMinvCPU (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span></div>

<div class="param">userId (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> The userId of the current user.</div>

</div>

</div>

<div class="model">

### <a name="HostActionTerminate" id="HostActionTerminate">`HostActionTerminate`</a> [Up](#__Models)

<div class="field-items">

<div class="param">dockerContainerId (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> Docker image to launch</div>

</div>

</div>

<div class="model">

### <a name="HostDetail" id="HostDetail">`HostDetail`</a> [Up](#__Models)

</div>

<div class="model">

### <a name="HostDrainReasonEnum" id="HostDrainReasonEnum">`HostDrainReasonEnum`</a> [Up](#__Models)

<div class="model-description">The reason for draining the host</div>

</div>

<div class="model">

### <a name="HostLaunchConfig" id="HostLaunchConfig">`HostLaunchConfig`</a> [Up](#__Models)

<div class="field-items">

<div class="param">controller (optional)</div>

<div class="param-desc"><span class="param-type">[HostLaunchControllerConfig](#HostLaunchControllerConfig)</span></div>

<div class="param">modes (optional)</div>

<div class="param-desc"><span class="param-type">[array[RunModeEnum]](#RunModeEnum)</span></div>

<div class="param">nfs (optional)</div>

<div class="param-desc"><span class="param-type">[HostLaunchNFSConfig](#HostLaunchNFSConfig)</span></div>

<div class="param">postgres (optional)</div>

<div class="param-desc"><span class="param-type">[HostLaunchPostgresConfig](#HostLaunchPostgresConfig)</span></div>

<div class="param">registry (optional)</div>

<div class="param-desc"><span class="param-type">[HostLaunchRegistryConfig](#HostLaunchRegistryConfig)</span></div>

</div>

</div>

<div class="model">

### <a name="HostLaunchControllerConfig" id="HostLaunchControllerConfig">`HostLaunchControllerConfig`</a> [Up](#__Models)

<div class="field-items">

<div class="param">containerId (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">host (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">imageId (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">port (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span></div>

<div class="param">protocol (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">url (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

</div>

</div>

<div class="model">

### <a name="HostLaunchDetail" id="HostLaunchDetail">`HostLaunchDetail`</a> [Up](#__Models)

<div class="field-items">

<div class="param">completedTimestamp (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> UTC Timestamp of NOW() when launch was completed format: int64</div>

<div class="param">createdDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the core was created format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">hostID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">launchAction (optional)</div>

<div class="param-desc"><span class="param-type">[LaunchActionEnum](#LaunchActionEnum)</span></div>

<div class="param">launchID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">launchStatus (optional)</div>

<div class="param-desc"><span class="param-type">[LaunchStatusEnum](#LaunchStatusEnum)</span></div>

<div class="param">launchSuccessful (optional)</div>

<div class="param-desc"><span class="param-type">[Boolean](#boolean)</span> If true, the launch was successful</div>

<div class="param">modifiedDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the core was last modified. format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">serverTypeID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

</div>

</div>

<div class="model">

### <a name="HostLaunchNFSConfig" id="HostLaunchNFSConfig">`HostLaunchNFSConfig`</a> [Up](#__Models)

<div class="field-items">

<div class="param">containerId (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">imageId (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">port (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span></div>

</div>

</div>

<div class="model">

### <a name="HostLaunchPostgresConfig" id="HostLaunchPostgresConfig">`HostLaunchPostgresConfig`</a> [Up](#__Models)

<div class="field-items">

<div class="param">containerId (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">dbname (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">imageId (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">password (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">port (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span></div>

<div class="param">username (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

</div>

</div>

<div class="model">

### <a name="HostLaunchRegistryConfig" id="HostLaunchRegistryConfig">`HostLaunchRegistryConfig`</a> [Up](#__Models)

<div class="field-items">

<div class="param">containerId (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">imageId (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">password (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">port (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span></div>

<div class="param">username (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

</div>

</div>

<div class="model">

### <a name="HostMountInfo" id="HostMountInfo">`HostMountInfo`</a> [Up](#__Models)

<div class="model-description">This payload directs the agent to mount the specified directories on the hosts.</div>

<div class="field-items">

<div class="param">cache_number (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> the cache number for the nfs mount. 0 is /cache, 1 is /cache/1, ...</div>

<div class="param">ips (optional)</div>

<div class="param-desc"><span class="param-type">[array[String]](#string)</span> The host name or IP to mount.</div>

<div class="param">local_path (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> The mount on the local filesystem</div>

<div class="param">mountType (optional)</div>

<div class="param-desc"><span class="param-type">[HostMountTypeEnum](#HostMountTypeEnum)</span></div>

<div class="param">options (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> a comma separated list of options to pass into the mount commmand. An example is nfsvers=4,rsize=1048576,wsize=1048576,hard,timeo=600,retrans=2,noresvport</div>

<div class="param">port (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> The port the NFS service is listening on</div>

<div class="param">priority (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> The priority to mount them. Lowest first to highest numbers. For example, /cache is 10, /cache/1 is 100\. If they have the same priority then they are run in random order for the priority number.</div>

<div class="param">server_path (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> The mount path to mount</div>

</div>

</div>

<div class="model">

### <a name="HostMountTypeEnum" id="HostMountTypeEnum">`HostMountTypeEnum`</a> [Up](#__Models)

</div>

<div class="model">

### <a name="HostRegisterRequest" id="HostRegisterRequest">`HostRegisterRequest`</a> [Up](#__Models)

<div class="field-items">

<div class="param">info (optional)</div>

<div class="param-desc"><span class="param-type">[HostDetail](#HostDetail)</span></div>

<div class="param">launchConfig (optional)</div>

<div class="param-desc"><span class="param-type">[HostLaunchConfig](#HostLaunchConfig)</span></div>

<div class="param">status (optional)</div>

<div class="param-desc"><span class="param-type">[HostStatus](#HostStatus)</span></div>

</div>

</div>

<div class="model">

### <a name="HostRegisterResponse" id="HostRegisterResponse">`HostRegisterResponse`</a> [Up](#__Models)

</div>

<div class="model">

### <a name="HostRegisterResponse_configProperties" id="HostRegisterResponse_configProperties">`HostRegisterResponse_configProperties`</a> [Up](#__Models)

<div class="field-items">

<div class="param">localCacheDirectory (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> This should be /cache and will be mapped to the containers as /cache</div>

<div class="param">veritoneDockerRegistries (optional)</div>

<div class="param-desc"><span class="param-type">[array[DockerRegistry]](#DockerRegistry)</span></div>

</div>

</div>

<div class="model">

### <a name="HostStatus" id="HostStatus">`HostStatus`</a> [Up](#__Models)

<div class="field-items">

<div class="param">CPUUtilized (optional)</div>

<div class="param-desc"><span class="param-type">[Float](#float)</span> The CPU of the container as a percentage from 0-100 format: float</div>

<div class="param">containerStatus (optional)</div>

<div class="param-desc"><span class="param-type">[array[HostStatusContainer]](#HostStatusContainer)</span></div>

<div class="param">diskAvailableOptAiware (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> The available bytes in the /opt/aiware partition format: int64</div>

<div class="param">diskAvailableRoot (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> The available bytes in the root partition format: int64</div>

<div class="param">hostID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">memoryAvailable (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> The available memory to the container in bytes format: int64</div>

<div class="param">memoryUsed (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> The memory used by container in bytes format: int64</div>

<div class="param">numCPU (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> The number of CPU available</div>

<div class="param">numContainers (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> The number of containers running</div>

<div class="param">numEngineInstances (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> The number of engine instances running</div>

<div class="param">numGPU (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> The number of GPU available</div>

<div class="param">vCPUAvailable (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> The number of vCPUs available. THis is calculated by Number of CPUs * % available * 1024</div>

</div>

</div>

<div class="model">

### <a name="HostStatusContainer" id="HostStatusContainer">`HostStatusContainer`</a> [Up](#__Models)

</div>

<div class="model">

### <a name="HostTerminationReasonEnum" id="HostTerminationReasonEnum">`HostTerminationReasonEnum`</a> [Up](#__Models)

<div class="model-description">The reason for the termination of the host</div>

</div>

<div class="model">

### <a name="JobDetail" id="JobDetail">`JobDetail`</a> [Up](#__Models)

<div class="field-items">

<div class="param">abortedDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the task was aborted format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">completedDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the job was completed format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">coreID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">coreJobID (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> Core Job ID format: string</div>

<div class="param">coreRecordingId (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> This is the recording id in the core of the content for this job format: int64</div>

<div class="param">coreScheduledJobId (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> This is the core scheduled job id.</div>

<div class="param">coreSourceId (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> This is the Core Source Id format: int64</div>

<div class="param">createdDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the job was created format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">currentRetries (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> This is the current retries for the job</div>

<div class="param">dueDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the time the job is due to be complete. This is used by edge to set the priorities. format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">internalJobID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> Internal Job ID format: uuid</div>

<div class="param">internalOrganizationID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">internalScheduledJobId (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> The internal scheduled job id.</div>

<div class="param">isTemplate (optional)</div>

<div class="param-desc"><span class="param-type">[Boolean](#boolean)</span> If true, this job is a template</div>

<div class="param">jobConfigJSON (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> This is the job config expressed as JSON format: JSON</div>

<div class="param">jobStatus (optional)</div>

<div class="param-desc"><span class="param-type">[JobStatusEnum](#JobStatusEnum)</span></div>

<div class="param">jobTemplateId (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> If set, this job was created from this job template</div>

<div class="param">maxRetries (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> This is the max retries for the job</div>

<div class="param">modifiedDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the job was last modified. format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">priority (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> The priority for the job. Default is 0\. format: int32</div>

<div class="param">scheduledDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> If from scheduled job, this is the date when the job should be launched. There is sometimes a difference between scheduled and start to allow for the edge to start processing at the right time if warmup is needed. If not, blank format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">startDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> If from scheduled job, this is the date when the job should be started. This is a planning time not the actual whcih is startedDateTime. If not, blank format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">startedDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the job was started (actual) format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">stopDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> If from scheduled job, this is the date when the job should be stopped. Start and Stop are used for recording from a stream. If not, blank format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">taskRoutes (optional)</div>

<div class="param-desc"><span class="param-type">[array[TaskRouteDetail]](#TaskRouteDetail)</span></div>

<div class="param">tasks (optional)</div>

<div class="param-desc"><span class="param-type">[array[TaskDetail]](#TaskDetail)</span></div>

</div>

</div>

<div class="model">

### <a name="JobOutput" id="JobOutput">`JobOutput`</a> [Up](#__Models)

<div class="field-items">

<div class="param">contents (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> The content of the output.</div>

<div class="param">contentsValid (optional)</div>

<div class="param-desc"><span class="param-type">[Boolean](#boolean)</span> If true, the contents are valid even if empty</div>

<div class="param">created (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> The time the file was created as seconds since Unix epoch in UTC. format: int64</div>

<div class="param">name (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> The name of the output file</div>

<div class="param">size (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> The size of the output file in bytes format: int64</div>

</div>

</div>

<div class="model">

### <a name="JobOutputs" id="JobOutputs">`JobOutputs`</a> [Up](#__Models)

<div class="field-items">

<div class="param">internalJobID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> Internal Job ID format: uuid</div>

<div class="param">outputs (optional)</div>

<div class="param-desc"><span class="param-type">[array[JobOutput]](#JobOutput)</span></div>

</div>

</div>

<div class="model">

### <a name="JobPerformanceInfo" id="JobPerformanceInfo">`JobPerformanceInfo`</a> [Up](#__Models)

<div class="field-items">

<div class="param">cpu (optional)</div>

<div class="param-desc"><span class="param-type">[Float](#float)</span> CPU Utilization format: float</div>

<div class="param">dateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:00Z</span></div>

<div class="param">gpu (optional)</div>

<div class="param-desc"><span class="param-type">[Float](#float)</span> GPU Utilization format: float</div>

<div class="param">memory (optional)</div>

<div class="param-desc"><span class="param-type">[Float](#float)</span> Memory available in percent format: float</div>

</div>

</div>

<div class="model">

### <a name="JobStatus" id="JobStatus">`JobStatus`</a> [Up](#__Models)

<div class="field-items">

<div class="param">internalJobID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> Internal Job ID format: uuid</div>

<div class="param">jobStatus (optional)</div>

<div class="param-desc"><span class="param-type">[JobStatusEnum](#JobStatusEnum)</span></div>

</div>

</div>

<div class="model">

### <a name="JobStatusEnum" id="JobStatusEnum">`JobStatusEnum`</a> [Up](#__Models)

<div class="model-description">This is the status for the job. This will be created as 'pending' for new jobs</div>

</div>

<div class="model">

### <a name="JobWorkRequest" id="JobWorkRequest">`JobWorkRequest`</a> [Up](#__Models)

<div class="field-items">

<div class="param">buildID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">completedDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime for completed_date_time in a task format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:15:28Z</span></div>

<div class="param">engineCategoryID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">engineID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">engineInstanceID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">engineName (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">errorCount (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span></div>

<div class="param">internalJobID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">internalTaskID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">startDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime for start_date_time in a task format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">status (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">workRequestID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

</div>

</div>

<div class="model">

### <a name="JobsCountsInfo" id="JobsCountsInfo">`JobsCountsInfo`</a> [Up](#__Models)

<div class="field-items">

<div class="param">count (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> Total amount of jobs with a particular status format: int64</div>

<div class="param">status (optional)</div>

<div class="param-desc"><span class="param-type">[JobStatusEnum](#JobStatusEnum)</span></div>

</div>

</div>

<div class="model">

### <a name="JobsEnginesCountsInfo" id="JobsEnginesCountsInfo">`JobsEnginesCountsInfo`</a> [Up](#__Models)

<div class="field-items">

<div class="param">count (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> Total amount of jobs with a particular status and an engine category format: int64</div>

<div class="param">engineCategoryName (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> Engine category name</div>

<div class="param-desc"><span class="param-type">example: Logo Recognition</span></div>

<div class="param">status (optional)</div>

<div class="param-desc"><span class="param-type">[JobStatusEnum](#JobStatusEnum)</span></div>

</div>

</div>

<div class="model">

### <a name="JobsHostsCountsInfo" id="JobsHostsCountsInfo">`JobsHostsCountsInfo`</a> [Up](#__Models)

<div class="field-items">

<div class="param">count (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> Total amount of jobs with a particular status and a host name format: int64</div>

<div class="param">hostName (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> Host name</div>

<div class="param-desc"><span class="param-type">example: Host1</span></div>

<div class="param">status (optional)</div>

<div class="param-desc"><span class="param-type">[JobStatusEnum](#JobStatusEnum)</span></div>

</div>

</div>

<div class="model">

### <a name="JobsOrganizationCountsInfo" id="JobsOrganizationCountsInfo">`JobsOrganizationCountsInfo`</a> [Up](#__Models)

<div class="field-items">

<div class="param">count (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> Total amount of jobs with a particular status and a time range format: int64</div>

<div class="param">organizationId (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> Id of organization format: int64</div>

<div class="param">organizationName (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> Name of organization</div>

<div class="param">status (optional)</div>

<div class="param-desc"><span class="param-type">[JobStatusEnum](#JobStatusEnum)</span></div>

</div>

</div>

<div class="model">

### <a name="JobsTimeRangesCountsInfo" id="JobsTimeRangesCountsInfo">`JobsTimeRangesCountsInfo`</a> [Up](#__Models)

<div class="field-items">

<div class="param">count (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> Total amount of jobs with a particular status and a time range format: int64</div>

<div class="param">endDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> Start of a time range format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T10:12:28Z</span></div>

<div class="param">startDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> Start of a time range format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">status (optional)</div>

<div class="param-desc"><span class="param-type">[JobStatusEnum](#JobStatusEnum)</span></div>

</div>

</div>

<div class="model">

### <a name="LaunchActionEnum" id="LaunchActionEnum">`LaunchActionEnum`</a> [Up](#__Models)

</div>

<div class="model">

### <a name="LaunchJobTemplateRequest" id="LaunchJobTemplateRequest">`LaunchJobTemplateRequest`</a> [Up](#__Models)

<div class="field-items">

<div class="param">isInternal (optional)</div>

<div class="param-desc"><span class="param-type">[Boolean](#boolean)</span> Whether to launch the job template within the edge cluster or back to core</div>

<div class="param">payloadJSON (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> This is the payload encoded as a JSON string. This will be used format: json</div>

<div class="param">scheduledJobID (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> the scheduled job id that started the pipeline involving this template</div>

<div class="param">sourceID (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> the source Id that associated with the pipeline involving this template</div>

</div>

</div>

<div class="model">

### <a name="LaunchJobTemplateResponse" id="LaunchJobTemplateResponse">`LaunchJobTemplateResponse`</a> [Up](#__Models)

<div class="field-items">

<div class="param">operation (optional)</div>

<div class="param-desc"><span class="param-type">[AdminOperationResponse](#AdminOperationResponse)</span></div>

</div>

</div>

<div class="model">

### <a name="LaunchStatusEnum" id="LaunchStatusEnum">`LaunchStatusEnum`</a> [Up](#__Models)

</div>

<div class="model">

### <a name="LicenseDetail" id="LicenseDetail">`LicenseDetail`</a> [Up](#__Models)

<div class="model-description">This provides the detailed information about the license.</div>

<div class="field-items">

<div class="param">currentAPI (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> The current number of API calls allowed by the license. format: int64</div>

<div class="param">currentBytes (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> The current number of bytes to be processed under this license. format: int64</div>

<div class="param">currentTasks (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> The current number of tasks that can be processed on the system. format: int64</div>

<div class="param">licenseExpiration (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the license will expire format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">licenseID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> License ID format: uuid</div>

<div class="param">licenseKey (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> This is the encoded license string</div>

<div class="param">licenseValidation (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> This contains the validation information for the license</div>

<div class="param">maxAPI (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> The maximum number of API calls allowed by the license. If 0, then unlimited. format: int64</div>

<div class="param">maxBytes (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> The maximum number of bytes to be processed under this license. If 0, then unlimited. format: int64</div>

<div class="param">maxHosts (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> The maximum number of hosts allowed in the system. If 0, then unlimited. format: int64</div>

<div class="param">maxTasks (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> The maximum number of tasks that can be processed on the system. If 0, then unlimited. format: int64</div>

</div>

</div>

<div class="model">

### <a name="OperationSuccess" id="OperationSuccess">`OperationSuccess`</a> [Up](#__Models)

<div class="model-description">If true, the operation was successful.</div>

</div>

<div class="model">

### <a name="OrganizationDetail" id="OrganizationDetail">`OrganizationDetail`</a> [Up](#__Models)

<div class="field-items">

<div class="param">applicationID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">basePriority (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span></div>

<div class="param">coreID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">coreOrganizationID (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span></div>

<div class="param">createdDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the core was created format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">defaultRetries (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span></div>

<div class="param">defaultSLASeconds (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span></div>

<div class="param">kvpJSON (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> format: json</div>

<div class="param">modifiedDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the core was last modified. format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">name (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">organizationID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">taskPriorityAdjustmentStarted (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span></div>

</div>

</div>

<div class="model">

### <a name="OrganizationID" id="OrganizationID">`OrganizationID`</a> [Up](#__Models)

</div>

<div class="model">

### <a name="PauseBuildRequest" id="PauseBuildRequest">`PauseBuildRequest`</a> [Up](#__Models)

<div class="field-items">

<div class="param">buildID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">engineID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

</div>

</div>

<div class="model">

### <a name="PauseEngineRequest" id="PauseEngineRequest">`PauseEngineRequest`</a> [Up](#__Models)

<div class="field-items">

<div class="param">engineID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

</div>

</div>

<div class="model">

### <a name="RecheckJobStatusResponse" id="RecheckJobStatusResponse">`RecheckJobStatusResponse`</a> [Up](#__Models)

<div class="field-items">

<div class="param">job (optional)</div>

<div class="param-desc"><span class="param-type">[JobStatus](#JobStatus)</span></div>

</div>

</div>

<div class="model">

### <a name="RemoveServersToServerTypeRequest" id="RemoveServersToServerTypeRequest">`RemoveServersToServerTypeRequest`</a> [Up](#__Models)

<div class="field-items">

<div class="param">serversToAdd (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> The number of servers to remove format: int32</div>

</div>

</div>

<div class="model">

### <a name="ReplaceEngineRequest" id="ReplaceEngineRequest">`ReplaceEngineRequest`</a> [Up](#__Models)

<div class="field-items">

<div class="param">engineID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

</div>

</div>

<div class="model">

### <a name="ResumeBuildRequest" id="ResumeBuildRequest">`ResumeBuildRequest`</a> [Up](#__Models)

<div class="field-items">

<div class="param">buildID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">engineID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

</div>

</div>

<div class="model">

### <a name="ResumeEngineRequest" id="ResumeEngineRequest">`ResumeEngineRequest`</a> [Up](#__Models)

<div class="field-items">

<div class="param">engineID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

</div>

</div>

<div class="model">

### <a name="RunModeEnum" id="RunModeEnum">`RunModeEnum`</a> [Up](#__Models)

<div class="model-description">Run modes for the Host</div>

</div>

<div class="model">

### <a name="ServerProviderEnum" id="ServerProviderEnum">`ServerProviderEnum`</a> [Up](#__Models)

<div class="model-description">This selects</div>

</div>

<div class="model">

### <a name="ServerTypeDetail" id="ServerTypeDetail">`ServerTypeDetail`</a> [Up](#__Models)

<div class="field-items">

<div class="param">agentStartupScript (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">awsAmi (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">awsInstanceProfile (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">awsInstanceType (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">awsKeyName (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">awsSecurityGroups (optional)</div>

<div class="param-desc"><span class="param-type">[array[String]](#string)</span> aws subnets</div>

<div class="param">awsSpot (optional)</div>

<div class="param-desc"><span class="param-type">[Boolean](#boolean)</span></div>

<div class="param">awsSpotMaxPrice (optional)</div>

<div class="param-desc"><span class="param-type">[Float](#float)</span> format: float</div>

<div class="param">awsSpotPersistent (optional)</div>

<div class="param-desc"><span class="param-type">[Boolean](#boolean)</span></div>

<div class="param">awsSubnets (optional)</div>

<div class="param-desc"><span class="param-type">[array[String]](#string)</span> aws subnets</div>

<div class="param">awsTagsJSON (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> format: json</div>

<div class="param">awsUserData (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">createdDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the core was created format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">gpuType (optional)</div>

<div class="param-desc"><span class="param-type">[GPUEnum](#GPUEnum)</span></div>

<div class="param">hasGPU (optional)</div>

<div class="param-desc"><span class="param-type">[Boolean](#boolean)</span></div>

<div class="param">isAutoScaleActive (optional)</div>

<div class="param-desc"><span class="param-type">[Boolean](#boolean)</span></div>

<div class="param">maxServers (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> format: int64</div>

<div class="param">memoryBytes (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> format: int64</div>

<div class="param">minServers (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> format: int64</div>

<div class="param">modifiedDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the core was last modified. format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">numGPU (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> format: int64</div>

<div class="param">onlyOrganizationId (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">runModes (optional)</div>

<div class="param-desc"><span class="param-type">[array[RunModeEnum]](#RunModeEnum)</span> run modes</div>

<div class="param">serverConfigJSON (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> format: json</div>

<div class="param">serverProvider (optional)</div>

<div class="param-desc"><span class="param-type">[ServerProviderEnum](#ServerProviderEnum)</span></div>

<div class="param">serverTypeID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">vcpus (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> format: int64</div>

</div>

</div>

<div class="model">

### <a name="SortOrderEnum" id="SortOrderEnum">`SortOrderEnum`</a> [Up](#__Models)

</div>

<div class="model">

### <a name="StatusFormatEnum" id="StatusFormatEnum">`StatusFormatEnum`</a> [Up](#__Models)

</div>

<div class="model">

### <a name="TaskDetail" id="TaskDetail">`TaskDetail`</a> [Up](#__Models)

<div class="field-items">

<div class="param">abortedDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the task was aborted format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">buildID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">childTaskIDs (optional)</div>

<div class="param-desc"><span class="param-type">[array[UUID]](#UUID)</span> Array of Internal Child Task Id format: uuid</div>

<div class="param">completedDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the task was completed format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">coreJobID (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> This is the core job id associated with this job</div>

<div class="param">coreRecordingID (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> This is the recording id in the core of the content for this job format: int64</div>

<div class="param">coreTaskID (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> This is the core task id associated with this job</div>

<div class="param">createdDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the core was created format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">currentRetries (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> This is the current retries for the task</div>

<div class="param">dueDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the time the task is due to be complete. This is used by edge to set the priorities. format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">engineCategoryID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> Category Id format: uuid</div>

<div class="param">engineCategoryName (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> Category name</div>

<div class="param-desc"><span class="param-type">example: Transcription</span></div>

<div class="param">engineID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">engineName (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> Engine name</div>

<div class="param-desc"><span class="param-type">example: Speechmatic en - V3F</span></div>

<div class="param">errorCount (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> This is the error count for the task</div>

<div class="param">failureDetail (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> If there is an error, the detail will be set here.</div>

<div class="param">failureReason (optional)</div>

<div class="param-desc"><span class="param-type">[FailureReasonEnum](#FailureReasonEnum)</span></div>

<div class="param">internalJobID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> Internal Job ID format: uuid</div>

<div class="param">internalOrganizationID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">internalTaskID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> Internal Task ID format: uuid</div>

<div class="param">ioFolders (optional)</div>

<div class="param-desc"><span class="param-type">[array[TaskIOInfo]](#TaskIOInfo)</span></div>

<div class="param">isTemplate (optional)</div>

<div class="param-desc"><span class="param-type">[Boolean](#boolean)</span> If true, this job is a template</div>

<div class="param">maxEngines (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> The maximum number of engine instances to run against this task. Defaults to 1 if parallelProcessing is false, or 2 otherwise.</div>

<div class="param">maxRetries (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> This is the max retries for the task</div>

<div class="param">modifiedDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the core was last modified. format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">parallelProcessing (optional)</div>

<div class="param-desc"><span class="param-type">[Boolean](#boolean)</span> If true, multiple engine instances can process this task in parallel. If false, maxEngines will be 1\.</div>

<div class="param">parentMustBeCompleteBeforeStarting (optional)</div>

<div class="param-desc"><span class="param-type">[Boolean](#boolean)</span> If true, this task won't start until the parent is complete</div>

<div class="param">parentTaskID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> Internal Parent Task Id format: uuid</div>

<div class="param">payloadJSON (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> This is the payload encoded as a JSON string format: json</div>

<div class="param">scheduledDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> If from scheduled job, this is the date when the task should be launched. There is sometimes a difference between scheduled and start to allow for the edge to start processing at the right time if warmup is needed. If not, blank format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">startDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> If from scheduled job, this is the date when the task should be started. This is a planning time not the actual which is startedDateTime. If not, blank format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">startedDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the task was started (actual) format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">stopDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> If from scheduled job, this is the date when the task should be stopped. Start and Stop are used for recording from a stream. If not, blank format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">taskOutputSON (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> This is the taskOutput as a JSON string format: json</div>

<div class="param">taskPayloadJSON (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> This is the taskPayload as a JSON string format: json</div>

<div class="param">taskStatus (optional)</div>

<div class="param-desc"><span class="param-type">[JobStatusEnum](#JobStatusEnum)</span></div>

<div class="param">taskTemplateID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> If set, this task was created from this task template. format: uuid</div>

</div>

</div>

<div class="model">

### <a name="TaskIO" id="TaskIO">`TaskIO`</a> [Up](#__Models)

<div class="model-description">An input or output folder. For type output, all fields required. For type input, only id is required.</div>

</div>

<div class="model">

### <a name="TaskIOFolder" id="TaskIOFolder">`TaskIOFolder`</a> [Up](#__Models)

<div class="field-items">

<div class="param">id (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> IO ID format: uuid</div>

<div class="param">taskId (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> The task id containing the io folder</div>

</div>

</div>

<div class="model">

### <a name="TaskIOInfo" id="TaskIOInfo">`TaskIOInfo`</a> [Up](#__Models)

<div class="model-description">This is the task IO Object that provides paramenters for the input and output</div>

<div class="field-items">

<div class="param">correlationId (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> On create, this field will be used to look up task routes for binding.</div>

<div class="param">createdDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the task was created format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">id (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> This is the IO Id. On create, this is not set. format: uuid</div>

<div class="param">mode (optional)</div>

<div class="param-desc"><span class="param-type">[TaskIOModeEnum](#TaskIOModeEnum)</span></div>

<div class="param">modifiedDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the task was last modified. format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">optionsJSON (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> Any options for this input or output folder for the task to use on processing format: json</div>

<div class="param">type (optional)</div>

<div class="param-desc"><span class="param-type">[TaskIOTypeEnum](#TaskIOTypeEnum)</span></div>

</div>

</div>

<div class="model">

### <a name="TaskIOModeEnum" id="TaskIOModeEnum">`TaskIOModeEnum`</a> [Up](#__Models)

</div>

<div class="model">

### <a name="TaskIOStatus" id="TaskIOStatus">`TaskIOStatus`</a> [Up](#__Models)

</div>

<div class="model">

### <a name="TaskIOTypeEnum" id="TaskIOTypeEnum">`TaskIOTypeEnum`</a> [Up](#__Models)

</div>

<div class="model">

### <a name="TaskOutput" id="TaskOutput">`TaskOutput`</a> [Up](#__Models)

<div class="field-items">

<div class="param">contents (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> The content of the output.</div>

<div class="param">contentsValid (optional)</div>

<div class="param-desc"><span class="param-type">[Boolean](#boolean)</span> If true, the contents are valid even if empty</div>

<div class="param">created (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> The time the file was created as seconds since Unix epoch in UTC. format: int64</div>

<div class="param">name (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> The name of the output file</div>

<div class="param">size (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> The size of the output file in bytes format: int64</div>

</div>

</div>

<div class="model">

### <a name="TaskOutputs" id="TaskOutputs">`TaskOutputs`</a> [Up](#__Models)

<div class="field-items">

<div class="param">internalTaskID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> Internal Task ID format: uuid</div>

<div class="param">outputs (optional)</div>

<div class="param-desc"><span class="param-type">[array[TaskOutput]](#TaskOutput)</span></div>

</div>

</div>

<div class="model">

### <a name="TaskRouteDetail" id="TaskRouteDetail">`TaskRouteDetail`</a> [Up](#__Models)

<div class="field-items">

<div class="param">endpoint (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> This is endpoint to be used for this route. This does not have to be unique. format: uuid</div>

<div class="param">firstWriteDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the the first byte or chunk was written format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">lastWriteDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the the last byte or chunk was written format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">taskChildId (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> This is the task child id. On create, this is the taskCorrelationId</div>

<div class="param">taskChildInputCount (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> This is the count of bytes or chunks available to the child.</div>

<div class="param">taskChildInputId (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> This is the task child input id. On create, this is the correlationId for the input IO Folder</div>

<div class="param">taskChildInputRemainingCount (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> This is the count of bytes or chunks remaining to the child.</div>

<div class="param">taskChildNumEngines (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> This is the number of engine instances running against this task.</div>

<div class="param">taskParentId (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> This is the task parent id. On create, this is the taskCorrelationId</div>

<div class="param">taskParentOutputCount (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> This is the count of bytes or chunks produced by the parent.</div>

<div class="param">taskParentOutputId (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> This is the task parent output id. On create, this is the correlationId for the output IO Folder</div>

</div>

</div>

<div class="model">

### <a name="TaskStatusDetail" id="TaskStatusDetail">`TaskStatusDetail`</a> [Up](#__Models)

<div class="model-description">Represent a task status as being worked on by an engine instance. This can be sent as part of heartbeat status update or when getting new work. The updates are deltas since last post</div>

<div class="field-items">

<div class="param">engineID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">errorCount (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> How many errors since last error update</div>

<div class="param">errorDetails (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> JSON string containing an array of JSON Object to describe indvidiual errors e.g. [{&quot;id&quot;:&quot;xxx&quot;, &quot;msg&quot;:&quot;xxx&quot;},..]</div>

<div class="param">failureReason (optional)</div>

<div class="param-desc"><span class="param-type">[FailureReasonEnum](#FailureReasonEnum)</span></div>

<div class="param">inputs (optional)</div>

<div class="param-desc"><span class="param-type">[array[TaskIOStatus]](#TaskIOStatus)</span></div>

<div class="param">internalJobID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> Internal Job ID format: uuid</div>

<div class="param">internalTaskID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> Internal Task ID format: uuid</div>

<div class="param">outputs (optional)</div>

<div class="param-desc"><span class="param-type">[array[TaskIOStatus]](#TaskIOStatus)</span></div>

<div class="param">priorTimestamp (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> UTC Timestamp of last status update or start of new task format: int64</div>

<div class="param">retryCount (optional)</div>

<div class="param-desc"><span class="param-type">[Integer](#integer)</span> How many retries since last status update</div>

<div class="param">taskOutput (optional)</div>

<div class="param-desc"><span class="param-type">[Object](#object)</span> available at the end of a batch, when getting the next batch to work, or last heartbeat before exiting. May not present in heartbeat update</div>

<div class="param">taskRouteID (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> the task route associated with this work item</div>

<div class="param">taskStatus (optional)</div>

<div class="param-desc"><span class="param-type">[JobStatusEnum](#JobStatusEnum)</span></div>

<div class="param">timestamp (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> UTC Timestamp of NOW() format: int64</div>

<div class="param">workRequestID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

</div>

</div>

<div class="model">

### <a name="TaskStatusEnum" id="TaskStatusEnum">`TaskStatusEnum`</a> [Up](#__Models)

<div class="model-description">This is the status for the task. This will be created as 'pending' for new task</div>

</div>

<div class="model">

### <a name="TasksCountsInfo" id="TasksCountsInfo">`TasksCountsInfo`</a> [Up](#__Models)

<div class="field-items">

<div class="param">count (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> Total amount of tasks with a particular status format: int64</div>

<div class="param">status (optional)</div>

<div class="param-desc"><span class="param-type">[TaskStatusEnum](#TaskStatusEnum)</span></div>

</div>

</div>

<div class="model">

### <a name="TasksEnginesCountsInfo" id="TasksEnginesCountsInfo">`TasksEnginesCountsInfo`</a> [Up](#__Models)

<div class="field-items">

<div class="param">count (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> Total amount of tasks with a particular status and an engine category format: int64</div>

<div class="param">engineCategoryName (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> Engine category name</div>

<div class="param-desc"><span class="param-type">example: Logo Recognition</span></div>

<div class="param">status (optional)</div>

<div class="param-desc"><span class="param-type">[TaskStatusEnum](#TaskStatusEnum)</span></div>

</div>

</div>

<div class="model">

### <a name="TasksHostsCountsInfo" id="TasksHostsCountsInfo">`TasksHostsCountsInfo`</a> [Up](#__Models)

<div class="field-items">

<div class="param">count (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> Total amount of tasks with a particular status and a host name format: int64</div>

<div class="param">engineCategoryName (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> Engine category name</div>

<div class="param-desc"><span class="param-type">example: Translation</span></div>

<div class="param">hostName (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> Host name</div>

<div class="param-desc"><span class="param-type">example: Host1</span></div>

</div>

</div>

<div class="model">

### <a name="TasksTimeRangesCountsInfo" id="TasksTimeRangesCountsInfo">`TasksTimeRangesCountsInfo`</a> [Up](#__Models)

<div class="field-items">

<div class="param">count (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> Total amount of tasks with a particular status and a time range format: int64</div>

<div class="param">endDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> Start of a time range format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T10:12:28Z</span></div>

<div class="param">startDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> Start of a time range format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">status (optional)</div>

<div class="param-desc"><span class="param-type">[TaskStatusEnum](#TaskStatusEnum)</span></div>

</div>

</div>

<div class="model">

### <a name="TerminateHostRequest" id="TerminateHostRequest">`TerminateHostRequest`</a> [Up](#__Models)

<div class="field-items">

<div class="param">detail (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">reason (optional)</div>

<div class="param-desc"><span class="param-type">[HostTerminationReasonEnum](#HostTerminationReasonEnum)</span></div>

</div>

</div>

<div class="model">

### <a name="TokenDetail" id="TokenDetail">`TokenDetail`</a> [Up](#__Models)

<div class="field-items">

<div class="param">apiRateLimitHour (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> format: int64</div>

<div class="param">bytesRateLimitHour (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> format: int64</div>

<div class="param">createdDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the core was created format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">engineInstanceID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">expiration (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the core was created format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">hostID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">kvpJSON (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> format: json</div>

<div class="param">maxAPI (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> format: int64</div>

<div class="param">maxBytes (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> format: int64</div>

<div class="param">maxTasks (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> format: int64</div>

<div class="param">modifiedDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the core was last modified. format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">organizationIDs (optional)</div>

<div class="param-desc"><span class="param-type">[array[OrganizationID]](#OrganizationID)</span></div>

<div class="param">taskRateLimitHour (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> format: int64</div>

<div class="param">tokenID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">totalCountAPI (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> format: int64</div>

<div class="param">totalCountBytes (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> format: int64</div>

<div class="param">totalCountTasks (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> format: int64</div>

<div class="param">type (optional)</div>

<div class="param-desc"><span class="param-type">[TokenTypeEnum](#TokenTypeEnum)</span></div>

</div>

</div>

<div class="model">

### <a name="TokenTypeEnum" id="TokenTypeEnum">`TokenTypeEnum`</a> [Up](#__Models)

</div>

<div class="model">

### <a name="UpdateBuildResponse" id="UpdateBuildResponse">`UpdateBuildResponse`</a> [Up](#__Models)

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[BuildDetail](#BuildDetail)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="UpdateEngineCategoryResponse" id="UpdateEngineCategoryResponse">`UpdateEngineCategoryResponse`</a> [Up](#__Models)

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[EngineCategoryDetail](#EngineCategoryDetail)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="UpdateEngineResponse" id="UpdateEngineResponse">`UpdateEngineResponse`</a> [Up](#__Models)

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[EngineDetail](#EngineDetail)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="UpdateServerTypeResponse" id="UpdateServerTypeResponse">`UpdateServerTypeResponse`</a> [Up](#__Models)

<div class="field-items">

<div class="param">result (optional)</div>

<div class="param-desc"><span class="param-type">[ServerTypeDetail](#ServerTypeDetail)</span></div>

<div class="param">success (optional)</div>

<div class="param-desc"><span class="param-type">[OperationSuccess](#OperationSuccess)</span></div>

</div>

</div>

<div class="model">

### <a name="UserDetail" id="UserDetail">`UserDetail`</a> [Up](#__Models)

<div class="field-items">

<div class="param">createdBy (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">createdDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the core was created format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">datePasswordLastUpdated (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the password was last updated format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">displayName (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">email (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> format: email</div>

<div class="param">internalOrganizationID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">kvpJSON (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> format: json</div>

<div class="param">lastLoggedIn (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the user last logged in format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">modifiedBy (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">modifiedDateTime (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> This is the datetime the core was last modified. format: date-time</div>

<div class="param-desc"><span class="param-type">example: 2018-03-20T09:12:28Z</span></div>

<div class="param">passwordChangeRequired (optional)</div>

<div class="param-desc"><span class="param-type">[Boolean](#boolean)</span></div>

<div class="param">status (optional)</div>

<div class="param-desc"><span class="param-type">[UserStatusEnum](#UserStatusEnum)</span></div>

<div class="param">userID (optional)</div>

<div class="param-desc"><span class="param-type">[UUID](#UUID)</span> format: uuid</div>

<div class="param">userName (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">userSettingsJSON (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span> format: json</div>

</div>

</div>

<div class="model">

### <a name="UserStatusEnum" id="UserStatusEnum">`UserStatusEnum`</a> [Up](#__Models)

<div class="model-description">Flag denoting user status. Trial users will be deactived in the future or converted. Inactive users can't login. Deleted users are soft deleted.</div>

</div>

<div class="model">

### <a name="WorkRequestStatusEnum" id="WorkRequestStatusEnum">`WorkRequestStatusEnum`</a> [Up](#__Models)

<div class="model-description">The final status of the last work request</div>

</div>