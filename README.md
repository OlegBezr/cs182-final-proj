## Using pre-trained models

Use use_saved_model.ipynb together with our saved models from https://drive.google.com/drive/folders/1ffTch3jfYCOGON4Tefq1nxdoSWEdg8A1?usp=drive_link to generate different texts. All the dependencies are listed in **saved_req.txt**.

## Training your own model

Use one of the following notebooks to train your own model. We would typically run them on Google Colab. All the dependencies are listed in **train_req.txt**. We use just the **combined_data.csv** file for model training. You might upload it to your Google Drive and mount it to the Colab notebook or just upload it directly to the notebook (then you need to change the path in the notebook).

With Google Colab pro V100 runtime, 1 epoch of training takes about 50 seconds.

With Google Colab free T4 runtime, 1 epoch of training takes about 2 minutes.

Running the model on CPU is highly not recommended. 1 epoch of training on MacBook Pro M1 takes about 60 minutes.


- **baseline.ipynb** - another baseline model using pretrained GPT-2 and finetuned by additional training on combined_data.csv dataset
- **keras_LoRA.ipynb** - baseline GPT-2 using Keras and LoRA finetuned GPT2. The baseline version needs to be trained on Colab Pro due to larger RAM requirement. Training data is parsed from **combined_data.cvs**. 
- **pytorch_baseline.ipynb** - this notebook contains the code for training the model on the articles from **final_labels_MBIC.csv** file. The model is trained using Google Colab Pro. We have existing pre-training models for this notebook, so you can skip the training part and use the pre-trained model to generate texts.
- **pytorch_LoRA.ipynb** - New LoRA model implemented with PyTorch and Hugging Face.