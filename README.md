# HirdEngine
A PHP actor network framework compatible with both Swoole and PHP-FPM, designed around the architectural principles of 'The Method' by Juval Löwy.

# 🛡️ Hird Engine: The Philosophy of Controlled Chaos

> **"Traditional architecture scales by adding complexity. We scale by enforcing discipline."**

## 📖 The Backstory: Why Hird Engine Exists

For years, developers have faced an impossible choice when building complex, high-traffic systems:
1.  **The Monolith:** Fast to start, but inevitably devolves into unmaintainable, intertwined spaghetti code where one bug crashes the whole system.
2.  **The Microservice Tax:** Splitting the monolith solves isolation but introduces a massive new layer of network complexity, DevOps overhead, and exorbitant server costs.

**Hird Engine** was born from a desire to reject this compromise. After months of isolation and rethinking PHP architecture from the ground up, we built a framework that provides **microservice-level isolation without the network tax**, leveraging memory-based actors living directly in the PHP runtime (powered by Swoole). 

We named it after **The Hird**—the elite, disciplined inner circle of Viking protectors who fought as an unbreakable shield wall. In this engine, your data is the kingdom, and your code is the Hird.

## 🏛️ Core Principles & Values

Hird Engine isn't just a framework; it's a strict architectural philosophy. If you adopt Hird Engine, you are adopting these four core values:

### 1. Security by Obliteration (Zero-Trust Runtime)
We do not believe in "filtering" bad data; we believe in destroying the pathways it uses to enter. 
* **The Principle:** By design, Hird Engine purges all PHP Super Globals (`$_GET`, `$_POST`, etc.) the moment the system boots. 
* **The Value:** We create a pristine "Clean Room." Data only exists in the system if it has successfully passed through a strict, predefined Validation & Sanitation gate. You aren't just patching vulnerabilities; you are eliminating the environment where they breed.

### 2. The Sovereign Actor Model (Internal Immunity)
Systems shouldn't just be protected from the outside; they must be protected from themselves.
* **The Principle:** Instead of objects blindly calling other objects, everything is an **Actor**. Every Actor operates under a strict, immutable **Contract** and a policy of **Mutual Distrust**. 
* **The Value:** If one Actor (e.g., an API handler) is compromised or fails, it cannot destroy, alter, or sabotage neighboring Actors (e.g., the billing processor). This creates internal "Lateral Immunity."

### 3. Absolute Governance & Architectural Enforcement
A framework should prevent developers (or AI agents) from making critical architectural mistakes.
* **The Principle:** Actors are bound by granular **Right Limitations**. An Actor cannot perform an action (like a database write) unless its explicit contract allows it. 
* **The Value:** The architecture enforces your design. This makes the system incredibly safe for modern AI-assisted development—you can give an AI agent access to modify a single Actor, knowing the framework will physically prevent it from breaking the wider system.

### 4. Frictionless, Native Scale (The Shield Wall)
Scaling shouldn't require a total rewrite of your infrastructure. 
* **The Principle:** The engine features a built-in **Service Bridge** (for instant or queued message routing) and **File Cluster Sharing**, all natively aligned with horizontal scaling concepts like MariaDB Galera.
* **The Value:** When traffic spikes, you simply add another standard node to the network. Every new server is born with the exact same firewalls, resources, and limitations. The "Shield Wall" expands effortlessly.

## 🎯 Who is this for?

Hird Engine is not for building a simple blog. It is a battle-ready engine designed for:
* **Mission-Critical ERPs:** Where data integrity and module isolation are paramount.
* **High-Growth SaaS Platforms:** Where horizontal scaling needs to happen quickly and cheaply.
* **Complex Distributed Systems:** Where you need the discipline of microservices but the execution speed of a unified runtime.

## 🤝 The Promise
With Hird Engine, developers stop writing boilerplate security and infrastructure plumbing. You spend 100% of your time defining strict contracts and business logic. 

**Welcome to the Hird. Let's control the chaos.**
