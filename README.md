# QLoRA for Ours

```shell
conda create -y -n qlora9 python=3.9
conda activate qlora9
pip install -U -r requirements.txt
pip install --upgrade bitsandbytes
pip install "numpy<2.0"
```

```shell
conda activate qlora9

python qlora.py --model_name_or_path "facebook/opt-1.3b"

python qlora.py --model_name_or_path "meta-llama/Llama-2-7b-hf" --use_auth_token True
```
