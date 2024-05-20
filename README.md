# ssc_ukr_ru

This repo contains deliverables of a diploma project with title "Speech Sentiment Classification in a
Ukrainian-Russian Environment".
The aim of this project is to clreate a system for binary sentiment classification (negative - non-negative) for Ukrainian, Russian or mixed conversations (audio)

Note, the dataset for this work is proprietary and cannot be shared.

The structure of the repo is the following:
- evaluation_notebooks
  - asr_eval.ipynb - evalution of ASR model for mix of Ukrainian and Russian languages
  - class_eval.ipynb - evaluation of zero-shot LLM classifiers + testing classification with LLM inference
  - audio_feature_extr_eval.ipynb - extracting hidden states from LLM clasifiers and training LR. Evaluation results are reported using 5-fold cross validation
  - opensmile_feature_significance.ipynb - explored feature significance for opensmile ComParE features
  - text_feature_extr_eval.ipynb - contains opensmile hand-crafted features and wav2vec2.0 feature extraction (for 300m, 1b and 2b XLS-R model without fine-tuning). Evaluation results for LR model are reported using 5-fold cross validation
  - bimodal_fusion.ipynb - bimodal fusion (early and late) for audio and text components. Evaluation results for LR model are reported using 5-fold cross validation
- w2v_finetuning - contains notebook with Wav2Vec2.0 XLS-R 300m finetuning (not very succesfull) 
- inference_notebook
  - baseline_inference.ipynb - interference for baseline model (ASR + zero-shot LLM clasifier), no previous training is required
- experiment_results - contains xlsx files with wandb experiment logging
