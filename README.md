> This is the official project's fork. Added `uv` and CPU support for easier code replication.

# GraphLoRA

This is an official implementation of KDD 25 paper GraphLoRA: Structure-Aware Contrastive Low-Rank Adaptation for Cross-Graph Transfer Learning.

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

**If use GPU, please install cuda12.1.** Other versions don't guarantee whether they can run

### Using `pip` and `conda`

```shell
pip install -r requirements.txt -f 'https://mirrors.aliyun.com/pytorch-wheels/cu121/'

# If you use conda, it is highly recommended to create a Python empty environment and use the above pip command to install dependencies 
conda env create -n <env_name> "python==3.11.5"
```

### Using `uv`

```shell
# If you just want to synchronous enironment, you can try command below
uv sync

# But you should run this command when you just directly run code.
# Don't worry environment's problems, uv will take care of everything for you
uv run python main.py ...
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
