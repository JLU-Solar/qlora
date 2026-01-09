# QLoRA for Ours

## SSH Tunnel

```shell
ssh s34 -R 17890:127.0.0.1:17890
```

## Env

```shell
export https_proxy=http://127.0.0.1:17890
export http_proxy=http://127.0.0.1:17890
export all_proxy=http://127.0.0.1:17890

# git clone git@github.com:JLU-Solar/qlora.git
git clone https://github.com/JLU-Solar/qlora.git

conda create -y -n qlora9 python=3.9
conda activate qlora9
pip install -U -r requirements.txt
pip install --upgrade bitsandbytes
pip install "numpy<2.0"
```

## Run

```shell
export https_proxy=http://127.0.0.1:17890
export http_proxy=http://127.0.0.1:17890
export all_proxy=http://127.0.0.1:17890
conda activate qlora9

python qlora.py --model_name_or_path "facebook/opt-1.3b"

python qlora.py --model_name_or_path "meta-llama/Llama-2-7b-hf" --use_auth_token True
```
