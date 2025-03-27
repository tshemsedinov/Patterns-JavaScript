# 🧩 Шаблони для JavaScript та Node.js

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
    - [Фабричний метод (Factory method)](https://github.com/HowProgrammingWorks/Factory) — вибирає потрібну абстракцію для створення екземпляра, у JavaScript це можна реалізувати через `if`, `switch` або вибір конструктора з колекції.
    - [Прототип (Prototype)](https://github.com/HowProgrammingWorks/PrototypePattern) — клонування об'єкта із заздалегідь підготовленого екземпляра для економії ресурсів при створенні (не плутати з [прототипним наслідуванням](https://github.com/HowProgrammingWorks/Prototype), воно ближче до Flyweight).
    - [Легковаговик (Flyweight)](https://github.com/HowProgrammingWorks/Flyweight) — економія пам'яті для групи об'єктів через доступ до спільного (розділюваного) стану в конкретному екземплярі.
    - [Одинак (Singleton)](https://github.com/HowProgrammingWorks/Singleton) — глобальний доступ до єдиного екземпляра, часто вважається антипатерном, найпростіше реалізувати через кеш модульних систем ESM/CJS.
    - [Пул об'єктів (Object Pool)](https://github.com/HowProgrammingWorks/Pool) — повторне використання заздалегідь створених об'єктів для економії ресурсів при частому створенні й знищенні.
  - 🤝 Структурні шаблони
    - [Адаптер (Adapter)](https://github.com/HowProgrammingWorks/Adapter) — конвертер, що перетворює несумісний інтерфейс на сумісний, дозволяючи використовувати сторонній компонент без змін його коду, може перетворювати контракт функції в об'єкт або навпаки.
    - [Обгортка (Wrapper)](https://github.com/HowProgrammingWorks/Wrapper) — обгортка над функцією з прокиданням виклику (делегуванням) і додаванням поведінки, частковий випадок патерна Adapter.
    - Боксування (Boxing) — упаковка примітивів у об'єктні типи для додавання методів або уніфікації інтерфейсів, наприклад, звуження String до AddressString.
    - Декоратор — динамічно розширює поведінку без наслідування, зазвичай через композицію та декларативний синтаксис, по суті додає метадані.
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
- 🧩 Шаблони (патерни чи принципи) GRASP
  - 📢 Вступний семінар
    - [Загальний огляд GRASP](https://youtu.be/ExauFjYV_lQ)
    - Частина 1 - [GRASP для Node.js та Javascript](https://youtu.be/vm8p4jIQwp4)
    - Частина 2 - скоро
  - [Інформаційний експерт (Information expert)](https://youtu.be/cCHL329_As0)
  - Утворювач (Creator)
  - Контролер (Controller)
  - Ненаправленість (Indirection)
  - [Низьке зчеплення (Low coupling)](https://youtu.be/IGXdPOZ3Fyk)
  - [Висока згуртованість (High cohesion)](https://youtu.be/IGXdPOZ3Fyk)
  - Поліморфізм (Polymorphism)
  - Захищені варіації (Protected variations)
  - [Чиста вигадка (Pure fabrication)](https://youtu.be/CV577a0RHBM)
  - [Приклади коду](https://youtu.be/4AMVQ2-2DcM)
- 🧩 Шаблони (патерни чи принципи) SOLID
  - 📢 Вступний семінар: [SOLID for Node.js and Javascript](https://youtu.be/B2guSV8EMn0)
  - [SOLID питання на інтерв'ю](https://youtu.be/-9OM6-6pZw8)
  - [Принцип єдиної відповідальності (Single responsibility principle)](https://youtu.be/o4bQywkBKOI)
  - [Принцип відкритості/закритості (Open/closed principle)](https://github.com/HowProgrammingWorks/OpenClosed)
  - [Принцип підстановки Лісков (Liskov substitution principle)](https://youtu.be/RbhYxygxroc)
  - [Принцип розділення інтерфейсів (Interface segregation principle)](https://github.com/HowProgrammingWorks/InterfaceSegregation)
  - [Принцип інверсії залежностей (Dependency inversion principle)](https://github.com/HowProgrammingWorks/DependencyInversion)
