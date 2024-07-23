# Day07

![부스트캠프웹모바일 커버용](https://github.com/user-attachments/assets/d640ce10-4cae-45f9-bccc-342ac0dcbe3b)

<br>

## 단위 테스트
메서드 단위 등 프로그램의 작은 단위로 테스트를 진행  

테스트에 걸리는 시간과 비용 절감 가능  

새로운 기능이 추가될 때 빠르게 테스트 가능  

각각의 테스트는 독립적이며 서로 의존하지 않아야 가능  

<br>

## 목 객체

단위 테스트는 항상 독립적  

하지만 실제 코드는 객체 간의 의존성 발생  

단위 테스트를 하는 동안, 의존성 제거를 위해서 가짜 목 객체 생성  

<br>

## Jest  

### 설치 방법
````
npm init -y
npm install --save-dev jest
````

<br>

### 패키지 파일 
package.json 파일에 아래 설정 추가  
````json
{
    "scripts": {
        "test": "jest"
    }
}
````

<br>

### Test Matcher

1. toBe()   
    객체가 아닌 기본형 값 비교에 사용  
       
    ````javascript
    test("test name", () => {
        expect(1 + 1).toBe(2);
    });
    ````

2. toEqual()  
    객체 검증에 사용   

    ````javascript
    test("test name", () => {
        expect(getUser()).toEqaul({id: 1, name: "jjeonghak"});
    });
    ````

3. toBeTruthy()/toBeFalsy()  
    검증값이 true/false 값으로 간주되는지 확인    

    ````javascript
    test("test name", () => {
        expect(null).toBeFalsy();
    });
    ````

4. toHaveLength()/toContain()  
    배열의 길이/포함을 검증  

    ````javascript
    test("test name", () => {
        const target = [1, 2, 3, 4, 5];
        expect(target).toHaveLength(5);
        expect(target).not.toContain(6);
    });
    ````

5. toMatch()  
    정규표현식을 만족하는지 검증  

    ````javascript
    test("test name", () => {
        const regex = /^[0-9]*$/;
        expect("1234").toMatch(regex);
    });
    ````

6. toThrow()  
    예외 발생 검증    

    ````javascript
    test("test name", () => {
        expect(() => throwMethod()).toThrow();
    });
    ````

<br>

### 테스트 실행
````
npm test
````


