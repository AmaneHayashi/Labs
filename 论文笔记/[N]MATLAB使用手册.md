# MATLAB学习笔记

### 1. 线型、颜色、标记符
线型|说明|颜色|说明|标记符|说明
:---:|:---:|:---:|:---:|:---:|:---:
*-*|实线(默认)|*r*|<font color='red'>红色(red)</font>|+|加号
*--*|双划线|*g*|<font color='green'>绿色(green)</font>|*o*|空心圆
*:*|虚线|*b*|<font color='blue'>蓝色(blue)</font>|*|星号
*-.*|点划线|*c*|<font color='cyan'>青绿色(cyan)</font>|.|实心圆
|||*m*|<font color='magenta'>洋红色(magenta)</font>|*x*|叉号
|||*y*|<font color='yellow'>黄色(yellow)</font>|*s*|正方形
|||*k*|<font color='black'>黑色(black)</font>|*d*|菱形
|||*w*|<font color='white'>白色(white)</font>|^|上三角形
|||||*v*|下三角形
|||||>|右三角形
|||||<|左三角形
|||||*p*|五角星
|||||*h*|六边形

举例：
- `'-ko'`：实线，黑色，空心圆
- `'-.bx'`：点划线，蓝色，叉号
- `'--r^'`：双划线，红色，上三角形
- `':mx'`：虚线，洋红，叉号
- `'--g^'`：双划线，绿色，上三角形
- `'-.bv'`：点划线，蓝色，下三角形

### 2. 2D绘图函数
函数名|函数意义|举例
:---:|:---:|:---:
`figure(序号)`|产生一张图片|`figure(1)`
`subplot(行,列,序号)`|分区域绘图|`subplot(2,1,1)`
`plot(X,Y,样式,…)`|绘图函数|`plot(x,y1,’-ko’,x,y2,’:r^’)`
`semilogx/semilogy(X,Y,样式,…)`|单轴对数坐标绘图函数|`semilogy(x,y1,’-ko’,x,y2,’:r^’)`
`loglog(X,Y,样式,…)`|双轴对数坐标绘图函数|`loglog(x,y1,’-ko’,x,y2,’:r^’)`
`legend(字符串,...)`|标注图例(字符串数应与因变量数一致)|`legend('A','B','C')`
`title(字符串)`|给绘图加标题|`title('Simulation I')`
`xlabel(字符串)/ylabel(字符串)`|给坐标轴取名|`ylabel('y')`
`xlim([min max])/ylim[min max]`|限制X/Y轴区间|`xlim([0 10])`
`axis([Xmin Xmax Ymin Ymax])`|限制X、Y轴区间|`axis([1 2 1 -1])`
`grid on`|增加网格|`grid on`

标题、坐标轴名的备注：
```matlab
% 可以是多行的
xlabel({'Population','(in thousands)'})

% 可以通过TeX标记添加数学公式
xlabel('-2\pi \leq x \leq 2\pi')`,`ylabel('e^t')

% 可以添加变量值
year = 2020
xlabel(['Population for Year ',num2str(year)])

% 可以修改属性
xlabel('Population','FontSize',12,'FontWeight','bold','Color','r')

% 可以作为对象被引用
t = xlabel('Population');
t.Color = 'red';
```

举例：
```matlab
figure(1)
subplot(2,1,1)
semilogy(simParamVector,timeThPolicyAvrMatrix(g,i,j),'-ko',simParamVector,timePolicyAvrMatrix(g,i,j),'-.bx',simParamVector,timeIterativeAvrMatrix(g,i,j),'--r^','LineWidth',2)
legend('New','Policy iteration','Value iteration')
xlabel('-\alpha_2','FontSize',12)
ylabel('Computation time (s)','FontSize',12)
xlim([0 10])
```

### 3. `norm()`函数
- $1-范数$：${\left\| X \right\|_1} = \sum\limits_{i = 1}^n {\left| {{x_i}} \right|}$

- $2-范数$：${\left\| X \right\|_2} = {\left( {\sum\limits_{i = 1}^n {{x_i}^2} } \right)^{\frac{1}{2}}} = \sqrt {\sum\limits_{i = 1}^n {{x_i}^2} }$
  
- $p-范数$：${\left\| X \right\|_p} = {\left( {\sum\limits_{i = 1}^n {{{\left| {{x_i}} \right|}^p}} } \right)^{\frac{1}{p}}}，p≥1$
  
- $无穷范数$：${\left\| X \right\|_\infty } = \mathop {\max }\limits_{1 \le i \le n} \left| {{x_i}} \right|$

- `round()`：四舍五入
- `ceil()`：天花板
- `floor()`：地板