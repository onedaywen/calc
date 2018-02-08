## 摘要
calc主要为了解决js浮点数计算的精度问题。例如在console中打印下
```
0.1 + 0.2 = 0.30000000000000004
19.9 * 100 = 1989.9999999999998
```
浮点数在计算机中是以二进制来存储的。对于整数，可用公比为2的等比数列求和公式来计算,对于小数公比则为1/2。n为数的位数。
```
Sn = (a1 - a1 * Math.pow(q, n + 1)) / (1 - q);
```
根据上述公式，公比为2时，Sn可表示任意整数。
```
Sn = (a1 * (Math.pow(2, n + 1) - 1));
```
根据上述公式，公比为1/2时，n为有限值时，Sn无法表示任意小数，即存在无限小数。而计算机能表示的精度是有限的，必然存在误差。
```
Sn = (a1 * (2 - Math.pow(2, -n)));
```
## 引入方式
calc.js支持script标签引入,挂载在全局的window.calc变量下。
```
<script type="text/javascript" src="./calc.js"></script>
```
也支持通过es6的import语法
```
import calc from 'calc';
```
也可以通过commonjs规范引入
```
const calc =  require('calc');
```
calc提供了四个方法。
```
calc.add(a, b);
calc.sub(a, b);
calc.mul(a, b);
calc.div(a, b);
```

