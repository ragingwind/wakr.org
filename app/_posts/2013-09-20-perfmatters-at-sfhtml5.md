---
layout: post
title:  "#performaters at SFHTML5"
post_author: ragingwind
---

![#performaters at SFHTML5](https://lh6.googleusercontent.com/-B4S81iHufKY/Uh_6RAeCDkI/AAAAAAAAAAA/rp2DzUgAFJU/w940-h235/event_theme.jpg)

동부시간 기준으로 2013-09-19 에 샌프란시스코에서 [#perfmatters](http://goo.gl/3ku1xm) 들이 #sfhtml5 meetup 에서 Web [performance - HTML5 Rocks]( http://goo.gl/7Wxf6 ) 에 대한 주제로 발표와 Q&A가 있었습니다. #perfmatters 는 Google IO 2013[^1] 에서 부터 꾸준히 Chrome의 DevTools 와 Under the hood 한 내용을 바탕으로 Web performance 를 개선하는 기술들을 지속적으로 소개하고 있는데 이번 #sfhtml5 meetup 에서는 기존의 발표했던 내용을 정리하고 개선한 것을 [YouTube]( http://goo.gl/sc9ONj ) 를 통해서 한자리에서 모두 볼 수 있습니다.

첫번째 세션에서는 Performance of Chrome developer relations[^2] 의 팀리더인 [+Colt McAnlis](https://plus.google.com/+ColtMcAnlis) 이 Javascript 에서 Manual manage(pooling), counting object 그리고 linear growth 등을 이용한 메모리 관리 방법에 대해서 설명합니다. 특히 [해적처럼 말하기날]( http://goo.gl/A0I95V ) 을 맞아서 해적말투로 진행하는 것이 인상적입니다. 그리고 Chrome DevTools 의 Heap monitoring 과 Adobe 의 gcview 를 사용한 heap tracking 을 소개합니다.

두번째 세션에서는 다른 Bald 인 [+Paul Lewis](https://plus.google.com/+aerotwist) 이 Request / Response 이후 Rendering 과정 [^3] 과 Style, image, animation 그리고 scrolling 처리에 사용되는 비용들에 대해서 설명하고 개선시키는 방법을 설명합니다. 다음 세번째 세션은 [+Jake Archibald](https://plus.google.com/+jakearchibald) 이 브라우저별로 이미지가 다운로드 되는 여러가지 상황을 코드와 W3C 스펙을 곁들여서 재미있게 설명합니다.

마지막 세션에서는 [+Paul Irish](https://plus.google.com/+PaulIrish) 는 이전[^4] 부터 계속 보여주던 스타일 대로 이미 구현된 사이트/앱들을 Chrome DevTools 로 Profiling 하고 개선시키는 데모를 보여줍니다. Frame recording 과 Frame chart 그리고 [Continuous painting mode]( http://goo.gl/Z3IXq ) 를 사용해서 Bottle-neck 과 Pain-point 를 찾아내고 `translatez hack` 등을 사용하여 성능을 개선시킵니다. 그외에도 여러가지 Profiling 도구를 소개하는데요 로딩이 진행되는 동안 Rendering 된 화면도 캡처해서 보여주는 [WebPagetest]( http://goo.gl/bzCd ) 이 주목할 만 합니다.


[^1]: [#PERFMATTERS at Google IO 2013]( http://goo.gl/LeYHsn )
[^2]: Introduction to Google Developer Relations]( http://goo.gl/sUUL1j )
[^3]: HTML parsing, DOM tree creation, Recalculate style with css, Rendering DOM tree, vector / bitmat drawing and decode and Layer composite.
[^4]: [Chrome DevTools Timeline's new Frame Mode - YouTube]( http://goo.gl/v7CYfm )