---
title: 트렌드, 팁, 통행료 - 비트코인 수수료에 대한 종단연구
updated: 2018-06-28 10:57:52
layout: post
---

Trends, Tips, Tolls: A Longitudinal Study of Bitcoin Transaction Fees

[원문](http://fc15.ifca.ai/preproceedings/bitcoin/paper_8.pdf)

거래 수수료는 암호화폐 시스템 일관성을 유지하는 분산 합의 메커지즘에 기여한 마이너에게 주는 보상으로, 점차적으로 블록에 대한 보상을 대체하도록 설계되어 있다. 장기적인 거래 수수료가 불확실한 상황에서 시스템 전체의 보안과 지속 가능성을 고려 해보았을 때 여전히 이문제가 비트코인 생태계에 어떻게 작용될지 물음표로 남아 있다. 몇몇 사람들은 높은 수수료가 비트코인의 소액지불 시스템을 비경제적으로 만들 것이라고 추측하기도 하였다. 예상되는 다른 시나리오에는 사용자간의 시간 선호도에 따라 (거래를 얼마나 빨리 검증할 것인지) 지불되는 수수료의 방대한 변화, 또는 블록체인외에 다른 보상체계가 설계되는지 등이 있다. 미래를 예측하는 것은 프로토콜의 속성 뿐만 아니라 참여자들의 행동, 비트코인의 생태계에 따라 달려 있기 때문에 예측하기가 어렵다.

이를 위해 과거 2014년 8월 말부터 현재까지 퍼블릭 블록체인에 기록된 4천만건의 거래로 지불된 거래 수수료를 분석하여, 종단연구를 수행하였다. 이 짧은 역사에서, 거래수수료를 지불하는 것과 관련된 몇가지 변화가 있었다. 이러한 변화를 설명하고, 비트코인 커뮤니티에서 전통적으로 믿고 있는 몇가지 가설을 시험할 수 있는 증거를 추출하고자 한다.

### 트렌드: 거래 수수료

![transaction-fee-trend](/images/2018/06/transaction-fee-trend.png)

검정선은 블록당 거래 수수료를 나타내고 있다. 2013년 까지 증가하다가 그 이후로 감소하는 추세를 보이고 있다.

파랑선은 거래금액(비율)에 따른 수수료를 보여주고 있다. 전체적으로, 비트코인 거래 수수료는 전체 거래금액의 0.1% 이하의 수준에 서 형성되고 있으며, 이는 이러한 수수료가 두 개 이상의 비트코인 거래에 포함된다는 사실에 비추어 보았을 때 기존의 지불 시스템이 부과하는 수수료보다 훨씬 낮다는 것을 알 수 있다.

빨간선은 평균 블록크기를 나타내고 있다. 평균 블록크기는 꾸준히 증가하고 있는 것으로 보인다. 블록의 크기가 서서히 한계에 근접할 때 까지 커지고 있지만, 아직 까지는 거래수수료에 영향을 미치지 않는 것으로 보인다.

![transaction-fee-per-block](/images/2018/06/transaction-fee-per-block.png)

블록당 총 거래수수료를 달러당 비트코인 환율과 비교할 때 상당히 같은 추세로 이동하고 있는 것을 볼 수 있다. 이는 비트코인으로 결제되지만 기존통화로 가치가 고정되는 많은 상품과 서비스 가격 과는 달리, 수수료를 결정할 때는 비트코인이 지배적인 역할을 하고 있는 것으로 보인다. 대략 블록당 45달러 선에서 안정세를 가지고 있는 것으로 보인다.

> 주: 2014년 초 블록당 거래수수료는 약 0.07BTC였는데, 2018년 들어서 9.65 BTC까지 치솟았다가 현재는 0.23 BTC내에서 형성되고 있다. 지난 2년간 거래 수수료의 변화량의 변동폭이 매우 극심했다. [참조](https://www.smartbit.com.au/charts/transaction-fees-per-block?from=2013-6-28&to=2018-6-28&day_average=1)

![distribution-trasaction-fees](/images/2018/06/distribution-trasaction-fees.png)

다음으로는 명목상 수수료의 가치 변화를 살펴본다. 위 그림은 시간 경과에 다른 거래당 지불되는 수수료의 추세를 보여준다. 2011년 1월 부터는 거의 어떠한 거래도 수수료를 지불하지 않았다. 2011년 6월 이후에 0.0005 비트코인을 받는 수수료가 등장하고, 이는 곧 전체 거래의 20~30%를 차지한다. 2012년 2분기에 제로 수수료의 거래는 감소하고, 60~70%의 거래는 약 0.0005 비트코인의 수수료를 지불한다. 2014년을 기준으로 보았을때, 가장 많은 거래수수료는 0.0001 BTC다. 이러한 추세는 정적이 아니라 시간이 지남에 따라 뚜렷한 추세를 가지고 있음을 보여준다.

이러한 변화에 대해서 추론하기 위해서는, 비트코인 생태계에서 일어난 주요 사건들을 알아 둘필요가 있다. 2011년 6월에 Bitcoin Core 클라이언트 버전 0.3.23이 릴리즈 되었는데, 이는 기본 거래 수수료를 0.01 비트코인에서 0.0005 비트코인으로 줄이는 계기가 되었다. 2012년 2/4분기에 거래 수수료가 증가한 것은 도박 사이트 [SatoshiDice](https://satoshidice.com/) ([참조](https://en.bitcoin.it/wiki/Satoshi_Dice))의 등장 때문일 것이다. 이 서비스가 4월에 출시된 이후에 이 도박 서비스는 급속도로 인기를 끌기 시작헀다. 이는 블록체인에 거래가 넘쳐나게 만들었으며, 이는 '비트코인 네트워크에 대한 DDoS공격'과 같은 양상을 띄었다.

2013년초 명목수수료가 0.0005 비트코인 떨어진 것과 직접적인 연관이 있는 사건은 찾지 못했지만, SatoshiDice에서 추정 가능한 이유를 발견했다. 이 전에는 SatoshiDice는 각 지불에 0.0005 비트코인을 거래 수수료로 추가헀다. 그런다음 2012년 4/4분기에 거래수수료를 두배로 늘렸고, (0.001 비트코인) 다른 모든 사람들은 여전히 기본적인 거래수수료 0.0005 비트코인을 지불했다.

2013년 5월, 비트코인 코어 0.8.2가 출시되면서 기본 거래 수수료를 0.0005 BTC/kb에서 0.0001 BTC/kb 로 낮추었다. 그러므로 0.0001 비트코인 수수료의 점유율 증가는 사람들이 해당 클라이언트의 새버전을 채택했는지 여부를 확인할 수 있게 해준다.

### 팁: 수수료 지급에 대한 설명

![transaction-latency-by-transaction-fee](/images/2018/06/transaction-latency-by-transaction-fee.png)

지금 이 와중에도 거래수수료를 전혀 지불하지 않는 거래가 소수 존재한다. 수수료를 지불하지 않는 많은 사람들은 채무불이행 상태를 고수하지만, 일부는 더 넢은 수수료를 기꺼이 지불하려고 한다. 이에 대한 합리적인 추론 중 하나는 수수료를 지불하면 마이너가 거래 우선순위를 정하는 인센티브를 제공하여 보다 빠른 확인을 이끌어 낼 수 있다는 것이다. 이것이 사실이라면 인내심 없는 사용자들은 거래수수료를 지불할 의향이 있을 것이다. (예를 들어, 거래출력으로 포함된 비트코인을 바로 다시 사용하려 할 경우.)

위 표는 서로 다른 수수료에 대한 거래 대기 시간을 보여준다. 수수료가 없는 거래는 첫번째 확인을 위해 대략 20분이상을 기다려야 했다. 이와 대조적으로, 0.0005 비트코인을 지불하면 절반 시간 내에 블록에 포함될 수 있다. 하지만 극단적인 경우에는 더 차이가 컸다. 제로 수수료 거래 중 10%는 확인하는데만 4시간이 걸렸으며, 0.0005 비트코인을 지불할 경우는 최대 40분까지만 걸렸다. 0.0005 와 0.001 간의 차이는 크지 않지만, 중간값에서의 차이는 여전히 통계적으로나 경제적으로도 중요하다.

![Distribution-of-holding-times-and-propensity-to-pay-a-fee](/images/2018/06/Distribution-of-holding-times-and-propensity-to-pay-a-fee.png)

위 그림은 보유 시간에 따라 달라지는 수수료를 포함하는 거래 금액을 보여준다. 블록에 포함된 직후에 출력을 사용하는 거래의 경우, 수수료를 포함한 거래의 비율이 더 높다는 것을 알 수 있다. (블록은 10분 마다 생성되므로) 이로 알 수 있는 또다른 사실은, 동일한 블록에서 출력을 재사용하는 트랜잭션의 양이 약 40%를 넘는 다는 것이다.

### 통행료: 문지기 역할을 하는 마이닝 풀

마지막으로, 제로 수수료 거래를 체계적으로 배제하는 마이닝 풀의 동작을 분석한다.

![block-solution-share-of-mining-pools](/images/2018/06/block-solution-share-of-mining-pools.png)

위 그림은 시간의 흐름에 따란 각 마이닝 풀의 블록 솔루션 점유율을 보여준다. 2013년 BTC Guild는 40%에 가까운 점유율을 보였는데, 이는 2014년 GHash.IO와 동일한 크기다. 이 짧은 시간 동안 거의 50%의 점유율에 육박했을때, 논란의 여지가 있기도 했었다. 2014년에는 이외에 다른 마이닝 풀의 점유율이 증가했다. 이전에 인기있었던 마이닝풀 (Slush, 50BTC 등)의 인기가 시들해졌다. 이러한 이유에는 아마도 마이닝 풀 수수료 같은 경제적이거나 기술적인 요인,서비스 가용성, 혹은 공격에 대한 방어 등이 있었을 것이다. 몇 개의 지배적인 마이닝 풀이 지배적인 위치에 있다는 것을 감안한다면, 왜 일부 마이닝 풀이 체계적으로 수수료를 강요하는지 알 수 있다.

![Enforcement-of-transaction-fees-by-mining-pools](/images/2018/06/Enforcement-of-transaction-fees-by-mining-pools.png)

위 표에서는 가장 큰 10개의 마이닝풀의 제로 수수료 거래와 그렇지 않은 거래의 점유율을 보여주고 있다. Discus Fish와 Eligius의 경우 각각 30.6%, 62.5% 비율로 거래 수수료가 있는 블록을 선호한다는 것을 볼수 있는데, 이는 평균 14.4%와 비교했을 때 굉장히 큰 수치다. 그러나 이 두 마이닝 풀 이외에는 딱히 거래수수료가 있는 블록을 선호한다는 증거를 찾을 수 없다.

Discus Fish와 Eliguis에서 제로 수수료 거래가 없는 블록이 많은 이유는 이러한 블록들은 트랜잭션을 가지고 있지 않기 때문이다. 빈 블록은 2014년 을 기준으로 117개중 한번 꼴로 나타나고 있다. 이를 제어하기 위해, 이러한 블록내의 거래 중앙 값을 알 필요가 있다. Eliguis의 경우, 거래의 중앙값은 75이고, Discus Fish는 233개 이다. 따라서, 제로 수수료가 없는 블록들은 완전히 비어있지 않다. 이 두 마이닝 풀은 블록에서 거래 수수료를 부과한는데 더 엄격한 자세를 취하고 있음을 알 수 있다.

> 주: 위와 같은 순위는 2014년 기준이고, 2018년 현재 마이닝 풀의 점유율에는 많은 변화가 있었다. [참고](https://blockchain.info/ko/pools)

### 결론

시간이 지남에 따라 거래 수수료의 이질성과 불안정성은 곧, 시장 메커니즘이 거래 수수료에 대한 공정한 가격을 설정하지 못한다는 것으로 해석할 수 있다. 이는 블록 보상이 마이닝의 수입의 대부분을 차지하고, 그 시스템을 방어하기 위한 적절한 동기를 제공하는 한 받아 드릴 수 있는 수준의 불안정성으로 보인다. 그러나 거래수수료만 남게 될 비트코인의 미래에는 두가지 질문이 남아 있다.

1. 공정한 거래 수수료 수준을 형성하는데 영향을 미치는 것은 무엇인가?
2. 이 적정 수준의 수수료를 대략이라도 찾기 위해 실행할 수 있는 메커니즘은 무엇인가?

비용은 시스템내에서 두가지 형태로 발생한다.

1. 마이너들은 최초 확인을 위해 작업 증명 퍼즐을 해결하는 비용을 부담한다. 이 비용은 일회적이고 블록당 고정되어 있으므로, 동시에 확인을 원하는 거래의 숫자에 따라 다르다.
2. 네트워크의 릴레이 (전체 블록체인을 저장하는 모든 클라이언트)가 거래기록을 저장하는 비용. 현재 규칙은 그것을 영원히 저장하는 것이지만, 이론적으로는 거래가 완전히 소비된 이후에는 폐기 될 수 있다. 이 비용은 시간이 지남에 따라 트랜잭션의 크기에 따라 발생하며 (저장 공간) 모든 출력이 소비될때까지의 시간 및 네트워크의 크기 (몇개의 사본이 있어야 하는지)에 따라 달라진다.

1의 비용은 마이너들에 의해 내재화 될 수 있다고 생각 할 수 있다. 그러나 두 번째와 같이 내재화 되지 않는 공공재의 비용 (스토리지를 저장하는데 소모되는 비용)이 무임승차 비용으로 남아 있는 문제가 있다. 두 번째 비용을 유발하는 세가지 요소 중 두 가지 (마이닝 풀에게 유의미한 수수료는? 빠르게 처리되기 위한 적장한 수수료는?)는 트랜잭션이 생성될 때 예측 할 수 없다. 수 많은 트랜잭션에 대해 평균값을 찾는 것은 이에 대한 해답이 아니다. 이는 체리 피킹과 같은 문제를 야기할 것이다. 거래 수수료 위주의 체제에서는, 높은 트랜잭션에 대한 수요와 시간의 선호도가 높은 사람들이, 비트코인이라는 자산을 가지고 아무런 행동을 취하지 않는 사람들에게 보조금을 주는 모양새가 될 수 있다. 이러한 배경에서 보았을 때, 인플레이션을 바탕으로 화폐가치를 평가절하를 유도하는 것이 거래에 수수료를 매기는 것 보다 더 최적의 매커니즘을 보인다.