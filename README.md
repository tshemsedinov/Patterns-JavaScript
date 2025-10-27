# 🧩 Шаблони для JavaScript, TypeScript та Node.js

> Переосмислення шаблонів GRASP (розподілу обов’язків - General Responsibility Assignment Software Patterns), SOLID (єдина відповідальність, відкритий–закритий, підстановка Лісков, розподілення інтерфейсів, інверсія залежностей), шаблони GoF (Банда чотирьох) для фронтенду (браузери) і бекенду (node.js, інші рантайми) розробки на JavaScript і TypeScript

Переклади:
[EN](https://github.com/tshemsedinov/Patterns-JavaScript/tree/en),
[UA](https://github.com/tshemsedinov/Patterns-JavaScript/tree/ua),
[RU](https://github.com/tshemsedinov/Patterns-JavaScript/tree/ru).

- 🧩 Патерни
  - 📢 [GoF патерни для Node.js та JavaScript (фрагмент семінару)](https://youtu.be/7TjzsZCQQqg)
  - 🏭 Шаблони, що породжують
    - [Абстрактна фабрика (Abstract factory)](https://github.com/HowProgrammingWorks/AbstractFactory) — створює пов’язані об'єкти одного сімейства без зазначення їх конкретних класів, наприклад, візуальні компоненти під різні платформи.
    - [Будівельник (Builder)](https://github.com/HowProgrammingWorks/Builder) — покрокова збірка складного об'єкта з можливістю конфігурації, часто через чейнінг, наприклад, Query Builder або Form Generator.
    - [Фабрика (Factory)](https://github.com/HowProgrammingWorks/Factory) — функція або метод для створення об'єктів різними способами: складанням частинами з літералів об'єктів і окремих методів, через міксіни, setPrototypeOf.
    - [Фабричний метод (Factory method)](https://github.com/HowProgrammingWorks/FactoryMethod) — вибирає потрібну абстракцію для створення екземпляра, у JavaScript це можна реалізувати через `if`, `switch` або вибір конструктора з колекції.
    - [Прототип (Prototype)](https://github.com/HowProgrammingWorks/PrototypePattern) — клонування об'єкта із заздалегідь підготовленого екземпляра для економії ресурсів при створенні (не плутати з [прототипним наслідуванням](https://github.com/HowProgrammingWorks/Prototype), воно ближче до Flyweight).
    - [Легковаговик (Flyweight)](https://github.com/HowProgrammingWorks/Flyweight) — економія пам'яті для групи об'єктів через доступ до спільного (розділюваного) стану в конкретному екземплярі.
    - [Одинак (Singleton)](https://github.com/HowProgrammingWorks/Singleton) — глобальний доступ до єдиного екземпляра, часто вважається антипатерном, найпростіше реалізувати через кеш модульних систем ESM/CJS.
    - [Пул об'єктів (Object Pool)](https://github.com/HowProgrammingWorks/Pool) — повторне використання заздалегідь створених об'єктів для економії ресурсів при частому створенні й знищенні.
  - 🤝 Структурні шаблони
    - [Адаптер (Adapter)](https://github.com/HowProgrammingWorks/Adapter) — конвертер, що перетворює несумісний інтерфейс на сумісний, дозволяючи використовувати сторонній компонент без змін його коду, може перетворювати контракт функції в об'єкт або навпаки.
    - [Обгортка (Wrapper)](https://github.com/HowProgrammingWorks/Wrapper) — обгортка над функцією з прокиданням виклику (делегуванням) і додаванням поведінки, частковий випадок патерна Adapter.
    - [Боксування (Boxing)](https://github.com/HowProgrammingWorks/ADT) — упаковка примітивів у об'єктні типи для додавання методів або уніфікації інтерфейсів, наприклад, звуження String до AddressString.
    - [Декоратор](https://github.com/HowProgrammingWorks/Decorator) — динамічно розширює поведінку без наслідування, зазвичай через композицію та декларативний синтаксис, по суті додає метадані.
    - [Проксі чи Замісник (Proxy)](https://github.com/HowProgrammingWorks/Proxy) — контролює доступ до об'єкта, перехоплює виклики, читання та запис, може застосовуватись для лінивої ініціалізації, кешування та безпеки; реалізується як через патерн GoF, так і вбудованим JavaScript Proxy.
    - [Міст (Bridge)](https://github.com/HowProgrammingWorks/Bridge) — розділення двох або більше ієрархій абстракцій через композицію або агрегацію, дозволяючи їм змінюватися незалежно.
    - [Компоновщик (Composite)](https://github.com/HowProgrammingWorks/Composite) — реалізує загальний інтерфейс, що дозволяє однаково працювати з окремими об'єктами та їхніми деревами, наприклад, DOM чи файлова система.
    - [Фасад (Facade)](https://github.com/HowProgrammingWorks/Facade) — спрощує доступ до складної системи, надаючи єдиний і зрозумілий інтерфейс споживачеві (коду, що використовує), захищає та приховує складність.
    - [Легковаговик (Flyweight)](https://github.com/HowProgrammingWorks/Flyweight) — економія пам'яті для групи об'єктів через доступ до спільного (розділюваного) стану в конкретному екземплярі.
  - ⚡ Шаблони поведінки
    - [Ланцюжок відповідальності (Chain of responsibility)](https://github.com/HowProgrammingWorks/ChainOfResponsibility) — передача управління ланцюжком обробників для вибору відповідального, читають всі, але змінити може тільки один.
    - [Middleware](https://www.youtube.com/watch?v=RS8x73z4csI) — ланцюжок обробників, як CoR, але кожен може змінювати стан і передавати управління далі, що може призводити до гонки, конфліктів, помилок.
    - [Команда (Command)](https://github.com/HowProgrammingWorks/Command) — інкапсулює дію (запит на виконання) та її параметри в об'єкт, щоб передавати виконавцю, ставити в чергу, скасовувати, повторювати тощо.
    - [Інтерпретатор (Interpreter)](https://github.com/HowProgrammingWorks/Interpreter) — реалізація мови (DSL—предметно-орієнтована мова) або розбір виразів у AST (абстрактне синтаксичне дерево) з можливістю інтерпретації.
    - [Ітератор (Iterator)](https://github.com/HowProgrammingWorks/Iterator) — послідовний обхід колекції або потоку без доступу до всіх даних; у JavaScript є вбудовані Iterator та AsyncIterator.
    - [Посередник (Mediator)](https://github.com/HowProgrammingWorks/Mediator) — оптимізація взаємодії між N компонентами, що потребували б N*(N-1)/2 зв’язків, а централізація взаємодії знижує зв’язність до N.
    - [Знімок (Memento)](https://github.com/HowProgrammingWorks/Memento) — збереження та відновлення історії станів об'єкта без прямого доступу до самого стану.
    - [Спостерігач (Observer)](https://github.com/HowProgrammingWorks/Observer) — повідомлення підписників про зміни стану об’єкта.
      - [EventEmitter](https://github.com/HowProgrammingWorks/EventEmitter) для Node.js: Observable + listener
      - [EventTarget](https://github.com/HowProgrammingWorks/Events) для Web API: EventTarget + Event (CustomEvent) + listener
      - [Signal](https://github.com/HowProgrammingWorks/Signals)
    - [Стан (State)](https://github.com/HowProgrammingWorks/State) — реалізація скінченного автомата (FSM), де методи — це переходи, а стан додається через композицію та змінюється при переходах.
    - [Стратегія (Strategy)](https://github.com/HowProgrammingWorks/Strategy) — вибір взаємозамінної поведінки в рантаймі через колекцію реалізацій: функцій, об'єктів, класів.
    - [Шаблонний метод (Template method)](https://github.com/HowProgrammingWorks/TemplateMethod) — фіксує кроки алгоритму, дозволяючи підкласам перевизначати окремі кроки та використовувати кроки предка як поведінку за замовчуванням.
    - [Відвідувач (Visitor)](https://github.com/HowProgrammingWorks/Visitor) — дозволяє додавати операції до об'єктів без зміни їх класів, розділяючи структуру та поведінку на кілька абстракцій.
    - [Відкритий конструктор (Revealing Constructor)](https://github.com/HowProgrammingWorks/RevealingConstructor) — зміна поведінки без наслідування, впровадження поведінки в конструктор у вигляді функції чи об'єкта, що містить поведінку та її опис.
    - Реактор (Reactor, event-loop) – Обрабатывает параллельные события синхронно, помещая их в очередь и направляя зарегистрированным обработчикам. Реализует событийно-ориентированную асинхронную обработку поверх синхронного цикла событий. Часто применяется в системах с интенсивным I/O, упрощая управление конкурентными событиями.
    - [Actor](https://github.com/HowProgrammingWorks/Actor) — Інкапсулює стан та поведінку, взаємодіючи асинхронно через передачу та послідовну обробку повідомлень у черзі. Забезпечує потокову та асинхронну безпеку при паралельному виконанні через ізоляцію стану актора.
    - [Reactor (event-loop)](https://github.com/HowProgrammingWorks/Reactor) — Обробляє конкурентні події синхронно, додаючи їх до черги та спрямовуючи до зареєстрованих обробників. Реалізує подієво-орієнтовану асинхронну обробку на основі синхронного циклу подій. Часто використовується в системах з інтенсивним I/O, спрощуючи керування конкурентними подіями.
    - [Proactor](https://github.com/HowProgrammingWorks/Proactor) — Цикл подій, у якому операції розпочинаються кодом користувача, але завершуються зовнішнім агентом (наприклад, I/O підсистемою), який запускає обробник завершення, коли операція завершується (повернення даних відбувається через callback).
  Translate into ukrainian in same md format:
  - 🗃️ Шаблони доступу до даних
    - [Transaction Script](https://github.com/HowProgrammingWorks/TransactionScript) — процедурний шаблон, у якому кожна бізнес-операція реалізується як функція (процедура або скрипт).
    - Pattern SAGA — шаблон розподіленої транзакції, у якому складний бізнес-процес розбивається на послідовність малих транзакцій, кожна з яких має компенсуючу дію на випадок збою. Дозволяє уникати розподілених блокувань.
    - Unit of Work — шаблон відстежує зміни у бізнес-об'єктах і координує збереження як одну атомарну операцію в ORM або Repository, інкапсулюючи всю роботу в межах транзакції.
    - Table Module — шаблон, у якому вся доменна логіка, пов’язана з таблицею бази даних, інкапсулюється в одному класі або модулі, при цьому рядки розглядаються як прості дані.
    - [Value Object](https://github.com/HowProgrammingWorks/ValueObject) — незмінний, самоперевіряючийся об'єкт, що представляє концепт у домені без ідентифікатора. Використовується для вираження доменних обмежень і узгодженості логіки значень, порівняння за значенням у типобезпечній, явно вираженій формі.
    - [Null Object](https://github.com/HowProgrammingWorks/ValueObject) — об'єкт, який реалізує стандартний інтерфейс, але надає нейтральну поведінку «do-nothing». Призначений для уникнення перевірок на null, спрощення логіки та забезпечення поліморфної безпеки. Є заміною дії «за замовчуванням», що усуває умовні конструкції та перевірки через гварди.
    - [Active Record](https://github.com/HowProgrammingWorks/ActiveRecord) — доменний об'єкт, що інкапсулює запис у таблиці бази даних і надає методи для безпосереднього виконання операцій CRUD (створення, читання, оновлення, видалення) та специфічних запитів до себе.
    - [Data access object (DAO)](https://github.com/HowProgrammingWorks/Repository) — абстракція, яка визначає інтерфейс для збереження та отримання доменних об'єктів, ізолюючи доменну логіку від конкретних реалізацій сховища.
    - Data transfer object (DTO) — анемічний об'єкт (лише дані) без доменної поведінки, призначений виключно для передавання структурованих даних між шарами, модулями, підсистемами або архітектурними межами.
    - Data Access Layer (DAL) — шар, що абстрагує доступ до множини DAO або сирих джерел даних. Може бути реалізований як шаблон Facade. Часто включає трансформацію даних.
    - [Repository](https://github.com/HowProgrammingWorks/Repository) — доменно-центрична абстракція для доступу до даних, яка повертає доменні сутності, а не сирі дані або DTO.
    - Див. інші шаблони: [Template method](https://github.com/HowProgrammingWorks/TemplateMethod), [Actor](https://github.com/HowProgrammingWorks/Actor), [State](https://github.com/HowProgrammingWorks/State), [Memento](https://github.com/HowProgrammingWorks/Memento)
- 🧩 Шаблони (патерни чи принципи) GRASP
  - [Загальний огляд GRASP](https://youtu.be/ExauFjYV_lQ)
  - [GRASP Part 1: Information expert, Creator, Low coupling, High cohesion](https://youtu.be/vm8p4jIQwp4)
  - [GRASP Part 2: Protected variations, Indirection, Pure fabrication, Polymorphism, Controller](https://youtu.be/aJGB7TLwiig)
  - [Інформаційний експерт (Information expert)](https://youtu.be/cCHL329_As0)
  - [Низьке зчеплення (Low coupling)](https://youtu.be/IGXdPOZ3Fyk)
  - [Висока згуртованість (High cohesion)](https://youtu.be/IGXdPOZ3Fyk)
  - [Поліморфізм (Polymorphism)](https://youtu.be/IGXdPOZ3Fyk)
  - [Чиста вигадка (Pure fabrication)](https://youtu.be/CV577a0RHBM)
  - [Приклади коду](https://youtu.be/4AMVQ2-2DcM)
  - Information Expert - розподіляйте обов'язок із виконання завдання на ті абстракції, які мають потрібні дані. Пов'язано: Encapsulation, Cohesion, Coupling, Information hiding, SOLID: SRP, SoC.
  - Creator - якщо одна абстракція пише, читає, аггрегує, використовує, та сильно зачеплена з іншою, то вона і повинна її створювати та ініціалізувати. Зв'язно: Information Expert, GoF Creational patterns.
  - Controller - містить use-case сценарії обробки зовнішніх I/O запитів, від UI, API чи Event Bus і делегує виконання іншим абстракціям. Пов'язано: GoF Command, Facade, Layers, Pure Fabrication.
  - Low Coupling – кожна абстракція мінімально залежить від деталей реалізації інших, містить мінімум "знань" (звернень). Дає стійкість, простоту тестування та супроводу. Пов'язано: High Cohesion, Controller, Indirection, DIP, DI, IoC, Revealing constructor, Facade, Mediator, Observer, Strategy, State, Bridge, Adapter, Proxy.
  - High Cohesion - усі внутрішні елементи абстракції тісно пов'язані спільною метою і "знають" контракти одне одного, спільно вирішують одну конкретну задачу. Такі абстракції легко розуміються, тестуються та супроводжуються. Пов'язано: Low Coupling, Information Expert, Composite, Facade, Adapter. Висока зв'язаність усередині модуля та низьке зачеплення між модулями дають стійкість системи.
  - Polymorphism - за допомогою динамічної диспетчеризації абстракції вибирають поведінку та делегують дії об'єктам із загальним інтерфейсом замість явного розгалуження за типом. Пов'язано: GoF Strategy, Adapter, Creator, Command, State, Bridge, Template Method, Visitor, Factory Method, Proxy.
  - Pure Fabrication – штучні абстракції, які не належать до предметної області, а обслуговують структурні, архітектурні та технічні потреби. Пов'язано: SRP, ISP, GoF: Facade, Adapter, Observer, Command, Mediator, Repository, Service. Приклади: EventEmitter, Stream, Connection, Promise, Error.
  - Indirection – посередник для реалізації слабкого зачеплення між компонентами. Пов'язані: GoF Mediator, Facade, Observer, Service Layer, API Gateway, Message Broker, Event Bus.
  - Protected Variations - захищає абстракції від зміни за допомогою винесення взаємодії у фіксований інтерфейс, тільки через який можлива взаємодія між абстракціями. Пов'язано: Interface, Contract programing, Generics, OCP, DIP, DI, IoC, GoF: Strategy, Bridge, Abstract Factory, Factory Method, Adapter, Proxy, Facade.
- 🧩 Шаблони (патерни чи принципи) SOLID
  - 📢 Вступний семінар: [SOLID for Node.js and Javascript](https://youtu.be/B2guSV8EMn0)
  - [SOLID питання на інтерв'ю](https://youtu.be/-9OM6-6pZw8)
  - [Принцип єдиної відповідальності (Single responsibility principle)](https://youtu.be/o4bQywkBKOI)
  - [Принцип відкритості/закритості (Open/closed principle)](https://github.com/HowProgrammingWorks/OpenClosed)
  - [Принцип підстановки Лісков (Liskov substitution principle)](https://youtu.be/RbhYxygxroc)
  - [Принцип розділення інтерфейсів (Interface segregation principle)](https://github.com/HowProgrammingWorks/InterfaceSegregation)
  - [Принцип інверсії залежностей (Dependency inversion principle)](https://github.com/HowProgrammingWorks/DependencyInversion)
  - Single responsibility principle - у абстракції має бути лише одна причина зміни. "Модуль повинен відповідати за одного і тільки за одного актора."
  - Open-closed principle - абстракції (класи, типи тощо.) мають бути відкриті для розширення, але закриті для модифікації.
  - Liskov substitution principle - функції, які використовують базовий тип, повинні мати можливість використовувати підтипи базового типу, не знаючи про це.
  - Interface segregation principle – багато інтерфейсів, спеціально призначених для клієнтів, краще ніж один інтерфейс загального призначення.
  - Dependency inversion principle - Залежність на абстракції. Немає залежностей від конкретного.
