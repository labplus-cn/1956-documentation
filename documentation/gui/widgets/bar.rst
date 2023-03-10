进度条
======================================================
概述
~~~~~~~~~~~~~~~
条对象上有一个背景和一个指示器。指示器的宽度根据条的当前值进行设置。

如果对象的宽度小于其高度，则可以创建垂直条。

不仅可以结束，还可以设置条的起始值，从而改变指示器的起始位置。

零件和样式
~~~~~~~~~~~~~~~
进度条的主要部分称为 LV_BAR_PART_BG ，它使用典型的背景样式属性。

LV_BAR_PART_INDIC 是一个虚拟部件，还使用了所有典型的背景属性。默认情况下，指示器的最大尺寸与背景的尺寸相同，但是在其中设置正的填充值 LV_BAR_PART_BG 将使指示器变小。（负值会使它变大）如果在指标上使用了值样式属性，则将根据指标的当前大小来计算对齐方式。
例如，中心对齐的值始终显示在指示器的中间，而不管其当前大小如何。

用法
~~~~~~~~~~~~~~~
值和范围
可以通过 lv.Bar.set_value(new_value, lv.ANIM.ON/lv.ANIM.OFF) 设置新值。该值以一个范围（最小值和最大值）解释，可以使用 lv.Bar.set_range(min, max) 进行修改。默认范围是 1 ~ 100。

lv.Bar.set_value中的新值可以根据最后一个参数 (lv.ANIM.ON/lv.ANIM.OFF) 设置是否带有动画。
动画的时间可以通过 lv.Bar.set_anim_time(100) 进行调整。时间以毫秒为单位。

也可以使用 lv.Bar.set_start_value(new_value, lv.ANIM.ON/lv.ANIM.OFF) 设置进度条的起始值

模式
~~~~~~~~~~~~~~~
如果已通过 lv.Bar.set_type(Lv.BAR.TYPE_SYMMETRICAL) 启用，则条形可以对称地绘制为零（从零开始，从左至右绘制）。

事件
~~~~~~~~~~~~~~~
仅 通用事件 是按对象类型发送的。

了解有关`事件`_ 的更多信息。

按键
~~~~~~~~~~~~~~~
对象类型不处理任何输入按键。

进一步了解 按键 。

范例
~~~~~~~~~~~~~~~


例：简单的进度条::

    from gui_lib import *
    import time

    scr = lv.scr_act()


    bar1 = lv.Bar(scr)
    bar1.set_pos(0, 50)
    bar1.set_range(0, 100)
    bar1.set_value(50, lv.ANIM.ON)
    while True:
        time.sleep(1)
