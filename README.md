# 🧩 Patterns for JavaScript, TypeScript, Node.js

> Rethinking GRASP (General Responsibility Assignment Software Patterns), SOLID (Single responsibility, Open–closed, Liskov substitution, Interface segregation, Dependency inversion), GoF (Gang of Four) patterns, for Frontend (browsers) & Backend (node.js, other runtimes) development with JavaScript and TypeScript

Translations:
[EN](https://github.com/tshemsedinov/Patterns-JavaScript/tree/en),
[UA](https://github.com/tshemsedinov/Patterns-JavaScript/tree/ua),
[RU](https://github.com/tshemsedinov/Patterns-JavaScript/tree/ru).

- 🧩 Patterns
  - 📢 [GoF patterns for Node.js and JavaScript (seminar fragment)](https://youtu.be/7TjzsZCQQqg)
  - 🏭 Creational patterns
    - [Abstract factory](https://github.com/HowProgrammingWorks/AbstractFactory) — creates related objects belonging to one family without specifying their concrete classes, e.g., UI components for different platforms.
    - [Builder](https://github.com/HowProgrammingWorks/Builder) — step-by-step assembly of a complex configurable object, often using chaining, e.g., Query Builder or Form Generator.
    - [Factory](https://github.com/HowProgrammingWorks/Factory) — function or method that creates objects using different techniques: assembling from literals and methods, mixins, setPrototypeOf.
    - [Factory Method](https://github.com/HowProgrammingWorks/FactoryMethod) — chooses the correct abstraction to create an instance; in JavaScript, this can be implemented using `if`, `switch`, or selection from a collection (dictionary).
    - [Prototype](https://github.com/HowProgrammingWorks/PrototypePattern) — creates objects by cloning a prepared instance to save resources (not to be confused with [Prototype-programming](https://github.com/HowProgrammingWorks/Prototype), which is closer to Flyweight).
    - [Flyweight](https://github.com/HowProgrammingWorks/Flyweight) — saves memory allocation by sharing common state among multiple instances.
    - [Singleton](https://github.com/HowProgrammingWorks/Singleton) — provides global access to a single instance; often considered an anti-pattern, easiest implemented via ESM/CJS module caching exported refs.
    - [Object Pool](https://github.com/HowProgrammingWorks/Pool) — reuses pre-created objects to save resources during frequent creation and destruction.
  - 🤝 Structural patterns
    - [Adapter](https://github.com/HowProgrammingWorks/Adapter) — converts an incompatible interface into a compatible one, enabling third-party component usage without altering its code; can even transform a function contract into an object or vice versa.
    - [Wrapper](https://github.com/HowProgrammingWorks/Wrapper) — function wrapper that delegates calls and adds behavior; a specialized case of Adapter.
    - Boxing — wraps primitives into object types to add methods or unify interfaces, e.g., narrowing `String` to `AddressString`.
    - Decorator 
    - [Decorator](https://github.com/HowProgrammingWorks/Decorator) — dynamically extends behavior without inheritance, typically via composition and declarative syntax, effectively adding metadata.
    - [Proxy](https://github.com/HowProgrammingWorks/Proxy) — controls access to an object by intercepting calls, reads, and writes; useful for lazy initialization, caching, and security; can be implemented via GoF or native JavaScript Proxy.
    - [Bridge](https://github.com/HowProgrammingWorks/Bridge) — separates two or more abstraction hierarchies via composition or aggregation, allowing them to evolve independently.
    - [Composite](https://github.com/HowProgrammingWorks/Composite) — implements a common interface to uniformly handle individual objects and their tree structures, e.g., DOM or file systems.
    - [Facade](https://github.com/HowProgrammingWorks/Facade) — simplifies access to a complex system, providing a unified and clear interface, hiding and protecting internal complexity.
    - [Flyweight](https://github.com/HowProgrammingWorks/Flyweight) — saves memory allocation by sharing common state among multiple instances.
  - ⚡ Behavioral patterns
    - [Chain of Responsibility](https://github.com/HowProgrammingWorks/ChainOfResponsibility) — passes control through a chain of handlers, selecting a responsible one; all handlers can read, but only one will modify.
    - [Middleware](https://www.youtube.com/watch?v=RS8x73z4csI) — handler chain similar to CoR, but each can modify state and pass control to the next one, potentially leading to race conditions and conflicts.
    - [Command](https://github.com/HowProgrammingWorks/Command) — encapsulates an action (execution request) and parameters into an object, allowing queuing, cancellation, repetition, etc.
    - [Interpreter](https://github.com/HowProgrammingWorks/Interpreter) — implements a DSL language (Domain Specific Language) or parses expressions into AST (Abstract Syntax Tree) for interpretation.
    - [Iterator](https://github.com/HowProgrammingWorks/Iterator) — sequentially traverses collections or streams element-by-element without exposing all data; JavaScript provides built-in Iterator and AsyncIterator.
    - [Mediator](https://github.com/HowProgrammingWorks/Mediator) — optimizes communication between N components, centralizing interaction to reduce coupling from `N*(N-1)/2` down to `N`.
    - [Memento](https://github.com/HowProgrammingWorks/Memento) — saves and restores snapshots of an object's state without direct access to its internal state.
    - [Observable](https://github.com/HowProgrammingWorks/Observer) — notifies subscribers about changes to an object's state via Events:
      - [EventEmitter](https://github.com/HowProgrammingWorks/EventEmitter) for Node.js: Observable + listener
      - [EventTarget](https://github.com/HowProgrammingWorks/Events) for Web API: EventTarget + Event (CustomEvent) + listener
      - [Signals](https://github.com/HowProgrammingWorks/Signals)
    - [State](https://github.com/HowProgrammingWorks/State) — implements a Finite State Machine (FSM) where methods represent transitions, and state is composed into abstraction and switched during transitions.
    - [Strategy](https://github.com/HowProgrammingWorks/Strategy) — selects interchangeable behavior at runtime from a collection of implementations: functions, objects, or classes
    - [Template method](https://github.com/HowProgrammingWorks/TemplateMethod) — defines algorithm steps, allowing subclasses to override individual steps while defaulting to the superclass behavior.
    - [Visitor](https://github.com/HowProgrammingWorks/Visitor) — adds operations to objects without altering their classes, separating structure and behavior into distinct abstractions.
    - [Revealing Constructor](https://github.com/HowProgrammingWorks/RevealingConstructor) — changes behavior without inheritance, injecting functionality into constructors via functions or objects describing the behavior.
    - [Actor](https://github.com/HowProgrammingWorks/Actor) – Encapsulates state and behavior, communicating asynchronously via message passing and processing messages in a queue. Ensures thread-safe and async-safe concurrent operations by isolating actor state.
    - [Reactor (event-loop)](https://github.com/HowProgrammingWorks/Reactor) - Handles concurrent events synchronously by adding them to queue and dispatching them to registered handlers. Implements event-driven async processing on the top of the sync one; commonly used in I/O-bound systems.
    - [Proactor](https://github.com/HowProgrammingWorks/Proactor) - Event loop where operations started by user-land code but completed by an external agent (for example I/O subsystem), which then triggers a completion handler when the operation finishes (returning data to callback).
- 🧩 GRASP patterns
  - 📢 Intro video
    - [GRASP Overview](https://youtu.be/ExauFjYV_lQ)
    - Part 1 - [GRASP for Node.js and Javascript](https://youtu.be/vm8p4jIQwp4)
    - Part 2 - coming soon
  - [Information expert](https://youtu.be/cCHL329_As0)
  - Creator
  - Controller
  - Indirection
  - [Low coupling](https://youtu.be/IGXdPOZ3Fyk)
  - [High cohesion](https://youtu.be/IGXdPOZ3Fyk)
  - Polymorphism
  - Protected variations
  - [Pure fabrication](https://youtu.be/CV577a0RHBM)
  - [Real code examples](https://youtu.be/4AMVQ2-2DcM)
- 🧩 SOLID Patterns
  - 📢 Intro video: [SOLID for Node.js and Javascript](https://youtu.be/B2guSV8EMn0)
  - [SOLID Interview questions](https://youtu.be/-9OM6-6pZw8)
  - [Single responsibility principle](https://youtu.be/o4bQywkBKOI)
  - [Open/closed principle](https://github.com/HowProgrammingWorks/OpenClosed)
  - [Liskov substitution principle](https://youtu.be/RbhYxygxroc)
  - [Interface segregation principle](https://github.com/HowProgrammingWorks/InterfaceSegregation)
  - [Dependency inversion principle](https://github.com/HowProgrammingWorks/DependencyInversion)
