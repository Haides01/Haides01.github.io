---
layout: post
title:  "최근 보안 기술 동향 : 제로 트러스트, EDR, XDR"
date:   2025-05-14
category: Security
image: assets/img/blog/security-trends.png
author: Ryan Adlard
tags: Security ZeroTrust EDR XDR
---

사이버 위협이 정교해지고 있는 만큼, 보안 기술도 빠르게 발전하고 있습니다.  
이번 포스트에서는 최근 가장 주목받는 **3가지 보안 기술 동향**을 소개합니다:  
**제로 트러스트(Zero Trust)**, **EDR(Endpoint Detection and Response)**, **XDR(Extended Detection and Response)**.

---

##  1. 제로 트러스트 (Zero Trust)

**“아무도 믿지 마라. 내부도 예외는 아니다.”**

제로 트러스트는 **모든 사용자와 기기, 네트워크 활동을 지속적으로 검증**하는 보안 모델입니다.  
VPN이나 경계 기반의 보안 모델과는 달리, 네트워크 내부에 있다고 해서 자동으로 신뢰하지 않습니다.

###  핵심 개념
- 사용자/디바이스 인증과 권한 최소화
- 지속적인 모니터링과 이상 탐지
- 마이크로 세그먼테이션 (Micro-Segmentation)

> 전통적인 보안은 성벽 기반이었다면, 제로 트러스트는 ‘출입 통제소’ 기반입니다.

---

## 🛡️ 2. EDR (Endpoint Detection & Response)

**“엔드포인트에서의 실시간 감지와 대응”**

EDR은 각종 단말(PC, 서버, 모바일 등)에서 발생하는 이벤트를 모니터링하여 **의심스러운 활동을 탐지하고 대응**할 수 있는 시스템입니다.

### 🔍 주요 기능
- 실시간 이상 징후 탐지
- 위협 분석 및 경고
- 포렌식용 로그 수집
- 수동/자동 위협 대응

### 🧠 대표 솔루션
- CrowdStrike Falcon
- SentinelOne
- Microsoft Defender for Endpoint

## 3. XDR (Extended Detection & Response)

“모든 보안 이벤트를 통합적으로 연결하다”

XDR은 EDR보다 확장된 개념으로, 엔드포인트 + 이메일 + 네트워크 + 클라우드 + ID 등 여러 소스에서 데이터를 수집하고, 이를 통합적으로 분석해 위협을 탐지합니다.

###  차별점
다양한 보안 데이터의 연계 분석

경고의 정확도 향상 (false positive 감소)

자동화된 대응 (SOAR와 연계)

XDR은 보안 운영 센터(SOC)의 '멀티센서' 역할을 합니다.

```python
# 위협이 감지되면 자동으로 대응하는 예시
def detect_threat(event):
    if event == "malicious_behavior":
        return "Isolate endpoint and alert SOC"
    return "No action"

detect_threat("malicious_behavior")
#=> 'Isolate endpoint and alert SOC'

{% if site.disqus.shortname %}
  <div id="disqus_thread"></div>
  <script>
    var disqus_config = function () {
      this.page.url = '{{ page.url | absolute_url }}';
      this.page.identifier = '{{ page.url }}';
    };
    (function() {
      var d = document, s = d.createElement('script');
      s.src = 'https://{{ site.disqus.shortname }}.disqus.com/embed.js';
      s.setAttribute('data-timestamp', +new Date());
      (d.head || d.body).appendChild(s);
    })();
  </script>
  <noscript>댓글을 보시려면 자바스크립트를 활성화해주세요.</noscript>
{% endif %}