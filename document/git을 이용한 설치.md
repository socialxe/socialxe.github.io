---
layout: document
title: git을 이용한 설치 - 설치 - SocialXE
permalink: /document/설치/git을-이용한-설치/
redirect_from:
 - manual/2763/
---
# git을 이용한 설치

XE 설치 경로에서 각 애드온, 모듈, 위젯을 clone하기 위해 아래 명령어를 입력합니다.

{% highlight bash %}
$ git clone https://github.com/socialxe/addon-mid-forwarder.git addons/socialxe_mid-forwarder
$ git clone https://github.com/socialxe/addon-helper.git addons/socialxe_helper/
$ git clone https://github.com/socialxe/module-client.git modules/socialxe/
$ git clone https://github.com/socialxe/widget-comment.git widgets/socialxe_comment/
$ git clone https://github.com/socialxe/widget-info.git widgets/socialxe_info/
{% endhighlight %}

이 후 설치 과정은 [최종 설치](../최종-설치/)를 참고하세요.

<div class="pull-left">
	<a class="btn btn-default" href="../FTP를-이용한-설치/">< FTP를 이용한 설치</a>
</div>

<div class="pull-right">
	<a class="btn btn-default" href="../최종-설치/">최종 설치 ></a>
</div>

<script>
	set_pills('toc_3-3');
</script>