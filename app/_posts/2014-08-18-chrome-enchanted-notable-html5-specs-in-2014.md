---
layout: post
title: "Chrome Enchanted: Notable HTML5 Specifications in 2014"
date:   2014-08-18 13:00:00
categories: HTML5
post_author: Chang W. Doh
description: "2014년은 HTML5의 정식 Recommended가 예정되어 있으며, 개인적으로 기대하고 있는 몇가지 HTML5 새로운 규격들이 라이브되는 시기이기도 합니다. Web Components, Web Animations, WebRTC, ServiceWorker에 대해 개괄적으로 정리해보았습니다."
published: true
---

2014년은 HTML5의 정식 Recommended가 예정되어 있으며, 개인적으로 기대하고 있는 몇가지 HTML5 새로운 규격들이 라이브되는 시기이기도 합니다. Web Components, Web Animations, WebRTC, ServiceWorker에 대해 개괄적으로 정리해보았습니다. :)

## 2014년에 주목할만한 HTML5 규격들

아시다시피 2014년도에도 다양한 HTML5 규격이 작성되고 있거나 구현 단계에 있습니다. [W3C는 올해 말 HTML 5.0 표준안을 확정할 예정][1]입니다만 살아있는 표준(Living Standard)로써의 HTML5의 혁신은 지속되고 있습니다. 이번 포스트에서는 현재 시점에서 크롬에 코드가 일부 혹은 전체가 탑재되고 있는 HTML5 규격 중 기존 웹 개발의 패러다임에 변화를 가져올 수 있어 보이는 주목할만한 4가지 규격들에 대해 정리해보았습니다.

| 주요 HTML5 규격 | 설명 |
|---|
| **Web Components** | 웹을 위한 컴포넌트 시스템 |
| **Web Animations** | 통합된 애니메이션 제어 모델을 제공하기 위한 자바스크립트 API |
| **WebRTC** | 실시간 통신(RealTime Communication)을 지원하기 위한 P2P 통신 |
| **Service Worker** | 웹 페이지와 독립적으로 오프라인/시스템 기능을 제공하는 이벤트 기반 Worker |

## 1. Web Components

Web Components는 (HTML, CSS, JavaScript을 통해) 통상적으로 구성된 웹 페이지 일부 혹은 그 자체를 컴포넌트화하여 다른 웹 페이지 내에서 재사용할 수 있도록 하는 기술입니다. 개인적으로 `Web Components`를 규격이 아니라 기술이라고 하는 이유는 통상적인 웹 기능과는 달리 4가지의 독립적인 규격의 집합으로 구현할 수 있는 기술이기 때문입니다.

> 개괄적인 내용은 '[웹 컴포넌트: 차세대 프론트엔드 웹 개발로 가는 관문](http://html5rocksko.blogspot.kr/2014/02/mashup-web-component-evolution-of-web-development.html)'이라는 거창한 제목의 포스트에서 다룬 바가 있기 때문에 여기서 이를 복잡하게 다루지는 않을 것입니다. :)

### 웹에서 컴포넌트가 왜 필요할까?

'컴포넌트(Component)'라는 개념은 개발자에게 있어 이미 충분히 친숙한 개념입니다. 소프트웨어 개발에서는 이러한 요소들을 '컴포넌트(Component)'라는 개념으로 오랜동안 사용해 왔으며 이미 이미 다양한 형태의 컴포넌트가 각 플랫폼에 적합한 형태로 오랜동안 배포되고 사용되어 왔습니다.

10여년전과 다를 바 없이 우리는 여전히 다른 프로젝트에서 사용했던 리스트 아이템들을 새로운 프로젝트에서도 적용하기 위해 *마크업을 복사해서 수정하고 스타일링을 위한 새로운 CSS를 작성하거나 기존 스타일과의 충돌을 제거하고, 자바스크립트를 최대한 모듈화하여 작성*하고 있습니다. 이러한 과정으로 인해 웹 개발자는 개발 프로세스 내에서 언제던지 태그의 바다(Tag Soup)에 빠질 수 있는 가능성을 안고 있습니다. 이제 우리는 조금 더 나아가서 컴포넌트를 웹에서 (특히 프론트엔드 개발에서) 사용할 방법이 필요하며 가능하다면 도구적인 지원을 받을 수 있으면 더 좋을 것입니다.

