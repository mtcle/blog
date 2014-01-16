---
layout: post
title: "自己简陋的代码高亮"
description: "将java的高亮转变成html的高亮"
category: "杂乱"
tags: [java,随笔]
---
###最近折腾这个markdown的高亮,忽然想起来以前我们的一个小小作业,和高亮有关,觉得挺好玩的就拿出来折腾折腾.  
  
**要求** :java的高亮转变成html文件后里面依旧高亮   
思路:  

*  关键字搜索匹配高亮
*  注释搜索匹配
*  html特殊符号处理
*  注释中的关键词处理  

---
效果如下:  
java里面:(由于blog用的js代码高亮不是太完美)  

{% highlight java %}  

package work1;
public class Messageprint {
  // 测试的文档test
  /**
   * ghghghgh
   * 
   * @mtcle the first javawork
   */
  public static void main(String[] args) {
    System.out.println("Welcome\"<html></html> to Java");// 这里是注释
    System.out.println("Welcome to computer Science");// 也是注释
    System.out.println("Programming is fun");// 还是注释
  }
}  
 
{% endhighlight %}  
---
html效果如下:    
这里好像是markdown对于html的bug,段注释在html页面运行正常,放到markdown里就不行了主要是 * 的特殊含义吧  原[html格式](/source/javaToHtml.html)

<html><pre><font color="blue">**package**</font> work1; </font> <p><font color="blue">**public**</font> <font color="blue">**class**</font> Messageprint { </font> <p>  <font color="green">// 测试的文档test </font> <p>   <font color="orange">/**  </font> <p>    <font color="orange">*  ghghghgh </font> <p>    <font color="orange">*   </font> <p>    <font color="orange">*  @mtcle the first javawork </font> <p>    <font color="orange">*/</font>  </font> <p>  <font color="blue">**public**</font> <font color="blue">**static**</font> <font color="blue">**void**</font> main(String[] args) { </font> <p>    System.<font color="blue">**out**</font>.println( <font color="blue">" Welcome \" &lthtml&gt&lt/html&gt to Java "</font> );<font color="green">// 这里是注释 </font> <p>    System.<font color="blue">**out**</font>.println( <font color="blue">" Welcome to computer Science "</font> );<font color="green">// 也是注释 </font> <p>    System.<font color="blue">**out**</font>.println( <font color="blue">" Programming is fun "</font> );<font color="green">// 还是注释 </font> <p>  } </font> <p>} </font> <p></pre></html>  




-------


