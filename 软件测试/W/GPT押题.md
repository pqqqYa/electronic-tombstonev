### 期末考试试卷 （一）
**课程：软件测试**  
**考试形式：闭卷**  
**题型分布：选择题（10题）、简答题（4题）、大题（4题）**  

---

#### **一、选择题（每题 5 分，共 50 分）**  

1. **以下关于黑盒测试的说法正确的是：**  
   A. 黑盒测试主要关注程序内部结构  
   B. 黑盒测试又称功能测试  
   C. 黑盒测试常用于检查逻辑覆盖  
   D. 黑盒测试需要对代码进行详细分析  
   <br>**答案：B**  

2. **白盒测试的主要目的是：**  
   A. 检查功能是否符合需求  
   B. 验证系统性能  
   C. 验证代码逻辑正确性  
   D. 检查用户界面设计  
   <br>**答案：C**  

3. **以下属于静态测试的是：**  
   A. 单元测试  
   B. 代码审查  
   C. 回归测试  
   D. 系统测试  
   <br>**答案：B**  

4. **以下测试属于动态测试的是：**  
   A. 静态代码分析  
   B. α测试  
   C. 检查需求文档  
   D. 编写测试计划  
   <br>**答案：B**  

5. **以下哪个选项不是单元测试的特点：**  
   A. 测试独立模块  
   B. 程序员负责执行  
   C. 涉及硬件和软件整体  
   D. 通常使用测试驱动开发  
   <br>**答案：C**  

6. **增量式集成测试的优点包括：**  
   A. 能一次性测试整个系统  
   B. 测试覆盖率低  
   C. 便于早期发现问题  
   D. 仅限于白盒测试方法  
   <br>**答案：C**  

7. **环形复杂度可以用于：**  
   A. 测试静态文档  
   B. 度量代码逻辑复杂性  
   C. 测试黑盒功能  
   D. 验证用户体验  
   <br>**答案：B**  

8. **以下关于条件覆盖的描述正确的是：**  
   A. 条件覆盖包含语句覆盖  
   B. 条件覆盖和路径覆盖完全相同  
   C. 条件覆盖需要检查每个判定的结果  
   D. 条件覆盖仅在白盒测试中使用  
   <br>**答案：C**  

9. **关于 Selenium 的描述正确的是：**  
   A. 只能进行 API 测试  
   B. 用于自动化测试 Web 应用  
   C. 不能测试动态网页  
   D. 不支持与 JUnit 集成  
   <br>**答案：B**  

10. **以下关于微服务架构测试的说法正确的是：**  
    A. 不需要进行集成测试  
    B. 只需测试单一服务的功能  
    C. 应重点关注接口和服务间通信测试  
    D. 微服务架构不适用回归测试  
    <br>**答案：C**  

---

#### **二、简答题（每题 10 分，共 40 分）**  

1. **简述黑盒测试和白盒测试的主要区别，并列举各自的常见测试方法。**  

2. **测试驱动开发（TDD）的主要流程是什么？如何通过测试驱动开发提高代码质量？**  

3. **软件测试的基本原则有哪些？请结合实例说明其重要性。**  

4. **嵌入式程序的测试方法有哪些特点？与普通软件测试有何异同？**  

---

#### **三、大题（每题 20 分，共 80 分）**  

1. **【代码测试题（JUnit）】**  
   给出如下代码：  
   ```java
   public class Calculator {
       public int add(int a, int b) {
           return a + b;
       }
       public int subtract(int a, int b) {
           return a - b;
       }
       public int multiply(int a, int b) {
           return a * b;
       }
       public int divide(int a, int b) throws ArithmeticException {
           if (b == 0) throw new ArithmeticException("Cannot divide by zero");
           return a / b;
       }
   }
   ```  
   **要求：**  
   编写 JUnit 测试用例，覆盖 `add`、`subtract`、`multiply` 和 `divide` 方法。  

