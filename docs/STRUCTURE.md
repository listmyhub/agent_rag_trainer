# 仓库结构说明

## 当前分层

- `.langgraph_api/`：LangGraph 运行时产物。
- `docs/`：仓库级说明文档。
- `src/agent/`：通用 Agent、LLM、工具、记忆、数据库和日志实验。
- `src/RAG开发应用项目/`：健康档案 PDF 的传统 RAG 主流程。
- `src/RAG开发应用项目_Agent/`：RAG Agent 封装。
- `src/RAG知识库/`：文档切分、向量化和检索优化实验。
- `src/*.py`：独立学习示例。

## 依赖方向

- `RAG开发应用项目_Agent` 依赖 `RAG开发应用项目`，并复用 `agent.my_llm`。
- `agent` 提供模型、环境变量、工具、记忆和数据库能力。
- `RAG知识库` 是相对独立的实验区，部分脚本复用 `agent.my_llm`。


