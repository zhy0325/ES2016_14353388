#DOL配置#
- 安装必要环境
<pre>
$ sudo apt-get update
$ sudo apt-get install ant
$ sudo apt-get install openjdk-7-jdk
$ sudo apt-get install unzip
</pre>
- 下载文件
<pre>
$ sudo wget http://www.accellera.org/images/downloads/standards/systemc/systemc-2.3.1.tgz
$ sudo wget http://www.tik.ee.ethz.ch/~shapes/downloads/dol_ethz.zip
</pre>
- 解压文件
-
新建dol文件夹
<pre>
$ mkdir dol
</pre>
将dolethz.zip解压到 dol文件夹中
<pre>
$ unzip dol_ethz.zip -d dol
</pre>
解压systemc
<pre>
$ tar -zxvf systemc-2.3.1.tgz
</pre>
- 编译systemc
- 
解压后进入systemc-2.3.1的目录下
<pre>
$ cd systemc-2.3.1
</pre>
新建一个临时文件夹objdir
<pre>
$ mkdir objdir
</pre>
运行configure
<pre>
$ ../configure CXX=g++ --disable-async-updates
</pre>
运行configure之后的截图

![编译结果](http://a3.qpic.cn/psb?/V13EEK1H1WsmOX/VMJ4BOAWpOpuUlnlwXY9nd0jl3a*NF9NyHkys8tPU7A!/b/dPgAAAAAAAAA&bo=4AJMAAAAAAADB4w!&rf=viewer_4)

编译
<pre>
$ sudo make install
</pre>
接着
<pre>
$cd .. 
$ls
</pre>
编译完后文件目录如下
![目录](http://a3.qpic.cn/psb?/V13EEK1H1WsmOX/VMJ4BOAWpOpuUlnlwXY9nd0jl3a*NF9NyHkys8tPU7A!/b/dPgAAAAAAAAA&bo=4AJMAAAAAAADB4w!&rf=viewer_4)


记录当前的工作路径
<pre>
$ pwd
</pre>
![路径](http://a2.qpic.cn/psb?/V13EEK1H1WsmOX/nVsogEgagbW9x5EuiE.HuI4bWfzL9RhKZ*6b.3.xzfM!/b/dLIAAAAAAAAA&bo=owErAAAAAAADB6s!&rf=viewer_4)

- 编译dol
- 
进入刚刚的dol文件夹，修改build.xml文件，找到下面这段话
<pre>
property name=”systemc.inc” value=”X/include” 
property name=”systemc.lib” value=”X/lib-linux/libsystemc.a”/
</pre>
X为pwd中的路径

接着编译
<pre>
$ ant -f build_zip.xml all
</pre>

运行第一个例子(build/bin/main路径下)
<pre>
$ cd build/bin/main
$ ant -f runexample.xml -Dnumber=1
</pre>
运行成功如下
![结果](http://a1.qpic.cn/psb?/V13EEK1H1WsmOX/6vPPrXoAK36Mh1XX1.TOU2L0PiM461qIMe0MC6UbJYE!/b/dLEAAAAAAAAA&bo=2gJHAgAAAAADB78!&rf=viewer_4)