2. **【自动化测试题（Selenium）】**  
   **要求：**  
   使用 Selenium 完成以下任务：  
   - 打开一个指定的网页（例如：www.example.com）。  
   - 登录测试账号（假设账号：test，密码：123456）。  
   - 验证页面标题是否为“Welcome”。  

3. **【逻辑覆盖】**  
   给定如下流程图，要求：  
   - 计算其环形复杂度；  
   - 写出实现“条件覆盖”的测试用例。  

   **流程图说明：**  
   ```  
      开始  
       ↓  
      判定A → 条件真 → 输出X  
       ↓条件假  
      判定B → 条件真 → 输出Y  
       ↓条件假  
      结束  
   ```  

4. **【等价类划分】**  
   某程序要求输入一个 0-100 的分数，程序将判断其所属的等级：  
   - [90, 100]: 优  
   - [80, 89]: 良  
   - [60, 79]: 中  
   - [0, 59]: 差  

   **要求：**  
   - 划分等价类（弱一般、强一般、弱健壮、强健壮）；  
   - 写出每类等价类对应的测试用例。  

<div class="page-break" style="page-break-before: always;"></div>


### 期末考试试卷（二）  
**课程：软件测试**  
**考试形式：闭卷**  
**题型分布：选择题（10题）、简答题（4题）、大题（4题）**  

---

#### **一、选择题（每题 5 分，共 50 分）**  

1. **黑盒测试中使用以下哪种方法：**  
   A. 等价类划分  
   B. 环形复杂度分析  
   C. 语句覆盖  
   D. 判定覆盖  
   <br>**答案：A**  

2. **以下不属于白盒测试的特点是：**  
   A. 使用代码覆盖分析工具  
   B. 检查内部逻辑  
   C. 基于系统的外部行为进行测试  
   D. 包括条件覆盖  
   <br>**答案：C**  

3. **动态测试的特点是：**  
   A. 在代码执行前完成  
   B. 必须依赖测试工具  
   C. 检查程序运行时的行为  
   D. 无法发现运行时错误  
   <br>**答案：C**  

4. **以下关于 α 测试的描述正确的是：**  
   A. 由开发团队执行，模拟真实用户环境  
   B. 由实际用户执行  
   C. 主要用于性能测试  
   D. 通常由开发团队在开发阶段执行  
   <br>**答案：A**  

5. **集成测试的主要目的是：**  
   A. 验证单个模块的功能  
   B. 测试模块之间的交互  
   C. 确保系统满足用户需求  
   D. 检查代码的逻辑覆盖率  
   <br>**答案：B**  

6. **以下关于持续集成的说法正确的是：**  
   A. 持续集成仅在项目上线后执行  
   B. 持续集成要求频繁集成代码并进行自动化测试  
   C. 持续集成必须覆盖所有的白盒测试方法  
   D. 持续集成的目标是减少测试成本  
   <br>**答案：B**  

7. **以下哪个属于白盒测试的逻辑覆盖方法：**  
   A. 等价类划分  
   B. 回归测试  
   C. 路径覆盖  
   D. α测试  
   <br>**答案：C**  

8. **关于弱健壮等价类划分的描述正确的是：**  
   A. 包括无效等价类和有效等价类  
   B. 只考虑有效输入的等价类  
   C. 等价类数量少于弱一般等价类  
   D. 仅在动态测试中使用  
   <br>**答案：A**  

9. **以下关于 JUnit 的描述正确的是：**  
   A. JUnit 是一种编写 Java 程序的 IDE  
   B. JUnit 用于自动化测试 Java 程序  
   C. JUnit 无法进行断言验证  
   D. JUnit 仅支持白盒测试  
   <br>**答案：B**  

10. **嵌入式系统测试的特殊性包括：**  
    A. 不需要考虑硬件环境  
    B. 必须重点测试用户界面  
    C. 需要考虑硬件和软件的协同测试  
    D. 测试只关注功能正确性  
    <br>**答案：C**  

---

#### **二、简答题（每题 10 分，共 40 分）**  

