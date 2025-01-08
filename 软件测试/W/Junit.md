# 一. Calculator的测试

下面是一个简单的基于 JUnit 的测试代码示例，适用于实现加减乘除的业务逻辑。假设你已经有一个名为 `Calculator` 的类，其中包含加减乘除方法。以下是步骤和代码：

---

### 1. 业务代码
```java
package review;

public class Calc {

    int add (int a, int b) {
        int c = a + b;
        return c;
    }
    int subtract (int a, int b) {
        int c = a - b;
        return c;
    }
    int multiply (int a, int b) {
        int c = a * b + 1;
        return c;
    }
    int divide (int a, int b) {
        int c ;
        if (b == 0) {
            throw new ArithmeticException("Divide by zero");
        }
        c = a / b;
        return c;
    }
    public static void main(String[] args) {
        Calc c = new Calc();
        int r = c.add(2, 1);
        if (r == 3) {
            System.out.println("test passed");
        } else {
            System.out.println("test failed");
        }
    }
}

```

---

### 2. 基于 JUnit 的测试代码

以下代码测试了每个方法的功能：

```java
package review;

import static org.junit.Assert.*;
import org.junit.Test;

public class Demo {

    @Test
    public void testAdd() {
        Calc c = new Calc();
        int r = c.add(2, 3);
        assertEquals(5, r); // 测试加法
    }

    @Test
    public void testSubtract() {
        Calc c = new Calc();
        int r = c.subtract(5, 3);
        assertEquals(2, r); // 测试减法
    }

    @Test
    public void testMultiply() {
        Calc c = new Calc();
        int r = c.multiply(3, 4);
        assertEquals(12, r); // 测试乘法
    }

    @Test
    public void testDivide01() {
        Calc c = new Calc();
        // 如果 divide 返回浮点数
        double r = c.divide(3, 2);
        assertEquals(1.5, r, 0.000001); // 测试除法，允许小误差

        // 如果 divide 返回整数
        // int r = c.divide(3, 2);
        // assertEquals(1, r);
    }
	
    //期望抛出ArithmeticException类型错误，
    //设置测试方法的执行时间限制为1ms
    @Test(expected = ArithmeticException.class, timeout = 1)
    public void testDivide02() {
        Calc c = new Calc();
        int r = c.divide(3, 0); // 测试除以 0 抛出异常
    }
}

```

# 二. 常用的assert

## 总结表格

| 断言方法                | 功能              |
| ------------------- | --------------- |
| 1.`assertEquals`    | 验证两个值是否相等       |
| `assertNotEquals`   | 验证两个值是否不相等      |
| `assertTrue`        | 验证条件是否为 `true`  |
| `assertFalse`       | 验证条件是否为 `false` |
| 5.`assertNull`      | 验证对象是否为 `null`  |
| `assertNotNull`     | 验证对象是否不为 `null` |
| `assertSame`        | 验证两个对象是否引用同一个对象 |
| `assertNotSame`     | 验证两个对象是否引用不同对象  |
| `assertArrayEquals` | 验证两个数组是否相等      |
| 10.`fail`           | 强制使测试失败         |

---

## **1. `assertEquals`**
用于验证**实际值**是否与**期望值**相等。

### 语法
```java
assertEquals(expected, actual);
assertEquals(message, expected, actual);
```
- `expected`：期望值。
- `actual`：实际值。
- `message`：断言失败时的错误提示信息（可选）。

### 示例
```java
assertEquals(5, 2 + 3); // 测试通过
assertEquals("结果不符合预期", 10, 2 * 5); // 测试通过
assertEquals("字符串比较", "hello", "he" + "llo"); // 测试通过
```

### 不仅限数值的比较

`assertEquals` 可以比较的不仅是数值，还包括字符串、布尔值、对象等各种数据类型，具体取决于被比较的数据及其 `equals` 方法的实现。


 **`assertEquals` 的适用类型**

1. **数值类型**
   - 比较两个数值是否相等：`assertEquals(5, 2 + 3);`

2. **字符串类型**
   - 比较两个字符串是否相等：`assertEquals("Hello", "He" + "llo");`

3. **布尔类型**
   - 验证布尔值是否一致：`assertEquals(true, 1 < 2);`

