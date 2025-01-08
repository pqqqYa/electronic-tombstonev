# 一. 常见的字符串处理

好的！我们再来看一个同样适合初学者的例子，涉及简单的字符串操作的业务逻辑，比如实现一个工具类 `StringUtil`，包括一些常见的字符串处理方法。然后为其编写对应的测试代码。

---

### **业务代码**

假设我们有一个名为 `StringUtil` 的工具类，它提供以下方法：
1. 判断字符串是否为空或仅包含空白字符。
2. 将字符串反转。
3. 检查两个字符串是否为回文（忽略大小写）。
4. 将字符串的首字母大写。

```java
package review;

public class StringUtil {

    // 判断字符串是否为空或仅包含空白字符
    public boolean isBlank(String str) {
        return str == null || str.trim().isEmpty();
    }

    // 将字符串反转
    public String reverse(String str) {
        if (str == null) {
            return null; // 空字符串直接返回 null
        }
        return new StringBuilder(str).reverse().toString();
    }

    // 检查两个字符串是否为回文（忽略大小写）
    public boolean isPalindrome(String str1, String str2) {
        if (str1 == null || str2 == null) {
            return false; // 任何一个字符串为 null 都不是回文
        }
        String reversed = new StringBuilder(str2).reverse().toString();
        return str1.equalsIgnoreCase(reversed); // 忽略大小写比较
    }

    // 将字符串的首字母大写
    public String capitalize(String str) {
        if (str == null || str.isEmpty()) {
            return str; // 空字符串直接返回
        }
        return str.substring(0, 1).toUpperCase() + str.substring(1); // 首字母大写
    }
}
```

---

### **测试代码**

针对 `StringUtil` 类的方法，我们编写单元测试，测试各种正常和异常输入的情况：

```java
package review;

import static org.junit.Assert.*; // 导入断言方法
import org.junit.Test; // 导入测试注解

public class StringUtilTest {

    // 测试 isBlank 方法
    @Test
    public void testIsBlank() {
        StringUtil util = new StringUtil();
        assertTrue("空字符串应该返回 true", util.isBlank("")); // 空字符串
        assertTrue("只有空格的字符串应该返回 true", util.isBlank("   ")); // 空格字符串
        assertTrue("null 应该返回 true", util.isBlank(null)); // null
        assertFalse("非空字符串应该返回 false", util.isBlank("hello")); // 非空字符串
    }

    // 测试 reverse 方法
    @Test
    public void testReverse() {
        StringUtil util = new StringUtil();
        assertEquals("字符串反转不正确", "olleh", util.reverse("hello")); // 正常字符串
        assertEquals("空字符串反转应该返回空字符串", "", util.reverse("")); // 空字符串
        assertNull("null 反转应该返回 null", util.reverse(null)); // null
    }

    // 测试 isPalindrome 方法
    @Test
    public void testIsPalindrome() {
        StringUtil util = new StringUtil();
        assertTrue("回文检查失败", util.isPalindrome("madam", "madam")); // 完全一样的回文
        assertTrue("忽略大小写的回文检查失败", util.isPalindrome("Madam", "madam")); // 忽略大小写
        assertFalse("非回文字符串检查失败", util.isPalindrome("hello", "world")); // 非回文
        assertFalse("任何一个字符串为 null 都不应该是回文", util.isPalindrome(null, "madam")); // null 情况
    }

    // 测试 capitalize 方法
    @Test
    public void testCapitalize() {
        StringUtil util = new StringUtil();
        assertEquals("首字母大写失败", "Hello", util.capitalize("hello")); // 正常字符串
        assertEquals("已经首字母大写的字符串不应该改变", "Hello", util.capitalize("Hello")); // 已经首字母大写
        assertEquals("空字符串应该返回空字符串", "", util.capitalize("")); // 空字符串
        assertNull("null 应该返回 null", util.capitalize(null)); // null
    }
}
```

---

### **测试解释**

#### **1. 测试 `isBlank` 方法**

