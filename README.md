딱새의 리액트 스터디 자료
=============
#### 시작일 : 2020.09.14 🤨
<img src="https://static-cdn.jtvnw.net/jtv_user_pictures/1a82ef2b-023e-40fa-8d35-f278bedd9f9e-profile_image-300x300.png">

Record1.
-------------
#### Git❕
##### 깃으로 처음 협업 할 때의 기본 세팅을 기재 

* * *
#### Git->Local Repository❕
##### 1.git clone url (url:작업할 프로젝트를 fork하거나, 가져왔을때 git의 소스 코드를 가져오는 명령어이다. root project의 url이 아닌 본인 저장소 url)
##### 2.git remote add upstream url (url:root project 다른 협업자가 push하거나 변동이 있을때 기본 저장소에서 소스를 가져오기위한 remote local 저장소이다.)
##### 3.git fetch upstream & git merge upstream/master (remote 저장소에 root 저장소에 업로드된 소스를 fetch하고, 본인 로컬 저자송에 merge 한다. 이를 합친 과정이 pull이다.)
#### Local Repository->Git ❕
##### 4.git add . (본인이 작업한 파일을 PR에 올릴 준비를 한다.)
##### 5.git commit -m "msg" (PR에 올릴 때,git에 찍히는 메시지를 남긴다.)
##### 6.git push (커밋이 완료되면 최종적으로 깃 레파지토리에 본인이 작업한걸 보낸다.)
##### 7.이후 사이트에서 pull request를 클릭하여서 작업한 것을 root 저장소에 합쳐주자
* * * 
#### [Cookie&Session&Cache](https://www.youtube.com/watch?v=OpoVuwxGRDI) 🥨
##### Cookie
쿠키는 **클라이언트**가 가지고 있는 것, 임의로 고치거나 지울 수 있기에 보안성이 취약해 가벼운 정보들로 이루어져 있다.
##### Session
세션은 **서버**가 가지고 있는 것, 클라이언트의 중요 정보를 가지고 있으며 클라이언트와의 연결수단은 **임시키**를 이용해서 정보를 확인한다.
##### Cache
쿠키는 클라이언트가 서버측에서 정보를 요청하면 **재사용성을 대비하여** 서버사이드에서 임시로 저장하는 용어.
* * * 
#### TypeScript 🤨
수 많은 자바스크립트 문법중에 SPA의 호환성을 높인 스크립트 언어.
기본적으로 자바스크립트의 특징을 가진 객체지향성 정적언어이다.
초기 에러를 잡지못하는 자바스크립트와 다르게 타입스크립트는 선언을 초반부에 잡아준다.
컴파일하고 에러를 찾지 못하는 웹개발자들 ... 에게 얼큰한 돼지국밥같은 존재다.
* * *
#### Higher order Component(HOC)🎶
컨포넌트에 날개를 달아주는 기술이다.
한 컨포넌트를 사용하면 쓰고 버리기 아깝지않나... 라는 생각에서 나온 기술
보통은 AppBar같은 변동없는 컨포넌트들에서 사용하는 재사용성 기술이다
* * *
#### ServerSide&Client Rendering 📲
##### 클라이언트 사이드 렌더링
자바스크립트나 API에 대한 모든 데이터를 받은 후에 View에 렌더링 한다.
이는 검색엔진을 사용할 경우에 초기에 빈 페이지를 받기 때문에 검색엔진에는 적합하지 않다.
모든 것을 처음에 받기 때문에 쿠키에 부담이 너무 많아서 세션에 저장하여, 보안면이나 서버에 대한 부담이 많다.
페이지 요청마다 새로고침이 일어나지 않아서 트래픽 요소가 적다.
##### 서버 사이드 렌더링 
클라이언트에서 필요한 HTML파일만 렌더링한다. (그 외 요소는 렌더링이 되지는 않지만 클라이언트에게 표시는 해주지 않아, 이용면에서는 굉장히 빠르게 느껴진다.)
서버측에서 이미 렌더링을 한 데이터가 있기에 검색엔진이 데이터를 이용하기 수월하다.
변경된 부분만을 렌더링 해주기에 서버부담이 적다. 
* * * 
#### MVC&Flux Pattern 🤡
MVC에서는 애플리케이션이 점점 복잡해질수록, 컨트롤러가 많아지면서 서버 로직이 복잡하고 부담이 가기시작한ㄷ.
이를 해결하기 위해서 나온 패턴이 Flux패턴인데 이는 여러 컨트롤러를 하나의 Store를 만들어서 클라이언트가 실행(action)을 할 때마다,
Dispatch를 통해서 재귀적으로 사용했던 컨트롤러에 접근해서 로직을 간단하게 만든다 리액트에서는 React-Redux/React-Context를 사용하여 만들 수 있다.
* * * 
#### [Redux.context](https://velog.io/@velopert/typescript-context-api) 😊
Flux 패턴에 사용되는 React문법이다. 이는 Redux와 같이 사용하며 기본적으로 index.ts 루트 컨포넌트에 씌워주면서, 전역으로 데이터를 사용할 수 있게끔 하는 기술이다.
src경로에서 context라는 폴더를 만든 후에 context 구조를 만들고 provider라는 폴더를 만든 다음에 루트 컨포넌트에 Dispatch하여서, 씌워준다. 
여러곳에서 데이터를 서버에서 끌어오는 것의 귀찮음을 해결해주기 위해 등장하였지만 처음 사용하는 대에는 난이도가 생각보다 있다.
* * * 
#### Async ~ await 😊
기본적으로 서버와 클라이언트는 실시간 통신을 하기 때문에, 비동기통신 처리를 해야한다. 주고받는 오브젝트는 Promise객체로 선언되어 주고받기에 비동기 선언을 해주지 않으면 원치 않는 값이 제공 될 수도 있다.
아래 그림은 기본적인 서버통신에 status 상태에 대한 정보이다.
> ##### Server Status
> > * 200번대 : 정상작동
> > * 400번대 : 클라이언트 문제 및 서버 닫힘
> > * 500번대 : 서버문제
> > * 600번대 : DB문제 



