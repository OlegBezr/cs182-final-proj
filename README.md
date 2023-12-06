## Using pre-trained models

Use use_saved_model.ipynb together with our saved models from https://drive.google.com/drive/folders/1ffTch3jfYCOGON4Tefq1nxdoSWEdg8A1?usp=drive_link to generate different texts. All the dependencies are listed in **saved_req.txt**.

## Training your own model

Use one of the following notebooks to train your own model. We would typically run them on Google Colab. 
- **baseline.ipynb** - another baseline model using pretrained GPT-2 and finetuned by additional training on combined_data.csv dataset
- **keras_LoRA.ipynb** - baseline GPT-2 using Keras and LoRA finetuned GPT2. The baseline version needs to be trained on Colab Pro due to larger RAM requirement. Training data is parsed from **combined_data.cvs**. 
- **pytorch_articles.ipynb** - this notebook contains the code for training the model on the articles from **final_labels_MBIC.csv** file. The model is trained using Google Colab Pro. We have existing pre-training models for this notebook, so you can skip the training part and use the pre-trained model to generate texts.
- **pytorch_LoRA.ipynb** - New LoRA model implemented with PyTorch and Hugging Face.