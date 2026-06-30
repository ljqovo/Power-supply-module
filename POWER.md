## 电源输入电路：  
<img width="574" height="403" alt="image" src="https://github.com/user-attachments/assets/ddbab690-4943-4534-ac51-80955d8a8062" />  

## 电路分析：  
当开关接1时  
&emsp;-MOS管的G(栅极)通过R2接地形成压差 MOS导通 为后续电路提供电源  
当开关接3时：  
&emsp;-引脚3连着S极(源极) 引脚2连着G极（栅极） 这就相当于你拿了一根没有任何阻力的导线 直接把G和S强行绑在了一起 压差归零 此时 G极电压瞬间被强制拉高 变成和S极一模一样的12V 栅源压差变为0V 因为 PMOS 必须要有负压差（比如 -5V）才能导通 现在压差归零 PMOS 的内部通道瞬间“断崖式”闭合  

>R1的作用：
R1看似没用  但是当





>&emsp;-对于 PMOS
  
&emsp;&emsp;G 极电压越低 = 阀门开得越大 = 电流越大

