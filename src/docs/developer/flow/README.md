# Building Flows with Automate Studio

With Veritone Automate Studio, less-technical users can create their own AI Solutions that incorporate Veritone's cognitive engines and real time services directly into custom business applications.

## What is Veritone Automate Studio?

Automate Studio has three components:

1. The Automate Studio design environment, where users can drag and drop activity nodes &mdash; representing discrete units of business logic &mdash; onto a Flow Designer canvas, and test the logic using the Flow Designer runtime.
2. The Veritone Engine framework, which serves as the production-grade runtime for Flow instances, which run "as an engine." (In Veritone parlance, this is just a fancy way of saying "custom logic that runs on Veritone's aiWARE platform.")
3. An Admin component, accessible via the Veritone Developer admin UI.

## Why do you need Automate Studio?

Automate Studio lets you quickly develop enterprise-grade AI solutions that tap into veritone's 300+ Cognitive engines across more than a dozen classes of AI cognition.

## What can you do with Automate Studio?

What you build is entirely up to you! Want to send out e-mail alerts when a Face is recognized? You can use Automate Studio to do that! Want to scrape the web for training data? You can automate it! You could even build a flow that texts your designated recipients and asks them to confirm if certain detections are accurate, and then setup logic to handle the recipient's response!

## How does it work?

Veritone Automate Studio is built with the [Node-RED](https://nodered.org/) open source technology that is supported by the JS Foundation. At Veritone, we have taken this foundational open source technology and infused our own aiWARE palette of nodes that abstract away the underlying Veritone logic and data model, making it easier for users to take advantage of the underlying power of aiWARE.

For more info on how Automate Studio fits into the aiAWARE architecture, see [our FAQ](developer/flow/faq).

### Designing your flow engines

For your flow to successfully run on the aiWARE engine processing framework, each flow needs to be designed so that it can accept incoming webhooks from the engine framework and communicate back.

This design is reflected by the “Readyz” and “Process” http in and http response nodes.

While these nodes might not look obviously necessary for the logic to run in Automate Studio, this is how the flow receives messages from aiWARE and is orchestrated at large.

For more information on engine creation generally and a deeper dive into how engine toolkit would be implemented through code, check out the Engine Toolkit section [here](developer/engines/toolkit)

### Debugging your flows

Your debugging experience in Automate Studio can be thought of as two steps:

1. running the flow in the Automate Studio runtime, and 
2. debugging the output of the logic you configured in previous nodes 

You can use several types of input nodes to run your node, and keep in mind that this run is intended to simulate how the flow will behave running as a flow engine on aiWARE’s processing framework. Drag an inject node onto the canvas, wire it to the node containing your logic that you wish to process next, click deploy to save your changes and operationalize the flow in Automate Studio, and then click the “inject button” on the left side of the node. 

To view your logic outputs, drag the debug node from the palette menu on the left and connect an output wire from one or more nodes that you wish to evaluate. The outputs sent to the debug node are then logged on the right hand menu in the “debug” tab with the “bug” icon.
