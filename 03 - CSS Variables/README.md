Try

- forEach 각 `.key` 마다 이벤트 적용
    - 메소드는 배열 요소마다 한 번씩 제공한 함수를 실행합니다.

    ``` js
    const inputs = document.querySelectorAll('.controls input');
    inputs.forEach(input => input.addEventListener('change', handleUpdate));
    inputs.forEach(input => input.addEventListener('mousemove', handleUpdate));
    ```

- css

    ``` js
    const suffix = this.dataset.sizing || '';
      document.documentElement.style.setProperty(`--${this.name}`, this.value + suffix);
    ```

    - :root{ --blur: 10px; }은 :root 선택자 안에 --blur라는 변수의 값은 10px이다. 즉 --blur = 10px 할당
    - 사용시에는 filter: blur(var(--blur)); 즉 var(--blur)로 사용
    - style.setProperty를 사용해 속성명+value+suffix를 사용해 지정한다.
    - suffix는 dataset를 활용