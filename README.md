<p align="center">
  <img src="https://artificialanalysis.ai/img/logos/happyhorse_small.svg" alt="Happy Horse logo" width="96" />
</p>

<p align="center"><strong>Community-curated prompts, benchmark signals, and playable sample results.</strong></p>

<h1 align="center">Awesome Happy Horse 1.0</h1>

<p align="center">
  <a href="https://github.com/sindresorhus/awesome"><img src="https://awesome.re/badge.svg" alt="Awesome"></a>
  <a href="https://creativecommons.org/licenses/by/4.0/"><img src="https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg" alt="License: CC BY 4.0"></a>
  <a href="https://github.com/ZeroLu/awesome-happy-horse/stargazers"><img src="https://img.shields.io/github/stars/ZeroLu/awesome-happy-horse?style=social" alt="GitHub stars"></a>
</p>

Last updated on 2026-04-14

## What is Happy Horse 1.0?

Happy Horse 1.0 is a groundbreaking AI video generation model that has set a new standard for high-quality text-to-video (T2V) and image-to-video (I2V) generation. Developed by an independent research collective (led by Zhang Di, former VP of Kuaishou and technical lead of Kling AI, and composed of a team formerly from Alibaba's Taotian Group ATH-AI Innovation Division), the model initially launched anonymously as a "mystery model" and swiftly dominated global blind-test leaderboards.

Unlike traditional diffusion models that handle video and audio separately, Happy Horse 1.0 is built on a **15-billion-parameter unified 40-layer single-stream "sandwich" Transformer**. It processes text, image, video, and audio tokens in a single shared sequence, enabling native multimodal outputs. 

**Key Technical Capabilities:**
- **Joint Audio/Video Generation:** Generates natively synced dialogue, ambient sound, and Foley in one single forward pass without requiring post-processing or a separate audio pipeline.
- **Multilingual Lip-Sync:** Phoneme-level lip synchronization across 7 languages (English, Mandarin, Cantonese, Japanese, Korean, German, and French) with an ultra-low 14.60% Word Error Rate.
- **Blazing Fast Inference:** Features DMD-2 distillation requiring only 8 denoising steps (no CFG needed), delivering 1080p cinematic video in ~38 seconds on a single NVIDIA H100 GPU.
- **Multi-Shot Storytelling:** Maintains persistent character identity, smooth motion, and consistent scene transitions automatically.

## News
- **2026-04-08:** HappyHorse-1.0 abruptly appeared on the Artificial Analysis Video Arena leaderboard, bypassing heavyweights like Seedance 2.0 and Kling 3.0 to hit #1 globally in both T2V and I2V.
- **2026-04-08:** Multiple creators reported unprecedented multi-shot consistency, human-centric motion, and unified multimodal control. 
- **2026-04-08:** Community members warned about mislabeled clips and suggested verifying sources before comparing quality, given its initial anonymous launch.

## Leaderboard Data

Top of the Artificial Analysis leaderboard (no audio categories), April 2026:

| Rank | Model | T2V Elo | I2V Elo | API Available | Released |
|---|---|---:|---:|---|---|
| #1 | HappyHorse-1.0 | **1333** | **1392** | No (Open Source) | Apr 2026 |
| #2 | Seedance 2.0 720p | 1273 | - | No public API | Mar 2026 |
| #3 | SkyReels V4 | 1245 | - | Yes ($7.20/min) | Mar 2026 |
| #4 | Kling 3.0 1080p Pro | 1241 | - | Yes ($13.44/min) | Feb 2026 |
| #5 | PixVerse V6 | 1240 | - | Yes ($5.40/min) | Mar 2026 |

## Prompts & Sample Results

### 1) Cave Flashlight Cinematic

```text
A flashlight beam exploring a cave system, illuminating wet limestone formations. The light catches crystalline calcite deposits that glitter and flash. Where the beam passes through shallow standing water, it creates bright caustic patterns on the submerged floor. Stalactites cast long, swinging shadows as the flashlight moves. Audio: Dripping water echoing, footsteps on wet rock, breathing in enclosed space.
```

<video src="https://github.com/user-attachments/assets/37892764-d152-4aa0-b778-11c3a38288fc" controls width="720"></video>

### 2) Graduation Banner Chaos

```text
A massive "CONGRATULATIONS GRADUATES" banner being unfurled across a university building by maintenance workers on the roof. The wind catches it mid-unfurl, turning it into a sail that nearly lifts one worker off their feet. Coworkers grab him, everyone laughs, and the banner finally drops into place. Below, students start taking selfies immediately. Audio: Wind gusting, workers shouting and laughing, distant cheering.
```

<video src="https://github.com/user-attachments/assets/b34c99c2-8009-45b7-b67b-528abe1bae44" controls width="720"></video>

### 3) Additional Community Samples (No Public Prompt Text)

These are useful output references where full prompt text was not publicly shared.

- Benchmark matchup reel

<video src="https://github.com/user-attachments/assets/f1e9c5db-9672-4c77-bc4c-8391395d36ff" controls width="720"></video>

- Sample set A

<video src="https://github.com/user-attachments/assets/c439a7f6-4f1b-45ae-8de9-b64bdbf37b74" controls width="720"></video>

- Sample set B

<video src="https://github.com/user-attachments/assets/80ebd7e4-d970-4fcd-9221-5ab2185ec32f" controls width="720"></video>

- Sample set C

<video src="https://github.com/user-attachments/assets/42882658-f168-489c-a7f8-927964f9bb56" controls width="720"></video>

- HappyHorse vs Seedance

<video src="https://github.com/user-attachments/assets/10a2f25a-ad95-45f9-abd5-7acee9832173" controls width="720"></video>

- Community sample (CN)

<video src="https://github.com/user-attachments/assets/a0e70cf0-b564-4a61-91ff-cc6cc88209c3" controls width="720"></video>

- Community sample (multi-shot)

<video src="https://github.com/user-attachments/assets/0d0b701b-2032-4e89-8e30-6abf883b8d03" controls width="720"></video>

## Resources

- [Happy Horse Official Website](https://happyhorseone.com)
- [Happy Horse GitHub](https://github.com/happy-horse/happyhorse-1)
- [Happy Horse Technical Report](https://happyhorseone.com/report)
- [Happy Horse Demo](https://happyhorseone.com/demo)

## Contributing

Contributions are welcome.

Please include:

- Prompt text (if available)
- One short description of the intended effect
- Sample output (video/image)
- Source attribution
