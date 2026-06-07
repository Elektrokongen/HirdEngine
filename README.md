# Hird Engine
A PHP actor network framework compatible with both Swoole and PHP-FPM, designed around the architectural principles of *Righting Software* ('The Method') by Juval Löwy.

We named it after **The Hird**—the elite, disciplined inner circle of Viking protectors who fought as an unbreakable shield wall to protect their king (the system you build).

For years, developers have faced an impossible choice when building complex, high-traffic systems:
* **The Monolith:** Fast to start, but inevitably devolves into unmaintainable, intertwined spaghetti code where a single bug can crash the entire system.
* **The Microservice Tax:** Splitting the monolith solves isolation but introduces a massive new layer of network complexity, DevOps overhead, and exorbitant server costs.

**Hird Engine** was born from a desire to reject this compromise. After studying Juval Löwy's architectural methodologies and the foundational Actor Model from the 1970s, we rethought PHP architecture from the ground up. The result is a framework that provides **microservice-level isolation without the network tax**, leveraging DI-container-based actors living directly in the PHP runtime. 

It scales horizontally out of the box and enforces strict architectural principles proven to extend a system's lifespan far beyond the norm—specifically by isolating *volatility* rather than just functionality.

### Core Features
* **Zero-Trust Security:** Built from the ground up with a strict, no-trust security model.
* **Service-as-Config (Auto-CRUD):** Features an automated CRUD system with built-in database migrations. Developers can focus entirely on designing the Actor Contracts and writing business logic; the framework handles the rest.
* **AI-Ready Architecture:** By its nature, the framework mitigates the risks of AI-assisted development. The strict isolation of actors ("The Hand Grenade Principle") massively reduces the blast radius of poorly written AI code. It also allows developers to safely use newer AI models to rewrite code in small, isolated parts of the system, confident that strict contracts will protect the surrounding services.

### Current Status & Roadmap
Hird Engine is currently running in production. The open-source code will be released here once the beta phase concludes in early 2027. 

Our ultimate goal is to provide Hird Engine both as Open Source software and as a fully managed Platform-as-a-Service (PaaS). The managed service will include all necessary infrastructure—development, staging, and production environments, deployment pipelines, backups, logging, and monitoring. Crucially, this PaaS will be accessible not only via an intuitive web-based control panel, but also through a dedicated programmatic MVC/API layer. This ensures that autonomous AI agents can seamlessly interact with, manage, and scale the infrastructure on your behalf.

**For more information or to request early access, please contact me at:** roy.arne@skeyl.app