1. **简述动态测试和静态测试的区别，并举例说明静态测试在软件开发中的作用。**  
   **答案：**  
   - 动态测试：在程序运行过程中执行，验证运行时的功能、性能和行为。例如：单元测试、系统测试等。  
   - 静态测试：在程序未运行时完成，检查代码或文档的质量。例如：代码审查、需求文档检查等。  

2. **测试过程中，遵循的基本原则有哪些？举例说明每个原则的应用场景。**  
   **答案：**  
   - **测试应以用户需求为中心**（例如：测试用户登录功能是否符合需求）。  
   - **尽早介入测试工作**（例如：需求分析阶段进行需求验证）。  
   - **穷尽测试是不可能的**（例如：测试中通过等价类划分降低测试用例数量）。  

3. **什么是回归测试？如何在持续集成过程中应用回归测试？**  
   **答案：**  
   - 回归测试：在软件修改后，验证修改没有引入新的缺陷。  
   - 在持续集成中，自动化运行所有测试用例，以发现修改对现有功能的影响。  

4. **根据以下流图，计算环形复杂度，并写出独立路径：**  
   ```  
      开始  
       ↓  
      判定A → 条件真 → 输出X  
       ↓条件假  
      判定B → 条件真 → 输出Y  
       ↓条件假  
      结束  
   ```  
   **答案：**  
   - 环形复杂度 = 判定数 + 1 = 2 + 1 = 3  
   - 独立路径：  
     1. 开始 → 判定A条件真 → 输出X → 结束  
     2. 开始 → 判定A条件假 → 判定B条件真 → 输出Y → 结束  
     3. 开始 → 判定A条件假 → 判定B条件假 → 结束  

---

#### **三、大题（每题 20 分，共 80 分）**  

1. **【代码测试题（JUnit）】**  
   给出如下代码：  
   ```java
   public class MathUtils {
       public int square(int x) {
           return x * x;
       }
       public boolean isEven(int x) {
           return x % 2 == 0;
       }
   }
   ```  
   **要求：**  
   编写 JUnit 测试用例，覆盖 `square` 和 `isEven` 方法。  
   **答案：**  
   ```java
   import org.junit.Assert.*;
   import org.junit.Test;

   public class MathUtilsTest {
       MathUtils mathUtils = new MathUtils();

       @Test
       public void testSquare() {
           Assert.assertEquals(4, mathUtils.square(2));
           Assert.assertEquals(9, mathUtils.square(-3));
       }

       @Test
       public void testIsEven() {
           Assert.assertTrue(mathUtils.isEven(4));
           Assert.assertFalse(mathUtils.isEven(3));
       }
   }
   ```  

2. **【自动化测试题（Selenium）】**  
   **要求：**  
   使用 Selenium 完成以下任务：  
   - 打开百度首页。  
   - 搜索关键字“软件测试”。  
   - 验证页面标题中是否包含“软件测试”。  
   **答案：**  
```java
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import static org.junit.jupiter.api.Assertions.assertTrue;

public class SeleniumExample {
    public static void main(String[] args) {
        // 打开浏览器
        WebDriver driver = new ChromeDriver();
        driver.get("https://www.baidu.com");

        // 搜索“软件测试”
        WebElement searchBox = driver.findElement(By.id("search"));
        searchBox.sendKeys("软件测试");
        searchBox.sendKeys(org.openqa.selenium.Keys.RETURN);

        // 验证标题
        assertTrue(driver.getTitle().contains("软件测试"));

        // 关闭浏览器
        driver.quit();
    }
}
```

3. **【逻辑覆盖】**  
   **题目：** 对以下代码，编写测试用例，确保达到“条件覆盖”。  
   ```java
   public boolean isEligible(int age, boolean hasLicense) {
       return age >= 18 && hasLicense;
   }
   ```  
   **答案：**  
   - 条件覆盖测试用例：  
     1. age = 20, hasLicense = true （条件1、2均为真）  
     2. age = 17, hasLicense = true （条件1假，条件2真）  
     3. age = 20, hasLicense = false （条件1真，条件2假）  
     4. age = 17, hasLicense = false （条件1、2均为假）  

