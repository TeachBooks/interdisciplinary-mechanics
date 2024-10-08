# Assignment 5

## Introduction
This assignment aims to apply the "wave-based" methods to solve some classical river and traffic flows problems. All required methodological backgrounds can be found in the slides of lectures 14, 15.


## Section 1: The "Fancy" race
We are going to organize a race between cars and water in a river. At time $t <0$, both flows are packed between $x = -200 \mathrm{m}$ and $x = 0 \mathrm{m}$ and hold by gates/traffic signals. We remove the gates and turn traffic signals into green at time $t = 0$. Let's see what is happening!

```{figure} ../../figures/Assignment_5/A5_1.png
---
width: 60%
name: A5_Figure_1
align: center
---
Initial boundary conditions for the "fancy" race. (a) traffic flow (b) river flow.
```

{numref}`Figure {number} <A5_Figure_1>` represents the initial boundary conditions for both traffic (a) and river (b) flows. They define two Riemann problems at location $x = -200 \mathrm{m}$ and $x = 0 \mathrm{m}$. We are going to first focus on the front of the race, i.e., the Riemann problem at $x = 0 \mathrm{m}$. Our first objective is to draw the space-time diagram in both cases. {numref}`Figure {number} <A5_Figure_2>` provides the fundamental diagram of the traffic flow.

```{figure} ../../figures/Assignment_5/A5_2.png
---
width: 60%
name: A5_Figure_2
align: center
---
The traffic fundamental diagram providing the model parameters
```

### Question 1
The fundamental diagram in {numref}`Figure {number} <A5_Figure_2>` is quadratic in free-flow and linear in congestion. The equations are

$$ 
\begin{align}
Q(\rho) &= a \rho^2 + b\rho \quad &&\text{in free-flow} \\
Q(\rho) &= w(\rho_{max} - \rho) \quad &&\text{in congestion}
\end{align}
$$ 


<iframe src="https://tudelft.h5p.com/content/1292346473325637887/embed" aria-label="Assignment 5 Q1a" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>


````{admonition} Model answer
:class: dropdown

$w$ is the slope of the line in congestion modus.

$$ w = \frac{q_{max} - 0}{\rho_{max} - \rho_c} = \frac{0.6}{0.02 - 0.05} = 4 \mathrm{m/s}$$
````


<iframe src="https://tudelft.h5p.com/content/1292346477166812027/embed" aria-label="Assignment 5 Q01b" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>


````{admonition} Model answer
:class: dropdown
To find the value of $a$, 

$Q(\rho_c) = a \rho_c^2 + b\rho_c = q_{max}$

$a = \frac{q_{max} - v_{max}\rho_c}{\rho_c^2}= -20 \mathrm{m/s}$

To find the value of $b$, 

$Q'(0) = 2a \cdot 0 + b = v_{max}$
````


### Question 2
Draw the space-time diagram corresponding the Riemann problem at $x = 0 \mathrm{m}$ considering that the traffic obeys to the LWR model (first order macroscopic traffic flow model - cf. lecture 14). You will need it to answer the following questions.


````{admonition} Model Answer
:class: dropdown
You should have drawn a rarefaction wave to represent the front of the race (downstream $x=0$), otherwise double-check lecture 14.
````


<iframe src="https://tudelft.h5p.com/content/1292346481215822377/embed" aria-label="Assignment 5 Q02a" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>


````{admonition} Model Answer
:class: dropdown
The speed is the slope of the $q$-$\rho$ diagram. Have a look at the first part.

The steepest part of the curve is when $\rho = 0$ and the most gentle part when $\rho = \rho_c$. The fastest kinematic wave speed is $13 \mathrm{m/s}$ ($v_{max}$).
The slowest kinematic wave speed is 
$Q'(\rho_c) = 2 a \rho_c + v_{max} = 11 \mathrm{m/s}$
````


Q.2b
Draw the final space-time diagram with all the relevant information. 


````{admonition} Model Answer
:class: dropdown
Your space-time diagram should match the following:

```{figure} ../../figures/Assignment_5/A5_3.png
---
width: 50%
name: A5_Figure_3
align: center
---
Space-Time Diagram for Traffic
```
````


### Question 3
Let's consider we have a referee waiting for the race at $x = 200 \mathrm{m}$ (she will wait for the water flow too later on!).


<iframe src="https://tudelft.h5p.com/content/1292346496449340087/embed" aria-label="Assignment 5 Q03a" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>


