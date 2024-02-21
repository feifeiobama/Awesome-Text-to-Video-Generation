# Awesome Text-to-Video Generation

This repository contains a curated list of text-to-video generation papers and [BibTeX entries](https://github.com/feifeiobama/Awesome-Text-to-Video-Generation/blob/main/T2V.bib) (until Dec. 2023).

* [Paper summary](#Paper-summary)
* [Zero-shot leaderboard](#Zero-shot-leaderboard)
* [Dataset summary](#Dataset-summary)



### Paper summary

| Name                                                         | Date         | Affiliation | Train set                                 | Test set                                    | Other expr                                                   |
| ------------------------------------------------------------ | ------------ | ----------- | ----------------------------------------- | ------------------------------------------- | ------------------------------------------------------------ |
| GODIVA                                                       | 21.04        | Microsoft   | HowTo100M                                 | MSR-VTT                                     | **user study**                                               |
| NUWA [website](https://github.com/microsoft/NUWA/blob/main/NUWA.md) | ECCV22       | Microsoft   | 241k VATEX                                | Kinetics, MSR-VTT                           | sketch2video, edit                                           |
| Video Diffusion [website](https://video-diffusion.github.io) | NIPS22       | Google      | 10M                                       | -                                           | **unconditional**, **longer**                                |
| Imagen Video [website](https://imagen.research.google/video/) | 22.10        | Google      | 14M                                       | -                                           | -                                                            |
| MagicVideo [website](https://magicvideo.github.io)           | 22.11        | ByteDance   | WebVid-10M (+ 10M from HD-VILA-100M + 7M) | **UCF-101**, **MSR-VTT**                    | **user study**                                               |
| LVDM [website](https://yingqinghe.github.io/LVDM/) [code](https://github.com/YingqingHe/LVDM) | 22.11        | HKUST       | 2M from WebVid-10M                        | UCF-101, Sky Time-lapse, Taichi             | **unconditional**, **long**                                  |
| Make-A-Video [website](https://makeavideo.studio)            | ICLR23       | Meta        | WebVid-10M + 10M from HD-VILA-100M        | **UCF-101**, **MSR-VTT**                    | **user study**                                               |
| Phenaki [website](https://sites.research.google/phenaki/)    | ICLR23       | Google      | ~15M                                      | Kinetics-400                                | img conditioned                                              |
| CogVideo **[demo](https://huggingface.co/spaces/THUDM/CogVideo)** [website](https://models.aminer.cn/cogvideo/) [code](https://github.com/THUDM/CogVideo) | ICLR23       | THU         | 5.4M                                      | UCF-101, Kinetics-600                       | **user study**                                               |
| Video LDM [website](https://research.nvidia.com/labs/toronto-ai/VideoLDM/) | CVPR23 23.04 | NVIDIA      | WebVid-10M (+ 683k driving)               | **UCF-101**, **MSR-VTT**                    | personalized                                                 |
| Gen1 **[demo](https://app.runwayml.com)** [website](https://research.runwayml.com/gen1) | ICCV23       | Runway      | 6.4M                                      | -                                           | **user study**, edit, iv2v, customization                    |
| PYoCo [website](https://research.nvidia.com/labs/dir/pyoco/) | ICCV23 23.05 | NVIDIA      | 22.5M                                     | **UCF-101**, **MSR-VTT**                    | **unconditional**                                            |
| VideoComposer [website](https://videocomposer.github.io) [code](https://github.com/ali-vilab/videocomposer) | NIPS23       | Alibaba     | WebVid-10M                                | **MSR-VTT**                                 | compositional i2v, sketch, motion control                    |
| GLOBER [website](https://iva-mzsun.github.io/GLOBER) [code](https://github.com/iva-mzsun/GLOBER) | NIPS23       | CASIA       | WebVid-10M or less                        | UCF-101, Sky Time-lapse, Taichi, WebVid-10M | **unconditional**                                            |
| VideoFusion                                                  | 23.03        | CASIA       | WebVid-10M or less                        | UCF-101, Sky Time-lapse, Taichi, WebVid-10M | **unconditional**, long                                      |
| Latent-Shift [website](https://latent-shift.github.io)       | 23.04        | Meta        | WebVid-10M                                | UCF-101, **MSR-VTT**                        | **user study**                                               |
| VideoFactory                                                 | 23.05        | PKU         | HD-VG-130M + WebVid-10M                   | **UCF-101**, **MSR-VTT**, WebVid-10M        | **user study**, personalized                                 |
| Make-Your-Video [website](https://doubiiu.github.io/projects/Make-Your-Video/) [code](https://github.com/AILab-CVC/Make-Your-Video) | 23.06        | CUHK        | WebVid-10M                                | **UCF-101**                                 | **depth**, **re-rendering**, **user study**                  |
| Animate-A-Story [website](https://ailab-cvc.github.io/Animate-A-Story/) | 23.07        | HKUST       | WebVid-10M                                | **UCF-101**                                 | storytelling, **personalized**                               |
| InternVid                                                    | ICLR24 23.07 | Shanghai    | WebVid10M + InternVid18M                  | **UCF-101**, **MSR-VTT**                    | dialogue                                                     |
| ModelScopeT2V **[demo](https://huggingface.co/spaces/damo-vilab/modelscope-text-to-video-synthesis)** [website](https://modelscope.cn/models/damo/text-to-video-synthesis/summary) | 23.08        | Alibaba     | WebVid-10M                                | **MSR-VTT**                                 | -                                                            |
| Dysen-VDM [website](http://haofei.vip/Dysen-VDM/)            | 23.08        | NUS         | WebVid-10M                                | **UCF-101**, **MSR-VTT**                    | **user study**                                               |
| VidRD [website](https://anonymous0x233.github.io/ReuseAndDiffuse/) [code](https://github.com/anonymous0x233/ReuseAndDiffuse) | 23.09        | Huawei      | WebVid-2M, TGIF, VATEX, Pexels (5.3M)     | **UCF-101**                                 | -                                                            |
| LaVie **[demo](https://huggingface.co/spaces/Vchitect/LaVie) [demo2](https://replicate.com/cjwbw/lavie)** [website](https://vchitect.github.io/LaVie-project/) [code](https://github.com/Vchitect/LaVie) | 23.09        | Shanghai    | WebVid-10M + Vimeo25M                     | **UCF-101**, **MSR-VTT**                    | **user study**, long, personalized                           |
| Show-1 **[demo](https://huggingface.co/spaces/showlab/Show-1) [demo2](https://replicate.com/cjwbw/show-1)** [website](https://showlab.github.io/Show-1/) [code](https://github.com/showlab/Show-1) | 23.09        | NUS         | WebVid-10M                                | **UCF-101**, **MSR-VTT**                    | **user study**                                               |
| VideoCrafter **[demo](https://huggingface.co/spaces/VideoCrafter/VideoCrafter) [demo2](https://replicate.com/cjwbw/videocrafter)** [website](https://ailab-cvc.github.io/videocrafter/) [code](https://github.com/AILab-CVC/VideoCrafter) | 23.10        | Tencent     | WebVid-10M + 10M                          | -                                           | **user study**, img conditioned, i2v                         |
| Emu Video [website](https://emu-video.metademolab.com)       | 23.11        | Meta        | 34M                                       | **UCF-101**                                 | **user study**, longer                                       |
| SVD **[demo](https://colab.research.google.com/github/mkshing/notebooks/blob/main/stable_video_diffusion_img2vid.ipynb)** [website1](https://stability.ai/news/stable-video-diffusion-open-ai-video-model) [website2](https://huggingface.co/stabilityai/stable-video-diffusion-img2vid)  [code](https://github.com/Stability-AI/generative-models) | 23.11        | Stability   | LVD (580M) / LVD-F (152M)                 | **UCF-101**                                 | i2v, **user study**, camera motion, multi-view               |
| PixelDance [website](https://makepixelsdance.github.io)      | 23.11        | ByteDance   | WebVid-10M + 500k watermark-free          | **UCF-101**, **MSR-VTT**                    | **long**, sketch instruction, edit                           |
| W.A.L.T [website](https://walt-video-diffusion.github.io)    | 23.12        | Google      | 89M                                       | **UCF-101**, Kinetics-600                   | **class-conditional**, i2v                                   |
| VideoPoet [website](https://sites.research.google/videopoet/) | 23.12        | Google      | ~270M (100M paired)                       | **UCF-101**, **MSR-VTT**                    | **user study**, **stylization**, edit, i2v, long, camera motion |

**Bold** dataset indicates zero-shot evaluation.

 Models without a technical report such as [Gen-2](https://research.runwayml.com/gen2), [Pika 1.0](https://pika.art), [zeroscope](https://zeroscope.replicate.dev) are not included.

**Bold** expr for quantitative



VideoComposer (NeurIPS23), PixelDance: 4fps 16 frames; VideoPoet: 8fps 17 frames; EMU Video: input 4/8fps 8 frames, output 16fps 37 frames



### Zero-shot leaderboard

| Name                | Date         | Data      | MSR-VTT CLIPSIM | MSR-VTT FID      | MSR-VTT FVD | UCF-101 FID | UCF-101 FVD | UCF-101 IS |
| ------------------- | ------------ | --------- | --------------- | ---------------- | ----------- | ----------- | ----------- | ---------- |
| **CogVideo**        | ICLR23       | ~~5.4M~~  | 0.2631          | 23.59            | 1294        | 179.00      | 701.59      | 25.27      |
| MagicVideo          | 22.11        | 10M       |                 |                  | 998         | 145.00      | 655.00      |            |
| **LVDM**            | 22.11        | 2M        | 0.2381          |                  | 742         |             | 641.80      |            |
| VideoFusion         | 23.03        | 10M       | 0.2795          |                  |             | 75.77       | 639.90      | 17.49      |
| Latent-Shift        | 23.04        | 10M       | 0.2773          | 15.23            |             |             |             |            |
| **VideoCrafter**    | 23.10        | ~~20M~~   | 0.2875          |                  |             | 66.95       | 910.87      | 18.26      |
| Video LDM           | CVPR23 23.04 | 10M       | 0.2929          |                  |             |             | 550.61      | 33.45      |
| **VideoComposer**   | NIPS23       | 10M       | 0.2932          |                  | 580         |             |             |            |
| InternVid           | ICLR24 23.07 | ~~28M~~   | 0.2951          |                  |             | 60.25       | 616.51      | 21.04      |
| Animate-A-Story     | 23.07        | 10M       |                 |                  |             |             | 516.15      |            |
| **ModelScopeT2V**   | 23.08        | 10M       | 0.2930          | 11.09            | 550         |             |             |            |
| **LaVie**           | 23.09        | ~~35M~~   | 0.2949          |                  |             |             | 526.30      |            |
| Emu Video           | 23.11        | ~~34M~~   |                 |                  |             |             | 606.20      | 42.70      |
| Make-A-Video        | ICLR23       | 20M       | 0.3049          | 13.17            |             |             | 367.23      | 33.00      |
| VideoFactory        | 23.05        | ~~140M~~  | 0.3005          |                  |             |             | 410.00      |            |
| **Show-1**          | 23.09        | 10M       | 0.3072          | 13.08            | 538         |             | 394.46      | 35.42      |
| **VidRD**           | 23.09        | 5.3M      |                 |                  |             |             | 363.19      | 39.37      |
| Dysen-VDM           | 23.11        | 10M       | **0.3204**      | 12.64            |             |             | 325.42      | 35.57      |
| W.A.L.T             | 23.12        | ~~89M~~   |                 |                  |             |             | 258.10      | 35.10      |
| VideoPoet           | 23.12        | ~~270M~~  | 0.3049 / 0.3123 |                  | **213**     |             | 355.00      | 38.44      |
| PYoCo               | ICCV23 23.05 | ~~22.5M~~ |                 | **9.73** / 22.14 |             |             | 355.19      | **47.76**  |
| **Make-Your-Video** | 23.06        | 10M       |                 |                  |             |             | 330.49      |            |
| PixelDance          | 23.11        | ~~10.5M~~ | 0.3125          |                  | 381         | **49.36**   | 242.82      | 42.10      |
| **SVD**             | 23.11        | ~~152M~~  |                 |                  |             |             | **242.02**  |            |

**Bold** indicates open-source code or demo release.

 ~~Strikethrough~~ indicates private data involved.



### Dataset summary

| Name           | Size       | Type  | Date   | Affiliation     |
| -------------- | ---------- | ----- | ------ | --------------- |
| UCF-101        | 13k        | class | 2013   | UCF             |
| MSR-VTT        | 10K        | text  | CVPR16 | Microsoft       |
| Kinetics       | 650k       | class | CVPR17 | DeepMind        |
| HowTo100M      | 136M       | text  | ICCV19 | ENS             |
| WebVid-10M     | 10M        | text  | ICCV21 | Oxford          |
| HD-VILA-100M   | 103M       | text  | CVPR22 | Microsoft       |
| ~~HD-VG-130M~~ | 130M       | text  | 23.05  | Microsoft       |
| InternVid      | 234M (10M) | text  | 23.07  | Shanghai AI Lab |
| ~~Vimeo25M~~   | 25M        | text  | 23.09  | Shanghai AI Lab |

 ~~Strikethrough~~ indicates not yet released.

UCF-101: 320x240 25fps

MSR-VTT: resize to 320x240 30fps



### Evaluation protocol

eval CLIPSIM, FID, FVD on MSR-VTT, FVD, IS on UCF-101

* CLIP similarity (CLIPSIM): [clipscore](https://github.com/jmhessel/clipscore) ([TorchMetrics](https://lightning.ai/docs/torchmetrics/stable/multimodal/clip_score.html)) CLIP ViT-B/32, ViT-B/16
* Frechet inception distance (FID): [pytorch-fid](https://github.com/mseitzer/pytorch-fid) ([TorchMetrics](https://lightning.ai/docs/torchmetrics/stable/image/frechet_inception_distance.html)) CLIP ViT-B/32
* Frechet video distance (FVD): [TATS](https://github.com/songweige/TATS/blob/main/scripts/sample_vqgan_transformer_short_videos.py) ([LVDM](https://github.com/YingqingHe/LVDM/blob/main/scripts/eval_cal_fvd_kvd.py), [stylegan-v](https://github.com/universome/stylegan-v/blob/master/src/metrics/frechet_video_distance.py)) I3D Kinetics-400
* Inception score (IS): [tgan2](https://github.com/pfnet-research/tgan2/blob/master/tgan2/evaluations/inception_score.py) ([TorchMetrics](https://lightning.ai/docs/torchmetrics/stable/image/inception_score.html), [stylegan-v](https://github.com/universome/stylegan-v/blob/master/src/metrics/inception_score.py)) C3D UCF-101

Table for #evaluation samples and backbone

|               | MSR-VTT CLIPSIM     | MSR-VTT FVD | MSR-VTT FID            | UCF-101 IS | UCF-101 FVD          |
| ------------- | ------------------- | ----------- | ---------------------- | ---------- | -------------------- |
| CogVideo      | -                   | -           | -                      | 10k        | 2048                 |
| Video LDM     | 2990 CLIP32         | -           | -                      |            | 10k                  |
| VideoComposer |                     |             | -                      | -          | -                    |
| InternVid     | 2990 CLIP32         | -           | -                      | 2020       | 2020                 |
| Make-A-Video  | 59794               | -           | 59794                  | 10k        | 10k                  |
| VideoPoet     | 59794 CLIP16/CLIP32 | 40960       | -                      | 10k        | 10k training         |
| PYoCo         | -                   | -           | 59794 CLIP32/Inception | 2020       | 2048                 |
| SVD           | -                   | -           | -                      | -          | 13320 script 240x320 |

