---
title: title_test
date: 2022-07-25
author: Hannah Jaywon Kim
description: Dropout summary
permalink: https://jwkimowl.github.io/title_test
---
# Dropout
## 그놈의 over-fitting!

딥러닝 모델 개발을 조금이라도 심도있게 해본 개발자라면 over-fitting이란 단어에 매우 친숙할 것입니다. over-fitting이란 딥러닝 모델이 다양한 요인들로 인해 학습데이터를 과하게 학습하여 학습데이터와 유사한 다른데이터에 대해서는 성능이 좋지않은 현상을 말합니다. 자세한 내용은 포스팅 regularization의 서두에서 다루었습니다.

이런 over-fitting을 해결하게 위해 현재까지 다양한 방법들이 개발되었습니다. Dropout은 딥러닝의 태동기 때부터 사용되었던 over-fitting해결방법으로써, 간단하게 설명하면 딥러닝 layer를 연결하는 각 node를 랜덤하게 사용하지 않고 데이터를 학습하는 방법입니다. 딥러닝을 처음 접하고 배우고 계신분들은 이런 방식이 왜 모델의 성능을 올리는지 이해가 되지 않을 것입니다. 자세한 내용은 본문에서 다루겠습니다.

이번 포스팅은 아래와 같은 순서로 진행합니다.
1. Dropout
2. Effect of Dropout 
3. Type of Dropout
4. 정리
5. reference

## 1. Dropout
Dropout은 deep learning기법의 태동기에 개발된 기술로 당시에는 under-fitting의 문제도 있었지만 동시에 over-fitting에 대한 이슈가 많았습니다. 그래서 '복잡한 딥러닝 모델을 오히려 간단하게 만들면 성능이 증가하지 않을까?'라는 가정에서 개발된 기술로, 딥러닝의 대가인 Geoffrey Hinton교수에 의해 JMLR, 14년에 처음으로 제안된 기술입니다. (추가내용으로 해당 논문의 편집자로 무려 딥러닝의 또 다른 대가인 Yoshua Bengio교수도 참여했습니다. 그렇기에 기술뿐만아니라 좋은 논문 작성법을 익히고 싶은 개발자라면 한번 쯤은 정독해볼만한 좋은 논문입니다.)
