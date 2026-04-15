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

Last updated on 2026-04-15

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

### 3) Flower Time-Lapse Continuity

```text
A flower blooming and wilting over two weeks, one photo per day. Same vase, same window, same angle. Light changes with weather. Audio: Quiet domestic.
```

Source: [Brent Lynch](https://x.com/BrentLynch/status/2039462980715524457). 

<video src="https://github.com/user-attachments/assets/de6a8b9d-55a0-400e-9356-b5003c936a3f" controls width="720"></video>


### 4) 1990s Action Cartoon Firebending

```text
1990s action cartoon style. A young martial artist performs a firebending kata. The flames are hand-drawn with thick outlines and bold orange-yellow gradients. Dynamic camera swoops around the character. The fighting stance shows anime influence while maintaining Western animation proportions. Smoke effects use the signature layered look of the era. Audio: Whooshing fire, martial arts grunts, dramatic percussion.
```

Source: [Brent Lynch](https://x.com/BrentLynch/status/2039465595041890540)

<video src="https://github.com/user-attachments/assets/21fea2ed-ecc9-4120-8ac9-e222a62db5a9" controls width="720"></video>

### 5) Cyberpunk Android Repair Bay

```text
Cyberpunk anime style (aesthetic). A female android sits in a maintenance chair as robotic arms repair her damaged arm. The skin panel is open, revealing intricate servos and fiber-optic cables beneath. Her eyes are blank and unfocused during the repair cycle. Neon city lights filter through rain-streaked windows. Cool blue and pink color palette with high contrast shadows. Audio: Mechanical whirring, the hum of electronics, distant city ambience.
```

Source: [Brent Lynch](https://x.com/BrentLynch/status/2039465595041890540)

<video src="https://github.com/user-attachments/assets/bcbf409c-09c3-472c-a5db-e09c419aebf6" controls width="720"></video>

### 6) Voice Assistant Day-In-The-Life

```text
A time-lapse of a family using a home voice assistant throughout the day. From setting morning alarms, playing music, checking the weather, and controlling smart lights, the product integrates seamlessly into their daily life.
```

Source: [Justine Moore](https://x.com/venturetwins/status/2041556160055333180)

<video src="https://github.com/user-attachments/assets/c1b705b4-6231-4d1c-a5f0-5f3eba59b91e" controls width="720"></video>

### 7) Tracking Shot Street Escape

```text
TRACKING SHOT follows her from behind as she runs through the street. Sari fabric flows and trails behind her, catching the wind. CLOSE-UP on bare feet hitting the ground. Fabric billowing. She glances back. Keeps running. Determined. Footsteps, fabric whooshing, and heavy breathing.
```

Source: [Brent Lynch](https://x.com/BrentLynch/status/2042316613329043472)

<video src="https://github.com/user-attachments/assets/d2374d19-7c89-452f-8e3a-7483806f5cd4" controls width="720"></video>

### 8) Additional Community Samples (No Public Prompt Text)

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

- Wildminder: HappyHorse-1.0 vs All

<video src="https://github.com/user-attachments/assets/c8ee9ee9-032a-478c-aed5-64745f6f8b44" controls width="720"></video>

- GENEL: HappyHorse vs Seedance 2.0

<video src="https://github.com/user-attachments/assets/3f070c3a-6910-4fc6-9cd5-8201ac9e97f4" controls width="720"></video>

- GMI Cloud: Seedance 2.0 Comparison Challenge

<video src="https://github.com/user-attachments/assets/9b632903-cdf4-4507-b0af-d436aa1c6a72" controls width="720"></video>

## Resources

- [Happy Horse Official Website](https://happyhorseone.com)

## Contributing

Contributions are welcome.

Please include:

- Prompt text (if available)
- One short description of the intended effect
- Sample output (video/image)
- Source attribution
