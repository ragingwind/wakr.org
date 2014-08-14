---
layout: post
title:  "Poly, Poly, Polymer - Short introduction"
post_author: ragingwind
---

![Web Components Logo](http://www.polymer-project.org/images/logos/webcomponents.png)

[Polymer]( http://goo.gl/PcE1R ) 는 Google I/O 2013 에서 처음 소개되었습니다. [Web Components]( http://goo.gl/tZbhQ ) 기반으로 만들어졌으며 Web Components 를 정형화된 방법으로 사용할 수 있는 새로운 Framework 입니다.

Webapp 을 개발하면서 가장 불편한 점 중에 하나는 표준/공식적인 방법으로 재사용이 가능한 UI Components 를 만들거나 사용하는 방법이 존재 하지 않았습니다. 다른 플랫폼에서 제공하는 Widget 들 처럼 내부 구현이 감추어지고 독립적으로 동작해서 Widget 의 사용법을 알면 되는 것과는 다르게 Boilerplate 한 코드를 매번 사용하거나 서로 다른 방식으로 사용하고 개발자가 간단하게, 이미 알려진 일반적인 방법으로 적용하기가 힘들기 때문에 서로 공유가 되지 않고 한정적으로 사용되었습니다.

위와 같은 문제를 해결 하기 위한 HTML 표준이 [Web Components]( http://goo.gl/tZbhQ ) 이며, 아래와 같이 5개의 구성요소를 가지고 있으며 개발자가 Custom 하게 만든 Widget 을  생성하고 배포해서 사용하는 방법을 제공하고 있습니다.

  - [Shadow DOM]( http://goo.gl/3B0C4 ): Shadow DOM 으로 독립적으로 DOM 과 Style 을 가질 수 있습니다.[^1] 만들어진 Shadow DOM 은 기존의 Contents 와 독립적으로 Styling 을 유지하고 독립적으로 사용될 수 있어서 재사용이 가능한 Web Components 의 주요 기능이 됩니다.
  - [HTML Templates]( http://goo.gl/0VqcP ): 내부에 있는 다른 여러 요소들은 실행/렌더링/재이 되지 않은 비활성화된 DOM 을 사용하여 클라이언트 사이드에서 언제든지 복사(Clone)해서 사용가능합니다.
  - Decorators [^2]
  - [Custom Elements]( http://goo.gl/EaB7p ): 사용자가 새로운 HTML Element 를 만들 수 있습니다. 다른 Custom/General Element 를 이용해서 새로운 Composite Element 를 만들 수 있습니다.
  - [HTML Imports]( http://goo.gl/Bnh0JY ): 만들어진 Components 를 패키지로 만들어 배포하고 공유하고 재사용 할 수 있도록 해줍니다.
  - 그외로 Keyframe 기반으로 복잡한 Animation 을 지원하는 Web Animations Mutation Observers / MDV 그리고 Pointer Events 가 있습니다.

![Polymer Architecture](/images/posts/polymer-arch.png)

Polymer 는 위의 그림과 같이 platform.js, polymer.js (Polymer core), Polymer elements 로 구성되어 있습니다. [platform.js]( http://goo.gl/Ell1s ) 는 현재, 모든 모던 브라우저에서 Web Components 를 모두 지원하지 않기 때문에 모던 브라우저에서 Web Components 를 사용할 수 있도록 해주는 Polyfill 프로젝트 입니다. [Polymer core](http://www.polymer-project.org/polymer.html) 는 platform.js 를 통해서 Web Components 를 사용하며 Polymer 의 기본적인 사용방법을 제공합니다. `polymer-element` 선언하거나 Properties 와 Methods 를 추가할 수 있으며 Element 의 Lifecycle 과 Web Components 이벤트를 제어할 수 있는 방법을 제공합니다. 마지막으로 Polymer element 는 UI Components 를 포함한 여러가지 응용 element 를 제공합니다.

현재 Polymer 는 pre-alpha mode 이며 계속 개발되고 발전하고 있는 중입니다. 표준에 친화적이고 다른 Framework 와 달리 덜 `Opinionated` 하면서 강력한 기능과 빠른 개발을 할 수 있는 Framework 입니다. 기대하고 관심을 가져보세요. 더 자세한 사용방법은 다음의 자료를 참고하세요.

  - Google I/O 2013 에서 [Web Components 을 소개하는 동영상]( http://goo.gl/xjRdBk ) 입니다. 중간에 Youtube Widget 을 이용해서 간단히 검색해서 동영상을 보여주는 부분이 인상적입니다.
  - [Eric Bidelman+]( http://goo.gl/v9uH5a ) 이 작성하는 [Web Components 리소스 모음]( http://goo.gl/oZ7WIb ) 입니다.
  - Google I/O 2013 에서 발표된 슬라이드에 최신 내용을 업데이트 한 것입니다. [Web Components]( http://goo.gl/Lfacj ) 에 대한 새로운 슬라이드입니다. 아래 슬라이드의 최신 버전입니다.
    - Google I/O 2013 에서 발표된 [Web Components]( http://goo.gl/50rV1c ) 에 대한 슬라이드입니다.
  - [Chromium Dashboard]( http://goo.gl/vulIi ) 는 Polymer 로 만들어진 첫 production app 입니다.
  - [Hello Polymer]( http://goo.gl/TfmnFL ) 는 Polymer team 에서 간단한 Polymer 소개와 Q&A 에 대한 영상입니다.
  - Mozilla 에서 제공하는 Web Compornts 를 위한 [X-Tag]( http://goo.gl/ZoYNXt ) 라이브러리입니다. 같이 한번 참고하시는 것도 좋겠습니다.
  - [Addy Osmani+]( http://goo.gl/mvuIi8 ) 가 [Yeoman 의 Polymer Generator]( http://goo.gl/qaTt1e ) 를 사용해서 에 필요한 리소스와 코드를 자동으로 생성해서 Polymer 를 바로 사용해 볼 수 있는 방법에 대해서 설명합니다.
  - Github의 [Polymer/polymer]( http://goo.gl/LvzGOy ) 프로젝트 입니다.
  - [Future CSS in Web Components]( http://goo.gl/SZlR42 )

[^1]: Markup encapsulation, Style boundaries. 다만 iframe 을 이용한 구현 방법는 다르게 CORS 문제나 추가적인 Network request 그리고 실제 보여지지 않아도 Redering 을 해야하는 비용에 대해서 고려해야할 필요가 없다.
[^2]: 다만 Decorators 경우 아직까지 스펙이 없는 상태입니다.