4. **【等价类划分】**  
   某登录系统要求：用户名长度必须在 6 到 12 个字符之间。  
   **要求：**  
   - 划分等价类；  
   - 写出每类等价类的测试用例。  
   **答案：**  
   - **等价类划分：**  
     1. 有效等价类：用户名长度在 [6, 12] 之间（如“abcdef”）。  
     2. 无效等价类：用户名长度 < 6（如“abc”）。  
     3. 无效等价类：用户名长度 > 12（如“abcdefghijklmn”）。  

   - **测试用例：**  
     1. 输入用户名“abcdef” → 有效  
     2. 输入用户名“abc” → 无效  
     3. 输入用户名“abcdefghijklmn” → 无效  



<div class="page-break" style="page-break-before: always;"></div>



### 期末考试试卷（三）  
**课程：软件测试**  
**考试形式：闭卷**  
**题型分布：选择题（10题）、简答题（4题）、大题（4题）**  

---

#### **一、选择题（每题 5 分，共 50 分）**  

1. **以下哪种测试属于黑盒测试：**  
   A. 逻辑覆盖  
   B. 边界值分析  
   C. 环形复杂度分析  
   D. 判定覆盖  
   <br>**答案：B**  

2. **软件测试的基本原则包括：**  
   A. 测试应尽量延后到开发完成后  
   B. 穷尽测试是可能的  
   C. 一个测试用例只能验证一个需求  
   D. 测试应尽早介入到项目中  
   <br>**答案：D**  

3. **以下关于单元测试的说法正确的是：**  
   A. 单元测试只关注性能问题  
   B. 单元测试主要由测试人员完成  
   C. 单元测试的目标是验证模块功能是否正确  
   D. 单元测试通常不使用自动化工具  
   <br>**答案：C**  

4. **关于增量式集成测试，以下描述正确的是：**  
   A. 一次性测试整个系统  
   B. 通过逐步增加模块来进行测试  
   C. 仅适用于黑盒测试方法  
   D. 无法发现模块之间的交互问题  
   <br>**答案：B**  

5. **以下关于动态测试的说法错误的是：**  
   A. 动态测试是在程序运行时进行的  
   B. 动态测试可以发现运行时错误  
   C. 动态测试不包括代码覆盖分析  
   D. 动态测试需要执行被测试的软件  
   <br>**答案：C**  

6. **以下哪种方法可以用来减少测试用例数量：**  
   A. 边界值分析  
   B. 语句覆盖  
   C. 等价类划分  
   D. 判定覆盖  
   <br>**答案：C**  

7. **回归测试的目的是：**  
   A. 验证新功能是否符合需求  
   B. 验证修改后的系统是否引入新的问题  
   C. 测试模块之间的接口  
   D. 测试系统性能是否达到要求  
   <br>**答案：B**  

8. **环形复杂度是用来衡量什么的？**  
   A. 代码的执行速度  
   B. 代码的逻辑复杂度  
   C. 系统的性能  
   D. 用户界面的友好程度  
   <br>**答案：B**  

9. **关于 Selenium，以下说法错误的是：**  
   A. Selenium 可用于自动化测试 Web 应用  
   B. Selenium 无法与其他测试框架集成  
   C. Selenium 支持模拟用户操作  
   D. Selenium 可以运行在不同的浏览器上  
   <br>**答案：B**  

10. **以下属于微服务架构测试的关键点是：**  
    A. 测试模块内部的逻辑覆盖  
    B. 测试硬件与软件的协作  
    C. 测试服务之间的接口和通信  
    D. 测试单个功能模块是否完整  
    <br>**答案：C**  

---

#### **二、简答题（每题 10 分，共 40 分）**  

1. **什么是边界值分析？结合实例说明边界值分析的应用。**  
   **答案：**  
   - 边界值分析是一种测试技术，用于检查输入值在边界处是否正确处理。  
   - **实例：** 如果一个系统要求输入的年龄在 18 到 60 岁之间，边界值测试用例包括：17（无效）、18（有效）、60（有效）、61（无效）。  

