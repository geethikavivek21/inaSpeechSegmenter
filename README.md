# 🎧 Audio Segmentation with inaSpeechSegmenter

This guide walks you through using the [inaSpeechSegmenter](https://github.com/ina-foss/inaSpeechSegmenter) tool for segmenting an audio file into speech, music, and noise sections.

---

## STEP 1: Create Conda Environment

```bash
conda create -n audio_env python=3.9 -y
```

---

## STEP 2: Activate the Environment

```bash
conda activate audio_env
```

---

## STEP 3: Install inaSpeechSegmenter

```bash
pip install inaSpeechSegmenter

```

---


## STEP 4: Download a Sample Audio File

```bash
wget https://file-examples.com/wp-content/uploads/2017/11/file_example_WAV_1MG.wav -O test.wav


```

---

## STEP 5: Run the Segmentation Script
Make sure you're inside the environment and the folder containing segmentation.py.

```bash
python segmentation.py

```

---

## STEP 6: Visualize in Sonic Visualiser
If Sonic Visualiser is installed, run:

```bash
sonic-visualiser test.wav


```
Then, in Sonic Visualiser:

Go to Layer → Import Annotation Layer → From CSV File

Select segments.csv

You will see speech/music/noise segments overlaid on the waveform!


## Optional: Install Sonic Visualiser
If not already installed:

```bash
sudo apt update
sudo apt install sonic-visualiser -y


```

---



