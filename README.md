# BERT와 ELECTRA 모델을 활용한 영어, 한국어 감성분석 
# Sentiment Analysis using BERT and ELECTRA Models

## 1. Abstract
코로나 19시대와 과학기술의 발달로 인해 보다 많은 사람들은 더욱 더 비대면 채널로 자신의 경험을 공유한다. 
본 연구에서는 BERT 모델과 ELECTRA모델을 사용하여 기존의 NLP모델의 문제점인 ‘방향성 문제’를 해결하고자 하였다. 
또한, 본 프로젝트에서는 영어는 어절로 Token화 하면 되는 것과 달리, 한국어는 형태소로 Token화 해야한다는 언어의 특이성을 고려하고자 하였다. 
따라서, 영어 데이터와 한국어 데이터에 각각 BERT 모델과 ELECTA 모델을 적용하여 Accuracy를 비교하였다.


## 2.Kaggle Leaderboard
2.1 Korean SA Competition - BDC101
https://www.kaggle.com/c/korean-sa-competition-bdc101/overview

2.2 English SA Competition - BDC101
https://www.kaggle.com/c/english-sa-competition-bdc101


## 3. 데이터
3.1 영어 데이터
Friends 데이터셋은 Json파일형태이므로 Python에서 Json라이브러리를 import하여 Json Type의 데이터 파일을 DataFrame형태로 만들고자 한다. 
Friends 데이터 셋은 Speaker, Utterance, Emotion, Annotation 총 4개의 변수로 이루어졌다.  Emotion은 Neutral, Joy, Sadness, Fear, Anger, Surprise, Disgust, non 8개로 분류된다.
http://doraemon.iis.sinica.edu.tw/emotionlines/

3.2 한국 데이터
NSMC(=Naver sentiment movie corpus)는 네이버 영화 리뷰에 달린 별점을 긍정/부정으로 변환한 binary-class 데이터셋이다.
NSMC의 데이터셋은 텍스트 파일로, id, document, label 총 3개의 변수를 갖는다. 
변수 Label은 긍정/부정(=1/0) 2가지로 감성이 표현된다.
https://github.com/e9t/nsmc/


## 4.출처
4.1 BERT_영어_오근영.ipynb
https://colab.research.google.com/drive/1EMzEfTYjYLgEHjCCP1vEr9oOZLXMocGh?usp=sharing

4.2 BERT_한국어_오근영.ipynb
https://github.com/deepseasw/bert-naver-movie-review/blob/master/bert_naver_movie.ipynb
https://github.com/SKTBrain/KoBERT/blob/master/scripts/NSMC/naver_review_classifications_pytorch_kobert.ipynb

4.3 Transformer_한국어_오근영.ipynb
https://github.com/jiwonny/nlp_emotion_classification/blob/master/NSMC_KoELECTRA.ipynb

4.4 Transformer_영어_오근영.ipynb
https://github.com/jiwonny/nlp_emotion_classification/blob/master/friends_electra.ipynb
