title: HTML5 新特性
date: 2017-08-10 13:42:21
author: dam
tags: HTML5
---
https://segmentfault.com/a/1190000010081812
http://hyuhan.com/2017/07/06/html5-of-interview/

[新增标签和移除标签](https://leohxj.gitbooks.io/front-end-database/html-and-css-basic/assets/html5-cheat-sheet.png)

# HTML5 新特性
1. localStorage和sessionStorage
2. 新的特殊内容元素，header、hgroup、nav、article、section、aside、figure和figcaption、footer
3. 其他元素
* video元素，用来定义视频。
* audio元素，用来定义音频。
* canvas元素，用来展示图形，该元素本身没有行为，仅提供一块画布。
* SVG，
* embed元素，用来插入各种多媒体，格式可以是Midi、Wav、AIFF、AU、MP3等。
* mark元素，用来展示高亮的文字。
* progress元素，用来展示任何类型的任务的进度。
* meter元素，表示度量衡，定义预定义范围内的度量。
* time元素，用来展示日期或者时间。
* command元素，表示命令按钮。
* details元素，用来展示用户要求得到并且可以得到的细节信息。
* summary元素，用来为details元素定义可见的标题。
* datalist元素，用来展示可选的数据列表，与input元素配合使用，可以制作出输入值的下拉列表。
* datagrid元素，也用来展示可选的数据列表，以树形列表的形式来显示。
* keygen元素，表示生成密匙。
* output元素，表示不同类型的输出。
* source元素，为媒介元素定义媒介资源。
* menu元素，表示菜单列表。
* ruby元素，表示ruby注释， rt元素表示字符的解释或发音。 rp元素在ruby注释中使用，以定义不支持ruby元素的浏览器所显示的内容。
* wbr元素，表示软换行。与br元素的区别是：br元素表示此处必须换行，而wbr元素的意思是浏览器窗口或父级元素的宽度够宽时。不进行换行，而当宽度不够时，主动在此处进行换行。
* bdi元素，定义文本的文本方向，使其脱离其周围文本的方向设置。
* dialog元素，表示对话框或窗口。

4. 表单控件，calendar、date、time、email、url、search

5. 移除了一些可以用css处理的纯表现元素，如basefont、big、center、font、s、strike、tt、u
6. 移除对性能有负面影响的元素，frameset、frame和noframes，只支持iframe


# 新增的API
1. Canvas
2. SVG
3. audio和video
4. Geolocation (地理定位)
5. postMessage 
6. XMLHttpRequest Level2  
跨源XMLHttpRequest
进度事件
7. WebSockets 
8. 拖放
9. Web Workers  
Javascript是单线程的。因此，持续时间较长的计算，回阻塞UI线程，进而导致无法在文本框中填入文本，单击按钮等，并且在大多数浏览器中，除非控制权返回，否则无法打开新的标签页。该问题的解决方案是Web Workers，可以让Web应用程序具备后台处理能力，对多线程的支持性非常好。  
但是在Web Workers中执行的脚本不能访问该页面的window对象，也就是Web Workers不能直接访问Web页面和DOM API。虽然Web Workers不会导致浏览器UI停止响应，但是仍然会消耗CPU周期，导致系统反应速度变慢。

10. Web Storage （localStorage和sectionStorage）
11. form 新属性
input添加了placeholder，required,autofocus,pattern等属性
12. contenteditable 属性