4. **对象类型**
   - 比较两个对象是否相等（调用对象的 `equals` 方法进行判断）。  
     示例：`assertEquals(new Integer(5), Integer.valueOf(5));`

5. **不适用数组类型**
   - 对于数组，可以使用 `assertArrayEquals`，因为数组需要逐元素比较：  
     `assertArrayEquals(new int[]{1, 2, 3}, new int[]{1, 2, 3});`

 **注意**
1. 对于浮点数比较，建议使用带精度参数的方法：  
   `assertEquals(expected, actual, delta)`，`delta` 是允许的误差范围。
   ```java
   assertEquals(3.14, 3.14159, 0.01); // 允许误差0.01
   ```

2. 如果比较数组，应使用 `assertArrayEquals`，因为普通的 `assertEquals` 比较的是对象引用，而不是数组内容。


---

## **2. `assertNotEquals`**
用于验证**实际值**是否与**不期望的值**不同。

### 语法
```java
assertNotEquals(unexpected, actual);
assertNotEquals(message, unexpected, actual);
```
- `unexpected`：不期望的值。
- `actual`：实际值。
- `message`：断言失败时的错误提示信息（可选）。

### 示例
```java
assertNotEquals(4, 2 + 3); // 测试通过
assertNotEquals("结果不应该相等", 8, 2 * 5); // 测试通过
```

---

## **3. `assertTrue`**
用于验证条件表达式是否为 **`true`**。

### 语法
```java
assertTrue(condition);
assertTrue(message, condition);
```
- `condition`：布尔条件。
- `message`：断言失败时的错误提示信息（可选）。

### 示例
```java
assertTrue(5 > 3); // 测试通过
assertTrue("值必须大于0", 10 > 0); // 测试通过
```

---

## **4. `assertFalse`**
用于验证条件表达式是否为 **`false`**。

### 语法
```java
assertFalse(condition);
assertFalse(message, condition);
```
- `condition`：布尔条件。
- `message`：断言失败时的错误提示信息（可选）。

### 示例
```java
assertFalse(5 < 3); // 测试通过
assertFalse("值不能为负", -1 > 0); // 测试通过
```

---

## **5. `assertNull`**
用于验证对象是否为 **`null`**。

### 语法
```java
assertNull(actual);
assertNull(message, actual);
```
- `actual`：实际值。
- `message`：断言失败时的错误提示信息（可选）。

### 示例
```java
Object obj = null;
assertNull(obj); // 测试通过
assertNull("对象应该为 null", obj); // 测试通过
```

---

## **6. `assertNotNull`**
用于验证对象是否 **不为 `null`**。

### 语法
```java
assertNotNull(actual);
assertNotNull(message, actual);
```
- `actual`：实际值。
- `message`：断言失败时的错误提示信息（可选）。

### 示例
```java
Object obj = new Object();
assertNotNull(obj); // 测试通过
assertNotNull("对象不应该为 null", obj); // 测试通过
```

---

## **7. `assertSame`**
用于验证两个对象是否引用的是**同一个对象**（内存地址相同）。

### 语法
```java
assertSame(expected, actual);
assertSame(message, expected, actual);
```
- `expected`：期望的对象。
- `actual`：实际的对象。
- `message`：断言失败时的错误提示信息（可选）。

### 示例
```java
String str1 = "hello";
String str2 = str1;
assertSame(str1, str2); // 测试通过
assertSame("两个对象引用应该相同", str1, str2); // 测试通过
```

---

## **8. `assertNotSame`**
用于验证两个对象是否引用的是**不同的对象**（内存地址不同）。

### 语法
```java
assertNotSame(unexpected, actual);
assertNotSame(message, unexpected, actual);
```
- `unexpected`：不期望的对象。
- `actual`：实际的对象。
- `message`：断言失败时的错误提示信息（可选）。

### 示例
```java
String str1 = new String("hello");
String str2 = new String("hello");
assertNotSame(str1, str2); // 测试通过
assertNotSame("两个对象引用不应该相同", str1, str2); // 测试通过
```

---

## **9. `assertArrayEquals`**
用于验证两个数组是否相等（包括长度和每个元素值都相等）。

