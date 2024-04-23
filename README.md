

# <img src="vitron.png" style="width: 5%"> VITRON: A Unified Pixel-level Vision LLM for Understanding, Generating, Segmenting, Editing
[Hao Fei](http://haofei.vip/)$^{1,2}$, [Shengqiong Wu](https://chocowu.github.io/)$^{1,2}$, [Hanwang Zhang](https://personal.ntu.edu.sg/hanwangzhang/)$^{1,3}$, [Tat-Seng Chua](https://www.chuatatseng.com/)$^{2}$, [Shuicheng Yan](https://yanshuicheng.info/)$^{1}$

**▶ $^{1}$ Skywork AI, Singapore   ▶ $^{2}$ National University of Singapore   ▶ $^{3}$ Nanyang Technological University**



<a href='https://vitron-llm.github.io/'><img src='https://img.shields.io/badge/Project-Page-Green'></a>
<a href='http://101.200.223.110:18088/'><img src='https://img.shields.io/badge/Demo-Page-purple'></a> 
<a href='https://is.gd/aGu0VV'><img src='https://img.shields.io/badge/Paper-PDF-orange'></a> 
![License](https://img.shields.io/badge/License-BSD-blue.svg)
[![YouTube](https://badges.aleen42.com/src/youtube.svg)](https://youtu.be/wiGMJzoQVu4)


## 📰 News
* **[2024.04.04]**  👀👀👀 Our [Vitron](https://vitron-llm.github.io/) is available now! Welcome to **watch** 👀 this repository for the latest updates.



## 😮 Highlights

Existing vision LLMs might still encounter challenges such as superficial instance-level understanding, lack of unified support for both images and videos, and insufficient coverage across various vision tasks. To fill the gaps, we present Vitron, a universal pixel-level vision LLM, designed for comprehensive understanding (perceiving and reasoning), generating, segmenting (grounding and tracking), editing (inpainting) of both static image and dynamic video content.

<p align="center" width="100%">
<a target="_blank"><img src="assets/intro.png" alt="vitron" style="width: 90%; min-width: 200px; display: block; margin: auto;"></a>
</p>


## 🛠️ Requirements and Installation
* Python >= 3.8
* Pytorch == 2.1.0
* CUDA Version >= 11.8
* Install required packages:
```bash
git clone https://github.com/SkyworkAI/Vitron
cd Vitron
conda create -n vitron python=3.10 -y
conda activate vitron
pip install --upgrade pip 
pip install -e .
pip install -e ".[train]"
pip install flash-attn --no-build-isolation
pip install decord opencv-python git+https://github.com/facebookresearch/pytorchvideo.git@28fe037d212663c6a24f373b94cc5d478c8c1a1d
```
<details> 
<summary>🔥🔥🔥 Installation or Running Fails? 🔥🔥🔥 </summary>

1. When running ffmpeg, `Unknown encoder 'x264'`:
    -  try to re-install ffmpeg:
    ```
    conda uninstall ffmpeg
    conda install -c conda-forge ffmpeg   # `-c conda-forge` can not omit
    ```
  
2. Fail to install detectron2, try this command:
    ```
    python -m pip install 'git+https://github.com/facebookresearch/detectron2.git'
    ```
    or refer this [Website](https://detectron2.readthedocs.io/en/latest/tutorials/install.html).
  
3. Error in gradio. As there are a big update in `gradio>=4.0.0`, please make sure install gradio with the same verion in `requirements.txt`.
</details>

## 👍 Deploying Gradio Demo
* Firstly, you need to prepare the checkpoint, and then you can run the demo locally via:
```
python app.py
```


## 🙌 Related Projects
You may refer to related work that serves as foundations for our framework and code repository, 
[Vicuna](https://github.com/lm-sys/FastChat), 
[SEEM](https://github.com/UX-Decoder/Segment-Everything-Everywhere-All-At-Once), 
[i2vgenxl](https://github.com/ali-vilab/VGen), 
[StableVideo](https://github.com/rese1f/StableVideo), and
[Zeroscope](https://huggingface.co/cerspense/zeroscope_v2_576w).
We also partially draw inspirations from 
[Video-LLaVA](https://github.com/PKU-YuanGroup/Video-LLaVA),
and [LanguageBind](https://github.com/PKU-YuanGroup/LanguageBind).
Thanks for their wonderful works.


## 🔒 License
* The majority of this project is released under the Apache 2.0 license as found in the [LICENSE](https://github.com/SkyworkAI/Vitron/blob/main/LICENSE) file.
* The service is a research preview intended for non-commercial use only, subject to the model [License](https://github.com/facebookresearch/llama/blob/main/MODEL_CARD.md) of LLaMA, [Terms of Use](https://openai.com/policies/terms-of-use) of the data generated by OpenAI, and [Privacy Practices](https://chrome.google.com/webstore/detail/sharegpt-share-your-chatg/daiacboceoaocpibfodeljbdfacokfjb) of ShareGPT. Please contact us if you find any potential violation.




## ✏️ Citation
If you find our paper and code useful in your research, please consider giving a star :star: and citation :pencil:.

```BibTeX
@articles{hao2024vitron,
  title={Vitron: A Unified Pixel-level Vision LLM for Understanding, Generating, Segmenting, Editing},
  author={Hao Fei, Shengqiong Wu, Hanwang Zhang, Tat-Seng Chua, Shuicheng Yan},
  journal={CoRR},
  year={2024}
}
```


<!---->
## ✨ Star History
[![Star History](https://api.star-history.com/svg?repos=/SkyworkAI/Vitron&type=Date)](https://star-history.com/#SkyworkAI/Vitron&Date)




