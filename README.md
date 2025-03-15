# GraphLoRA
This is an official implementation of KDD 25 paper GraphLoRA: Structure-Aware Contrastive Low-Rank Adaptation for Cross-Graph Transfer Learning.

## Requirements
```
python==3.11.5
torch==2.1.0
cuda==12.1
numpy==1.26.0
torch_geometric==2.4.0
pyyaml==6.0.1
setuptools>=68.0.0
packaging>=23.2
```

## How to Run
You can easily run our code by

```
# Pre-training
python main.py --is_pretrain True

# Fine-tuning
python main.py --is_transfer True
```
