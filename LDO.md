LDO电路拓扑图  
<img width="448" height="231" alt="f84663b10155175ce7e84ea439bff3b0" src="https://github.com/user-attachments/assets/8d2f0f73-887e-4d68-8b8b-769c8b5134c6" />


```mermaid
graph TD
    %% 样式定义
    classDef steady fill:#e3f2fd,stroke:#1565c0,stroke-width:2px;
    classDef transient fill:#fff3e0,stroke:#ef6c00,stroke-width:2px;
    classDef dropout fill:#ffebee,stroke:#c62828,stroke-width:2px;

    A[正常稳态 Steady State<br/>运放稳定控制G极]:::steady
    
    %% 负载突增路径
    A -->|负载电流瞬间增大| B(负载突增 Transient Heavy):::transient
    B -->|运放来不及反应| C[输出电容 C_T 放电支撑<br/>Vout 产生微幅跌落]
    C -->|运放感知反馈下降| D[迅速拉低 Vgate<br/>PMOS 阀门全开]
    D -->|大电流涌入供给负载并为电容充电| A

    %% 负载突降路径
    A -->|负载突然进入休眠| E(负载突降 Transient Light):::transient
    E -->|多余电流无处可去| F[电流灌入 C_T 充电<br/>Vout 产生突波尖峰]
    F -->|运放感知反馈上升| G[迅速拉高 Vgate<br/>PMOS 阀门关小]
    G -->|电容缓慢释放多余电荷| A

    %% 压差过低路径
    A -->|输入电压 Vin 严重下跌| H(压差过低 Dropout):::dropout
    H -->|运放将 Vgate 压低至 0V| I[PMOS 完全导通<br/>退化为固定电阻 Rdson]
    I -->|Vout = Vin - I*Rdson<br/>失去稳压能力| A
