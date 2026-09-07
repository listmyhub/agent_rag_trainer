# RAG开发应用项目

这是一个面向健康档案 PDF 的传统 RAG 流程：

1. `data_processor.py` 加载 PDF 并切分文本。
2. `vector_store.py` 生成向量并写入 Chroma。
3. `retriever.py` 组合向量检索和 BM25 等检索策略。
4. `qa_engine.py` 调用模型生成答案。
5. `main.py` 串联完整流程。

配置集中在 `config.py`，输入文件位于 `input/`。保持中文目录名是为了兼容现有导入。
