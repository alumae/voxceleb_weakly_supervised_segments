This repository contains speaker segmentations for the VoxCeleb1 and VoxCeleb2 datasets, generated using weakly supervised training, as described in the paper referenced below.

In the `voxceleb1` directory, there are two segmentation files:
[One](voxceleb1/voxceleb1_sid_segments) contains the segmentations for training portion of the speaker identification task and the [other](voxceleb1/voxceleb1_sv_segments) for the training portion of the speaker verification task.
Both are in format:

    <fileID> <start> <end> <speaker>
    
In the `voxceleb1+voxceleb2/data.tgz` there are files `voxceleb1+voxceleb2/segments` and `voxceleb1+voxceleb2/utt2spk`. The files are Kaldi-style training data definition files.
The wav file ID in the segments file is in format

    <dataset>#<fileID>
  
E.g.:

    voxceleb2#H0XKvvTYxgo
  
The above means that the wav file corresponds to a YouTube file from the Voxceleb2 dataset, with a YouTube ID `H0XKvvTYxgo`.

Note that the VoxCeleb2 dataset doesn't come with the full audio files, it conly contains the reference audio segments
extracted from the videos. Therefore, it's your task to download the files yourself. Or frop me an e-mail,
I can make the downloaded and extracted audio available online (it's around 1.1 TB).

For more information see the paper [_Training Speaker Recognition Models with Recording-level Labels_](doc/alumae2018training.pdf), to appear in the proceedings of SLT 2018.

BibTex reference for the paper:

    @inproceedings{alumae2018training,
      author={Tanel Alum\"{a}e,
      title={Training Speaker Recognition Models with Recording-level Labels},
      bootlitle={IEEE Workshop on Spoken Language technology (SLT)},
      year=2018
    }

