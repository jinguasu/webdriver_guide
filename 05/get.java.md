访问链接
========

情景
----
web UI测试里最简单也是最基本的事情就是访问1个链接了。

webdriver的api里有2种访问url的方式，分别是get和navigate.to方法。一般情况下建议使用get，因为其字母比较少，不太容易出错。

代码
----

```
	import org.openqa.selenium.WebDriver;
	import org.openqa.selenium.chrome.ChromeDriver;


	public class Get {

		public static void main(String[] args) throws InterruptedException {
			WebDriver dr = new ChromeDriver();
			Thread.sleep(2000);
			
			String url = "http://www.baidu.com";
			System.out.printf("now accesss %s \n", url);
			dr.get(url);
			Thread.sleep(2000);
			
			System.out.println("browser will be close");
			dr.quit();	
		}

	}

```

讨论
----
navigate方法实际上会产生1个Navigator对象，其封装了与导航相关的一些方法，比如前进后退等。


