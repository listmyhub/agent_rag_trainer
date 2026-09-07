# agent：通用 Agent 能力

## 模块

- `my_llm.py`：统一初始化多个模型提供商。
- `load.py`：读取环境变量和 API Key。
- `my_memory/`：SQLite / MySQL 检查点与记忆实验。
- `tools/`：Tavily 搜索、SQL 工具和自定义工具定义示例。
- `sqr/`：数据库访问和日志封装。
- `resource/`：资源包目录。

## 入口示例

- `my_agent1.py`：基础 Agent。
- `ai私厨管家助手.py`：带记忆和搜索工具的助手示例。
- `mysql_agent.py`：数据库 Agent 示例。
- `llm_test.py`：模型调用测试。


