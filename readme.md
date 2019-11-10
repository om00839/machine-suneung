# 머신수능 프로젝트

머신수능 프로젝트는 ‘BERT라면 수능도 풀 수 있지 않을까?’라는 아이디어에서 시작되어, 딥러닝 모델을 통해 수능 영어 빈칸 추론 문제를 푸는 프로젝트입니다. [Pre-Trained BERT](https://github.com/huggingface/transformers)와 SAN(Stochastic Answer Network)를 사용했고, 약 36%의 성능을 확인할 수 있었습니다. 

## 프로젝트 소개 및 발표 자료

- 링크: [버트야 수능풀자](./presentation/버트야 수능풀자.pdf)

## Requirements

- transformers 2.1.1
- pytorch 1.3.0

## Data

> 데이터셋은 저작권관련 문제로 공개하기 어렵습니다.

- 수능, 모의고사 영어 빈칸추론 문제
  - 모의고사
    - 출처: 평가원, EBSi
    - 고등학교 1학년 ~ 3학년
    - 2003~2020 학년도 3,4,6,7,9,10월 모의고사
  -  수능
    - 출처: 평가원
    - 2006~2019학년도
  - Train: 770개 (모의고사 문제)
  - Test: 95개 (수능 문제)

## 코드

BERT + SAN 모델 구현 및 학습, 성능 평가

- san.ipynb

### 문제 예시

2012학년도 수능 25번 (정답률 88%)

What you do in the 15 to 30 minutes after eating your evening meal sends powerful signals to your metabolism. You’ll set the stage for more vigor throughout the evening hours along with a weight-loss benefit if you stay ___________ after your meal. Among many possible activities, walking is one of the easiest ways to get some minutes of exercise after a meal. In fact, research shows that if you walk after a meal, you may burn 15 percent more calories than if you walk the same time, distance, and intensity on an empty stomach.

① active        ② alone        ③ full        ④ satisfied        ⑤ silent

2011학년도 수능 26번 (정답률 14%)
So far as you are wholly concentrated on bringing about a certain result, clearly the quicker and easier it is brought about the better. Your resolve to secure a sufficiency of food for yourself and your family will induce you to spend weary days in tilling the ground and tending livestock; but if Nature provided food and meat in abundance ready for the table, you would thank Nature for sparing you much labor and consider yourself so much the better off. An executed purpose, in short, is a transaction in which the time and energy spent on the execution are balanced against the resulting assets, and the ideal case is one in which ____________. Purpose, then, justifies the efforts it exacts only conditionally, by their fruits.

① demand exceeds supply, resulting in greater returns
② life becomes fruitful with our endless pursuit of dreams
③ the time and energy are limitless and assets are abundant
④ Nature does not reward those who do not exert  efforts
⑤ the former approximates to zero and the latter to infinity

## 참고자료

- MTDNN: https://arxiv.org/abs/1901.11504
- BERT: https://arxiv.org/abs/1810.04805
- SAN: https://arxiv.org/abs/1712.03556

