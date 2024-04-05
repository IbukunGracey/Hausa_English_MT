# A Transformer Based Translation Model for Hausa Language using Pretrained Models 

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

### Limitations and bias
This model is limited by its training dataset. This may not generalize well for all use cases in different domains. Also the Bleu score can be improved on, if some of the hyper-parameters are tuned. We used 3 epoch and 2 beams due to the computational resources available at the time. As such, more work can be done to improve the model.

### Benefits/Recommendations
Using pre-trained model is highly efficient compared to training the model from scratch, as the later can be more time consuming and costly with respect to time and computational resorces.

### Citation

@inproceedings{adelani-etal-2022-thousand,
    title = "A Few Thousand Translations Go a Long Way! Leveraging Pre-trained Models for {A}frican News Translation",
    author = "Adelani, David  and
      Alabi, Jesujoba  and
      Fan, Angela  and
      Kreutzer, Julia  and
      Shen, Xiaoyu  and
      Reid, Machel  and
      Ruiter, Dana  and
      Klakow, Dietrich  and
      Nabende, Peter  and
      Chang, Ernie  and
      Gwadabe, Tajuddeen  and
      Sackey, Freshia  and
      Dossou, Bonaventure F. P.  and
      Emezue, Chris  and
      Leong, Colin  and
      Beukman, Michael  and
      Muhammad, Shamsuddeen  and
      Jarso, Guyo  and
      Yousuf, Oreen  and
      Niyongabo Rubungo, Andre  and
      Hacheme, Gilles  and
      Wairagala, Eric Peter  and
      Nasir, Muhammad Umair  and
      Ajibade, Benjamin  and
      Ajayi, Tunde  and
      Gitau, Yvonne  and
      Abbott, Jade  and
      Ahmed, Mohamed  and
      Ochieng, Millicent  and
      Aremu, Anuoluwapo  and
      Ogayo, Perez  and
      Mukiibi, Jonathan  and
      Ouoba Kabore, Fatoumata  and
      Kalipe, Godson  and
      Mbaye, Derguene  and
      Tapo, Allahsera Auguste  and
      Memdjokam Koagne, Victoire  and
      Munkoh-Buabeng, Edwin  and
      Wagner, Valencia  and
      Abdulmumin, Idris  and
      Awokoya, Ayodele  and
      Buzaaba, Happy  and
      Sibanda, Blessing  and
      Bukula, Andiswa  and
      Manthalu, Sam",
    booktitle = "Proceedings of the 2022 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies",
    month = jul,
    year = "2022",
    address = "Seattle, United States",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2022.naacl-main.223",
    doi = "10.18653/v1/2022.naacl-main.223",
    pages = "3053--3070",
    abstract = "Recent advances in the pre-training for language models leverage large-scale datasets to create multilingual models. However, low-resource languages are mostly left out in these datasets. This is primarily because many widely spoken languages that are not well represented on the web and therefore excluded from the large-scale crawls for datasets. Furthermore, downstream users of these models are restricted to the selection of languages originally chosen for pre-training. This work investigates how to optimally leverage existing pre-trained models to create low-resource translation systems for 16 African languages. We focus on two questions: 1) How can pre-trained models be used for languages not included in the initial pretraining? and 2) How can the resulting translation models effectively transfer to new domains? To answer these questions, we create a novel African news corpus covering 16 languages, of which eight languages are not part of any existing evaluation dataset. We demonstrate that the most effective strategy for transferring both additional languages and additional domains is to leverage small quantities of high-quality translation data to fine-tune large pre-trained models.",
}
