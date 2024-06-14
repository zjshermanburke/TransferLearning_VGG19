# FineTuningBERT

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![LinkedIn][linkedin-shield]][linkedin-url]

 Project is the transfer learning of VGG-19 on 525 Bird Species. 

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>

## About The Project

Fine-tuning DistilBERT, BERT, and Large BERT cased models for sentiment analysis of financial data and creating a user interface that allows a user to select one of the models and enter a sentence for analysis.

### Built With
* [![Tensorflow][Tensorflow.org]][Tensorflow-url]
* [![NumPy][Numpy.com]][NumPy-url]
* [![Pandas][Pandas.org]][Pandas-url]

## Getting Started

### Prerequisites

Required Libraries/Frameworks: <br>
Tensorflow ([configured for CUDA](https://www.tensorflow.org/install/pip#windows-native)), Numpy, and Pandas

Required Hardware: <br>
NVidia GPU

### Installation

1. Clone the Repo
```sh
git clone https://github.com/zjshermanburke/TransferLearning_VGG19
```
2. Download the dataset from [Kaggle Birds 525 Species](https://www.kaggle.com/datasets/gpiosenka/100-bird-species)
3. Extract dataset in Data Folder so that the structure follows "Data/train", "Data/valid", "Data/test"


## Usage

Adjust the options in cell below "Establishing Hyperparameters" and modify output layers as desired in cell below "Creating Our Output Layers"

Hyperparameters
```sh
BATCH_SIZE = 64
EPOCHS =50
LEARNING_RATE = 0.0001
IMAGE_SIZE = [224, 224]
```

Output Layers
```sh
K = len(folders)
x = Flatten()(pretrained_model.output)
# x = Dense(1024, activation='relu')(x)
# x = Dense(512, activation='relu')(x)
# x = Dense(256, activation='relu')(x)
x = Dense(K, activation='softmax')(x)
```

## License

Distributed under the Unlicense license. See `LICENSE.txt`for more information.

## Contact

Zachary Sherman-Burke - [LinkedIn](https://www.linkedin.com/in/zachary-sherman-burke-6b7589125) - zjshermanburke@gmail.com

Project Link: [https://github.com/zjshermanburke/TransferLearning_VGG19](https://github.com/zjshermanburke/TransferLearning_VGG19)


## Acknowledgments

* [Kaggle Birds 525 Species](https://www.kaggle.com/datasets/gpiosenka/100-bird-species)
* [Img Shields](https://shields.io)
* [Best ReadMe Template](https://github.com/othneildrew/Best-README-Template)
* [Choose an Open Source License](https://choosealicense.com)

<!-- Markdown Links and Images-->

<!-- GitHub and LinkedIn-->
[contributors-shield]: https://img.shields.io/github/contributors/zjshermanburke/FineTuningBert.svg?style=for-the-badge
[contributors-url]: https://github.com/zjshermanburke/FineTuningBert/graphs/contributors

[forks-shield]: https://img.shields.io/github/forks/zjshermanburke/FineTuningBert.svg?style=for-the-badge
[forks-url]: https://github.com/zjshermanburke/FineTuningBert/network/members

[stars-shield]: https://img.shields.io/github/stars/zjshermanburke/FineTuningBert.svg?style=for-the-badge
[stars-url]: https://github.com/zjshermanburke/FineTuningBert/stargazers

[issues-shield]: https://img.shields.io/github/issues/zjshermanburke/FineTuningBert.svg?style=for-the-badge
[issues-url]: https://github.com/github/issues/zjshermanburke/FineTuningBERT.svg

[linkedin-url]: https://www.linkedin.com/in/zachary-sherman-burke-6b7589125
[linkedin-shield]: https://img.shields.io/badge/LinkedIn-blue.svg?style=for-the-badge&logo=linkedin&colorB=555


<!-- Built With Badges -->

<!-- [HuggingFace.com]: https://img.shields.io/badge/%F0%9F%A4%97Hugging_Face-ffd21e -->
[Tensorflow.org]: https://img.shields.io/badge/TensorFlow-white?style=for-the-badge&logo=tensorflow&style=plastic
[Tensorflow-url]: https://tensorflow.org/

[NumPy.com]: https://img.shields.io/badge/NumPy-white?style=for-the-badge&logo=numpy&logoColor=4584b6&textColor=4584b6&style=plastic
[NumPy-url]: https://numpy.org/

[Pandas.org]: https://img.shields.io/badge/-pandas-05122A?style=flat&logo=pandas
[Pandas-url]: https://pandas.pydata.org/

