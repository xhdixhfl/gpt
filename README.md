# [AI CONNECT] GPT on a Labtop 💻
> 23년도 AI CONNECT에서 진행한 노트북으로 gpt 맛보기 수행 상황 <br>
> 기간 : 23.03.25.~ 23.03.28.
<br>
<br>

## 수행 배경
**1. 참고한 사이트** <br>
- kobart-summarization 훈련 모델 제공 ____________[github](https://github.com/seujung/KoBART-summarization)<br>
 → Dacon 한국어 문서 생성요약 AI 경진대회 의 학습 데이터<br>
- kobart-summarization 다운 및 훈련 포스팅 (java)__[web1](https://younghwani.github.io/posts/kobart-summary-1/)<br>
- kobart-summarization 다운 및 훈련 포스팅________[web2](https://blog.ju-ing.com/posts/KoBART-summarization/)<br>
- kobart-summ, news 등 open API 사용 포스팅 _____[web3](https://www.dinolabs.ai/395)
<br>

**2. 사용 도구 및 언어** <br>
<div>
<img src="http://img.shields.io/badge/Python-3776AB?style=round&logo=Python&logoColor=white" />
<img src="http://img.shields.io/badge/PyTorch-EE4C2C?style=round&logo=PyTorch&logoColor=white" />
<img src="http://img.shields.io/badge/coLab-F9AB00?style=round&logo=googlecolab&logoColor=white" />
</div>
<br>

**3. 파일 설명** <br>
① [Kobart-summarization으로 문장 요약](https://github.com/xhdixhfl/gpt/blob/main/kobart_summ.ipynb) <br>
→ 사용한 api : gogamza/kobart-summarization
<br>

② [Kobart-news로 문장 요약](https://github.com/xhdixhfl/gpt/blob/main/kobart_news.ipynb) <br>
→ 사용한 api : ainize/kobart-news
<br>
<br>

**4. 결과** <br>
![ddd](https://user-images.githubusercontent.com/114147352/233560626-3eb5e0c9-6d41-4a9c-bef0-301f8c7215bb.png)

> **※ ROUGE SCORE** <br>
> : ROUGE (또는 Recall-Oriented Understudy for Gisting Evaluation )는 NLP에서 automatic summarization 및 machine translation 소프트웨어를 평가하는 데 사용되는 일련의 metric 및 소프트웨어 패키지임 <br>
-> 모델을 통해 생성된 요약 또는 번역을 참조 또는 사람이 라벨링한 참조된 요약 또는 번역과 비교하여 평가함

**rouge score 종류**
- ROUGE-N: 시스템 요약과 참조 요약 사이 의 n-gram 중첩
- **ROUGE-1**: 시스템과 참조 요약 사이의 유니그램 (각 단어) 의 겹침을 나타냄
- **ROUGE-2**: 시스템과 참조 요약 간의 바이그램 중첩을 나타냄
- **ROUGE-L**: LCS(Longest Common Subsequence)기반 통계, 가장 긴 공통 하위 시퀀스 문제는 자연스럽게 문장 수준 구조 유사성을 고려하고 시퀀스 n-그램에서 가장 긴 동시 발생을 자동으로 식별
- ROUGE-W: 연속 LCS를 선호하는 가중 LCS 기반 통계
- ROUGE-S: Skip- bigram 기반 동시 발생 통계, Skip-bigram은 문장 순서에 있는 단어 쌍을 나타냄
- ROUGE-SU: Skip-bigram과 unigram 기반 동시 발생 통계
<출처> [나무위키](https://en.wikipedia.org/wiki/ROUGE_(metric))
