---
layout: document
title: SocialXE 댓글 위젯 - Document - SocialXE
permalink: /document/사용/SocialXE-댓글-위젯/
redirect_from:
 - manual/3241/
---
# SocialXE 댓글 위젯

<div id="toc-container"></div>
<script>
$(document).ready(function($){
	$('.content').toc();
})
</script>

SocialXE 댓글 위젯은 홍보 페이지 등에 사용하기 적합한 형태의 소셜 댓글 위젯입니다. 위젯으로 되어 있어 원하는 곳 어디든 삽입할 수 있습니다.

{% include image.html baseurl=true url="/document/img/소셜 댓글 - 01.jpg" description="SocialXE 댓글 위젯" %}

## 페이지에 SocialXE 댓글 위젯 달기

SocialXE 공식 사이트의 메인 페이지와 같이 페이지에 SocialXE 댓글 위젯을 달기 위해서는 우선 **댓글이 등록될 문서**가 필요합니다.

SocialXE 댓글 위젯 전용으로 사용할 게시판 하나를 생성합니다. 그런 후에 모든 권한을 없앱니다. **SocialXE 댓글 위젯은 게시판의 권한을 무시하고 작동되도록 되어 있습니다.** 여기서 설정하는 권한은 더미용 게시판에 접근하지 못하도록 하기 위함입니다.

{% include image.html baseurl=true url="/document/img/SocialXE 댓글 위젯 - 01.jpg" description="" %}

이제 그 게시판에 위젯을 위한 글을 하나 작성합니다. 그리고 그 글의 문서번호(document_srl)을 기억해 둡니다.

{% include image.html baseurl=true url="/document/img/SocialXE 댓글 위젯 - 02.jpg" description="이 글은 문서번호가 116인 것을 확인할 수 있습니다" %}

이제 페이지 수정에서 위젯을 추가합니다.

{% include image.html baseurl=true url="/document/img/SocialXE 댓글 위젯 - 03.jpg" description="" %}

- 댓글이 등록될 문서번호 : 아까 기억해둔 문서번호를 입력합니다.
- 소셜 서비스에 등록될 제목 : 말 그대로 어떤 제목으로 등록될지 적어줍니다.
- 소셜 서비스에 등록될 주소 : 소셜 서비스로 댓글이 전송될 때 표시될 주소입니다. 이 주소를 적을 때는 XE의 경로를 포함하여 현재 페이지의 mid값까지 rewirte룰을 적용하지 않은 값으로 적어주시기 바랍니다. 대댓글이 달렸을 때 해당 댓글 타래를 한번에 보여주는 기능을 사용할 수 있습니다.

{% include image.html baseurl=true url="/document/img/SocialXE 댓글 위젯 - 04.jpg" description="소셜 서비스의 링크를 눌러 접속했을 때 해당 댓글 타래를 보여주는 모습" %}

페이지 수정 상태일 때는 더미 디자인이 적용되어 보입니다.

{% include image.html baseurl=true url="/document/img/SocialXE 댓글 위젯 - 05.jpg" description="" %}

페이지 저장을 누르면 위젯이 추가된 것을 확인할 수 있습니다.

{% include image.html baseurl=true url="/document/img/SocialXE 댓글 위젯 - 06.jpg" description="" %}

### mid 포워딩

SocialXE 댓글을 페이지에 넣어 사용할 때 한가지 불편한 점이 있을 수 있습니다. 바로 댓글 알림 쪽지나 관리자 페이지의 댓글 관리 화면에서 링크를 누르면 더미용 게시판 본문으로 간다는 점입니다. 이런 불편함을 없애기 위해서 포워더 애드온이 있습니다.

{% include image.html baseurl=true url="/document/img/SocialXE 댓글 위젯 - 07.jpg" description="" %}

포워더 애드온에서 원본 문서번호와 포워딩할 mid를 적은 후 애드온을 적용하면 더미용 본문으로 접속시 mid를 변경하여 줍니다.

## 게시판 등 모듈에 적용하기

SocialXE 댓글은 위젯으로 되어 있기 때문에 페이지는 물론 특정 모듈에도 손쉽게 적용할 수 있습니다. 메뉴얼에서는 세세하게 하나하나 적용법을 알려드리지는 않을 겁니다. 대신 '고기 잡는 법'을 알려드립니다.

위젯을 넣기 위해 우선 알아야 할 사항들은 **위젯의 넣을 화면의 스킨 파일과 해당 모듈에서 사용하는 문서의 변수명**입니다. 게시판 모듈을 예로 들면 view_document.html 파일이 본문 화면을 담당하는 스킨 파일이고, $oDocument가 문서의 변수명입니다.

위와 같이 스킨 파일과 변수명을 알아냈으면 이제 해당 스킨 파일의 적당한 위치에 아래 코드를 이용하여 위젯을 추가합니다.

{% highlight html %}
<img class="zbxe_widget_output" widget="socialxe_comment" skin="스킨명" colorset="컬러셋" document_srl="{$문서 변수->document_srl}" content_link="{getFullUrl('', 'document_srl', $문서 변수->document_srl, 'dummy', '1')}" content_title="{htmlspecialchars($문서변수->getTitleText())}" enter_send="Y|N" />
{% endhighlight %}

위 코드에서 '스킨명', '컬러셋', '문서 변수' 그리고 엔터시 등록되도록 할 것인지 여부를 결정하는 enter_send 부분만 변경하시면 됩니다. 게시판 모듈에 넣는 코드를 예를 들면 아래와 같을 겁니다.

{% highlight html %}
<img class="zbxe_widget_output" widget="socialxe_comment" skin="default" colorset="white" document_srl="{$oDocument->document_srl}" content_link="{getFullUrl('', 'document_srl', $oDocument->document_srl, 'dummy', '1')}" content_title="{htmlspecialchars($oDocument->getTitleText())}" enter_send="Y" />
{% endhighlight %}

게시판과 텍스타일에 적용하는 자세한 방법이 블로그에 소개되어 있습니다. 참고하시기 바랍니다.

- SocialXE 댓글을 Textyle에 적용하기
- 게시판에 SocialXE 댓글을 적용하기

<div class="pull-left">
	<a class="btn btn-default" href="../소셜-댓글/">< 소셜 댓글</a>
</div>

<div class="pull-right">
	<a class="btn btn-default" href="../소셜-로그인/">소셜 로그인 ></a>
</div>

<script>
	set_pills('toc_5-2');
</script>