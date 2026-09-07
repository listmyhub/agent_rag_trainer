# simply_agent_train

这是一个基于 LangChain / LangGraph 的多项目学习与实验仓库，集中整理了 Agent、RAG、工具调用、结构化输出和流式输出等示例。

> 本次整理遵循“代码逻辑不改”的原则：未修改任何 Python 源代码、导入路径或运行配置；保留了原有源码中的历史注释。新增内容以 README 和结构说明文档为主。

## 项目导航

| 目录 | 内容 | 建议入口 |
| --- | --- | --- |
| [`src/agent`](src/agent/readme.md) | Agent、LLM、记忆、MySQL 与搜索工具实验 | `my_agent1.py`、`mysql_agent.py` |
| [`src/RAG开发应用项目`](src/RAG开发应用项目/readme.md) | 面向健康档案 PDF 的传统 RAG 流程 | `main.py` |
| [`src/RAG开发应用项目_Agent`](src/RAG开发应用项目_Agent/readme.md) | 将健康档案 RAG 封装为 Agent 工具 | `health_agent.py` |
| [`src/RAG知识库`](src/RAG知识库/readme.md) | 文本切分与检索优化实验 | 各分块/检索脚本 |
| `src/流式输出.py`、`src/结构化输出*.py` | 独立学习示例 | 直接运行文件 |

## 环境准备

- Python `>=3.10`
- 创建虚拟环境：`python -m venv .venv`
- 安装依赖：`pip install -r requirements.txt`
- 在根目录配置 `.env`；变量名以现有 `load.py`、`config.py` 文件为准。

## 运行说明

建议从仓库根目录运行。LangGraph 入口由 `langgraph.json` 指向 `src/RAG开发应用项目_Agent/health_agent.py:agent`。

```bash
python src/流式输出.py
python src/结构化输出1.py
python src/RAG开发应用项目/main.py
```

## 整理

1. `src/agent`：通用 Agent 基础能力与外部工具。
2. `src/RAG开发应用项目`：完整的 PDF → 切分 → 向量库 → 检索 → 问答流程。
3. `src/RAG开发应用项目_Agent`：RAG 能力的 Agent 化封装。
4. `src/RAG知识库`：独立知识库实验，保留原始中文文件名。
5. `.langgraph_api`：运行时生成的检查点/向量数据目录，不建议手工编辑。

## 注意事项

- 本次没有移动源码，因为现有导入语句依赖中文包目录和 `agent` 包路径。
- API Key、数据库连接信息和本地路径应放在 `.env` 或个人配置中，不要提交到版本库。
- `requirements.txt` 保留原有环境导出内容，后续可单独拆分运行时依赖和开发依赖。
