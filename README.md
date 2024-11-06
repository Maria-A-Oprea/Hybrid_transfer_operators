## Hybrid infinitesimal generators of the Transfer operator

The hybrid transfer operator for a hybrid dynamical system 
$$ 
            \dot{x} = X(x),  x\not\in \mathcal{S}
            $$ $$
            x^+ = \Delta(x^-),  x\in\mathcal{S}.
        $$ wuth hybrid flow $\varphi^\mathcal{H}$, 
 is defined by the equation
 $\int_E P_t^\mathcal{H}f \, d\mu = \int_{\varphi_{-t}^\mathcal{H} (E)}\ f \, d\mu \qquad \text{for all } E \subseteq M$. The infinitesimal generator is defined by:
 $$A^\mathcal{H}f = \lim_{\Delta t \to 0}\frac{P_{t + \Delta t}^\mathcal{H}f - P_{t}^\mathcal{H}f}{\Delta t}$$

 In this project we write code to find a formula for $u(t, x) = P_t f(x)$ through the PDE that the infinitesimal generator has to satisfy i.e.
 $$\begin{cases}
            \displaystyle \frac{\partial u}{\partial t} - du(X) = 0 & \text{for } x \notin \mathcal{S}; \\[2ex]
            \displaystyle u(t^+,\Delta(x)) = u(t^-,x) & \text{for } x \in \mathcal{S}.
        \end{cases}$$

  We implemet the following examples:
  ### 1. The Bouncing ball
  $ \dot{x} = \frac{p}{m}, \quad
    \dot{p} = -mg$ and impacts occur when the ball strikes the ground ($x = 0$), and the reset map is $\Delta(0, p) = (0, -p)$. 

  ### 2. The redued chaplygin sleigh
  | Continuous | Discrete|
  | --------- | ---------|
  |$\dot v = a\omega^2$ | $v^+ = v^-$ |
  | $\dot\omega = -\frac{ma}{I + ma^2}v\omega$ | $\omega^+ = -\omega^-$ |
  | $\dot \theta = \omega$ | $\theta^+ = \theta^-$ |



  ### 3. Matrix groups 

  The configuration space is $Q = G = \text{GL}_n(\mathbb{R}) $, with impact surface $\Sigma = \text{SL}_n(\mathbb{R})$

  ### 4. An SIR model 

  Consider the general SIR model, with $S + I + R = N$ constant and impacts occur when the number of infected individuals reaches a treshold $\alpha$.  The equations of motion are

  \begin{align*}
    \begin{split}
        \dot{s} = & \ \mu - \mu s - (\beta - \delta) si\\
        \dot{i} = & \ \beta  si + \delta i^2 - (\gamma + \mu + \delta )i
    \end{split}
    \qquad \text{if } i \neq\alpha; \qquad \qquad 
    \begin{split}
        s^+ = & \ s^-\\
        i^+ = & \ (1 -f)i^-
    \end{split}
     \qquad \text{if } i  = \alpha,
\end{align*}


 For more information check https://arxiv.org/abs/2309.12569
