---
title: 탈중앙화된 개인정보-블록체인으로 개인정보 지키는 법
updated: 2018-06-28 10:57:52
layout: post
mathjax: true
---

Decentralizing Privacy: Using Blockchain to Protect Personal Data

[원문](https://enigma.co/ZNP15.pdf)

전세계에서 유통되고 있는 데이터의 총량이 급속도로 증가하고 있다. 최근 조사에 따르면, 지난 2년간 대략 전체 데이터의 20%가 생성되었다는 사실이 밝혀졌다. 세계에서 가장 큰 소셜네트워크 서비스인 페이스북의 경우 개인정보로만 300 페타 바이트를 수집하였는데, 이는 미국의회 도서관이 200년에 걸쳐 수집한 장서의 양보다 100배 더 많은 수치다. 빅데이터 시대에서, 데이터는 지속적으로 수집되고 분석되며, 이는 혁신과 경제발전을 이룩하는 원동력이 되고 있다. 많은 기업과 단체는 개인화된 서비스를  제공하거나, 중요한 결정을 내리거나, 미래 트렌드를 예측하기 위하여 데이터를 수집한다.

데이터 위주의 사회가 주는 이익이 커지는 반면,개인정보에 대한 우려도 자라나고 있다. 공공 및 민간등 중앙 집중화된 조직에서 많은 양의 개인 및 민감한 정보를 축적하고 있다. 개인은 자신에 대해 저장된 데이터와 그 사용 방법을 거의 제어하지 못한다. 최근 몇 년간 사생활 침해와 관련된 사건이 반복적으로 대두되었다. 페이스북이 참가자들에 대해 명시적으로 알리지 않고 수행한 대규모 실험이 이 중 가장 큰 이슈로 대두되기도 했다. [참고기사](https://www.nytimes.com/2014/06/30/technology/facebook-tinkers-with-users-emotions-in-news-feed-experiment-stirring-outcry.html)

이 논문에서는 블록체인과 비블록체인 스토리지를 결합하여 개인정보보호에 초점을 맞춘 개인 데이터 관리 플랫폼을 구축한다. 그리고 블록체인이 어떻게 신뢰할 수 있는 컴퓨팅 하에서 중요한 자원이 될 수 있는지를 소개한다. 그리고 이 시스템 하에서는 다음과 같은 일반적인 사생활 보호 문제를 방지한다.

- 데이터 소유권: 사용자는 자신의 데이터에 대한 소유권과 제어권이 있어야 한다. 이 시스템에서는, 사용자는 데이터의 소유자로, 서비스는 허가 받은 게스트로 인식되어야 한다.
- 데이터 투명성과 감사가능성: 각 사용자는 수집되는 데이터와 액세스 방법에 대해 완전한 투명성을 가지고 있다.
- 세분화된 접근 제어: 모바일 어플리케이션의 주요 이슈중 하나는 사용자가 가입시 일련의 권한을 부여 해야 한다는 것이다. 이러한 권한은 무기한을 주어지며, 이를 변경하는 방법은 '선택옵션'을 선택하는 것이다.  이 대신, 이 프레임워크 내에서 사용자는 자신이 원하는 아무 때나 자신의 권한을 변경하고 수집된 데이터에 대한 액세스를 취소할 수 있다. 이러한 메커니즘을 적용하면, 모바일 어플리케이션의 기존의 권한 수집 대화상자를 더욱 향상시키고 있다. 사용자 인터페이스는 기존대로 유지하고, 개인정보 액세스 제어 정책은 사용자만 변경할 수 있는 블록체인에 안전하게 저장한다.

![privacy-blockchain](/images/2018/06/privacy-blockchain.png)

- User: 모바일 어플리케이션을 다운로드 받고 이용하는 사용자
- Service: 개인정보를 수집하는 어플리케이션을 제공하는 업체
- Node: 인센티브를 대가로 블록체인을 유지하고 개인 Key/Value 값을 분산시켜 저장하는 주체

사용자는 일반적으로 익명으로 남아있지만, 블록체인에 서비스 프로필을 저장하고 신원을 확인할 수 있다.

블록체인은 두가지 타입의 트랜잭션을 받아드린다.

1. $$T_{access}$$: 권한 제어 관리
2. $$T_{data}$$: 데이터 수집과 회수

이 프레임워크는 기존에 존재하는 모바일 소프트웨어와 쉽게 연동되기 위해 SDK형태로 배포되어야 한다.

다음과 같은 상황을 가정해 보자.

사용자가 자신의 개인정보를 보호하기 위해 해당 어플리케이션을 설치했다. 처음 가입을 하게 되면, 유저의 권한과 함께 새로운 신원정보가 생성되어 $$T_{transaction}$$ 내에 포함되어 블록체인으로 보내진다. 스마트폰에서 수집된 데이터 (위치정보 등)은 암호화키로 암호화되고 $$T_{data}$$ 내에 포함되어 블록체인으로 보내진다. 이 트랜잭션은 이후, 공개원장에 대한 포인터만 유지하면서 비블록체인 Key-Value 스토리지 저장소로 라우팅 된다. (포인터는 데이터의 SHA256 해쉬값이다.)

서비스와 사용자 $$T_{data}$$와 포인터를 사용하여 데이터를 요청할 수 있다. 블록체인은 사용자 또는 서비스의 디지털 서명으로 해당 내용을 검증한다. 서비스의 경우에는, 이에 대한 권한도 함께 확인하게 된다. 사용자는 새로운 일련의 권한을 $$T_{access}$$ 과 함께 발급하여 언제든 개인정보 제한 권한을 변경하거나, 이전에 제공한 정보를 폐기 할 수 있다. 사용자의 데이터와 권한을 변경할 수 있는 웹이나 모바일 기반의 대시보드를 개발하는 것은 매우 쉽고, 이는 비트코인의 코인베이스와 같은 중앙 집중형 지갑을 개발하는 것과 유사하다.

이러한 비블록체인 KeyValue 저장소로는 분산형 해쉬 테이블인 [Kademilia](https://en.wikipedia.org/wiki/Kademlia) ([참고논문](https://pdos.csail.mit.edu/~petar/papers/maymounkov-kademlia-lncs.pdf))에 persistence를 위해 [LevelDB](https://github.com/google/leveldb) 추가해 구현하였다. Distributed Hash Table(이하 DHT)는 승인된 읽기/쓰기 트랜잭션을 수행하는 노드네트워크(블록체인으로 네트워크로 부터 분리될 수 있음)에 의해 유지 된다. 고가용성을 보장하기 위해 데이터가 노드 전체에서 충분히 임의로 추출되고 복제된다. 스토리지에 대해 비블록체인 솔루션을 고려할 수 있다는 점을 유의하자. 예를 들어, 데이터를 저장하는데 중앙 집중형 클라우드가 사용될 수도 있다. 이를 위해서는 타사에 대한 신뢰가 필요하지만, 어느정도 확장성과 구축 용이성에서 이점을 얻을 수도 있다.

개인 정보를 비롯한 민감한 데이터는 공격과 오남용에 취약한 제3자의 손에서 관리되면 안된다. 그대신, 사용자들은 보안을 위협받거나 회사나 관리당국의 개인화된 서비스를 제공할 수 있는 능력을 손상시키지 않는 범위 내에서 자신의 정보를 관리하고 소유할 수 있어야 한다. 이 플랫폼은 블록체인을 액세스 제어 중재자로 사용하는 블록체인과, 비블록체인 스토리지 솔루션을 결합하여 이러한 기능을 제공하였다.

또한 이런 분산 플랫폼을 통해 데이터 수집, 저장 및 공유하는 것에 대한 법적 혹은 규제적인 결정을 내리는 것이 더욱 간결해 져야 한다. 또한 법이나 규제등을 블록체인 그 자체에 프로그래밍하여 자동으로 시행할 수 있다. 원장은 위조가 불가능하기 때문에 데이터에 액세스 하기 위한 법적인 증거로도 사용할 수 있다.
