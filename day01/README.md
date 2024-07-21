# Day 01  

![부스트캠프웹모바일 커버용](https://github.com/user-attachments/assets/a6e4b320-72b4-48f6-a1c7-011583dabed2)

<br>

## 모듈  
모듈은 분리된 파일 각각을 칭함  
또는 특정한 목적을 가진 라이브러리 하나로 구성  
여러 파일을 다루면서 모듈의 필요성 인식  

<br>

## Export
1. Named exports  
  여러값을 한번에 가져오는데 유용

````javascript
export { foo, bar };

const foo = [1, 2, 3, 4];
const bar = [5, 6, 7, 8];
````

<br>

2. Default exports
  모듈 당 딱 한개만 존재  
  가장 간단하게 export 가능

````javascript
class A {
  ...
}

export default A;
````

<br>

## 모듈 통합  
부모 모듈이 자식 모듈을 가져와서 다시 내보내기 가능  
여러 개의 모듈을 모아놓고 하나의 모듈 생성 가능  

````javascript
export foo from "bar.js";
````

<br>

````javascript
import foo from "bar.js";
export foo;
````

<br>

## Import

1. 모듈 전체 가져오기  

````javascript
import * as module from "module.js";
````
<br>

2. 하나의 멤버 가져오기  

````javascript
import { module } from "module.js";
````

<br>

3. 여러개의 멤버 가져오기  

````javascript
import { foo, bar } from "module.js";
````

<br>

4. 다른 이름으로 멤버 가져오기

````javascript
import { module as m } from "module.js";
````

<br>

5. 바인딩 없이 모듈만 실행

````javascript
import "module.js";
````

<br>

6. default export 가져오기

````javascript
import module from "module.js";
````

<br>
