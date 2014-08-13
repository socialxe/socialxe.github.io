---
layout: document
title: FTP를 이용한 설치 - Document - SocialXE
permalink: /document/설치/FTP를-이용한-설치/
redirect_from:
 - manual/2758/
---
# FTP를 이용한 설치

<div id="toc-container"></div>
<script>
$(document).ready(function($){
	$('.content').toc();
})
</script>


## 파일 다운로드

XE 공식 사이트 [http://xpressengine.com](http://xpressengine.com) 으로 접속합니다. 상단 메뉴 중 *다운로드*를 선택하세요.

![]({{ site.baseurl }}/document/img/FTP를 이용한 설치 - 01.jpg)

'socialxe'로 검색합니다.

![]({{ site.baseurl }}/document/img/FTP를 이용한 설치 - 02.jpg)

목록의 '*클라이언트 모듈*', '*도우미 애드온*', '*댓글 위젯*', '*정보 위젯*'을 다운로드 받은 후 적당한 폴더에 압축을 풉니다.

## FTP 업로드

다운로드 받은 파일을 FTP 프로그램을 이용하여 업로드합니다. 메뉴얼에서는 FTP 프로그램으로 FileZilla를 이용하도록 하겠습니다. 많이 사용하시는 알FTP의 경우 사용하지 않으시는 것을 추천합니다. 업로드 과정에서 파일이 제대로 올라가지 않는 경우가 많습니다. 그리고 이곳에서 FTP 프로그램에 대한 기본 사용법은 다루지 않습니다.

FTP 프로그램을 이용하여 본인 계정으로 접속한 후 각 애드온, 모듈, 위젯을 아래 경로에 업로드하시기 바랍니다.

- SocialXE 도우미 애드온 : XE경로/addons/socialxe_helper
- SocialXE 클라이언트 모듈 : XE경로/modules/socialxe
- SocialXE 댓글 위젯 : XE경로/widgets/socialxe_comment
- SocialXE 정보 위젯 : XE경로/widgets/socialxe_info

![]({{ site.baseurl }}/document/img/FTP를 이용한 설치 - 03.jpg)

업로드 후에는 항상 실패한 파일은 없는지 확인하여 실패한 파일이 있다면 재시도 해주세요.

![]({{ site.baseurl }}/document/img/FTP를 이용한 설치 - 04.jpg)

이 후 설치 과정은 [최종 설치](../최종-설치/)를 참고하세요.

<div class="pull-left">
	<a class="btn btn-default" href="../쉬운-설치를-이용한-설치/">< 쉬운 설치를 이용한 설치</a>
</div>

<div class="pull-right">
	<a class="btn btn-default" href="../git을-이용한-설치/">git을 이용한 설치 ></a>
</div>

<script>
	set_pills('toc_3-2');
</script>