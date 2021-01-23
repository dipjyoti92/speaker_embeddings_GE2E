# GE2E Speaker Embeddings
This repository is an implementation of Generalized End-to-End Loss for Speaker Verification
paper: [GE2E](https://arxiv.org/abs/1710.10467)

### Requirements

**Python 3.6 +**.

Run `pip install -r requirements.txt` to install the necessary packages.

A GPU is mandatory, but you don't necessarily need a high tier GPU if you only want to use the toolbox.

### Datasets

Ideally, all your datasets are kept under a same directory i.e., <datasets_root>. All prepreprocessing scripts will, by default, output the clean data to a new directory SV2TTS created in your datasets root directory. Inside this directory will be created a directory for the encoder.

For the encoder:

LibriSpeech: train-other-500 (extract as LibriSpeech/train-other-500)
VoxCeleb1: Dev A - D as well as the metadata file (extract as VoxCeleb1/wav and VoxCeleb1/vox1_meta.csv)
VoxCeleb2: Dev A - H (extract as VoxCeleb2/dev)

### Preprocessing and training

python encoder_preprocess.py <datasets_root>
python encoder_train.py my_run <datasets_root>/SV2TTS/encoder

### Generate speaker embeddings

python generate_embeddings.py

## For more details
(https://github.com/CorentinJ/Real-Time-Voice-Cloning)