2. **白盒测试中环形复杂度的计算方法是什么？为什么要计算环形复杂度？**  
   **答案：**  
   - **环形复杂度计算公式：** `环形复杂度 = 判定数 + 1`。  
   - **作用：** 环形复杂度用于衡量代码的逻辑复杂性，帮助确定需要测试的独立路径数量。  

3. **什么是弱一般等价类和强健壮等价类？请举例说明两者的区别。**  
   **答案：**  
   - **弱一般等价类：** 仅考虑有效输入的等价类。例如，输入为 1-100，有效类为 [1, 100]，无效类可不考虑。  
   - **强健壮等价类：** 考虑所有有效和无效的输入类。例如，[1, 100] 是有效类，但还需要考虑小于 1 和大于 100 的无效类。  

4. **集成测试有哪些常见方法？简述自顶向下和自底向上的集成方法的优缺点。**  
   **答案：**  
   - **常见方法：** 自顶向下集成、自底向上集成、混合集成、持续集成。  
   - **自顶向下：**  
     - 优点：模块优先，方便发现高层问题。  
     - 缺点：需要使用很多桩模块。  
   - **自底向上：**  
     - 优点：低层模块测试充分。  
     - 缺点：无法尽早发现顶层问题。  

---

#### **三、大题（每题 20 分，共 80 分）**  

1. **【代码测试题（JUnit）】**  
   给出如下代码：  
   ```java
   public class StringUtils {
       public boolean isPalindrome(String str) {
           if (str == null) return false;
           return str.equals(new StringBuilder(str).reverse().toString());
       }
   }
   ```  
   **要求：**  
   编写 JUnit 测试用例，覆盖 `isPalindrome` 方法。  
   **答案：**  
   ```java
   import org.junit.Assert.*;
   import org.junit.Test;

   public class StringUtilsTest {
       StringUtils utils = new StringUtils();

       @Test
       public void testIsPalindrome() {
           Assert.assertTrue(utils.isPalindrome("madam"));
           Assert.assertFalse(utils.isPalindrome("hello"));
           Assert.assertFalse(utils.isPalindrome(null));
           Assert.assertTrue(utils.isPalindrome("a"));
       }
   }
   ```  

2. **【自动化测试题（Selenium）】**  
   **要求：**  
   使用 Selenium 完成以下任务：  
   - 打开某电商网站。  
   - 搜索商品“手机”。  
   - 验证搜索结果页面是否包含关键字“手机”。  
   **答案：**  
   ```python
   from selenium import webdriver
   from selenium.webdriver.common.keys import Keys

   driver = webdriver.Chrome()
   driver.get("https://www.example-ecommerce.com")

   search_box = driver.find_element("id", "search-bar")
   search_box.send_keys("手机")
   search_box.send_keys(Keys.RETURN)

   assert "手机" in driver.page_source

   driver.quit()
   ```  

3. **【逻辑覆盖】**  
   **题目：** 对以下代码，编写测试用例，确保达到“语句覆盖”和“条件覆盖”。  
   ```java
   public boolean isAdult(int age) {
       if (age >= 18) {
           return true;
       } else {
           return false;
       }
   }
   ```  
   **答案：**  
   - **语句覆盖：**  
     1. age = 20 （覆盖 if 条件为真的分支）  
     2. age = 15 （覆盖 if 条件为假的分支）  
   - **条件覆盖：**  
     1. age = 18 （条件为真）  
     2. age = 17 （条件为假）  

4. **【等价类划分】**  
   某银行系统要求输入的转账金额范围是 1 到 10,000。  
   **要求：**  
   - 划分等价类；  
   - 写出每类等价类的测试用例。  
   **答案：**  
   - **等价类划分：**  
     1. 有效等价类：金额在 [1, 10,000] 之间（如：500）。  
     2. 无效等价类：金额小于 1（如：-10）。  
     3. 无效等价类：金额大于 10,000（如：20,000）。  
   - **测试用例：**  
     1. 输入金额 500 → 有效  
     2. 输入金额 -10 → 无效  
     3. 输入金额 20,000 → 无效  

