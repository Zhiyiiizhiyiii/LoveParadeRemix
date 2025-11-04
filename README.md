# Meet Her at the Love Parade (EarSketch Remix)

This project is a remix of *Alfons – Meet Her at the Love Parade*, recreated using **EarSketch**.  
The goal was to blend the original EDM rhythm with a **hardstyle-inspired drop** while experimenting with filters, risers, and vocal layers.

## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Features](#features)
* [Screenshots](#screenshots)
* [Setup](#setup)
* [Usage](#usage)
* [Project Status](#project-status)
* [Room for Improvement](#room-for-improvement)
* [Acknowledgements](#acknowledgements)
* [Contact](#contact)

## General Information
This project was created as part of a **music coding assignment** using **EarSketch**, a Python-based platform that allows musicians to create compositions through code.  
The remix draws inspiration from *Alfons – Meet Her at the Love Parade*, aiming to merge EDM and hardstyle elements while exploring creative coding techniques such as automation, layering, and sound modulation.

**Purpose:**  
To experiment with the fusion of electronic dance music and hardstyle elements using programming logic.  
It showcases how code can be used to structure rhythm, apply effects, and manipulate sound in real time.  

**Why this project?**  
Traditional DAWs have limitations in learning environments; EarSketch provides an opportunity to focus on *structure, rhythm, and pattern logic* — making it ideal for a creative remix assignment.

## Technologies Used
- Python 3 (EarSketch syntax)
- EarSketch digital audio coding platform  
- EarSketchsample libraries and my own audio imported into the platform
- Audio Effects: Reverb, Distortion, Filter Sweep, Volume Automation

## Features
- Custom intro vocal integration and atmospheric layering  
- Dynamic tempo (150 BPM) for high-energy EDM pacing  
- Reverb-enhanced vocal drops and riser automation  
- Hardstyle kick and reverse bass section with distortion  
- Filter sweeps to create tension and release moments  

## Setup
1. Open **[EarSketch](https://earsketch.gatech.edu/earsketch2/)** in your browser.  
2. Copy the contents of `meet_her_remix.py` into the EarSketch code editor.  
3. Click **“Run”** to generate and preview your track.  
4. Adjust code sections or loops to remix further.  

> No installation required — EarSketch runs entirely online.

## Project Overview
Using the EarSketch Python library, I built this remix by layering beats, synths, and effects to emulate festival energy while maintaining an original structure.  
The track transitions from an intro vocal and soft synth section into a hardstyle drop featuring distorted kicks, reverse bass, and sweeping risers.


## Key Features
- Intro vocals and atmospheric buildup  
- Filter automation and reverb effects for transitions  
- Hardstyle-inspired drop with distortion and bass layering  
- Custom audio samples integrated (`SHARONZYZY_I_KNOW_I_SHOULD_SLEEP_VOCAL_`,`SHARONZYZY_INTRO_ALFONS`)

## Usage
This remix uses standard EarSketch functions for music arrangement:  

```python
from earsketch import *
init()
setTempo(150)

# Main Beats and Rhythm
kick = YG_TECHNO_SYNTH_BASS_1
bass = YG_TECHNO_BASS_1
synth_stab = YG_TECHNO_SYNTH_1
hihat = YG_EDM_HIHAT_1
clap = YG_EDM_CLAP_3
lead = RD_EDM_ELECTRICLEAD_1
riser = RD_EDM_SFX_RISER_1
vocal = SHARONZYZY_I_KNOW_I_SHOULD_SLEEP_VOCAL_
intro_audio = SHARONZYZY_INTRO_ALFONS

# Hardstyle track
hardstyle_kick = YG_EDM_KICK_1  
hardstyle_bass = TECHNO_LOOP_PART_002 
hardstyle_lead = RD_EDM_ANALOGLEAD_5  
reverse_bass = RD_TRAP_BASSDROPS_1  

# INTRO AUDIO 
fitMedia(intro_audio, 10, 1, 9.6)

# INTRO SECTION 
fitMedia(kick, 1, 9.6, 13.6)
fitMedia(hihat, 2, 9.6, 13.6)
fitMedia(synth_stab, 3, 11.6, 13.6)

# Main track
fitMedia(kick, 1, 13.6, 17.6)
fitMedia(bass, 4, 13.6, 17.6)
fitMedia(hihat, 2, 13.6, 17.6)
fitMedia(clap, 5, 15.6, 17.6)
fitMedia(synth_stab, 3, 13.6, 17.6)
fitMedia(lead, 6, 15.6, 17.6)

# Buildup
fitMedia(kick, 1, 17.6, 20.6)
fitMedia(hihat, 2, 17.6, 20.6)
fitMedia(clap, 5, 17.6, 20.6)
fitMedia(riser, 7, 18.6, 21.6)

# Riser volume up
setEffect(7, VOLUME, GAIN, -20, 18.6, 6, 21.6)

# High-pass filter sweep 
setEffect(7, FILTER, FILTER_FREQ, 200, 18.6, 10000, 21.6)

# PAUSE & VOCAL DROP (measures 21.6-23.6)
fitMedia(vocal, 8, 21.6, 23.6)
# Add reverb to vocal only
setEffect(8, REVERB, REVERB_TIME, 2000)

# HARDSTYLE DROP (measures 23.6-31.6)
fitMedia(hardstyle_kick, 1, 23.6, 31.6)
fitMedia(hardstyle_bass, 4, 23.6, 31.6)
fitMedia(reverse_bass, 9, 23.6, 31.6)
fitMedia(hardstyle_lead, 6, 23.6, 31.6)
fitMedia(clap, 5, 23.6, 31.6)
fitMedia(hihat, 2, 23.6, 31.6)# Add hihat pattern

# EDM distortion and compression
setEffect(1, DISTORTION, DISTO_GAIN, 20)
setEffect(4, DISTORTION, DISTO_GAIN, 15)

# Volume adjust
setEffect(1, VOLUME, GAIN, 3)
setEffect(4, VOLUME, GAIN, 2)

finish()
```

## Project Status
Project is: _complete_ 

## Room for Improvement
Areas for improvement:

- Add smoother transitions between the buildup and hardstyle drop
- Improve overall mix balance (reduce distortion overlap in lower frequencies)
- Enhance vocal clarity and reverb tail precision
  
To do:

- Feature to be added 1: Experiment with dynamic tempo changes during the riser section
- Feature to be added 2: Incorporate a secondary breakdown with ambient synths or melodic bridge
- Feature to be added 3: Expand automation for filter and delay effects for more tension


## Acknowledgements
Give credit here.
- This project was inspired by Alfons - Meet Her at the Love Parade https://youtu.be/H3S8WguS0iw?si=OAWTsdKsi9v_vaXN
- This project was based on tutorial on EarSketch Website.

## Contact
Created by [@sharonchaizhiyi@student.uts.edu.au - feel free to contact me!
