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

- - -
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

>[!Math.asinh(x)]- 
>==x==--一个数值
>==return==--返回一个数值的反双曲正弦值

>[!Math.acosh(x)]- 
>==x==--一个数值
>==return==--返回一个数值的反双曲余弦值

>[!Math.atanh(x)]-
>==x==--一个数值
>==return==--返回一个数的反双曲余弦值，若该数大于1或者小于-1则返回NaN

>[!Math.pow(base,exponent)]-
>==base==--基数
>==exponent==--指数
>==return==--返回基数base的指数exponent次幂

>[!Math.exp(x)]-
>==x==--一个数值
>==return==--返回e^x

>[!note]- Math.expm1(x)
>==x==--任意数字
>==return==--返回E^x  -1

>[!note]- Math.log10(x)
>==x==--任意数字
>==return==--返回一个数字以10为底的对数，若传入的参数小于0，则返回NaN
>*例子*：Math.log10（100）； // 2
>*拓展*：logb(c),以b为底的对数，底数b要乘方多少次才能得到c。

>[!note]- Math.log1p(x)
>==x==--任意数字
>==return==--返回一个数字加一后的自然对数（底为E）,即loge(x+1)
\

>[!note]- Math.log2(x)
>==x==--任意数字
>==return==--返回一个数字以2为底的对数。若传入的参数小于0，则返回NaN

>[!note]- Math.floor(x)
>==x==--一个数字
>==return==--返回小于等于x的最大整数

>[!note]- Math.ceil(x)
>==x==--一个数值
>==return==--向上舍入，返回大于等于x的最小整数

>[!note]- Math.min(value1, ... , valueN)
>==参数==--0个或多个数字
>==return==--返回给定数值中最小的数，若任一参数不能转换为数值则返回NaN，没有参数则返回-Infinity

>[!note]- Math.max(value1, ... , valueN)
>==参数==--0个或多个数字
>==return==--返回给定数值中最大的数，若任一参数不能转换为数值则返回NaN，没有参数则返回-Infinity

>[!note]- Math.random()
>==return==--无参数，返回一个大于等于0且小于1的伪随机浮点数

>[!note]- Math.round(x)
>==x==--一个数值
>==return==--返回x四舍五入到最接近的整数

>[!note]- Math.fround(doubleFloat)
>==doubleFloat==--一个Number，若参数为非数字类型，则会被转成数字。无法转换则设置为NaN
>==return==--doubleFloat最接近的32位单精度浮点数表示

>[!note]- Math.trunc(value)
>==value==--任意数字
>==return==--value的整数部分

>[!note]- Math.sqrt(x)
>==x==--一个数值
>==return==--返回一个数的平方根，若参数为负值则返回NaN

>[!note]- Math.cbrt(x)
>==x==--任意数字
>==return==--x的立方根

>[!note]- Math.hypot(value1,value2, ...)
>==value1,value2, ...==--任意个数字
>==return==--将所提供的参数求平方和后开平方根。若有参数不能转换为数字，则返回NaN

>[!note]- Math.sign(x)
>==x==--任意数字
>==return==--返回一个数字的符号，指示数字是正数，负数还是零

***静态属性：***
>[!tip]- Math.E
>表示欧拉数，即自然对数的底数e，其值约为2.718

- - -
## 日期对象（Date）
#日期对象API
>[!success]- Date实例
>（1）new Date()
>==无参数==
>新创建的Date对象表示实例化时刻的日期和时间
>- - -
>（2）new Date(value)
>==value==--一个Unix时间戳，它是一个整数值，表示自1970年1月1日00:00:00 UTC以来的毫秒数
>- - -
>（3）new Date(dateString)
>==dateString==--表示日期的字符串值。该字符串应该能被Date.parse()正确方法识别。
>- - -
>（4）new Date(year, monthIndex [, day [, hours [, minutes [, seconds [ , milliseconds ]]]]]);
>==year==--表示年份的整数值，0-99会被映射至1900年至1999年，其他值代表实际年份
>==monthIndex==--表示月份的整数值，从0到11
>==date(可选)==--表示一个月中的第几天的整数值，从1开始，默认值为1
>==hours(可选)==--表示一天中的小时数的整数值，默认为0
>==minutes(可选)==--表示一个完整时间中的分钟部分的整数值，默认为0
>==seconds==--表示一个完整时间中的秒部分的整数值，默认为0
>==milliseconds==--表示一个完整时间的毫秒部分的整数值，默认为0

