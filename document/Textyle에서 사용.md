---
layout: document
title: Textyle에서 사용 - Document - SocialXE
permalink: /document/사용/Textyle에서-사용/
redirect_from:
 - manual/3421/
---
# Textyle에서 사용

<div id="toc-container"></div>
<script>
$(document).ready(function($){
	$('.content').toc();
})
</script>

Textyle에서는 SocialXE 사용을 위한 별도 방법을 제공하고 있습니다.

## 설정

SocialXE의 Textyle 설정은 Textyle 관리자 화면 -> 설정 -> SocialXE에 있습니다.

{% include image.html baseurl=true url="/document/img/Textyle에서 사용 - 01.jpg" description="" %}

기본 사이트의 설정과 별도로 Textyle의 설정을 따로 할 수 있습니다. 단, 도메인이 없이 사이트 ID 형식으로 생성된 Textyle의 경우 SocialXE 서버 연결과 관련된 설정은 나타나지 않습니다.

설정에 관한 자세한 내용은 [환경 설정 살펴보기](../../설정/환경-설정-살펴보기/)를 참고하세요.

## Textyle 발행 소셜 연동

Textyle 발행을 SocialXE와 연동하기 위해서는 '**소셜 정보 통합**'을 사용하고 '**SocialXE 도우미 애드온**'을 사용하셔야 합니다. 설정 -> 애드온 관리에서 'SocialXE 도우미 애드온'을 활성화시켜주세요.

SocialXE 도우미 애드온을 활성화한 후 발행을 하게 되면 자동으로 발행 화면에 SocialXE 정보 위젯을 출력해 줍니다. 발행 전 전송하고픈 소셜 사이트를 선택할 수 있겠죠.

{% include image.html baseurl=true url="/document/img/Textyle에서 사용 - 02.jpg" description="" %}

## 소셜 댓글 사용하기

소셜 댓글을 사용하는 방법은 두가지가 있습니다.

1. 'SocialXE 댓글 위젯'을 이용하여 스킨을 변경하는 방법
1. 스킨 본래의 댓글 입력창을 이용하며 '소셜 정보 통합' 기능과 'SocialXE 정보 위젯'을 이용하는 방법


첫번째 방법에 대해서는 [SocialXE 댓글 위젯](../SocialXE-댓글-위젯/)을 참고하세요.

두번째 방법에 대해서는 [소셜 통합 기능](../소셜-통합-기능/)을 참고하세요.

<div class="pull-left">
	<a class="btn btn-default" href="../소셜-통합-기능/">< 소셜 통합 기능</a>
</div>

<div class="pull-right">
	<a class="btn btn-default" href="../../서버/">서버 ></a>
</div>

<script>
	set_pills('toc_5-5');
</script>