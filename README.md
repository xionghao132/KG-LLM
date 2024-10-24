# KG-LLM

## 📄 Paper List

* KG for LLM

 Knowledge Graph Enhanced Large Language Model Editing   [ Paper](https://arxiv.org/abs/2402.13593)

InfuserKI: Enhancing Large Language Models with Knowledge Graphs via Infuser-Guided Knowledge Integration [paper](https://arxiv.org/abs/2402.11441)

Knowledge Graph-Enhanced Large Language Models via Path Selection [paper](https://arxiv.org/abs/2406.13862)

Learning to Plan for Retrieval-Augmented Large Language Models from Knowledge Graphs [paper](https://arxiv.org/abs/2406.14282)

EMERGE: Integrating RAG for Improved Multimodal EHR Predictive Modeling [ paper](https://arxiv.org/abs/2406.00036)

Mitigating Hallucinations in Large Language Models via Self-Refinement-Enhanced Knowledge Retrieval [paper](https://arxiv.org/abs/2405.06545)

ODA: Observation-Driven Agent for integrating LLMs and Knowledge Graphs [paper](https://arxiv.org/abs/2404.07677)

Logic Query of Thoughts: Guiding Large Language Models to Answer Complex Logic Queries with Knowledge Graphs [paper](https://arxiv.org/abs/2404.04264)

KnowLA: Enhancing Parameter-efficient Finetuning with Knowledgeable Adaptation [ paper](https://arxiv.org/abs/2403.14950)

Automatic Question-Answer Generation for Long-Tail Knowledge  [paper](https://arxiv.org/abs/2403.01382)

Large Language Models Can Better Understand Knowledge Graphs Than We Thought [paper ](https://arxiv.org/abs/2402.11541)

Contri(e)ve: Context + Retrieve for Scholarly Question Answering [paper](https://arxiv.org/abs/2409.09010)

GLaM: Fine-Tuning Large Language Models for Domain Knowledge Graph Alignment via Neighborhood Partitioning and Generative Subgraph Encoding [paper](https://arxiv.org/abs/2402.06764)

Chain-of-Knowledge: Integrating Knowledge Reasoning into Large Language Models by Learning from Knowledge Graphs [paper](https://arxiv.org/abs/2407.00653)

Multimodal Reasoning with Multimodal Knowledge Graph [paper](https://aclanthology.org/2024.acl-long.579/)



| 标题                                                         | 时间    | 方法名称（有就填） | 模型名称（包含大小）                                         | KG名称                                      | 数据集                                                       | 主要思路                                                     | 是否是KG增强LLM | 备注                               | 详情（之后补充） |
| ------------------------------------------------------------ | ------- | ------------------ | ------------------------------------------------------------ | ------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | --------------- | ---------------------------------- | ---------------- |
| [ Knowledge Graph Enhanced Large Language Model Editing](https://arxiv.org/abs/2402.13593) | 2024/02 | GLAME              | GPT-2 XL (1.5B) 、GPT-J (6B)                                 | Wikipedia                                   | COUNTERFACT、COUNTERFACTPLUS                                 | GLAME通过知识图谱增强模块抽取一个高阶子图，记录由于编辑过程导致的知识变化，使用LLM对子图中实体和关系进行编码，最后结合GNN将子图中的新知识关联融入到参数编辑过程中。 | 是              |                                    |                  |
| [InfuserKI: Enhancing Large Language Models with Knowledge Graphs via Infuser-Guided Knowledge Integration](https://arxiv.org/abs/2402.11441) | 2024/02 | InfuserKI          | LLaMa-2- 7B                                                  | UMLS，MetaQA                                | PubMedQA，MetaQA-1HopQA                                      | LLM在特定领域知识的任务表现不佳，InfuserKI通过外部模块将领域特定的知识图谱整合进LLMs，利用Transformer内部状态来判断是否需要对原始LLM输出进行增强，从而有效地减少了知识遗忘的问题 | 是              | 结合KG做知识编辑                   |                  |
| [Knowledge Graph-Enhanced Large Language Models via Path Selection](https://arxiv.org/abs/2406.13862) | 2024/06 | KELP               | gpt-3.5-turbo-0613                                           | MetaQA，DBpedia                             | MetaQA-1HopQA/2-HopQA,FACTKG dataset                         | 在推理阶段，从知识图谱中识别出与输入问题中实体相关的知识路径，从识别出的知识路径中挑选出有价值的知识作为上下文，将选定的知识上下文与原始的输入问题一起送入LLM | 是              |                                    |                  |
| [Learning to Plan for Retrieval-Augmented Large Language Models from Knowledge Graphs](https://arxiv.org/abs/2406.14282) | 2024/06 | LPKG               | CodeQwen1.5-7B-Chat, Llama3-8B-Instruct,GPT-3.5              | Wikidata15k                                 | HotPotQA,2WikiMQA,MuSiQue,Bamboogle                          | 利用从知识图谱中提取的规划数据来增强LLMs的规划能力           | 是              | 利用KG来增强LLM的规划能力          |                  |
| [ EMERGE: Integrating RAG for Improved Multimodal EHR Predictive Modeling](https://arxiv.org/abs/2406.00036) | 2024/06 | EMERGE             | Clinical-LongFormer,BGE-M3,Qwen 1.5-7B Chat,DeepSeek-V2 Chat(236B) | PrimeKG                                     | MIMIC-III、 MIMIC-IV                                         | 使用大型语言模型（LLMs）从时间序列数据和临床笔记中提取实体，并将这些实体与专业知识图谱PrimeKG对齐，基于提取的知识和检索实体关系的相关信息生成患者健康状况的任务相关摘要，最后结合一个交叉注意力的多模态网络。 | 是              | 多模态利用电子健康记录进行临床预测 |                  |
| [Mitigating Hallucinations in Large Language Models via Self-Refinement-Enhanced Knowledge Retrieval](https://arxiv.org/abs/2405.06545) | 2024/05 | Re-KGR             | LLaMA-7b                                                     | CKG,PrimeKG                                 | MedQuAD                                                      | 结合结构化的知识图谱并减少在医疗问答任务中的检索工作量，来有效地减轻LLM响应中的幻觉问题。 | 是              | 结合KG做医疗领域的检索增强         |                  |
| [ODA: Observation-Driven Agent for integrating LLMs and Knowledge Graphs](https://arxiv.org/abs/2404.07677) | 2024/04 | ODA                | GPT4                                                         | Wikidata                                    | QALD10-en, T-REx, Zero-Shot RE,  Creak                       | 结合LLM决策在图谱中检索信息后RAG                             | 是              | LLM做KBQA的                        |                  |
| [Logic Query of Thoughts: Guiding Large Language Models to Answer Complex Logic Queries with Knowledge Graphs](https://arxiv.org/abs/2404.04264) | 2024/04 | LGOT               | Llama-2-7b                                                   | MetaQA, ComplexWebQuestions, GraphQuestions |                                                              | 将复杂逻辑查询分解为易于回答的子问题                         | 是              | LLM做KBQA的                        |                  |
| [ KnowLA: Enhancing Parameter-efficient Finetuning with Knowledgeable Adaptation](https://arxiv.org/abs/2403.14950) | 2024/03 | KnowLA             | Llama 2-7B, Alpaca2-7B                                       | WordNet, ConceptNet, Wikidata               | CommonsenseQA, SIQA, BBH, WebQuestionSP, TriviaQA, TruthfulQA | 插入一层adaptation来整合输入中所包含实体在知识图谱中的表示，提升PEFT后的表现 | 是              | 在LORA的过程中引入KGE              |                  |
| [Automatic Question-Answer Generation for Long-Tail Knowledge](https://arxiv.org/abs/2403.01382) | 2024/03 |                    | GPT3                                                         | wikidata,wikipedia                          | Tail-entity datasets                                         | 使用wikidata生成针对tail entities的问答数据集，并探索了使用KG提高LLMs在long tail知识上的表现 | 是              |                                    |                  |
| [Large Language Models Can Better Understand Knowledge Graphs Than We Thought ](https://arxiv.org/abs/2402.11541) | 2024/02 |                    | ChatGPT, GPT-4o2 , LLaMA33 , Vicuna 7B and 13B               | KGQA，wikidata                              | QALD-7，LC-QuAD 2.0，KQAPro                                  | 研究KG注入LLM的各种输入格式，找出LLM偏好的文本               | 是              |                                    |                  |
| [Contri(e)ve: Context + Retrieve for Scholarly Question Answering](https://arxiv.org/abs/2409.09010) | 2024/09 |                    | Llama 3.1                                                    | DBLP KG, SemOpenAlex KG, Wikipedia text     | scholarly-QALD                                               | 使用混合数据源（包括KG和非结构化文本）来增强LLM的信息检索和问答能力 | 是              |                                    |                  |
| [GLaM: Fine-Tuning Large Language Models for Domain Knowledge Graph Alignment via Neighborhood Partitioning and Generative Subgraph Encoding](https://arxiv.org/abs/2402.06764) | 2024/02 | GLaM               | GLaM,Llama 7B Chat,Llama 13B Chat                            | UMLS                                        | DBLP                                                         | 通过微调将领域特定知识图谱整合到大规模语言模型中             | 是              |                                    |                  |
| [Chain-of-Knowledge: Integrating Knowledge Reasoning into Large Language Models by Learning from Knowledge Graphs](https://arxiv.org/abs/2407.00653) | 2024/07 | CoK                | n Llama3- 8B-instruct,Mistral-7binstruct-v0.2                | Wikidata5m                                  | KNOWREASON                                                   | 提出了CoK，包括数据构建和模型学习方法，以增强LLMs的知识推理能力 | 是              |                                    |                  |
| [Multimodal Reasoning with Multimodal Knowledge Graph](https://aclanthology.org/2024.acl-long.579/) | 2024/08 | MR-MKG             | FLAN-T5 3B,FLAN-T5 11B,FLAN-UL2 19B                          | MMKG,MarKG                                  | ScienceQA,MARS                                               | 使用多模态知识图谱（MMKGs）来增强LLMs的多模态推理能力        | 是              |                                    |                  |