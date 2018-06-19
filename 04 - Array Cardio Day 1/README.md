Try

- sort
    - 본래 값을 변경한다.
    ``` js
    var fruit = ["banana", "melon", "apple"];
    fruit.sort();
    // ["apple", "banana", "melon"]
    ```
    - 기본 정렬 순서는 문자열 유니 코드 코드 포인트에 따릅니다.

    ``` js
    var number = [48, 34, 50, 23, 15, 25];
    number.sort( (a,b) => a - b );

    var str = ["b","c","a"];
    str.sort( (a,b) => a < b );
    ```
    - 숫자
        - `a - b`일때는 오름차순
        - `b - a`일때는 내림차순
    - 문자
        - `a, b`의 리턴값이 음수(a가 b보다 작을떄) 일때는 `a, b, c`순 오름차순
        - `a, b`의 리턴값이 양수(a가 b보다 클때) 일때는 `c, b, a`순 내림차순
- reduce
- 비구조화할당
- 알파멧 순서 살펴보기