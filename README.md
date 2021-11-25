## Introduction

This repository contains speaker segmentations for the VoxCeleb1 and VoxCeleb2 datasets, generated using weakly supervised training, as described in the paper referenced below.

## Why?

Weakly supervised segmentation gives around 3.5 more audio material than the official segmentation,
generated using face recognition and lip sync detection. More data often results in better models.

## How

You need to download two files: one containing the raw unsegmented audio of VoxCeleb1 & VoxCeleb2, and the
definition of the segmentation. Here they are:

  * The audio: http://bark.phon.ioc.ee/voxceleb/voxceleb_unsegmented_audio.tar (*attention*: 1 TB)
  * The Kaldi-style data directory, contraining segmentation information: http://bark.phon.ioc.ee/voxceleb/voxceleb_weakly_supervised_train_datadir.tgz
  
Here is a list of commands to download and unpack (make sure you have around 2.5 TB available at this directory):

    wget -c --retry-connrefused --tries=0 --timeout=5 http://bark.phon.ioc.ee/voxceleb/voxceleb_unsegmented_audio.tar    
    wget -c --retry-connrefused --tries=0 --timeout=5 http://bark.phon.ioc.ee/voxceleb/voxceleb_weakly_supervised_train_datadir.tgz    
    mkdir -p audio
    tar xvf voxceleb/voxceleb_unsegmented_audio.tar -C audio
    tar xvf voxceleb_weakly_supervised_train_datadir.tgz    
    
After completition, you should have a Kaldi-stype data directory `data/voxceleb_weakly_supervised_train/` that contains the segmentation information and points to the downloaded audio files.

## Legalese

The copyright remains with the original owners of the videos. 

We also point out that the distribution of languages, accents, dialects, genders, races and societal factors in this dataset is not representative of the global population. Using this dataset for training and deploying models may thus introduce unintended biases.

### Notice and take down policy

Notice: Should you consider that the distributed audio data contains material that is owned by you and should therefore not be reproduced here, please:

- Clearly identify yourself, with detailed contact data such as an address, telephone number or email address at which you can be contacted.
- Clearly identify the copyrighted work claimed to be infringed.
- Clearly identify the material that is claimed to be infringing and information reasonably sufficient to allow us to locate the material.
- Send the request to [Tanel Alum&auml;e](mailto:tanel.alumae@taltech.ee)

Take down: We will comply to legitimate requests by removing the affected sources from the corpus.


## Remarks

For more information, see the paper [_Training Speaker Recognition Models with Recording-level Labels_](doc/alumae2018training.pdf) in the proceedings of SLT 2018.

BibTex reference for the paper:

    @inproceedings{alumae2018training,
      author={Tanel Alum\"{a}e},
      title={Training Speaker Recognition Models with Recording-level Labels},
      bootlitle={IEEE Workshop on Spoken Language technology (SLT)},
      year=2018
    }

