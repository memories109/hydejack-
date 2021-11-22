---
title:  "github.io 포트폴리오 제작하기"
excerpt: "GitHub Blog 서비스인 github.io 블로그 시작"

categories:
  - Blog
tags:
  - Blog
last_modified_at: 2021-11-22T08:06:00-05:00
---

포트폴리오는 제작하기에 어떤 방법이 있을지 고민을 많이 하였다.
여러 참고 사이트 무료 홈페이지 제작 사이트등 이런저런 꼼수도 여러곳 보았다.

개발자라면 그래도 자신이 만든 포트폴리오가 필요해 보였다.
그래서 GitHub Page를 이용한 나만의 포트폴리오를 만들려고 한다. 

GitHub Blog 서비스의 이름은 Pages이다.

천천히 해보기로 하였다. 

GitHub Blog Page 생성하는 과정은 쉬워보였다. 

하지만 실상은 달랐다. 이게 뭐라고... 어려웠다
도메인 설정이나 나만의 커스텀 되어있는 블러그를 만드는것은 어려웠다. 
루비? Hydejack? 이게 무엇인가?

![Screenshot](https://drive.google.com/uc?export=view&id=1VCnN949u6AEM_AKTr2WgbcJWjBB5NXwI){:.lead width="1920" height="1080" loading="lazy"}

# Jekyll's What is ?
Jekyll은 여러 텍스트 파일로부터 정적 웹사이트 구축을 위한 파일을 생성해주는 프레임워크이다.
쉽게 말해서 Jekyll은 다양한 형식의 텍스트 파일을 웹 페이지 구성 요소인 HTML, CSS로 변환해준다.

Jekyll에서 특히 내가 좋아하는 기능은 Markdown으로 작성한 문서를 HTML 파일로 변환시켜주는 기능이다.
Markdown으로 한 줄 작성하면 그 한 줄은 HTML의 <p></p> 태그로 변환된다.
물론 단순히 변환만으로 끝나는 것이 아니다. 정적 웹사이트를 만든다는 목적에 맞게, 변환된 내용이 그럴듯한 웹 화면으로 보이게끔 자동화된 방법으로 페이지를 꾸미는 것을 돕는다.

또한 인터넷에 아주 많은 Jekyll Theme이 올라와 있으므로 웹 페이지를 빈 화면으로부터 하나하나 다 만들 필요가 없으며, 적당한 테마를 다운받고 가져다 쓰면 된다. 이쁜 테마를 선택했고 뷰가 맘에 든다면 별다른 수정없이 그저 포스팅만 해도 된다.

예를들어, 내 블로그의 데스크탑 모드 화면에서 상단 메뉴(Topbar)와 왼쪽 사이드바는 내가 직접 HTML, CSS를 수정 및 적용했다. 또 Jekyll의 도움으로 다른 페이지에서도 항상 이 2가지가 화면에 보이도록 자동화했다. (반응형 웹으로 만들었기 때문에 모바일 모드로 보면 좀 다르다.)
동시에 포스트 페이지의 글 부분은 Markdown으로 작성하였다. 이것을 Jekyll이 자동으로 HTML 파일로 변환했고, 나는 그저 Markdown 포스트가 HTML로 변환된 이후를 가정하고 항상 페이지의 중앙에 보이게끔 배치하였다 (Layout을 만들었다).

[#jekyllrb](https://jekyllrb.com/docs/)
