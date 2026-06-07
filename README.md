# Hird Engine
A PHP actor network framework compatible with both Swoole and PHP-FPM, designed around the architectural principles of *Righting Software* ('The Method') by Juval Löwy.

For years, developers have faced an impossible choice when building complex, high-traffic systems:
* **The Monolith:** Fast to start, but inevitably devolves into unmaintainable, intertwined spaghetti code where a single bug can crash the entire system.
* **The Microservice Tax:** Splitting the monolith solves isolation but introduces a massive new layer of network complexity, DevOps overhead, and exorbitant server costs.

**Hird Engine** was born from a desire to reject this compromise. After studying Juval Löwy's architectural methodologies and the foundational Actor Model from the 1970s, we rethought PHP architecture from the ground up. The result is a framework that provides **microservice-level isolation without the network tax**, leveraging DI-container-based actors living directly in the PHP runtime. 

It scales horizontally out of the box and enforces strict architectural principles proven to extend a system's lifespan far beyond the norm, specifically by isolating *volatility* rather than just functionality.

So we named it after the elite, disciplined inner circle of Viking warriors who fought as an unbreakable shield wall to protect their king, called **The Hird**.

### Core Features
* **Zero-Trust Security & Dynamic Firewall**
  Built from the ground up with a strict, no-trust security model. The engine includes an active, cluster-aware firewall with automated IP blacklisting, geolocation restrictions, and built-in rate limiting. It also features an "Early Exit Filter" that handles routine requests (like pings or robot blocks) in milliseconds without waking up the application logic.

* **The Service Bridge (Actor Networking)**
  Instead of fragile external API calls between microservices, Hird Engine uses a native Service Bridge. It securely routes messages between isolated actors across the entire cluster, enforcing mutual distrust and contract validation on every payload. It seamlessly handles both instant delivery and queued task execution.

* **Strict Architectural Governance**
  The framework does not just suggest good architecture; it enforces it at runtime. Configuration rules physically prevent unauthorized actions, such as enforcing that only specific Resource Access actors can touch the database, strictly enforcing actor boundaries, and maintaining call hierarchy. 

* **Dynamic & Resilient Routing**
  Features an intelligent routing engine capable of scanning for new endpoints dynamically (even recovering from 404s) and seamlessly falling back to robust file-based routing. This eliminates massive, hard-to-maintain central routing tables while maintaining blistering performance.

* **Service-as-Config (Auto-CRUD & Auto-Docs)**
  Features an automated CRUD system with built-in database migrations, automated table generation, and automatic API documentation. Developers focus entirely on designing Actor Contracts and business logic; the framework handles the data layer natively.

* **Distributed Queue & Task Scheduler**
  No need for external tools like Redis or server crontabs. Hird Engine includes a native, distributed queue system (with worker scaling, failure retries, and execution limits) and a built-in Task Scheduler for background jobs and maintenance cycles.

* **Integrated Messaging & Smart Alarms**
  The engine comes with native SMS (GatewayAPI) and Email (SendGrid) integration built-in. It continuously monitors its own health—tracking memory consumption, slow database queries, FPM pool utilization, and queue backlogs. If thresholds are breached, the Smart Alarm system routes alerts via these channels, utilizing intelligent duplicate suppression to prevent alert fatigue.

* **Native Event Streams & Clustered File Sync**
  Real-time data is handled out of the box with native Server-Sent Events (SSE) configuration. Additionally, the engine handles its own distributed state with an automated File Store Sync that seamlessly propagates files across your cluster network.

* **AI-Ready Architecture**
  By its nature, the framework mitigates the risks of AI-assisted development. The strict isolation of actors ("The Hand Grenade Principle") massively reduces the blast radius of poorly written AI code. It allows developers to safely use AI models to rewrite code in small, isolated parts of the system, confident that strict contracts will protect the surrounding services.

### Current Status & Roadmap
Hird Engine is currently running in production. The open-source code will be released here once the beta phase concludes in early 2027. 

Our ultimate goal is to provide Hird Engine both as Open Source software and as a fully managed Platform-as-a-Service (PaaS). The managed service will include all necessary infrastructure for development, staging, and production environments, deployment pipelines, backups, logging, and monitoring. Crucially, this PaaS will be accessible not only via an intuitive web-based control panel, but also through a dedicated programmatic MVC/API layer. This ensures that autonomous AI agents can seamlessly interact with, manage, and scale the infrastructure on your behalf.

**For more information or to request early access, please contact me at:** roy.arne@skeyl.app
