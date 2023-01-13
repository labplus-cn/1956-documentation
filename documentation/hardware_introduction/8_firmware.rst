烧录系统固件
==============

下载烧录工具
------------

下载全志烧录工具，并解压到一个目录

* :download:`PhoenixSuit </_static/tools/PhoenixSuit-v1.10.rar>`

下载固件
------------

* :download:`tina-r329-20230105 <https://steamaker.oss-cn-shenzhen.aliyuncs.com/1956/r329-20230105.img>`

USB线准备
------------
一根type-c，一根双头USB-A
将1956用两根线连接电脑

.. figure:: /_static/image/firmware_tutorial/jx4.png
    :align: center
    :width: 800

安装驱动
------------
（1）点击我的电脑
++++++++

（2）设备管理
++++++++

.. figure:: /_static/image/firmware_tutorial/jx1.png
    :align: center
    :width: 300

.. figure:: /_static/image/firmware_tutorial/jx2.png
    :align: center
    :width: 800

.. figure:: /_static/image/firmware_tutorial/jx3.png
    :align: center
    :width: 800


使设备进入刷机模式
------------

打开PhoenixSuit，选择对应系统固件
++++++++

.. figure:: /_static/image/firmware_tutorial/jx6.png
    :align: center
    :width: 1400

.. figure:: /_static/image/firmware_tutorial/jx5.png
    :align: center
    :width: 1400

在linux终端输入reboot后，不断回车打断 在出现=>后输入efex
++++++++

.. figure:: /_static/image/firmware_tutorial/jx7.png
    :align: center
    :width: 1400


等待烧录完成
++++++++

.. figure:: /_static/image/firmware_tutorial/jx8.png
    :align: center
    :width: 1400

.. figure:: /_static/image/firmware_tutorial/jx9.png
    :align: center
    :width: 1000
