LDO电路拓扑图  
<img width="448" height="231" alt="f84663b10155175ce7e84ea439bff3b0" src="https://github.com/user-attachments/assets/8d2f0f73-887e-4d68-8b8b-769c8b5134c6" />  
LDO 最经典的应用场景是5V 转 3.3V  
将运算放大器的Vref（基准电压）设为1.2V  
其中  
&emsp;-R1和R2为反馈电阻网络  
&emsp;&emsp;它们组成了一个分压器 负责对输出电压Vout进行采样 采样后的电压送到运放的（+）端与基准电压进行比较  

输出电压的大小完全由R1 R2的比值决定 计算公式为：Vout = Vref*(1 + R1/R2)  
在设计带外置反馈引脚的 LDO 模块时 就是通过调整这俩电阻来设定目标电压的  

  