```java
@Test
public void testIsBlank() {
    StringUtil util = new StringUtil();
    assertTrue("空字符串应该返回 true", util.isBlank("")); // 空字符串
    assertTrue("只有空格的字符串应该返回 true", util.isBlank("   ")); // 空格字符串
    assertTrue("null 应该返回 true", util.isBlank(null)); // null
    assertFalse("非空字符串应该返回 false", util.isBlank("hello")); // 非空字符串
}
```

- 测试了 4 种输入情况：
  - 空字符串。
  - 仅包含空格的字符串。
  - `null`。
  - 非空字符串。

---

#### **2. 测试 `reverse` 方法**

```java
@Test
public void testReverse() {
    StringUtil util = new StringUtil();
    assertEquals("字符串反转不正确", "olleh", util.reverse("hello")); // 正常字符串
    assertEquals("空字符串反转应该返回空字符串", "", util.reverse("")); // 空字符串
    assertNull("null 反转应该返回 null", util.reverse(null)); // null
}
```

- 验证字符串反转的功能：
  - 正常字符串的反转。
  - 空字符串的反转（应返回空字符串）。
  - `null` 输入的处理（应返回 `null`）。

---

#### **3. 测试 `isPalindrome` 方法**

```java
@Test
public void testIsPalindrome() {
    StringUtil util = new StringUtil();
    assertTrue("回文检查失败", util.isPalindrome("madam", "madam")); // 完全一样的回文
    assertTrue("忽略大小写的回文检查失败", util.isPalindrome("Madam", "madam")); // 忽略大小写
    assertFalse("非回文字符串检查失败", util.isPalindrome("hello", "world")); // 非回文
    assertFalse("任何一个字符串为 null 都不应该是回文", util.isPalindrome(null, "madam")); // null 情况
}
```

- 测试了回文检查：
  - 两个字符串是完全一样的回文。
  - 忽略大小写的回文。
  - 非回文字符串。
  - 输入 `null` 的处理。

---

#### **4. 测试 `capitalize` 方法**

```java
@Test
public void testCapitalize() {
    StringUtil util = new StringUtil();
    assertEquals("首字母大写失败", "Hello", util.capitalize("hello")); // 正常字符串
    assertEquals("已经首字母大写的字符串不应该改变", "Hello", util.capitalize("Hello")); // 已经首字母大写
    assertEquals("空字符串应该返回空字符串", "", util.capitalize("")); // 空字符串
    assertNull("null 应该返回 null", util.capitalize(null)); // null
}
```

- 验证了字符串首字母大写的功能：
  - 正常字符串首字母大写。
  - 已经首字母大写的字符串保持不变。
  - 空字符串直接返回空字符串。
  - 输入 `null` 返回 `null`。

# 二. 奇偶数判段

好的，再举一个难度更低的例子！这次我们选择一个简单的业务逻辑，比如实现一个判断整数奇偶性的功能，并为其编写测试代码。

---

### **业务代码**

假设我们有一个名为 `NumberUtil` 的工具类，它提供以下两个方法：
1. 判断一个整数是否是偶数。
2. 判断一个整数是否是奇数。

```java
package review;

public class NumberUtil {

    // 判断一个整数是否是偶数
    public boolean isEven(int number) {
        return number % 2 == 0;
    }

    // 判断一个整数是否是奇数
    public boolean isOdd(int number) {
        return number % 2 != 0;
    }
}
```

---

### **测试代码**

针对 `NumberUtil` 类的方法，我们编写对应的单元测试。

```java
package review;

import static org.junit.Assert.*; // 导入断言方法
import org.junit.Test; // 导入测试注解

public class NumberUtilTest {

    // 测试 isEven 方法
    @Test
    public void testIsEven() {
        NumberUtil util = new NumberUtil();
        assertTrue("4 应该是偶数", util.isEven(4)); // 测试偶数
        assertTrue("0 应该是偶数", util.isEven(0)); // 测试 0
        assertFalse("5 应该不是偶数", util.isEven(5)); // 测试奇数
        assertTrue("-6 应该是偶数", util.isEven(-6)); // 测试负偶数
    }

    // 测试 isOdd 方法
    @Test
    public void testIsOdd() {
        NumberUtil util = new NumberUtil();
        assertTrue("5 应该是奇数", util.isOdd(5)); // 测试奇数
        assertFalse("4 应该不是奇数", util.isOdd(4)); // 测试偶数
        assertFalse("0 应该不是奇数", util.isOdd(0)); // 测试 0
        assertTrue("-3 应该是奇数", util.isOdd(-3)); // 测试负奇数
    }
}
```

