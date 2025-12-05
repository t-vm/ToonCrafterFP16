## Introduction
This repository modifies the inference code of the Tooncrafter project to reduce GPU memory usage. You do not need to make any changes to the model itself.

Generated quality may be slightly affected.

本仓库对Tooncrafter项目的推理代码进行修改以达到减少显存占用的目的，您无需对模型权重等相关文件做出任何改动。
生成质量可能受到些许影响。




## 🧰 Models

|Model|Resolution|GPU Mem. & Inference Time (RTX2080Ti(22GiB), ddim 50steps)|Checkpoint|
|:---------|:---------|:--------|:--------|
|ToonCrafter_512|320x512| ~24G & 24s (`perframe_ae=True`)|[Hugging Face](https://huggingface.co/Doubiiu/ToonCrafter/blob/main/model.ckpt)|



## ⚙️ Setup

### Install Environment via Anaconda (Recommended)
```bash
conda create -n tooncrafter python=3.8.5
conda activate tooncrafter
pip install -r requirements.txt
```


## 💫 Inference
### 1. Command line
First, create directory
```bash
mkdir checkpoints/tooncrafter_512_interp_v1
```

Then download pretrained ToonCrafter_512 and put the `model.ckpt` in `checkpoints/tooncrafter_512_interp_v1/model.ckpt`.
```bash
  sh scripts/run.sh
```


### 2. Local Gradio demo

Download the pretrained model and put it in the corresponding directory according to the previous guidelines.
```bash
  python gradio_app.py 
```




