# UWB
UWB

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/788b48d9da634188ba0c08bcc56c5859.png)


## 1.测距

距离（长度）是最常用的物理量之一，距离的测量是我们日常生活中最常见的，如日常生活工作中的物体的长度尺寸测量，人身高的测量。

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/1f85b97a0761ab71dd26b89150ce8492.png)


长度是一维空间的度量，是点到点的距离。长度的国际单位是“米”（“m”），常用单位有千米（km）、米（m）、分米（dm）、厘米（cm）、毫米（mm）、微米（μm）、纳米（nm）等等。长度测量的国家标准为GBT1219-2000 。

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/a8902f9820977c1881604da18f63a6c8.png)


## 2.测距方式

## 2.1量尺测距

使用带刻度的尺直接测量距离，这种方法操作简单，精度较高。

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/3b946e96dcf28c91a0925133f3cf3877.png)


## 2.2视距测距
有些测量仪器使用视距测量距离，仪器使用光学和三角学原理测定两点间距离的方法。常见的视距测量仪器有经纬仪、平板仪、水准仪等。这些仪器通过望远镜内部的视距丝，视距丝在标尺上的间隔称为视距读数，仪器到标尺间的距离是尺间隔的函数，大多数视距测量仪器的测量精度可达1/400。水准仪的测距原理如下图：

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/f86323ad2ff13c004cbad3ea66b23bce.png)


## 2.3超声波测距

有些设备使用超声波测量距离，超声波测距原理是使用超声波发射器发射超声波，在发射超声波的同时开始计时，超声波在空气中传播，碰到障碍物就立即返回来，超声波接收器收到反射波就立即停止计时。超声波在空气中的传播速度为340m/s，根据计时器记录的时间t（秒），可以计算出发射点距障碍物的距离s：s=340*t/2

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/e52631f2a10cfe28b111b55712b45984.png)


## 2.4激光测距

激光测距仪是利用激光实现对目标的距离测量的仪器，按照测距方法大致有三种：**脉冲法，相位法和三角反射法**。脉冲式激光测距仪工作原理相对简单，这里简单描述一下脉冲式激光测距，其工作原理是向目标射出一束短暂的脉冲激光束，激光照射到目标后产生反射，激光测距仪的光电元件接收反射的激光束，计时器测定激光束从发射到接收的时间，计算出从观测者到目标的距离。

　　激光以速度c在空气中传播，激光在A、B两点往返一次所需时间为t，则A、B两点间距离D可用下列表示。
  
![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/d7a9eda27a18d3048904072454bdc631.png)


　　式中：D为测站点A、B两点间距离；c为光在大气中传播的速度；t为光往返A、B一次所需的时间。
  
　　![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/c7de494cf585dc40ef0f9e166db3cdae.png)
  
除上述测距方式之外，还有一种近些年比较火的测距方式（就是今天我们要讲的主角）：**UWB测距**。

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/bbbac49b4def6fe297b1c10df9e27357.png)



## 3.UWB技术及应用

**UWB技术是使用1GHz以上频率的无线通信技术**。UWB不使用正弦载波，而是**使用用纳秒级的窄脉冲传输数据**。UWB所占的频谱范围很大，其数据传输速率可以达每秒几百兆比特以上。UWB技术使用超宽基带脉冲进行通信，主要用于军用雷达、定位和低截获率的通信系统中。2002年2月，美国联邦通信委员会发布了民用UWB设备使用频谱和功率的初步规定。该规定中，在**3.1~10.6GHz频段**中传输数据带宽大于500MHz的通信系统称为UWB系统。

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/90447246190800ff2f88c53920c51b8e.png)

UWB技术是以**占空比很低的脉冲**作为信息载体的无载波扩谱技术，它是通过对具有很陡上升和下降时间的冲击脉冲进行直接调制。冲击脉冲通常采用单周期高斯脉冲，一个信息比特可映射为数百个这样的脉冲。单周期脉冲的宽度在纳秒级，具有很宽的频谱。

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/15408eded3f4fe47e440a70c02018ec3.png)

