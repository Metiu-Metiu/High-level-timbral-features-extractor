# Freesound One-Shot Percussive Sounds Dataset


This dataset contains 10254 one-shot (single event) percussive sounds from Freesound.org and the corresponding timbral analysis. These were used to train the generative model for "Neural Percussive Synthesis Parameterised by High-Level Timbral Features". 

## Dataset Construction

To collect this dataset, the following steps were performed:

* Freesound was queried with words associated with percussive instruments, such as "percussion", "kick", "wood" or "clave". Only sounds with less than one second of [effective duration](https://essentia.upf.edu/reference/std_EffectiveDuration.html) were selected.

* This stage retrieved some audio clips that contained multiple sound events or that were of low quality.
Therefore, we listened to all the retrieved sounds and manually discarded the sounds presenting one of these characteristics. For this, the [percussive-annotator](https://github.com/xavierfav/percussive-annotator) was used.

* The sounds were then cut or padded to have 1-second length, normalized and downsampled to 16kHz.

* Finally, the sounds were analyzed with the [AudioCommons Extractor](https://github.com/AudioCommons/ac-audio-extractor), to obtain the AudioCommons timbral descriptors. This information is contained in the 'analysis' folder.


## Dataset Organisation

The dataset contains two folders and two files in the root directory:

* 'one_shot_percussive_sounds' encloses the pre-processed audio files. These are named '<freesound_sound_id>.wav'

* 'analysis' holds the AudioCommons analysis files for each of the sounds in the dataset. This analysis is stored as a .json file, named '<freesound_sound_id>_analysis.json', with a key for each of the features extracted.

* Two more files are present in the root directory of the dataset: this 'README' and the 'licenses.json'. The latter one is a '.json' file containing the name, the username of the uploader and the license for each of the sounds in the dataset.


## Authors and Contact

This dataset was developed by António Ramires, Pritish Chadna, Xavier Favory, Emilia Gómez and Xavier Serra.

Any questions related to this dataset please contact:

António Ramires

antonio.ramires@upf.edu

aframires@gmail.com


## References

Please cite this paper if you use this dataset:

```

@inproceedings{ramires2020,
    author = "Antonio Ramires and Pritish Chandna and Xavier Favory and Emilia Gómez and Xavier Serra",
    title = "Neural Percussive Synthesis Parametrerised by High-Level Timbral Features",
    booktitle = "Proc. of the IEEE Int. Conf. on Acoustics, Speech and Signal Processing (ICASSP)",
    year = "2020"

}

```


## Acknowledgements

This work has received funding from the European Union's Horizon 2020 research and innovation programme under the Marie Skłodowska-Curie grant agreement No. 765068 (MIP-Frontiers).

This work has received funding from the European Union's Horizon 2020 research and innovation programme under grant agreement No. 770376 (TROMPA).

<img src="https://upload.wikimedia.org/wikipedia/commons/b/b7/Flag_of_Europe.svg" height="64" hspace="20">