````{admonition} Model Answer
:class: dropdown
The first car follows the fastest wave while the pack arrives right after the slowest wave. Front wave arrives at 

$$
t_1 = \frac{200 \mathrm{m}}{v_{max}} = 15.4 \mathrm{s}
$$
````


<iframe src="https://tudelft.h5p.com/content/1292346497928338447/embed" aria-label="Assignment 5 Q03b" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>


````{admonition} Model Answer
:class: dropdown
The first car follows the fastest wave while the pack arrives right after the slowest wave. 

The main pack arrives at 

$$
t_2 = \frac{200}{11} = 18.2 \mathrm{s}
$$
````


### Question 4
<iframe src="https://tudelft.h5p.com/content/1292346501098286397/embed" aria-label="Assignment 5 Q04" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>


````{admonition} Model Answer
:class: dropdown
We look for the kinematic wave starting at $x = 0$ at $t = 0$ and reaching $x = 200$ at $t$. The slope of this kinematic wave is $Q'(\rho)$ but also $\frac{x}{t}$.

So, 

$$2a\rho + v_{max} = \frac{x}{t}$$

Hence, 

$$\rho = \frac{\frac{x}{t} - v_{max}}{2a}$$
````


### Question 5
<iframe src="https://tudelft.h5p.com/content/1292346504923539137/embed" aria-label="Assignment 5 Q05a" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>


````{admonition} Model Answer
:class: dropdown
The condition is when the integral of the flow at $x = 200 \mathrm{m}$ is equal to $1$.
````


<iframe src="https://tudelft.h5p.com/content/1292346508077904517/embed" aria-label="Assignment 5 Q05b" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>


````{admonition} Model Answer
:class: dropdown
The conservation principle makes the calculation straightforward as we have

$$ \rho_c (x - 0) = 0 + q_{max}T - 1 $$

So,

$$ T = \frac{1 + k_c x}{q_{max}} = 18.33 > t_2 $$
````


### Question 6
Draw now the space-time diagram corresponding to the Riemann problem at $x = 0 \mathrm{m}$ for the river flow. Please refer to the non-linear solution method in lecture 15. Remember that a python code has been provided to automatically determine the state diagram, so you only have to draw the space-time diagram. Do not use the linear approximation here, as the initial conidition is too sharp.


<iframe src="https://tudelft.h5p.com/content/1292346512670545717/embed" aria-label="Assignment 5 Q06" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>


````{admonition} Model Answer
:class: dropdown
$$d_m = 0.56 \mathrm{m}$$

$$ V = 4.08 \mathrm{m/s} $$

(this only requires to set the values in the code `Water_flow` and run it)
````


### Question 7
<iframe src="https://tudelft.h5p.com/content/1292346514408516477/embed" aria-label="Assignment 5 Q07" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>


### Question 8
<iframe src="https://tudelft.h5p.com/content/1292346514974078997/embed" aria-label="Assignment 5 Q08" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>


### Question 9
<iframe src="https://tudelft.h5p.com/content/1292346517636055867/embed" aria-label="Assignment 5 Q09" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>


````{admonition} Model Answer
:class: dropdown
For a rarefaction wave, wave speeds are defined by $\lambda_1(U)$ where, $U$ is between the two boundary states (here $U_{l}$ and $U_m$). The kinematic wave speeds are $\lambda(U_l)$ and $\lambda(U_m)$ with $\lambda = V - \sqrt{gd}$.
````


### Question 10
<iframe src="https://tudelft.h5p.com/content/1292346519289245377/embed" aria-label="Assignment 5 Q10" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>


````{admonition} Model Answer
:class: dropdown
For a shockwave, the speed is given by the Rankine-Hugoniot condition, which depends on the two boundary states (here $U_m$ and $U_r$).

This wave is a shockwave, whose speed is 

$$
\frac{U_r d_r - U_m d_m}{d_r - d_m} = 4.1 \mathrm{m/s}
$$
````


### Question 11
<iframe src="https://tudelft.h5p.com/content/1292346522387676937/embed" aria-label="Assignment 5 Q11a" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>


````{admonition} Model Answer
:class: dropdown
Use the speed of the front wave from the previous question: 

$$ v = 4.1 m/s $$
$$ t= \frac{s}{v} = \frac{200}{4.1} = 48.8 \mathrm{s}$$
````


<iframe src="https://tudelft.h5p.com/content/1292346523472525407/embed" aria-label="Assignment 5 Q11b" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>


