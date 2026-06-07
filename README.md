# HirdEngine
A PHP actor network framework compatible with both Swoole and PHP-FPM, designed around the architectural principles of 'The Method' by Juval Löwy.
We named it after **The Hird**—the elite, disciplined inner circle of Viking protectors who fought as an unbreakable shield wall to protect their king (the system you build)
For years, developers have faced an impossible choice when building complex, high-traffic systems:
**The Monolith:** Fast to start, but inevitably devolves into unmaintainable, intertwined spaghetti code where one bug crashes the whole system.
**The Microservice Tax:** Splitting the monolith solves isolation but introduces a massive new layer of network complexity, DevOps overhead, and exorbitant server costs.

**Hird Engine** was born from a desire to reject this compromise. After studying the book Righting Software by Juval Löwy and the Actor model from the 1970s, we started rethinking PHP architecture from the ground up, and built a framework that provides **microservice-level isolation without the network tax**, leveraging DI-container based actors living directly in the PHP runtime. It scales horisontaly out of the box and enforces a strict rules of architectual principles that have proven to make systems live longer than the expected lifetime of a system by isolating volatility, rather than functionality.

It also includes a no-trust security level and has a service-as-config system for CRUD operations with automatic database migration, so that developers can focus on contract design of the actors and the business logic. Everything else should be handled by the framwork.

The framework is in production now, and will be released here once the beta phase is over, early 2027. The goal is to provide it as Open Source and as a service with all the infrastructure needed including dev, staging and production envirnment, deployment, backup, logging and monitoring in a webbased control panel for ease of use and clarity. 

The framework will also by its nature solve a problem with AI assisted- or based development, where the isolation of actors will massivly reduce the damage a sometimes poorly written AI code might damage the system. It will also make it possible to maintaign the code better by siimply letting better models rewrite the code in safe,saml isolated parts of teh system with a strict contract protecting the surrounding services and actors (The handgranade principle)

For more info, or early access, send me a msg ar roy.arne@skeyl.app