<div class="page-break" style="page-break-before: always;"></div>

### 期末考试试卷（四）  

#### **一、选择题（每题 3 分，共 30 分）**

  

1. 以下哪种测试方法主要关注软件的功能而不考虑内部结构？（ ）  
    A. 白盒测试  
    B. 黑盒测试  
    C. 静态测试  
    D. 灰盒测试
    
2. 在软件测试的四个级别中，一般由程序员执行的是（ ）。  
    A. 单元测试  
    B. 集成测试  
    C. 系统测试  
    D. 验收测试
    
3. TDD 是指（ ）。  
    A. 测试数据驱动  
    B. 测试文档驱动  
    C. 测试驱动开发  
    D. 测试设计驱动
    
4. 以下哪种测试不属于动态测试？（ ）  
    A. 黑盒测试  
    B. 白盒测试  
    C. 代码审查  
    D. α 测试
    
5. 自顶向下的集成测试是（ ）。  
    A. 从最底层模块开始组装和测试  
    B. 从最顶层模块开始组装和测试  
    C. 随机选择模块开始组装和测试  
    D. 从中间模块开始组装和测试
    
6. 计算环形复杂度的公式是（ ）。（其中 E 是边数，N 是节点数）  
    A. V (G)=E - N + 2  
    B. V (G)=E - N + 1  
    C. V (G)=E - N  
    D. V (G)=E + N - 1
    
7. 以下哪种逻辑覆盖要求设计足够的测试用例，使得判定中每个条件的所有可能结果至少出现一次？（ ）  
    A. 语句覆盖  
    B. 判定覆盖  
    C. 条件覆盖  
    D. 路径覆盖
    
8. 以下关于 Junit 的说法正确的是（ ）。  
    A. 不能用于测试方法  
    B. 主要用于 Web 自动化测试  
    C. 可以通过断言来判断测试结果  
    D. 不需要导入任何包
    
9. Selenium 主要用于（ ）。  
    A. 单元测试  
    B. Web 自动化测试  
    C. 嵌入式测试  
    D. 系统测试
    
10. 以下哪种等价类测试方法考虑了无效等价类的边界情况？（ ）  
    A. 弱一般等价类测试  
    B. 强一般等价类测试  
    C. 强健壮等价类测试  
    D. 弱健壮等价类测试
    

  

#### **二、简答题（每题 10 分，共 40 分）**

  

1. 简述黑盒测试和白盒测试的主要区别，并分别列举两种黑盒测试和白盒测试的方法。
    
2. 请说明单元测试、集成测试、系统测试和验收测试的主要目的和特点。
    
3. 解释什么是回归测试，并说明在什么情况下需要进行回归测试。
    
4. 请描述软件测试过程中应该遵循的三个基本的原则。
    

  

#### **三、大题（每题 15 分，共 60 分**

  

1. 已知以下程序流程图：  
    （此处请自行绘制一个简单的程序流程图，包含判断框和执行框等）  
    （1）计算该流程图的环形复杂度。  
    （2）写出该流程图的独立路径。  
    （3）根据独立路径，设计实现条件覆盖的测试用例。
    
2. 给定以下代码片段：

```
public class Calculator {
    public int add(int a, int b) {
        return a + b;
    }
    public int subtract(int a, int b) {
        return a - b;
    }
}
```
  
（1）使用 Junit 编写测试代码来测试 add 和 subtract 方法，要求使用断言来验证结果。  
（2）说明测试的思路和预期结果。

  

3. 请描述如何对一个 Web 应用进行 Selenium 自动化测试。包括导入包、打开网站、执行操作等基本步骤，并给出一个简单的示例（例如登录一个网站）。
    
