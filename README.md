# GlobalPointer_NER

## Description:


This code implements the use of the GlobalPointer model to solve the problem of Chinese medical named entity recognition. The model uses a pre-trained BERT model to extract features and uses a CRF layer for sequence labeling. Experimental results show that the model achieves good performance on Chinese medical named entity recognition tasks.

The idea is from [GlobalPointer](https://kexue.fm/archives/8373).
## Environment
+ python 3.8.1
+ pytorch==1.8.1
+ transformer==4.9.2
+ tqdm
+ numpy

## Dataset
The current dataset used in the code is just for demonstration purposes. If you need a more formal dataset, you can download it from [here](https://tianchi.aliyun.com/dataset/dataDetail?dataId=95414#1), or you can use your own dataset.

## Usage:
1. Clone this code repository to your local machine:
```sh
$ git clone https://github.com/hualaobisi/GlobalPointer_NER.git
```
2. Install the required dependencies:

3. Download the pre-trained BERT model and put it into the models directory.

   You can download the chinese-roberta-wwm-ext model from the following websites:

- [Hugging Face](https://huggingface.co/hfl/chinese-roberta-wwm-ext)
- [Google Drive](https://drive.google.com/drive/folders/1dFvF7W1qJc3m6UQYbHvz8lwEg3KjzKQ2)

  After downloading the model, you need to update the "bert_model_path" in the train_CME/predict.CME.py with your own path..

  > Note: the chinese-roberta-wwm-ext model is developed by the Harbin Institute of Technology at iFLYTEK Research.

4. Run the training program:
```sh
$ python train_CME.py
```
5. Run the predicting program:
```sh
$ python predict_CME.py
```
