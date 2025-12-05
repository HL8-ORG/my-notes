## ValidationPipe
[文章](https://open.forem.com/italoqueiroz/nestjs-validationpipe-ensuring-secure-input-contracts-3dng)

### Abstract
本文介绍了 NestJS 的 ValidationPipe 如何通过与验证装饰器协同工作，自动对输入数据进行格式和类型的验证与变换，从而建立稳健的输入契约。通过配置 transform、whitelist、forbidNonWhitelisted 等选项，可以实现自动类型转换、移除未声明属性以及在检测到非法数据时返回错误，从而提升安全性、数据一致性和开发体验。

### Key Points
- ValidationPipe 是一个全局管道，基于装饰器元数据进行输入数据的自动验证与转换。  
- transform: true 能将输入数据自动转换为对应 DTO 的实例，提升类型安全与基于类的验证。  
- whitelist: true 会自动删除 DTO 未声明的属性，增强数据清理和安全性。  
- forbidNonWhitelisted: true 在遇到非被允许的属性时返回 HTTP 400，提供即时反馈并提升安全性。  
- 通过 DTO 进行集中验证，减少手动验证代码，提升可维护性。  
- 全局配置示例展示：在 main.ts 使用 ValidationPipe 并启用 transform、whitelist、forbidNonWhitelisted。  
- 结合实际 DTO 与控制器的实现，确保输入数据在进入业务逻辑前已被验证和类型化。  
- 条件验证和自定义验证等高级用例可进一步增强输入契约的灵活性与强制性。  
- 结论强调将这些配置作为基础实践，有助于构建安全、可维护且可靠的 API。

### Related Questions
- [如何在现有项目中无缝引入 ValidationPipe 以最小化对现有代码的影响？](#related)  
- [ValidationPipe 的性能开销在高并发场景下是否显著，如何优化？](#related)  
- [除了 class-validator 和 class-transformer，还有哪些替代方案或自定义验证策略可与 ValidationPipe 结合使用？](#related)
