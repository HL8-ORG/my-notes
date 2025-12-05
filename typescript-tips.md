### Abstract
本文综合介绍了 Typescript 的若干高级用法与思维方式，强调通过集合论思维理解类型、利用自动缩小、区分联合类型、使用类型谓词与断言、控制推断行为、以及在实际编码中偏好类型（type）而非接口（interface）、使用元组、以及 infer 等特性，以提升对语言潜力的把握。

### Key Points
- 使用 Set 作为理解类型的概念模型，帮助理解类型之间的交集、并集以及可分配性。  
- 自动类型缩小基于控制流，使同一变量在不同位置具有声明类型和缩小后的类型两种类型信息。  
- 使用可区分联合（discriminated union）替代可选字段，避免大量非空断言，提升类型可预测性。  
- 通过类型谓词来精确缩小类型，避免与显式类型断言相关的常见问题。  
- 控制联合类型的分布行为，了解分布式条件类型，并可通过特定语法改变分布方式。  
- 详尽检查未处理分支，利用 never 类型在编译期捕获遗漏的情况。  
- 优先使用 type 而非 interface，除非需要接口的合并特性或面向对象风格的场景。  
- 在适当情况下偏好元组而非数组，以提高类型的严格性与可预测性。  
- 通过 const、satisfies 等手段控制推断的具体性与检查类型的准确性。  
- 使用 infer 在泛型中提取和创建额外的类型参数，提升类型表达能力。  
- 通过创造性地进行类型操作（如 Pick、ReturnType、模板字面量等）实现 DRY，并推断出更智能的工厂与类型结构。  

### Related Questions
- [What are practical examples of using discriminated unions in complex TypeScript code?](#related)
- [How can I decide when to use type vs interface in a large codebase?](#related)
- [What are common pitfalls when applying advanced TypeScript techniques in libraries?](#related)
