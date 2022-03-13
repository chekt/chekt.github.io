---
layout: post
title: "Josh is here"
categories: Vue.js
writer: Josh
---

<!-- @format -->

# [03.10] Vuejs Started

------

- Vuejs란?

  - 유저 인터페이스를 만들기 위한 프로그레시브 프레임워크

    ![https://media.vlpt.us/images/rimo09/post/d73a99ba-3e22-46a4-92fa-61843a4b7fe0/image.png](https://media.vlpt.us/images/rimo09/post/d73a99ba-3e22-46a4-92fa-61843a4b7fe0/image.png)

    ![https://bulhwi.github.io/images/progressiveImage.PNG](https://bulhwi.github.io/images/progressiveImage.PNG)

    - Vue는 코어 라이브러리 > 컴포넌트 개발 > 클라이언트 사이드 라우팅 > 상태관리가 가능하다

      - 코어 라이브러리(선언적 렌더링Declarative Rendering)

        - “HTML 템플릿에 렌더링 대상을 선언적으로 기술해 데이터가 변경될 때마다 DOM을 반응적으로 렌더링하고 사용자 입력 데이터를 동기화 할 수 있다.”
          - 화면단 데이터 표현에 관한 기능들을 중점적으로 지원
          - 라우터, 상태 관리, 테스팅 등을 쉽게 결합할수 있다.
          - 명시적(선언적) 렌더링 {{data}} <div class="test">test</div>
            - 데이터와 DOM을 연결하여 반응형으로 제작되었다.
              - data의 값을 변경되면 자동적으로 변경된 값이 render된다.
            - HTML과 직접 상호작용없이 단일 DOM element에 연결되어 DOM을 제어.
            - HTML는 엔트리 포인트일뿐 다른 모든 것은 새롭게 생성된 Vue 인스턴스 내에서 발생.
              - 엔트리 포인트(entry point)
                - 파일을 합칠 때는 파일을 합치는 시작점이 되는 파일이 필요하고 이러한 파일을 시작점 혹은 엔트리 포인트(Entry point)라고 한다.

      - 컴포넌트 개발(Component System)

        - **“UI를 모듈화하여 재사용한다”**

          Vuejs의 컴포넌트의 구성은 Single File Component로 html, css, js가 하나로 묶여있다.

          일반적으로 개발할 때, UI의 구성에 따라 컴포넌트 분리를 진행한다. 하지만 보다 나은 Vuejs의 컴포넌트 개발을 위해서는 두가지를 확인하면 된다.

          - Props
            - Props가 많다는 것은 해당 컴포넌트가 특정한 부모 컴포넌트에 종속되었다는 의미이다.
            - 또한 props는 직접적인 변경이 불가하기에 data에 재바인딩, watch로 감지, $emit을 통한 이벤트전달하는 과정이 많지게 된다.
          - watch
            - watch가 많다는 것은 이미 해당 컴포넌트에서 반강제적으로 반응 적인 모델이 필요하다는 경우이다.
            - watch가 많아질 경우, Vue.js의 반응적 모델이 어플리케이션 성능에 영향을 주기에 성능을 저하시킬 수 있다. (React의 UseEffect도 마찬가지다)

          그렇기에 props와 watch를 최소화 하고 공통적인 methods는 따로 JS파일로 분리하는 것이 좋다.

          [참고](https://kdydesign.github.io/2019/04/27/vue-component/)

      - 클라이언트 사이드 라우팅(Client-Side Routing)

        - **“단일 페이지 어플리케이션이 동작하기 위해 필요한 영역으로 URL설계, 지시와 같이 Vue Router를 사용하여 구현할 수 있다.”**

          기존의 웹은 서버사이드 렌더링에 의존할 수 밖에 없었지만, 라우터를 통해 클라이언트 사이드 렌더링이 가능해졌다.

      - 대규모 상태관리(Large Scale State Management)

        **컴포넌트 간에 상태를 공유하는 방법을 필요로 하는 영역이다. Vuex를 사용하여 기존 컴포넌트를 확장하는 형태로 상태를 중앙에서 관리할 수 있다.**

      - 빌드 시스템(Build System)

        **웹어플리케이션을 구성하는 컴포넌트 관리, 운영환경배포, 프로젝트 구성 등과 관련된 영역이다.**

      - 데이터 퍼시스턴스(Client-Server Data Persistance)

        **웹어플리케이션의 복잡한 데이터는 클라이언트 사이드와 서버 사이드 양쪽 모두에서 퍼시스턴스 데이터로 유지돼야 한다. 서드파티 라이브러리 사용자들이 직접 작성한 라이브러리를 사용해 구현한다. (ex - axios, vue-apollo)**

      참고 : https://bulhwi.github.io/vuejs에서-제공하는-단계적영역/

  - SPA 프레임워크(리액트, 앵귤러)와 달리 Vue는 점진적으로 채택할 수 있다.

  - 핵심 라이브러리는 뷰 레이어만 초점을 맞추어 다른 라이브러리나 기존 프로젝트와의 통합이 쉽다.

  - Vue는 현대적 도구 및 지원하는 라이브러리와 함께 사용하여 SPA을 완벽지원할 수 있다.

    - 현대적 도구(modern toolling) : Single File Component
    - [지원하는 라이브러리](https://github.com/vuejs/awesome-vue#components--libraries)

- Vue.js vs Other Framworks

  - React

    - React와 Vue의 공통점

      - 가상 DOM을 활용한다.
      - 반응적이고 조합 가능한 컴포넌트를 제공한다.
      - 코어 라이브러리에만 집중하고 있고 라우팅 및 전역 상태를 관리하는 라이브러리가 있다.

    - Runtime Performance

      - 렌더링 성능

        - 리액트와 뷰는 UI를 렌더링하기 위해 필요한 DOM 조작수를 최소화한다. 가상 DOM 추상화를 사용하여 작업을 수행
        - Javascript의 오버헤드는 필요한 DOM 작업을 계산할 때, 사용된다.
        - 리액트에 비교하여 Vuejs의 가상돔 라이브러리(snabbdom)이 현저히 가벼워서 더 적은 오버헤드가 발생한다.
          - 이를 비교하기 위해 [벤치 마크 프로젝트](https://github.com/chrisvfritz/vue-render-performance-comparisons)를 사용하여 성능을 비교해냈다.

      - HTML & CSS

        - 리액트는 모든 것이 Javascript이다.

          - JSX를 통해서 HTML 구조가 들어와있고, CSS도 자바스크립트에서 한다.(style-component)

        - JSX vs Template

          - JSX의 장점

            JS를 통해 뷰를 만들기에, 임시 변수, 플로우 제어를 스코프 내에서 직접적으로 자바스크립트 값을 적용한다.

            JSX의 툴지원(linting, 타입검사, 자동완성)은 Vue template보다 좋다.

          - template의 장점

            - 쉽다

- 참고

  [React에서의 가상돔 개념](https://velog.io/@mollog/React에서의-가상돔-개념)

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]: https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
