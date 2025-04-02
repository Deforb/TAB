# Algorithms
## Methods introduction
FoundTS envaluated a diverse range of time series foundation models,including  time series pre-trained models pretrained with multi-domain time series and LLM-based models pretrained with large-scale text, along with specific models.

**Time Series Pre-trained Models (TS Pre-trained Models):** 

-  Reconstruction methods: MOIRAI, UniTS, Moment
-  Autoregressive methods: TimesFM, Timer
-  Direct prediction methods: TTM
-  Hybrid pre-training methods: ROSE

**LLM-based Models:**

- Parameter-efficient fine-tuning methods: GPT4TS, SS2IPLLM
- Prompting methods: UniTime, Time-LLM

**Specific Models:**

- CNN-based models: TimesNet
- Transformer-based models: FEDformer, iTransformer, PatchTST
- MLP-based models: FITS, TimeMixer, DLinear

## Frame introduction

<!-- **Data** -->

- The data module includes time series datasets from various domains, each exhibiting diverse statistical characteristics. This wide-ranging coverage facilitates a comprehensive comparison of the prediction and generalization performance of different models.

<!-- **Models** -->

- The model module comprises foundational time series models, including LLM-based models pretrained on large-scale text, multi-domain time series pretrained models, and specific models tailored for particular datasets.

<!-- **Evaluation** -->

- The evaluation module offers a scalable pipeline and standardized evaluation environment with comprehensive strategies and consistent settings, ensuring fair comparisons of models and facilitating reliable results.

<div align="center" style="margin-top:15px">
<img src="architecture.png" width="90%"/>
</div>