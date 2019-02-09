<!--
## Transfer protocol over UDP

QUIC is a transfer protocol implemented on top of UDP. If you watch your network
traffic casually, you will see QUIC appear as UDP packets.

Based on UDP it also then uses UDP port numbers to identify specific network
services on a given IP address.

All known QUIC implementations are currently in user-space, which allows for
more rapid evolution than kernel-space implementations typically allow.
-->

## UDP 상의 전송 프로토콜

QUIC은 UDP 위에서 구현된 전송 프로토콜입니다. 
당신이 우연히 네트워크 트래픽을 보게 된다면 QUIC이 UDP 패킷으로 나타나는 것을 볼 수 있습니다.

UDP에 기반을 둔 QUIC은 UDP 포트 번호를 사용해서 주어진 IP 주소의 특정 네트워크 서비스를 식별합니다.

현재 알려진 모든 QUIC 구현체는 사용자 영역에 구현되어 있으므로 일반적으로 커널 영역의 구현체보다 훨씬 빠른 발전이 가능합니다.

<!--
## Will it work?

There are enterprises and other network setups that block UDP traffic on other
ports than 53 (used for DNS). Others throttle such data in ways that makes
QUIC perform worse than TCP based protocols. There is no end to what some
operators may do.

For the foreseeable future, all use of QUIC-based transports will probably
have to be able to gracefully fall-back to another (TCP-based) alternative.
Google engineers have previously mentioned measured failure rates in the low
single-digit percentages.
-->

## 동작할 것인가?

(DNS에 사용되는) 53 포트를 제외한 다른 포트를 사용하여 통신하는 트래픽을 차단하는 기업용 및 기타 네트워크 설정이 있습니다.
이러한 설정들은 QUIC을 통한 데이터 전송의 성능을 TCP 기반의 프로토콜보다 저하되게 합니다. 운영자가 해야하는 일에는 끝이 없습니다.

가까운 미래에 QUIC 기반의 모든 전송은 아마도 그레이스풀하게 (TCP 기반의) 다른 대안 프로토콜로
전환될 수 있어야 합니다. Google 엔지니어는 측정한 실패 비율이 한 자릿수라고 얘기했습니다.

<!--
## Will it improve?

Chances are that if QUIC proves to be a valuable addition to the Internet
world, people will want to use it and they will want it to function in their
networks and then companies may start to reconsider their obstacles. During
the years the development of QUIC has progressed, the success rate for
establishing and using QUIC connections across the Internet has increased.
-->

## 개선될 것인가?

QUIC이 인터넷 세상에 가치를 더할 수 있음을 증명한다면 사람들은 사용하기를 원할 것이고 자신들에
네트워크에서 동작하기를 원할 것입니다. 회사는 자신들의 장애물을 검토하기 시작할 것입니다.
수년간 QUIC 개발이 진행되어 인터넷에서 QUIC 연결을 수립하고 사용하는 성공률이 증가했습니다.
