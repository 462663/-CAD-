# -CAD-
大学CAD作业


*此文字为项目内的   03200904张晨.docx  的文件文字


2022年  05 月04日
1 键盘、流水灯设计

1.1 设计任务
创建自己的原理图库，在立创商城导入封装生成自己的封装库，掌握原理图和封装的链接方法；了解器件布放基本原则，添加适当标注；绘制流水灯、键盘原理图，生成其PCB板。

1.2设计过程及思路
①绘制原理图生成PCB。生成原理图库和封装库后绘制流水灯、键盘原理图，检查无误后生成其PCB；
②器件的布放、边框的绘制。布放时按器件布放要求，通过对齐、缩小间距、等间距分布等工具手段布放美观化。将按键摆放成手柄状，为了摆放美观将电容和电阻矩阵摆放，布放到相应位置后，在“机械层”绘制边框来确定板的长宽和限制布线的范围，框选框内部分后通过快捷键DSD删除框外部分栅格；
③设置规则和布线。根据基本布线原则，在布线前设置不同的“类”，给不同的类的线设置不同的布线宽度，根据工厂加工能力和其他要求设置调整好过孔大小等规则，以上操作完成后通过“自动布线”的方式完成布线；
④铺铜。由于大面积铺铜具有屏蔽等作用，故通过“取消布线”选取GND网络进行“板外形”铺铜；
⑤标注。去掉元件不必要的标注，在Top Layer 顶层添加相关标注管脚等，底层添加姓名、功能描述等

1.3设计中的关键问题
绘制原理图时要保证网络标签落位准确无误，连线要注意交叉处是否有是节点不是的话要删除节点，生成PCB后要确认封装是否正确；器件的布放位置要合理，边框的绘制要选择正确的板层；铺铜时不要忘选标签；标注时要对应管脚标注，在底层标注是注意勾选镜像。
数码管设计

2.1 设计任务

以数码管为例，学会根据原件规格自行绘制元件的原理图和PCB封装；绘制数码管的驱动电路原理图和其PCB图。

2.2设计过程及思路

⓪新添元件和绘制数码管的原理图和封装。通过立创商城导出三极管的原理图和封装添加到自己已有的两个库；在原理图库中添加“BS2481”元件完成参数设置后进行绘制：跟据管脚功能添加摆放管脚到相应位置，跟据元件的管脚和轮廓，绘制矩形作为元件外框，数码管的“8”字通过粗直线画成，圆点由工具“圆”画成，绘制完成后保存；在PCB封装库中添加“BS2481”元件完成参数设置后进行PCB的绘制：设置好原点后，将第一个“焊盘”添加到原点位置，逆时针方向依次添加其他焊盘，焊盘位置通过规格书确定间距，以设置相关栅格大小的方式让栅格“吸引”焊盘，使焊盘间距符合管脚要求，绘制直线方角封闭圈作为元件外框，数码管的“8”字通过粗直线画成，圆点由工具“圆”画成，绘制完成后保存。
①绘制原理图生成PCB。绘制数码管模块的原理图，检查无误后生成其PCB；
②器件的布放、边框的绘制。由于数码管器件特殊如三极管电阻和显示面在同一面放置的话，反面管脚之间会留有大量空白且板子尺寸相对较大，因此通过镜像将其放在相对显示面的另外一层，布放时按器件布放要求，通过对齐、缩小间距、等间距分布等工具手段布放美观化，合理布放到相应位置后，在“机械层”绘制边框来确定板的长宽和限制布线的范围，框选框内部分后通过快捷键DSD删除框外部分栅格；
③设置规则和布线。根据基本布线原则，在布线前设置不同的“类”（gnd,vcc,signal(gnd和vcc以外的网络)），给不同的类的线设置不同的布线宽度（vcc：首选15mil，最小10mil，最大20mil等），根据工厂加工能力和其他要求设置调整好过孔大小（孔径12mil，过孔22mil）等规则，以上操作完成后通过“自动布线”的方式完成布线；
④铺铜。由于大面积铺铜具有屏蔽等作用，故通过“取消布线”选取GND网络进行“板外形”铺铜；
⑤标注。去掉元件不必要的标注，在Top Layer 顶层添加相关标注管脚等，底层或顶层添加姓名、功能描述等

2.3设计中的关键问题
由于我绘制器件库的原理图时，没有将第一个管脚置于十字交叉线交点位置，在绘制原理图添加该器件时出现器件跳到纸外和软件崩溃的情况，因此绘制器件库的原理图时，没有将第一个管脚置于十字交叉线交点位置；焊盘的放置一定要按顺序放置，避免对应连线错误，器件的布放时要思考镜像和合理性，避免使管脚位置错乱导致工作异常。

