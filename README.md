# just-enough-docs
Software teams often struggle with deciding what documentation is necessary for their own development lifecycle. Many software systems end up varying between no documentation at all or tons of paper which are useless and/or outdated.

This page defines a minimum set of documents that should provide the necessary information for the stakeholders to enable them in understanding and taking correct decisions about the system.

This list was originally suggested by [@simonbrown](https://twitter.com/simonbrown), all credits to him. In order to record it for my own future projects as well as to serve as a point of research for the software community I decided to create this page.

## Documents
### 1 - System Context diagram
"A System Context diagram is a good starting point for diagramming and documenting a software system, allowing you to step back and see the big picture. Draw a diagram showing your system as a box in the centre, surrounded by its users and the other systems that it interacts with.

Detail isn't important here as this is your zoomed out view showing a big picture of the system landscape. The focus should be on people (actors, roles, personas, etc) and software systems rather than technologies, protocols and other low-level details. It's the sort of diagram that you could show to non-technical people." (1)

![enter image description here](https://c4model.com/img/bigbankplc-SystemContext.png)

### 2 - Container diagram

"Once you understand how your system fits in to the overall IT environment, a really useful next step is to zoom-in to the system boundary with a Container diagram. A "container" is something like a server-side web application, single-page application, desktop application, mobile app, database schema, file system, etc. Essentially, a container is a separately runnable/deployable unit (e.g. a separate process space) that executes code or stores data.

The Container diagram shows the high-level shape of the software architecture and how responsibilities are distributed across it. It also shows the major technology choices and how the containers communicate with one another. It's a simple, high-level technology focussed diagram that is useful for software developers and support/operations staff alike." (1)

![enter image description here](https://c4model.com/img/bigbankplc-Containers.png)

### 3 - Deployment diagram(s)

"A deployment diagram allows you to illustrate how containers in the static model are mapped to infrastructure. This deployment diagram is based upon a  [UML deployment diagram](https://en.wikipedia.org/wiki/Deployment_diagram), although simplified slightly to show the mapping between  **containers**  and  **deployment nodes**. A deployment node is something like physical infrastructure (e.g. a physical server or device), virtualised infrastructure (e.g. IaaS, PaaS, a virtual machine), containerised infrastructure (e.g. a Docker container), an execution environment (e.g. a database server, Java EE web/application server, Microsoft IIS), etc. Deployment nodes can be nested.

You may also want to include infrastructure nodes such as DNS services, load balancers, firewalls, etc." (1)

### 4 - Architecture Decision Records

A collection of records for "architecturally significant" decisions like those that affect the system structure, non-functional characteristics, dependencies, interfaces, or construction techniques. (2)

Keeping a record of such decisions is proven do be very helpful both to support on balancing the tradeoffs when making the decision as well as to clearly keep track of **why** certain decisions have been taken.

A template that is friendly and may be used is the following: 

ADR 1: Deployment on Ruby on Rails 3.0.10
TODO: ....

### 5 - Lightweight Markdown docs

(e.g. software guidebook, or arc42)
## Additional docs for .NET Class Libraries
### 6 - XML comments of public types

It is essential that developers have useful and immediate feedback when coding against an API. This is usually achieved with an IDE with  code completion capabilities. In Visual Studio this is named [IntelliSense](https://docs.microsoft.com/en-us/visualstudio/ide/using-intellisense).

When providing .NET Class Libraries, do provide useful information of all your public types by exporting the [XML comments](https://docs.microsoft.com/en-us/dotnet/csharp/codedoc) to your consumers. 

## References
(1) Text and images by Simon Brown, licensed under [Creative Commons](https://creativecommons.org/licenses/by/4.0/). The System Context diagram and the Container diagram are part of the C4 Model Core diagrams. Access the [C4 Model website](https://c4model.com/#CoreDiagrams) for more information.

(2) More information on Documenting Architecture Decisions: [http://thinkrelevance.com/blog/2011/11/15/documenting-architecture-decisions](http://thinkrelevance.com/blog/2011/11/15/documenting-architecture-decisions)
