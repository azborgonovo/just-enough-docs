
# just-enough-docs
Software teams often struggle with deciding what documentation is necessary for their own development lifecycle. Many software systems end up varying between no documentation at all or tons of paper which are useless and/or outdated.

This page defines a minimum set of documents that should provide the necessary information for its stakeholders and to enable them on understanding and taking correct decisions about the system.

A similar list was originally proposed in Tweeter by [@simonbrown](https://twitter.com/simonbrown), all credits to him. In order to record it for my own future projects as well as to serve as a point of research for the software community I decided to create this page.

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

As [evolutionary architecture](https://www.thoughtworks.com/radar/techniques/evolutionary-architecture) has been recommended as an alternative to traditional up-front, heavy-weight enterprise architectural designs, decisions have become more frequent in the lifecycle of a software system. Keeping record of such decisions is proven to be very helpful when the need of new changes emerge. To be able to clearly revisit the reasons (why) certain decisions have been made and what were the forces and alternatives considered previously may be a valuable input data to make a consistent and efficient new decision. 

The following template provides a fluent way to write down ADRs:

> **ADR 1: *[decision title]***
> In *[a system, context]* facing *[a requirement, situation, challenge]*
> we decided *[decision]* and not *[alternatives]*
> to achieve *[goal, benefits]* accepting *[constraints, drawbacks]*

### 5 - Lightweight Markdown docs

Beyond the previous document, extra information may still be needed to guide the stakeholders in the software. Lightweight Markdown files can fulfill this need with documents close to the source code (and possibly versioned), searcheable, easily updatable and nicely formatted.

There are references and templates that might inspire the fullfilment of this section (on-demand basis), such as the [Software Guidebook](https://softwarearchitecturefordevelopers.com/) or [arc42](https://arc42.org/overview/).

## Important docs for API providers

### 6 - Developer manual

When providing an [interface](https://martinfowler.com/bliki/PublishedInterface.html) to other developers (Class Library, Web API, etc) it is fundamental that clients can easily understand and get acquainted with consuming the provided functionalities.

Lightweight markdown files with a "Getting Started" or "How To" sections will come as a piece of cake and will increase the satisfaction of your fellow colleagues.

## Important docs for .NET Class Libraries

### 7 - XML comments of public types and members

It is essential that developers have useful and immediate feedback when coding against an API. This is usually achieved with an IDE with code-completion capabilities. In Visual Studio that is called [IntelliSense](https://docs.microsoft.com/en-us/visualstudio/ide/using-intellisense).

When providing .NET Class Libraries, do provide useful information of all your public types by exporting the [XML comments](https://docs.microsoft.com/en-us/dotnet/csharp/codedoc) to your consumers.

## References

(1) Quoted text and images by Simon Brown, licensed under [Creative Commons](https://creativecommons.org/licenses/by/4.0/). The System Context diagram and the Container diagram are part of the C4 Model Core diagrams. Access the [C4 Model website](https://c4model.com/#CoreDiagrams) for details.

(2) More information on Documenting Architecture Decisions: [http://thinkrelevance.com/blog/2011/11/15/documenting-architecture-decisions](http://thinkrelevance.com/blog/2011/11/15/documenting-architecture-decisions)
