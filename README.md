## Task : 문장 내 개체간 관계 추출
- sentence와 sentence 안의 entity 2개를 입력 받으면 entity 간의 관계를 출력한다.


<br>

## Data
- column 1: 데이터가 수집된 정보.
- column 2: sentence.
- column 3: entity 1
- column 4: entity 1의 시작 지점.
- column 5: entity 1의 끝 지점.
- column 6: entity 2
- column 7: entity 2의 시작 지점.
- column 8: entity 2의 끝 지점.
- column 9: entity 1과 entity 2의 관계를 나타내며, 총 42개의 classes가 존재함.

<br>

## Training
* python train_trainer.py --config_name [config(json)]
* ex) python train_trainer.py --config_name config_example

<br>

## Inference
* python inference.py --config_name [config(json)] --ckpt_name [saved_model_ckpt]
* ex) python inference.py --config_name config_example --ckpt_name checkpoint-1000

<br>

## Ensemble
* 코드 상에서 경로 변경 후 앙상블 (soft vote, hard vote)

<br>

## QA task
* dataset&evaulate_QA : QA task를 위한 데이터 셋 생성과 pipeline을 활용한 간단한 테스트
* train_QA : QA dataset을 활용하여 학습
* inference_QA : 실제 inferece하지 않고 한 테스트 데이터에 대해 질문 별 결과만 출력한다. 
  (결과 확인 후 성능이 좋지 않아 사용 x)
