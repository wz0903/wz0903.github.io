# 大气湍流针对性复习


## 一、Lorenz方程
$$
\dot{X}=-\sigma X+\sigma Y,\quad \dot Y=R_a X-Y-XZ,\quad \dot Z=-bz+XY
$$

**各项的物理意义**

模型各项的意义：模型三个状态量X,Y,Z分别表示垂直速度、位温在不同空间频率上的扰动幅度（随时间变化），模型有三个参数，分别是普朗特数$\sigma=\frac{\nu}{\kappa}$是分子黏性和热扩散系数比值（给定流体则为常数），$R_a=-\sigma R_iR_e^2$为Rayleigh数，$b=\frac{8}{3}$为常数。系统有唯一驱动力$R_aX$，耗散项$-\sigma X,-Y,-bZ$和非线性项$-XZ,XY$。驱动+耗散+非线性将使得系统可能出现复杂现象。

Lorenz方程对研究大气湍流的物理意义

**模型的来源和研究的问题**：研究黏性不可压缩流体热对流问题，模型简化为上下两个无穷大有温度差的平板间流体的温度扰动与垂直运动间的作用。在N-S方程基础上，用(空间)谱截断方法，得到了三维非线性自洽动力系统，即以上的Lorenz模型。

**非线性系统演化的多样形态**：模型构成三维非线性自洽动力系统，系统有驱动+耗散+非线性的性质，可能出现多样形态和混沌现象。已经证实，随着驱动力参数$R_a\in (0,+\infty)$由小变大，系统经历定常状态，最终达到混沌状态。

**混沌概念和性质**：确定的系统出现的貌似随机的不确定的现象，系统对初始条件敏感，即所谓的蝴蝶效应。混沌现象是系统本身的特征，是系统内在的随机现象，而非外部扰动所引起。在相空间表现为奇怪吸引子。混沌对湍流发生的认识有重要的意义。

**对大气湍流发生的认识**：大气运动常为湍流运动，$R_e:10^6\sim10^8$，是大气运动的本身具有的特征。




## 二、三个参数的物理意义：$R_i$，$R_e$，Monin-Obukhov长度

**Reynolds数**

$$
R_e=\frac{UL}{\nu}=\frac{惯性力}{黏性力}
$$
源于雷诺实验，其中$U$是流体速度的尺度，$L$是流体运动空间的尺度，$\nu$是分子粘性系数。雷诺数是非线性惯性项和黏性力之比。$R_e$是确定黏性流体宏观运动形态（层流和湍流）的唯一参数。惯性力的速度剪切驱动湍流发展，黏性力减弱扰动发展。因此当$R_e$较小时，与惯性力相比，黏性力较大，扰动衰减，流动稳定为层流；$R_e$较大时，惯性力较大，扰动容易发展增强，流动不稳定最终形成湍流。临界Reynolds数为2000，大气中$R_e\sim10^6$，为湍流状态。

**Richardson数**
$$
R_i=\frac{\frac{g}{\bar{\theta}}\frac{\partial \bar{\theta}}{\partial z}}{(\frac{\partial \bar{u}}{\partial z})^2}=\frac{N^2}{(\frac{\partial \bar{u}}{\partial z})^2}
$$
源于湍流能量方程，其中$N^2=\frac{g}{\bar{\theta}}\frac{\partial  \bar{\theta}}{\partial z}$，$N$称为Brunt（内波）频率，$R_i$是浮力和剪切之比，是热力湍流因素和机械湍流因素之比。大气湍流中用$R_i$表示层结对湍流强弱的影响。大气层结不稳定时$N^2<0$，内能驱动释放湍流发展；中性层结时只有机械湍流；大气层结稳定时，剪切力驱动湍流发展，一般$R_i$越小，越容易产生湍流，大气边界层内，白天$R_i<0$，夜间$R_i>0$，大气湍流发展的临界值为0.25。

