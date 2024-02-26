# 멀티모달 추천 시스템 (Multi-modal Recommender System)

- Avengers Team 3등 수상
  'Avengers.pdf'
  
## Index
- [Competition INFO](#competition-info)
- [DATA](#data)
- [MODEL](#model)
- [RESULT](#result)
- [HOW TO DO](#how-to-do)

## Competition INFO
[대회 사이트](https://dacon.io/competitions/open/236113/overview/rules)

**대회설명**   
추천 시스템은 사용자의 정보를 분석하여 사용자에게 적합한 상품을 추천해주는 인공지능 기술 중 하나입니다. 추천 시스템 기술을 통해 사용자 편의성 증가 및 사용자의 상품의 접근성을 높여 기업의 이익 증대를 기대할 수 있습니다. 추천 시스템은 주로 사용자의 상품에 대한 선호도 정보를 사용하지만, 데이터 수집의 어려움으로 Data Sparseness나 Cold Start 문제가 발생합니다. 이를 보완하고자, 최근 사용자 로그 정보 뿐만 아니라 이미지 혹은 리뷰 정보를 결합하여 Multi-modal 데이터 기반 추천 시스템 연구가 다수 진행되고 있습니다.

**주관 / 운영**  
- 주관: 인공지능융한연구센터, BK 산업융합형 차세대 인공지능 혁신인재 교육연구단
- 운영: 데이콘

**평가 산식**   
DCCG@50 (Normalized Discounted Cumulative Gain)

**대회 기간**   
2023.07.04 ~ 2023.08.07

**Avengers Team**  
- [ColdTbrew](https://github.com/ColdTbrew)  
- [hyjk826](https://github.com/hyjk826)  
- [uijinee](https://github.com/uijinee)  
- [junghyun2moon](https://github.com/junghyun2moon)

## DATA
| name        | count    |
|-------------|----------|
| user_id     | 192403   |
| item_id     | 62989    |
| interaction | 1254441  |

Dacon 데이터셋: [open.zip 다운로드](https://drive.google.com/file/d/1Qi5SI-bEDxHmKN_lPaN41MC_oI1TyScw/view)

## Model
- BM3 : [논문 링크](https://arxiv.org/pdf/2207.05969.pdf)
- 모델 YAML 설정 파일: [overall.yaml](/configs/overall.yaml)

**Model Train**
```
python main-BM3.py
```

**Model Inference**
```
python MMRec_for_infer/src/main-infer.py
```
