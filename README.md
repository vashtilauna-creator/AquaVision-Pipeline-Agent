# AquaVision-Pipeline-Agent# AquaVision-Pipeline: Multi-Agent Underwater Multimodal Data Processing

> 🚀 **Status:** Active Development / Internal Testing

## 📖 项目简介
AquaVision-Pipeline 是一个基于多 Agent 协作架构的水下多模态数据集（RGB-Depth/Sonar）自动化预处理与质量对齐流水线。专为解决水下复杂退化环境（色偏、高浑浊度）下，万级别规模数据集处理过程中的人工干预成本高、深度估计失效拦截难等痛点而设计。

## ✨ 核心特性
- **感知与路由 (Routing Agent):** 动态评估图像退化情况，生成定制化预处理策略。
- **自动化执行 (Execution Agent):** 对接云端 GPU (如 PAI-DSW)，自动化调度基础模型 (如 Depth-Anything-V2) 完成大规模推理任务。
- **VLM 驱动质检 (QA Agent):** 自动化核对多模态空间对齐情况，剔除无效伪深度图。

## 📊 运行状态 (Proof of Work)
- 目前已成功在 USOD10K 与 USIS10K 数据集上完成初步流转。
- 自动化生成并校验了 >10,000 张伪深度图，极大提升了下游双分支分割网络（如 Swin-T + TinyViT 架构）的训练数据准备效率。

## 🛠 技术栈
- **Agents:** LangChain / 自定义 Prompt 编排
- **Vision Models:** Depth-Anything-V2, SAM
- **Framework:** Native PyTorch
