---
layout: post
title: "SUNINATAS No.1"
date: 2021-01-24 21:56:00
categories: SUNINATAS
tags: SUNINATAS
---

써니나타스의 1번 문제.

<img src="/assets/image/2021-01-24-SUNINATAS_No.1/1.png" width="100%" height="100%" />

이 코드의 언어는 ASP 이다.

그냥 눈으로만 분석하기엔 내 기억력이 받쳐주지 않으니 위 코드에 주석을 넣어보도록 하자.

{% hightlight ruby %}
result = Replace(str,"a","aad") // str 의 a 를 aad 로 바꾼다.
result = Replace(result,"i","in") // result 의 i 를 in 으로 바꾼다.
{% endhighlight %}

Replace(문자열, "바뀔 문자열", "바꿀 문자열")

{% highlight ruby %}
result1 = Mid(result,2,2) // result 의 2번째 인덱스에서부터 문자 2개를 반환
result2 = Mid(result,4,6) // result 의 4번째 인덱스에서부터 문자 6개를 반환
{% endhighlight %}

Mid(문자열, 시작 인덱스, 길이)
// 길이는 생략해도 된다.
// 생략하게 되면 문자열의 끝까지 반환한다.
// 또, 길이가 문자열의 길이를 넘어버리면 마찬가지로 문자열의 끝까지만 반환한다.

{% highlight ruby %}
result = result1 & result2 // result1 과 result2 를 합친다.
{% endhighlight %}

결과가 admin 이니 마지막부터 거슬러 올라가보기로 했다.

admin 을 result = result1 & result2 에 대입해보면
admin = result1 & result2 이다.

result1 와 result2 를 합한 result 는 총 다섯 글자이므로
result1 에 앞의 두 글자 'ad' 가 저장되어 있고, result2 에 뒤의 세 글자 'min' 이 저장되어 있다는 것을 알 수 있다.

Mid 함수를 고려하면
result1 는 result 의 2번째 자리에서 문자 2개를 가져왔고,
result2 는 result 의 4번째 자리에서 문자 6개를 가져왔다는 뜻이다.

그렇다면 result 는 ~admin 일 것이라 예상된다.

위에서 Replace 함수로 인해 a 는 aad 로, i 가 in 으로 교체된다는 것을 알고 있으니 반영시켜주면
입력해야 할 문자열은 'ami' 라는 것을 알 수 있다.

<img src="/assets/image/2021-01-24-SUNINATAS_No.1/2.png" width="100%" height="100%" />

해결이다.