````{admonition} Model Answer
:class: dropdown
After the cars, see question 3 (first car arrives at $t = 15.4 \mathrm{s}$).
````


### Question 12
<iframe src="https://tudelft.h5p.com/content/1292346525283913577/embed" aria-label="Assignment 5 Q12a" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>


````{admonition} Model Answer
:class: dropdown
A linear diagram is free-flow with a free-flow speed equal to $4.1 \mathrm{m/s}$. Because the front wave in water is a single wave. The only way to get that with the traffic is that the fan collapses into a signgle contact wave, which can only happen in the fundamental diagram in linear in free-flow.
````


<iframe src="https://tudelft.h5p.com/content/1292346528710464427/embed" aria-label="(NO ANSWER) Assignment 5 Q12b" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>


**(I dont have the modal answer/No Modal answer)**


<iframe src="https://tudelft.h5p.com/content/1292346530080687457/embed" aria-label="Assignment 5 Q12c" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>


````{admonition} Model Answer
:class: dropdown
With the linearization, the state diagram is a simple triangle, whose base is $(0, 0)$, $(d_0, 0)$. The height of this triangle represents the speed at $U_m$, which is also the speed of the shockwave in that particular case as the downstream state is $(0, 0)$. The slope of the triangle is $\sqrt{\frac{2d}{d_0}}$. 

In this end, we want that :

$$
\sqrt{\frac{2g}{d_0}} \cdot \frac{d_0}{2} = \sqrt{\frac{gd_0}{2}} > 13 = v_{max, traffic}
$$

It happens when $d_0 > 34.34 \mathrm{m}$. Note that when you check with the non-linear state diagram, the value is different close to $18 \mathrm{m}$ because it is clear that non-linear effect matters here.
````


### Question 13
Now we focus on the rear Riemann problem at $x = -200 \mathrm{m}$.


<iframe src="https://tudelft.h5p.com/content/1292346538141588587/embed" aria-label="Assignment 5 Q13a" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>


<iframe src="https://tudelft.h5p.com/content/1292346540077173667/embed" aria-label="Assignment 5 Q13b" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>


````{admonition} Model Answer
:class: dropdown
A steady shockwave whose speed is $0$. Physically, that means that even if now cars are allowed to drive backwards, they don't!
````


### Question 14
<iframe src="https://tudelft.h5p.com/content/1292346546488462707/embed" aria-label="Assignment 5 Q14" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>


````{admonition} Model Answer
:class: dropdown
Because the eigenvalues of the river flow problem are symmetric when $V = 0 (\lambda = \pm \sqrt{gh})$, the solutions are also symmetric if the initial condition is. So, it suffices to reverse the solution of the front Riemann problem to derive the rear Riemann problem.
````


### Question 15
<iframe src="https://tudelft.h5p.com/content/1292346548305881537/embed" aria-label="Assignment 5 Q15" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>


````{admonition} Model Answer
:class: dropdown
It is when the contact wave propagating backward from $x = 0$ (see the solution of the front Riemann problem in Q2) meets the steady shockwave of the rear Riemann problem. The first wave starts at $x = 0, t = 0$ with a speed $-4 \mathrm{m/s}$ (see {numref}`Figure {number} <A5_Figure_2>` and question Q1) and the second from $x = -200$ at $t = 0$, with a speed equal to $0$. They meet at time $t = 50 \mathrm{s}$.
````


### Question 16
<iframe src="https://tudelft.h5p.com/content/1292346565305691827/embed" aria-label="Assignment 5 Q16" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>


````{admonition} Model Answer
:class: dropdown
There are two boundary waves starting at $x = 0 \mathrm{m}$ and $x = -200 \mathrm{m}$ have a speed equal to $-4.4$ and $4.4 \mathrm{m/s}$ respectively. So, they meet at time $22.7 \mathrm{s}$. It is worth noticing that the initial state disappears quicker in the river (water is less "stable" than a compact car platoon!)

$$
\begin{align}
-4.4 \cdot t &= -200 + 4.4 \cdot t \\
8.8 \cdot t &= 200 \\
t &= 22.7 \mathrm{s}
\end{align}
$$
````


## Section 2
### Question 17
We are going to further investigate what happens at the front of the race. Let's start with the river flow. Imagine now we have a gate every $200 \mathrm{m}$ (like traffic signals at intersections).


<iframe src="https://tudelft.h5p.com/content/1292346567249701637/embed" aria-label="Assignment 5 Q17" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>


