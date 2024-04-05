# Hausa_English_MT

This repository contains a machine translation model that translates english to hausa languages. This was trained using pre-trained models MBART and M2M100 - "facebook/m2m100_418M" like architectures from [Masakhane](https://github.com/masakhane-io/lafand-mt) git repo and fine-tuned on [MAFAND_MT](https://github.com/masakhane-io/lafand-mt/tree/main/data/json_files) datasets. 

### Model description
mt-ha-en is a machine translation model from English language to Hausa language based on a fine-tuned MBART-base model. It establishes a strong baseline for automatically translating texts from English to Hausa.

### Training data
This model was fine-tuned  on [MAFAND_MT](https://github.com/masakhane-io/lafand-mt/tree/main/data/json_files)  en_hau datasets with 

* Train data - 5865 
* Test data- 1500
* Validation data - 1300

### Training procedure
This model was trained on Colab - NVIDIA V100 GPU

**Eval results on Test set (BLEU score)**
Fine-tuning the model achieves 12.16 BLEU on the test set and 12.18 BLEU on the validation set with a training runtime of 37 mins and prediction runtime of approx 10mins



