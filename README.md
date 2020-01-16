<!--

#################################################
### THIS FILE WAS AUTOGENERATED! DO NOT EDIT! ###
#################################################
# file to edit: 99_index.ipynb
# command to build the docs after a change: nbdev_build_docs

-->

# Decoder head

> Exploration of unsupervised translation using fastai and pytorch


Imagine you have trained a language model (LM) to perform some task, say predict the next word or perform sentiment analysis. You freeze the model with removing one piece of information from it - the mapping from embeddings to words.

Can you create a setup in which the mapping from words to embeddings will be learnable? Something that the model could learn utilizing the information encoded in the LM? Surprisingly, the answer is yes. This repository is based on original work by Aza Raskin exploring this idea.

![Decoder Head](https:/files.nuclino.com/files/d6fa05cd-3e8f-4bbe-882c-5a7560d3a06b/c69e3627-d16f-41ce-98e8-5341081201b5.png?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiJkNmZhMDVjZC0zZThmLTRiYmUtODgyYy01YTc1NjBkM2EwNmIiLCJwdXJwb3NlIjoiZ2V0LWZpbGUiLCJleHAiOjE1NzUwNzg5MDcsImlhdCI6MTU3NTA3NTMwN30.lEtc8pcKJ5EYIHNXNBt3j-iYjknIrLf_l1pHOf0lZX4&preview=l)

Please read this for a more full description of a [potential Decoder Head architecture](https://share.nuclino.com/p/Method-lXZu4iBCQMv1op2Bv8wM4n).

How well will the model be able to learn this mapping? How will it handle synonyms? Is there a way to present this task to the model to make the learning more efficient? Iterating on the original idea and answering these questions is what the experiments in this repository will center on.

## Special thanks

Special thanks to the authors of the [MultiFiT: Efficient Multi-lingual Language Model Fine-tuning](https://arxiv.org/abs/1909.04761) that is Julian Eisenschlos, Sebastian Ruder, Piotr Czapla, Marcin Kardas, Sylvain Gugger and Jeremy Howard! We trained our models on the wikipedia dumps that you were so kind to provide!

Another round of thanks goes out to authors of [MUSE framework @ facebookresearch](https://github.com/facebookresearch/MUSE), that is Guillaume Lample and Alexis Conneau. We used the ground-truth bilingual dictionaries to evaluate the performance of our models.
