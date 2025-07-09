
# Hardware Trojan Detection using TabNet & TabTransformer

## What’s This About?

In today’s hardware design world, security isn’t just a software concern—**hardware can be hacked too**. One such threat? **Hardware Trojans**—malicious modifications embedded in chips during design or manufacturing. These Trojans can leak data, degrade performance, or open secret backdoors.

This project explores how to **detect such hardware Trojans** using the power of **deep learning on tabular data**. Specifically, we use two cutting-edge models:

-   [**TabNet**](https://arxiv.org/abs/1908.07442) – interpretable deep learning for tabular data.
-  [**TabTransformer**](https://arxiv.org/abs/2012.06678) – leverages transformers for categorical and numerical feature fusion.

---

##  Why Tabular Deep Learning?

Most hardware datasets are structured—think rows of features like `num_gates`, `power_profile`, `area`, `frequency_shift`, etc. Traditional ML (like SVMs or Random Forests) can handle these, but **deep learning** opens up:

- More powerful feature representation.
- Better handling of categorical + numerical mix.
- Potential for **end-to-end Trojan detection** pipelines.

---
## How It Works

1. **Dataset Preparation**  
   Preprocessed datasets are structured with Trojan-free vs. Trojan-infected hardware examples. Missing values are handled, and categorical columns are encoded.

2. **Model Training**  
   - **TabNet** is trained with feature masks for interpretability.
   - **TabTransformer** encodes categorical features using attention before feeding them into a deep network.

3. **Evaluation Metrics**  
   - Accuracy  
   - Precision & Recall (especially important for Trojan detection)  
   - ROC-AUC  

4. **Inference**  
   Once trained, the models can predict whether a new IC design is potentially infected or safe.

---
