# GraphLoRA

This is an official implementation of KDD 25 paper GraphLoRA: Structure-Aware Contrastive Low-Rank Adaptation for Cross-Graph Transfer Learning.

> This is the official project's fork. Added `uv` and CPU support for easier code replication.

## Requirements

```requirements.txt
python==3.11.5
torch==2.1.0
numpy==1.26.0
torch_geometric==2.4.0
pyyaml==6.0.1
setuptools>=68.0.0
packaging>=23.2
```

**If use GPU, please install cuda12.1.** Other versions do not guarantee whether they can run

### Using `pip` and `conda`

```shell
# If use CPU
pip install -r requirements_cpu.txt

# If use GPU
pip install -r requirements_gpul.txt # Linux system
pip install -r requirements_gpuw.txt # Windows system

# If you use conda, it is highly recommended to create a Python empty environment and use the above pip command to install dependencies 
conda env create -n <env_name> "python==3.11.5"
```

### Using `uv`

```shell
# If use CPU
uv sync --extra cpu

# If use GPU
# !!! Because a bug about `uv sync` torch==2.1.0+cu121, Please distinguish your system
uv sync --extra gpul # Linux system
uv sync --extra gpuw # Windows system
```

## How to Run

You can easily run our code by

```shell
# Pre-training
python main.py --is_pretrain True

# Fine-tuning
python main.py --is_transfer True
```

If you use CPU, please use

```shell
# Pre-training
python main.py --is_pretrain True --no-gpu

# Fine-tuning
python main.py --is_transfer True --no-gpu
```

Please refer to the [main.py](./main.py) file for other options
