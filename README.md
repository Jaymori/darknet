# Yolo-v3 Test

들어오는 인풋이 커진다면 이에 따른 배치도 크게 줄어들게 됨. 하지만 이 경우 배치, subdivision의 감소로 인하여 학습에 지장이 생길 수 있으므로 되도록 16이하로 하지 않음이 좋음.

## 성능향상
YOLO V3의 경우 cfg파일을 사용하여 구조를 변경. 만약 yolo layer를 추가하여 계층을 높일 시 더 detect를 잘할 수 있으나 이에 따른 batch가 줄어들게 됨

## 오류
Class avg.loss 가 nan으로 표시 되는 경우 학습이 잘못되어 가고 있다는 뜻. 현재 test데이터에서 아무것도 찾지 못할 경우 이러한 문제가 발생하게 된다.
-> input size를 줄여 batch size를 늘려보면 해결되는 경우가 있음

## 라벨링
Pascal VOC로 만들었던 경우 이를 yolo annotation으로 변경해야 하는데 이 변경은 다른 git에서 코드를 받아 작성하면 된다.
