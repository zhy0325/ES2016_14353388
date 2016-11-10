#死锁Deaklock#
##实验所用的代码##

**Deadlock.java**


![java](http://a3.qpic.cn/psb?/V13EEK1H01RXpe/0Q49ncmUSr*S7TCOn6rYWpbdHso0dMKn5.IAripq8bE!/b/dOMAAAAAAAAA&bo=8wFJAgAAAAADB5s!&rf=viewer_4)

**Deadlock.bat**


![bat](http://a3.qpic.cn/psb?/V13EEK1H01RXpe/flUvM8TFIpBnsZWxcUrexLPFwNk.dVuMZwGfmV0ja*U!/b/dHwBAAAAAAAA&bo=4ADpAAAAAAADBys!&rf=viewer_4)

##产生死锁的四个必要条件##
1. 互斥条件：一个资源每次只能被一个进程使用
1. 请求与保持条件：一个进程因请求资源而阻塞时，对已获得的资源保持不放
1. 不剥夺条件:进程已获得的资源，在末使用完之前，不能强行剥夺
1. 循环等待条件:若干进程之间形成一种头尾相接的循环等待资源关系

##实验结果截图##
**count=20000时**

![20000](http://a2.qpic.cn/psb?/V13EEK1H01RXpe/c5W6iwRGMCH8fBh1A8e0WGrtx*kSm2n93oV54wCMlMg!/b/dAkBAAAAAAAA&bo=gAL9AwAAAAADB14!&rf=viewer_4)


**count=10000时**

![10000](http://a3.qpic.cn/psb?/V13EEK1H01RXpe/3JH7yqc1U.xVoHMTaxdyKdfg*s3M*nYmvUOyYvrwjxU!/b/dAoBAAAAAAAA&bo=gAL9AwAAAAADAFk!&rf=viewer_4)

**count=40000时**

![40000](http://a1.qpic.cn/psb?/V13EEK1H01RXpe/g4Ndouood9*8yI3WT18F5cgnaTNiAZ3umetwxw2YaJA!/b/dHcBAAAAAAAA&bo=gAL9AwAAAAADAFk!&rf=viewer_4)

##对实验程序产生死锁的分析##

在Deadlock.java中我们可以看到，首先我们是定义了两个类：A与B，其中A与B类中的方法类似（methodA（B b），methodB（A a）），由于这些方法全是用关键字synchronized修饰，表明了A与B类中的方法最多只有一个线程执行该方法并且当一个线程访问object的一个synchronized同步代码块或同步方法时，其他线程对object中所有其它synchronized同步代码块或同步方法的访问将被阻塞。所以此处就已经满足了产生死锁的前三个必要条件。在Deadlock.java的类Deadlock中，利用count设置进程等待时间，循环地调用methodA与methodB方法，这里就满足了死锁产生的第四个必要条件。至此产生死锁的所有的必要条件都已经满足，所以该程序运行时的确会产生死锁。
