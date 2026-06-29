### BOOST电路拓扑图：
<img width="1607" height="833" alt="BOOST" src="https://github.com/user-attachments/assets/7a742cc7-6b9d-4fa0-8b2c-83717b317676" />

结合电路图可知：  
1.当MOS管处于打开状态时  
&emsp;-MOS管导通 整个电路的电流来源于电源  
&emsp;-电流会经过二极管 此时二极管处于正向导通状态  
  
&emsp;-电流流向为：电源——电感——二极管——负载 还有一小部分会经过滤波电容  
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;|  
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;MOS管——电源  
  
&emsp;-电感会阻碍电流发生巨变 负载上的电压会慢慢升到5V 同时电感会储能  
&emsp;-当负载上的电压升到5V时 MOS管会断开  
  
2.当MOS管处于断开状态时  
&emsp;-原本流经MOS管的电流突然消失 电感会阻碍这种变化 此时电感变为左-右+ 电感相当于一个小电源 开始释放能量  
&emsp;-此时电流会经过二极管——负载 负载上的电压升高 直到升到12V   
&emsp;-当负载上的电压升到12V时 MOS管又会导通 从而进入一个循环  
