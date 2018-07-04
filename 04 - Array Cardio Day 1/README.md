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
    - 1번째 인자로는 함수(인자 4개)
        - 1번째 인자 accumulator : 초기값이 설정되어 있으면 빈객체(`{}`), 그 다음부터는 리턴받은 값
        - 2번째 인자 value : 배열의 값
        - 3번째 인자 index : 배열의 인덱스
        - 4번재 인자 array : reduce를 호출한 배열
    - 2번재 인자로는 initialValue 초기값({})
    ``` js
    //let votes = ["kim", "hong", "lee", "hong", "lee", "lee", "hong"];
    /*
    votes.reduce((accumulator, value, index, array)=>{
        if(!accumulator[value]) { // 0이 false이므로 !0은 true
            accumulator[value] = 0;
        } else { 
            accumulator[value]++;
        }
        return accumulator
    },{});
    */
    let votes = ["kim", "hong", "lee", "hong", "lee", "lee", "hong"];
    votes.reduce((accumulator, value, index, array)=>{
      if(!accumulator[value]) {
          accumulator[value] = 0;
      } 
      accumulator[value]++;
      return accumulator
    },{});
    ```
- 비구조화할당
    - 비구조화 할당(destructuring assignment) 구문은 배열의 값이나 객체의 속성을 별개의 변수로 추출할 수 있게 하는 자바스크립트 식(expression)입니다.
    ``` js
    // Array
    let fruits = ["apple", "banana"];
    const [apple, banana] = fruits;
    // apple에는 "apple"
    // banana에는 "banana"

    // Object
    let city = { "korea" : "seoul", "japan" : "tokyo" };
    const { korea, japan } = city;
    // korea변수에는 "seoul"
    // japan변수에는 "tokyo"
    ```
- 알파멧 순서 살펴보기
    - 

[[JS #1] 자바스크립트 배열 메서드 1: forEach, map](https://medium.com/@hongkevin/js-1-%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EB%B0%B0%EC%97%B4-%EB%A9%94%EC%84%9C%EB%93%9C-1-foreach-map-b1cb1c2237d1)
[[JS #2] 자바스크립트 배열 메서드 2: filter, reject, every, some](https://medium.com/@hongkevin/js-2-%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EB%B0%B0%EC%97%B4-%EB%A9%94%EC%84%9C%EB%93%9C-2-filter-reject-every-some-4517f99fc998)
[[JS #3] 자바스크립트 배열 메서드 3, reduce 100% 활용법 (feat. egghead.io)](https://medium.com/@hongkevin/js-3-%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EB%B0%B0%EC%97%B4-%EB%A9%94%EC%84%9C%EB%93%9C-reduce-100-%ED%99%9C%EC%9A%A9%EB%B2%95-feat-egghead-io-97c679857ece)