다행스럽게도 W3C에서는 이러한 컴포넌트 기술을 웹에서 적용할 수 있도록 새로운 규격의 집합을 만들었으며 이 규격들을 묶어 `웹 컴포넌트(Web Component)`라고 부르며 이를 지원하는 도구와 라이브러리들의 작업이 여러 곳에서 매우 빠르게 진행되고 있습니다.

### 웹 컴포넌트를 지탱하는 4개의 기둥

웹 컴포넌트는 다음과 같은 4가지의 규격으로 구성되어 있습니다.

| 규격 | 설명 |
|---|---|
| Shadow DOM | 컴포넌트의 DOM, CSS, JS의 캡슐화(encapsulation)와 스코프(Scope)의 분리를 제공 |
| HTML Template | 로딩 시간에는 비활성화되는 마크업을 정의하고 이를 실행 시간에 복제할 수 있는 기능을 제공 |
| Custom Element | 웹 문서에서 사용할 엘리먼트의 동적인 등록을 통해 컴포넌트의 명시적인 alias를 선언 |
| HTML Imports | 웹 문서 내에 외부 리소스를 포함(Import)하기 위한 기능을 제공 |

이를 웹 컴포넌트의 사용 관점에서 좀 더 단순하게 설명하자면 다음과 같습니다.

1. **HTML Imports**를 이용하여 외부에 존재하는 웹 컴포넌트를 로딩하고,
2. **Custom Element**로 이를 사용자 태그(Tag)로 지정하여 웹 페이지 내에서 태그가 사용될 떄
3. **Template**를 통해 웹 컴포넌트의 인스턴스를 생성(Clone)하고,
4. **Shadow DOM**을 이용하여 생성된 컴포넌트 인스턴스를 웹 페이지 내에서 독립적인 형태로 사용합니다.

#### 가장 손쉽게 설명할 수 있는 장점은 역시 재사용성

웹 컴포넌트에서 로딩, 등록 등의 신규 규격으로 제공되는 부분을 제거하면 컴포넌트 자체는 순수한 자바스크립트, 마크업, CSS의 덩어리입니다. 즉, `웹 페이지`의 **일부** 혹은 **그 자체**라고 할 수 있습니다. 필요하다면 우리는 어떠한 페이지를 컴포넌트화해서 사용할 수도 있고, 지금까지 그랬던 것처럼 특정한 컴포넌트를 만들거나 재사용할 수 있습니다.

