JUnit


# 단위 테스트 프레임워크 이해하기
- 단위 테스트는 다른 모든 단위 테스트들과 독립적으로 실행되어야 한다.
- 프레임워크는 테스트 각각의 오류를 식별하고 보고해야 한다.
- 어떤 테스트를 실행할지 선택하기 쉬워야 한다.

# JUnit의 설계 목표
- 유용한 테스트를 작성하는 데 보탬이 되어야 한다.
- 시간이 지나도 가치가 변하지 않는 테스트를 작성하는 데 보탬이 되어야 한다.
- 코드 재사용을 통해 테스트 작성 비용을 낮추는 데 보탬이 되어야 한다.

💁 간단한 예시
public class CalculatorTest {
    @Test
    public void testAdd() {
        Calculator calculator = new Calculator();
        double result = calculator.add(10, 50);
        assertEquals(60, result, 0);
    }
}
< 설명 > 
1. 반드시 public 이어야 한다.
2. @Test 어노테이션을 사용하여 이 메서드가 단위 테스트 메서드임을 표시한다.
3. Calculator 클래스의 인스턴스를 생성 -- 객체 형태
4. assertEquals 메서드를 호출해 테스트 결과를 확인한다.
5. 반환형은 void이어야 하고, 파라미터를 받아서는 안된다.