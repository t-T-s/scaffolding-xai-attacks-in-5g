#  Deceiving XAI Methods in 5G and Beyond

This repository accompanies Chapter 6 of the thesis: **"Deceiving XAI Methods in 5G and Beyond"**, which introduces and analyzes *scaffolding attacks*: a novel threat vector that silently undermines post-hoc explanation methods such as SHAP and LIME in security-critical AI models deployed in 5G networks.

Unlike conventional adversarial attacks, scaffolding does not alter prediction labels but instead *deceives auditors and developers by modifying explanations*, creating a dual-model behavior: one for real-world inputs and another for XAI-generated synthetic perturbations. This blind spot has serious implications for trust, accountability, and safety in AI-driven network infrastructures.

## 🚨 Key Features

- 🔐 **Adversarial Scaffolded Model**: Implementation of a black-box ML model with hidden components that return biased decisions for real-world data while masking them under synthetic queries from explainers like SHAP/LIME.
- 🧠 **Target Feature Selection**: A novel method using weighted feature attributions across multiple models combined with domain knowledge filtering to select the best feature for attackers to suppress.
- 🧪 **Detection Framework**: Lightweight Hellinger distance-based detection method to identify discrepancies between real-world and perturbed sample outputs.
- 🧰 **Experimentation on Real-world Datasets**:
  - **5GNIDD**: Real 5G traffic collected in Finland.
  - **NSL-KDD**: Widely-used benchmark dataset in NIDS research.

📈 Detection Performance

  Fidelity (XAI fooling rate): ~60%

  Detection Accuracy (perturbation classifier): 100%

  Hellinger Distance (attack vs. benign): 0.86 (scaffolded) vs. 0.41 (control)

  Target Features Identified: service_http (NSL-KDD), Seq (5GNIDD)

📚 Citation

If you use this repository or the ideas in your own research, please cite:

```
@inproceedings{senevirathna2024deceiving,
  title={Deceiving post-hoc explainable ai (xai) methods in network intrusion detection},
  author={Senevirathna, Thulitha and Siniarski, Bartlomiej and Liyanage, Madhusanka and Wang, Shen},
  booktitle={2024 IEEE 21st Consumer Communications \& Networking Conference (CCNC)},
  pages={107--112},
  year={2024},
  organization={IEEE}
}

```
