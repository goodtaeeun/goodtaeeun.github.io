---
title:  결함 위치 추정 기술에 대하여
date:   2021-08-26
author: Tae Eun Kim
kor_author: 김태은
tags:
  - Writing Practice
classes: 
---

### 요약
결함 위치 추정은 자동으로 프로그램의 결함이 존재하는 위치를 찾아내는 기술이다. 이 분야에서 지금까지 제안된 기술들은 크게 두 가지로 나눌 수 있다. 최근에는 다양한 기술들의 결과를 조합하는 기술들이 연구되고 있다. 

### 본문
결함 위치 추정은 자동으로 프로그램의 결함이 존재하는 위치를 찾아내는 기술이다. 프로그램에 결함이 발생하였을 때, 자동으로 이를 찾아 준다면 개발자 입장에서는 많은 시간이 절약될 수 있다. 또한 결함 위치 추정 기술은 소프트웨어 유지 보수 자동화의 완성체인 자동 프로그램 수정 기술의 등장과 맞물려 재조명을 받게 되었다. 왜냐하면 결함 위치 추정 기술은 프로그램을 수정할 위치의 정보를 제공해주기에 자동 프로그램 수정 기술에 꼭 필요한 요소이기 때문이다.


이 분야에서 지금까지 제안된 다양한 기술들은 크게 두 가지로 나눌 수 있다. 이 두 가지는 Spectrum-based, 그리고 Mutation-based 방법으로 각각 주어진 테스트 케이스 실행을 통해 수집된 커버리지 정보를 활용하는 방법, 그리고 프로그램을 변이시켜 그 실행결과를 활용하는 방법이다. Spectrum-based는 매우 단순하지만 효과적인 발상으로 문제를 접근하는데, 이는 특정 프로그램 위치를 실패한 테스트 케이스가 많이 지나가고, 성공한 테스트 케이스는 덜 지나갈 수록 해당 위치에 결함이 있을 확률이 높다는 것이다. Mutation-based 또한 단순한 발상에서 시작한다. 특정 프로그램 위치를 변이시켰을 때, 성공하던 테스트 케이스는 유지하면서 실패하던 테스트 케이스는 줄어든다면, 해당 위치에 결함이 있을 확률이 높다는 것이다. 해당 발상에 기반하여 많은 연구자들이 지금까지 다양한 기술을 제안해왔다.


최근에는 다양한 기술들의 결과를 조합하는 기술들이 연구되고 있다. 이러한 접근은 기존의 기술들로부터 도출된 결함위치 추정 결과들을 함께 학습하여, 더 정확한 결과를 도출하고자 하는 노력으로 이어졌다. 구체적으로는 특히 Learn to Rank로 불리는 방법을 사용하여 각 프로그램 위치들을 어떻게 정렬하면 될지 학습하고, 새로운 프로그램이 주어졌을 때, 그 안의 위치들을 올바르게 정렬하는 것을 목표로 한다. 