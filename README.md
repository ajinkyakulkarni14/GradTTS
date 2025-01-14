# GradTTS
## Unofficial Pytorch implementation of "Grad-TTS: A Diffusion Probabilistic Model for Text-to-Speech" ([arxiv](https://arxiv.org/abs/2105.06337))

## About this repo
This is an unofficial implementation of GradTTS. We created this project based on GlowTTS (https://github.com/jaywalnut310/glow-tts). We replace the GlowDecoder with DiffusionDecoder which follows the settings of the original paper. 

Orignal author of this repo replaced torch.distributed with horovod. For convience of installation on our GPU cluster, I have replaced back horovod to torch.distributed. The pretrained model trained on LJS dataset will be released soon.

## Updates

2021/07/28: [LJSpeech Samples](https://github.com/WelkinYang/GradTTS/tree/main/egs/gradtts_n_1000/n_1000_steps_259000_ljspeech_hifigan) uploaded which has the same performance as the original paper's demo.

## Training and inference
Please go to egs/ folder, and see run.sh and inference_waveglow_vocoder.py for example use. Before training, please download and extract the [LJ Speech dataset](https://keithito.com/LJ-Speech-Dataset/), then rename or create a link to the dataset folder: `ln -s /path/to/LJSpeech-1.1/wavs DUMMY`. And build Monotonic Alignment Search Code (Cython): `cd monotonic_align; python setup.py build_ext --inplace`.  Before inference, you should download waveglow checkpoint from [download_link](https://drive.google.com/file/d/1rpK8CzAAirq9sWZhe9nlfvxMF1dRgFbF/view) and put it into the waveglow folder.

## Reference Materials
[Grad-TTS: A Diffusion Probabilistic Model for Text-to-Speech](https://arxiv.org/abs/2105.06337)

[GlowTTS](https://github.com/jaywalnut310/glow-tts)

[Score-Based Generative Modeling through Stochastic Differential Equations](https://openreview.net/forum?id=PxTIG12RRHS)

[score_sde_pytorch](https://github.com/yang-song/score_sde_pytorch)

[denoising-diffusion-pytorch](https://github.com/lucidrains/denoising-diffusion-pytorch)

## Authors
Heyang Xue(https://github.com/WelkinYang) and Qicong Xie(https://github.com/QicongXie)




