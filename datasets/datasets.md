# Datasets

This section contains datasets relevant to citation verification, hallucination detection, retrieval-augmented generation (RAG), and evaluation of evidence-grounded large language model outputs.

## 1. SciCiteVal

- **Source:** Qinyue Liu, Yongxin Zhou, and Cyril Labbe
- **Year:** 2026
- **Dataset Type:** Scientific citation verification
- **Description:** SciCiteVal is a manually annotated dataset designed for automated scientific citation verification. Each instance pairs a citation context from a citing paper with an evidence passage from the cited source. Citations are labeled as Correct, Incorrect, or Unrelated, with Incorrect citations further divided into fine-grained error categories.
- **Size:** 1,034 annotated citations
- **Application:** Training and evaluating systems that determine whether a scientific citation actually supports the claim or citation context in which it appears.
- **Official paper:** https://aclanthology.org/2026.lrec-1.125/
- **Dataset access:** https://huggingface.co/datasets/birdie0111/SciCiteVal
- **Why it is relevant:** This is directly aligned with the research topic because it evaluates whether cited scientific evidence actually supports the citation context.

## 2. RAGTruth

- **Source:** Cheng Niu, Yuanhao Wu, Juno Zhu, Siliang Xu, KaShun Shum, Randy Zhong, Juntong Song, and Tong Zhang
- **Year:** 2024
- **Dataset Type:** Retrieval-augmented generation hallucination corpus
- **Description:** RAGTruth is a human-annotated corpus for studying hallucinations in retrieval-augmented generation systems. It contains naturally generated responses from multiple language models together with source information and word-level hallucination annotations.
- **Size:** Nearly 18,000 generated responses from approximately 2,965 source instances
- **Application:** Training and evaluating hallucination detection systems for RAG, analyzing unsupported claims, and studying hallucination patterns across language models and tasks.
- **Official paper:** https://aclanthology.org/2024.acl-long.585/
- **Dataset access:** https://github.com/ParticleMedia/RAGTruth
- **Why it is relevant:** Agentic search and retrieval-augmented systems can produce citations or claims that are not supported by retrieved evidence; RAGTruth provides data for evaluating this problem.

## 3. HaluEval

- **Source:** Junyi Li, Xiaoxue Cheng, Xin Zhao, Jian-Yun Nie, and Ji-Rong Wen
- **Year:** 2023
- **Dataset Type:** Large-scale LLM hallucination evaluation benchmark
- **Description:** HaluEval is a large benchmark containing generated and human-annotated hallucinated and non-hallucinated samples. It covers general user queries, question answering, knowledge-grounded dialogue, and text summarization.
- **Size:** 35,000 samples
- **Application:** Evaluating the ability of language models to recognize hallucinated content and studying the types of information that LLMs tend to fabricate or fail to verify.
- **Official paper:** https://aclanthology.org/2023.emnlp-main.397/
- **Dataset access:** https://github.com/RUCAIBox/HaluEval
- **Why it is relevant:** Citation fabrication is one manifestation of a broader hallucination problem, so HaluEval provides a useful general benchmark for evaluating hallucination detection.

## Dataset Selection Rationale

These three datasets were selected because they cover complementary levels of the research problem:

- **SciCiteVal:** Directly evaluates scientific citation correctness and citation-to-evidence alignment.
- **RAGTruth:** Evaluates hallucinations in retrieval-augmented generation and source-grounded responses.
- **HaluEval:** Provides a broader benchmark for hallucination recognition across different LLM tasks.

Together, they provide a useful progression from general hallucination detection to retrieval-grounded evaluation and finally to direct scientific citation verification.
