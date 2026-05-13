# Transferable Cross-scale Reasoning for Mechanistic Drug Interaction Understanding(TRACER)
This is the code necessary to run experiments on the TRACER algorithm.

## Abstract
Polypharmacy introduces complex pharmacological interactions that remain poorly understood, posing major challenges for drug safety and clinical decision-making. Although computational methods can predict adverse drug interactions, the mechanistic basis underlying adverse interactions remains largely unresolved. Here we present TRACER, a computational framework that traces hierarchical determinants of pharmacological interactions across molecular and biological scales. By integrating self-supervised molecular representations with biomedical knowledge, TRACER links interaction-relevant molecular fragments to pharmacological pathways, enabling cross-scale mechanistic inference. Across multiple datasets, TRACER identifies molecular motifs and biological pathways consistent with known metabolic and transporter-mediated mechanisms, while achieving robust generalization to diverse and previously unseen drug combinations. These results suggest that mechanistic signals governing drug interactions can be systematically recovered from large-scale data through cross-scale representation learning. Together, TRACER provides a unified framework for tracing the mechanistic basis of adverse drug interactions, offering interpretable insights into pharmacological risks in polypharmacy and supporting mechanism-informed drug development and safer clinical decision-making.

## Requirements

All the required packages can be installed by running pip install -r requirements.txt.

```shell
tensorboard==2.9.1
torch==1.11.0+cu113
tqdm==4.61.2
rdkit==2023.9.6
torchdrug==0.2.1
hyperopt==0.2.7
scipy==1.7.3
scikit-learn==1.0.2
pandas
```

## Running scripts

First `cd` into the corresponding directory, i.e., DrugBank , TWOSIDES or Pretrain.

Our data is uploaded on the [google drive link](https://drive.google.com/file/d/1qH_hmJB3EVFSuuOlALAaekQUqxCFiFwm/view?usp=drive_link)

Once the data is ready, you can run the following scripts to reproduce the results:

```shell
python {dataset}/F_train.py 
```

All the hyperms are setting in file.

## Acknowledge
The code is implemented based on MAE_pytorch (https://github.com/IcarusWizard/MAE/tree/main). The benchmark datasets are from [EmerGNN](https://github.com/LARS-research/EmerGNN) (DrugBank & TWOSIDES & inductive), and process few-shot data based on [META-DDIE](https://github.com/YifanDengWHU/META-DDIE).
We thank them very much.
