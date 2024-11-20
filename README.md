Repository for training multimodal world model
- Dataset: [Multimodal Mind2Web (labeled)](https://huggingface.co/datasets/DLI-Lab/Multimodal-Mind2Web-HTML-WM-messages)
- Base model: [Qwen2-VL-7B-Instruct](https://github.com/QwenLM/Qwen2-VL)


## Setup (Installation)

Tested on Python 3.11 & CUDA 12.4 (check [original requirements](https://github.com/QwenLM/Qwen2-VL))

```bash
git clone --depth 1 https://github.com/aeromaki/Qwen-2-VL-WM.git
cd Qwen-2-VL-WM
pip install -e ".[torch,metrics]"
```

## Training

You can edit the train config in `train-qwen-config.yaml`. After editing, just run the command below to start training.

```bash
bash train-qwen.sh
```

## Modifications from [original source](https://github.com/hiyouga/LLaMA-Factory)
- Specified `torch` version in `requirements.txt` to avoid dependency conflict
- Added `liger-kernel`, `bitsandbytes` in `requirements.txt` for optimization & quantization
- Added [custom dataset](https://huggingface.co/datasets/DLI-Lab/Multimodal-Mind2Web-HTML-WM-messages) in `data/dataset_info.json` (`"multimodal-mind2web"`)
- Added `train-qwen-config.yaml`, `train-qwen.sh`
- Removed unnecessary files (assets)
- Edited `README.md`

Nothing else!