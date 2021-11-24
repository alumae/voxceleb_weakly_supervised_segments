This repository contains speaker segmentations for the VoxCeleb1 and VoxCeleb2 datasets, generated using weakly supervised training, as described in the paper referenced below.

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


For more information, see the paper [_Training Speaker Recognition Models with Recording-level Labels_](doc/alumae2018training.pdf) in the proceedings of SLT 2018.

BibTex reference for the paper:

    @inproceedings{alumae2018training,
      author={Tanel Alum\"{a}e},
      title={Training Speaker Recognition Models with Recording-level Labels},
      bootlitle={IEEE Workshop on Spoken Language technology (SLT)},
      year=2018
    }

