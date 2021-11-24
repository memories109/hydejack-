---
title:  "Blog - GitHub Action 자동화 배포"
excerpt: "Github Action"

categories: [Blog, Git]
tags: [springboot, webrtc, jwt, redis, docker, nginx, mysql]
mermaid: true
---


# GitHub Action 자동화 배포
 이전 문서화 작업중에서 TravisCi에 대해서 언급한적이 있다
개발도중 만나게된 응답 오류, 빌드 시간, 커스텀 어려움 복잡도 기타등등 .....
그런 문제로 찾아본 결과 GitHub Action을 검토 하였으며 
속도측면이나 기존 GitHub 관리하는 입장에서 AccessTokene등록후 간단한 Workflows작성시 Git Push 이후에 자동 배포가 무척간편해 졌다

## GitHub Action 설정방법
 - 기본 설정 방법
![gitAction](/assets/customer/gitaction.png)
Github Action의 메뉴 구성들이다. Jekyll Workflow를 사용하기 설치 해준다. 

![gitAction](/assets/customer/gitaction2.png)
- 코드 
![gitAction](/assets/customer/blog4.png)

- 빌드 과정