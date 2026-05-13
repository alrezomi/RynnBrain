# RynnBrain Thesis Setup

## Ubuntu setup

```bash
sudo apt update
sudo apt install python3.10 python3.10-venv python3.10-dev git

python3.10 -m venv venv310
source venv310/bin/activate

pip install --upgrade pip
pip install -r requirements.txt

python -m ipykernel install --user --name rynnbrain310 --display-name "Python (RynnBrain 3.10)"


# Download CoP model:

source venv310/bin/activate
pip install -U hf_transfer
export HF_HUB_ENABLE_HF_TRANSFER=1

hf download Alibaba-DAMO-Academy/RynnBrain-CoP-8B \
  --local-dir hf_cache/RynnBrain-CoP-8B