**Monin-Obukhov长度**
$$
L=-\frac{u_*^3}{k_0\frac{g}{\bar{T}}\frac{H'}{\bar{\rho}c_p}}=-\frac{u_*^3}{k_0\frac{g}{\bar{\theta}}\overline{w'\theta'}}=\frac{u_*^3}{k_0\frac{g}{\bar{\theta}}u_*\theta_*}
$$

是由大气近地面层相似理论得到的结果。其中浮力因子$\frac{g}{\overline{T}}$，湍流热通量因子$\frac{H'}{\bar{\rho}c_p}=\overline{w'T'}=-K_T\frac{\partial \overline{\theta}}{\partial z}=-u_*T_*$。$u_*$是摩擦速度，其平方可以代表动量通量。反映了机械和热力因素对近地面层大气运动的共同作用。稳定层结$\overline{w'T'}<0,\frac{\partial \bar{\theta}}{\partial z}>0,T_*>0,L>0$，不稳定层结$\overline{w'T'}>0,\frac{\partial \bar{\theta}}{\partial z}<0,T_*<0,L<0$，中性层结$T_*=0,L\rightarrow \infty$。从而得到近地面层不同的通量-廓线关系。**稳定度参数**$\frac{z_i}{L}$进行无量纲化满足流体力学相似性。


## 四、相似理论，$\Pi$定理，并推导近地面中性层结下的风廓线通量关系表达式

在近地层中，由于大气受到下垫面影响剧烈，气象要素日变化很大，同时近地层厚度小，湍流的各种通量随高度的变化很小，因此称为常通量层。

**近似理论**是一种经验方法，将复杂的动力过程参数化。他认为对同一类型层结，温度，湿度，风速廓线表达式中，将各个变量除以适当的特征量后可转换成无量纲形式，都是无量纲稳定度因子（无因次高度）$\frac{z}{L}$的普适函数，即同一类型层结其普适函数形式一样。

相似理论的基础是$\bold{\Pi}$**定理**：设某个物理问题涉及$n$个物理量，其中有$m$个独立量纲，则可以形成$(n-m)$个无因次量（无量纲量）$\Pi_1,\Pi_2,...,\Pi_{n-m}$，他们构成一个关系式$F(\Pi_1,\Pi_2,...,\Pi_{n-m})=0$。

特别的，若只构成一个无因次量$\Pi$，则$\Pi=constant$；若构成两个无因次量$\Pi_1,\Pi_2$，则$\Pi_2=\varphi(\Pi_1)$。

**中性层结下风速通量廓线关系**
近地面层中性层结有$\frac{\partial \overline{\theta}}{\partial z}=0$，可以认为风速随高度的廓线$\frac{\partial \overline{u}}{\partial z}$是由动量通量$u_*$和高度$z$来决定的，即$f(\frac{\partial \overline{u}}{\partial z},u_*,z)=0$。

上式中有三个物理量$n=3$，两个独立量纲[Length]h和[Time]$m=2$，因此有一个无因次量$\Pi$，满足$\Pi=(\frac{\partial \overline{u}}{\partial z})^a(u_*)^bz^c=[Length]^{(b+c)}[Time]^{(-a-b)}$所以$a=1,b=-1,c=1$，即$\Pi =\frac{\partial \overline{u}}{\partial z}(u_*)^{-1}z=Constant$，设$\Pi=\frac{1}{k_0}$，则
$$
\frac{z}{u_*}\frac{\partial \overline{u}}{\partial z}=\frac{1}{k_0}
$$
其中$k_0=0.35$是Von Karman常数。同理对位温分布$\partial_z\bar{\theta}$,湿度分布$\partial_z\bar{q}$有类似关系，$\frac{k_\theta z}{u_*}\frac{\partial \overline{\theta}}{{\partial z}}=1$,$\frac{k_q z}{u_*}\frac{\partial \overline{q}}{\partial z}=1$。


## 五、近地面层湍流交换系数和高度的关系
对非中性层结通量廓线关系

对稳定和不稳定层结，动力因子和热力因子同时发生作用，Monin-Obukhov认为，层结大气近地面的湍流性质决定于4个因子：$u_*,z,\frac{H'}{\overline{\rho}c_p},\frac{g}{\overline{\theta}}$，其中后两者是热力因子。
考察非中性层结下的近地面层风廓线，根据相似理论，有关系
$$f(\frac{\partial \overline{u}}{\partial z},u_*,z,\frac{g}{\overline{\theta}},\frac{H'}{\overline{\rho}c_p})=0$$
5个物理量，三个独立量纲[Length]、[Time]、[Temp]，所以存在2个无因次量$\Pi_1,\Pi_2$。
$$\Pi = (\frac{\partial \overline{u}}{\partial z})^a(u_*)^b(z)^c(\frac{g}{\overline{\theta}})^d(\frac{H'}{\overline{\rho}c_p})^e\\
=[Time]^{-a}(\frac{[Length]}{[Time]})^b[Length]^c(\frac{[Length]}{[Time]^2[Temp]})^d(\frac{[Length][Temp]}{[Time]})^e\\
=[Time]^{-a-b-2d-e}[Length]^{b+c+d+e}[Temp]^{-d+e}$$
如果$d=0$，则$e=0,b=-a,c=a$，令$a=1$，则$a=1,b=-1,c=1,d=0,e=0$。$\Pi_1 = \frac{z}{u_*}\frac{\partial \overline{u}}{\partial z}$。
如果$d=1$，则$e=1,b=-3-a,c=a+1$，令$a=0$，则$a=0,b=-3,c=1,d=1,e=1$。$\Pi_2 = \frac{z}{u_*^3}\frac{g}{\overline{\theta}}\frac{H'}{\overline{\rho}c_p}$。
$$
\Pi_2=\frac{z}{u_*^3}\frac{g}{\overline{\theta}}\frac{H'}{\overline{\rho}c_p}=\frac{z}{L},\quad L=\frac{u_*^3}{-k_0\frac{g}{\bar{\theta}}\frac{H'}{\bar{\rho}c_p}}=\frac{u_*^3}{-k_0\frac{g}{\bar{\theta}}}\overline{w'\theta'}=\frac{u_*^3}{k_0\frac{g}{\bar{\theta}}u_*\theta_*}\quad \text{Monin-Obukhov length}\\
\Pi_1 = f(\Pi_2)\rightarrow\frac{k_0z}{u_*}\frac{\partial \overline{u}}{\partial z}=\varphi_m(\frac{z}{L})=\varphi_m(\zeta)$$
**湍流交换系数**
近地面层认为是常通量层，有
$$\rho\overline{w'u'}=-\rho K_m\frac{\partial \overline{u}}{\partial z}=-\rho u_*^2\\
K_m=\frac{u_*^2}{\frac{\partial \overline{u}}{\partial z}}=\frac{\frac{k_0z}{u_*}u_*^2}{\frac{k_0z}{u_*}\frac{\partial \overline{u}}{\partial z}}=\frac{k_0u_*z}{\varphi_m(\zeta)} \tag{7.1}$$
湍流动能变化的原因有三个：切应力做功$-\overline{w'u'}\frac{\partial \overline{u}}{\partial z}$、浮力做功$\frac{g}{\overline{T}}\overline{w'T'}$和耗散率$\epsilon$，即
$$
\frac{\partial E}{\partial t}=-\overline{w'u'}\frac{\partial \overline{u}}{\partial z}+\frac{g}{\overline{T}}\overline{w'T'}+\epsilon = 0\quad\text{steady}\\
\epsilon=-\overline{w'u'}\frac{\partial \overline{u}}{\partial z}+\frac{g}{\overline{\theta}}\overline{w'\theta'}\\
\varphi_\epsilon = \frac{k_0z\epsilon}{u_*^3} =\frac{k_0z}{u_*^3}u_*^2\frac{\partial \overline{u}}{\partial z}- \frac{k_0z}{u_*^3}\frac{g}{\overline{\theta}}\frac{H}{\overline{\rho} c_p}= \varphi_m(\zeta)-\zeta
$$
对于中性大气，$\varphi_m \rightarrow 1,\zeta \rightarrow 0$，则$\varphi_\epsilon\rightarrow 1$，所以
$$
\epsilon=\frac{u_*^3}{k_0z}=\frac{u_*^3}{k_0z}\frac{(k_0z)^3}{(k_0z)^3}=\frac{K_m^3}{(k_0z)^4}
$$
假设上述关系适用于非中性大气，则
$$
\varphi_\epsilon=\frac{k_0z\epsilon}{u_*^3}=\frac{k_0z}{u_*^3}\frac{K_m^3}{(k_0z)^4}=(\frac{K_m}{k_0u_*z})^3=\varphi_m^{-3}\\
\varphi_m^4-\zeta \varphi_m^3 -1 = 0\quad\text{Keyps Equation}
$$
对于稳定层结，$\frac{\partial \overline{u}}{\partial z}$较大，$\varphi_m>1$，则$\varphi_m=\zeta$，线性关系；正幂次稳定。
对于不稳定层结，$\frac{\partial \overline{u}}{\partial z}$较小，$\varphi_m<1$，则$\varphi_m=-\zeta^{-1/3}$，近似幂函数关系；负幂次不稳定。



## 六、特征函数求一、二、三阶原点矩和中心距，求概率密度

**特征函数**
定义：设$F(x)$是随机变量$\xi$的分布函数，则特征函数$\varphi(k)$定义为
$$
\varphi(k)=\int_{-\infty}^\infty e^{ikx}dF(x)=\int_{-\infty}^\infty e^{ikx}p(x)dx\\
p(x)=\frac{1}{2\pi}\int_{-\infty}^\infty e^{-ikx}\varphi(k)dk
$$

**原点矩$b_n=\overline{x^n}$**：按定义，有
$$
b_n=\int_{-\infty}^\infty x^n p(x)dx\\
\frac{d^n\varphi}{dk^n}=\int_{-\infty}^\infty \frac{d^n}{dk^n}e^{ikx}p(x)dx=\int_{-\infty}^\infty (ix)^np(x)e^{ikx}dx=(i)^n\int_{-\infty}^\infty x^n p(x)e^{ikx}dx\\
b_n=\int_{-\infty}^\infty x^n p(x)dx=\frac{1}{(i)^n}\frac{d^n\varphi}{dk^n}|_{k=0}
$$

**中心距$B_n=\overline{(x-\overline{x})^n}$**:按定义，有
$$
B_n=\int_{-\infty}^\infty (x-\overline{x})^n p(x)dx=\int_{-\infty}^\infty x^n p(x+\overline{x})dx
$$

所以概率分布为$p(x)$的随机变量的中心距等于相应阶数的概率分布为$p(x+\overline{x})$的原点矩。而$p(x+\overline{x})$对应的特征函数为
$$
\Phi(k)=\int_{-\infty}^\infty e^{ikx}p(x+\overline{x})dx=\int_{-\infty}^\infty e^{ik(x-\overline{x})}p(x)dx=\varphi(k)e^{-ik\overline{x}}\\
B_n=\frac{1}{(i)^n}\frac{d^n\Phi(k)}{dk^n}|_{k=0}=\frac{1}{(i)^n}\frac{d^n}{dk^n}\left[\varphi(k)e^{-ik\overline{x}}\right]|_{k=0}
$$

如果该分布对称，即$\overline{x}=0$，则$b_n=B_n$，即原点矩和中心距相等。
Example:
$$
\varphi(k) = \exp{\left(-\frac{1}{2}\sigma^2k^2\right)}
$$
求一阶、二阶、三阶原点矩和中心矩，并求出该随机分布的概率密度函数
$$
\begin{align*}
p(x) =& \frac{1}{2\pi}\int_{-\infty}^\infty e^{-ikx}\varphi(k)dk=\frac{1}{2\pi}\int_{-\infty}^\infty \exp{\left(-\frac{1}{2}\sigma^2k^2\right)}\left[\cos (kx)+i\sin(kx)\right]dk\\
=&\frac{1}{2\pi}\int_{-\infty}^\infty \exp{\left(-\frac{1}{2}\sigma^2k^2\right)}\cos (kx)dk=\frac{2}{2\pi}\int_0^\infty \exp{\left(-\frac{1}{2}\sigma^2k^2\right)}\cos (kx)dk\\
=&\frac{1}{\sqrt{2\pi}\sigma}\exp(-\frac{x^2}{2\sigma^2})
\end{align*}\\
b_1=B_1 = \frac{1}{i}\frac{d\varphi(k)}{dk}|_{k=0}=0\\
b_2=B_2 = \frac{1}{i^2}\frac{d^2\varphi(k)}{dk^2}|_{k=0}=\sigma^2\\
b_3=B_3 = \frac{1}{i^3}\frac{d^3\varphi(k)}{dk^3}|_{k=0}=0
$$






## 七、比较Fourier变换，Gabor变换和Wavelet变换

**Fourier变换**
$$
F(\omega)=\int_{-\infty}^{\infty}f(t)e^{-i\omega t}dt\\
f(t)=\frac{1}{2\pi}\int_{-\infty}^\infty F(\omega)e^{i\omega t}d\omega\\
=\frac{1}{2\pi}\int_{-\infty}^\infty F(\omega)(\cos \omega t+i\sin \omega t)d\omega
$$
傅里叶变换将信号作为一个整体进行分析，将信号从时间域变换到频率域分析。
意义：任何连续测量的时序信号$f(t)$，都可以表示为不同频率的正弦波$F(\omega)$的叠加；
优点：1.信号与不同尺度（频率）相结合；2.用整体信号全域分析，偏重全局特征
缺点：不能分辨出信号的局部特征，比如突变现象。在离散的傅里叶变换中有截断频率的问题$\omega_c = 2\omega$

**Gabor变换**
$$
G_f(\omega,\tau)=\int_{-\infty}^{\infty} f(t) g(t-\tau) e^{i\omega t} dt
$$
意义：将信号划分为很多小的时间间隔，对每个间隔进行Fourier变换；
优点：1.良好的时域局部化；2.$\tau$变化时可以看到不同的局部；
缺点：1.只是位置的平移，窗的形状不变；2.高频区希望窄窗提高分辨率；3.低频去希望宽窗，信息更完整；

**Wavelet变换**
$$
T_g(a,\tau)=\frac{1}{\sqrt{a}}\int_{-\infty}^{\infty}f(t)g(\frac{t-\tau}{a})dt
$$
其中$\tau$为平移因子，$a$为尺度因子,$\frac{1}{a}$为放大倍数。$g(t)$为小波母函数。相比傅里叶变换，小波$g(t)$是局部性很强的波，$a$影响小波形状，越小局部性越强。小波有对应的时间和频率域性质。但是由于窗口面积为不变量，时间域和频率域的分辨率不可能同时提高，通过改变$\tau$和$a$可以对任何时刻不同尺度的成分进行分析。
优点：1.在时域和频率域上，同时具有良好的局部性质，比如诊断突变点和精细结构；3.信号可分解为多尺度成分，并对各种不同尺度研究局部信号的微小细节；
缺点：存在边界问题，可以通过适当的方法消除边界效应。


## 八、大气扩散中Taylor横向扩散方差公式
$$
\begin{align*}
\sigma_y^2(T) =& 2\sigma_v^2\int_0^Tdt\int_0^tR_L(\tau)d\tau\\
= & 2\sigma_v^2\int_0^Tdtf(t) = 2\sigma_v^2\left[tf(t)|_0^T-\int_0^T df(t)dt\right]\\
=&2\sigma_v^2\left[T\int_0^T R_L(\tau)d\tau-\int_0^T R_L(t)dt\right]\\
=&2\sigma_v^2\int_0^T (T-t)R_L(t)dt
\end{align*}
$$

## 九、大气湍流和实验室湍流的区别
1. 地球旋转。
大气在自旋转的地球上运动，其运动（包括湍流）必须考虑科氏力的作用，表现在无因次方程中的Rossby数，即惯性力和科氏力之比，Rossby数越小，说明科氏力也重要。
$$
R_o = \frac{U^2/L}{fU} = \frac{U}{fL},\quad f=2\omega \sin \theta
$$
2. 大气分层。大气的平均状态，如温度、密度、压力、位温等都随高度变化，即大气是分层的。白天大气边界层处于极不稳定状态，湍流很强；夜间边界层处于稳定状态，湍流较弱。因此在大气中，经常用Richardson数表示层结对湍流强弱的影响。
3. 大Reynolds数。大气性质:$\nu=1.5\times10^{-5}m^2·s^{-1},U\sim10m·s^{-1}$，若$L=1m$，则$R_e\sim10^6$，而湍流的临界值大概是2000。物理上Reynolds数可以看成是湍流涡旋粘性系数$K$和分子粘性系数$\nu$的比值$R_e = \frac{UL}{\nu} = \frac{K}{\mu}$。大气的$R_e$很大，可以只考虑湍涡的粘性忽略分子粘性。
从物理上讲，Reynolds数可以看成是湍流涡旋黏性系数$K$和分子黏性系数$\nu$的比值，对$R_e$很大的湍流运动，一般可以只考虑湍涡黏性而忽略分子黏性。
4. 大气湍流分布在很宽的尺度上，从毫米到百米尺度的涡旋均有可能存在，能谱为连续宽带谱，带谱宽度大。
5. 边界层内湍流观测难度大。