---

### **代码解释**

#### **1. 测试 `isEven` 方法**

```java
@Test
public void testIsEven() {
    NumberUtil util = new NumberUtil();
    assertTrue("4 应该是偶数", util.isEven(4)); // 测试偶数
    assertTrue("0 应该是偶数", util.isEven(0)); // 测试 0
    assertFalse("5 应该不是偶数", util.isEven(5)); // 测试奇数
    assertTrue("-6 应该是偶数", util.isEven(-6)); // 测试负偶数
}
```

- **`assertTrue`**：验证结果为 `true` 的情况（偶数）。
- **`assertFalse`**：验证结果为 `false` 的情况（奇数）。
- 测试了以下情况：
  - 一个正偶数（`4`）。
  - 特殊情况：`0`（偶数）。
  - 一个奇数（`5`）。
  - 一个负偶数（`-6`）。

---

#### **2. 测试 `isOdd` 方法**

```java
@Test
public void testIsOdd() {
    NumberUtil util = new NumberUtil();
    assertTrue("5 应该是奇数", util.isOdd(5)); // 测试奇数
    assertFalse("4 应该不是奇数", util.isOdd(4)); // 测试偶数
    assertFalse("0 应该不是奇数", util.isOdd(0)); // 测试 0
    assertTrue("-3 应该是奇数", util.isOdd(-3)); // 测试负奇数
}
```

- **`assertTrue`**：验证结果为 `true` 的情况（奇数）。
- **`assertFalse`**：验证结果为 `false` 的情况（偶数）。
- 测试了以下情况：
  - 一个正奇数（`5`）。
  - 一个偶数（`4`）。
  - 特殊情况：`0`（不是奇数）。
  - 一个负奇数（`-3`）。

---

### **运行测试**

#### **运行步骤**：
1. 将 `NumberUtil` 和 `NumberUtilTest` 编写完成。
2. 在 IDE 中运行 `NumberUtilTest` 测试类：
   - 使用 IntelliJ IDEA 或 Eclipse，右键测试类，选择 **Run As > JUnit Test**。
3. 所有测试通过时，显示绿色进度条。如果某个测试失败，则显示红色，并提示失败的断言和相关信息。

#### **运行结果（通过时）：**

所有测试通过时，控制台输出：
```
Tests run: 2, Failures: 0, Errors: 0, Skipped: 0
```

#### **运行结果（失败时）：**

如果 `isEven` 方法实现错误（例如返回 `false`），控制台会显示类似错误信息：
```
java.lang.AssertionError: 4 应该是偶数
    at org.junit.Assert.fail(Assert.java:88)
    at org.junit.Assert.assertTrue(Assert.java:41)
    at review.NumberUtilTest.testIsEven(NumberUtilTest.java:10)
```

这表明在 **`testIsEven`** 方法中，断言失败。

# 三. 正负数判断

好的！再来一个简单易懂的例子，这次的业务逻辑是实现一个**数字判断工具**，包括判断数字是否为正数、负数或零。

---

### **业务代码**

`NumberChecker` 类实现以下方法：
1. 判断数字是否为正数。
2. 判断数字是否为负数。
3. 判断数字是否为零。

```java
package review;

public class NumberChecker {

    // 判断数字是否为正数
    public boolean isPositive(int number) {
        return number > 0;
    }

    // 判断数字是否为负数
    public boolean isNegative(int number) {
        return number < 0;
    }

    // 判断数字是否为零
    public boolean isZero(int number) {
        return number == 0;
    }
}
```

---

### **测试代码**

我们为 `NumberChecker` 的三个方法编写单元测试。

