## 摘要
calc主要为了解决js浮点数计算的精度问题。
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