## String对象
#字符串对象API
>[!success]- 构造函数 new String(thing)
>String对象用于表示和操作字符序列
>==thing==--任何要转换为字符串的内容
>==return==--返回String类型的原始值
>***注：***String函数返回一个字符串（即原始值）；而String（）生成了一个类型为String的实例（即一个对象包装器）

***静态方法：***
>[!tip]- String.fromCharCode(num1,num2,/* ..., */ numN)
>==numN==--表示一个UTF-16码元
>==return==--一个长度为N的字符串，由N个指定的UTF-16码元组成
>*例子：*String.fromCharCode(65,66,67)；返回ABC

***实例方法：***
>[!example]- String.prototype.toLowerCase()
>==return==--将字符串转换为小写形式后的值

## 向量相关（Vec3）
>[!error]- 向量
>数学定义：有序的三元数组（x,y,z），几何上表示为**从三维坐标系原点（0,0,0）指向空间中点（x,y,z）的有向线段**。向量核心特征是方向（线段指向的方位）和大小（线段长度，非负数值）
>==**向量长度：**== length = $x^2 + y^2 + z^2$
>==**单位向量：**==Normaliz = $(x/length,y/length, z/length)$。模为1的向量
>==**向量加法：**== $Vec3(a.x+b.x, a.y+b.y, a.z+b.z)$。两个向量的和向量
>==**向量减法：**== $Vec3(a.x-b.x, a.y-b.y, a.z-b.z)$。从向量b指向向量a的新向量
>==**数乘：**== $Vec3(x*n, y*n, z*n)$。放大/缩小向量的大小，方向不变
>==**点乘：**== $a·b = a.x*b.x + a.y*b.y + a.z*b.z$。结果是一个标量（数字），非向量
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;核心含义：**>0**，夹角<90°（方向相近）；**=0**，夹角=90°（垂直）；**<0**，夹角>90°（方向相反）。
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;公式延伸：$cosθ = a·b / |a|*|b|$。为两向量夹角
>==**叉乘：**== $a*b = Vec3(a.y*b.z - a.z*b.y, a.z*b.x - a.x*b.z, a.x*b.y - a.y*b.x)$。结果是一个新向量，且垂直于a和b所在的平面。新向量的模等于a和b组成的平行四边形的面积。常用于判断相对左右方向。
>==**向量投影：**== 向量a在向量b上的投影 = $(a·b / |b|²)$。将向量a投射到向量b所在直线上的新向量。

***静态方法：***
>[!tip]- $Vec3.zero$<Out extends IVec3Like>($out: Out$): Out;
>==returnd==--将out赋值为零向量

>[!tip]- $Vec3.clone$<Out extends IVec3Like>($a: Out$): Vec3;
>==a==--源对象
>==return==--获得指定向量的拷贝，返回新创建的Vec3实例

>[!tip]- $Vec3.copy$<Out extends IVec3Like,Vec3Like extends IVec3Like>($out: Out, a: Vec3Like$): Out;
>==a==--源对象
>==return==--返回复用的out对象

>[!tip]- $Vec3.set$<Out extends IVec3Like>($out: Out,x: number, y: number, z: number$): Out;
>==out==--目标对象
>==return==--返回out设置成x,y,z的值