4. 请分别简述微服务架构、嵌入式软件和移动应用（app）测试的特点和重点关注的内容。
    

  

#### **答案**

  

**一、选择题答案**

  

1. B。黑盒测试把软件看成一个黑盒子，只关注输入输出，不考虑内部结构。
2. A。单元测试一般由程序员来执行，用于测试最小的可测试单元。
3. C。TDD 是测试驱动开发的缩写。
4. C。代码审查属于静态测试，而黑盒测试、白盒测试和 α 测试都属于动态测试。
5. B。自顶向下的集成测试是从最顶层模块开始组装和测试。
6. A。环形复杂度公式是 V (G)=E - N + 2。
7. C。条件覆盖要求判定中每个条件的所有可能结果至少出现一次。
8. C。Junit 可以用于测试方法，通过断言来判断测试结果，需要导入相关包。
9. B。Selenium 主要用于 Web 自动化测试。
10. C。强健壮等价类测试考虑了无效等价类的边界情况。

  

**二、简答题答案**

  

1. - 区别：
        - 黑盒测试：不关注软件内部结构和代码，只关注软件的功能需求。它通过输入输出数据来验证软件是否满足功能要求。
        - 白盒测试：基于软件的内部结构和代码逻辑进行测试，主要用于检查程序的逻辑结构、代码路径等。
    - 黑盒测试方法：等价类划分、边界值分析。
    - 白盒测试方法：语句覆盖、路径覆盖。
2. - 单元测试：
        - 目的：验证软件中最小的可测试单元（如函数、方法等）是否正确实现了其功能。
        - 特点：通常由开发人员自己执行，测试范围小，针对性强，便于发现代码中的基本逻辑错误。
    - 集成测试：
        - 目的：将各个单元组合在一起测试，检查模块之间的接口是否正确，以及它们相互协作是否正常。
        - 特点：关注模块之间的交互，可能会发现单元测试时未发现的接口问题。
    - 系统测试：
        - 目的：对整个软件系统进行全面测试，确保系统满足功能、性能、安全等各方面的要求。
        - 特点：在接近实际运行环境下进行测试，测试范围广，能发现系统层面的问题。
    - 验收测试：
        - 目的：由用户或用户代表来验证软件是否满足业务需求和用户期望。
        - 特点：从用户角度出发，是软件交付前的最后一道测试工序。
3. - 回归测试是指在对软件进行修改（如修复缺陷、增加功能等）后，重新执行之前的测试用例，以确保修改没有引入新的错误，并且没有影响软件原有的功能。
    - 需要进行回归测试的情况：
        - 当修复了软件中的一个缺陷后，为了验证该修复没有影响其他功能。
        - 当增加了新的功能后，需要验证新功能与原有功能是否兼容，没有产生冲突。
        - 当对软件的配置、环境等进行了更改后，需要检查软件是否还能正常运行。
4. - 尽早和不断地测试：软件测试应该在软件开发的早期阶段就开始介入，并且贯穿整个软件开发周期。例如，在需求分析阶段就可以开始进行测试用例的设计，随着开发的进行不断完善和执行测试用例。
    - 完全测试是不可能的：由于软件系统的复杂性和输入输出的多样性，不可能对软件进行完全彻底的测试。因此，需要根据风险评估和测试目标，选择合适的测试策略和测试用例集，重点测试高风险和关键功能部分。
    - 测试用例应由测试输入数据和对应的预期输出结果组成：明确的测试输入和预期输出可以帮助测试人员准确地判断软件是否正确运行。例如，对于一个加法函数的测试用例，输入是 2 和 3，预期输出应该是 5。

  

**三、大题答案**

  

1. - （1）计算环形复杂度：
        - 首先确定节点数 N 和边数 E（根据自己绘制的流程图来确定），然后使用公式 V (G)=E - N + 2 计算环形复杂度。
    - （2）独立路径：
        - 通过分析流程图中的判断节点和循环结构，找出所有从起点到终点的独立路径。例如，如果有一个判断框（if - else），那么就会产生两条独立路径，一条是 if 分支的路径，一条是 else 分支的路径。
    - （3）测试用例设计：
        - 根据独立路径，为每条路径设计输入数据，使得能够覆盖路径中的条件。例如，如果一条独立路径中有一个条件是 x> 5，那么可以设计一个测试用例，让 x = 6 来满足这个条件。
