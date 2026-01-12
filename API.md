# 全局属性
#全局属性API
- `Infinity`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;是一个数值，表示无穷大
# ==数字对象（Number）==
#数字对象API
***属性：***
>[!tip]- Number.MAX_VALUE
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;表示在JavaScript中可表示的最大数值，大约为1.797e308

>[!tip]- Number.MIN_VALUE
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;表示在JavaScript中可表示的最小正数值，大约为2e-1074

>[!tip]- Number.NaN
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;表示非数字值。NaN是Number类型的特殊值，代表“无效的数值运算结果”。

>[!tip]- Number.NEGATIVE_INFINITY
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;表示负无穷值

>[!tip]- Number.POSITIVE_INFINITY
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;表示正无穷大值

>[!tip]- Number.EPSILON
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;此属性表示1与大于1的最小浮点数之间的差值。值为2e-52
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;使用适合要比较的数字的数量级和精度的阈值。

>[!tip]- Number.MIN_SAFE_INTEGER
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;表示在JS中最小的安全整数-（2e53-1）

>[!tip]- Number.MAX_SAFE_INTEGER
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;表示在JS中最大的安全整数（2e53-1）

***方法：***
>[!note]- Number.parseFloat(string)
>==string==--要解析的值，会被强制转换为字符串
>==return==--解析得到的浮点数，若第一个非空白字符不能转换成数字，则返回NaN

>[!note]- Number.parseInt(string, radix?)
>==参数==：string--要被解析的值，会被强制转化为字符串
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;radix--可选进制数，2到36之间的整数，表示string的基数，默认为10
>==返回==：解析出的一个整数；
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;若radix小于2或大于36，或第一个非空白字符不能转换为数字，则返回NaN。

>[!note]- Number.isFinite(value)
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;判断传入值是否是一个有限数——检查给定值是一个数字，且该数字既不是正的Infinity，也不是负的Infinity或NaN。
>==value==--要测试有限性的值
>==return==--若value是有限数，则返回true，否则为false

>[!note]- Number.isInteger(value)
>==value==--要测试是否为整数的值
>==return==--若给定的值是整数，则返回true，否则为false

>[!node]- Number.isNaN(value)
>==value==--要测试是否为NaN的值
>==return==--若是NaN的数字，则返回true，否则返回false

>[!node]- Number.isSafeInteger(testValue)
>==testValue==--要测试是否为安全整数的值
>==return==--若是一个安全整数，则返回true，否则为false

***实例方法***
>[!example]- Number.prototype.toExponential(fractionDigits?)
>==frationDigits==--可选，一个整数，用来指定小数点后面有几位数字。默认设置为完整表示该数字所需要的数字。
>==return==--一个以指数表示法表示给定Number对象的字符串，其小数点前为一位数字，小数点后舍入到fractionDigits位。
>*例子*：console.log(77.1234.toExponential());  // 7.71234e+1
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;77.1234本身是不带Number属性/方法，是调用方法JS自动给转成Number实例了

>[!example]- Nubmer.proptotype.toFixed(digits?)
>==digits==--小数点后的位数。范围0-100，若参数被省略，默认为0
>==return==--使用顶点表示法表示给定的字符串

>[!example]- Number.proptotype.toPrecision(precision?)
>==precision==--一个指定有效位数的整数
>==return==--一个以顶点表示法或指数表示法表示Number对象的字符串，该字符串四舍五入到precision个有效数字。
>*注意*：当需要表示的有效数字位数无法用定点表示法清晰展示时，就会自动切换到指数表示法。

>[!example]- Number.proptotype.toString(radix?)
>==radix==--一个整数，范围在2-36之间，用于指定表示数字值的基数，默认为10。
>==return==--一个表示指定数字值的字符串。


# ==数学对象（Math）==
#数学对象API
***方法：***
>[!node]- Math.abs(x)
>==x==--一个数字
>==return==--x的绝对值，若x是负数（包括-0），则返回-x，否则返回x
>*注意：*这个方法将参数强制转换为数字。无法强制转换的值将变成NaN

>[!node]- Math.sin(x)
>==x==--一个数值（以弧度为单位）
>==return==--x的正弦值，-1到1，若x为Infinity、-Infinity或NaN，则返回NaN

>[!node]- Math.cos(x)
>==x==--一个以弧度为单位的数值
>==return==--返回一个-1到1的数值，表示角度（单位：弧度）的余弦值

>[!node]- Math.tan(x)
>==x==--一个数值，表示一个角（单位：弧度）
>==return==--返回一个数值，表示一个角的正切值

>[!node]- Math.asin(x)
>==x==--一个数值，-1到1之间的数值
>==return==--返回一个介于-π/2到π/2弧度的反正弦值（对应的角度的弧度），若接收的参数超出范围，则返回NaN

>[!node]- Math.acos(x)
>==x==--一个数值，范围为-1到1
>==return==--返回一个0到π的数值（对应的角度的弧度）。若传入的参数值超出了限定的范围，将返回NaN

>[!node]- Math.atan(x)
>==x==--一个数值
>==return==--返回一个-π/2到π/2弧度之间的数值（反正切值）

>[!node]- Math.atan2(y,x)
>返回从原点（0,0）到（x,y）点的线段与x轴正方向之间的平面角度（弧度值）
>==y,x==--数值
>==return==--返回一个-pi到pi之间的数值，表示点（x,y）对应的偏移角度。这是一个逆时针角度，以弧度为单位，正X轴和点（x,y）与原点连线之间。

>[!node]- Math.sinh(x)
>==x==--任意数字，单位为度
>==return==--返回一个数字（单位为角度）的双曲正弦值

>[!Math.cosh(x)]- 
>==x==--数值
>==return==--返回数值的双曲余弦函数

>[!Math.tanh(x)]- 
>==x==--待计算的数值
>==return==--返回一个数的双曲正切函数


