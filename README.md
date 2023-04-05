# js-rollingTest





- index.html
: 기능 모아보기


----

### :computer: 작업


<details>
    <summary>rolling-css.html</summary>
    - 참고자료 :  JOY님 깃헙 (https://github.com/leejoys-lab/jslibrary)
    
    
   - css를 이용해서 text 옆으로 이동
  

</details>

<details>
<summary>rolling-js.html</summary>
    - 같은 내용으로 js를 이용하여 text 옆으로 이동
    

</details>

<details>
<summary>bannerrolling.html</summary>
    - 참고자료 : https://velog.io/@seoyaon/Javascript-%EC%9E%90%EB%8F%99-%EB%A1%A4%EB%A7%81-%EB%B0%B0%EB%84%88-%EB%A7%8C%EB%93%A4%EA%B8%B0
    
    
  - js를 이용하여 배너 옆으로 이동
</details>


-----


###  :question: 궁금증-1



```
<script>
// 롤링 배너 복제본 생성
let roller = document.querySelector('.rolling-list');
roller.id = 'roller1'; // 아이디 부여

let clone = roller.cloneNode(true)
// cloneNode : 노드 복제. 기본값은 false. 자식 노드까지 복제를 원하면 true 사용
clone.id = 'roller2';
document.querySelector('.wrap').appendChild(clone); // wrap 하위 자식으로 부착

document.querySelector('#roller1').style.left = '0px';
document.querySelector('#roller2').style.left = document.querySelector('.rolling-list ul').offsetWidth + 'px';
// offsetWidth : 요소의 크기 확인(margin을 제외한 padding값, border값까지 계산한 값)

roller.classList.add('original');
clone.classList.add('clone');
<script>
```

위 코드를 기반으로

```
<script>
// 롤링 배너 복제본 생성
let roller = document.querySelector('.rolling-list');

let clone = roller.cloneNode(true)
// cloneNode : 노드 복제. 기본값은 false. 자식 노드까지 복제를 원하면 true 사용

document.querySelector('.wrap').appendChild(clone); // wrap 하위 자식으로 부착


roller.classList.add('original');
clone.classList.add('clone');
<script>
```

이렇게 중간에 들어간 일부분을 지워도 작동은 되는데 
그럼 이렇게 적어도 되는지??



### :question: 궁금증-2

어차피 js로 작업해도 `cloneNode` 하고 css에서 `@keyframe` 거는건 똑같은데 굳이 js말고 
그냥 css로 작업하는게 맞는건지..? (css로 하는 것이 더 간편해 보임)
