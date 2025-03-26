# 🧩 Патерны для JavaScript и Node.js

> Переосмысление GRASP (разделения ответственности - General Responsibility Assignment Software Patterns), SOLID (единственной ответственности, открытый-закрытый, подстановки Лисков, разделения интерфейсов, инверсии зависимостей), GoF (Банды четырех - Gang of Four) для фронтенда (браузерное программирование) & бекенда (node.js, другие рантаймы) разработки на JavaScript и TypeScript

Переводы:
[EN](https://github.com/tshemsedinov/Patterns-JavaScript/tree/en),
[UA](https://github.com/tshemsedinov/Patterns-JavaScript/tree/ua),
[RU](https://github.com/tshemsedinov/Patterns-JavaScript/tree/ru).

- 🧩 Патерны GoF
  - 📢 [GoF патерны для Node.js и JavaScript (фрагмент семинара)](https://youtu.be/7TjzsZCQQqg)
  - 🏭 Порождающие шаблоны
    - [Абстрактная фабрика (Abstract factory)](https://github.com/HowProgrammingWorks/AbstractFactory) — создает связанные объекты, принадлежащие одному из семейств, без указания их конкретных классов, например, визуальные компоненты под разные платформы.
    - [Строитель (Builder)](https://github.com/HowProgrammingWorks/Builder) — пошаговая сборка сложного объекта с возможностью конфигурации, часто с помощью чеининга, например, Query Builder или Form Generator.
    - [Фабрика (Factory)](https://github.com/HowProgrammingWorks/Factory) — функция или метод для создания объектов различными способами: сборки по частям из литералов объектов и отдельных методов, через примеси, setPrototypeOf.
    - Фабричный метод (Factory method) — выбирает нужную абстракцию для создания экземпляра, в JavaScript это можно сделать через if, switch или выбор конструктора из коллекции.
    - [Прототип (Prototype)](https://github.com/HowProgrammingWorks/PrototypePattern) — клонирование объекта из заранее подготовленного экземпляра, для экономии ресурсов на создание (не путать с [прототипным наследованием](https://github.com/HowProgrammingWorks/Prototype), оно ближе к Flyweight).
    - [Flyweight](https://github.com/HowProgrammingWorks/Flyweight) — экономия выделения памяти для группы объектов через проброс доступа к общему (разделяемому) состоянию, у конкретного инстанса.
    - [Одиночка (Singleton)](https://github.com/HowProgrammingWorks/Singleton) — глобальный доступ к единственному экземпляру, часто считаться анти-паттерном, проще всего реализовать через кэш системы модульности ESM/CJS.
    - [Object Pool](https://github.com/HowProgrammingWorks/Pool) — повторное использование заранее созданных объектов для экономии ресурсов при частом создании и уничтожении.
  - 🤝 Структурные шаблоны
    - [Адаптер (Adapter)](https://github.com/HowProgrammingWorks/Adapter) — конвертор, преобразует несовместимый интерфейс в совместимый, позволяя использовать сторонний компонент без изменения его кода, можно даже преобразовать контракт функции в объект или наоборот.
    - [Обертка (Wrapper)](https://github.com/HowProgrammingWorks/Wrapper) — обертка над функцией с пробросом вызова (делегирование) с добавлением поведения, частный случай паттерна Adapter.
    - Boxing — упаковка примитивов в объектные типы для добавления методов или унификации интерфейсов, например, можно сузить String до AddressString.
    - Decorator — динамически расширяет поведение без наследования, обычно через композицию и декларативный синтаксис, по сути добавляет метаданные.
    - [Прокси (Proxy)](https://github.com/HowProgrammingWorks/Proxy) — контролирует доступ к объекту, перехватывая вызовы, чтение и запись, может применяться для ленивой инициализации, кэширования и безопасности, может реализовываться как в GoF или встроенным в JavaScript Proxy.
    - [Мост (Bridge)](https://github.com/HowProgrammingWorks/Bridge) — разделение двух и более иерархий абстракций за счет композиции или агрегации, позволяя им изменяться независимо.
    - [Компоновщик (Composite)](https://github.com/HowProgrammingWorks/Composite) — реализует общий интерфейс, который позволяет единообразно работать с отдельными объектами деревьями объектов, например, DOM или файловая система.
    - [Фасад (Facade)](https://github.com/HowProgrammingWorks/Facade) — упрощает доступ к сложной системе, предоставляя потребителю (использующему коду) единый и понятный интерфейс, для защиты и сокрытия сложности.
    - [Легковес (Flyweight)](https://github.com/HowProgrammingWorks/Flyweight) — экономия выделения памяти для группы объектов через проброс доступа к общему (разделяемому) состоянию, у конкретного инстанса.
  - ⚡ Поведенческие шаблоны
    - [Цепочка обязанностей (Chain of responsibility)](https://github.com/HowProgrammingWorks/ChainOfResponsibility) — передача управления по цепочке обработчиков для выбора одного ответственного, все в цепочке читают, но менять может только один.
    - [Middleware](https://www.youtube.com/watch?v=RS8x73z4csI) — цепочка обработчиков, как CoR, но каждый может изменять состояние и передавать управление дальше, что может привести к гонке, конфликтам, ошибкам.
    - [Команда (Command)](https://github.com/HowProgrammingWorks/Command) — инкапсулирует действие (запрос исполнения) и его параметры в объект, чтоб передавать исполнителю, ставить в очередь, отменять, повторять и т.д.
    - [Интерпретатор (Interpreter)](https://github.com/HowProgrammingWorks/Interpreter) — реализация языка (DSL - domain specific language) или разбор выражений в AST (абстрактное синтаксическое дерево) с возможностью интерпретации.
    - [Итератор (Iterator)](https://github.com/HowProgrammingWorks/Iterator) — обход коллекции или потока поэлементно, без доступа ко всем данным, можно сделать как в GoF, но в JavaScript есть встроенные Iterator и AsyncIterator.
    - [Посредний (Mediator)](https://github.com/HowProgrammingWorks/Mediator) — оптимизация взаимодействия между N компонентами, что потребовало бы N * (N - 1) / 2 связей, а централизация взаимодействия снижает зацепление до N.
    - [Снимок (Memento)](https://github.com/HowProgrammingWorks/Memento) — сохранение и восстановление истории снимков состояния объекта, без прямого доступа к самому состоянию.
    - [Наблюдатель (Observable)](https://github.com/HowProgrammingWorks/Observer) — уведомление подписчиков об изменении состояния объекта.
      - [EventEmitter](https://github.com/HowProgrammingWorks/EventEmitter) для Node.js: Observable + listener
      - [EventTarget](https://github.com/HowProgrammingWorks/Events) для Web API: EventTarget + Event (CustomEvent) + listener
      - [Signal](https://github.com/HowProgrammingWorks/Signals)
    - [Состояние (State)](https://github.com/HowProgrammingWorks/State) — реализация конечного автомата (Automaton или FSM), где методы - это переходы, а состояние добавляется через композицию и меняется на переходах.
    - [Стратегия (Strategy)](https://github.com/HowProgrammingWorks/Strategy) — выбор взаимозаменяемого поведения в рантайме, через коллекцию реализаций: функций, объектов, классов.
    - [Шаблонный метод (Template method)](https://github.com/HowProgrammingWorks/TemplateMethod) — фиксирует шаги алгоритма, позволяя подклассам переопределять отдельные шаги, и использовать шаги предка как дефолтное поведение.
    - [Посетитель (Visitor)](https://github.com/HowProgrammingWorks/Visitor) — позволяет добавлять операции к объектам без изменения их классов, разделяя структуру и поведение, на несколько абстракций.
    - [Открытый конструктор (Revealing Constructor)](https://github.com/HowProgrammingWorks/RevealingConstructor) - изменение поведения без наследования, внедрение поведения в конструктор в виде функции или объекта, содержащего поведение и его описание.
- 🧩 Шаблоны (патерны или принципы) GRASP
  - 📢 Вводная лекция
    - [Общий обзор GRASP](https://youtu.be/ExauFjYV_lQ)
    - Часть 1 - [GRASP для Node.js и Javascript](https://youtu.be/vm8p4jIQwp4)
    - Часть 2 - скоро
  - [Информационный эксперт (Information expert)](https://youtu.be/cCHL329_As0)
  - Создатель (Creator)
  - Контроллер (Controller)
  - [Ненаправленность (Indirection)](https://youtu.be/IGXdPOZ3Fyk)
  - [Низкое зацепление (Low coupling)](https://youtu.be/IGXdPOZ3Fyk)
  - Высокая связность (High cohesion)
  - Полиморфизм (Polymorphism)
  - Защищенные вариации (Protected variations)
  - [Чистая выдумка (Pure fabrication)](https://youtu.be/CV577a0RHBM)
  - [Примеры кода](https://youtu.be/4AMVQ2-2DcM)
- 🧩 Шаблоны (патерны или принципы) SOLID
  - 📢 Вводная лекция: [SOLID for Node.js and Javascript](https://youtu.be/B2guSV8EMn0)
  - [SOLID вопросы на интервью](https://youtu.be/-9OM6-6pZw8)
  - [Принцип единственной ответственности (Single responsibility principle)](https://youtu.be/o4bQywkBKOI)
  - [Принцип открытости/закрытости (Open/closed principle)](https://github.com/HowProgrammingWorks/OpenClosed)
  - [Принцип подстановки Лисков (Liskov substitution principle)](https://youtu.be/RbhYxygxroc)
  - [Принцип разделения интерфейса (Interface segregation principle)](https://github.com/HowProgrammingWorks/InterfaceSegregation)
  - [Принцип инверсии зависимостей (Dependency inversion principle)](https://github.com/HowProgrammingWorks/DependencyInversion)
