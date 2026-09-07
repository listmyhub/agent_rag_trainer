# RAG开发应用项目_Agent

该目录将健康档案 RAG 流程封装为 Agent：

- `health_agent.py`：定义 LangGraph Agent 入口 `agent`。
- `tools.py`：把健康问答能力注册为 Agent 工具。

根目录 `langgraph.json` 当前指向 `health_agent.py:agent`。
