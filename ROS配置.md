#ROS配置#
- 确认系统

	确认ubantu系统是否能够允许执行"restricted," "universe," and "multiverse." 

- 设置sources.list

<pre>
$ sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
</pre>

- 设置你的键值

<pre>
$ sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 0xB01FA116
</pre>

- 安装

<pre>
$ sudo apt-get update
</pre>
执行此指令后结果如下：

![update结果](http://a2.qpic.cn/psb?/V13EEK1H4HgV0g/c9ELa0YdR32q9Mp7APgW7cd.kKf2mir.5ySubOvcPRw!/b/dAkBAAAAAAAA&bo=WQK4AQAAAAADAMc!&rf=viewer_4)

<pre>
$ sudo apt-get install ros-jade-desktop-full
</pre>

执行此指令后结果如下：

![datafull结果](http://a2.qpic.cn/psb?/V13EEK1H4HgV0g/6bOWh8V4acrbx.B*5ZaW5RKpcaovBEpu8dkhgn3b4.g!/b/dNwAAAAAAAAA&bo=rwKfAQAAAAADABY!&rf=viewer_4)

- 初始化ros
<pre>
$ sudo rosdep init
rosdep update
</pre>
执行此指令后结果如下：

![初始化结果](http://a2.qpic.cn/psb?/V13EEK1H4HgV0g/.Ta3Jj41vMQIosI6mOUC9lJhDP*4OGNwQQBwb.hBoaA!/b/dAkBAAAAAAAA&bo=2gKeAQAAAAADB2U!&rf=viewer_4)


- 环境设置
<pre>
$ echo "source /opt/ros/jade/setup.bash" >> ~/.bashrc
source ~/.bashrc
</pre>

- 安装ros

<pre>
$ sudo apt-get install python-rosinstall
</pre>
执行此指令后结果如下：

![ros安装结果](http://a3.qpic.cn/psb?/V13EEK1H4HgV0g/pAa0JHEBAxYbBaS.M6Admfreqrba4PNmX3YBvfFcgmc!/b/dHABAAAAAAAA&bo=ggKcAQAAAAADADg!&rf=viewer_4)

- ros测试

<pre>
$ roscore
</pre>
新建一个命令行窗口，输入如下指令，打开小海龟界面
<pre>
$ rosrun turtlesim turtlesim_node
</pre>
再新建一个命令行窗口，输入如下指令
<pre>
$ rosrun turtlesim turtle_teleop_key
</pre>
按方向键若是小海龟可移动并且留下轨迹，则配置成功

![测试结果](http://a2.qpic.cn/psb?/V13EEK1H4HgV0g/qdl.RxtlnzEnXJ9PN*BjE2vrKZ265yo2.fIRmvY8lZA!/b/dOUAAAAAAAAA&bo=UgSAAgAAAAADAPE!&rf=viewer_4)

