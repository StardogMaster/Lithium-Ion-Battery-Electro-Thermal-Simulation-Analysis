# Lithium-Ion-Battery-Electro-Thermal-Simulation-Analysis
This is a simulation and analysis project for lithium battery performance. Based on a second-order RC electrical-thermal coupling model and real battery datasets, it can reproduce the operational characteristics and performance degradation patterns of lithium batteries under various scenarios.

## Project Overview
This project focuses on simulating and analyzing lithium-ion battery behavior under real-world scenarios, with core functions:
1. Second-order RC electro-thermal coupling simulation (voltage/temperature/current during discharge)
2. NASA battery dataset calibration (capacity decay & impedance growth)
3. Battery model parameter estimation
4. Nonlinear current demand analysis ("death spiral" effect)
5. Runtime sensitivity analysis (power/temperature/aging impact)
6. Cross-validation of simulation results


## Project Structure
projection
├── Source Codes
│   ├── battery_thermal_rc_model.py      # 二阶RC电热耦合电池模型：仿真放电过程的电压、温度、电流
│   ├── electrothermal_coupling.py       # 简化版电热耦合模型：验证“电流-温度-内阻”耦合关系
│   ├── nasa_metadata_cleaning.py        # NASA电池数据集清洗与预处理
│   ├── nasa_calibration_seaborn.py      # NASA数据校准：容量衰减+阻抗增长拟合
│   ├── parameter_estimation.py          # 电池模型参数估计（RC网络、老化系数等）
│   ├── power_nonlinearity_analysis.py   # 功率非线性分析：“电压下降→电流激增”的死亡螺旋效应
│   ├── sensitivity_analysis.py          # 运行时间敏感性分析：功率/温度/老化对续航的影响
│   └── cross_validation.py              # 模型交叉验证：验证仿真结果的可靠性
├── Data Files
│   ├── metadata.csv                     # NASA B0005电池测试数据：容量、阻抗等老化指标
│   ├── user_behavior_dataset.csv        # 手机用户行为数据：屏幕时长、电池消耗等
│   ├── RedmiK70pro.csv                  # Redmi K70 Pro使用实验数据
│   ├── data.csv                         # 补充性电池测试数据
│   └── Mobiles Dataset(2025).csv        # 2025年多机型手机电池数据集
└── Output Figures
    ├── Fig1_Voltage.png                 # 新旧电池端电压对比曲线
    ├── Fig2_Temperature.png             # 电池放电过程温度变化曲线
    ├── Fig3_Current.png                 # 放电电流变化+雪崩效应标注
    ├── nasa_calibration_seaborn.png     # NASA数据校准后的容量/阻抗曲线
    ├── parameter_identification_seaborn.png  # 参数估计结果图
    └── power_nonlinearity_analysis.png  # 功率非线性的电流激增曲线
