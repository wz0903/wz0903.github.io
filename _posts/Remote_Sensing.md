


# Part1 Radiation Theory
A technology that, from a certain distance away and without direct contact with the object being measured or the relevant physical phenomena, uses remote sensors to receive electromagnetic radiation emitted or reflected by the target, and then processes, classifies, identifies, and applies that information.

$$
F(x_1,x_2,\dots, x_n) = y_i,\quad i = 1,2,\dots,m
$$
From $m$ channels signal $y_i$ to get $n$ target variables $x_i$, there is no unique solution or analytical solution.

Radiative Transfer Equations
$$
\frac{dT_\lambda}{ds} = -Absorption + Emission + InScattering - OutScatterint
$$

![Radiation Transmitted by the Atmosphere](image.png)

**Air mass:** The ratio of the optical depth when light is incident at an angle $\theta$ to that when it is incident at the zenith, $m\approx \frac{1}{\cos\theta}$

$$
F_{\lambda,m} = F_{\lambda,0}\exp\left(-m\int_0^\infty \beta_{e,\lambda}dz\right) = F_{\lambda,0}\exp \left(-m\tau_{\lambda,0} \right)\\
\log F_{\lambda,m} = \log F_{\lambda, 0}-m\tau_{\lambda,0}
$$
to get $F_{\lambda,0}$

## 1.1 Basic radiation knowledge

### 1.1.1 Wave equations
frequency $f$ (Hz), wavelength $\lambda$ ($\mu$m, nm), wavenumber $\nu$ (cm^-1), wavespeed $c$ (m/s).
$\lambda f =c,\quad \nu = \frac{1}{\lambda} = \frac{f}{c}$

