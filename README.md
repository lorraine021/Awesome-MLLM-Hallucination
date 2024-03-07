# Awesome MLLM Hallucination[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
This repository collects research on the hallucination problem of the Multimodal Large Language Model(MLLM), including their papers and codes/datasets.  

✈️
The main aspects involved are **Surveys**, **Benchmarks**, **Hallucination Mitigation methods** and some interesting papers that are not directly related to the current topic. Since some of the papers are relatively new and cannot be sure whether they have been included in the specific conferences, they are currently only marked according to the conference acceptance status of the articles that Google Scholar can find.  

Besides, we have extracted the name or the core solution's category of each paper for you to read in a targeted manner.

If you find some interesting papers not included, please feel free to contact me. We will continue to update this repository! :sunny:

:large_blue_diamond: citation >= 20 &emsp; | &emsp; :star: citation >= 50 &emsp; | &emsp; :fire: citation >= 100

## Contents  
- [Surveys](#Surveys)
-  [Benchmarks](#Benchmarks)
-  [Hallucination Mitigation methods](#Hallucination-Mitigation-methods)
-  [Other](#Other)
   
## Papers
### Surveys
| **Number** | **Title** | **Conference** | **Paper** | **Repo** | **Citation** |
|:--------:|:--------:|:---------:|:---------:|:---------:|:---------:|
|1| A Survey on Hallucination in Large Vision-Language Models| :heavy_minus_sign: |  [![arXiv](https://img.shields.io/badge/arXiv-2402.00253-b31b1b.svg)](https://arxiv.org/pdf/2402.00253.pdf) | :heavy_minus_sign: | :heavy_minus_sign: |
|2| A Survey of Hallucination in “Large” Foundation Models| :heavy_minus_sign: | [![arXiv](https://img.shields.io/badge/arXiv-2309.05922-b31b1b.svg)](https://arxiv.org/pdf/2309.05922.pdf) | :heavy_minus_sign: | :star:|

### Benchmarks
Here are some works that could evaluate the hallucination performances of MLLMs, including some popular benchmarks. Most work products fine-tuning using their benchmark dataset, which could reduce the likelihood of hallucinating without sacrificing its performance on other benchmarks. And some papers have designed clever ways to construct such datasets.
| **Number** | **Title** | **Conference(Date)** | **Paper** | **Repo** | **Citation** | **Benchmark Name** |
|:--------:|:--------:|:---------:|:---------:|:---------:|:---------:|:---------:|
|1|MME: A Comprehensive Evaluation Benchmark for Multimodal Large Language Models| :heavy_minus_sign: |[![arXiv](https://img.shields.io/badge/arXiv-2306.13394-b31b1b.svg)](https://arxiv.org/pdf/2306.13394.pdf) |[![GitHub Page](https://img.shields.io/badge/GitHub-Code-7395C5.svg)](https://github.com/BradyFU/Awesome-Multimodal-Large-Language-Models/tree/Evaluation)|:fire: | MME |
|2|Evaluating Object Hallucination in Large Vision-Language Models|EMNLP(2023)|[![arXiv](https://img.shields.io/badge/arXiv-2305.10355-b31b1b.svg)](https://arxiv.org/pdf/2305.10355.pdf) | :heavy_minus_sign: | :fire: | POPE |
|3|HALLUSIONBENCH: An Advanced Diagnostic Suite for Entangled Language Hallucination & Visual Illusion in Large Vision-Language Models|:heavy_minus_sign: |[![arXiv](https://img.shields.io/badge/arXiv-2310.14566-b31b1b.svg)](https://arxiv.org/pdf/2310.14566.pdf) | [![Google Drive](https://img.shields.io/badge/Google-Drive-7395C5.svg)](https://drive.google.com/drive/folders/1C_IA5rx_Hm67TYpdNf3TL5VlM30TLGRQ) | :heavy_minus_sign: | HALLUSIONBENCH |
|4|Aligning Large Multimodal Models with Factually Augmented RLHF|:heavy_minus_sign: |[![arXiv](https://img.shields.io/badge/arXiv-2309.14525-b31b1b.svg)](https://arxiv.org/pdf/2309.14525.pdf) |[![GitHub Page](https://img.shields.io/badge/GitHub-Code-7395C5.svg)](https://llava-rlhf.github.io.)|:large_blue_diamond: | MMHAL-BENCH |
|5|Evaluation and Analysis of Hallucination in Large Vision-Language Models| :heavy_minus_sign: |[![arXiv](https://img.shields.io/badge/arXiv-2308.15126-b31b1b.svg)](https://arxiv.org/pdf/2308.15126.pdf) |[![GitHub Page](https://img.shields.io/badge/GitHub-Code-7395C5.svg)](https://github.com/junyangwang0410/HaELM)|:large_blue_diamond: | HaELM |
|6|AMBER: An LLM-free Multi-dimensional Benchmark for MLLMs Hallucination Evaluation| :heavy_minus_sign: |[![arXiv](https://img.shields.io/badge/arXiv-2311.07397v2-b31b1b.svg)](https://arxiv.org/pdf/2311.07397v2.pdf) |[![GitHub Page](https://img.shields.io/badge/GitHub-Code-7395C5.svg)](https://github.com/junyangwang0410/AMBER)|:heavy_minus_sign:| AMBER |
|7|Negative object presence evaluation (nope) to measure object hallucination in vision-language models | :heavy_minus_sign: |[![arXiv](https://img.shields.io/badge/arXiv-2310.05338-b31b1b.svg)](https://arxiv.org/pdf/2310.05338.pdf) |:heavy_minus_sign:|:heavy_minus_sign:| NOPE |
|8|Ciem: Contrastive instruction evaluation method for better instruction tuning| NeurIPS(2023) Workshop|[![arXiv](https://img.shields.io/badge/arXiv-2309.02301-b31b1b.svg)](https://arxiv.org/pdf/2309.02301.pdf) |:heavy_minus_sign:|:heavy_minus_sign:| Ciem|
|9|Faithscore: Evaluating hallucinations in large vision-language models| :heavy_minus_sign: |[![arXiv](https://img.shields.io/badge/arXiv-2311.01477-b31b1b.svg)](https://arxiv.org/pdf/2311.01477.pdf) |[![GitHub Page](https://img.shields.io/badge/GitHub-Code-7395C5.svg)](https://github.com/bcdnlp/FAITHSCORE)|:heavy_minus_sign:| Faithscore(metric) |
|10|Mitigating hallucination in large multimodal models via robust instruction tuning|ICLR(2024)|[![arXiv](https://img.shields.io/badge/openreview-net-b31b1b.svg)](https://openreview.net/pdf?id=J44HfH4JCg) |:heavy_minus_sign:|:large_blue_diamond:| GAVIE|
|11|Mitigating Fine-Grained Hallucination by Fine-Tuning Large Vision-Language Models with Caption Rewrites| MMM(2024) |[![arXiv](https://img.shields.io/badge/arXiv-2312.01701v1-b31b1b.svg)](https://arxiv.org/pdf/2312.01701v1.pdf) |[![GitHub Page](https://img.shields.io/badge/GitHub-Code-7395C5.svg)](https://github.com/bcdnlp/FAITHSCORE)|:heavy_minus_sign:| FGHE/FOHE(An upgraded version of POPE) |
|12|Visual Hallucinations of Multi-modal Large Language Models|:heavy_minus_sign:|[![arXiv](https://img.shields.io/badge/arXiv-2402.14683-b31b1b.svg)](https://arxiv.org/pdf/2402.14683.pdf) |[![GitHub Page](https://img.shields.io/badge/GitHub-Code-7395C5.svg)](https://github.com/wenhuang2000/VHTest)|:heavy_minus_sign:| two benchmarks generated by VHTest |
|13|Eyes wide shut? exploring the visual shortcomings of multimodal llms|:heavy_minus_sign:|[![arXiv](https://img.shields.io/badge/arXiv-2401.06209-b31b1b.svg)](https://arxiv.org/pdf/2401.06209.pdf) |:heavy_minus_sign:|:heavy_minus_sign:| MMVP|
|14|Evaluation and Enhancement of Semantic Grounding in Large Vision-Language Models|AAAI-ReLM Workshop(2024)|[![arXiv](https://img.shields.io/badge/arXiv-2309.04041-b31b1b.svg)](https://arxiv.org/pdf/2309.04041.pdf) |:heavy_minus_sign:|:heavy_minus_sign:| MSG-MCQ| 
|15|Detecting and Preventing Hallucinations in Large Vision Language Models|AAAI(2024)|[![arXiv](https://img.shields.io/badge/arXiv-2308.06394-b31b1b.svg)](https://arxiv.org/pdf/2308.06394.pdf) |[![GitHub Page](https://img.shields.io/badge/GitHub-Code-7395C5.svg)](https://github.com/hendryx-scale/mhal-detect)|:large_blue_diamond:| M-HalDetect|




### Hallucination Mitigation methods 
Here are some labels that represent the core points of the papers, corresponding to mitigation methods from different angles, you could read the surveys mentioned earlier to further understand these categories:  
 __`data.`__: data improvement (most benchmarks) &emsp; | &emsp; __`vis.`__: vision enhancement &emsp; | &emsp;
__`align.`__: multimodal alignment &emsp; | &emsp;
__`dec.`__: decoding optimization &emsp; | &emsp; __`post.`__: post-process &emsp; | &emsp; __`else.`__: other kinds

| **Number** | **Title** | **Conference(Date)** | **Paper** | **Repo** | **Citation** | **Core** |
|:--------:|:--------:|:---------:|:---------:|:---------:|:---------:|:---------:|
|1|Enhancing the Spatial Awareness Capability of Multi-Modal Large Language Model|:heavy_minus_sign:|[![arXiv](https://img.shields.io/badge/arXiv-2310.20357-b31b1b.svg)](https://arxiv.org/pdf/2310.20357.pdf) |:heavy_minus_sign:|:heavy_minus_sign:|__`vis.`__|
|2|Hallucination Augmented Contrastive Learning for Multimodal Large Language Model|:heavy_minus_sign:|[![arXiv](https://img.shields.io/badge/arXiv-2312.06968v3-b31b1b.svg)](https://arxiv.org/pdf/2312.06968v3.pdf) |[![GitHub Page](https://img.shields.io/badge/GitHub-Code-7395C5.svg)](https://github.com/X-PLUG/mPLUG-HalOwl/tree/main/hacl)|:heavy_minus_sign:| __`align.`__|
|3|Position-Enhanced Visual Instruction Tuning for Multimodal Large Language Models|:heavy_minus_sign:|[![arXiv](https://img.shields.io/badge/arXiv-2308.13437-b31b1b.svg)](https://arxiv.org/pdf/2308.13437.pdf) |[![GitHub Page](https://img.shields.io/badge/GitHub-Code-7395C5.svg)](https://github.com/PVIT-official/PVI)|:large_blue_diamond:| __`vis.`__ __`align.`__|
|4|VCoder: Versatile Vision Encoders for Multimodal Large Language Models|CVPR(2024)|[![arXiv](https://img.shields.io/badge/arXiv-2312.14233-b31b1b.svg)](https://arxiv.org/pdf/2312.14233.pdf) |[![GitHub Page](https://img.shields.io/badge/GitHub-Code-7395C5.svg)](https://github.com/SHI-Labs/VCoder)|:heavy_minus_sign:| __`vis.`__ |
|5|Seeing is believing mitigating hallucination in large vision-language models via clip-guided decoding|:heavy_minus_sign:|[![arXiv](https://img.shields.io/badge/arXiv-2402.15300v1-b31b1b.svg)](https://arxiv.org/pdf/2402.15300v1.pdf) |:heavy_minus_sign:|:heavy_minus_sign:|__`dec.`__|
|6|OPERA: Alleviating Hallucination in Multi-Modal Large Language Models via Over-Trust Penalty and Retrospection-Allocation|CVPR(2024)|[![arXiv](https://img.shields.io/badge/arXiv-2311.17911-b31b1b.svg)](https://arxiv.org/pdf/2311.17911.pdf) |[![GitHub Page](https://img.shields.io/badge/GitHub-Code-7395C5.svg)](https://github.com/shikiw/OPERA)|:heavy_minus_sign:| __`dec.`__ |
|7|Mitigating Object Hallucinations in Large Vision-Language Models through Visual Contrastive Decoding|:heavy_minus_sign:|[![arXiv](https://img.shields.io/badge/arXiv-2311.16922-b31b1b.svg)](https://arxiv.org/pdf/2311.16922.pdf) |[![GitHub Page](https://img.shields.io/badge/GitHub-Code-7395C5.svg)](https://github.com/DAMO-NLP-SG/VCD)|:heavy_minus_sign:| __`dec.`__ |
|8|HALC: Object Hallucination Reduction via Adaptive Focal-Contrast Decoding|:heavy_minus_sign:|[![arXiv](https://img.shields.io/badge/arXiv-2403.00425-b31b1b.svg)](https://arxiv.org/pdf/2403.00425.pdf) |[![GitHub Page](https://img.shields.io/badge/GitHub-Code-7395C5.svg)](https://github.com/BillChan226/HALC)|:heavy_minus_sign:| __`dec.`__ |
|9|Woodpecker: Hallucination Correction for Multimodal Large Language Models|:heavy_minus_sign:|[![arXiv](https://img.shields.io/badge/arXiv-2310.16045-b31b1b.svg)](https://arxiv.org/pdf/2310.16045.pdf) |[![GitHub Page](https://img.shields.io/badge/GitHub-Code-7395C5.svg)](https://github.com/BradyFU/Woodpecker)|:large_blue_diamond:| __`post.`__ |
|10|Analyzing and mitigating object hallucination in large vision-language models **(LURE)**|:heavy_minus_sign:|[![arXiv](https://img.shields.io/badge/arXiv-2310.00754-b31b1b.svg)](https://arxiv.org/pdf/2310.00754.pdf) |[![GitHub Page](https://img.shields.io/badge/GitHub-Code-7395C5.svg)](https://github.com/YiyangZhou/LURE)|:large_blue_diamond:| __`post.`__ |
|11|VIGC: Visual Instruction Generation and Correction|:heavy_minus_sign:|[![arXiv](https://img.shields.io/badge/arXiv-2308.12714-b31b1b.svg)](https://arxiv.org/pdf/2308.12714.pdf) |[![GitHub Page](https://img.shields.io/badge/GitHub-opendatalab-7395C5.svg)](https://opendatalab.github.io/VIGC/)|:large_blue_diamond:| __`other.`__    (Iterative Generation)|
|12|Can We Edit Multimodal Large Language Models?|EMNLP(2023)|[![arXiv](https://img.shields.io/badge/arXiv-2310.08475-b31b1b.svg)](https://arxiv.org/pdf/2310.08475.pdf) |[![GitHub Page](https://img.shields.io/badge/GitHub-code-7395C5.svg)](https://github.com/zjunlp/EasyEdit)|:heavy_minus_sign:| __`other.`__    (Model Edition)|
|13|HALO:Estimation and Reduction of Hallucinations in Open-Source Weak Large Language Models|:heavy_minus_sign:|[![arXiv](https://img.shields.io/badge/arXiv-2308.11764-b31b1b.svg)](https://arxiv.org/pdf/2308.11764.pdf) |[![GitHub Page](https://img.shields.io/badge/GitHub-code-7395C5.svg)](https://github.com/EngSalem/HaLo)|:heavy_minus_sign:| __`other.`__    (knowledge Injection and Teacher-Student Approaches)|



### Other
Here are some papers that are not directly related to MLLM hallucinations, but may have unexpected inspiration for you.
| **Number** | **Title** | **Conference(Date)** | **Paper** | **Repo** | **Citation** |
|:--------:|:--------:|:---------:|:---------:|:---------:|:---------:|
|1|Hallucination improves the performance of unsupervised visual representation learning|ICCV(2023)|[![arXiv](https://img.shields.io/badge/arXiv-2307.12168-b31b1b.svg)](https://arxiv.org/pdf/2307.12168.pdf) |:heavy_minus_sign:|:heavy_minus_sign:|
|2|Multi-Grained Vision Language Pre-Training: Aligning Texts with Visual Concepts|ICML(2022)|[![arXiv](https://img.shields.io/badge/arXiv-2111.08276-b31b1b.svg)](https://arxiv.org/pdf/2111.08276.pdf) |[![GitHub Page](https://img.shields.io/badge/GitHub-Code-7395C5.svg)](https://github.com/zengyan-97/X-VLM)|:fire:|
|3|Overcoming Language Priors in Visual Question Answering via Distinguishing Superficially Similar Instances|COLING(2022)|[![arXiv](https://img.shields.io/badge/arXiv-2209.08529-b31b1b.svg)](https://arxiv.org/pdf/2209.08529.pdf) |[![GitHub Page](https://img.shields.io/badge/GitHub-Code-7395C5.svg)](https://github.com/wyk-nku/Distinguishing-VQA)|:heavy_minus_sign:|

 
