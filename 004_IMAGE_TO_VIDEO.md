# Image2Video

This document covers step-by-step guide to get Stable Diffusion 1.1 working in AUTOMATIC1111.
At time of writing, the UI part is not supported by the official WebUI.
You will need to leverage either comfy workflow or download [forge](https://github.com/lllyasviel/stable-diffusion-webui-forge).
In this document, we will cover the latter.

## Download forge

- Clone the repository: https://github.com/lllyasviel/stable-diffusion-webui-forge
- Run `cd stable-diffusion-webui-force`
- Run `./webui.sh`
- Copy configuration / models from previous normal installation

## Download model

Download the model from:

- https://huggingface.co/stabilityai/stable-video-diffusion-img2vid-xt-1-1/tree/main

We only need the `svd_xt_1_1.safetensors` file and place it under `/models/svd`

## Generate an image with txt2img

Main thing to keep in mind is that the underlying model needs a 1024 by 576 image.

## Use image with svd

After generating an image, you can click the button that moves the image to SVD tab.
By default all the parameters should be kept the same, ensure you can select the svd model.

## Upscaling the video

The output is only 6fps, you can opt to upscale to 4k/60fps with a tool like topaz video AI upscale.
