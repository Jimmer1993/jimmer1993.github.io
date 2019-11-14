---
layout:     post
title:      for 循环内部switch语句使用break与continue
subtitle:   for循环与switch
date:       2019-07-26
author:     Jimmer
header-img: img/post-bg-cook.jpg
catalog: true
tags:
    - java
	- for循环
	- switch

---

# for 循环内部switch语句使用break与continue

- 结论:

​	for内部的swtich使用continue,属于对循环的continue,会跳过当前循环.

```java
		int[] ints = {1,5,2,3,4};
        for (int i:
        ints) {
            switch (i){
                case 1:
                    System.out.println(i);
                    break;
                case 2:
                    System.out.println(i);
                    break;
                case 3:
                    System.out.println(i);
                    break;
                default:
                    System.out.println("not");
                    continue;
            }
            System.out.println("lalala");
        }
```

输出:

```
1
lalala
not
2
lalala
3
lalala
not
```



- swtich

​	单独使用swtich时,明显是不能用continue的.

​	switch中,会依次判断case.case中可以没有break,没有break的话,执行完当前的case下的语句,会继续判断下面的case语句,直到遇到break.

​	default一般放在最后.可以不带break.

​	default不带break时,当所有case语句都不满足条件,直接进入default,之后执行default后面的case语句(即使case语句不满足条件),知道遇到break或switch结束.

 

​	







