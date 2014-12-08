---
layout: post
title:  "Digest for Web applications, Apr, 2014"
post_author: ragingwind
categories: digests
---

```Digest for Web Applications``` 에서는 Web Applications 개발에 관련된 소식을 모아서 간단한 코멘트와 함께 전달해 드립니다.

## Chrome Apps
- [Minimize button for Window](http://goo.gl/34GqKt): minimize button 이 드디어? #dev, #chromeos
- [Multiple profiles on Chrome OS](http://goo.gl/xqZJ8f): `chrome://flags/#enable-multi-profiles` 를 통해서 바로 다른 profile 이 적용 가능합니다. #dev,,#chromeos
- [Close windows directly from the Overview mode](http://goo.gl/bXlHna): Overview 모드에서 바로 종료가 해졌습니다.  #dev, #chromeos
- [CCA (Cordova Chrome App) updated for Chrome Apps on Mobile](http://goo.gl/HI5Mhu): Cordova 를 사용해서 모바일에서 Chrome App 을 만들 수 있는 [CCA](http://goo.gl/nU5O6U) 가 업데이트 되었습니다. #chromemobile
- [`chrome.sessions` API](http://goo.gl/pJGYWp): `chrome.sessions` API 에 여러 이벤트들이 추가되어서 tab 의 close 이벤트를 핸들링 할 수 있습니다. #dev
- [`chrome.accessibilityFeatures` API](http://goo.gl/iFzYaL): `chrome.accessibilityFeatures` experimental Chrome Extension library 가 추가되었습니다. 개별적인 Accessibility 장치들 (Large cursor, Virtual keyboard) 에 대해서 접근 할 수 있습니다. #dev, #chromeos
- [IME extensions](http://goo.gl/q9YImo): `<shift>+<space>` 로 IME 변경이 가능합니다. #dev #chromeos
- [Video Player Chrome App](http://goo.gl/sgAaui): 비디오 플레이어가 별도의 Chrome App 으로. #chromeos, #dev
- [Chrome apps/extensions commands global scope](http://goo.gl/j1ZbjK): Chrome apps / extensions 에서 keyboard shortcuts 이 사용 가능해졌습니다. 그래서 Google music mini player 를 포커스를 주지 않아도 제어 가능합니다. #dev
- [Chrome App windows bounds API](http://goo.gl/4rzkJN): inner/outter Bound properties 가 추가되었습니다. window 의 decorations 포함여부가 중요합니다. #dev
- [Chrome App NFC Library is now open-source](http://goo.gl/UYdsBR): [Chrome App NFC Library](http://goo.gl/1odqXO) 가 Open source 로 공개되었습니다. 현재 지원되는 장비는 2대 정도이고 `chrome.nfc` 로 사용 가능합니다.
- [Web Store API to programmatically create, update and publish items in the Web Store](http://goo.gl/Hp6L7l): RESTful API 로  Web Store 를 컨트롤 할 수 있습니다. [web-store](http://goo.gl/3dVfG1) 을 참고하세요.
- [App Info Dialog](http://goo.gl/oLpyb8): `chrome://flags/#enable-app-list-info` 를 통해서 App Info 가 확인 가능해졌습니다. #canary
- [chrome.webstore API for inline installation](http://goo.gl/sT7aAU): `<link>` 태그와 `chrome.webstore` 를 이용하여 inline 으로 설치가 가능합니다. #chromium
- [Mobile Chrome Apps and Android Wear](http://goo.gl/EE1zaG): Mobile Chrome Apps 에서 `chrome.notifications` API 를 사용하여 Android Wear 와 연동하는 방법입니다. #chromemobile
- [Chrome Apps `<webview>` with context menus](http://goo.gl/e2Gth7): `<webview>` 에 `chrome.contextMenus` API 를 이용하여 context menu 를 설정할 수 있습니다. #chromium
- [ServiceWorkers internal page](http://goo.gl/gfCxzk): ServiceWorkers 를 위한 `chrome://serviceworker-internals` internal page 가 생겼습니다. `chrome://flags/#enable-service-worker` 를 이용해서 사용가능합니다. #chromium
- [Perform a simple search in a Chrome App `<webview>`](http://goo.gl/OGKbG5): 생성된 `<webview>` 에서 `webview.find` 로 문자열 검색이 가능합니다. #chromium
- [Handle URLs by Chrome Apps](http://goo.gl/BSrZRr): `url_handlers` 에 URL Pattern 을 등록해서 해당 url 에 접근시 `app.runtime.onLaunched`로 이벤트가 발생해서 추가적인 작업을 할 수 있도록 해줍니다. #chromium
- ["always maximized" TouchView](http://goo.gl/bG8u1v): `chrome://flags/#ash-enable-touch-view-testing` 를 사용하면 `<Ctrl>+<Shift>+<Alt>+D` 키를 사용하면 TouchView 를 최대 사이즈로 고정시킬수 있습니다.
- [Brand new chrome.i18n API](http://goo.gl/r7Omgi): `chrome.i18n` API 에 `getUILanguage` 가 추가 되었습니다.
- [Error Console has been enabled by default](http://goo.gl/AHtOCH): chrome://extentions 에서 Installed apps and extensions 의 에러를 볼 수 있습니다. #chromium
- [Sublime Text 3 plugins for Chromium development on Mac OSX](http://goo.gl/mzNd9f): Chromium 을 Sublime Text 3 에서 하고 싶다면
- [Grunt 0.4.3 released](http://goo.gl/DVW5cw): Grunt 0.4.3 이 릴리즈 되었습니다. grunt.util 에서 제공하던 여러 모듈이 이제 각각의 모듈료 존재 합니다. 이전에 사용하던 `grunt.util.*` 는 `grunt-legacy-util` 로 변경되었습니다.
- [Debugging Asynchronous JavaScript with Chrome DevTools](http://goo.gl/wXDrIf): Asynchronous javascript callbacks 의 full call stack 을 볼 수 있습니다.
- [JS Live Recompilation while doing breakpoint debugging](http://goo.gl/HsDT67): Breakpoint debugging 시에 JS 소스를 바로 수정해서 Recompile 해서 결과를 볼 수 있습니다.
- [Release Polymer Stable release 0.2.2](http://goo.gl/pLaOG8): Polymer 가 0.2.2 로 릴리즈 되었습니다. Shadow DOM Selectos 가 변경되었습니다. HTMLImports 시에 Data URIs 지원 NodeBind 관련 업데이트 등이 있습니다. `Vulcanize` 도 업데이트 되었으니 바로 업데이트 하세요.
- [Release prism-js](http://goo.gl/ecw6vc): Code highlighter prismjs 을 위한 Polymer element 입니다.
- [jansepar/picturefill](http://goo.gl/4N7whj): [The picture Element](http://goo.gl/jXv27) 의 polyfill 프로젝트입니다. 이제 `<picture>` element 를 사용하세요.
- [The +AngularJS  2.0 change detection](http://goo.gl/KCTcEq): Angular.dart 에서 draft 로 구현되었던 AngularJS 2.0 Change detection 이 별도의 프로젝트로 분리되었습니다. 이름은 `watchtower.js` 이고 ES6 으로 작성되고 있습니다.
- [New WebP update 0.4.0](http://goo.gl/suhJma): WebP 가 0.4.0 으로 업데이트 되었습니다. 200% 빠른 인코딩과 25% 빠른 디코딩이 된다고 합니다.
- [x-gif A +Polymer element for flexible GIF playback](http://goo.gl/Znmuiv): GIF 를 마음대로 playback 할 수 있는 Polymer element
- [V8 hopes to ship Object.observe()](http://goo.gl/A7XiV6): `Object.observe()` 가 V8 에 land 될 예정입니다. 관련해서 여러 자료들을 먼저 살펴보세요. `Object.observe()` 는 Webapp 구조에 많은 변화를 줄 것입니다.
  - [Issue 2409 - v8 - Implement Object.observe - V8 JavaScript Engine - Google Project Hosting](http://goo.gl/V9xnzu)
  - [Polymer/observe-js](http://goo.gl/eJnZVm)
  - [Addy Osmani: Plight Of The Butterfly: Object.observe() -- JSConf EU - YouTube](http://goo.gl/72Kvz5)
- [Are Chromebooks the Future of Computing? I was recently…](http://goo.gl/l9gYNq): [Joe Marini](http://goo.gl/MSd5fV) 가 Chromebooks 의 역사와 발전에 대해서 쓴 글입니다.
- [Extensions Manifest v3 brainstorming](http://goo.gl/z8aXUK): Extensions Manifest v3 에 대해서 활발히 논의중입니다. Promise-style API 도 제안되었네요.
- [Chromium Blog: New monetization and publishing options in the Chrome Web Store](http://goo.gl/7uCRTG): Packaged Apps 에서 Free-trial, Chrome Web Store Managed In-App Payments 가 제공됩니다.
