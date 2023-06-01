# Server_IO_prediction_by_machine_learning_method
머신러닝 기술을 사용한 서버 I/O 요청크기 예측 기법 검증 
## 3줄 요약
### 1. Microsoft media server I/O block 데이터셋으로 I/O request size 예측 
### 2. 머신러닝 회귀모델 여러개 + 튜닝, LSTM 사용하여 테스트 해봄 
### 3. 망함 (구체적인 망한 원인은 Project_report.pdf 참조) 

## 망한 원인
### 데이터셋 분석을 제대로 안하고 시도했음, 뒤늦게 보니 타겟 피처(request size)가 매우 작은 구간에 80% 이상 편중되어 있음 
### Min-max, 이상치 제거 시 타겟 피처가 다양성이 아예 사라짐... -> 엄청난 과적합, 의미없는 훈련(자세한건 Report.pdf 참조) 

## 결론 
### 선택한 데이터가 별로임, 전처리를 잘 하던가 좋은 데이터를 찾던가...

## Future work
### SNIA에서 최근에 나온 Block trace 데이터셋이 여러개 있음, 특히 SSD 서버 트레이스가 있는데 
### README 읽어보니 쓸만할 것 같음. 이걸로 테스트 해보면 좋을 듯. 
