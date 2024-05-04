# Robotic-and-Control
#![pr](https://github.com/KianoushAqabakee/Robotic-and-Control/tree/main/Nvidia%20Jetiracer%20Pro%20Control/MPC-RBF%20Control/QT_Tracking_Results_1.png)
<img src="./Nvidia%20Jetiracer%20Pro%20Control/MPC-RBF%20Control/QT_Tracking_Results_1.png" alt="">
<img src="./Nvidia%20Jetiracer%20Pro%20Control/MPC-RBF%20Control/QT_Tracking_Results_2.png" alt="">

## Type-2 Generalized Fuzzy Hyperbolic (IT2-GFH)

### Forward Formula

$y_{I T 2-G F H S}=W \psi$
$W=[\alpha, \underline{\beta}, \bar{\beta}]$
$\psi=\left[1, \tanh \left(\frac{K(u-d)}{\underline{\sigma}^2}\right), \tanh \left(\frac{K(u-d)}{\bar{\sigma}^2}\right)\right]$


### Update Rule

$E=\frac{1}{2}\left(y_{\text {actual }}-y_{I T 2-G F H S}\right)^2=\frac{1}{2} e^2$

$\Delta \mathrm{W} = e  \psi$

$\Delta \mathrm{d}=e\left[-\frac{\mathrm{K}}{\underline{\sigma}^2}\left(1-\tanh \left(\frac{K(u-d)}{\underline{\sigma}^2}\right)^2\right),\right.$

$\left.\qquad\qquad-\frac{\mathrm{K}}{\bar{\sigma}^2}\left(1-\tanh \left(\frac{K(u-d)}{\bar{\sigma}^2}\right)^2\right)\right]$

$\Delta \bar{\sigma}=-e\frac{\mathrm{K}(u-d)}{\bar{\sigma}^3}\left(1-\tanh \left(\frac{K(u-d)}{\bar{\sigma}^2}\right)^2\right)$

$\Delta \underline{\sigma}=-e\frac{\mathrm{K}(u-d)}{\underline{\sigma}^3}\left(1-\tanh \left(\frac{K(u-d)}{\underline{\sigma}^2}\right)^2\right)$

$\Delta \mathrm{K}=e\left[-\frac{(u-d)}{\underline{\sigma}^2}\left(1-\tanh \left(\frac{K(u-d)}{\underline{\sigma}^2}\right)^2\right),\right.$

$\left.\qquad\qquad-\frac{(u-d)}{\bar{\sigma}^2}\left(1-\tanh \left(\frac{K(u-d)}{\bar{\sigma}^2}\right)^2\right)\right]$

## Kinematic Model of Nvidia Jetracer Pro AI 

<img src="./Images/Jetracer_K.png" alt="">

$\dot{p}_x =V \cos (\psi+\beta)$

$\dot{p}_y =V \sin (\psi+\beta)$

$\dot{\psi} =\frac{V \cos (\beta)}{L_{x f}+L_{x r}}\left(\tan \left(\delta_f\right)-\tan \left(\delta_r\right)\right)$

$\beta =\arctan \left(\frac{L_{x f} \tan \left(\delta_r\right)+L_{x r} \tan \left(\delta_f\right)}{L_{x f}+L_{x r}}\right),$

## Dynamic Model of Lower Limb Exoskeleton Rehabilitation Robot 

<img src="./Images/Exo_Dynamic.png" alt="">