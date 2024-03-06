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
1. A Survey on Hallucination in Large Vision-Language Models, arxiv, 2024, Liu, Hanchao, et al.[[PDF](https://arxiv.org/pdf/2402.00253.pdf)]
2. A Survey of Hallucination in “Large” Foundation Models, arxiv, 2024, Rawte, et al. [[PDF](https://arxiv.org/pdf/2309.05922.pdf)] :star:

### Benchmarks
Here are some works that could evaluate the hallucination performances of MLLMs, including some popular benchmarks. Most work products fine-tuning using their benchmark dataset, which could reduce the likelihood of hallucinating without sacrificing its performance on other benchmarks. And some papers have designed clever ways to construct such datasets. 
#### 【2023】  
1. [[PDF](https://arxiv.org/pdf/2306.13394.pdf)][[Code/Data](https://github.com/BradyFU/Awesome-Multimodal-Large-Language-Models/tree/Evaluation)] MME: A Comprehensive Evaluation Benchmark for Multimodal Large Language Models, arxiv, 2023, Fu, Chaoyou, et al.   [__`ben.`__:MME] :fire: 
2. [[PDF](https://arxiv.org/pdf/2305.10355.pdf)] Evaluating Object Hallucination in Large Vision-Language Models, EMNLP 2023, Li, Yifan, et al. [__`ben.`__:POPE] :fire: 
3. [[PDF](https://www.researchgate.net/profile/Fuxiao-Liu-2/publication/376072740_HALLUSIONBENCH_An_Advanced_Diagnostic_Suite_for_Entangled_Language_Hallucination_Visual_Illusion_in_Large_Vision-Language_Models/links/6568af0e3fa26f66f43abf17/HALLUSIONBENCH-An-Advanced-Diagnostic-Suite-for-Entangled-Language-Hallucination-Visual-Illusion-in-Large-Vision-Language-Models.pdf)][[Code/Data](https://drive.google.com/drive/folders/1C_IA5rx_Hm67TYpdNf3TL5VlM30TLGRQ)] HALLUSIONBENCH: An Advanced Diagnostic Suite for Entangled Language Hallucination & Visual Illusion in Large Vision-Language Models, arxiv, 2023, Guan, Tianrui, et al.  [__`ben.`__:HALLUSIONBENCH]
4. [[PDF](https://arxiv.org/pdf/2309.14525.pdf)][[Code/Data](https://llava-rlhf.github.io.)] ALIGNING LARGE MULTIMODAL MODELS WITH FACTUALLY AUGMENTED RLHF, arxiv, 2023, Sun, Zhiqing, et al.   [__`ben.`__:MMHAL-BENCH] :large_blue_diamond:
5. [[PDF](https://arxiv.org/pdf/2308.15126.pdf)][[Code/Data](https://github.com/junyangwang0410/HaELM)] Evaluation and Analysis of Hallucination in Large Vision-Language Models, arxiv, 2023, Wang, Junyang, et al.   [__`ben.`__:HaELM] :large_blue_diamond:
6. [[PDF](https://arxiv.org/pdf/2311.07397v2.pdf)][[Code/Data](https://github.com/junyangwang0410/AMBER)] AMBER: An LLM-free Multi-dimensional Benchmark for MLLMs Hallucination Evaluation, arxiv, 2023, Wang, Junyang, et al.   [__`ben.`__:AMBER]
7. [[PDF](https://arxiv.org/pdf/2310.05338.pdf)] Negative object presence evaluation (nope) to measure object hallucination in vision-language models, arxiv, 2023, Lovenia, Holy, et al.   [__`ben.`__:NOPE]
8. [[PDF](https://arxiv.org/pdf/2309.02301.pdf)] Ciem: Contrastive instruction evaluation method for better instruction tuning, NeurIPS 2023 Workshop, Hu, Hongyu, et al.   [__`ben.`__:Ciem]
9. [[PDF](https://arxiv.org/pdf/2311.01477.pdf)][[Code/Data](https://github.com/bcdnlp/FAITHSCORE)] Faithscore: Evaluating hallucinations in large vision-language models, arxiv, 2023, Jing, Liqiang, et al.   [__`ben.`__:Faithscore(metric)]   
#### 【2024】   
10. [[PDF](https://openreview.net/pdf?id=J44HfH4JCg)] MITIGATING HALLUCINATION IN LARGE MULTIMODAL MODELS VIA ROBUST INSTRUCTION TUNING, ICLR 2024,    [__`ben.`__:GAVIE] :large_blue_diamond:
11. [[PDF](https://arxiv.org/pdf/2312.01701v1.pdf)][[Code/Data](https://github.com/Anonymousanoy/FOHE)] Mitigating Fine-Grained Hallucination by Fine-Tuning Large Vision-Language Models with Caption Rewrites, MMM 2024, Wang, Lei, et al.   [__`ben.`__:FGHE/FOHE(An upgraded version of POPE)]
12. [[PDF](https://arxiv.org/pdf/2402.14683.pdf)][[Code/Data](https://github.com/wenhuang2000/VHTest)] Visual Hallucinations of Multi-modal Large Language Models, arxiv, 2024, Huang, Wen, et al.    [__`ben.`__:two benchmarks generated by VHTest]
13. [[PDF](https://arxiv.org/pdf/2401.06209.pdf)] Eyes wide shut? exploring the visual shortcomings of multimodal llms, arxiv, 2024, Tong, Shengbang, et al.   [__`ben.`__:MMVP]
14. [[PDF](https://www.cs.emory.edu/~jyang71/files/lvlm-workshop.pdf)] Evaluation and Enhancement of Semantic Grounding in Large Vision-Language Models, AAAI-ReLM Workshop. 2024, Lu, Jiaying, et al.   [__`ben.`__:MSG-MCQ]
15. [[PDF](https://arxiv.org/pdf/2308.06394.pdf)][[Code/Data](https://github.com/hendryx-scale/mhal-detect)] Detecting and Preventing Hallucinations in Large Vision Language Models, AAAI 2024, Gunjal, et al.   [__`ben.`__:M-HalDetect] :large_blue_diamond:
16. [[PDF]()][[Code/Data]()]   [__`ben.`__:]
17. 



### Hallucination Mitigation methods 
1. Enhancing the Spatial Awareness Capability of Multi-Modal Large Language Model, arxiv, 2023, Zhao, Yongqiang, et al.[[PDF](https://arxiv.org/pdf/2310.20357.pdf)]   [__`vis.`__]
2. VCoder: Versatile Vision Encoders for Multimodal Large Language Models, CVPR 2024, Jain, et al.[[PDF](https://arxiv.org/pdf/2312.14233.pdf)][[Code/Data](https://github.com/SHI-Labs/VCoder)]   [__`vis.`__]
3. Hallucination Augmented Contrastive Learning for Multimodal Large Language Model, arxiv, 2023, Jiang, Chaoya, et al.[[PDF](https://arxiv.org/pdf/2312.06968v3.pdf)][[Code/Data](https://github.com/X-PLUG/mPLUG-HalOwl/tree/main/hacl)]   [__`align.`__]
4. 

### Other
1. Hallucination improves the performance of unsupervised visual representation learning, ICCV 2023, Wu, Jing, et al.[[PDF](https://openaccess.thecvf.com/content/ICCV2023/papers/Wu_Hallucination_Improves_the_Performance_of_Unsupervised_Visual_Representation_Learning_ICCV_2023_paper.pdf)]  



