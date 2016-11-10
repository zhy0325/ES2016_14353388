#DOL实例分析和编程一#
##example1##
- 源代码分析


分析代码我们可以看到，生产者产生从1开始到length的数传给平方计算的模块（square），，然后将所得的平方数输出出来。所以为了使example1得到立方数，只需要在原来的square.c中（如下图）我将原来的i=i^2，改成i=i^3即可。

**修改前**

![修改前](http://a3.qpic.cn/psb?/V13EEK1H41EsoZ/EQB2GCHt7TSViSeRxaGLZQzy339vdkKGlROtBFpMh40!/b/dAoBAAAAAAAA&bo=EAJ.AAAAAAADAEk!&rf=viewer_4)

**修改后**

![修改后](http://a3.qpic.cn/psb?/V13EEK1H41EsoZ/M*j053qCuPoddn10LNqm5Nw7*PRtg3192BDuEyyUfwQ!/b/dAoBAAAAAAAA&bo=9gF8AAAAAAADAK4!&rf=viewer_4)

**修改后结果**

![修改后结果](http://a3.qpic.cn/psb?/V13EEK1H41EsoZ/iUNDAMjuC8tBegJB6OSIc8nBAaVoVVuqtnBOfRmWRr8!/b/dNoAAAAAAAAA&bo=pgKfAQAAAAADAB8!&rf=viewer_4)

**修改后dot图**

![修改后dot图](http://a2.qpic.cn/psb?/V13EEK1H41EsoZ/mtjgdMPBFcavTOMDcftK.LLLXh1BFB8Ai4etystjKq4!/b/dNwAAAAAAAAA&bo=*gEfAgAAAAADAMc!&rf=viewer_4)
##example2##
- 源代码分析

分析代码我们可以知道，为了将三个square模块变为两个，我们需要把产生进程square的迭代器（如下图）中起始的value值改为2即可。
![迭代器](http://a3.qpic.cn/psb?/V13EEK1H41EsoZ/Eh139NRo*bH93EkbTBu7oXrg1yA4ikShQ.YFIYfkGeg!/b/dAoBAAAAAAAA&bo=nwGLAAAAAAADADA!&rf=viewer_4)

**修改前**

![修改前](http://a1.qpic.cn/psb?/V13EEK1H41EsoZ/X2KdcmL.sBsOffbmqM6XjZVsICeayGDRhNv1WgYvQl0!/b/dHcBAAAAAAAA&bo=KgEiAAAAAAADACw!&rf=viewer_4)

**修改后**

![修改后](http://a2.qpic.cn/psb?/V13EEK1H41EsoZ/ghuCTIgQtTWYr65zp3.p5xsqryNasWxSGMh3ahFUDno!/b/dAkBAAAAAAAA&bo=sgEcAAAAAAADAIo!&rf=viewer_4)

**修改后结果**

![修改后结果](http://a2.qpic.cn/psb?/V13EEK1H41EsoZ/szhloKzesSSFTRo1B8uQ1MOhZ3aM4xGwnawSBJFiHY0!/b/dAkBAAAAAAAA&bo=kQGOAQAAAAADADo!&rf=viewer_4)

**修改后dot图**

![修改后dot图](http://a3.qpic.cn/psb?/V13EEK1H41EsoZ/MJ5XOSg7gOSXmp45qjDbkgPlcs*u0t5d2Xw*CvPnuJk!/b/dI8AAAAAAAAA&bo=vAJFAgAAAAADANw!&rf=viewer_4)