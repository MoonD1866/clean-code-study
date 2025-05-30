# Chapter 8: 경계

## 1. 외부 코드를 사용할 때 경계를 설정하라

### **외부 코드 사용의 문제점**  
프로젝트에서 외부 라이브러리나 다른 부서에서 제공하는 API를 사용할 때, 해당 외부 코드를 직접 호출하는 경우가 많다.<br>
하지만 이렇게 직접 호출하면 외부 코드의 변화나 문제가 내 코드에 영향을 미칠 수 있고,
또한 외부 코드의 동작을 완전히 파악하지 않은 상태에서 사용하는 것은 위험할 수 있다.<br>
이로 인해 코드의 유지보수성이 떨어지고, 버전 변경 또한 위험하다.

### **경계 설정 방식**  
외부 코드를 사용할 때는 외부 라이브러리나 API를 **경계 클래스로 래핑** 해서 사용하는 것이 좋음.<br>
경계 클래스는 외부 코드와의 의존성을 분리하고, 외부 코드에서 발생할 수 있는 문제를 관리할 수 있도록 도와준다.<br>
이렇게 하면 외부 코드가 변경되어도 내 코드에 미치는 영향을 최소화할 수 있다.

## 2. 외부 코드를 사용하는 방식 개선

외부 코드의 반환값을 그대로 사용하기보다는, 이를 **경계 클래스로 감싸서 처리**하는 것이 더 바람직하다.<br>
외부 코드의 반환값을 적절하게 처리할 수 있는 방법을 경계 클래스로 작성하는 것이 좋다.

## 3. 외부 코드 사용 시 경계 클래스를 만들라

외부 코드를 사용할 때는 경계 클래스를 만들어 해당 코드의 동작을 추상화하는 것이 중요하다.<br>
경계 클래스는 외부 라이브러리나 API와의 상호작용을 내부 로직에서 분리할 수 있게 해준다.<br>
이렇게 하면 외부 코드가 변경되어도 경계 클래스를 통해 변경 사항을 관리하고, 다른 부분에 영향을 미치지 않도록 할 수 있다.

## 4. 학습 테스트를 활용하라

외부 코드에 대한 이해를 높이고, 이를 안전하게 사용할 수 있는 방법을 학습하기 위해서는 **학습 테스트(Learning Test)**를 작성하는 것이 좋다.<br>
학습 테스트는 외부 코드의 동작을 이해하고, 이를 실제 코드에서 어떻게 사용할지 명확히 파악할 수 있는 방법이다.<br>
테스트를 통해 외부 코드의 사용법과 예상되는 결과를 미리 학습하고, 문제 발생 가능성을 줄일 수 있다.

## 5. 경계 클래스를 사용할 때의 장점

경계 클래스를 사용하면 외부 코드의 의존성을 잘 관리할 수 있다.<br>
또한 코드가 더 깔끔하고 유지보수가 용이.<br>
외부 코드의 변경에 영향을 덜 받으며, 새로운 외부 코드나 라이브러리로 변경이 필요할 때도 경계 클래스만 수정하면 됨<br>
따라서 경계 클래스를 사용하면 코드의 안정성과 재사용성이 높아진다.

## 6. 외부 코드의 변경을 추적하라

외부 코드를 사용할 때는 해당 코드의 버전 변경이나 업데이트가 있을 수 있다.<br>
따라서 외부 코드에 대한 버전 관리나 변경 사항을 주기적으로 확인하고, 필요 시 코드에 반영하는 것이 중요하다.<br>
이를 통해 외부 코드의 변경이 내 코드에 미치는 영향을 사전에 파악하고, 수정할 수 있다.
