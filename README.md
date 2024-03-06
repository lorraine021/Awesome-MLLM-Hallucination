# Awesome-MLLM-Hallucination
This repository collects research on the hallucination problem of the Multimodal Large Language Model(MLLM), including their papers and codes/datasets.  
The main aspects involved are Surveys, Hallucination Evaluation methods (Benchmarks), Hallucination Mitigation methods and some interesting papers that are not directly related to the current topic. Since some of the papers are relatively new and cannot be sure whether they have been included in the specific conferences, they are currently only marked according to the conference acceptance status of the articles that Google Scholar can find.  
If you find some interesting papers not included, please feel free to contact me. We will continue to update this repository!

Here are some labels that represent the core points of the papers, corresponding to benchmarks or mitigation methods from different angles:   
__`data.`__: data improvement &emsp; | &emsp; __`vis.`__: vision enhancement &emsp; | &emsp;
__`align.`__: multimodal alignment &emsp; | &emsp; __`dec.`__: decoding optimization &emsp; |
__`post.`__: post-process &emsp; | &emsp; __`ben.`__: it creates a benchmark  

:large_blue_diamond: citation >= 20 &emsp; | &emsp; :star: citation >= 50 &emsp; | &emsp; :fire: citation >= 100

## Contents  
1. [Surveys](#Surveys)
2. [Benchmarks](#Benchmarks)
3. [Hallucination Mitigation methods](#Hallucination-Mitigation-methods)
4. [Other](#Other)
   
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
|4|ALIGNING LARGE MULTIMODAL MODELS WITH FACTUALLY AUGMENTED RLHF| :heavy_minus_sign: |[![arXiv](https://img.shields.io/badge/arXiv-2309.14525-b31b1b.svg)](https://arxiv.org/pdf/2309.14525.pdf) |[![GitHub Page](https://img.shields.io/badge/GitHub-Code-7395C5.svg)](https://llava-rlhf.github.io.)|:large_blue_diamond: | MMHAL-BENCH |
|5|Evaluation and Analysis of Hallucination in Large Vision-Language Models| :heavy_minus_sign: |[![arXiv](https://img.shields.io/badge/arXiv-2308.15126-b31b1b.svg)](https://arxiv.org/pdf/2308.15126.pdf) |[![GitHub Page](https://img.shields.io/badge/GitHub-Code-7395C5.svg)](https://github.com/junyangwang0410/HaELM)|:large_blue_diamond: | HaELM |
|6|AMBER: An LLM-free Multi-dimensional Benchmark for MLLMs Hallucination Evaluation| :heavy_minus_sign: |[![arXiv](https://img.shields.io/badge/arXiv-2311.07397v2-b31b1b.svg)](https://arxiv.org/pdf/2311.07397v2.pdf) |[![GitHub Page](https://img.shields.io/badge/GitHub-Code-7395C5.svg)](https://github.com/junyangwang0410/AMBER)|:heavy_minus_sign:| AMBER |
|7|Negative object presence evaluation (nope) to measure object hallucination in vision-language models | :heavy_minus_sign: |[![arXiv](https://img.shields.io/badge/arXiv-2310.05338-b31b1b.svg)](https://arxiv.org/pdf/2310.05338.pdf) |:heavy_minus_sign:|:heavy_minus_sign:| NOPE |
|8|Ciem: Contrastive instruction evaluation method for better instruction tuning| NeurIPS(2023) Workshop|[![arXiv](https://img.shields.io/badge/arXiv-2309.02301-b31b1b.svg)](https://arxiv.org/pdf/2309.02301.pdf) |:heavy_minus_sign:|:heavy_minus_sign:| Ciem|
|9|Faithscore: Evaluating hallucinations in large vision-language models| :heavy_minus_sign: |[![arXiv](https://img.shields.io/badge/arXiv-2311.01477-b31b1b.svg)](https://arxiv.org/pdf/2311.01477.pdf) |[![GitHub Page](https://img.shields.io/badge/GitHub-Code-7395C5.svg)](https://github.com/bcdnlp/FAITHSCORE)|:heavy_minus_sign:| Faithscore(metric) |
|10|MITIGATING HALLUCINATION IN LARGE MULTIMODAL MODELS VIA ROBUST INSTRUCTION TUNING|ICLR(2024)|[![arXiv](https://img.shields.io/badge/openreview-net-b31b1b.svg)](https://openreview.net/pdf?id=J44HfH4JCg) |:heavy_minus_sign:|:large_blue_diamond:| GAVIE|
|11|Mitigating Fine-Grained Hallucination by Fine-Tuning Large Vision-Language Models with Caption Rewrites| MMM(2024) |[![arXiv](https://img.shields.io/badge/arXiv-2312.01701v1-b31b1b.svg)](https://arxiv.org/pdf/2312.01701v1.pdf) |[![GitHub Page](https://img.shields.io/badge/GitHub-Code-7395C5.svg)](https://github.com/bcdnlp/FAITHSCORE)|:heavy_minus_sign:| FGHE/FOHE(An upgraded version of POPE) |
|12|Visual Hallucinations of Multi-modal Large Language Models|:heavy_minus_sign:|[![arXiv](https://img.shields.io/badge/arXiv-2402.14683-b31b1b.svg)](https://arxiv.org/pdf/2402.14683.pdf) |[![GitHub Page](https://img.shields.io/badge/GitHub-Code-7395C5.svg)](https://github.com/wenhuang2000/VHTest)|:heavy_minus_sign:| two benchmarks generated by VHTest |

   


13. [[PDF](https://arxiv.org/pdf/2401.06209.pdf)] Eyes wide shut? exploring the visual shortcomings of multimodal llms, arxiv, 2024, Tong, Shengbang, et al.   [__`ben.`__:MMVP]
14. [[PDF](https://www.cs.emory.edu/~jyang71/files/lvlm-workshop.pdf)] Evaluation and Enhancement of Semantic Grounding in Large Vision-Language Models, AAAI-ReLM Workshop. 2024, Lu, Jiaying, et al.   [__`ben.`__:MSG-MCQ]
15. [[PDF](https://arxiv.org/pdf/2308.06394.pdf)][[Code/Data](https://github.com/hendryx-scale/mhal-detect)] Detecting and Preventing Hallucinations in Large Vision Language Models, AAAI 2024, Gunjal, et al.   [__`ben.`__:M-HalDetect] :large_blue_diamond:
16. [[PDF]()][[Code/Data]()]   [__`ben.`__:]
17. 



### Hallucination Mitigation methods 
1. [[PDF](https://arxiv.org/pdf/2310.20357.pdf)] Enhancing the Spatial Awareness Capability of Multi-Modal Large Language Model, arxiv, 2023, Zhao, Yongqiang, et al.   [__`vis.`__]
2. [[PDF](https://arxiv.org/pdf/2312.06968v3.pdf)][[Code/Data](https://github.com/X-PLUG/mPLUG-HalOwl/tree/main/hacl)] Hallucination Augmented Contrastive Learning for Multimodal Large Language Model, arxiv, 2023, Jiang, Chaoya, et al.   [__`align.`__]
3. [[PDF](https://arxiv.org/pdf/2308.13437.pdf)][[Code/Data](https://github.com/PVIT-official/PVIT)] Position-Enhanced Visual Instruction Tuning for Multimodal Large Language Models, arxiv, 2023, Chen, Chi, et al.   [__`vis.`__][__`align.`__] :large_blue_diamond:
4. 
5. [[PDF](https://arxiv.org/pdf/2312.14233.pdf)][[Code/Data](https://github.com/SHI-Labs/VCoder)] VCoder: Versatile Vision Encoders for Multimodal Large Language Models, CVPR 2024, Jain, et al.   [__`vis.`__]
6. SEEING IS BELIEVING: MITIGATING HALLUCINATION IN LARGE VISION-LANGUAGE MODELS VIA CLIP-GUIDED DECODING, arxiv, 2024   [__`dec.`__]

### Other
Here are some papers that are not directly related to MLLM hallucinations, but may have unexpected inspiration for you.
1. [[PDF](https://openaccess.thecvf.com/content/ICCV2023/papers/Wu_Hallucination_Improves_the_Performance_of_Unsupervised_Visual_Representation_Learning_ICCV_2023_paper.pdf)] Hallucination improves the performance of unsupervised visual representation learning, ICCV 2023, Wu, Jing, et al.  
2. [[PDF](https://arxiv.org/pdf/2111.08276.pdf)][[Code/Data](https://github.com/zengyan-97/X-VLM)] Multi-Grained Vision Language Pre-Training: Aligning Texts with Visual Concepts, ICML 2022, Zeng, Yan, et al. :fire:








[[Code/Data](https://github.com/BradyFU/Awesome-Multimodal-Large-Language-Models/tree/Evaluation)]   [__`ben.`__:MME] :fire:


