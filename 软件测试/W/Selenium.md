# 一. 母版的基础讲解 

Selenium 的基本语法和页面操作。以下是一个简化的示例，同时详细解释每一步：

---

### 代码示例

```java
// 1. 导入必要的 Selenium 包
import org.openqa.selenium.*;
import org.openqa.selenium.chrome.*; // 控制 Chrome 浏览器

public class Example1 {         // 定义一个主类
    public static void main(String[] args) { 
        
    	// 固定配置
        // 2. 设置 ChromeDriver 的路径
	System.setProperty("webdriver.chrome.driver","C:/chromeDriver/chromedriver.exe");
        // 3. 创建一个 Chrome 浏览器对象
        WebDriver driver = new ChromeDriver();
        
	    try { 
			//固定操作
	        // 4. 打开一个网页(从打开网页后就开始try)
	        driver.get("https://example.com"); // 这里可以换成你要测试的网站
	
			//网页操作
	        // 5. 定位网页中的元素
	        // 比如，找到页面上的 "更多信息" 链接
	        WebElement link = driver.findElement(By.linkText("More information..."));
	        // 6. 对元素进行操作，比如点击这个链接
	        link.click();
        } catch (Exception e) {  
            // 处理异常  
            System.err.println("Error occurred: " + e.getMessage());  
        } finally {  
            // 7. 关闭浏览器  
            driver.quit();  
        } 
    }
}
```

---

### 代码运行流程
1. 设置驱动路径，启动 Chrome 浏览器。
2. 打开指定网页。
3. 定位到网页上的特定元素（例如一个链接）。
4. 对该元素进行操作（例如点击）。
5. 最后关闭浏览器。

---

### 扩展练习

为了让你更熟悉 Selenium，你可以尝试以下简单练习：
1. **输入文本**：在搜索框中输入内容。
   
   ```java
   WebElement searchBox = driver.findElement(By.name("q")); // 通过元素的 name 属性定位
   searchBox.sendKeys("Selenium 教程"); // 输入文本
   ```
2. **点击按钮**：找到并点击搜索按钮。
   
   ```java
   WebElement searchButton = driver.findElement(By.name("btnK")); // 定位按钮
   searchButton.click(); // 点击按钮
   ```
3. **获取文本**：获取页面某个元素的文本内容。
   ```java
   WebElement heading = driver.findElement(By.tagName("h1")); // 定位标题
   String text = heading.getText(); // 获取文本内容
   System.out.println(text); // 打印出来
   ```

# 二. 页面操作语法


！！方法一般遵循小驼峰命名法，类（对象）名遵循大驼峰命名法。

## 1. 元素定位方式

selenium 提供了**8种**的定位方法: id, name, className, tagName, linkText, cssSelector,

| 方法                            | 描述                  | 参数         | 示例                                     |
| :---------------------------- | ------------------- | ---------- | -------------------------------------- |
| findElement(By.id())          | 通过元素的 id 属性值来定位元素   | 对应的id属性值   | findElement(By.id("kw"))               |
| findElement(By.name())        | 通过元素的 name 属性值来定位元素 | 对应的name值   | findElement(By.name("user"))           |
| findElement(By.className())   | 通过元素的 class 名来定位元素  | 对应的class类名 | findElement(By.className("passworld")) |
| findElement(By.tagName())     | 通过元素的 tag 标签名来定位元素  | 对应的标签名     | findElement(By.tagName("input"))       |
| findElement(By.linkText())    | 通过元素标签对之间的文本信息来定位元素 | 文本内容       | findElement(By.linkText("登录"))         |
| findElement(By.cssSelector()) | 通过css选择器来定位元素       | css元素选择器   | findElement(By.cssSelector("#kw"))     |

同时这8种方法都对应有着返回复数元素的方法，分别在调用的方法findElements(By.id()) 加上一个s：

- findElements(By.id())
- findElements(By.name())
- findElements(By.className())
- findElements(By.tagName())
- findElements(By.linkText())
- findElements(By.cssSelector())

## 2. WebDriver 浏览器的交互

WebDriver 提供了一系列的 API 来完成**浏览器的交互**，如下：

| 方法                  | 描述               |
| ------------------- | ---------------- |
| get(String url）     | 访问目标 url 地址，打开网页 |
| getCurrentUrl()     | 获取当前页面 url 地址    |
| getTitle()          | 获取页面标题           |
| getPageSource()     | 获取页面源代码          |
| close()             | 关闭浏览器当前打开的窗口     |
| quit()              | 关闭浏览器所有的窗口       |
| **findElement(by)** | 查找单个元素           |
| findElements(by)    | 查到元素列表，返回一个集合    |


## 3. WebElement 元素的交互

 通过 WebElement 实现与网站页面上**元素的交互**，这些元素包含文本框、文本域、按钮、单选框、div等，WebElement提供了一系列的方法对这些元素进行操作：

| 方法                          | 描述                        |
| --------------------------- | ------------------------- |
| click()                     | 对元素进行点击                   |
| clear()                     | 清空内容（如文本框内容）              |
| sendKeys(...)               | 写入内容与模拟按键操作               |
| isDisplayed()               | 元素是否可见（true:可见，false：不可见） |
| isEnabled()                 | 元素是否启用                    |
| isSelected()                | 元素是否已选择                   |
| getTagName()                | 获取元素标签名                   |
| getAttribute(attributeName) | 获取元素对应的属性值                |
| getText()                   | 获取元素文本值（元素可见状态下才能获取到）     |
| submit()                    | 表单提交                      |

## 4.其他常用

### **（1）隐式等待：**
1. 导入包:`import java.time.Duration;`
2. 设置等待时间（单位为：秒）`driver.manage().timeouts().implicitlyWait(Duration.ofSeconds(100));`
### （2）最大化浏览器：

- 直接使用`driver.manage().window().maximize();`
- 含义：
	1. 导入包：`import org.openqa.selenium.WebDriver.Window;`
	2. 获取对象：`Window window = driver.manage().window();`
	3. 最大化：`window.maximize()`

### （3）操作键盘：
> sendKeys(Keys.###)
- sendKeys(Keys.**BACK_SPACE**) 回格键（BackSpace）
- sendKeys(Keys.SPACE) 空格键 (Space)
- sendKeys(Keys.TAB) 制表键 (Tab)
- sendKeys(Keys.**ESCAPE**) 回退键（Esc）
- sendKeys(Keys.**ENTER**) 回车键（Enter）

>sendKeys(Keys.CONTROL,'###')
- sendKeys(Keys.CONTROL,'a') 全选（Ctrl+A）
- sendKeys(Keys.CONTROL,'c') 复制（Ctrl+C）
- sendKeys(Keys.CONTROL,'x') 剪切（Ctrl+X）
- sendKeys(Keys.CONTROL,'v') 粘贴（Ctrl+V）

### （3）操作鼠标：

1. 导入包
	`import org.openqa.selenium.interactions.Actions;`
2. 创建Actions对象
	`Actions action = new Actions(driver);`
3. 调用方法(鼠标悬停)
	`action.clickAndHold(#WebElement#).perform();`

|方法|描述|
|---|---|
|contextClick()|鼠标右击|
|clickAndHold(WebElement)|点击并控制（模拟悬停）|
|doubleClick(WebElement)|鼠标双击|
|dragAndDrop(webElement1,webElement2)|鼠标拖动|
|moveToElement(WebElement)|鼠标移动到某个元素上|
|perform()|执行所有Actions中存储的行为|
|click()|鼠标单击（左击）|
## 5.代码演示

~~~java
public class BaiduSearch { 
	public static void main(String[] args) { 
	// 1.创建webdriver驱动 WebDriver 
	driver = new ChromeDriver(); 
	// 2.打开百度首页 
	driver.get("https://www.baidu.com"); 
	// 获取搜索框元素 
	WebElement inputElem = driver.findElement(By.id("kw")); 
	// clear()方法，清空输入框内容 
	inputElem.clear(); 
	// sendKeys()方法，在搜索框中输入搜索内容 
	inputElem.sendKeys("selenium"); 
	// 元素是否显示 
	boolean displayed = inputElem.isDisplayed(); 
	System.out.println(displayed); // 输出true 
	// 元素是否启用 
	boolean enabled = inputElem.isEnabled(); System.out.println(enabled); // 输出true 
	// 判断元素是否被选中状态，一般用在Radio(单选),Checkbox（多选）,Select（下拉选） 
	// 在输入框中使用无意义 
	boolean selected = inputElem.isSelected(); System.out.println(selected); // 输出fasle 
	// 获取标签名 
	String tagName = inputElem.getTagName(); 
	System.out.println(tagName); // 输出input 
	// 获取属性名(name属性) 
	String name = inputElem.getAttribute("name"); 
	System.out.println(name); // 输出wd 
	// 获取文本值 
	String text = inputElem.getText(); 
	System.out.println(text); // 输出selenium 
	// 通过submit提交 
	driver.findElement(By.id("su")).submit(); 
	// click()方法，点击百度一下按钮 
	driver.findElement(By.id("su")).click(); 
	// 退出浏览器 
	driver.quit(); } }
~~~
