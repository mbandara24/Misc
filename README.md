# Misc

Test examples and code of markdown commands
 $\sqrt{3x-1}+(1+x)^2$

$`\sqrt{3x-1}+(1+x)^2`$

$`\hat{Y} = \hat{\beta}_{0} + \sum \limits _{j=1} ^{p} X_{j}\hat{\beta}_{j}`$


***
$\mathbf{\text{Gradient Tree Boosting Algorithm}}$<br>
***
1.&emsp;Initialize model with a constant value $$`f_{0}(x) = \textrm{arg min}_{\gamma} \sum \limits _{i=1} ^{N} L(y_{i}, \gamma)`$$

2.&emsp;For m = 1 to M:<br>
&emsp;&emsp;(a)&emsp;For $i = 1,2,...,N$ compute: $`r_{im} = - \displaystyle \Bigg[\frac{\partial L(y_{i}, f(x_{i}))}{\partial f(x_{i})}\Bigg]_{f=f_{m−1}}`$
    
&emsp;&emsp;(b)&emsp;Fit a regression tree to the targets $`r_{im}`$ giving terminal regions<br>
&emsp;&emsp;&emsp;&emsp;$`R_{jm}, j = 1, 2, . . . , J_{m}.`$<br><br>

&emsp;&emsp;(c)&emsp;For $j = 1, 2, . . . , J_{m}$ compute: $`\gamma_{jm} = \underset{\gamma}{\textrm{arg min}} \sum \limits _{x_{i} \in R_{jm}} L(y_{i}, f_{m−1}(x_{i}) + \gamma)`$


&emsp;&emsp;(d)&emsp;Update: $`f_{m}(x) = f_{m−1}(x) + \sum_{j=1}^{J_{m}} \gamma_{jm} I(x \in R_{jm})`$
3. Output $\hat{f}(x) = f_{M}(x)$
   
***