UWB技术解决了困扰传统无线通信技术多年的有关传播方面的重大难题，UWB技术有以下特点：

> 1.系统结构的实现简单
> 2.高速的数据传输
> 3.功耗低
> 4.安全性高
> 6.定位精确
> 7.系统成本低

**UWB的实现**
UWB系统结构实现比较简单，UWB发射器直接用低成本的脉冲激励发射器。高速数据传输时，一般要求UWB信号的传输范围为10 m以内，其传输速率可达到5 00 Mbit/s以上。UWB系统使用间隙的脉冲来发送数据，有很低的占空因数，系统耗电可以做到很低。在高速通信时，系统的耗电量仅为几百μW～几十mW。图为超宽带无线通信系统的基本电路结构：

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/5a365a9797a4cf9a89d81b22c9c2180a.png)

**UWB应用**
1、**通信应用**，基于UWB技术的通信速度可达到1Gb/s。当传输距离很近时，UWB通信的速度优势更加明显。非常适合VR、手机文件传输、无线组网等领域。 
2、**测距应用**，基于UWB技术可以实现高精度距离测量，并解决了范围、瞄准等问题。适用于社交距离追溯、物品防丢失等等

3、**定位应用**，基于UWB技术可以实现室内外高精度定位，这是UWB技术最有优势的应用，UWB定位可以适用于各种复杂环境高精度定位。例如：监狱人员定位管理、活动轨迹追踪、高危作业场所人员定位管理扽等。

4、**加密和认证应用**，由于UWB通讯安全性高，适用于手机支付、认证，、信用卡、身份证、刷卡等等 。

## 4.测距媒介和算法

在讲解UWB测距原理之前我们先来了解测距过程中的两个概率：
1、**测距媒介**，距离测量时依靠的媒介或工具。
2、**测距算法**，距离测量时使用的距离计算方法。

基于这两个概念，我们将第二章提到的几种距离测量方法分别使用的什么测距媒介和测距算法。

**量尺测距**
测距媒介：带刻度的量尺。
测距算法：最小差值法，找到被测物体与量尺刻度中差值最小的刻度，以此刻度值作为测量距离。


**视距测距**
测距媒介：光学成像。
测距算法：逼近法，调节光学焦距或者位置，使得光学镜头内的视距丝和目标接近，当视距丝与目标吻合时，根据光学参数确定距离。

**超声波测距**
测距媒介：超声波。
测距算法：飞行时间法（TOF），通过记录超声波从发射到接受到超声波回波的时间差，根据声音传播速度乘以时间得出距离值。

**激光测距**
测距媒介：激光。
测距算法：飞行时间法（TOF），通过记录激光从发射到接受到激光回波的时间差，使用光传播速度乘以时间得出距离值。

**UWB测距**
测距媒介：UWB电磁波。
测距算法：飞行时间法（TOF），接收到的无线电信号中的时间错信息，根据时间戳计算时间差，利用无线电传播速度乘以时间得出距离值。

**时间戳差值法**
我们可以利用时间戳的方法来计算时间差，我们使用一个例子来描述**时间戳算法**：
例如，有一个朋友给我们写了一封纸质的信，在信内容的最后朋友写下了寄信时的日期2022年10月1日，经过漫长的路程邮差将信送到我们家，我们们打开信件读取日期（2022年10月1日）然后根据收到信封的日期2022年10月8日，**根据这两个时间推算出这封信从寄出到收到一共花8天**。
这就是时间戳算法，我们在通讯过程中加上时间，接受者根据接受到信息那一刻的时间，就可以计算出信息发送和接受的时间差（接受者和发送者时间是同步的）。

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/f30709152e3447367ae2edfe2df3d150.png)

