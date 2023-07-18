# text-generation-webui-docker
text-generation-webui in an NVIDIA/JupyterLab/Anaconda supported environment

Designed to facilitate the operation of Large Language Models, such as LLaMA, llama.cpp, GPT-J, Pythia, OPT, and GALACTICA, through a Gradio web interface. This inclusion is designed to replicate the functionality provided by AUTOMATIC1111/stable-diffusion-webui, integrated into our Docker container stack, aiming at developers who need a web-based interface for text generation tasks.

The Docker layer is designed with hardware optimization in mind and is compatible with NVIDIA GPUs. This layer transitions from Jupyter Notebooks to JupyterLab, providing a more versatile and feature-rich integrated development environment. It includes developer-friendly features such as an efficient text streaming system, API endpoints for websocket streaming, and the capacity to create custom chat characters. Detailed documentation is provided to assist developers in understanding and utilizing the full capabilities of this layer within the Docker stack.

This Docker layer supports three distinct interface modes: default, notebook, and chat. It is compatible with various model backends including transformers, llama.cpp, AutoGPTQ, GPTQ-for-LLaMa, ExLlama, RWKV, and FlexGen. Switching between these models is made straightforward through a dropdown menu. Additional functionalities, such as dynamic LoRA operations (loading and unloading), multimodal pipelines, 8-bit and 4-bit inference through bitsandbytes, and DeepSpeed ZeRO-3 inference are also incorporated into this layer.

Will write a better documentation later.

```bash
docker run \
    --rm
    --gpus=all \
    -it -d \
    -p 7860:7860 \
    -p 8888:8888 \
    xychelsea/text-generation-webui:latest-gpu-jupyter /bin/bash
```
