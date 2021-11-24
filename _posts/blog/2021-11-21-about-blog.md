---
title:  "Blog - Jekyll Hydejack 개념잡기"
excerpt: "GitHub Blog 서비스인 github.io 블로그 시작"
categories: [Blog, Jekyll]
tags:
  - Blog
last_modified_at: 2021-11-21T08:07:00-08:00
---


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


## jekyll Hydejack 구조 설명

> _config.yml
환경설정 정보를 담고 있다. head에 넣는 메타 정보3와 비슷한 정보를 담기도 하고 baseurl, url 등도 설정할 수 있다.

> _drafts
아직 게시하지 않은, 날짜 정보가 없는 Post를 보관할 수 있는 디렉터리이다.

>_includes
재사용할 수 있는 부분적으로 만들어진 html 파일을 보관할 수 있는 폴더이다. 예를 들면 header나 footer는 모든 곳에서 반복적으로 사용하기 때문에 include 폴더에 만들어놓고 가져다 쓰면 편하다. liquid 태그로 _include 안에 html을 소환할 수 있다.

>_layouts
default.html 은 최상위 Jekyll Blog 구성을 담고 있는 파일이라고 볼 수 있다. _include 폴더 안에 부분적인 html 들이 소환되어 있다. post.html 은 Post의 형태를 정의해놓은 html 파일이다.

>_posts
날짜별로 정렬되는 형태의 아이템이 모여있는 폴더이다. 파일명은 반드시 2018-01-28-title.md 형태를 띠어야 한다.

>_data
블로그에 사용할 수 있는 데이터를 모아놓을 수 있는 폴더이다. 확장자가 .yml, .yaml, .json, .csv 일 경우 자동으로 읽어 들여서 site.data 변수를 써서 불러올 수 있다.

>_site
Jekyll이 다른 디렉터리에 있는 모든 파일을 활용해서 Site로 자동 변환 작업을 마치면 그 파일들이 저장되는 폴더이다. _site 폴더 내 파일은 건드리면 안 된다.

>index.html
블로그에 접속했을 때 제일 먼저 자동으로 보여주는 파일이다.