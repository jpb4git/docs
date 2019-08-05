<!-- This is the Readme for the `Building Flows` sub-section of the Developer section on docs.veritone.com -->
<!-- The general layout will read something like: Building Flows -> What is Flow -> Why Flow -> Creating Flows --> 
<!-- How does it work? -> Quickstarts -> FAQ -->

# Building Flows with Automate Studio

With Veritone Automate Studio, less technical users can create their own AI Solutions that incorporate Veritone's cognitive engines and real time services directly into daily business problems that were historically untenable with out an active intelligence participating.

## What is Veritone Automate?

Automate Studio has three components: 
1. The Automate Studio itself where users can drag and drop shapes (or "nodes") that visualize discrete logic onto the Flow Designer canvas and test the logic using the Flow Designer runtime.
2. The Veritone Engine framework which serves as the production grade runtime for the Flow, running "as an engine," which in Veritone vocab, is just a fancy way of saying "custom logic that runs on Veritone's runtime"
3. Managing the Automate Studio application and related features as they are released to aiWARE users in the Admin app

## Why do you need Automate Studio?

Automate Studio enables you to rapidly develop AI solutions that let you tap into veritone's 400+ Cognitive engines across more than a dozen classes of AI cognition and incorporate that artificial intelligence into an existing business process that you want to automate. 

## What can you do with Automate Studio?

While Automate Studio enables you to rapidly develop AI solutions that run on Veritone's real time and horizontally scaling framework, what you build is entirely up to you. Want to send out email alerts when a Face is recognized? You can use Automate Studio to do that! Want to automate scraping the web for training data? You can do that too! You could even build a flow that texts your designated recipients and asks them to confirm if certain detections are accurate, and then setup logic to handle the recipient's text back!

## How does it work?

The Automate Studio is built with the Node-RED open source technology that is supported by the JS Foundation. At Veritone, we have taken this foundational open source technology and infused our own aiWARE palette of nodes that abstract away the underlying Veritone logic and data model, as well as make it easier for users to take advantage of the underlying power of aiWARE in a more approachable and less technically demanding format. 

For more info on how Automate Studio fits into the aiAWRE architecture, see the *Flow Engine* section of the docs.