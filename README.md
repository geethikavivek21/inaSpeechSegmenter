# 🎧 Audio Segmentation with inaSpeechSegmenter

This guide walks you through using the [inaSpeechSegmenter](https://github.com/ina-foss/inaSpeechSegmenter) tool for segmenting an audio file into speech, music, and noise sections.

---

## Set Up Your Environment
Before running segmentation, ensure your Anaconda environment is set up.
```bash
conda create --name speech_seg python=3.8 -y
conda activate speech_seg
```
Install the required dependencies:
```bash
conda install -c conda-forge numpy scipy matplotlib ffmpeg requests -y
pip install torch tensorflow inaSpeechSegmenter
```
---

## Navigate to Your Audio File Directory
Change directory to where your MP3 file and Segmenter.py file is stored:
```bash
cd /home/ssl/Downloads/
```

---

## Convert MP3 to WAV
inaSpeechSegmenter works best with WAV files. Convert the MP3:
```bash
ffmpeg -i "Top Singer _ Musical Reality Show _ Flowers _ Ep# 09.mp3" "top_singer.wav"
```

---


## Segment the Audio Using inaSpeechSegmenter

```bash
python Segmenter.py -i "/home/ssl/Downloads/top_singer.wav" -o ~/Downloads/ina_output


```

---

## Open the CSV to Check Labels

```bash
cat ~/speech_seg_project/top_singer.csv

```

---

## Import Labels into Sonic Visualiser
If Sonic Visualiser is installed, run:

```bash
sonic-visualiser


```
In Sonic Visualiser:

File → Open → select top_singer.wav

Layer → Import Annotation Layer → From CSV File → select top_singer.csv

You’ll see labeled segments aligned with the waveform.

## Optional: Install Sonic Visualiser
If not already installed:

```bash
sudo apt update
sudo apt install sonic-visualiser -y


```

---