Maxwell equations:
$$
\left\{
\begin{aligned}
\nabla \cdot \mathbf{E} &= \frac{\rho}{\varepsilon_0} && \text{(Gauss's Law)} \\
\nabla \cdot \mathbf{B} &= 0 && \text{(Gauss's Law for Magnetism)} \\
\nabla \times \mathbf{E} &= -\frac{\partial \mathbf{B}}{\partial t} && \text{(Faraday's Law of Induction)} \\
\nabla \times \mathbf{B} &= \mu_0 \mathbf{J} + \mu_0 \varepsilon_0 \frac{\partial \mathbf{E}}{\partial t} && \text{(Ampere-Maxwell Law)}
\end{aligned}
\right.
$$
Therefore wave euqations
$$
\left\{
\begin{aligned}
\nabla^2 \mathbf{E} - \mu_0 \varepsilon_0 \frac{\partial^2 \mathbf{E}}{\partial t^2} &= 0 \\
\nabla^2 \mathbf{B} - \mu_0 \varepsilon_0 \frac{\partial^2 \mathbf{B}}{\partial t^2} &= 0
\end{aligned}
\right.
$$
If wave oscillates along the z-axis and propagates along the y-axis, there is
$$
E_z(y,t)\hat{z} = E_0\cos (ky-\frac{k}{\sqrt{\mu_0\epsilon_0}}t)\hat{z} = E_0\cos(ky-\omega t)\hat{z},k = constant
$$

### 1.1.2 Basic vatiables

Radiant Energy: $Q$ with unit J, radiation energy through a specific area.

Radiant Power/Flux: $\Phi$ with unit W, radiation energy through (emit/absorb) a specific area per unit of time. $\Phi = \frac{dQ}{dt}$

Radiant Power/Flux Density (irradiance, radiation intensity), $F$ with unit W/m^2, radiation energy through (emit/absorb) a unit area per unit of time. $F = \frac{d\Phi}{dA} = \frac{d^2Q}{dtdA}$

Radiance(radiant intensity), $I$ with unit W/m^2/sr, the radiant energy passing through a unit area, in a unit of time, and within a unit solid angle along the normal direction. $I = \frac{dF}{d\Omega} = \frac{d^3Q}{dtdAd\Omega}$

**Specific Intensity**
$$
I = I(\Omega) = \frac{d^3Q}{\cos\theta dtdAd\Omega} = \frac{d^3Q}{\bold{n}\cdot \bold{\Omega} dtdAd\Omega}
$$

**Radiance is the most common variables since it describe the dist. and transfer of a light comprehensively. Besides, radiance is conserved in free space.**

### 1.1.3 Radiation objects
Including point radiation source and surface radiation source (**Lambert source**).

#### 1.1.3.1 Parallel radiation
$$
I(\mu,\phi) = \frac{dF}{d\Omega} = F\delta (\Omega-\Omega_0) = F\delta(\mu-\mu_0)\delta(\phi-\phi_0)
$$

#### 1.1.3.2 Lambert Source
The radiance from a lamber source is unique in any direction. $I(\theta) = I_0$, therefore $F(\theta) = I(\theta)\cos\theta d\Omega= Id\Omega \cos\theta = F_0\cos\theta$

Irradiance of all direction on a half sphere is
$$
F_{total} = \int_\Omega F(\theta)d\Omega = \int_0^{2\pi}\int_0^{\pi/2}I_0\cos\theta \sin\theta d\theta d\phi=\pi I
$$

### 1.1.4 Interaction between radiation and objects
A beam of radiation strikes a object with a radiant flux density of $F$, the amounts of radiation absorbed, reflected, and transmitted by the medium are $F_a$, $F_r$, and $F_t$, respectively. According to the law of conservation of energy
$$
F = F_a+F_r+F_t
$$
Define absorption $a = \frac{F_a}{F}$, transmittance $t = \frac{F_t}{F}$, reflectance $r = \frac{F_r}{F}$, therefore $a+r+t = 1$.

**Kirchhoff's Law of Thermal Radiation**
The absorption equals to emittance under thermal equilibrium, i.e., $\varepsilon = a$, therefore $\varepsilon + t + r = 1$

**Blackbody**
An object is called a blackbody if it can absorb radiation with any wavelength without emitting any radiation.

Therefore, $\varepsilon = a = 1$, $t = r = 0$.

**Greybody**
Absorb a part of radiation but same $a$ for all wavelengths.


## 1.2 Radiation laws
**Kirchhoff's Law of Thermal Radiation**
The ratio of an object's irradiance $F$ to its absorption $a$ is a universal function $B(\lambda,T)$.

The absorption equals to emissivity under **thermal equilibrium**, i.e., $\varepsilon = a$, therefore $\varepsilon + t + r = 1$
**Stefan-Boltzmann law**
The total energy radiated per unit area by an absolutely blackbody surface in a unit of time $F = \int Fd\lambda$ is proportional to the fourth power of the blackbody's temperature.
$$
F = \epsilon \sigma T^4,\sigma = \frac{2\pi^5k_B^4}{15c^2h^3}
$$
**Wien’s Displacement Law**
The product of the wavelength $\lambda_m$ and temperature $T$ corresponding to the peak of the blackbody radiation spectrum is a constant.

**Planck's Law**
Radiance $I$ from a blackbody at a given temperature $T$ satisfies
$$
I_\nu(\nu,T) = \frac{2h\nu^3}{c^2}\left(\exp{\frac{h\nu}{k_BT}}- 1\right)^{-1}, B_\lambda(T) =\frac{2hc^2}{\lambda^5}\left(\exp{\frac{hc}{\lambda k_BT}}- 1\right)^{-1}
$$
Integrate over all direction (lambert source),
$$
F_B(\lambda,T) = \pi I = \frac{2\pi hc^2}{\lambda^5}\left(\exp{\frac{hc}{\lambda k_BT}}- 1\right)^{-1}
$$
Relationships:
$$
\frac{\partial B}{\partial \lambda} = 0\rightarrow \lambda_m T = constant\\
\int_0^\infty F_B(\lambda,T)d\lambda = \sigma T^4
$$

**Effective blackbody temperature (Brightness temperature)**
$$
T_b = B_\lambda^{-1}(T_b) = \frac{hc}{k_B\lambda \ln \left(\frac{2hc^2}{\lambda^5 I_\lambda} + 1\right)}
$$

**Polarization**

Brewster's angle: The reflection light is totally polarized if reflection angle is perpendicular to the refraction angle.

## 1.3 Absorption and emission of atmosphere

### 1.3.1 Absorption
When electromagnetic waves propagate through air, the air molecules interact with the waves, causing some of the energy from the electromagnetic field to be **transferred** to the molecules or atoms, which generally results in an **increase in temperature**.

**Local Thermodynamic Equilibrium**: the air molecules are in equilibrium in a local place. Under this assumption, the molecules follow Boltzmann distribution, and Kirchhoff's Law of Thermal Radiation establishes.

#### 1.3.1.1 Absorption of air molecules
$$
E = E_e+E_v+E_{\tau}
$$
Where $E_e$ is orbital energy, $E_v$ is vibration energy, and $E_{\tau}$ is rotation energy, all of them are quantized.
Every transition of energy level $\Delta E$ is corresponding to a frequency $f$. Therefore, the absorption/emission bands are fingerprints of molecules.

**Orbital transition**
For H atom, there is
$$
E_n = -\frac{me^4}{8\varepsilon^2h^2}\frac{1}{n^2} = -\frac{R_Hhc}{n^2}, n = 1,2,\dots
$$
The corresponding wavenumber of absorption or emission $\nu$ is 
$$
\nu = R_H\left(\frac{1}{j^2}-\frac{1}{k^2}\right)
$$
**Vibration transition**
$$
E_\nu = \left(k+\frac{1}{2}\right)h\nu', k = 1,2,\dots
$$
Where $\nu'$ is determined by molecules. Quantum mechanics requires the lawful transition is $\Delta k = \pm 1$. Therefore the corresponding frequency of vibration is $f = \nu'$ (Equal spacing)
**Rotation transition**
Angular Momentum $L$, angular velocity $\omega$,
moment of inertial $I$, rotational kinetic energy $E$so
$$
L = I\omega, E = \frac{1}{2}I\omega^2 = \frac{L^2}{2I}
$$
Quantum mechanics requires
$$
L = \frac{h}{2\pi} \sqrt{J(J+1)}, J = 1,2,\dots \\
E_J = \frac{L^2}{2I} = \frac{J(J+1)h^2}{8\pi^2I} \\
\Delta E_J = E_{J+1}-E_J = \frac{h^2}{4\pi^2I}(J+1), J = 1,2,\dots
$$
Corresponding frequency $f = \frac{\Delta E}{h} = \frac{h}{4\pi^2I}(J+1)$ (Equal spacing)

The corresponding wavelength of orbital transition is about $<1\mu m$ (visible or ultraviolet), vibration is about $1\sim 20\mu m$ (near infrared and thermal infrared), rotation is about $>20\mu m$ (far infrared and micarowave).

#### 1.3.1.2 Spectral broadening
**Natural Broadening**
Due to the quantum uncertainty of energy level, there is a inherent width.

**Doppler Broadening**
The thermal motion of molecules leads to doppler effects to broaden the spectral. This broadening **increases with rising temperature.**

**Collisional Broadening/Pressure Broadening**
Disturbance of energy levels happenes when molecule colliding with each other, changing the frequency of spectral. This broadening **increases with rising pressure.**

$$
k_\nu = Sf(\nu-\nu_0),\int_{-\infty}^{\infty} k_\nu d\nu = S,\int_{-\infty}^{\infty} f(\nu-\nu_0)d\nu = 1
$$
Where $\alpha$ is half width.
For pressure broadening, Lorentz
$$
f_L(\nu-\nu_0) = \frac{1}{\pi}\frac{\alpha_L}{(\nu-\nu_))^2+\alpha_L^2},\alpha_L = \alpha_0\frac{p}{p_0}\left(\frac{T_0}{T}\right)^n
$$
For doppler broadening,
$$
f_L(\nu-\nu_0) = \left(\frac{\ln2}{\pi}\right)^{1/2}\frac{1}{\alpha_D}\exp \left[-\left( \frac{\nu_-\nu_0}{\alpha_D}\right)^2\ln2 \right],\alpha_D = \frac{\nu_0}{c}\left(\frac{2k_BT}{m}\right)^{1/2}\sqrt{\ln2}
$$
Combined these two broadening, Vogit,
$$
\alpha_V = \frac{\alpha_L}{\alpha_D}\sqrt{\ln2}
$$
Below 30km, pressure broadening dominant, while doppler broaneding dominant above 30km.

### 1.3.2 Characteristic absorption spectrum in atmosphere
- H2O: 0.94 $\mu$m, 1.13 $\mu$m, 1.38 $\mu$m, 1.87 $\mu$m, 2.7 $\mu$m, 6.3 $\mu$m (strongest), >12 $\mu$m (strongest). Cloud with depth 100m is blackbody in long wave bands.
- OZONE/O2:
  - O2: 0.13-0.175 $\mu$m, 0.20-0.26 $\mu$m, 0.60 $\mu$m 0.76 $\mu$m;
  - OZONE: 0.2-0.3 $\mu$m, 0.30-0.36 $\mu$m, 4.7 $\mu$m, 9.6 $\mu$m, 14.1 $\mu$m, heating stratophere;
- CO2: 1.6 $\mu$m, 2.7 $\mu$m, 4.3 $\mu$m, 15 $\mu$m;
- CH4: 1.65 $\mu$m, 3.3 $\mu$m, 7.7 $\mu$m;
- N2O: 4.6 $\mu$m, 7.7 $\mu$m;

Summary: O2&OZONE absorb all radiation less than 0.29 $\mu$m, visible window 0.4-0.76 $\mu$m, then there are H2O, CO2, and CH4 in infrared region, another window at 8-12 $\mu$m, nearly blackbody over 14 $\mu$m.

The average of earth surface temperature is 288 K,corresponding to 10 $\mu$m, which is a window to emit radiation outside to maintain thermal equilibrium.

### 1.3.3 Equations
Absorption cross-section $\sigma_a$:
A physical quantity that describes the efficiency with which a molecule or atom absorbs radiation at a specific wavelength or energy (unit area).

Air absorption coefficient per volume (unit per m) and per mass (unit m^2/kg):
$$
\beta_a = \sum_{i=1}^{n}\sigma_{a,i}, k_a = \frac{\beta_a}{\rho} \\
(dI)_a = -\beta_a Ids = -\rho k_aIds
$$
**Beer/Bouguer-Lambert law**
$$
I(s_2) = I(s_1) \exp\left(-\int_{s_1}^{s_2}\rho k_a ds\right) = I(s_1) \exp(-\tau)
$$
transmittance $t = \exp (-\tau)$

### 1.3.4 Vertical dist. of absorption
Assume a thoroughly mixed composition A with mass mixing ratio $\omega$, therefore
$$
\rho_{air}(z) = \rho_0\exp(-\frac{z}{H})\\
\rho(z) = \omega \rho_0\exp(-\frac{z}{H})\\
\beta_{a,\lambda} = k_{a,\lambda}\rho(z) = k_{a,\lambda }\rho_0\omega\exp(-\frac{z}{H})\\
\tau_\lambda(z) = k_{a,\lambda}\omega \rho_0\int_z^\infty e^{-z'/H}dz' = k_{a,\lambda}\omega \rho_0He^{-z/H}
$$
For inner radiation, at height $z$ with depth $dz$, there is
$$
dF_\lambda = F_\lambda(z) \beta_{a,\lambda}(z)dz = F_{\lambda,\infty}\exp(-\tau(z))k_{a,\lambda }\rho_0\omega\exp(-\frac{z}{H})dz\\
\frac{dF_\lambda}{dz} = \frac{F_{\lambda,\infty}\exp(-\tau(z))\tau(z)}{H}
$$
Strongest absorption height
$$
\frac{d}{dz}\frac{dF_\lambda}{dz} = \frac{d}{dz} \frac{F_{\lambda,\infty}\exp(-\tau_\lambda(z))\tau_\lambda(z)}{H} = 0\rightarrow \tau_\lambda = 1
$$

At a height with small $\tau$, the air can NOT absorb enough radiation; at a height with high $\tau$, the radiation can be absorbed is less, indicating a balance at $\tau_\lambda = 1$


## 1.4 Scattering of atmosphere
Electromagnetic waves excite internal vibrations in the scatterer, causing it to emit secondary waves and change transmission direction.

If the frequency of scattered wave do NOT changes, this process is called elastic scattering (including Rayleigh and Mie scattering), this is called inelastic scattering conversely (including Brillouin, Raman, and Compton scattering).

### 1.4.1 Rayleigh Scattering
Treat an air molecule as a vibrating dipole. The inner radiation generates a uniform eletric fields $E_0$ and the dipole generates plane-polarized electromagnetic waves with scattering dipole moment $p_0 = \alpha E_0$, where $\alpha$ called polarizability is proportional to volume $r^3$. According to theoretical calculation, the **differential scattering cross section** is
$$
\beta(\theta,\varphi) = \frac{d\sigma_s}{d\Omega} = \frac{16\pi^4r^6}{\lambda^4}\left|\frac{m^2-1}{m^2+2}\right|^2(\cos ^2\theta\cos^2\varphi+\sin^2\varphi)
$$
and radiant flux density (irradiance) $F(\theta,\varphi) = \frac{F_0}{4\pi R^2}\sigma(\theta,\varphi)$, and radiance $I(\theta,\varphi) = \frac{dF}{d\Omega} = \frac{I_0}{4\pi R^2}\frac{d\sigma}{d\Omega}\propto r^6\frac{I_0}{R^2}(\frac{2\pi}{\lambda})^4(\cos^2\theta\cos^2\varphi+\sin^2\varphi)$ 
But for sunlight, which is not a plane-polarized waves but homogeneous at any direction $\varphi$, therefore need to average along $\varphi$, $\overline{\cos^2\varphi} = \overline{\sin^2\varphi} = \frac{1}{2}$. Therefore
$$
I(\theta) \propto r^6 \frac{I_0}{R^2}(\frac{2\pi}{\lambda})^4 \frac{1+\cos^2\theta}{2}
$$
**Scattering cross section** $\sigma_s = \int_{4\pi}\sigma(\theta,\varphi)d\Omega = \int_{4\pi}\beta(\theta,\varphi)d\Omega$

**Phase function**$P(\theta)$
$$
\begin{align*}
P(\theta) =& \frac{4\pi\sigma(\theta)}{\sigma_s} = \frac{4\pi}{\sigma_s}\int\frac{d\sigma_s}{d\Omega}d\varphi = \frac{4\pi\beta(\theta,\varphi)}{\int_{4\pi}\beta(\theta,\varphi)d\Omega}\\
=& \frac{2 (\cos^2\theta+1)}{\int_0^{\pi}(\cos^2\theta+1) \sin\theta d\theta}\\
=& \frac{3}{4}(1+\cos^2\theta)
\end{align*}
$$
$$
I = I_0\frac{\sigma_s}{R^2}\frac{P(\theta)}{4\pi},\sigma_s = \frac{128\alpha^2\pi^5}{3\lambda^4}\\
\alpha \approx \frac{V}{4\pi N} (m_r^2-1)
$$
Volume scattering coefficient 
$$
\beta_{\lambda,s}(m^{-1}) = n\sigma_s = \frac{8V\pi^3}{3N\lambda^4} (m_r^2-1)^2 = \frac{1.056e-6}{\lambda(\mu m)^4}
$$

**Asymmetry factor**$g$
$$
g = \frac{\int\sigma(\theta,\varphi)\cos\theta d\Omega}{\int\sigma(\theta,\varphi)d\Omega}
 = \frac{\int P(\theta,\varphi)\cos\theta d\Omega}{\int P(\theta,\varphi)d\Omega}$$

Polarization $P(\theta) = \frac{I_r(\theta)-I_l(\theta)}{I_r(\theta)+I_l(\theta)}$
for inner sunlight scattered by molecule,
$$
P(\theta) = \frac{\sin^2\theta}{1+\cos^2\theta}
$$

**Independent Scattering**
When the distance between scattered particles is greater than a few wavelengths, the scattering by each particle can be considered independent; that is, the total scattering effect is the sum of the scattering by each particle. Therefore

$$
\beta(\theta) = \sigma^m(\theta)N^m+\int_r \sigma^a(r,\theta)n(r)dr\\
k_s = \sigma_s^m(\theta)N^m+\int_r \sigma_s^a(r,\theta)n(r)dr\\
k_a = \sigma_a^m(\theta)N^m+\int_r \sigma_a^a(r,\theta)n(r)dr\\
k_e = \sigma_e^m(\theta)N^m+\int_r \sigma_e^a(r,\theta)n(r)dr\\
$$


### 1.4.3 Mie Scattering


## 1.5 Radiation Transfer Equations
Considering the temperature of Sun $5800$ K and Earth $288$ K, the strongest radiation is at 4 $\mu$m  and 10 $\mu$m respectively based on Wien's displacement law. The intensity of longwave from earth and shortwave from sun is balanced at 4 $\mu$m. The characteristics are below:

Radiation: Earth's radiation is a source of long-wave radiation and diffuse radiation (isotropic). Direct solar radiation is parallel radiation. In the long-wave band, direct solar radiation reaching the Earth's surface can be neglected.
Transport: Consider emission and absorption for longwave and neglect scattering (weak rayleigh). For shortwave consider scattering and emission but neglect emission.

A beam of monochromatic radiation passes through a layer of gaseous medium; the intensity of the radiation decreases over an infinitesimally small distance $ds$ along the direction of propagation is 
$$
dI = -\beta_{extinction} I ds + \beta_{absorption} B(T)ds+\beta_{inscatter} I_s ds
$$
To get the third term (scatter in), consider a incident irradiance from a random direction $\Omega'$ with solid angle $\Delta \Omega'$, there is
$$
F_{in} N \sigma_s = I(\Omega')\Delta\Omega' \cdot n\Delta A \Delta s\cdot \sigma_s = I(\Omega')\Delta\Omega' \cdot \Delta A \Delta s\cdot \beta_s
$$
The ratio scattered into direction $\Omega$ is $\frac{P(\Omega, \Omega')}{4\pi}$. As for per area medium and per solid angel at per distance, the radiance to $\Omega$ is $I(\Omega')\frac{P(\Omega,\omega')}{4\pi}\beta_s$, integrate over all inner direction $\Omega'$ there is all in-scatter radiance
$$
I_s = \frac{\beta_s}{4\pi}\int_{4\pi}I(\Omega')P(\Omega,\Omega')d\Omega'
$$
Therefore the radiation transfer equation is
$$
\frac{dI(\Omega)}{ds} = -\beta_e I(\Omega) + \beta_a B(T) + \frac{\beta_s}{4\pi}\int_{4\pi}I(\Omega')P(\Omega,\Omega')d\Omega'
$$
Since $d\tau = -\beta_e ds$ and single scattering albedo $\omega = \frac{\beta_s}{\beta_e}$, there is
$$
\frac{dI(\Omega)}{d\tau} = I(\Omega)-\left[(1-\omega)B(T)+\frac{\omega}{4\pi}\int_{4\pi}I(\Omega')P(\Omega,\Omega')d\Omega'\right]
$$
The first term in square brackets is thermal radiation source while the second term is scattering source. Let $\mu = \cos\theta$, there is **RTE**
$$
\boxed{
\mu\frac{dI(\mu,\varphi)}{d\tau} = I(\mu,\varphi)-\left[(1-\omega)B(T)+\frac{\omega}{4\pi}\int_0^{2\pi}\int_{-1}^1P(\mu,\varphi;\mu',\varphi')I(\mu',\varphi')d\mu'd\varphi'\right]
}
$$

### 1.5.1 Single scattering RTE (shortwave)
For sunlight radiation, neglect the emission radiation (thermal radiation source), therefore
$$
\mu\frac{dI(\mu,\varphi)}{d\tau} = I(\mu,\varphi)-\frac{\omega}{4\pi}\int_0^{2\pi}\int_{-1}^1P(\mu,\varphi;\mu',\varphi')I(\mu',\varphi')d\mu'd\varphi'
$$
And consider only once scattering from sunlight at angle $\Omega_0 = (\mu_0,\varphi_0)$ ($\mu_0<0$), that is $I(\mu',\varphi') = F_0\delta(\mu'-\mu_0)\delta(\varphi'-\varphi_0)e^{\tau/\mu_0}$
Downward $\mu<0$, $dz<0,ds>0$.
$$
\begin{align*}
\mu\frac{dI(\mu,\varphi)}{d\tau} =& I(\mu,\varphi)-\frac{\omega}{4\pi}\int_0^{2\pi}\int_{-1}^1P(\mu,\varphi;\mu',\varphi')F_0\delta(\mu'-\mu_0)\delta(\varphi'-\varphi_0)e^{\tau/\mu_0}d\mu'd\varphi' \\
=& I(\mu,\varphi)-\frac{\omega}{4\pi}P(\mu,\varphi;\mu_0,\varphi_0)F_0e^{\tau/\mu_0} \\
=& I(\mu,\varphi)-\frac{F_0\omega P(\cos\theta)e^{\tau/\mu_0}}{4\pi}(\text{Sunlight is non-polarized, only $\theta$ works})
\end{align*} 
$$
Integrate from $\tau_1$ to $\tau_2$
$$
I(\tau_2) = I(\tau_1)\exp\left(-\frac{\tau_1-\tau_2}{\mu}\right)+\frac{F_0\omega P(\cos\theta)}{4\pi\mu(-\frac{1}{\mu_0}+\frac{1}{\mu})}\left[e^{\tau_2/\mu}-e^{\left(\frac{\tau_1}{\mu_0}-\frac{\tau_1-\tau_2}{\mu}\right)}\right]
$$
For upward radiation $\mu>0$, $\tau_1=\tau_0$, $\tau_2=0$, there is
$$
I(0) = I(\tau_0)\exp\left(-\frac{\tau_0}{\mu}\right)+\frac{F_0\omega P(\cos\theta)}{4\pi\mu(-\frac{1}{\mu_0}+\frac{1}{\mu})}\left[1-e^{\left(\frac{\tau_0}{\mu_0}-\frac{\tau_0}{\mu}\right)}\right]
$$
If neglecting direct radiation $I(\tau_0)\exp\left(-\frac{\tau_0}{\mu}\right)$ ($\tau_0\gg 1$) there is the fundamentals of satellite-derived optical depth
$$
\boxed{
I(0) = \frac{F_0\omega \tau_0 P(\cos\theta)}{4\pi\mu}
}
$$

### 1.5.2 Multiple scattering RTE (shortwave)

**Two-stream approximation**
Neglecting emission stil, there is
$$
\begin{align*}
\mu\frac{dI(\mu,\varphi)}{d\tau} =& I(\mu,\varphi)-\frac{\omega}{4\pi}\int_0^{2\pi}\int_{-1}^1P(\mu,\varphi;\mu',\varphi')I(\mu',\varphi')d\mu'd\varphi' \\ 
= &I(\mu)-\frac{\omega}{4\pi}\int_0^{2\pi}\int_{-1}^1I(\mu')d\mu'd\varphi' \quad \text{(assume diffuse scattering)}\\
= & I(\mu)-\frac{\omega}{2}\left[\int_{0}^1I(\mu')d\mu'+ \int_{-1}^0I(\mu')d\mu'\right] = I- \frac{\omega}{2} (I^\uparrow+I^\downarrow)
\end{align*}
$$
Therefore
$$
\left\{
\begin{aligned}
\int_0^1\mu\frac{dI^\uparrow}{d\tau}d\mu = \int_0^1\left[I^\uparrow - \frac{\omega}{2}(I^\uparrow+I^\downarrow)\right]d\mu \\
\int_{-1}^0\mu\frac{dI^\downarrow}{d\tau}d\mu = \int_{-1}^0\left[I^\downarrow - \frac{\omega}{2}(I^\uparrow+I^\downarrow)\right]d\mu
\end{aligned}
\right.\rightarrow
\left\{
\begin{aligned}
\frac{1}{2}\frac{dI^\uparrow}{d\tau} = (1-\omega)I^\uparrow + \frac{\omega}{2}(I^\uparrow-I^\downarrow) \\
\frac{1}{2}\frac{dI^\downarrow}{d\tau} = (1-\omega)I^\downarrow - \frac{\omega}{2}(I^\uparrow-I^\downarrow) 
\end{aligned}
\right.
$$
$$
\left\{
\begin{aligned}
\frac{1}{2}\frac{d}{d\tau}(I^\uparrow+I^\downarrow) =&\omega(I^\uparrow-I^\downarrow)   \\
\frac{1}{2}\frac{d}{d\tau}(I^\uparrow-I^\downarrow) =&(1-\omega)(I^\uparrow+I^\downarrow) 
\end{aligned}
\right. \rightarrow
\left\{
\begin{aligned}
\frac{d^2}{d\tau^2}(I^\uparrow+I^\downarrow) =&4\omega(1-\omega)(I^\uparrow+I^\downarrow)   \\
\frac{d^2}{d\tau^2}(I^\uparrow-I^\downarrow) =&4\omega(1-\omega)(I^\uparrow-I^\downarrow)  
\end{aligned}
\right.
$$

### 1.5.3 Thermal infrared RTE at atmosphere (longwave)
For earth surface thermal equilibrium, there is 
$$
S\pi R_e^2 (1-r) = \sigma T_e^44\pi R_e^2, T_e = [\frac{S(1-r)}{4\sigma}]^{1/4} = 255 K
$$
$$
T_s = T_e+\gamma H = 255+6.5\times5 = 288K
$$
RTE
$$
dI = -\beta_{extinction} I ds + \beta_{absorption} B(T)ds+\beta_{inscatter} I_s ds
$$

If there is no aerosols/clouds, the longwave scattering can be neglected. Therefore $\beta_s =0$, $\beta_e = \beta_a$.
For local thermal equilibrium (therefore $I = B(T)$), isotropic (no $\mu$ or $\varphi$), monochromatic long-wavelength radiation (no frequency shift), only emission and absorption, there is **Schwarzschild's equation**
$$
\frac{dI}{ds} = \beta_a(B-I)\rightarrow \frac{dI}{d\tau} = I-B(T)\\
I = I(\tau_0)e^{-\tau_0}+\int_0^{\tau_0}Be^{-\tau}d\tau
$$
Let transmittance $t = e^{-\tau}$, $I = I(\tau_0)t_0+\int_0^1Bdt$, $\mu =\cos\theta$,
$$
\left\{
\begin{aligned}
I^\uparrow (0) =& I^\uparrow(\tau_0)e^{-\tau_0/\mu}+\int_0^{\tau_0}Be^{-\tau/\mu}\frac{d\tau}{\mu}\quad\text{(upward)}\\
I^\downarrow (\tau_0) =& I^\downarrow(0)e^{\tau_0/\mu}+\int_0^{\tau_0}Be^{(\tau_0-\tau)/\mu}\frac{d\tau}{\mu}\quad\text{(downward)}
\end{aligned}
\right.
$$
If **vertical** ($\mu=\pm1$)
$$
\left\{
\begin{aligned}
I^\uparrow (0) =& I^\uparrow(\tau_0)t_0+\int_{t_0}^{1}Bdt \quad\text{(upward)}\\
I^\downarrow (\tau_0) =& I^\downarrow(0)t_0+\int_{t_0}^{1}B\frac{t_0}{t^2}dt\quad\text{(downward)}
\end{aligned}
\right.
$$
Consider reflectance and emission of surface ground to connect $I^\uparrow(\tau_0)$ and $I^\downarrow(\tau_0)$, assume the emission is $\varepsilon$, therefore the reflectance is $r = 1-\varepsilon$.
$$
I^\uparrow(\tau_0) = \varepsilon B(T_s) + (1-\varepsilon) I^\downarrow(\tau_0)\text{(surface)},\quad I^\downarrow(0)\approx 0\text{(lonewave)}
$$
Combine and get
$$
\begin{aligned}
I^\uparrow (0) =& I^\uparrow(\tau_0)t_0+\int_{t_0}^{1}Bdt\\
=& \left[\varepsilon B(T_s) + (1-\varepsilon) I^\downarrow(\tau_0)\right]t_0+\int_{t_0}^{1}Bdt\\
=& \left[\varepsilon B(T_s) + (1-\varepsilon) \left(I^\downarrow(0)t_0+\int_{t_0}^{1}B\frac{t_0}{t^2}dt\right)\right]t_0+\int_{t_0}^{1}Bdt\\
\end{aligned}\\
\boxed{
I^\uparrow (0) = \varepsilon t_0B(T_s) + \int_{t_0}^{1}Bdt + (1-\varepsilon)t_0^2 \int_{t_0}^{1}Bt^{-2}dt
}
$$
The first term is emission from ground surface, the second term is emission from each layer air upward, the third term is emission from each layer air downward to the ground surface and reflected by ground surface and upward again to raach the air top.

For transparent air ($t_0 = t=1$): $ I^\uparrow (0) = \varepsilon B(T_s)$;
For opaque air ($t_0 = 0$): $ I^\uparrow (0) = \int_{t_0}^{1}Bdt$;
For blackbody surface ($\varepsilon = 1$, $r=0$): $I^\uparrow (0) =B(T_s)t_0 + \int_{t_0}^{1}Bdt$

If consider any direction $\mu\ne \pm1$,

$$
\left\{
\begin{aligned}
I^\uparrow (0) =& I^\uparrow(\tau_0)t_0^{1/\mu}+\int_{t_0}^{1}Bt^{1/\mu-1}\frac{dt}{\mu}\quad\text{(upward)}\\
I^\downarrow (\tau_0) =& I^\downarrow(0)t_0^{1/\mu}+\int_{t_0}^{1}B(\frac{t_0}{t})^{1/\mu}\frac{dt}{t\mu}\quad\text{(downward)}
\end{aligned}
\right.
$$
$$
I^\uparrow(\tau_0) = \varepsilon B(T_s) + (1-\varepsilon) I^\downarrow(\tau_0)\text{(surface)},\quad I^\downarrow(0)\approx B(T_c)\text{(cosmic microwave)}
$$
Therefore,
$$
\begin{aligned}
I^\uparrow (0) =& \left[\varepsilon B(T_s) + (1-\varepsilon) [I^\downarrow(0)t_0^{1/\mu}+\int_{t_0}^{1}B(\frac{t_0}{t})^{1/\mu}\frac{dt}{t\mu}]\right]t_0^{1/\mu}+\int_{t_0}^{1}Bt^{1/\mu-1}\frac{dt}{\mu}\\
=& \varepsilon B(T_s)t_0^{1/\mu}+ (1-\varepsilon)\left[B(T_c)t_0^{1/\mu}+\int_{t_0}^{1}B(\frac{t_0}{t})^{1/\mu}\frac{dt}{t\mu}\right]t_0^{1/\mu}+\int_{t_0}^{1}Bt^{1/\mu-1}\frac{dt}{\mu}\\
=& \varepsilon B(T_s)t_0^{1/\mu}+ (1-\varepsilon)B(T_c)t_0^{2/\mu}+ (1-\varepsilon)\int_{t_0}^{1}Bt_0^{1/\mu}(\frac{t_0}{t})^{1/\mu}\frac{dt}{t\mu}+\int_{t_0}^{1}Bt^{1/\mu-1}\frac{dt}{\mu}
\end{aligned}\\
\boxed{
I^\uparrow (0) = \varepsilon B(T_s)t_0^{1/\mu}+ (1-\varepsilon)B(T_c)t_0^{2/\mu}+ (1-\varepsilon)\int_{t_0}^{1}Bt_0^{1/\mu}(\frac{t_0}{t})^{1/\mu}\frac{dt}{t\mu}+\int_{t_0}^{1}Bt^{1/\mu-1}\frac{dt}{\mu}
}
$$
The first term is emission from ground surface; the second term is cosmic microwave downward, reflected by ground surface, and upward finally; the third term is emission from each layer air downward, rereflected by ground surface, and upward finally; the last term is emission from each layer air upward.

Notice that $\frac{dt}{\mu} = t^{1-1/\mu}dt^{1/\mu}$, therfore
$$
\begin{align*}
I^\uparrow (0) =& \varepsilon B(T_s)t_0^{1/\mu}+ (1-\varepsilon)B(T_c)t_0^{2/\mu}+ \int_{t_0}^{1}B\left[(1-\varepsilon)t_0^{2/\mu}t^{-1/\mu-1}+t^{1/\mu-1}\right]t^{1-1/\mu}dt^{1/\mu}\\
=&\varepsilon B(T_s)t_0^{1/\mu}+ (1-\varepsilon)B(T_c)t_0^{2/\mu}+ \int_{t_0}^{1}B\left[(1-\varepsilon)(\frac{t_0}{t})^{2/\mu}+1\right]dt^{1/\mu}\\
=& \varepsilon B(T_s)t_0^{1/\mu}+ (1-\varepsilon)B(T_c)t_0^{2/\mu}+ \int_{p_s}^{0}BK(p,\mu)d\ln p \\
\end{align*}
$$
where $K(p,\mu)$ is weight function:
$$
K(p,\mu) = \left[1+(1-\varepsilon)(\frac{t_0}{t})^{2/\mu}\right]\frac{dt^{1/\mu}}{d\ln p}
$$
# Part2 Satellite Introduction
## 2.1 Satellite orbit
### 2.1.1 Newton law and circular orbit
$$
\frac{mv^2}{r} = \frac{GM_em}{r^2},\rightarrow T^2 = \frac{4\pi^2}{GM_e}r^3
$$
Geostationary satellite: $h=36000$ km;
Polar satellite: $T=105$ min with $h=850$ km;

Sidereal day: 1 day = 23h56min, 360 deg per day:
Solar day: 1 day = 24h, 360.986 deg per day.
### 2.1.2 Kepler orbit
$$
\ddot{r}-r\dot{\theta}^2 = -\frac{GM_e}{r^2}
$$
Let $u=\frac{1}{r}$, angular momentum per mass $h = r^2\dot{\theta} = const$, Binet Transformation
$$
\frac{d\theta}{dt} = \frac{h}{r^2} = hu^2,\quad \rightarrow \frac{d}{dt} = hu^2\frac{d}{d\theta}\\
\frac{dr}{dt} = \frac{h}{r^2}\frac{dr}{d\theta} = -h\frac{du}{d\theta},\frac{d^2r}{dt^2} = -\frac{d}{dt}h\frac{du}{d\theta} = -h^2u^2\frac{d^2u}{d\theta^2}
$$
Therefore
$$
\ddot{r}-r\dot{\theta}^2 = -h^2u^2\frac{d^2u}{d\theta^2}-h^2u^3 = -GM_eu^2\\
\frac{d^2u}{d\theta^2}+u = \frac{GM_e}{h^2}\\
u = \frac{GM_e}{h^2}+C\cos(\theta-\theta_0),\quad C=\frac{GM_e}{h^2}\sqrt{1+\frac{2Eh^2}{G^2M_e^2}}
$$
therefore
$$
r = \frac{p}{1+e\cos\theta},p=\frac{h^2}{GM_e} = \frac{b^2}{a},e = \sqrt{1+\frac{2Eh^2}{G^2M_e^2}} = \frac{c}{a}
$$

**Kepler orbit in space**
$(r,\Omega,\delta)$

### 2.1.3 Orbital perturbation
Due to some forces much smaller than Earth’s gravity, a satellite’s movement in orbit deviates from its intended path are called perturbations.
- **Non-spherical gravity**: Non-spherical Uniform Earth
- Other olanet gravity: moon,sun
- Radiation pressure: solar radiation
- Particle flux: Solar wind
- Air resistance: Residual atmosphere in space
- Tidal forces: Sea Tides
- Electromagnetic force: The Interaction Between Satellite Currents and the Earth's Magnetic Field


### 2.1.4 Actual satellite orbit

#### 2.1.4.1 Sunsynchronous orbits

#### 2.1.4.2 Geosynchronous orbits

#### 2.1.4.3 Asynchronous orbits

## 2.2 Characteristics of instrument
**Fraunhofer Diffraction** and Airy disk
$$
\sin\theta_c = 0.61\frac{\lambda}{r} = 1.22\frac{\lambda}{D}
$$
Increase size or reduce wavelength to increase the resolution.

### 2.2.1 Channel selection

#### 2.2.1.1 Imager
Within the **window bands (wavelength ranges where atmospheric transmittance is high)** to minimize the atmospheric medium’s impact on the target’s radiation, thereby providing a clearer view of targets on Earth and their changes.
- visible: 0.39-0.76 $\mu$m;
- shortwave infrared: 0.76-1.15 $\mu$m, 1.23-1.30 $\mu$m, 1.55-1.75 $\mu$m, 2.10-2.35 $\mu$m;
- thermal infrared: 3.5-4.1 $\mu$m;
- longwave infrared: 8-14 $\mu$m;
- microwave 0-20 GHz, 25-50 GHz, 70-110 GHz, 120-170 GHz:
  - Long bands: 1-2 GHz (15-30 cm);
  - Short bands: 2-4 GHz (7.5-15 cm);
  - Compromise bands: 4-8 GHz (3.75-7.5 cm);
  - X bands: 8-12.5 GHz(2.42-3.75 cm);
  - K-under bands: 12.5-18 GHz (1.67-2.42 cm);
  - K bands: 18-26.5 GHz (1.13-1.67 cm);
  - K-above bands: 26.5-40 GHz(0.75-1.13 cm);
  - W bands: 70-110 GHz(2.73-4.00 mm);

Specific spectral regions that make it easy to distinguish targets (e.g., differences in reflectance).
- AVIRIS: 0.4-2.5 $\mu$m with 200 channels;
- MODIS: 36 of AVIRIS;
- FY-3A/MERSI: like MODIS but 20 channels including 11.25 $\mu$m;
#### 2.2.1.2 Detector
**Selecting wavelengths that reflect the maximum radiation from targets in different atmospheric layers, the radiation signal from the targets is maximized, making it easier to determine the vertical distribution of the physical properties of different atmospheric layers or the vertical distribution of the targets' characteristics.**
- Temperature: CO2 with 4.3 $\mu$m, 15 $\mu$m; O2 with 50-60 GHz, 118 GHz;
- Humidity(H2O): 6.3 $\mu$m, 183.31 GHz;

### 2.2.2 Scanning imaging technology

- Cross-track or whishbroom scanner: AVHRR; hybrid cross-track scanner: MODIS;
- Circular scanning
- Along-track or pushbroom scanner: LADNSAT8;
- Frame imager

## 2.3 Data preprocess

### 2.3.1 Radiametric calubration
limb darkening effect
solar zenith angle rectification

# Part3 Clouds
Cooling effects: Warm low level clouds with a high albedo. Compared with no clouds, emit almost same longwave radiation (same temperature), but reflect more shortwave radaition, therefore cooling the earth.
Warming effects: Cold upper level clouds with a low albedo. Compared with no clouds, emit much less longwave radiation (much lower temperature but still blackbody with respect to longwave), hardly reflect shortwave radaition, therefore warming the earth.

Clouds category:
High clouds: cirrus (Ci), cirrocumulus (Cc), cirrostratus (Cs);
Middle clouds: altostratus (As), altocumulus (Ac), nimbostratus (Ns);
Low clouds: stratus (St), stratocumulus (Sc), cumulus (Cu), cumulonimbus (Cb);

## 3.1 Cloud atlas
### 3.1.1 Visible (reflectance)
High reflectivity therefore high radiation and bright atlas.
High resolution (short wavelength), easy to distinguish clouds, ground, and sea, but only for daytime.
Problems:
- Hard to distinguish clouds and snow.
- Small clouds will be smoothed into uniform brightness.
- Thin clouds will be affected by ground.

### 3.1.2 Shortwave infrared (3.75 $\mu$m, reflectance)
High reflectivity therefore high radiation and bright atlas.
Reflect sunlight and emit infrared radiation daytime but emit only at night (similar to longwave infrared).

Small size water clouds reflect more, making atlas darker.
Water clouds reflects more than ice clouds with same particle size.
Ocean clouds have larger particles, reflecting less.

For infrared bands, most clouds have a emission ratio 0.75, i.e., $I_\lambda =0.75B_\lambda(T_b)<B_\lambda(T_b)$. Therefore the effective blackbody temperature $T_b = \frac{hc}{k_B\lambda\ln (\frac{2hc^2}{\lambda^5I_\lambda}+1)}$ is lower than its true temperature $T_s$.

### 3.1.3 Vapor (6.7 $\mu$m, absorption)
Radiation from ground can NOT reach satellite since all of them are absorbed by vapor.
Radiation from lower level has higherr temperature, therefore is darker. Can NOT recognize different cloud categories, can not see low clouds.
Give information about large scale humidty.


### 3.1.4 Longwave infrared (10.7 $\mu$m, emission)
Emit radiation, clouds is higher than the ground with lower temperture, therefore low radiation and bright atlas (inverse of radiation to atlas).

Can see the ground, lower resolution due to wavelength.
Problems:
- Frogs and low clouds have less temperature difference to recognize at night;
- Thin clouds are warmer from radiation (low resolution therefore radiation is added by surface ground), therfore the cloud top height is lower than reality;
- Small absorption from CO2. H2O, therefore the radiation is smaller than reality.

## 3.2 Clou top height/fraction

### 3.2.1 Infrared Window Area (11 $\mu$m)
Only for blackbody clouds, $p$, $T$;
No other interference; some absorption; detect daytime and night; only for opaque clouds with higher heights.
**Principle:**
- Assume absorption above the cloud is very small, therefore the Temperature inversed by radiation is cloud top temperature as a blackbody. According to the temperature profile from numerical weather prediction to get the cloud top height. (bias: 100 hPa or higher)
- New: according to the temperature profile from radiation transfer model to get the cloud top height, and get new cloud top temperature from temperature profile of sounding or numerical weather prediction.

### 3.2.2 Residual Radiation Method (15 $\mu m$ and 53.74 GHz)
$p$, $T$, $N'$
$$
I(\lambda) = (1-N)I_{clr}(\lambda) + N\epsilon I_{cld} (\lambda) + (1-\epsilon)NI_{clr}(\lambda)
$$
The first term is clear sky radiation, second term is cloud radiation, third term is clear sky radiation penetrating clouds.
Def effective cloud fraction $N' = N\varepsilon$, observation $\tilde{I}$
$$
N' = \frac{I-I_{clr}}{I_{cld}-I_{clr}} = \frac{\tilde{I}-I_{clr}}{I_{cld}-I_{clr}}
$$
Adjacent fields of view with subscript 1 and 2 respectively.
$$
\tilde{I_i}(\lambda) = (1-N_i')I_{clr}(\lambda) + N_i' I_{cld} (\lambda),\quad i=1,2\\
I_{clr}(\lambda) = \frac{\tilde{I_1}(\lambda)-N^*\tilde{I_2}(\lambda)}{1-N^*},\quad N^*=\frac{N_1'}{N_2'} = \frac{\tilde{I_1}(\lambda)-I_{clr}(\lambda)}{\tilde{I_2}(\lambda)-I_{clr}(\lambda)}
$$
If $N^*$ is known, then $I_{clr}$ can be solved, so for $I_{cld}$.

**Estimation of $N^*$**
Microwave bands are hardly affected by non-precipitation clouds, therefore it equals to clear sky.
$$
I(\lambda_{MSU2}) = a_0+\sum_i a_iI(\lambda_i)\\
N^* = \frac{I_1(\lambda_{MSU2})-\tilde{I}_(\lambda_{MSU2})}{I_2(\lambda_{MSU2})-\tilde{I}(\lambda_{MSU2})}
$$
Get $N^*$ from microwave, therefore get $I_{clr}$, $I_{cld}$, and $N'$ in each field.

How to determine the cloud top height?
With known the clear sky radiation, temperature profiles.
Select a cloud top pressure $p_c$, calculate $I_{cld}$ from radiation transfer equation:
$$
I_{cld} = B_\lambda(T_c)t(p_c,0)+\int_0^{p_c}B_\lambda(T)\frac{\partial t_\lambda(p,0)}{\partial \ln p}d\ln p
$$
get a theoretical radiation $I_{cld}$. Then calculater effective cloud fraction $N' = \frac{\tilde{I}-I_{clr}}{I_{cld}-I_{clr}}$
Calculate radiation in other bands
$$
I_{cld,i} = B_{\lambda_i}(T_c)t(p_c,0)+\int_0^{p_c}B_{\lambda_i}(T)\frac{\partial t_{\lambda_i}(p,0)}{\partial \ln p}d\ln p\\
I(\lambda_i) = (1-N_i')I_{clr}(\lambda_i) + N_i' I_{cld,i} (\lambda_i)
$$
calculate residual 
$$
\chi(p_c) =\left\{ \sum_i \left[\frac{I(\lambda_i)-\tilde{I}(\lambda_i)}{\tilde{I}(\lambda_i)}\right]^2\right\} ^{1/2}
$$
$p_c = \min \chi(p_c)$ to get cloud top pressure/temperature.

Bias:
- $\varepsilon$ is assumed same in each channel, therefore more channels have less bias;
- has bias less than 25 hPa only above 600 hPa;

### 3.2.3 Radiation ratio levels
CO Slicing method, two channels at least 1 CO2 channel, $p$, $T$, $N'$,

### 3.2.4 H2O-Infrared Window Intersection Method
two channels, $p$, $T$;

### 3.2.5 Split window methods
two channels, $p$, $T$, only for blackbody clouds.

## 3.3 Cloud base
water clouds:
- satellite remote sensing: $Z_{cb} = Z_{ct}-\Delta Z = Z_{ct}-\frac{LWP}{LWC}$, $LWP\approx \frac{2\tau_c r_e}{3}$
- $T$, RH profiles:
  - $T-T_d>T_{th}$ is cloud
  - RH threshold
  - $\frac{\partial^2 T}{\partial z^2}$ and $\frac{\partial^2 RH}{\partial z^2}$
ice clouds:
- satellite remote sensing: $Z_{cb} = Z_{ct}-\Delta Z = Z_{ct}-\frac{LWP}{LWC}$, $IWP = \frac{\tau_c}{a+b/D_e}$, $\ln IWC = -7.6+e\exp \left[-0.2443e-3(|T|-20)^{2.455}\right]$, $D_e = 2r_e = c_0+c_1T+c_2T^2+c_3T^3$;


## 3.4 Cloud phase
complex refletivity:
$$
m =n+i\kappa, k =m\frac{\omega}{c} = (n+i\kappa)\frac{\omega}{c}\\
E(z,t) = E_0 \exp\left[-i(\omega t-kz)\right] = E_0\exp\left[-i(\omega t-\frac{n\omega}{c}z)\right]\exp\left(-\kappa\frac{\omega}{c}z)\right)\\
I(z) \propto E^2 \rightarrow I(z) = I_0 \exp(-2\kappa\frac{\omega}{c}z) = I_0 \exp(-4\frac{\pi\kappa}{\lambda}z) = I_0\exp(-\beta_a z)
$$

where $n$ indicating refraction and $\kappa$ indicating attenuation (absorption).

### 3.4.1 Visble-NearInfrared method (0.65 $\mu$m, $1.63\mu$m)
**At 0.65 $\mu$m, both ice and water has hugh reflectivity compared with absorption (and ice reflect less than water), indicating strong reflection on cloud atlas to recognize clouds. Besides, at 1.63 $\mu$m, ice absorb more and reflect less than water, indicating less radiation on cloud atlas than water.**

# Part4 Wind
## 4.1 Imager Wind measurement
Select trace target;
Track trace target;
Ensure height;
Calculater wind field.

## 4.2 Microwave Wind measurement
- Microwave has strong penetration capability, therefore it is not affected by clouds, observations can be made **around the clock.**
- The microwave spectra of certain land features vary greatly, easy to recognize (water and ice are 0.4 and 0.99 respectively, while 0.96 and 0.92 in infrared region).
- Ability to penetrate ice, snow, forests, soil, and other materials. The penetration ability of microwaves through objects is inversely proportional to the objects' dielectric constant and directly proportional to the wavelength.
- Ocean remote sensing, monitoring sea surface winds and waves as well as ocean circulation.
- Low resolution but obvious characteristics

5-37 GHz, high transmittance

### 4.2.1  Active scatterometer
An active microwave sensor, known as a scatterometer, transmits microwave pulses toward the ocean surface and then detects the backscattered energy from small-scale waves, thereby determining the wind vectors at the ocean surface.

Advantages:
- observe clouds-rain system vertically
- Less affected by the underlying surface
- high spatial resolution
- High measurement accuracy

5-15 GHz
**Principle:**
Let the received echo pulse power be $P_r$; then the backscattering coefficient $\sigma$ (scattering cross section per unit area) is
$$
P_r = P_t\frac{\sigma_s}{4\pi R^2}\frac{A_e}{4\pi  R^2}G,\quad G = \frac{4\pi A_e}{\lambda^2}\\
\sigma = \frac{\sigma_s}{A_e} = \frac{P_r}{P_t}\frac{(4\pi)^3R^4}{G^2\lambda^2A_e}
$$

Empirical formula

$$
\sigma = A \cdot v^\gamma = f(v,\theta,\phi,\cdots) \approx Av^\gamma(1+a\cos\phi+b\cos2\phi)
$$

Usually $a$ is small compared with $b$, therefore the period is $\pi$ with some perturbation.
Theoretically, from four different $(\sigma(\phi),\phi)$ can get $A, \gamma, a, b$, therefore can get $v$ from $\sigma$.
But actually, if neglecting $a\cos\phi$ term, and observe a field twice with $\Delta \phi = \pi/2$, there is
$$
\sigma_1 = Av^\gamma (1+b\cos2\phi),\sigma_2 = Av^\gamma (1+b\cos2(\phi+\pi/2))) = Av^\gamma (1-b\cos2\phi)\\
\sigma_1+\sigma2 = 2Av^\gamma,\frac{\sigma_1-\sigma_2}{\sigma_1+\sigma_2} = b\cos2\phi
$$

Possible solutions are $\phi = \phi_0,-\phi_0,\pi+\phi_0,\pi-\phi_0$. Add third measurement $\phi+\pi/4$, minimize the sum of residual square$\chi^2 = \sum_{i=1}^3\left[\frac{\tilde{\sigma_i}-\sigma_i}{\tilde{\sigma_i}\varepsilon_i} \right]^2$, there are two possible solutions $\phi_0, \pi+\phi_0$ or $-\phi_0,\pi-\phi_0$. Based on numerical prediction to determine the final resolution.



### 4.2.2 Passive radiometer
Advantages:
- large observation region
- low cost, multi satellite observation
- long lifetime
- better penetration than infrared

Principle:


## 4.3 Tropical cyclone
A cyclonic system is a non-frontal vortex that forms over tropical or subtropical oceans, characterized by organized convection and a well-defined cyclonic circulation.

A typhoon is a rapidly rotating atmospheric vortex that rotates counterclockwise in the Northern Hemisphere and clockwise in the Southern Hemisphere; it is a warm-core, non-frontal low-pressure system on a large scale.

Tropical Depression, Tropical Storm, Severe Tropical Storm, Typhoon, Severe Typhoon, and Super Typhoon.

The waters of the northwestern Pacific and the South China Sea are the most typhoon-prone regions in the world
### 4.3.1 Basic characteristics
The core of a mature typhoon has a quasi-symmetrical circular structure, while its outer regions typically exhibit distinct asymmetrical features. In the lower troposphere, the typhoon’s cyclonic circulation can extend to areas more than 1,000 kilometers from the center.
- Basic
Typhoons generally extend vertically to the top of the troposphere (15–20 kilometers), though some may extend into the lower stratosphere; the ratio of their vertical scale to their horizontal scale is approximately 1:50.
- Horizontal
Moving outward from the center of the typhoon are, in order, the eye, the eyewall, and the spiral rain bands. The eye of a typhoon is generally 10–70 kilometers wide. The most intense convection and precipitation occur in the eyewall region, which is on average 8–19 kilometers wide and generally coincides with the area of maximum surface wind speeds. On satellite imagery, a thick layer of intense convection can be seen forming a dense area of cirrostratus clouds. The area extending from the outer edge of the eyewall to the storm’s periphery constitutes the outer region of the typhoon.
- Temperature
The warm core structure is the most distinctive feature of a typhoon. Depending on the typhoon’s intensity and extent, the temperature anomaly ranges from a few degrees Celsius to 20°C. On either side of the warm core, from the outer edge of the eye region outward to the outer edge of the eye wall, there is a strong radial temperature gradient. The maximum temperature anomaly occurs at 200 hPa, while the minimum is found near 760 hPa. The stronger the typhoon, the greater the temperature anomaly in the warm core, and the higher the altitude at which it occurs.

## 4.4 Dvorak Techniques
Based on infrared and visible cloud atlas to estimate the strength of typhoon.

**Theoretical fundamentals:**
Dvorak tech includes environmental dynamics and thermal factors.
- Dynamics:
  - The curvature of the cloud band reflects the magnitude of cyclonic vorticity. 
  - The distance of deep convection from the center of the lower-level circulation reflects the magnitude of wind shear between the lower and upper levels and its effects.
- Thermal:
  -  The classification of different cloud types reflects the intensity of convective development.
  -  The temperature in the eye of a tropical cyclone reflects the intensity of its core.

This technique premise that changes in the characteristics of a typhoon's cloud patterns correspond to a specific stage of its development and a certain intensity.

Procedures:
1. Determine the center of the typhoon system
2. Identify cloud type
3. Center-Cooled Cloud-Covered 
4. Determine the trend in the system's intensity over the past 24 hours
5. Determine the Modeled Expectation of Time (MET)
6. Determining the Cloud Type Index—Pattern T Number (PT)
7. Ultimate Strength Index
8. Current Intensity (CI)

Strengths
- Proven over time as a primary analytical technique
- Simple method for a complex task
- Effective in all regions; capable of handling storms of varying intensities

**Weaknesses**
- Subjective in certain aspects; training and practice are crucial
- Poor estimates for small storms and typhoons of high intensity
- Does not account for rapid movement
- Poor estimates during transitions in subtropical or high-latitude zones
- Poor estimates when making landfall or approaching large islands

# Part5 Temperature

## 5.1 Sea surface temperature

### 5.1.1 Importance of sea surface temperature
The uneven distribution of global sea surface temperatures has a profound impact on the global climate.

El Nino and La Nina

SST is closely related to the formation and evolution of typhoons.

Sea surface temperature: The temperature of the seawater near the sea surface. Buoy with 3-10 m;
- Interface SST
- Skin SST
- Subskin SST
- Depth SST
- Foundation SST/Buoy SST

Near infrared was emitted by 10-100 $\mu$m water;
Infrared was emitted by 5-10 $\mu$m water;

Emission ratio near to 1, reflectivity of 3-4 $\mu$m is six times higher than 11 $\mu$m.

3-4 $\mu$m is sensitive to sunlight reflectance, only suitable at night, but 11-12 $\mu$m is suitable all time except the point of reflection.

### 5.1.2 Infrared single channel
$$
I_\lambda = \varepsilon_\lambda B_\lambda(T_s) t_\lambda(p,0)
$$
### 5.1.3 Infrared double (multi) channels (11,12 $\mu$m)
$$
I^\uparrow(0) = I^\uparrow(\tau_0)t_0+\bar{B}^\uparrow(1-t_0)\\
I_i = B_i(T_i) = B_i(T_s)t_i+B_i(T_a)(1-t_i),\quad  B_i(T_a) \frac{1}{1-t_i}\int_{t_i}^1B_i(T)dt
$$

$T_a$ is the average temperature of whole layer, approximating to $T_{850hPa}$. Approximate the radiation relationship by replacing it with a temperature relationship, and $T_{a,11} = T_{a,12} = T_a,T_{s,11} = T_{s,12}=T_s$,

$$
T_{11} = T_st_{11}+(1-t_{11})T_a\\
T_{12} = T_st_{12}+(1-t_{12})T_a\\
T_s = T_{11}+\gamma(T_{11}-T_{12}),\quad \gamma = \frac{1-t_{11}}{t_{11}-t_{12}}\\
t_i = \exp(-\tau_i/\mu) \approx \exp\left(-\int_0^\infty k_i\rho_v dz/\mu\right) = \exp\left(-k_iV_v/\mu\right)\approx 1-\frac{k_iV}{\mu}\\
\gamma = \frac{1-t_{11}}{t_{11}-t_{12}} \approx \frac{k_{11}}{k_{12}-k_{11}},\quad T_s =T_{11}+\gamma(T_{11}-T_{12})
$$

Assumption among calculation:
- consider only vapor influence
- upward radiation is small
- $t$ is a function of vapor, neglect aerosols
- $T_{11},T_{12},T_a,T_s$ are same order
- $k_iV_v/\mu$ is small

Multi channels like three, similarly
$$
T_s = T_1+\frac{k_1}{2(k_2-k_1)}(T_1-T_2)+\frac{k_1}{2(k_3-k_1)}(T_1-T_3)\\
T_s = a_0+\sum_{i=1}^Ma_iT_i+(aV_v)
$$

### 5.1.4 Near infrared double (multi) channels
Similar to 5.1.3

### 5.1.5 AVHRR
$$
T_s =T_{11}+\gamma(T_{11}-T_{12})
$$

consider second order term $t_i = 1-k_iV_b\mu+\frac{(k_iV/\mu)^2}{2}$, $u = V_v/\mu$
$$
\begin{align*}
\gamma =& \frac{1-t_{11}}{t_{11}-t_{12}} = \frac{k_{11}u-\frac{k_{11}^2u^2}{2}}{k_{12}u-\frac{k_{12}^2u^2}{2}-k_{11}u+\frac{k_{11}^2u^2}{2}}\\
=& \frac{k_{11}-\frac{k_{11}^2u}{2}}{k_{12}-\frac{k_{12}^2u}{2}-k_{11}+\frac{k_{11}^2u}{2}} = \frac{k_{11}-\frac{k_{11}^2u}{2}}{k_{12}-k_{11}}\left[1-\frac{k_{12}+k_{11}}{2}u\right]^{-1}\\
\approx & \frac{k_{11}-\frac{k_{11}^2u}{2}}{k_{12}-k_{11}} \left[1+\frac{k_{12}+k_{11}}{2}u \right]\approx \frac{k_{11}}{k_{12}-k_{11}}\left[1+(k_{11}+k_{12})\frac{V}{2\mu}\right]\\
=&c_1+c_2V\sec\theta
\end{align*}\\
T_s =a_0+a_1T_{11}+a_2(T_{11}-T_{12})+a_3V\sec\theta(T_{11}-T_{12})\qquad \text{(WVSST)}\\
T_s =a_0+a_1T_{11}+a_2(T_{11}-T_{12})+a_3V(\sec\theta-1)(T_{11}-T_{12})\qquad \text{(MCSST)}\\
T_s =a_0+a_1T_{11}+a_2T_R(T_{11}-T_{12})+a_3V(\sec\theta-1)(T_{11}-T_{12})\qquad \text{(NLSST)}
$$

### 5.1.5 MODIS
$$
T_s =a_0+a_1T_{11}+a_2T_R(T_{11}-T_{12})+a_3V(\sec\theta-1)(T_{11}-T_{12})\qquad \text{(daytime)}\\
T_s =a_0+a_1T_{3.9}+a_2(T_{3.9}-T_{4.0})+a_3(\sec\theta-1)\qquad \text{(nighttime)}
$$

### 5.1.6 Microwave SST
Compared with infrared methods, which has high resolution and mature technology but need precise calibration and without clouds, microwave can run all the day, do NOT affacted by clouds, and easy to calibrate, but low resolution and sensitive to surface and precipitation.


## 5.2 Land surface temperature
**Compared with ocean surface, land surface is less uniform and varies a lot.**
**The reflectivity of land is much higher than ocean, with emissivity close to 1.**


### 5.2.1 Single channel

$$
I =B(T_b) = B(T_s)t_0+B(T_a)(1-t_0)\rightarrow T_b\approx T_st_0+T_a(1-t_0)\\
t_0  = \exp (-kV\sec\theta) \approx 1-kV\sec\theta, T_a \approx aT_s\\
T_s = \frac{T_b}{1-(1-a)kV\sec\theta }=\frac{T_b}{1-bT\sec\theta}
$$
Different lands have different $b$. Also can be written
$$
T_s(i) \approx c_{0i}+c_{1i}T_b+c_{2i}V\sec\theta
$$
### 5.2.2 Split-Window
Review for two channels
$$
T_{11} = T_st_{11}+(1-t_{11})T_a\\
T_{12} = T_st_{12}+(1-t_{12})T_a\\
T_{11}-T_s = (T_a-T_s)(1-t_{11})\\
T_{12}-T_s = (T_a-T_s)(1-t_{12})\\
T_s = T_{11}+\gamma(T_{11}-T_{12}),\gamma = \frac{1-t_{11}}{t_{11}-t_{12}}
$$
Three channals:
$$
T_s = T_1+\frac{k_1}{2(k_2-k_1)}(T_1-T_2)+\frac{k_1}{2(k_3-k_1)}(T_1-T_3)\\
T_s = a_0+\sum_{i=1}^Ma_iT_i\\
T_s = a_0+\sum_{i=1}^Ma_iT_i+a_VV\quad \text{(consider precipitation)}
$$
Can **NOT ignore reflectance of land.**
$$
T_{11} = [\varepsilon_{11} B_{11}(T_s)+(1-\varepsilon_{11})I_{11}^d]t_{11}+(1-t_{11})I_a\\
T_{12} = [\varepsilon_{12} B_{12}(T_s)+(1-\varepsilon_{12})I_{12}^d]t_{12}+(1-t_{12})I_a
$$
Similarly, can get
$$
T_s = a_0+a_1T_{11}+a_2T_{12}
$$


### 5.2.3 Multi channels
Similar to sst multi channels.



## 5.3 Temperature profiles
Select a absorption channel with some specific atmosphere composition, reflect highest radiation at different level in infrared bands.
Temperature: gas conc. high relatively, uniform vertical distribution, like CO2, O2;
Humidity: maximum emission bands, like H2O, O3;

### 5.3.1 Weighting function
$$
dF_\lambda = F_{\lambda}(z)\rho'(z)k_adz = -F_\lambda \exp(-\tau_\lambda(z))d\tau\\
\frac{dF}{dz} = \frac{dF}{d\tau}\frac{d\tau}{dz} = -F_\lambda \exp(-\tau(z))\frac{d\tau}{dz} = F_\lambda \frac{dt}{dz}, t=e^{-\tau}\\
W(z) = \frac{dt}{dz} = e^{-\tau(z)}\rho'k_a\quad \text{or} \quad W(z,\mu) = \frac{d}{dz}(t^{1/\mu})\\
W(z) = -\frac{dt}{d\ln p} = \frac{dt}{d\ln (p_s/p)}\\
\frac{dF}{dz} = FW(z)
$$ 
Actually, for most composition, $\rho'(z) = \rho_s'e^{-z/H}$
$$
\tau(z) = \int_z^\infty k_a\rho'dz = Hk_a\rho'\\
W(z) = \frac{\tau(z)}{H}e^{-\tau(z)}, \frac{dW(z)}{dz} = 0\rightarrow \tau(z) = 1
$$
**Weighting function shows the contribution of each level, and level where $\tau_\lambda(z) = 1$ contributes most.**
Therefore, select several bands at the edge of absorption region, there are different weight function (different most contribution level at different height). Combined these bands to get the vertical distributions

### 5.3.2 Statistical Inversion
#### 5.3.2.1 Direction inversion

#### 5.3.2.2 Constrained inversion

### 5.3.3 Temperature profile inversion



#### 5.3.3.1 Chahine Relaxation methods
$$
I_i = B_i(p_0)t_i(p_0) +\int_{p_0}^0B_i(p)\frac{dt_i(p)}{d\ln p}d \ln p, i = 1,2,\dots, M\\
\tilde{I}_i \approx B_i(T_0)t_i(p_0) +B_i(T_i)\frac{dt_i(p)}{d\ln p}|_{p_i} \Delta \ln p, i = 1,2,\dots, M\\
I_i' \approx B_i(T_0)t_i'(p_0) +B_i(T_i')\frac{dt_i(p)}{d\ln p}|_{p_i} \Delta \ln p, i = 1,2,\dots, M
$$
where $T_i'$ is the supposed temperature, and $T_i$ is real temparature.
$$
\frac{\tilde{I}_i - B_i(T_0)t_i(p_0)}{I_i' - B_i(T_0)t_i'(p_0)}\approx \frac{B_i(T_i)\frac{dt_i(p)}{d\ln p}|_{p_i}}{B_i(T_i')\frac{dt_i(p)}{d\ln p}|_{p_i}}\\
\frac{\tilde{I}_i }{I_i' }\approx \frac{B_i(T_i)}{B_i(T_i')}\quad\text{(relaxation equation)}\\
T^{(n+1)}(p_i) = b\nu_i/\ln \{1-\left[1-\exp\left(\frac{b\nu_i}{T^{(n)_i}}\right)\right]\frac{I_i^{(n)}{\tilde{I_i}}}\}
$$

#### 5.3.3.2 Smith relaxation methods
$$
I^{(n+1)}_i-I^{(n)}_i = \left[B^{(n+1)}_i(p_0)-B^{(n)}_i(p_0)\right]t_i(p_0) +\int_{p_0}^0\left[B^{(n+1)}_i(p)-B^{(n)}_i(p)\right]\frac{dt_i(p)}{d\ln p}d \ln p
$$
Assume $B^{(n+1)}_i(p)-B^{(n)}_i(p)$ is independent of $p$, therefore
$$
\int_{p_0}^0\left[B^{(n+1)}_i(p)-B^{(n)}_i(p)\right]dt_i(p) = \left[B^{(n+1)}_i(p)-B^{(n)}_i(p)\right] \left[1-t_i(p_0)\right]\approx B^{(n+1)}_i(p)-B^{(n)}_i(p)
$$
Therefore
$$
I^{(n+1)}_i-I^{(n)}_i \approx B^{(n+1)}_i(p)-B^{(n)}_i(p)\\
B^{(n+1)}_i(p) = B^{(n)}_i(p)+\tilde{I}_i-I^{(n)}_i \\
T^{(n+1)}(p,\nu_i) = \frac{b\nu_i}{\ln \left[1+a\nu_i^3/B_i^{(n+1)}(p)\right]}\\
T^{(n+1)}(p) = \frac{\sum_{i=1}^M T^{(n+1)}(p,\nu_i)K_i(p)}{\sum_{i=1}^M K_i(p)}\\
$$

# Part6 Humidity (Precipitable water)
$$
V_v =\int_0^\infty \rho_v dz
$$
Some absorption of water but not too much, and the distrubance is less.
- visible/near infrared: 0.94 $\mu$m;
- microwave: 25GHz
- thermal infrared: 11-13 $\mu$m, split window

## 6.1 Near infrared (0.94 $\mu$m and near window 0.865 $\mu$m)
$$
I_\lambda = I_S(\lambda)t(\lambda)r(\lambda)+I_p(\lambda), V^* =V(\frac{1}{\cos\theta}+\frac{1}{\cos\theta_0})\\
I_v = I_{Sv}r_V t_{av}t_{v}+I_{pv},I_0 = I_{S0}r_0 t_{a0}+I_{p0}\\
I_{pv} = CI_{Sv}r_V t_{av}t_{v}, I_{p0} = CI_{S0}r_0 t_{a0}\\
\text{def}\quad r^*I/I_S,r^*_v = Cr_V t_{av}t_{v},r^*_0 = Cr_0 t_{a0}\\
t_{av}\approx t_{a0},\quad \text{therefore}\quad r^*_v/r^*_0 = (r_V/r_0) t_{v}
$$
From the reflectivity of two channels $r^*_v/r^*_0$, and the surface reflectivity $(r_V/r_0)$ to get $t_v$, then get $V^*$ and $V$.
MODIS:
$$
t_v \approx r^*_v/r^*_0 = \exp \left(\alpha -\beta \sqrt{V^*}\right), V = \frac{V^*}{(\frac{1}{\cos\theta}+\frac{1}{\cos\theta_0})}
$$

## 6.2 Infrared
11 $\mu$m and 12 $\mu$m,

## 6.3 Microwave
**22.235 GHz and 31 GHz.**
For non-precipitation conditions, vapor and cloud droplets has weak absoption ane neglectable scattering with respect to microwave.
Due to the low emit frequency, ocean provides a uniform cold background.
$$
T_b(\mu) =\varepsilon_S(\mu) T_st_0^{1/\mu}+ (1-\varepsilon_S(\mu))T_ct_0^{2/\mu}+ \int_{0}^{\infty}TK(z,\mu)dz \\
K(z,\mu) = \left[1+\left(1-\varepsilon_s(\mu)\right)(\frac{t_0}{t})^{2/\mu}\right]\frac{dt^{1/\mu}}{dz}
$$
Vertically, $\mu = 1$, therefore
$$
\begin{align*}
T_b =&\varepsilon_S T_st_0+ (1-\varepsilon_S)T_ct_0^{2}+ \int_{0}^{\infty}T\left[1+\left(1-\varepsilon_s\right)(\frac{t_0}{t})^{2}\right]\frac{dt}{dz}dz \\
\approx&0+ (1-\varepsilon_S)T_ct_0^{2}+\int_{0}^{h}Tdt - (1-\varepsilon_s)t_0^2\int_0^h Td\frac{1}{t}\\
=& (1-\varepsilon_S)T_ct_0^{2}+ (T_h-\int_0^ht\frac{dT}{dz}dz)-(1-\varepsilon_s)t_0^2\left[T_h- \int_0^h \frac{1}{t}\frac{dT}{dz}dz\right]\\
=& T_c(1-\varepsilon_S)t_0^{2}+ T_s\left[a-b(1-\varepsilon_S)t_0^2\right]
\end{align*}
$$
In 20-40 GHz, $t\approx 1$, $a\approx b\approx 1$,
$$
T_b =T_c(1-\varepsilon_S)t_0^{2}+ T_s\varepsilon_St_0^2\\
T_b \approx T_s\left[1-(1-\varepsilon_S)t_0^2\right]
$$

## 6.4 Vertical profiles

# Part7 Percipitation



# Part8 Chemistry



# Part9 Aerosols
Direct radiative forcing
- Scatter more, therefore negative;
- Absorb more, therefore positive; 

Indirect radiative forcing
- Twomey effects: more CCN, average size of clouddroplets decrease, reflect more, negative;
- Albrecht effects: small size clouds have long lifetime, reflect more, negative;


optical depth of air molecule scattering
$\tau_{\lambda,R}(0) = 0.0088\lambda(\mu m)^{-4}$

## 9.2 Dark target

four channels: 0.55-0.68 $\mu$m, 0.75-1.10 $\mu$m, 3.55-3.93 $\mu$m, 10.5-11.5 $\mu$m;
$$
\tilde{I} = I_0t_0+I_R+I_A
$$
**If dark background, the $I_0t_0$ can be neglected, and Rayleigh scattering from aie molecule can be solved analytically, therefore only aerosols scattering.** 
$$
I_A = \frac{F_0\omega\tau_A P(\cos\theta)}{4\pi\mu},\tau_A = \int\beta_e dz,\beta_e = \int Q_e \pi r_a^2 n_a(r)dr
$$
According to asymmetry factor to determine phase funtion
$$
P(\theta) = \frac{\alpha(1-g_1^2)}{1+g_1^2-2g_1\cos\theta}+\frac{(1-\alpha)(1-g_2^2)}{1+g_2^2-2g_2\cos\theta}
$$