我们推算出信从寄出到收到一共花8天，假设邮差寄信的平均速度是200km每天，因此我们得出，朋友家距我们家的路程大约为1600km，这就是**时间戳差值法测量距离**。

## 5.UWB测距原理及算法

## UWB测距原理

UWB测距原理是**使用时间戳差值法计算电磁波飞行时间**，从而计算距离。UWB测距应用中有两种实体：
1、基站，固定安装在某处用于计算距离和输出数据。
2、标签，安装在被测目标物体上。

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/3f1d184cbbac5c78703ea798bf7d2b9c.png)


基站和标签采用UWB通讯，**在通讯过程中带有时间戳，因此基站可以根据时间戳计算标签距离基站的距离**。UWB时间戳实现原理框图如下：

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/181c2b39179f54c90f2e50854e34cd56.png)


标签发起通讯，在通讯数据中带有发送数据的时间信息t1,基站收到数据时先记录下接收时间t2,然后在从接受信息中提取发送时间（假设基站和标签时间是同步的），**根据发送时间戳和接收时间戳计算飞行时间t=t2-t1**，由此计算出标签到基站的距离**d= (c * t )/2** ,其中c为光速。
上述描述只是简单的介绍UWB通过使用时间戳的方法测量距离的基本原理，但是实际应用中并不是如上图所示这么简单，在实际应用中UWB测距算法分为：**双向测距（TWR）和双边双向测距(ADSTWR)。**

## UWB测距算法
**双向测距（TWR）**
双向测距又称为TWR(Two-Way-Ranging)，基站发起测距请求并记下时间t1，标签收到请求之后记录接收时间t2，然后标签再回复一个响应，回复的响应信息中包含t2(接收请求时间)和t3（响应请求时间）这两个时间，基站接收到响应时记录接收时间t4，此时基站拥有4个时间：t1,t2,t3,t4，因此飞行时间T=( (t4 - t1) - (t3 - t2) )/ 2 ，计算基站和标签之间的距离D= T*c 。算法原理框图如下：

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/b6d473059e7d58610c7b9b15cb16c9b8.png)

**问题1：飞行时间为什么不直接用t2 - t1 或者t4 - t3 ?**
因为基站和标签这两个设备的时间不同步，两个设备想要时间同步难度非常大！

**问题2：如何解决时间同步问题？**
我们仔细观察t1,t2,t3,t4这4个时间，不难发现t1和t4是基站的记录的时间，这两个时间是同步的；t2和t3是标签的记录的时间，这两个时间是同步的。因此我们使用（t4 - t1） - （t3 - t2）得出飞行时间，**这样就不要求基站和标签这两个设备时间同步**。

TWR算法完美解决问题？事实上不是这样，我们以基站记录的时间差（t4 - t1）为例，这个时间差存在误差吗？我们假设MCU的工作主频为10Mhz，每个时钟周期计时器中的计数器都会加一，我们根据**计数器来得知时间**，例如计数器的值为800，此时我们认为时间为80us。

但是MCU真正工作主频绝对为10Mhz吗？想要每个MCU工作主频都绝对10Mhz是不可能的！没个MCU的工作主频都存在误差，假设MCU主频误差为1%，那么计数器的值为800时对应的真实时间为79.2us（80 * 0.99），时间误差为0.8us，距离误差为120m!

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/621291c7cfd99a79a52b676257316cde.png)

根据计算可知，当基站记录的时间差越大，时间误差就越大t = T * P  ,t为误差时间，T为记录的时间差，P为时钟误差。

## 双边双向测距(ADSTWR)

ADSTWR(Asymetic double side two way ranging)是 TWR的升级改进版本（改善TWR算法误差较大问题），**ADS-TWR在TWR的基础上增加了一次传输**，同时改进了时间计算方法。算法原理框图如下：

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/5ed20945c1832595c8100d751ca320b6.png)

根据这3次通讯，可以计算出两个飞行时间：

