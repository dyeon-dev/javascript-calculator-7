# javascript-calculator-precourse

## 기능 요구 사항

입력한 문자열에서 숫자를 추출하여 더하는 계산기를 구현한다.

- 쉼표(,) 또는 콜론(:)을 구분자로 가지는 문자열을 전달하는 경우 구분자를 기준으로 분리한 각 숫자의 합을 반환한다.
  - 예: "" => 0, "1,2" => 3, "1,2,3" => 6, "1,2:3" => 6
- 앞의 기본 구분자(쉼표, 콜론) 외에 커스텀 구분자를 지정할 수 있다. 커스텀 구분자는 문자열 앞부분의 "//"와 "\n" 사이에 위치하는 문자를 커스텀 구분자로 사용한다.
  - 예를 들어 "//;\n1;2;3"과 같이 값을 입력할 경우 커스텀 구분자는 세미콜론(;)이며, 결과 값은 6이 반환되어야 한다.
- 사용자가 잘못된 값을 입력할 경우 "[ERROR]"로 시작하는 메시지와 함께 Error를 발생시킨 후 애플리케이션은 종료되어야 한다.

## 구현 기능 목록

- Console.readLineAsync()으로 덧셈할 문자열을 입력값을 받고, Console.print()으로 결과를 출력한다. ✔️
- `구분자(, :)`로 구분할 조건에 `커스텀 구분자(//와 \n 사이에 위치하는 문자)`도 추가한다. ✔️
- `split`를 사용하여 문자열을 구분한다. ✔️
- 구분된 모든 숫자를 더한다. ✔️
- 숫자와 구분자가 없을 경우(아무 입력 없을 경우) 0 출력 ✔️

- 사용자가 잘못된 값을 입력할 경우 process.exit()가 아닌 다른 방식으로 프로그램을 `종료`한다.
  - 숫자 : 양수가 아닌 숫자나 숫자가 아닌 값을 입력했을 때 ERROR ✔️
  - 구분자 : 1개일 때는 무조건 구분자, 2개 이상일 때는 ERROR ✔️
  - 커스텀 구분자에서 `//`만 있고 `\n`가 없는 경우 ERROR ✔️
  - 숫자만 있을 경우 ERROR 출력 (구분자를 기준으로 분리한 각 숫자의 합을 반환하기 때문)
  - 구분자만 있을 경우 ERROR 출력 (구분자를 기준으로 분리한 각 숫자의 합을 반환하기 때문)

---

### 입출력 요구 사항

**입력**

- 구분자와 양수로 구성된 문자열

**출력**

- 덧셈 결과

```
결과 : 6
```

**실행 결과 예시**

```
덧셈할 문자열을 입력해 주세요.
1,2:3
결과 : 6
```
