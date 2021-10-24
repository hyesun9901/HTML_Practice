# HTML_Practice

MFC의 다이얼로그는 UI디자인의 한계가 있음!!ㅠㅠ
MFC가 제공해주는 CDHtmlDialog클래스를 사용하여 MFC다이얼로그 틀(?)안에 HTML로 디자인한 UI를 넣을 것...
그래서 html도 조금씩 하게되었다...!
(※완전 초보!!!!!※)

MFC다이얼로그는 호환성을 위해 Internet Explore7을 지원한다고한다..그래서 안 되는것도 많음
EX)border-radius?...

***MFC 다이얼로그에 HTML을 띄우는 종류**
**1. SetElementHtml();**
  -> html파일의 텍스트를 그대로 세팅하는 방식
  -> 디자인을 도와주는 text/css같은 태그는 사용할거면 MFC에서 HtmlDialog생성 시 생기는 .htm파일에다가 해줘야함!!
  -> 따라서 사용자가 디자인을 변경할 수 있도록 하려면 스타일은 MFC .htm파일 말고 띄우려는 html파일의 태그들의 <style>태그 내에서 지정해주는게 좋다!
  -> javascript도 MFC의 .htm파일에다가 해야 인식됨!(예시는 나중에 업로드 해야징~)
**2. Navigate("html파일경로");**
  -> html파일자체를 띄움 
  -> jquery/1.12.4 사용가능(상위버전은 스크립트 오류 발생)
  -> DOM Object 타입은 javascript에서 사용 불가ㅠㅠ (document.~~~~과 같이 object의 property를 지정하여 사용해야 한다)
	->예)onclick="getSum(event);"   <- event 는 DOM Ojbect 이므로 사용 불가!!!
	     onclick="getSum(document.getElementsByName('radio_1'));"사용 가능!!!
