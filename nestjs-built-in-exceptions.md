[NestJS 内置异常](https://dev.to/wakeup_flower_8591a6cb6a9/nestjs-built-in-exceptions-4ad1)

### Abstract
本文系统总结了 NestJS 内置异常的类型、对应的状态码与描述，并给出自定义异常的实现示例，强调通过扩展 HttpException 类来实现自定义错误信息与状态码的灵活处理。

### Key Points
- NestJS 提供了多种内置异常类，每个异常对应一个 HTTP 状态码与描述。  
- 示例展示了如何抛出一个 ConflictException，表示请求中存在冲突，如邮箱已被使用。  
- 文中列出并对照了常见的内置异常及其状态码（如 BadRequest 400、NotFound 404、Unauthorized 401 等）。  
- 还提供了如何创建自定义异常的代码示例，通常通过扩展 HttpException 实现。  
- 自定义异常可以在构造函数中设置自定义的状态码、消息和错误字段，以便前端更精准地处理。  
- 还给出了 HttpStatus 枚举的完整列表，便于在代码中使用统一的状态码常量。  
- 除了内置异常，还介绍了如何在控制器中通过抛出自定义异常来响应客户端请求错误。  
- 文中对一些特定场景（如 422、500、501、502 等）也给出了对应的描述，帮助开发者快速查阅。

### Related Questions
- [如何在 NestJS 中选择合适的内置异常来表达错误语义？](#related)  
- [自定义异常与全局过滤器/拦截器如何协同工作以统一错误响应？](#related)  
- [是否有最佳实践来组织和复用自定义异常及错误消息模板？](#related)
