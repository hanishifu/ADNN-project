# Do AI Agents Know Which Actions Cannot Be Undone?

### A Study of Reversibility Awareness in an LLM-Based Agent

**Authors:** Hanish Reddy and Aishika Reddy

## Abstract

This project investigates whether large language models (LLMs) can recognise when an action is irreversible and whether this awareness influences their decision-making in agent-based environments.

We study reversibility awareness through multiple research questions involving hidden-state representations, direct model classification, agent behaviour, and next-state prediction uncertainty.

## Research Questions

### RQ1 — Hidden-State Linear Probing

Can reversibility information be decoded from the internal representations of an LLM?

We investigate binary and three-class reversibility classification using hidden-state representations and linear probes.

### RQ2 — Direct Reversibility Classification

How accurately can an LLM directly classify actions according to their reversibility?

We compare direct model predictions with ground-truth labels and probe-based predictions.

### RQ3 — Agent Behaviour

Does an agent behave more cautiously when faced with irreversible actions?

We investigate differences in inspection, confirmation, caution, and action selection across reversible and irreversible scenarios.

**Important:** The initial six-family experiment has a safe-action availability confound, so its behavioural differences should not be interpreted as clean causal evidence of reversibility awareness.

### RQ5 — Next-State Prediction Uncertainty

Can uncertainty in next-state prediction help distinguish irreversible from reversible transitions?

This research question currently contains preliminary pilot work and requires further experimentation.

## Repository Structure

```text
ADNN-project/
├── RQ1/
│   ├── datasets
│   ├── probe results
│   └── plots
├── RQ2/
│   ├── classification datasets
│   └── evaluation results
├── RQ3/
│   ├── Six_Family_Primary/
│   └── Two_Family_Diagnostic/
├── notebooks/
│   └── ADNN_Irreversibility_Organised_Final.ipynb
├── report/
│   └── ADNN_Reversibility_Awareness_Report_Updated.pdf
├── requirements.txt
└── README.md
```

## Models and Experimental Setup

The project investigates LLM-based reversibility awareness using Qwen2.5-7B-Instruct, with a second model family, Llama-3.1-8B-Instruct, included in the broader research design.

Experiments involve labelled action scenarios, hidden-state extraction, classification, and simulated agent interactions.

## Key Findings and Limitations

- **RQ1:** Initial pilot experiments show strong reversibility classification performance from hidden-state representations. However, state-only baselines also achieved perfect performance, meaning the results do not establish that the model encodes abstract reversibility concepts independently of the input state.
- **RQ2:** Direct classification achieved 80% accuracy and 80% balanced accuracy on a 60-example pilot evaluation.
- **RQ3:** The initial six-family experiment showed behavioural differences between conditions, but the safe-action availability confound prevents a clean causal interpretation.
- **RQ5:** Preliminary next-state prediction results are exploratory and insufficient for a reliable AUROC conclusion.

These findings should be interpreted in light of the limitations of the current experiments.

## Installation

Clone the repository:

```bash
git clone https://github.com/hanishifu/ADNN-project.git
cd ADNN-project
```

Install dependencies:

```bash
pip install -r requirements.txt
```

## Research Report

The updated research report is available in the `report/` directory.

## Reproducibility

The repository includes research datasets, evaluation outputs, visualisations, and the organised experimental notebook.

Large hidden-state representations are stored separately because of GitHub file-size limitations.

## Disclaimer

All irreversible actions are simulated within research environments. No real-world files, accounts, emails, or financial transactions are modified.

## Acknowledgements

This project was conducted as part of an academic research assignment in Artificial Deep Neural Networks (ADNN).
