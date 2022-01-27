# jest study

npm 설치하기

```
npm i -D jest
```

세팅

```json
{
  "scripts" {
    "test": "jest"
  }
}
```

`npm run test`를 터미널에 입력하여 실행

## Using Matchers

Jest는 matchers를 다양한 값을 test한다. 전체 목록은 [API](https://jestjs.io/docs/expect) 참고

### 사용해본 Matchers

- expect(value): 값을 테스트할때마다 사용된다.
- tobe: 값이 동일한지 확인하는 matcher (===? ==?)
- .not: 반대되는 경우도 확인할 수 있다.

```js
test('adding positive numbers is not zero', () => {
  for (let a = 1; a < 10; a++) {
    for (let b = 1; b < 10; b++) {
      expect(a + b).not.toBe(0);
    }
  }
});
```

- toEqueal: object 전체를 확인할때 사용

```js
test('object assignment', () => {
  const data = { one: 1 };
  data['two'] = 2;
  expect(data).toEqual({ one: 1, two: 2 });
});
```

expect(value)를 통해 생성된 값이 .tobe(value)와 동일한지에 대한 여부를 확인하는 것같다.

# CLI를 통한 방법 [채택 x]

## 바벨사용

- 추후에 필요할때 적용 [바벨사용](https://jestjs.io/docs/getting-started#using-babel)

## 고민거리

1.  이 함수들을 따로 실행하고 싶으면 어떻게 해야하나??
2.  다른 디렉토리에서 import 해올순 없나?
3.  어떤 상황에서 이러한 test를 적용할 수 있을까?