````{admonition} Model Answer
:class: dropdown
The problem is easy as there is no dispersion at the front. We only need to have an offset of $\frac{200 \mathrm{m}}{4.1 \mathrm{m/s}} = 48.8 \mathrm{s}$.

You have just created a green wave for river flow (even though not really useful as there are no opposite flows passing during red time).
````


### Question 18
<iframe src="https://tudelft.h5p.com/content/1292346569582447107/embed" aria-label="Assignment 5 Q18" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>


````{admonition} Model Answer
:class: dropdown
$$
\begin{align}
x &= 200 \mathrm{m} \\
t_2 - t_1 &= 18.2 - 15.4 \\
&= 2.8 \mathrm{s} 
\end{align}
$$

Think $s = v \cdot t$. We know $s$ and $v_{min}$ and $v_{max}$, so we can calculate $t_2 - t_1$.

Similarly, for the rest, 

$$
\begin{align}
&x = 400 \mathrm{m}, &&t_2 - t_1 = 5.6 \mathrm{s} \\
&x = 600 \mathrm{m}, &&t_2 - t_1 = 8.4 \mathrm{s} \\
&x = 800 \mathrm{m}, &&t_2 - t_1 = 11.2 \mathrm{s} \\
&x = 1000 \mathrm{m}, &&t_2 - t_1 = 14 \mathrm{s} 
\end{align}
$$
````


### Question 19
By using similar (but more advance as $T$ is now in the middle of the rarefaction waves) technique as in Q5, it is possible to calculate the time required for one vehicle (cumulative flow value equal to 1) to completely cross each intersection after the front wave has passed. The values are $4.1 \mathrm{s}, 5 \mathrm{s}, 5.7 \mathrm{s}, 6.4 \mathrm{s}$ for the intersections at $x = 400$, $600$, $800$, and $1000 \mathrm{m}$ respectively.


<iframe src="https://tudelft.h5p.com/content/1292346571465229387/embed" aria-label="Assignment 5 Q19" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>


````{admonition} Model Answer
:class: dropdown
A rarefaction fan represents the dispersion of the front wave. The further we are from the initial discontinuity, the smoother the transition in flow is.
````


### Question 20
<iframe src="https://tudelft.h5p.com/content/1292346573241618227/embed" aria-label="Assignment 5 Q20" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>


````{admonition} Model Answer
:class: dropdown
You want to minimize the total delay in the system (collective optimum). If dispersion is observed it is useless to provide green immediately to the very first vehicles as the total outflow will not be maximum. It is better to stop them and wait for the main vehicle pack, especially if the possible green time is limited.
````


## Section 3: The Race between Slugs and Rabbits (trucks and cars!)
**NOTE: The last questions are extra material. Last year, this assignment was too long, but we didn't want to remove it, as it may serve as a challenge for those of you that cover the material well. Besides, it is more practice material!**

Now, we organize a multiclass traffic race. A platoon with $20 %$ of trucks is waiting upstream at $x = 0$ until the traffic signal turns green at $t = 0$, see {Add figure reference (Missing Figure 3)} that represents the initial Riemann problem. We label the car flow as $1$ with a density $\rho_1$ and truck flow as $2$ with a density $\rho_2$ **(CHECK $\rho$ VALUES)**. {Add Figure reference (Missing FIgure 4)} provides the fundamental diagrams in speed for both vehicle types and the model you should solve is given on slide 3 in the lecture 15.

The main objective is to draw the space-time diagram after the signal turns green. We are going to use two different methods. First, the linear approximation that allows you to make all calculations by yourself. However, it is clear here that the conditions for this approximation to be valid does not hold. Indeed, the jump in density between the left side (the platoon of vehicles) and the right side (void) is too high. By using then the full non-linear solution method, you will be able to assess the validity of the approximation.


### Question 21
Draw the state-space diagram using the linear approximation and determine the intermediate traffic states $U_m$ at the front of the race.


````{admonition} Model Answer
:class: dropdown
Applying the linear approximation requires to define a steady state $U_0$ along the full link. Indeed, the linear approximation is supposed to study the deviations $\epsilon$ around this steady state (like the average water height and speed for the water flow). Here, the $U_0$ is simply the average between the left ($U_l$) and the right ($U_r$) states.

The solution method for the linear approximation is given on slides 16, 17 and 18 of the lecture 15.

