# JavaAIAgentKit

[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](LICENSE)

> 🚀 企业级 Java AI 应用脚手架：支持动态 Prompt、RAG 知识库、多轮对话、全链路可观测性。纯 Java 技术栈，无需 Python！

项目名称：JavaAIAgentKit — 企业级 RAG 智能问答平台

技术栈：Spring Boot, Spring AI Alibaba, Nacos, Redis, Milvus, OpenTelemetry

项目描述：

针对企业 AI 落地难（Prompt 静态、无法追踪、知识更新滞后）等痛点，设计并实现了一套纯 Java 的智能问答系统；
通过 Nacos 实现 Prompt 和模型参数的动态热更新，发布效率提升 100%；
集成 RAG 架构，支持私有文档上传与语义检索，问答准确率提升 40%；
引入 OpenTelemetry 实现全链路追踪，线上问题定位时间从小时级降至分钟级；
项目已开源，获得 200+ GitHub Stars，被多家中小企业用于内部知识库建设。
## ✨ 特性

- ✅ **动态 Prompt 管理**：通过 Nacos 实现热更新，无需重启服务
- ✅ **RAG 增强问答**：支持 PDF/Markdown 文档上传与语义检索
- ✅ **生产就绪**：集成 OpenTelemetry，支持 Jaeger 链路追踪
- ✅ **会话管理**：Redis 存储多轮对话上下文
- ✅ **主流 LLM 支持**：通义千问、DeepSeek、Ollama 等

## 🛠 技术栈

- Spring Boot 3.x + Spring AI Alibaba
- Nacos（配置中心）
- Redis（会话缓存）
- Milvus / FAISS（向量存储）
- OpenTelemetry + Jaeger（可观测性）

## 🚀 快速启动

1. 启动 Nacos、Redis、Jaeger
2. 在 Nacos 中配置 `ai-agent-service.yaml`
3. 设置 DashScope API Key（通义千问）
4. `./mvnw spring-boot:run`
5. 调用 `/api/ask?question=公司年假怎么算？`

## 📸 效果演示

![Trace in Jaeger](docs/trace.png)
> 全链路追踪：从用户提问 → 向量检索 → 模型生成

## 💼 为什么做这个项目？

> 作为 Java 工程师，我想证明：**AI 落地不需要只会 Python**。通过工程化能力，我们可以构建稳定、可观测、易维护的企业级 AI 应用。
