# countdown
EDA project

基于FPGA实验板设计一台投币式手机充电仪的控制电路,可以实现投币、实时显示投币数额和充电时间等功能。要求用状态机完成控制电路的设计。具体操作过程如下:

1. 刚上电即“初始状态”,数码管显示全灭。
2. 按“开始”键后进入准备投币状态,数码管显示“0000”。
3. 矩阵键盘可直接输入投币数额1~20角, 并实时显示在左侧 2 位数码管上。
例如:输入 5 角(按下键 5)时,数码管显示 05;输入 15 角(先后按下键 1、键 5)时,数码管上先后显示 01、15。
4. 投币(按下数字键)时,2 倍于投币数额的允许充电时间实时显示在右侧 2 位数码管上。
5. 输入大于20角,均显示20;则充电时间最多显示40。 例如:先后输入 4、5,金额先后显示 04、20,时间先后显示 08、40。
6. 未确认充电之前可随时“清零”。清零回至“开始状态”,10秒无动作回到“初始状态”。
7. 确认充电后,充电时间(最多从40)开始倒计时,此时投币数额仍保持 显示;当时间计至 0 时,投币数额也同时归 0,回到“开始状态”,10 秒后回到 “初始状态”。
<br>说明:按照正常的输入,不会先输入 0。若先后输入 1、2、3,可认定输入 为 12 或是 23。由设计者确定。


## 免责声明

严禁直接使用这份代码用于完成大作业或作其他用途。由此造成的一切后果，原作者概不负责。