3 STC8核心板设计

3.1 设计任务
学会根据原理图设计PCB板；掌握差分布线。

3.2设计过程及思路
⓪新添元件的原理图和封装。通过立创商城导出二极管、stc8、安卓USB口等元件的封装添加到自己已有的两个库； 
①绘制原理图生成PCB。绘制STC核心板的原理图，检查无误后生成其PCB；
②器件的布放、边框的绘制。由于STC单片机是多管脚的器件，器件间连线复杂，为减少线与线之间的交叉，将STC置于45°放置，其他元件如电容等通过对齐、缩小间距、等间距分布等工具手段布放美观化，合理布放到相应位置后，在“机械层”绘制边框来确定板的长宽和限制布线的范围，框选框内部分后通过快捷键DSD删除框外部分栅格；
③设置差分对和差分布线。为避免自动布线后给差分布线造成阻碍，先自行差分布线下载线。在pcb中​选择“Differential Amplifiers”添加网络标签“USB P”和“USB N”为差分对，在工具中先取“差分布线”将“USB P”和“USB N”连接到STC的下载端；又由于连接器和STC下载端也有连线，因此也需要差分布线，考虑到在同板层差分会致使之前的两条差分线造成短路，因而通过放置过孔的方式在另一层从连接器差分到STC处，避免差分线相互影响。
④设置规则和布线。根据基本布线原则，在布线前设置不同的“类”（gnd,vcc,signal(gnd和vcc以外的网络)），给不同的类的线设置不同的布线宽度（vcc：首选15mil，最小10mil，最大20mil等），根据工厂加工能力和其他要求设置调整好过孔大小（孔径12mil，过孔22mil）等规则，以上操作完成后通过“自动布线”的方式完成布线；
⑤铺铜。由于大面积铺铜具有屏蔽等作用，故通过“取消布线”选取GND网络进行“板外形”铺铜；
⑥标注。去掉元件不必要的标注，在Top Layer 顶层添加相关的管脚标注、姓名等 

3.3设计中的关键问题
由于USB-STC、连接器-STC均需要差分布线，在同一面差分会致使其中某一对短路，因此需要通过过孔的方式将另一连接对在另一层走线。

4 单片机评估板设计

4.1 设计任务
读懂原理图，综合运用所学知识跟据原理图自行设计PCB板，做出单片机评估板。

4.2设计过程及思路
先在嘉立创下载添加RGB LED等能够找到的原理图库和封装库到自己的库中，通过原理图了解到NRF24L01并不是真正的元件，而是一个连接器，因此需要自行绘制原理图和封装，至于全彩LED通过淘宝的搜索找到了该型号的数据手册，通过手册中标注的管脚的间距自行绘制和他的绘制原理图和封装，准备好库后开始画原理图，其他步骤如上三个项目的步骤大致一样。

4.3设计中的关键问题
①注意管脚位置。在绘制该模块时才发现全彩LED在绘制原理图时不小心搞错了管脚的位置，使封装的管脚不能对应其功能，根据之前所学修改了全彩LED的Pin，使之正确。②PCB元件的摆放。根据已学知识，一般把连接器放置边缘位置，按照模块的划分，每个模块中的元件在一起放置。③不要忘了需要差分布线的地方。

5 收获与体会
通过本课程的学习，知道了一款电路板的诞生过程，比较系统的学习了原理图的绘制和PCB板的设计；掌握了AD软件的安装和熟悉了AD软件的使用方法，会比较熟练地运用一些常用的快捷键。认识到画板子是一件十分考验一个人的耐心的事情，遇到困难的时候不要着急，只有静下心来才能布出既能实现功能又美观的板子；其次画板子布线，布局的时候要有全局观念，各个模块之间的联系要时刻注意；画板子是一个慢慢积累的过程，时间的长久，经验都是宝贵的财富。通过理论和实践的结合，在设计以上四个板子的绘制的过程中，期中遇到过许许多多的问题，在解决这些问题的过程中，不断地熟练的软件的操作，不断的积累了画板的经验，期间的努力都是值得的；由生疏到熟练的过程中，深刻地认识掌握一门“技术”是需要不断的实践练习后才能习得的，想要得心应手使用某一工具，学习是必不可少的，因此即便是结课后，我也将继续该软件和其他类似软件的学习，更加掌握该门技术。

声明：已完成以上四个项目的设计