```c
T1  =  ( (t4 - t1)  -  (t3 - t2) ) / 2
T2  =  ( (t6 - t3)  -  (t5 - t4) ) / 2
```

由于两次测量时时间非常短，可以认为距离没变，飞行时间也也相等，因此有：

```c
T1  =  T2
```

我们可以通过两次飞行时间，求出平均飞行时间：

```c
T~  =  ( T1  +  T2 )/2  = ( ( (t4 - t1)  -  (t3 - t2) ) +  ( (t6 - t3)  -  (t5 - t4) ) )  / 4
```

我们将公式转换一下：

```c
Ta	=	t4 - t1
Tb	=	t3 - t2
Tc	=	t6 - t3
Td	=	t5 - t4
```

于是：

```c
T1  =  ( Ta 	-  Tb ) / 2 
T2  =  (Tc	-  Td ) / 2 
T~   =  ( ( Ta  -  Tb) +  ( Tc  -  Td ) )  / 4
```

这种算法和TWR算法一样，因此误差也是一样的！**因此我们要改变算法！**

已知：

```c
T1  =  ( Ta 	-  Tb ) / 2
T2  =  (Tc	-  Td ) / 2
T1  =  T2
```

转换：

```c
Ta 	= 	2*T1	  +  Tb
Tc 	= 	2*T2  +  Td

Ta*Tc 	=  ( 2*T1  +  Tb ) *(2*T2  +  Td)
		=  ( 2*T1  +  Tb ) *(2*T1  +  Td)
		=  4*T1*T1  +  2*T1*Td  +  2*T1*Tb  +  Tb*Td
```

于是：

```c
Ta*Tc  -   Tb*Td  =   4*T1*T1  +  2*T1*Td  +  2*T1*Tb 
Ta*Tc  -   Tb*Td  =   T1*(4*T1  +  2*Td  +  2*Tb )
```

其中： 

```c
4*T1  = (2*T1)  + ( 2*T2)  =  (Ta  -  Tb)  +  (Tc	-  Td )
```

于是：

```c
Ta*Tc  -   Tb*Td  =  T1*( (Ta  -  Tb)  +  (Tc  -  Td )  +  2*Td  +  2*Tb )
Ta*Tc  -   Tb*Td  =  T1*(Ta +  Tc  +  Td  +  Tb)
```

最终得到：

```c
T1  =  (Ta*Tc  -   Tb*Td ) /(Ta +  Tc  +  Td  +  Tb)
```

这种算法产生的误差和收到帧之后再发出的反应处理时间关系不大，**同样的时钟误差ADSTWR比TWR测距精度更高（我们软件算法设计就是用的这个算法）**。

## 6.UWB测距嵌入式设计

本节介绍UWB基站的硬件和软件设计，基站电路的MCU使用的是STM32F103，基站使用DW1000芯片进行UWB通信，基站使用锂电池供电。基站的电路原理图如下：

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/59e4c984cb1e15f77c40a484ede4579c.png)

UWB 定位电路基于 DecaWave公司 DW1000 系列的 UWB 定位系统，DW1000使用SPI接口，相关电路如下：

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/2bf78390fa122325b5adc5006e7bf2a3.png)


## 软件构架
嵌入式软件整体架构如图所示：主要分为驱动层、DW_API 层、应用层。

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/9abee05b29f26c9dcde7a5722e77b4eb.png)

**驱动层**主要实现 STM32 与 DWIC 的 SPI 通信，使用 HAL 库进行开发，完成SPI 配置、中断配置、IIC 配置、串口配置、看门狗配置等，对接到 DW_API 层，完成驱动层搭建。 

**DW_API 层**使用 DecaWave 官方 API 进行移植搭建，API 将常用功能进行函 数封装，DWIC 的主要功能实现基本通过读写相应的寄存器实现，通过官方 API 内的简单 example 结合DW1000_Software_API_Guide.pdf》可大概了解常用 API 功能。
 
