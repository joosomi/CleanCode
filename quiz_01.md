## QUIZ 01.

Hint❕ : 검색하기 쉬운 이름을 사용하세요. <br>
blastOFF는 로켓 발사를 의미. 86400000은 하루의 밀리초 (milliseconds) 의미.
```
setTimeout(blastOff, 86400000);

// 개선된 코드
const ONE_DAY_IN_MS = 86400000; 
setTimeout(blastOff, ONE_DAY_IN_MS);
```

### 어떻게 고쳤는지, 사례에서 무엇을 배워야 하는지 설명해주세요.

숫자 86400000은 의미가 명확하지 않아서 가독성이 떨어지고, 추후 검색도 어려워진다. <br>
따라서 상수를 사용하여 코드의 의미를 명확하게 알아볼 수 있게끔 수정하였다. <br>

`매직 넘버(Magic Number)` : 코드에서 상수(static final)로 선언하지 않은 하드 코딩된(literal value) 일정한 값을 의미하는 숫자나 문자열 <br>

_되도록이면 매직 넘버를 사용하지 말자. 의미있는 이름을 사용하여 미래에 소요될 시간을 절약하자._

## QUIZ 02.

- Hint❕ : 의미있는 이름을 사용해 주세요.
```
const yyyymmdstr = moment().format("YYYY/MM/DD");

// 개선된 코드
const formattedDate = moment().format("YYYY/MM/DD");
```

### 어떻게 고쳤는지, 사례에서 무엇을 배워야 하는지 설명해주세요.
yyyymmdstr은 의도가 명확하지 않고 읽기도 어렵다. <br>
처음엔 그냥 date로 변수명을 수정할까 했지만,  <br>
포맷팅한 날짜를 나타내기 때문에 formattedDate로 선언하는 것이 더 의미를 이해하기 쉬울 것 같다.

_약어 보다는 명확한 의도를 드러내는 이름을 사용하자_

## QUIZ 03.
Hint❕ : 불필요하게 반복하지 마세요.
```
const Car = {
  carMake: "Honda",
  carModel: "Accord",
  carColor: "Blue"
};

function paintCar(car, color) {
  car.carColor = color;
}

// 개선된 코드
const car = {
  make: "Honda",
  model: "Accord",
  color: "Blue"
}

function changeColor(car, newColor) {
  car.color = newColor;
}
```
### 어떻게 고쳤는지, 사례에서 무엇을 배워야 하는지 설명해주세요.
car 접두어를 제거했다.
객체 자체가 이미 car이기 때문에 굳이 붙일 필요가 없다. <br>

그리고 color의 의미를 명확하게 하기 위해 함수 파라미터의 이름을 newColor로 수정하였고, <br>
함수의 의미를 명확하게 하기 위해 paintCar 대신 changeColor로 수정하였다.

_중복을 줄이고, 코드의 맥락을 명확히 나타낼 수 있는 이름을 사용하자_
