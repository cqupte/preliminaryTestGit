# Scanner 类中next()和nextLine()的区别

### next与nextLine的结束标志不同

​	nextLine的结束标志 ：回车符

​	

​	next/nextInt/nextDoule的结束标志 ：空格，tab键，回车符



### next与nextLine的扫描方式不同

next/nextInt/nextDoule在扫描到第一个有效字符之前会自动过滤结束标记符





在nextLine前面如果使用了，next之类的方法，则nextLine执行完了就会关闭scanner这个扫描器。

nextLine作为第一个的使用没有问题。





``` java
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int i = sc.nextInt();
        String str = sc.next();zh
        String st = sc.next();
        System.out.println(i+" "+str+" "+st);
    }
}
```



![image-20200116173446383](C:\Code\Git\image-20200116173446383.png)

可能会出现这种情况，输入多了只会使用对应的部分，多余的将不予使用。



以我的代码为例，第一个输入的应该为int型的整数，如果输入的不是该类型

![image-20200116174346438](C:\Code\Git\image-20200116174346438.png)

会提示exception，在找到第一个有效字符之前的会忽略结束标记符，所以个人认为，第一个读到的值为“hello 99” 与int型不匹配。





win+shift+s  是自定义截图