**应用层**是实现 TWR 测距主要功能的实现代码，完成系统的状态读取，参数 配置，TWR 据收发，TOF 计算，卡尔曼滤波，串口数据发送等功能。

**主程序工作流程** 
主程序位于 Src/application/dw_main.c，主要完成设备参数初始化和按拨码开 
关状态进行基站或标签状态机运行，最后进行串口数据打包发送。基站工作过程由状态机实现，完成单周期ADSTWR 全过程，主要工作流程如图：

![请添加图片描述](https://i-blog.csdnimg.cn/blog_migrate/e871ac0c1b078555ee43a3a701fbaa55.png)

**代码源码如下**：

```c
void anchor_app(void)
{
    switch (state)
    {
        case STA_INIT_POLL_BLINK: //初始化接收机，接收poll消息

            dwt_setpreambledetecttimeout(0);                        //清除前导码超时，一直接收
            dwt_setrxtimeout(0);                                    //清除接收数据超时，一直接收
            int ret = dwt_rxenable(DWT_START_RX_IMMEDIATE);         //打开接收机，等待接收数据    
            rx_status = RX_WAIT;                                    //清rx标志位，中断服务函数更改其状态
            state = STA_WAIT_POLL_BLINK; 
			/*  省略代码*/
            break;
        
        case STA_WAIT_POLL_BLINK:                                   //等待poll消息，中断回调函数状态变更
        
            if(rx_status == RX_OK)                                  //接收到数据
            {
                rx_status = RX_WAIT;

                    state = STA_RECV_POLL_BLINK;
            }
            else if((rx_status == RX_TIMEOUT)||(rx_status == RX_ERROR))  //接收数据错误，重新开启接收
            {
                state = STA_INIT_POLL_BLINK;
            }
			/*  省略代码*/
            break;

        case STA_RECV_POLL_BLINK://接收处理poll消息
            if(rx_buffer[FUNC_CODE_IDX] == FUNC_CODE_POLL)      //判断收到的数据是POLL
            {
                range_nb = rx_buffer[RANGE_NB_IDX];             //取range_nb，resp发送时发送相同的range_nb
                recv_tag_id = rx_buffer[SENDER_SHORT_ADD_IDX];  //取发送标签的ID
                if(recv_tag_id >= inst_slot_number)             //标签ID如果大于标签总容量则退出
                {
                    state = STA_INIT_POLL_BLINK;
                    break;
                }
                range_time = portGetTickCnt();  //取得测距时间
                poll_rx_ts = get_rx_timestamp_u64(); //获得poll_rx时间戳
				/*  省略代码*/
            }
            else //非POLL数据重新开启接收POLL
            {
                state = STA_INIT_POLL_BLINK;
            }
			/*  省略代码*/
            break;

        case STA_SORR_RESP://根据基站ID按顺序进行发送或接收resp消息
            
            if(sr > 0)// sr>0 处于resp阶段，按基站ID判断接收resp或发送resp
            {
                if(rr & 0x01)//当前该基站需发送resp
                {
                    rr = 0;
                    state = STA_SEND_RESP;
                }
                else//当前该基站需接收resp
                {
                    dwt_setdelayedtrxtime(resp_rx_time);         //设置接收机开启延时时间
                    dwt_setrxtimeout(inst_resp_rx_timeout);      //设置接收数据超时时间
                    dwt_setpreambledetecttimeout(PRE_TIMEOUT);   //设置接收前导码超时时间
                    int ret = dwt_rxenable(DWT_START_RX_DELAYED);          //延时开启接收机
                    if(ret == DWT_ERROR)
                    {
                        state = STA_INIT_POLL_BLINK;
                        break;
                    }   
                    rr = rr >> 1;
                    state = STA_WAIT_RESP;
                }
                sr = sr - 1; 
				/*  省略代码*/				
            }
            else//准备接收final
            {      
				/*  省略代码*/
                dwt_setrxtimeout(inst_final_rx_timeout);       //设置接收数据超时时间
                dwt_setpreambledetecttimeout(PRE_TIMEOUT);     //设置接收前导码超时时间
                int ret = dwt_rxenable(DWT_START_RX_DELAYED);            //延时开启接收机
                if(ret == DWT_ERROR)
                {
                    state = STA_INIT_POLL_BLINK;
                    break;
                }   
                state = STA_WAIT_FINAL;
            }
            break;

        case STA_SEND_RESP: //打包发送resp消息
        {
			/*  省略代码*/
            /* resp数据打包 */
            tx_resp_msg[SEQ_NB_IDX] = frame_seq_nb++;
            tx_resp_msg[RANGE_NB_IDX] = range_nb;
            tx_resp_msg[SENDER_SHORT_ADD_IDX] = anc_id;
            tx_resp_msg[RECEIVER_SHORT_ADD_IDX] = recv_tag_id;
            tx_resp_msg[FUNC_CODE_IDX] = FUNC_CODE_RESP;

			/*  省略代码*/
            state = STA_SORR_RESP;
        }
            break;

        case STA_WAIT_RESP:  //等待接收resp消息，在中断回调函数内rx_status状态变更
            if(rx_status == RX_OK)
            {
                rx_status = RX_WAIT;
                state = STA_RECV_RESP;
            }
            else if((rx_status == RX_TIMEOUT)||(rx_status == RX_ERROR))
            {
                rx_status = RX_WAIT;
                state = STA_SORR_RESP;
            }   
            break;

            case STA_RECV_RESP: //接收到其他基站的resp消息
            {
                if(rx_buffer[FUNC_CODE_IDX] == FUNC_CODE_RESP)//正确接收到resp消息
                {
                    if(rx_buffer[RANGE_NB_IDX] == range_nb)//和当前测距具有相同的range_nb
                    {
                        uint8_t recv_anc_id = rx_buffer[SENDER_SHORT_ADD_IDX]; //取基站ID
                        distance_report[recv_anc_id]  = (int32_t)rx_buffer[RESP_MSG_PREV_DIS_IDX]   << 24;
                        distance_report[recv_anc_id] += (int32_t)rx_buffer[RESP_MSG_PREV_DIS_IDX+1] << 16;
                        distance_report[recv_anc_id] += (int32_t)rx_buffer[RESP_MSG_PREV_DIS_IDX+2] << 8;
                        distance_report[recv_anc_id] += (int32_t)rx_buffer[RESP_MSG_PREV_DIS_IDX+3];
                    }
                }
                state = STA_SORR_RESP;
            }
                break;
        

        case STA_WAIT_FINAL:  //等待接收final消息，在中断回调函数内rx_status状态变更
            if(rx_status == RX_OK)
            {

                {
                    state = STA_RECV_FINAL;
                }

            }
            else if((rx_status == RX_TIMEOUT)||(rx_status == RX_ERROR))
            {
                rx_status = RX_WAIT;
                state = STA_INIT_POLL_BLINK;
                range_status = RANGE_ERROR; 
            }
            break;

        case STA_RECV_FINAL:  //接收到final消息，数据处理
            if ((rx_buffer[FUNC_CODE_IDX] == FUNC_CODE_FINAL) && (rx_buffer[RANGE_NB_IDX] == range_nb))
            {
                resp_valid = rx_buffer[FINAL_MSG_FINAL_VALID_IDX];
                if((resp_valid >> anc_id) & 0x01) //final消息中，本基站发送的resp消息是有效的,则进行距离计算
                {
                    uint32_t poll_tx_ts, resp_rx_ts, final_tx_ts;
                    uint32_t poll_rx_ts_32, resp_tx_ts_32, final_rx_ts_32;
                    double Ra, Rb, Da, Db;
                    int64_t tof_dtu;
                    double tof;


                    resp_tx_ts = get_tx_timestamp_u64();   //取得resp_tx时间戳
                    final_rx_ts = get_rx_timestamp_u64();  //取得final_rx时间戳

                    /* 从final消息中，取得poll_tx时间戳，resp_rx时间戳，final_tx时间戳 */
                    final_msg_get_ts(&rx_buffer[FINAL_MSG_POLL_TX_TS_IDX], &poll_tx_ts);
                    final_msg_get_ts(&rx_buffer[FINAL_MSG_RESP1_RX_TS_IDX + anc_id * FINAL_MSG_TS_LEN], &resp_rx_ts);
                    final_msg_get_ts(&rx_buffer[FINAL_MSG_FINAL_TX_TS_IDX], &final_tx_ts);

                    /* 计算飞行时间 */
                    poll_rx_ts_32 = (uint32_t)poll_rx_ts;
                    resp_tx_ts_32 = (uint32_t)resp_tx_ts;
                    final_rx_ts_32 = (uint32_t)final_rx_ts;
                    Ra = (double)(resp_rx_ts - poll_tx_ts);
                    Rb = (double)(final_rx_ts_32 - resp_tx_ts_32);
                    Da = (double)(final_tx_ts - resp_rx_ts);
                    Db = (double)(resp_tx_ts_32 - poll_rx_ts_32);
                    tof_dtu = (int64_t)((Ra * Rb - Da * Db) / (Ra + Rb + Da + Db));

                    tof = (int32)tof_dtu; 
                    if (tof > 0x7FFFFFFF) 
                    {
                        tof -= 0x80000000;  
                    }

                    tof = tof * DWT_TIME_UNITS;
                    distance_now_m = tof * SPEED_OF_LIGHT;

                    if(distance_now_m > 20000.000)  
                    {
                        distance_now_m = -1;
                    }

                    distance_now_m = distance_now_m - (float)distance_offset_cm/100.0f;


                    //将上次的测距值写入distance_report用于串口输出
                    distance_report[anc_id] = prev_range[recv_tag_id].distance;
                    
                    //更新prev_range为本次测距值
                    prev_range[recv_tag_id].distance = distance_now_m * 1000;//单位转换为mm
                    prev_range[recv_tag_id].range_nb = range_nb;

                    valid_report = resp_valid;
					/*  省略代码*/
                }
            }
            dwt_forcetrxoff();
            state = STA_INIT_POLL_BLINK;
            break;
        
        default:
            break;
    }
    
}
```


**测距算法相关代码**：

```c
poll_rx_ts_32 = (uint32_t)poll_rx_ts;
resp_tx_ts_32 = (uint32_t)resp_tx_ts;
final_rx_ts_32 = (uint32_t)final_rx_ts;
Ra = (double)(resp_rx_ts - poll_tx_ts);
Rb = (double)(final_rx_ts_32 - resp_tx_ts_32);
Da = (double)(final_tx_ts - resp_rx_ts);
Db = (double)(resp_tx_ts_32 - poll_rx_ts_32);
tof_dtu = (int64_t)((Ra * Rb - Da * Db) / (Ra + Rb + Da + Db));

tof = (int32)tof_dtu; 

tof = tof * DWT_TIME_UNITS;
distance_now_m = tof * SPEED_OF_LIGHT;
```

代码对应的公式：
![**T1  =  (Ta*Tc  -   Tb*Td ) /(Ta +  Tc  +  Td  +  Tb)**](https://i-blog.csdnimg.cn/blog_migrate/5ff4f9491ed5a620c121dcc54767c06b.png)

**鸣谢：**

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/40ee89c90cabd0519985dbff8d42d929.png)


**CSDN：https://blog.csdn.net/li_man_man_man
今日头条：https://www.toutiao.com/article/7149576260891443724
创作不易希望朋友们点赞，转发，评论，关注!
您的点赞，转发，评论，关注将是我持续更新的动力!**
