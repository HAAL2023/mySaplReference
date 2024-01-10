---
layout: page
#title: Examples
permalink: /reference/Examples/
---

### Examples

The following example constitutes a full minimal SAPL unit test:

```
public class B_PolicyWithSimpleFunctionTest {

    private SaplTestFixture fixture;

    @BeforeEach
    void setUp() {
        fixture = new SaplUnitTestFixture("policyWithSimpleFunction.sapl");
    }

    @Test
    void test() {
        fixture.constructTestCaseWithMocks()
                .givenFunction("time.dayOfWeek", Val.of("SATURDAY"), times(1))
                .when(AuthorizationSubscription.of("willi", "read", "something"))
                .expectPermit()
                .verify();
    }
}
```

A lot of additional examples showcasing the various features of this SAPL test framework can be found in the demo project [here](https://github.com/heutelbeck/sapl-demos/tree/master/sapl-demo-testing/src/test/java/io/sapl/test).