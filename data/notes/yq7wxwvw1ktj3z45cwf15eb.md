
Java framework for writing and running [[unit tests|ser216.unit-testing]].

## Classes

```mermaid
classDiagram
    class TestResult
    class Test {
        run(TestResult)
    }
    class TestSuite {
        run(TestResult)
        addTest()
    }
    class TestCase {
        run(TestResult)
        setUp()
        tearDown()
        runTest()
    }
    class ConcreteTestCase {
        setUp()
        tearDown()
        runTest()
    }
    class UnitToBeTested
    
    ConcreteTestCase -- UnitToBeTested
    TestCase <|-- ConcreteTestCase
    Test <|-- TestCase
    Test <|-- TestSuite
    TestResult <.. Test
    TestSuite *-- "*" Test 
```

## Other features

- GUI interface
- [Integration with Visual Studio Code](https://code.visualstudio.com/docs/java/java-testing)