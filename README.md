# Automatic Speech Recognition (ASR) - DeepSpeech Swiss German

_This is the project for the paper [LTL-UDE at Low-Resource Speech-to-Text Shared Task : Investigating Mozilla DeepSpeech in a low-resource setting]() published at [SWISSTEXT 5th and KONVENS 2020](https://swisstext-and-konvens-2020.org/)._

This project aims to develop a working Speech to Text module using [Mozilla DeepSpeech](https://github.com/mozilla/DeepSpeech), which can be used for any Audio processing pipeline. [Mozillla DeepSpeech](https://github.com/mozilla/DeepSpeech) is a state-of-the-art open-source automatic speech recognition (ASR) toolkit. DeepSpeech is using a model trained by machine learning techniques based on [Baidu's Deep Speech](https://gigaom2.files.wordpress.com/2014/12/deep_speech3_12_17.pdf) research paper. Project DeepSpeech uses Google's TensorFlow to make the implementation easier.

<p align="center">
	<img src="media/deep-speech-v3.png" align="center" title="DeepSpeech v0.5.0" />
</p>


## Important Links:

**Paper:** 

**DeepSpeech-API:** https://github.com/AASHISHAG/DeepSpeech-API

This Readme is written for [DeepSpeech v0.6.0](https://github.com/mozilla/DeepSpeech/releases/tag/v0.6.0). Refer to [Mozillla DeepSpeech](https://github.com/mozilla/DeepSpeech) for lastest updates.

## Contents

1. [Requirements](#requirements)
2. [Speech Corpus](#speech-corpus)
3. [Language Model](#language-model)
4. [Training](#training)
5. [Hyper-Paramter Optimization](#hyper-paramter-optimization)
6. [Results](#results)
7. [Trained Models](#trained-models)
8. [Acknowledgments](#acknowledgments)
9. [References](#references)

### Requirements

#### Installing Python bindings

```
virtualenv -p python3 deepspeech-german
source deepspeech-german/bin/activate
pip3 install -r python_requirements.txt
```

#### Mozilla DeepSpeech

```
$ git clone https://github.com/mozilla/DeepSpeech.git
$ cd DeepSpeech
$ git checkout v0.6.0
$ docker build -t deepspeech_v0.6.0 .
$ docker run -d -it --name deepspeech_v0.6.0 --mount  type=bind,source="$(pwd)",target=/root deepspeech_v0.6.0
$ docker exec -it deepspeech_v0.6.0 /bin/bash
```

### Speech Corpus

**1. _English_**
* [LibriSpeech](http://www.openslr.org/12) ~1000h 
* [Mozilla Common Voice](https://voice.mozilla.org/) ~1488h

**1. _German_**
* [Mozilla Common Voice](https://voice.mozilla.org/) ~454h
* [Mailabs](https://www.caito.de/2019/01/the-m-ailabs-speech-dataset/) ~233h
* [German Distant Speech Corpus (TUDA-De)](https://www.inf.uni-hamburg.de/en/inst/ab/lt/resources/data/acoustic-models.html) ~184h
* [Voxforge](http://www.voxforge.org/home/forums/other-languages/german/open-speech-data-corpus-for-german) ~57h

**1. _Swiss-German_**
* [ArchiMob](https://www.spur.uzh.ch/en/departments/research/textgroup/ArchiMob.html) ~57h
* [SwissText](https://swisstext-and-konvens-2020.org/low-resource-speech-to-text/) ~70h

https://github.com/AASHISHAG/archimob-swissgerman-deepspeech-importer

## Acknowledgments
* [Prof. Dr.-Ing. Torsten Zesch](https://www.ltl.uni-due.de/team/torsten-zesch) - Co-Author
 
## References
If you use our findings/scripts in your academic work, please cite:
```

```
