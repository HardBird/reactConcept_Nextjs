딱새의 리액트 스터디 자료
=============
#### 시작일 : 2020.09.14 🤨
<img src="https://static-cdn.jtvnw.net/jtv_user_pictures/1a82ef2b-023e-40fa-8d35-f278bedd9f9e-profile_image-300x300.png">

Record1.
-------------
#### Git❕
##### 깃으로 처음 협업 할 때의 기본 세팅을 기재 
###### Accept Current Change -> 헤드 부분을 적용
##### Accept Incoming Change -> 변경된 부분을 적용(병합 대상이 된 브랜치의 내용으로 변경됨. 위에서 보여준 경우가 이에 해당됨)
##### Accept Both Change -> 둘다 적용(말그대로 헤드와 변경된 부분 둘다 남겨준다.
* * *
#### Git->Local Repository ❕ (fork작업)
##### 1.git clone url (url:작업할 프로젝트를 fork하거나, 가져왔을때 git의 소스 코드를 가져오는 명령어이다. root project의 url이 아닌 본인 저장소 url)
##### 2.git remote add upstream url (url:root project 다른 협업자가 push하거나 변동이 있을때 기본 저장소에서 소스를 가져오기위한 remote local 저장소이다.)
##### 3.git fetch upstream & git merge upstream/master (remote 저장소에 root 저장소에 업로드된 소스를 fetch하고, 본인 로컬 저자송에 merge 한다. 이를 합친 과정이 pull이다.)
#### Local Repository->Git ❕ (fork작업)
##### 4.git add . (본인이 작업한 파일을 PR에 올릴 준비를 한다.)
##### 5.git commit -m "msg" (PR에 올릴 때,git에 찍히는 메시지를 남긴다.)
##### 6.git push (커밋이 완료되면 최종적으로 깃 레파지토리에 본인이 작업한걸 보낸다.)
##### 7.이후 사이트에서 pull request를 클릭하여서 작업한 것을 root 저장소에 합쳐주자
* * *
#### 다른 브랜치의 작업을 옮기는 방법 ❕
##### 1.git add . 깃 작업을 추가한다
##### 2.git stash 기본적으로 stash는 스택 구조를 가지고 있다는 개념을 가지자. 스택에다가 add한 자료들을 넣어준다
##### 3.git checkout 브랜치이름 브랜치이름으로 브랜치를 이동한다 여기서 브랜치를 확인하는 방법은 gitbranch -a를 하면 된다.
##### 4.git stash pop stash 스택에 담겨있는 내용을 해당 브랜치에서 꺼낸다 
* * *
#### 깃 브랜치  
##### git init/git remote add를 한 가정하에 시작한다. (remote는 origin 이라 가정)
##### 1.git branch 브랜치이름 브랜치이름에 브랜치를 판다 
##### 2.git checkout 브랜치이름 브랜치이름으로 이동한다
##### 3.git push/pull origin 브랜치이름 (pull 브랜치로부터 내용을 받아온다 push 로컬작업을 브랜치로 전송한다. master로 하면 원격저장소에 대한 명령이 된다.)
* * *
#### 웹 작업을 pull 했는데 웹팩오류가 나타날때 
##### 1.노드모듈과 yarn.lock을 제거해준다.
##### 2.npm install을 설치해준다.
##### 3.yarn install도 실시해줘서 기본적인 패키지를 재설치한다. 
##### 처음부터 .gitignore를 해주면 되는데, 불가피한 상황이 오면 이렇게하자 ... 



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
단점을 나타내는 부분이라면, 타입에 대해서 정확하게 선언해줘서 에러를 잡아주는건데 사실상 시간이 급급하게 되면
타입에 any를 선언하여 어떠한 형태든지 다받게 할 수 있다. 근데 이렇게 써버리면 타입스크립트에 장점이 사라지게 되니
초기에 코드규칙을 잘 정학고 사용하자 
#### Typescript & React.context 
에러헨들링은 무조건 try~catch()문으로 에러를 처리해야한다. 해당 context를 제작하면서 provider에 유무로 에러헨들링을 하면 개발자 모드에서는 오류를 잡아내지 않지만,
타입스크립트 문법상 웹 배포에서는 에러 헨들링이 되지않아서 Dispatcher에 접근이 되지 않는다. 이는 기본적으로 try ~ catch 문에 익숙해진다면,
쉽게 해결할 수 있는 오류 구문이다.
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
MVC에서는 애플리케이션이 점점 복잡해질수록, 컨트롤러가 많아지면서 서버 로직이 복잡하고 부담이 가기시작한.
이를 해결하기 위해서 나온 패턴이 Flux패턴인데 이는 여러 컨트롤러를 하나의 Store를 만들어서 클라이언트가 실행(action)을 할 때마다,
Dispatch를 통해서 재귀적으로 사용했던 컨트롤러에 접근해서 로직을 간단하게 만든다 리액트에서는 React-Redux/React-Context를 사용하여 만들 수 있다.
* * * 
#### [Redux.context](https://velog.io/@velopert/typescript-context-api) 😊
Flux 패턴에 사용되는 React문법이다. 이는 Redux와 같이 사용하며 기본적으로 index.ts 루트 컨포넌트에 씌워주면서, 전역으로 데이터를 사용할 수 있게끔 하는 기술이다.
src경로에서 context라는 폴더를 만든 후에 context 구조를 만들고 provider라는 폴더를 만든 다음에 루트 컨포넌트에 Dispatch하여서, 씌워준다. 
여러곳에서 데이터를 서버에서 끌어오는 것의 귀찮음을 해결해주기 위해 등장하였지만 처음 사용하는 대에는 난이도가 생각보다 있다.
#### React UseEffect
무한 렌더링 오류에서 단비 같은 존재, 최초 렌더링시 한번만 실행을 시켜준다. useState나 서버통신에서 페이지네이션을 하거나 초기 값 세팅이 필요 할 때에 useEffect를 선언하여
렌더 이슈를 해결할 수 있다. 돔 트리 라이프 사이클에서는 마운트가 되기전에 미리 렌더링을 시켜준다고 이해하면 된다.
#### Next JS 배포시 렌더 이슈 해결법
서버사이드 렌더에 장점이자 단점이 된다. 클라이언트 측에서 렌더하지 않고 서버에서 렌더하기에 서버에 로직이 수행되기도 전에 렌더가 되어서 
윈도우나 도큐먼트를 찾을 수 없는 상황이 오게 된다. 그럴때 해결법은 Import하는 부분을 dynamic을 사용하여, 특정 부분만 클라이언트 사이드 렌더를 해주면
에러를 해결해줄수 있다.
#### [React UseMemo&CallBack](https://likejirak.tistory.com/48) 
callback 같은 경우에는 return을 하게되며 초기 값을 기억하고 호출하게 되고, usememon 같은 경우에는 초기 값이아닌 return 하는 값을 호출하게 된다.이는 useeffect처럼
렌더를 하는 개념이 아닌 값 자체만을 가지고 return을 해주기 때문에, 메모리 효율성을 높이는 기술이다. 다만 어중간하게 쓰게 되면 이도저도 아니게 되는 기술이 되기에 확실히 숙지하고 사용하자.
* * * 
#### Async ~ await 😊
기본적으로 서버와 클라이언트는 실시간 통신을 하기 때문에, 비동기통신 처리를 해야한다. 주고받는 오브젝트는 Promise객체로 선언되어 주고받기에 비동기 선언을 해주지 않으면 원치 않는 값이 제공 될 수도 있다.
아래 그림은 기본적인 서버통신에 status 상태에 대한 정보이다. 다만 스테이터스로 에러헨들링 처리를하려면 try ~ catch문으로 해결해주면 안된다. 애시당초 데이터는 전송이 되고 거기에 결과 값을 받기 때문에 
분기문을 사용하여 처리를 해주어야 한다.
> ##### Server Status
> > * 200번대 : 정상작동
> > * 400번대 : 클라이언트 문제 및 서버 닫힘
> > * 500번대 : 서버문제
> > * 600번대 : DB문제 
* * * 
#### Javascript local storage 👌🏻
JWT 자바토큰을 프론트엔드단에서 관리하면서 토큰을 기반으로한 이벤트를 제어하기 위한 자바스크립트 기술이다.
기본적으로 사용은 localstroage.setitem('이름',value)로 선언하면 되고 기본적인 데이터형은 string 이다. 이를 사용하는 이유는 데이터들이 새로고침을 하면 날아가는 context와다르게
사용자의 웹에 쿠키형태로 데이터를 임시저장한다. 주로 토큰값 같은 것을 저장할 때 사용하고 값을 가져올때는 localstroage.getitem('이름')으로 가져 올 수 있다. 
안드로이드에서 sharedpreferance 같은 개념으로 사용한다.
#### Javascript Cookies
로컬스토리지와 유사한 개념이다. 하지만 로컬스토리지는 보안성이 굉장히 취약해질수도 있다. 네트워크가 꺼져도 값이 유지되기 때문이다. 근데 이는 핸들링 하는 과정이 더 어려울수도 있으며,
특정 로짃에서 사용할 경우에는 분기처리로 계속해서 로컬스토리지를 관리해주어야한다. 그렇지만 단점만 있는것이 아니다. 영구성이 장점이 될 수 있으며 쿠키보다 더 많은 양을 저장할 수 있기 때문에 
상황에 따라서 로컬스토리지나 쿠키를 선택해서 사용하면 된다.
#### Javascript Hoisting 
HOC처럼 스크립트내에 선언한 변수를 어디서든 사용할 수 있게 전역변수처리로 위로 끌어올려서 사용하는 자바스크립트 기술이다. 우리가 코드상에서 위치를 바꾸는 것은 시각적으로만 보이지만,
실제 로직에서 메모리스택이 쌓이는 순서에는 변함이없다. 함수는 선언식에만 호이스팅이 적용되며, 표현식에는 적용되지 않는다. (선인식은 function(){} 표현식은 const temp = function(){})
#### Javascript && 와 ? 의 차이 
&&는 a&&a() 라는 함수 선언식을 쓰게 되면 a라는 함수가 있으면 실행을 하고, 없으면 그냥 그 행을 넘어간다. 
그렇다면 ?는 무슨 역할을 할까? 둘 다 분기처리를 하는건 동일하지만 a?.b.c 이런식으로 선언하면 a라는 인터페이스가 있으면 a.b.c로 차례로 접근한다.
단, a라는 인터페이스가 없으면 undefined를 내보내준다. 분기 처리후 반환 값이 있냐 없냐로 나뉠수 있다.
#### Javascript Date()
리액트에서는 시분초,밀리초에 대한 연산을 set,get() 함수를 이용하면 렌더링 이슈가난다. 그러므로 시간연산에 대해서는 new Date()를 통해서 새로운 date를 만들어서 연산을 시행하자.
#### Javascript 반응형 CSS ? 
기본적으로 웹에서는 축소와 확대에 따른 뷰가 변동이 되면 안된다. 하지만 별다른 핸들링 없이, 뷰를 구현하다보면 깨지는 부분을 발견할 수 있다. 이러한 부분은 
부모 컨포넌트위치에 DIV를 한개를 더 씌워줘서 minwidth:1903px를 선언해주면, 반응형처럼 사이트의 사이즈를 늘리거나 줄일때 뷰적인 부분이 깨지는 것을 막을 수 있다. 
이보다 효율적인 구현 방법이 있지만 임시방편으로 구현을 할 때에는 위와 같이 선언을 해주자.
#### JavaScript Closure
한 함수 내에서 여러 함수가 선언되어져 있을때, 연속적으로 그 함수에 접근하여 값을 업데이트하는 방법이다. 정보은닉과 캡슐화를 할 수 있는 이점을 가지고 있으며, 변수 선언을 할 때에 
변수에 해당된 함수에 연관이 없으면 같은 함수를 접근하더라도 클로저가 허용될 수 없다. 
* * *
#### Electron React
리액트 상에서 자바 스크립트가아닌 다른 C 문법을 사용해서, 리액트를 구현하는 법.
호환성이 굉장히 좋기에 많이 뜨는 라이브러리이다.

-coming : Server Deno
