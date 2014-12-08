---
layout: post
title:  "Digest for Web applications, Nov, 2014"
post_author: ragingwind
categories: digests
---

```Digest for Web Applications``` 에서는 Web Applications 개발에 관련된 소식을 모아서 간단한 코멘트와 함께 전달해 드립니다.

### Chrome Dev Summit

- [Chrome Dev Summit 2014 - YouTube](http://goo.gl/oZcLf7): Chrome Dev Summit 2014 비디오들
- [A Few Things from Chrome Dev Summit 2014, CSS-Tricks](http://goo.gl/aWhEoV): css-tricks.com 의 Chrome Dev Submmit 2014 관람기
- [The Future of the Web (According to Google)](http://goo.gl/WSfjzo): Google 이야기 하는 웹의 미래, Mobile First with Web Components!

### Web Application Manifest, Installable WebApps

- [awesome-webapplications/web-application-manifest](http://goo.gl/lZh5Pa): Web applications 의 Awesome Web application 에 Web application manifest 에 대한 링크자료가 추가되었습니다.
- [Installable Web Apps with the WebApp Manifest in Chrome for Android](http://goo.gl/DkQpIK): Paul Kinlan 이 전하는 Android 의 Chrome 에서 사용하는 WebApp Manifest
- [Web and Mobile Interest Group (WebMob)](http://goo.gl/ksSsHH): WC3  Mobile IG
  - [w3c-webmob/installable-webapps](http://goo.gl/PsLtzP): [유즈케이스](http://goo.gl/E923SB) 를 따르는 Installable Webapp 예제
- [vladikoff/chromeos-apk](http://goo.gl/njVXuQ): Android APK 를 Chrome OS 나 Chrome 이 설치되어 있는 OS X, Linux 그리고 윈도우즈에서 구동가능하게 하는 프로젝트. 소식을 안지는 한달여 되었고 실험도 해보았지만 아직은 Chrome OS 에서 잘 동작한다. 실제 동작은 [여기서](http://goo.gl/hc6RGF) 확인한다.
- [Humble SEGA Bundle (pay what you want and help charity)](http://goo.gl/mBoKA): asm.js 를 사용한 웹게임들
- [비트윈 PC 버전 개발기 - VCNC Engineering Blog](http://goo.gl/Myw27s): CEF 기반에서 react, websocket, commonjs 와 ES6 을 사용한 데스크탑 메신저 개발기
- [bbondy/khan-academy-fxos](http://goo.gl/XBTfk0): Khan 아카데미에서 만든 FirefoxOS 용 앱 소스
- [MacGap : Jekyll Docs Template](http://goo.gl/rOuFnI): OSX 앱 개발을 위한 Gap

### Service Worker

- [Introduction to Service Worker: How to use Service Worker - HTML5 Rocks](http://goo.gl/RRQTbN): HTML5 Rocks 의 Service Worker 사용하기
  - [samples/service-worker at gh-pages · GoogleChrome/samples](http://goo.gl/6XrQGc): Service Worker 예제들
- [Using ServiceWorker in Chrome today - JakeArchibald.com](http://goo.gl/h2wmBo): Chrome (Canaray) 에서 Service Worker 사용하기
- [agektmr/Responsive-Resource-Loader](http://goo.gl/4Y0rGd): Service Worker 를 사용한 RRL(Responsive Resource Loader) 의 컨셉을 구현한 예제, `srcset` 대신에 manifest 의 설정을 사용 
- [markdalgleish/serviceworker-loader](http://goo.gl/Vs2DdX): Webpack 위한 Service Worker Loader

### Web Components

- [platform.js ⇒ webcomponents.js](http://goo.gl/eUKygh): Polymer 의 Web components polyfill 인 platform.js 를 [webcomponents.org](http://webcomponents.org) 로 이전하면서 이름도 `webcomponents.js` 로 변경
- [Release Stable Release 0.5.1: A few hotfixes · Polymer/polymer](http://goo.gl/h9Eu5J): Polymer 0.5.1 릴리즈, Object.observe 가 지원되지 않는 브라우저의 탭이 보여지지지 않는 경우 dirty-check 하는 것을 중지, paper-item 에서 별도로 지정되는 icon label attribute 를 제
- [Built with Polymer](http://goo.gl/SJbeQJ): Polymer 로 만들어진 어플리케이션 모음
- [Polycasts: Core Icons with Rob Dodson - YouTube](http://goo.gl/xXj7qq): Polymer 팀의 [Rod dodson](https://twitter.com/rob_dodson) 이 진행하는 Polycast 시리즈. 2014 년 11 월에 전 세계적으로 있었던 Polytechinc 행사와 같은 선상에서 제공되는 Polymer materials
- [Home – Component Kitchen](http://goo.gl/Tc058M): Web component 카달로그, 각 Component 들의 미리보기 지원
- Material design
  - [FezVrasta/bootstrap-material-design](http://goo.gl/R0kxSQ): Material Design 을 위한 Bootstrap 3 라이브러리
  - [mateusortiz/webcomponents-the-right-way](http://goo.gl/ON4hJt): Web components 를 소개하는 페이지를 모음 Awesome 페이지
  - [callemall/material-ui](http://goo.gl/3166gM): React 를 위한 Material Design
  - [Upgrading Your Syntax Theme](http://goo.gl/jRxpBc) Shadow DOM 을 사용하는 Atom
  - [Daily Material Design Inspiration - MaterialUp](http://goo.gl/G9sI3E): Material Design 을 적용한 앱소개
  - [Polymer Material Design Playground](http://goo.gl/Oq83DM): Eric bidelman 의 Polymer Material Deisn 소개

### Javascripts and ES 6

- [Why Asana is switching to TypeScript - Asana Engineering Blog](http://goo.gl/40vsA4): Asana 가 Typescript 를 사용
- [My five promise patterns](http://goo.gl/j6pPLG)
- [Statically typed JavaScript via Microsoft TypeScript, Facebook Flow and Google AtScript](http://goo.gl/QxdmBx): Typescript, Flow, AtScript 에 대한 소개
- [Combining React, Flux & Web Components — Futurice](http://goo.gl/ZGEdJn): React, Flus 그리고 Web Components용 (Polymer) 를 사용하기 아래 구문이 인상적

  ```
render: function() {
    return <paper-tabs selected={this.props.selectedTab}>
        {tabContent}
    </paper-tabs>;
}
```

- ES6
  - [ECMAScript 6 returns JavaScript to original intent](http://goo.gl/SKlYvw)
  - [ECMAScript 6 promises (1/2): foundations](http://goo.gl/TkkBrs)
  - [ECMAScript 6 promises (2/2): the API](http://goo.gl/VmdNci)
  - [ES6 Repl - Chrome Web Store](http://goo.gl/kaLrqT)
  - [facebook/flow](http://goo.gl/xonNkN): Facebook 에서 내어 놓은 ES6 을 위한 Javascript type checker

### Browsers

- [Chrome 39 - Now stable](https://www.chromestatus.com/features): Chrome 39 가 Stable 되면서 Beacon, Generator(ES6), Web Animation Javascript API, WEb Application Manifest 가 지원
- [Firefox Developer Edition — Mozilla](http://goo.gl/u0hxpJ): 개발자를 위한 Firefox, Developer Editoion. 특히 extension 을 통해서 여러 브라우저 환경에서 테스팅 가능한 [Valence](https://developer.mozilla.org/en-US/docs/Tools/Valence)가 눈에 띈다.
- [Tizen 3.0 Features Announced: Multiple User Support, 64-bit Architecture & More](http://goo.gl/p8lZPV): 타이젠 3.0 소개, 64-bit 지원, Core OS, toolchain 업데이트, 새로운 3D UI Framework 그리고 Chromium / Blink 기반의 Crosswalk 포함
- [Until now, when you were developing a Chrome App with USB access you had to…](http://goo.gl/21cZSk): Chrome Dev Channel 에 USB 선택 API 추가
- [Generate APK · Issue #3125 · dart-lang/chromedeveditor](http://goo.gl/li9QP3): 새로운 APK Generator 의 냄새가

### Tools
- [zeman/perfmap](http://goo.gl/N9c8bz): 리소스 로딩되는 타이밍을 볼 수 있는 bookmarklet 과 Chrome extension
- [davidsonfellipe/awesome-wpo](http://goo.gl/QG98HQ): Web Performance Optimation 을 위한 Awesome 시리즈
- [cross platform - HTML5 Desktop Wrapper/Framework - Stack Overflow](http://goo.gl/Cep9Q0): HTML5 Desktop Wrapper(Shell) 리스트
