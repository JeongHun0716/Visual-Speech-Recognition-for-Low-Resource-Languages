# Visual-Speech-Recognition-for-Low-Resource-Languages
Visual Speech Recognition For Low-Resource Languages with Automatic Labels From Whisper Model

We will provide all VSR models, training code, and inference code for low-resource languages soon.

We release the automatic labels of the four low-resource languages([French](https://github.com/JeongHun0716/Visual-Speech-Recognition-for-Low-Resource-Languages/tree/main/French), [Italian](https://github.com/JeongHun0716/Visual-Speech-Recognition-for-Low-Resource-Languages/tree/main/Italian), [Portuguese](https://github.com/JeongHun0716/Visual-Speech-Recognition-for-Low-Resource-Languages/tree/main/Portuguese), and [Spanish](https://github.com/JeongHun0716/Visual-Speech-Recognition-for-Low-Resource-Languages/tree/main/Spanish)). 

To generate the automatic labels, we identify the languages of all videos in VoxCeleb2 and AVSpeech, and then the transcription (automatic labels) is produced by the pretrained ASR model. In this project, we use a "[whisper/large-v2](https://github.com/openai/whisper)" model to conduct these processes.  

## Dataset preparation
Multilingual TEDx(mTEDx), VoxCeleb2, and AVSpeech Datasets. 
  1. Download the mTEDx dataset from the [mTEDx link](https://www.openslr.org/100) of the official website.
  2. Download the VoxCeleb2 dataset from the [VoxCeleb2 link](https://www.robots.ox.ac.uk/~vgg/data/voxceleb/vox2.html) of the official website.
  3. Download the AVSpeech dataset from the [AVSpeech link](https://looking-to-listen.github.io/avspeech/) of the official website.

When you are interested in training the model for a specific target language VSR, we recommend using language-detected files (e.g., [link](https://github.com/JeongHun0716/Visual-Speech-Recognition-for-Low-Resource-Languages/blob/main/French/AVSpeech-Fr/train.txt) provided in this project instead of video lists of the AVSpeech dataset provided on the official website to reduce the dataset preparation time. Because of the huge amount of AVSpeech dataset, it takes a lot of time.

## Preprocessing 
After downloading the datasets, you should detect the facial landmarks of all videos and crop the mouth region using these facial landmarks. We recommend you preprocess the videos following [Visual Speech Recognition for Multiple Languages](https://github.com/mpc001/Visual_Speech_Recognition_for_Multiple_Languages).  

  
## Training the Model
The training code is available soon.


## Inference
The inference code is available soon.


## Models

<details open>

<summary>mTEDx Fr</summary>

| Model         | Training Datasets  | Training data (h)  |  WER [%]   |    Target Languages     |
|--------------|:----------|:------------------:|:----------:|:------------------------:|
| best_ckpt.pt |       mTEDx        |        85           |    65.25    | Fr  |
| best_ckpt.pt |        mTEDx + VoxCeleb2            |        209          |    60.61    | Fr  |
| best_ckpt.pt |        mTEDx + VoxCeleb2 + AVSpeech       |        331         |    58.30    | Fr  |



<details open>

<summary>mTEDx It</summary>

| Model         | Training Datasets  | Training data (h)  |  WER [%]   |    Target Languages     |
|--------------|:----------|:------------------:|:----------:|:------------------------:|
| best_ckpt.pt |       mTEDx        |        46           |    60.40    | It  |
| best_ckpt.pt |        mTEDx + VoxCeleb2            |        84          |    56.48    | It  |
| best_ckpt.pt |        mTEDx + VoxCeleb2 + AVSpeech       |        152         |    51.79    | It  |

<details open>

<summary>mTEDx Es</summary>

| Model         | Training Datasets  | Training data (h)  |  WER [%]   |    Target Languages     |
|--------------|:----------|:------------------:|:----------:|:------------------------:|
| best_ckpt.pt |       mTEDx        |        72           |    59.91    | Es  |
| best_ckpt.pt |        mTEDx + VoxCeleb2            |        114          |    54.05    | Es  |
| best_ckpt.pt |        mTEDx + VoxCeleb2 + AVSpeech       |        384         |    45.71    | Es  |



<details open>

<summary>mTEDx Pt</summary>

| Model         | Training Datasets  | Training data (h)  |  WER [%]   |    Target Languages     |
|--------------|:----------|:------------------:|:----------:|:------------------------:|
| best_ckpt.pt |       mTEDx        |        82           |    59.45    | Pt  |
| best_ckpt.pt |        mTEDx + VoxCeleb2            |        91          |    58.82    | Pt  |
| best_ckpt.pt |        mTEDx + VoxCeleb2 + AVSpeech       |        420         |    47.89    | Pt  |