>[!tip]- $Vec3.add$<Out extends IVec3Like>($out: Out, a: IVec3Like, b: IVec3Like$): Out;
>==out==--结果存储对象
>==a==--第一个加数向量
>==b==--第二个加数向量
>==return==--返回两向量相加的结果out

>[!tip]- $Vec3.subtract$<Out extends IVec3Like>($out: Out, a: IVec3Like, b: IVec3Like$) : Out;
>==out==--结果赋值对象
>==a==--被减数向量
>==b==--减数向量
>==return==-- 计算两个向量的差(a-b)的结果out,out方向是由b指向a

>[!tip]- $Vec3.multiply$<Out extends IVec3Like>($out: Out, a: IVec3Like, b: IVec3Like$): Out;
>==out==--结果赋值对象
>==a==--第一个乘数向量
>==b==--第二个乘数向量
>==return==--计算两个向量的分量级乘法的结果向量out。常对向量做（轴级独立缩放/反向）

>[!tip]- $Vec3.divide$<Out extends IVec3Like>($out: Out, a: IVec3Like, b: IVec3Like$): Out;
>==out==--结果存储对象
>==a==--被除数向量
>==b==--除数向量
>==return==--计算两个向量的分量级除法（对应x/y/z分别相除）的结果out。几何意义是对向量a的各轴做“反向缩放”。

>[!tip]- $Vec3.ceil$<Out extends IVec3Like>($out: Out, a: IVec3Like$): Out;
>==out==--结果存储对象
>==a==--需要取整的源向量
>==return==--对向量a的x/y/z三个分量分别执行向上取整，返回结果out

>[!tip]- $Vec3.floor$<Out extends IVec3Like>($out: Out, a: IVec3Like$): Out;
>==out==--结果存储对象
>==a==--需要取整的源向量
>==return==--对向量a的x/y/z三个分量分别执行向下取整操作，返回结果out

>[!tip]- $Vec3.min$<Out extends IVec3Like>($out: Out, a: IVec3Like, b: IVec3Like$): Out;
>==out==--结果存储对象
>==a==--第一个对比向量
>==b==--第二个对比向量
>==return==--对向量a和b的x/y/z分量分别取最小值，返回结果out

>[!tip]- $Vec3.max$<Out extends IVec3Like>($out: Out, a: IVec3Like, b: IVec3Like$): Out;
>==out==--结果存储对象
>==a==--第一个对比向量
>==b==--第二个对比向量
>==return==--对两个向量a和b的x/y/z分量分别取最大值，返回结果out

>[!tip]- $Vec3.round$<Out extends IVec3Like>($out: Out, a: IVec3Like$): Out;
>==out==--结果存储对象
>==a==--需要取整的源向量
>==return==--对向量a的x/y/z三个分量分别执行四舍五入操作，返回结果out

>[!tip]- $Vec3.multiplyScalar$<Out extends IVec3Like, Vec3Like extends IVec3Like>($out: Out, a: Vec3Like, b: number$): Out;
>==out==--结果存储对象
>==a==--源向量
>==b==--乘数，数字类型
>==return==--对向量a的x/y/z三个分量统一乘以数字b，返回结果out

>[!tip]- $Vec3.scaleAndAdd$<Out extends IVec3Like>($out: Out, a: IVec3Like, b: IVec3Like, scale: number$): Out;
>==out==--结果存储对象
>==a==--被加向量
>==b==--待缩放后相加的向量
>==scale==--缩放系数，数字
>==return==--$a+b*scale$，返回结果out

>[!tip]- $Vec3.distance$($a: IVec3Like, b: IVec3Like$): number;
>==a==--第一个点/向量
>==b==--第二个点/向量
>==return==--计算出两个3D点（向量a和b）之间的欧式直线距离（即空间中两点的直线长度）

>[!tip]- $Vec3.squaredDistance$($a: IVec3Like, b: IVec3Like$): number;
==a==--第一个点/向量
==b==--第二个点/向量
==return==--计算两个3D点（向量a和b）之间直线距离的平方值

