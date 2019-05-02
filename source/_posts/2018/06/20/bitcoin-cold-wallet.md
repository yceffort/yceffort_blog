---
title: Bitcoin) Cold Wallet
updated: 2018-06-20 11:05:01
layout: post
tags: [bitcoin]
---

비트코인 - 콜드월렛

오늘은 역사적인 날입니다. 국내 최대 가상화폐거래소인 빗썸 거래소가 해킹으로 350억원이 털렸습니다 [관련기사](http://v.media.daum.net/v/20180620110342755). 기사를 보면 자신의 자산을 콜드 월렛으로 옮겼다고 했는데요. 이 콜드월렛이 무엇인지 알아보겠습니다.

[원문](https://en.bitcoin.it/wiki/Cold_storage)

콜드월렛, 또는 콜드스토리지는 비트코인을 오프라인 상태로 보관하는 것을 의미한다. 이는 특히 많은 양의 비트코인을 다룰때, 보안 목적으로 사용된다.

비트코인은 즉각적으로 출금을 할 수 있는 기능을 제공 하고 있다. 그리고 이러한 비트코인이 보한침해로 인해 훔쳐가는 것을 방지하기 위해, 웹사이트 운영자는 대다수의 비트코인을 콜드 스토리지에 옮겨놓는 것이 좋은데, 이는 웹서버나 다른 컴퓨터로 부터 비트코인 지갑을 분리시키는 것을 의미한다. 그리고 서버에는 이를 출금하기 위해 필요한 최소한의 금액만 보관해 둔다.

비트코인을 콜드스토리지에 보관하는 방법은 여러가지가 있다.

- USB 드라이버에 넣어서 금고 같은 안전한 곳에 보관하는 방법
- paper wallet.

![Ethereum-paper-wallet](https://blockgeeks.com/wp-content/uploads/2017/07/image4-2.png)
- 피지컬 비트코인 [Physicial-bitcoin](https://en.bitcoin.it/wiki/Physical_bitcoin)

![Physical-bitcoin](https://insidebitcoins.com/wp-content/uploads/2014/11/TGBEXBitcoin.jpg)
- 하드웨어 월렛을 이용한 오프라인 비트코인 [Hardware Bitcoin](https://en.bitcoin.it/wiki/Hardware_wallet)

이와 같이 비밀/개인키를 다양한 매체에 백업하는 방법이 존재한다. 그러나 어쩄건, 이러한 방법들도 위험성이 존재한다.
예를들어

손으로 개인키 등을 작성할 경우

- 누가 보거나, 훔쳐가거나
- 손으로 잘못써서 영영 읽을수 없게되거나
- 잘못 옮겨졌거나
- 종이를 불태우거나, 찢거나 각 종 종이 자체의 손상

프린트 할 경우
- 누가 보거나, 훔쳐가거나
- 레이저 프린트가 아닌경우 젖어서 번지거나
- 신뢰할 수 없는 프린터로 인하여 프린팅 하는 과정에서 해킹당하거나
- 종이를 불태우거나, 찢거나 각 종 종이 자체의 손상

등등 사용하는 방법에 따라 각종 위험성이 존재한다.

좀 더 복잡하고 안전한 방법으로는 **Deep Cold Storage** 가 있다. 이는 더욱더 복잡한 방법을 사용하여 비트코인을 오프라인으로 유지하는 방법이다. 예를 들어 암호화된 월렛 파일이 있는 USB스틱을 안전한 금고에 보관하는 방법이다. 퍼블릭 어드레스를 이용하여 지갑으로 비트코인을 보낼 수느 ㄴ있지만, 비트코인을 소비하기 위해서는 암호화된 USB에 물리적으로 접근해야 한다. 이경우에는 단순히 금고를 보관하는 것을 넘어서 추가적으로 예방조치를 취해야 한다.

- 금고에 은행직원이나 유지보수인력이 접근할 수 있으므로 단순히 금고를 탈취하는 것 만으로는 지갑에 액세스 할 수 있어서는 안됨
- 금고가 재난을 맞닥들이거나 도난 당하거나, 저장장치가 손상을 당할 수 있으므로, 백업본이 반드시 존재해야 함.
- 수탁자가 죽거나 능력을 상실할 가능성. 지갑 보관장치의 물리적 위치를 잊어버리거나, 암호를 잊는 경우 비트코인은 영영 사라지게 된다. 암호화를 하는 것 뿐만 아니라 다른 믿을 수 있는 사람이 접근할 수 있는 규정이 있어야 한다.