We need first to determine the common steady state $U_0$ as the average of $U_l$ and $U_r$. Here, $U_0$ is then equal to ($\rho_1^0 = 0.075$; $\rho_2^0 = 0.015$). If we apply the multiclass model, we know that the elements of the $\mathbf{A}$ matrix that defines the model is quasi linear form considering the given fundamental diagrams are:


$$
\begin{align}
&a = V_1^{max}\left(1 - \frac{\rho_1 + \rho_2}{\rho_{max}}\right) - \frac{V_1^{max}}{\rho_{max}}\rho_1 \\
&b = \frac{V_1^{max}}{\rho_{max}}\rho_1  \\
&c = -\frac{V_2^{max}}{\rho_{max}}\rho_2  \\
&d = V_2^{max}\left(1 - \frac{\rho_1 + \rho_2}{\rho_{max}} \right) - \frac{V_2^{max}}{\rho_{max}}\rho_2
\end{align}
$$

We need to determine the two eigenvalues and the related eigenvectors for the state $U_0$. The formulae are provided on slides 8 and 10 of lecture C4.1.c. The numerical results are $\lambda_1 = 1.89 \mathrm{m/s}$; $\lambda_2 = 8.7 \mathrm{m/s}$; $w_1 = (4.65; 1)$; $w_2 = (-1.43; 1)$

To determine the intermediate state, one should first draw the line starting from $U_l$ with a directed vector $w_1$ and then draw the line starting from $U_r$ with a directed vector $w_2$. The intersection between these two lines give the intermediate state, here $U_m = (0.0024, -0.0017)$.

```{figure} ../../figures/Assignment_5/A5_6.png
---
width: 100%
name: A5_Figure_6
align: center
---

```
````


### Question 22
<iframe src="https://tudelft.h5p.com/content/1292347308414911257/embed" aria-label="Assignment 5 Q22" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>


````{admonition} Model Answer
:class: dropdown
The speed is equal to $\lambda_2(U_0) = 8.7 \mathrm{m/s}$.
````


### Question 23
<iframe src="https://tudelft.h5p.com/content/1292347309344085587/embed" aria-label="Assignment 5 Q23" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>


<iframe src="https://tudelft.h5p.com/content/1292347311798097117/embed" aria-label="Assignment 5 Q23b" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>


````{admonition} Model Answer
:class: dropdown
The intermediate state is not feasible because $\rho_2^m <0 $. Also, the speed of the front wave looks way to slow compared to the maximal speed of the car that should be on the front of the race. The main reason is that the linear approximation does not hold. The jump in density between $U_l$ and $U_r$ is way too sharp.
````


### Question 24
<iframe src="https://tudelft.h5p.com/content/1292347315665787567/embed" aria-label="Assignment 5 Q24" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>


````{admonition} Model Answer
:class: dropdown
By reading the state diagram, we see that $U_m$ is $(0.0252, 5.74 \times 10^{-5})$. Now the intermediate state is feasible.
````


### Question 25
<iframe src="https://tudelft.h5p.com/content/1292347318451985487/embed" aria-label="Assignment 5 Q25a" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>


````{admonition} Model Answer
:class: dropdown
The front wave is rarefaction wave as the state diagram is composed of a 1-wave intersecting a 2-wave.
````


<iframe src="https://tudelft.h5p.com/content/1292347320129310647/embed" aria-label="Assignment 5 Q25b" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>


````{admonition} Model Answer
:class: dropdown
The wave speeds in the rarefaction wave are between $\lambda_2(U_m)$ and $\lambda_2(U_r) = 20 \mathrm{ m/s}$.

The maximal speed is then equal to $20 \mathrm{ m/s}$ which represents the maximal speed of the cars.
````


### Question 26
<iframe src="https://tudelft.h5p.com/content/1292347322663344017/embed" aria-label="Assignment 5 Q26" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>


**(ADD ANSWERS IN H5P)**


**ADD MODEL ANSWER**


### Question 27
Now, we change the right state to $(0.14, 0.02)$. The linear approximation should provide good results as the densities are close on both sides of the Riemann porblem. Calculate the intermediate state with the linear approximation. Then, use the python code to determine the intermediate state and compare the results.


<iframe src="https://tudelft.h5p.com/content/1292347326882739447/embed" aria-label="Assignment 5 Q27" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>


````{admonition} Model Answer
:class: dropdown
With the linear approximation, $U_m = (0.1321, 0.0276)$.
The non-linear method gives $U_m = (0.1323, 0.0272)$.
The results are indeed very close and the linear approximation holds.
````












