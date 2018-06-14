Try

- transtionend 이벤트
    - `CSS transition`이 완료되었을때
    - transitionend 이벤트는 CSS 전환이 완료되면 시작됩니다. transition 속성이 제거되거나 display가 "none"으로 설정된 경우 이벤트가 발생되지 않는다.
    ``` js
    keys.forEach(key => key.addEventListener('transitionend', removeTransition));
    ```

- dataset
    - HTML5 명세
    ``` js
    <audio data-key="65" src="sounds/clap.wav"></audio>
    const audio = document.querySelector(`audio[data-key="${e.keyCode}"]`);

    document.querySelector(`audio[data-key="65"]`); // 이런식으로 접근 가능
    ```

- Array.from
    - 유사 배열 혹은 반복가능한 객체로부터 새 Array 인스턴스를 만듭니다.
    - Arguments, Map, String 등
    ``` js
    const keys = Array.from(document.querySelectorAll('.key'));
    ```

- forEach 각 `.key` 마다 이벤트 적용
    - 메소드는 배열 요소마다 한 번씩 제공한 함수를 실행합니다.

    ``` js
    keys.forEach(key => key.addEventListener('transitionend', removeTransition));
    ```