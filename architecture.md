[DDD, CQRS, EDA, ES, Clean, Layer, Hexagonal in one application](https://medium.com/@dykyi.roman/ddd-cqrs-eda-es-clean-layer-hexagonal-in-one-application-d8a0a680351c)

[Mastering NestJS: Building Scalable Systems with Abstractions, ex: different databases](https://medium.com/nestjs-ninja/mastering-nestjs-building-scalable-systems-with-abstractions-ex-different-databases-ea30a02699f9)

[示例](https://github.com/nestjsninja/nestjs-ecommerce)

### Abstract
本文通过 NestJS+Clean Architecture+DDD 的系列探讨抽象的应用，重点展示如何通过将数据库持久化层等外层模块抽象化来实现对数据库和技术栈的解耦，从而构建可扩展、技术无关的系统。以 Mongo 与 Postgres 为示例，说明在不同数据库之间通过抽象接口统一数据访问方式，并强调领域（Domain）在数据流转中的核心作用，以及在 Use Case 层按领域定义构建逻辑与数据处理的流程。

### Key Points
- 抽象用于将不同数据库和外部实现解耦，使内部领域逻辑不依赖具体技术栈。
- 在 Clean Architecture 中，持久化层位于最外层，应该独立于领域和其他内部层。
- 通过定义统一的仓储（Repository）抽象，使用 useClass 指定具体实现，实现数据库无关的数据操作。
- 对数据库实现的示例包括 Mongoose 和 Prisma 模块，它们的提供者结构保持一致，便于替换数据库。
- 域模型（Domain）定义了数据结构与行为，是抽象交互的核心，确保数据转换的一致性与可维护性。
- Use Case 层在执行业务逻辑时，依据域模型进行数据准备与计算（如订单总价计算），并通过仓储接口持久化。
- 抽象化的持久化方案提升模块耦合度的降低与灵活性，便于后续替换和扩展。
- 文章强调 NestJS 抽象能力的强大，是构建结构清晰、易扩展模块的关键工具。

### Related Questions
- [如何在现有 NestJS 项目中逐步引入领域模型与抽象层以实现数据库无关性？](#related)
- [在多数据库场景中，如何设计 Repository 与 Use Case 的交互以保持一致性与性能？](#related)
- [有哪些实用的策略可以在不改变业务逻辑的前提下替换底层数据库实现？](#related)