>[!tip]- $Vec3.len$($a: IVec3Like$): number;
>==a==--需要计算长度的向量
>==return==--计算单个3D向量a的模长（长度）（即向量从原点到终点的直线距离）

>[!tip]- $Vec3.lengthSqr$($a: IVec3Like$): number;
>==a==--需要计算长度平方的向量
>==return==--计算单个3D向量a的模长平方值

>[!tip]- $Vec3.negate$<Out extends IVec3Like>($out: Out, a: IVec3Like$): Out;
>==out==--结果存储对象
>==a==--需要取反的源向量
>==return==--对向量a的x/y/z分量取相反数（方向完全反转，长度保持不变）

>[!tip]- $Vec3.invert$<Out extends IVec3Like>($out: Out, a: IVec3LIke$): Out;
>==out==--结果存储对象
>==a==--需要取倒数的源向量
>==return==--对向量a的x/y/z分量分别执行取倒数操作（1/分量），返回结果out。

>[!tip]- $Vec3.invertSafe$<Out extends IVec3Like>($out: Out, a: IVec3Like$): Out;
>==out==--结果存储对象
>==a==--需要取倒数的源向量
>==return==--对向量a的x/y/z分量安全取倒数（自动处理0/极小分量，避免）

>[!tip]- $Vec3.normalize$<Out extends IVec3Like>($out: Out, a: IVec3Like$): Out;
>==out==--结果存储对象
>==a==--需要归一化的源向量
>==return==--将a归一化为单位向量（方向保持不变，模长强制变为1）

>[!tip]- $Vec3.dot$<Out extends IVec3Like>($a: Out, b: IVec3Like$): number;
>==a==--第一个向量
>==b==--第二个向量
>==return==--计算两个3D向量a和b的点积（数量积），返回一个标量（纯数字）。

>[!tip]- $Vec3.cross$<Out extends IVec3Like>($out: Out, a: IVec3Like, b: IVec3Like$): Out;
>==out==--结果存储对象
>==a==--第一个向量，基准向量
>==b==--第二个向量，待判断向量
>==return==--计算两个3D向量a和b的叉积（叉积/向量积），返回一个新向量。

>[!tip]- $Vec3.lerp$<Out extends IVec3Like>($out: Out, a: IVec3Like, b: IVec3Like, t: number$): Out;
>==out==--结果存储对象
>==a==--起点向量
>==b==--终点向量
>==t==--插值系数，通常取0-1
>==return==--对两个3D向量a和b做线性插值，根据插值系数t计算出a到b连线上的中间向量，结果赋给out。

>[!tip]- $Vec3.slerp$<Out extends IVec3Like>($out: Out, from: Readonly<IVec3Like>, to: Readonly<IVec3Like>, t: number$) => Out;
>==out==--结果存储对象
>==from==--起始方向向量，已归一化
>==to==--目标方向向量，已归一化
>==t==--插值系数，通常0-1
>==return==--对两个单位向量（方向向量）做球面线性插值，沿球面弧度平滑过渡（而非直线），保证插值过程中方向向量的模长始终为1。返回值为Out类型，插值后的单位方向向量。

>[!tip]- $Vec3.random$<Out extends IVec3Like>($out: Out, scale?: number$): Out;
>==out==--结果存储对象
>==scale==--可选，缩放系数，默认1
>==return==--生成一个各分量为随机值的3D向量，可选scale参数控制向量的模长范围。

>[!tip]- $Vec3.transformMat4$<Out extends IVec3Like>($out: Out, a: IVec3Like, m: IMatLike$): Out;
>==out==--结果存储对象
>==a==--待变换的3D向量
>==m==--4\*4变换矩阵
>==return==--将3D向量a（点/方向）通过4\*4矩阵m进行齐次变换，返回结果out。核心用于坐标空间转换。