물론 최신의 규격을 기반으로 하고 있기 때문에 당장 여러분의 브라우저에서 사용하는데는 무리가 될 수 있습니다만, 필요하다면 [폴리머(Polymer)](http://www.polymer-project.org/)나 [Bricks](https://developer.mozilla.org/en-US/Apps/Tools_and_frameworks/Web_components)를 사용하여 현재 네이티브로 기능이 지원되지 않는 브라우저에서도 웹 컴포넌트를 사용할 수 있습니다. 현재는 [성능에 대한 논란](http://developer.telerik.com/featured/web-components-arent-ready-production-yet/)도 존재합니다만 어쨌든 [크롬 브라우저에서는 완전한 네이티브 구현이 진행되었고, 여타의 브라우저에서도 기능이 일부 지원](http://caniuse.com/#search=web component)이 되고 있으므로 참고하시기 바랍니다.

### 참고 링크

#### 규격 관련

* [Introduction to Web Components](http://www.w3.org/TR/components-intro/)
* [Web Components Explainer](https://dvcs.w3.org/hg/webcomponents/raw-file/ccd579693e46/explainer/index.html)
* [Shadow DOM](http://www.w3.org/TR/shadow-dom/)
* [Custom Element](http://www.w3.org/TR/custom-elements/)
* [HTML Imports](http://www.w3.org/TR/html-imports/)
* [HTML Template](http://www.w3.org/TR/html-templates/)

#### Polyfill 라이브러리

* [Polymer Project](http://www.polymer-project.org/)
* [Mozilla Bricks](https://developer.mozilla.org/en-US/Apps/Tools_and_frameworks/Web_components)

#### 튜토리얼 및 기타 글

* [Shadow DOM 101](http://www.html5rocks.com/ko/tutorials/webcomponents/shadowdom/)
* [Shadow DOM 201](http://www.html5rocks.com/ko/tutorials/webcomponents/shadowdom-201/)
* [Shadow DOM 301](http://www.html5rocks.com/ko/tutorials/webcomponents/shadowdom-301/)
* [Custom Elements](http://www.html5rocks.com/ko/tutorials/webcomponents/customelements/)
* [HTML Imports](http://www.html5rocks.com/ko/tutorials/webcomponents/imports/)
* [Template](http://www.html5rocks.com/ko/tutorials/webcomponents/template/)
* [Building Web Apps With Yeoman And Polymer](http://www.html5rocks.com/ko/tutorials/webcomponents/yeoman/)
* [웹 컴포넌트: 차세대 프론트엔드 웹 개발로 가는 관문](http://html5rocksko.blogspot.kr/2014/02/mashup-web-component-evolution-of-web-development.html)

## Web Animations

오랜동안 웹에서의 애니메이션은 플래시 플레이어가 차지하고 있었습니다만, HTML5 이전에도 SVG(Scalable Vector Graphics)는 자체적인 애니메이션을 구현할 수 있는 방법이 존재하였고 HTML5에 이르러서는 CSS3 Animation과 Transition이 추가되었습니다. 하지만 왜 또 새로운 애니메이션 규격이 제안되었을까요?

### 지금까지의 애니메이션 기능들

다들 아시다시피 애니메이션에 관련해서 이미 4종의 규격이 존재하고 있습니다. Web Animations의 목적을 확인하기 전에 잠시 기존 애니메이션 규격들의 단점에 대해 간단하게 확인해보도록 하겠습니다.

| 규격 | 이슈 |
|---|---|
| **CSS Animation<br/>CSS Transition** | 조합, 시퀀싱, 병렬 처리 상의 문제점<br/>제한적인 스크립트 조작성 |
| **SVG Animation** | 고성능 요구 & 복잡성, HTML 컨텐츠에 범용적으로 적용 불가 |
| **requestAnimationFrame()** | JavaScript 기반이므로 애니메이션 업데이트에 메인 스레드 점유 |

특히 동적인 애니메이션 제어를 자바스크립트에 위임하는 모델은 확실히 자유도가 높지만 메인 스레드를 점유한다는 선천적인 문제점 그리고 애초에 제어가 불가능한 애니메이션 요소들이 존재하고, CSS 스타일(특히 inline style)에 의한 Recalculation, Layouting, Repaint 등의 이슈를 근본적으로 해결할 수 있는 방법은 아니라는 문제가 있으므로 기존의 규격으로 좋은 성능을 가지는 애니메이션을 개발하는 것은 무척 어렵습니다. 더불어 가장 큰 문제점은 이러한 여러가지 애니메이션 모델을 쉽게 제어할 수 있도록 설계된 단일화된 모델이 존재하지 않는다는 것입니다.



### Web Animations

Web Animations는 복잡한 애니메이션을 스크립트로 처리 가능하도록 기존 애니메이션 모델들에 대해 동기화된 API들을 제공하며 기존 4가지 애니메이션 규격에서 처리하기 어려운 부분들을 보완하고 근본적인 구현 사항들을 대체 방안을 제공하는 것이 주요 목적입니다. 이러한 규격을 기초로 얻을 수 있는 가장 큰 장점은 애니메이션 구현에 대한 실행 비용을 브라우저의 구현에 의해 절감할 수 있는 방법이 생긴다는 점 그리고 다양한 애니메이션 기술을 제어하는 공용 API입니다.

#### 웹 애니메이션 규격의 범주

![Web Animations의 범주](https://wiki.mozilla.org/images/f/f6/CSS-SVG-Web-Animations.png)

위의 그림에서 보시다시피 웹 애니메이션의 규격이 포함하는 범주는 매우 넓어보입니다만, 실제로 웹 애니메이션이 추가하고 있는 부분은 어두운 녹색으로 표시되어 있는 애니메이션의 `제어` 부분이며 애니메이션 방식 자체에 대한 기능은 기존의 CSS3 Animation/Transition, SVG 애니메이션을 그대로 차용합니다.

#### 애니메이션에 대한 동적인 제어를 가능하게 하는 API들

개발자들의 관점에서 볼 때 웹 애니메이션은 자바스크립트 기반의 애니메이션 제어 API 세트에 해당하며 웹 애니메이션의 규격을 통해 애니메이션을 처리하는 가장 단순한 예제는 아래와 같습니다.

	<div class="pulse" style="width:150px;">Hello world!</div>
	<script>
	  var elem = document.querySelector('.pulse');
	  var player = document.timeline.play(new Animation(elem, [
	      {opacity: "0.5", transform: "scale(0.5)"}, 
	      {opacity: "1.0", transform: "scale(1)"}
	    ],
	    {
	      direction: "alternate", duration: 500, iterations: Infinity
	    }));
	</script>

위 코드에서 보다시피 API들은 기존 CSS3 Animation 및 Transition, SVG Animation에 기반하여 애니메이션의 속성을 설정할 수 있습니다. 

#### 애니메이션 모델 기반의 논리적인 제어

웹 애니메이션 규격은 애니메이션과 타이밍 제어를 위한 2가지 모델을 추가하고 있습니다.

* 타이밍 모델 - 애니메이션의 재생 시간, 반복, 재생 속도 등의 속성을 기반으로 한 타임 라인 제어
* 애니메이션 모델 - 타이밍 모델에서 처리된 시간값을 기반으로 정의된 애니메이션의 처리

![Web Animations - Timing Model & Animation Model](http://dev.w3.org/fxtf/web-animations/img/timing-and-animation-models.svg)

웹 애니메이션에서 타이밍 모델을 전반적으로 애니메이션을 위한 시간 값을 처리하며, 처리된 시간 값은 정의된 애니메이션에서 재생을 위한 위치 값으로 활용됩니다. 예를 들자면 left 값이 0px에서 100px로 변경되는 애니메이션이 존재할 때 타이밍 모델에서 처리된 시간값이 애니메이션 모델에 입력으로 들어와서 50%에 해당하는 위치 값을 가진다면 애니메이션 모델의 출력값은 `left: 50px;`이 될 것입니다.

#### 선언적인 애니메이션 구조에서의 탈피가 가장 큰 의미

얼핏 보자면 API화 되어 있다는 점 외에는 기존의 기능과 크게 틀린 부분이 보이지는 않을 것이라고 생각되지만, 애니메이션의 대상이 되는 DOM 요소를 논리적인 트리 형태로 포함할 수 있는 기능을 가지고 있습니다. 또한, 타이밍 모델은 기본적인 타이밍의 제어룰 제공합니다만, 타이밍 그룹(Timing Group)을 통해 계층적인 제어가 가능하며 동적으로 애니메이션의 재생 속성을 변경할 수 있으며, 재생시간 등의 속성이 미리 선언되어야 하는 기존 방식과는 다른 편리함을 가지고 있습니다. 이에 대한 자세한 내용은 이후의 다른 포스트에서 다뤄보도록 하겠습니다. :)

#### 초기 단계지만 구현 상황에 대한 지속적인 관심이 필요

크롬을 기준으로 보자면 Blink의 Animation 및 Transition 엔진이 작년 말에 웹 애니메이션을 지원하기 위한 구조로 이미 변경되었으며 현재 [36 버전에서 `Element.animate()`가 구현된 상태](http://updates.html5rocks.com/2014/05/Web-Animations---element-animate-is-now-in-Chrome-36)이며 나머지 기능들이 계속 구현 진행 중입니다. [모질라](https://bugzilla.mozilla.org/show_bug.cgi?id=875219)와 [사파리](https://lists.webkit.org/pipermail/webkit-dev/2013-October/025758.html)는 네이티브 구현은 진행 단계에 있으며 [IE의 경우 구현에 대해 고려 중](http://status.modern.ie/webanimationsjavascriptapi)입니다. 그 외에도 [웹 애니메이션 폴리필 라이브러리](https://github.com/web-animations/web-animations-js)를 이용하여 웹 애니메이션을 다른 HTML5 기반의 브라우저에서 실행할 수 있습니다.

물론 전반적인 규격과 폴리필, 크롬에서의 구현을 포함하여 아직은 초기 단계이기 때문에 당장 사용하기에는 일부 어려운 점이 있습니다. 다만, 웹 애니메이션이 [폴리머에 포함](http://www.polymer-project.org/platform/web-animations.html)된 상태이며 그간 플래시가 차지하고 있었던 웹에서의 애니메이션 기능을 위한 대체 기술로써 고안되었으므로 이에 대한 관심은 지속적으로 가질 필요가 있습니다.

### 참고 링크

#### 규격 관련

* [W3C Web Animations Specification](http://dev.w3.org/fxtf/web-animations/)

#### Polyfill 라이브러리

* [Web Animations.js](https://github.com/web-animations/web-animations-js)

#### 튜토리얼 및 기타 글

* [Polymer - Web Animations](http://www.polymer-project.org/platform/web-animations.html)
* [Web Animations Demo](http://web-animations.github.io/web-animations-demos/)
* [Web Animations - element.animate() is now in Chrome 36](http://updates.html5rocks.com/2014/05/Web-Animations---element-animate-is-now-in-Chrome-36)



## WebRTC

Ajax를 비롯한 HTTP(S) 기반의 통신은 오랜동안 요청/응답(Request and Response) 기반의 모델을 취해왔습니다. 물론 네트워크 데이터의 대부분은 요청에 의한 응답으로 충분히 처리가 가능합니다만, 보다 고성능의 네트워크를 필요로 하는 현대적 서비스들은 이러한 부분에서 어려움을 겪어왔습니다. 이를 해결하기 위한 첫번째 움직임은 2012년 제정된 [Web Socket](http://www.w3.org/TR/websockets/)이었습니다. 그리고 웹 소켓이 해결하지 못하는 P2P 기반의 네트워크를 위한 규격이 바로 WebRTC입니다.

### 웹을 위한 P2P 통신 규격

WebRTC는 웹을 위한 실시간 통신 규격으로 오디오나 비디오 스트림을 P2P로 송수신하는 것뿐만이 아니라 데이터 전달을 위한 메커니즘을 포함하고 있습니다. 

대다수의 서비스들은 클라언트-서버 간의 데이터 통신을 통해 기능을 제공하고 있지만 어떤 경우는 클라이언트 간의 빠른 데이터 교환이 주요 기능 구현 사항이 되기도 합니다. 바로 이러한 경우 WebRTC는 중요한 기반 기능을 제공합니다. 뒤집어 얘기하자면 서버를 중계할 이유가 없으며 클라이언트 간의 데이터를 빠르게 송수신하고자 한다면 WebRTC는 좋은 선택이 될 수 있습니다.

![Architecture of WebRTC application](http://www.html5rocks.com/ko/tutorials/webrtc/basics/apprtcArchitecture.png)

#### 단지 성능이 아닌 신뢰성과 보안을 포함하는 규격

WebRTC는 문자열, Blob, ArrayBuffer 그리고 자바스크립트 바이너리 타입을 지원하며 UDP와 유사한 '신뢰성 없는 모드'와 TCP과 유사한 '신뢰성 있는 모드' 둘 중 하나로 동작할 수 있습니다. 신뢰성 있는 방식(Trusted Mode)은 메시지 전송과 메시지가 전달되는 순서를 보장하지만 추가적인 오버헤드가 있으며 신뢰성 없는 방식(Untrusted Mode)은 모든 메시지가 상대편에 도달하는지와 어떤 순서로 도달하는지를 보장하지 않는 대신 오버헤드를 제거합니다. 

또한, **암호화(Encryption)는 WebRTC 요소의 기본 사항**입니다. 모든 데이터가 데이터그램 전송 계층 보안 (Datagram Transport Layer Security, DTLS)을 사용하도록 정의되어 있으므로 WebRTC를 지원하는 모든 브라우저가 DTLS를 내장하고 있으므로 추가적인 구현없이도 안전한 데이터 송수신이 가능합니다.

#### 가장 대표적인 사례는 비디오 채팅

지난 세월동안 오디오와 비디오 캡쳐는 외부 플러그인들을 사용할 수 밖에 없었으나 HTML5는 다양한 하드웨어에 대한 접근을 표준 규격으로 정의하고 있으며 오디오와 비디오의 캡쳐 역시 그렇습니다. 이와 관련해서 그동안 다양한 규격들이 W3C에서 시도되어 왔지만 현재 [getUserMedia()](https://developer.mozilla.org/en-US/docs/NavigatorUserMedia.getUserMedia)를 통해 대다수의 작업을 할 수 있도록 정리되었습니다. WebRTC의 가장 대표적인 사례는 바로 이 getUserMedia()를 결합하여 별도의 플러그인 없이 구현할 수 있는 P2P 기반의 비디오 채팅입니다.

#### 게임 등에도 응용이 가능한 범용 규격

이러한 대표적인 사례로 인해 WebRTC는 종종 화상 회의와 같은 미디어 통신을 위한 규격처럼 인식되는 경우가 있으나 그렇지 않습니다. 화상회의와 같은 것은 WebRTC의 P2P 통신과 mediaCapture()이 결합된 좋은 사례 중 하나일 뿐입니다. 물론 커뮤니케이션, 게임, 혹은 파일 전송을 위한 두 브라우저 간의 데이터 전송은 상당히 복잡한 과정일 수 있습니다. 우리에게는 WebSocket, AJAX, 그리고 Server Sent Events가 있지만 이는 근본적으로 서버를 통한 통신 모델로써의 디자인입니다.

WebRTC는 근본적으로 P2P를 기반으로 하는 데이터 전송 메커니즘입니다. 이는 파일 전송뿐만이 아니라 P2P를 기반으로하는 멀티플레이어 게임에도 유용합니다. 이를 위한 RTCDataChannel은 파일 공유, 멀티플레이어 게임, 콘텐츠 전송을 위한 앱을 만드는 새로운 방식을 제공합니다. 이를 사용하여 낮은 지연 시간을 가지는 고성능 네트워크 어플리케이션을 제공할 수 있으며, 한 피어(peer)에서 다른 곳으로 직접 데이터를 전달하기 위해 P2P(peer-to-peer) 연결을 가능하게 하여 중개 서버가 없고 '홉(hops)'이 적어 지연 시간을 더 줄일 수 있습니다.


### 참고 링크

#### 규격

* [WebRTC - W3C Working Draft](http://www.w3.org/TR/webrtc/)
* [getUserMedia()](http://dev.w3.org/2011/webrtc/editor/getusermedia.html)

#### 튜토리얼 및 기타 글

* [MDN - WebRTC Basics](https://developer.mozilla.org/en-US/docs/Web/Guide/API/WebRTC/WebRTC_basics)
* [Getting Started with WebRTC](http://www.html5rocks.com/ko/tutorials/webrtc/basics/)
* [WebRTC in the real world: STUN, TURN and signaling](http://www.html5rocks.com/ko/tutorials/webrtc/infrastructure/)
* [WebRTC data channels: WebRTC data channels: for high performance data exchange
](http://www.html5rocks.com/ko/tutorials/webrtc/datachannels/)

## Service Worker

현재의 네이티브 앱들의 기능과 유사한 형태의 웹 어플리케이션을 구현할 때 가장 난해한 부분은 어떤 것일까요? 아마 그래픽스, 성능, 네트워크 등 다양한 의견이 나올 거이라고 생각됩니다만, 최소한 이들 기능은 현재 HTML5에서의 기능들에 의한 대체제가 존재합니다. 단연컨데 현재 가장 어려운 부분 중의 하나는 `오프라인`입니다. Service Worker는 1차적으로는 이러한 오프라인의 문제를 해결하기 위한 시작점입니다. 물론 Service Worker가 커버하는 범위는 이보다 더 넓습니다만, 요약하자면 **네이티브 어플리케이션의 동작 흐름을 웹으로 가져오기 위한 가장 중요한 기능**이라고 할 수 있겠습니다.

### 오프라인을 지원하기 위한 두번째 규격

서비스 워커 이전의 가장 대표적인 문제점은 역시 오프라인 리소스에 대한 관리입니다. 이전에도 [Application Cache](http://www.whatwg.org/specs/web-apps/current-work/#applicationcache)를 이용하여 일종의 Packaged App을 지원하고 오프라인 기반의 웹 어플리케이션을 지속적으로 시도해왔습니다.

#### 로직 기반의 오프라인 리소스 관리

Application Cache의 경우 캐싱 처리를 정적인 분기 로직을 기반으로 동작시켜야 했으며, 대체적으로 개발자가 원하던 방식보다는 **브라우저의 정책에 따라 리소스가 관리**되는 문제가 존재하였습니다. 대표적인 문제점들은 다음과 같이 [Application Cache is a douchebag](http://alistapart.com/article/application-cache-is-a-douchebag)에서 지적된 내용들입니다.

> 1. 온라인에 있을 때에도 파일들이 언제나 어플리케이션 캐시로부터 전달된다.
2. 어플리케이션 캐시는 Manifest 자체가 변경될 때만 업데이트된다.
3. 어플리케이션 캐시는 선택적이지 않은 추가적이 캐시(동작)이다.
4. 절대로 한참 후의 manifest를 캐시하지 않는다.
5. 캐싱되지 않은 리소스는 캐시된 페이지에서 로딩되지 않는다.

![Offline](http://cwdoh.com/images/notable-specs-2014/OMG.appcache.png)

서비스 워커는 이를 해결하기 위해 프로그램 가능(Programmable)한 오프라인 리소스의 근본적인 처리 방법을 제시합니다. 브라우저에서 일어나는 요청(Request)들을 조건에 따라 인터럽트하여 직접 응답(Custom response)할 수 있는 기능을 통해 사용자가 직접 리소스를 관리할 수 있습니다. 따라서 캐시 로직은 사용자가 직접 작성이 가능하며 언제든지 업데이트할 수 있습니다.

![Service Worker - Controlling fetch flow](http://cwdoh.com/images/notable-specs-2014/serviceworker_cache_flow.png)


#### 페이지 기반이 아닌 백그라운드 기반의 프로세싱 지원

익히 아시다시피 웹 어플리케이션은 브라우저 상에서 페이지 단위로 동작합니다. 이를 뒤집어 보자면 페이지가 로딩되지 않은 상황에서의 처리들이 불가능하다는 말과도 같습니다. 아마 기획 과정에서 요구되는 네이티브 어플리케이션 형태의 동작들, 예를 들어 Remote Push Notification과 같은 항목들 이로 인해 구현이 불가능하였습니다. 서비스워커는 시스템 이벤트에 대한 콜백 시스템을 제공하여 이러한 부분을 해결하고자 하고 있습니다. 물론 세부적인 기능들은 서비스 워커 자체에서 지원하는 것은 아닙니다만, 앞으로 백그라운드 프로세싱을 사용하는 대다수의 기능은 서비스 워커를 기반으로 동작할 것입니다. 현재 디자인되고 있는 규격들은 다음과 같이 원격 푸시, 스케쥴 기반의 로컬 알람, 백그라운드 동기화입니다.

원격 푸시 알림의 경우 네이티브에서도 익히 아실 듯하고, 태스크 스케쥴러는 웹 페이지가 로딩되지 않은 상태에서도 스케쥴링된 알람에 의해 특정한 동작을 수행할 수 있으며, 백그라운드 동기화를 통해 오프라인 상태에서의 업데이트된 데이터를 다음 온라인 시에 동기화할 수 있는 기능들을 제공합니다.

1. [Push API](https://dvcs.w3.org/hg/push/raw-file/tip/index.html)
2. [Task Schedular API(a.k.a. Local alarm)](http://www.w3.org/2012/sysapps/web-alarms/)
3. [Background Synchronization](https://github.com/slightlyoff/BackgroundSync)

### 가장 큰 패러다임 변화가 예상

`서비스 워커`는 `웹 컴포넌트`와 마찬가지로 네이티브 어플리케이션 개발자 입장에서는 익숙한 개념들을 가지고 있습니다. 다만, `웹 컴포넌트`가 컴포넌트의 재사용성을 추구하는 개념이라면 `서비스 워커`는 웹 어플리케이션의 근본적인 한계를 탈출하기 위한 내용을 담고 있습니다. 반대로 보자면 웹 어플리케이션 개발자 관점에서는 다소 익숙하지 않은 형태의 많은 개발 형태를 예고하고 있습니다. 하지만, 웹 어플리케이션의 오프라인 기능 지원이 일반화되고 있는 지금 반드시 익숙해져야 하는 대표적인 기능이기도 합니다.

서비스 워커는 그 특성상 폴리필 라이브러리를 제공할 수 없습니다만, 현재 크롬이 서비스워커의 첫번째 네이티브 구현을 포함하고 있습니다. 아직 캐시 API는 폴리필 형태로 제공하고 있습니다만, 대체적인 기능은 현재도 사용이 가능합니다. Google I/O 2014에서 폴리머 데모로 소개된 [Topeka](http://www.polymer-project.org/apps/topeka/)는 로딩 타임의 제거를 위해 [모든 리소스를 초기에 로딩하는 기능을 서비스 워커로 구현](http://www.polymer-project.org/apps/topeka/sw.js)하고 있습니다. 코드를 참조하시는 것만으로도 충분하게 기능을 확인해 볼 수 있을 것입니다.

### 참고 링크

#### 규격 관련

* [Service Worker - W3C repository](http://www.w3.org/TR/service-workers/)
* [Service Worker - Working repository](https://slightlyoff.github.io/ServiceWorker/spec/service_worker/)
* [Explainer](https://github.com/slightlyoff/ServiceWorker/blob/master/explainer.md)
* [Implementation Considerations](https://github.com/slightlyoff/ServiceWorker/blob/master/implementation_considerations.md)

#### 튜토리얼 및 기타 글

* [ServiceWorker first draft is published](http://jakearchibald.com/2014/service-worker-first-draft/)
* [Is ServiceWorker ready?](https://jakearchibald.github.io/isserviceworkerready/)
* [Service Worker: Bring your own magic! (Slide)](http://www.slideshare.net/jungkees/service-workers)
* [ServiceWorker: New Game Changer is coming! (Slide)](http://www.slideshare.net/cwdoh/serviceworker-new-game-changer-is-coming)















<!-- References -->

[1]: http://dev.w3.org/html5/decision-policy/html5-2014-plan.html#plan "W3C Plan 2014"