2. - （1）测试代码：

  

收起

java

```
import org.junit.jupiter.api.Test;
import static org.junit.jupiter.api.Assertions.*;

public class CalculatorTest {
    @Test
    public void testAdd() {
        Calculator calculator = new Calculator();
        int result = calculator.add(3, 5);
        assertEquals(8, result);
    }
    @Test
    public void testSubtract() {
        Calculator calculator = new Calculator();
        int result = calculator.subtract(7, 3);
        assertEquals(4, result);
    }
}
```

  

- （2）测试思路：
    - 对于 add 方法，通过创建 Calculator 对象，调用 add 方法传入两个参数，然后使用断言 assertEquals 来验证方法返回的结果是否等于预期的结果（两个参数相加的结果）。
    - 对于 subtract 方法，同样创建对象，调用 subtract 方法传入两个参数，使用断言验证返回结果是否等于两个参数相减的结果。
    - 预期结果：测试用例中的 assertEquals 语句不会抛出异常，即实际结果和预期结果相等。

  

3. - 步骤：
        - 导入 Selenium 相关的包，如 WebDriver 等。例如，对于 Java，需要导入 org.openqa.selenium.WebDriver 和对应的浏览器驱动包（如 org.openqa.selenium.chrome.ChromeDriver）。
        - 创建 WebDriver 对象，指定浏览器类型。例如，使用 Chrome 浏览器：

  

收起

java

```
WebDriver driver = new ChromeDriver();
```

  

- 打开网站：使用 driver.get ("网站地址");，例如：

  

收起

java

```
driver.get("https://www.example.com");
```

  

- 执行操作：可以通过定位网页元素并执行操作，如点击按钮、输入文本等。例如，通过定位用户名输入框并输入用户名：

  

收起

java

```
WebElement usernameInput = driver.findElement(By.id("username"));
usernameInput.sendKeys("testuser");
```

  

- 示例（登录网站）：

  

收起

java

```
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.By;

public class SeleniumLoginTest {
    public static void main(String[] args) {
        System.setProperty("webdriver.chrome.driver", "chromedriver.exe路径");
        WebDriver driver = new ChromeDriver();
        driver.get("https://www.example.com/login");
        WebElement usernameInput = driver.findElement(By.id("username"));
        usernameInput.sendKeys("testuser");
        WebElement passwordInput = driver.findElement(By.id("password"));
        passwordInput.sendKeys("testpassword");
        WebElement loginButton = driver.findElement(By.id("loginButton"));
        loginButton.click();
        // 可以添加后续验证登录是否成功的操作
        driver.quit();
    }
}
```

  

4. - 微服务架构测试：
        - 特点：微服务架构由多个独立的微服务组成，每个微服务可以独立开发、部署和扩展。
        - 重点关注内容：服务间的接口测试，确保不同微服务之间的通信正确；每个微服务的功能测试，包括性能、可靠性等；分布式环境下的数据一致性测试。
    - 嵌入式软件测试：
        - 特点：嵌入式软件运行在特定的硬件设备环境中，对资源（如内存、CPU 等）的限制比较严格。
        - 重点关注内容：硬件相关的功能测试，如与外部设备的交互；实时性测试，确保软件能够在规定的时间内完成任务；资源使用情况测试，如内存泄漏检测等。
    - 移动应用（app）测试：
        - 特点：移动应用需要考虑不同的移动设备（如不同的屏幕尺寸、操作系统版本等）和移动网络环境。
        - 重点关注内容：功能测试，确保在不同设备和网络条件下功能正常；兼容性测试，包括操作系统版本兼容性、设备兼容性等；用户体验测试，如界面布局、操作流畅性等。