**注意**：`assertArrayEquals` 只能验证 **一维数组**，对于多维数组，需要手动循环比较每个维度。

### 语法
```java
assertArrayEquals(expectedArray, actualArray);
assertArrayEquals(message, expectedArray, actualArray);
```
- `expectedArray`：期望的数组。
- `actualArray`：实际的数组。
- `message`：断言失败时的错误提示信息（可选）。

### 示例
```java
int[] expected = {1, 2, 3};
int[] actual = {1, 2, 3};
assertArrayEquals(expected, actual); // 测试通过
assertArrayEquals("两个数组应该相等", expected, actual); // 测试通过
```

---

## **10. `fail`**
强制使测试失败，用于明确标识代码中的逻辑问题。

### 语法
```java
fail();
fail(message);
```
- `message`：断言失败时的错误提示信息。

### 示例
```java
if (someCondition) {
    fail("逻辑错误：条件不应该满足");
}
```

# 三. 期望抛出异常

在 **JUnit 4** 中，可以通过在 `@Test` 注解中指定 `expected` 参数，声明测试方法期望抛出的异常类型。如果测试方法抛出了指定的异常，则测试通过；如果没有抛出或抛出其他类型的异常，测试将失败。

---

### 1. **语法格式**

```java
@Test(expected = 异常类型.class)
public void 方法名() {
    // 测试代码
}
```

- **`expected` 参数**：指定测试方法期望抛出的异常类型。
- **`异常类型.class`**：异常类的 `Class` 对象，例如 `NullPointerException.class`、`IllegalArgumentException.class` 等。

---

### 2. **示例**

#### **1. 测试抛出除以 0 的异常**

```java
@Test(expected = ArithmeticException.class)
public void testDivideByZero() {
    int result = 10 / 0; // 会抛出 ArithmeticException
}
```

- 测试方法调用了 `10 / 0`，这会抛出 `ArithmeticException`。
- 由于 `expected` 指定了 `ArithmeticException.class`，测试通过。

---

#### **2. 测试抛出空指针异常**

```java
@Test(expected = NullPointerException.class)
public void testNullPointer() {
    String str = null;
    str.length(); // 会抛出 NullPointerException
}
```

- 测试方法调用了 `str.length()`，而 `str` 为 `null`，会抛出 `NullPointerException`。
- 由于 `expected` 指定了 `NullPointerException.class`，测试通过。

---

#### **3. 测试抛出非法参数异常**

```java
@Test(expected = IllegalArgumentException.class)
public void testIllegalArgument() {
    Integer.parseInt("not a number"); // 会抛出 IllegalArgumentException
}
```

- 调用了 `Integer.parseInt("not a number")`，由于输入字符串不能解析为数字，抛出 `IllegalArgumentException`。
- 测试通过。

---

### 3. **注意事项**

1. **必须抛出指定类型的异常**
   - 如果测试方法没有抛出异常，或者抛出了与 `expected` 不匹配的异常，测试会失败。

2. **不能验证异常消息**
   - `@Test(expected = Exception.class)` 只能检查是否抛出指定的异常类型，但无法验证异常的具体消息内容。
   - 如果需要验证异常的消息，请使用其他方法（如 `try-catch` 或 `ExpectedException` 规则）。

---

### ***扩展：使用 ExpectedException 规则（可验证异常消息）**

如果需要在 **JUnit 4** 中验证异常的具体消息，可以使用 `ExpectedException` 规则：

**示例**

```java
import org.junit.Rule;
import org.junit.Test;
import org.junit.rules.ExpectedException;

public class ExceptionTest {
    @Rule
    public ExpectedException thrown = ExpectedException.none();

    @Test
    public void testExceptionWithMessage() {
        thrown.expect(IllegalArgumentException.class); // 指定异常类型
        thrown.expectMessage("Invalid input"); // 验证异常消息内容

        // 触发异常
        throw new IllegalArgumentException("Invalid input");
    }
}
```

- **`@Rule`** 定义了一个 `ExpectedException` 实例。
- 调用 `thrown.expect()` 指定期望的异常类型，调用 `thrown.expectMessage()` 验证异常消息。
- 如果抛出的异常类型和消息都符合预期，测试通过。
