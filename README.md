# 🎯 Uplift Model for Targeted Marketing

This repository implements an Uplift Modeling approach to identify customers who are positively influenced by marketing campaigns. The goal is to target only those customers whose behavior is changed by the campaign, thereby maximizing marketing ROI and avoiding wasted spend.

## 🔍 What is Uplift Modeling?

Uplift modeling (also known as incremental or true lift modeling) helps distinguish between:

- **Persuadables**: Respond because of the campaign
- **Sure Things**: Would respond anyway
- **Lost Causes**: Won’t respond either way
- **Do Not Disturbs**: Respond negatively to the campaign

This enables smarter targeting by focusing only on Persuadables.

## 🧠 Approach

The uplift model is built using a two-model method:

- A classifier is trained on the **treatment group** (those who received the campaign).
- Another classifier is trained on the **control group** (those who did not).
- The **uplift score** is the difference in predicted probabilities of response between these two models.

Alternatively, advanced learners such as Uplift Random Forests or X-Learners can be used (see `scikit-uplift`).

## 🚀 Getting Started

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/uplift-model.git
    cd uplift-model
    ```

2. Install the dependencies:

    ```bash
    pip install -r requirements.txt
    ```

3. Train the uplift models:

    ```bash
    python train_models.py
    ```

4. Evaluate the uplift:

    ```bash
    python evaluate_uplift.py
    ```

## 📈 Evaluation

Uplift performance is measured using:

- **Qini Curve** and **Qini Coefficient**
- **Uplift at Top N%** (e.g., top decile)
- **AUUC (Area Under the Uplift Curve)**

These metrics assess how effectively the model identifies Persuadables.

## 📦 Dependencies

- Python 3.7+
- `pandas`
- `numpy`
- `scikit-learn`
- `matplotlib`
- `seaborn`
- `scikit-uplift` (optional for advanced methods)

Install them with:

```bash
pip install -r requirements.txt