```java
package review;

import static org.junit.Assert.*; // 导入断言方法
import org.junit.Test; // 导入测试注解

public class NumberCheckerTest {

    // 测试 isPositive 方法
    @Test
    public void testIsPositive() {
        NumberChecker checker = new NumberChecker();
        assertTrue("10 应该是正数", checker.isPositive(10)); // 测试正数
        assertFalse("-5 不应该是正数", checker.isPositive(-5)); // 测试负数
        assertFalse("0 不应该是正数", checker.isPositive(0)); // 测试 0
    }

    // 测试 isNegative 方法
    @Test
    public void testIsNegative() {
        NumberChecker checker = new NumberChecker();
        assertTrue("-5 应该是负数", checker.isNegative(-5)); // 测试负数
        assertFalse("10 不应该是负数", checker.isNegative(10)); // 测试正数
        assertFalse("0 不应该是负数", checker.isNegative(0)); // 测试 0
    }

    // 测试 isZero 方法
    @Test
    public void testIsZero() {
        NumberChecker checker = new NumberChecker();
        assertTrue("0 应该是零", checker.isZero(0)); // 测试 0
        assertFalse("10 不应该是零", checker.isZero(10)); // 测试正数
        assertFalse("-5 不应该是零", checker.isZero(-5)); // 测试负数
    }
}
```

---

### **代码解释**

#### **1. 测试 `isPositive` 方法**

```java
@Test
public void testIsPositive() {
    NumberChecker checker = new NumberChecker();
    assertTrue("10 应该是正数", checker.isPositive(10)); // 测试正数
    assertFalse("-5 不应该是正数", checker.isPositive(-5)); // 测试负数
    assertFalse("0 不应该是正数", checker.isPositive(0)); // 测试 0
}
```

- 测试了以下情况：
  1. 正数（`10`）。
  2. 负数（`-5`）。
  3. 零（`0`）。

- **`assertTrue`** 和 **`assertFalse`** 用于验证方法的返回值是否正确。

---

#### **2. 测试 `isNegative` 方法**

```java
@Test
public void testIsNegative() {
    NumberChecker checker = new NumberChecker();
    assertTrue("-5 应该是负数", checker.isNegative(-5)); // 测试负数
    assertFalse("10 不应该是负数", checker.isNegative(10)); // 测试正数
    assertFalse("0 不应该是负数", checker.isNegative(0)); // 测试 0
}
```

- 测试了以下情况：
  1. 负数（`-5`）。
  2. 正数（`10`）。
  3. 零（`0`）。

---

#### **3. 测试 `isZero` 方法**

```java
@Test
public void testIsZero() {
    NumberChecker checker = new NumberChecker();
    assertTrue("0 应该是零", checker.isZero(0)); // 测试 0
    assertFalse("10 不应该是零", checker.isZero(10)); // 测试正数
    assertFalse("-5 不应该是零", checker.isZero(-5)); // 测试负数
}
```

- 测试了以下情况：
  1. 零（`0`）。
  2. 正数（`10`）。
  3. 负数（`-5`）。

---

### **运行测试**

#### **运行步骤：**
1. 编写完成 `NumberChecker` 和 `NumberCheckerTest`。
2. 在 IDE 中右键测试类 `NumberCheckerTest`，选择 **Run As > JUnit Test**。
3. 如果所有测试通过，进度条会显示绿色。
4. 如果某个测试失败，显示红色，并提示断言失败的信息。

#### **运行结果（通过时）：**

所有测试通过时，控制台显示：
```
Tests run: 3, Failures: 0, Errors: 0, Skipped: 0
```

#### **运行结果（失败时）：**

如果 `isPositive` 方法实现错误（如改成 `return number >= 0`），控制台会显示类似错误信息：
```
java.lang.AssertionError: 0 不应该是正数
    at org.junit.Assert.fail(Assert.java:88)
    at org.junit.Assert.assertFalse(Assert.java:63)
    at review.NumberCheckerTest.testIsPositive(NumberCheckerTest.java:12)
```

---

### **总结**

- **业务代码简单明了**：`NumberChecker` 类提供了三个基本判断方法。
- **测试覆盖全面**：每个方法都测试了正数、负数和零的情况。
- **断言信息清晰**：测试中的断言信息便于调试。

这个例子适合初学者进一步理解单元测试的基本写法，同时巩固 JUnit 的断言方法和测试流程！ 😊
