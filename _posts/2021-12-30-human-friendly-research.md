---
title:  인간 친화적인 결함 연구
date:   2021-12-30
author: Tae Eun Kim
kor_author: 김태은
tags:
  - Writing Practice
classes: 
---

### 요약
그 어느 개발자도 소프트웨어 결함으로부터 자유롭지 않다. 결함이 발생하는 것을 피할 수 없다면 결함이 발생했을 때 어떻게 대처하는지가 중요할 것이다. 다양한 연구들이 어떻게 개발자를 보조하여, 혹은 대체하여 결함에 대처할 것인지를 제안한다. 본 글에서는 이러한 연구들이 공통적으로 염두에 두어야 할 점을 고민해 볼 것이다.

### 본문
개발자라면 누구나 소프트웨어 결함으로부터 자유롭지 못하다. 언젠가는 어떠한 형태로든지 소프트웨어 결함에 기여하게 될 것이다. 이처럼 소프트웨어 결함을 피할 수 없다면 우리 연구자들은 어떻게 개발자를 도와서 효과적으로 소프트웨어 결함에 대처할 수 있을까? 

우선 결함이 발생했다는 것을 알려야 한다. 하지만 단순히 프로그램 위치를 하나 뱉어내는 것은 개발자를 귀찮게 할 뿐이다. 적절한 시점에 적절한 정보와 함께 주어져야 한다. 지난주에 수정한 코드의 결함을 오늘 알려준다면 개발자는 기억을 더듬어가야 간신히 관련된 내용을 떠올릴 수 있을 것이다. 따라서 결함이 발생하는 시점에 최대한 가깝게 이를 알리는 것이 중요하다. 또한 적절한 정보라 하면 해당 결함을 이해할 수 있도록 보조하는 정보를 말한다. 이 때, 시각적 자료가 효과적인데, 결함 위치와 실행흐름, 혹은 정보흐름으로 연결된 함수들을 그래프로 시각화하여 보여준다면 개발자에게 큰 도움이 될 것이다.

더 적극적으로 개발자를 돕는 것에는 자동으로 패치를 생성하고 개발자에게는 그 검토만 맡기는 방법이 있다. 하지만 현재 자동 패치 생성 도구들은 테스트만 통과하는 부정확한 패치들을 많이 생성한다. 따라서 검토해야 하는 패치의 수가 많고 이는 개발자에게 새로운 부담이 된다. 이 때, 결함 위치와 마찬가지로 시각적 정보를 함께 제공한다면 더 쉬운 검토가 가능할 것이다. 예를 들어 실패했던 테스트의 결함 위치 주변의 실행 정보를 그래프로 시각화해서 패치 전과 후를 비교하는 것이다. 이렇게 실행흐름과 정보흐름의 변화를 시각적으로 비교하여 제공한다면 패치의 의미를 파악하기 더욱 수월할 것이다. 

결국 핵심은 사람 친화적인 기술이 되어야 한다는 것이다. 사람은 시각적 자료를 통해 더 직관적으로 사고할 수 있고, 작업 맥락과 연관 있는 내용을 더 잘 이해하고 처리할 수 있다는 등 사람에 대한 이해가 필요하다는 것이다.  이것이 앞으로 결함 관련 연구들이 염두에 두어야 할 점이다.