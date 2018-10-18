---
title: Multinomial logistic model
category: open_loop
doctype: entry
entrynum: 1
---


Switches from-to:
<pre class='codeblock'>
{% raw %}
    to
from  1   2   3   4  sum
  1   0 173 163 142  478
  2 163   0 167 199  529
  3 144 168   0 248  560
  4 157 182 217   0  556
  
sum 464 523 547 589
{% endraw %}
</pre>

## Model A:
<pre class='codeblock'>
{% raw %}
  nxt ~ pval+relt+lrn+currentd|trial
{% endraw %}
</pre>

### Both groups
<pre class='codeblock'>
{% raw %}
Frequencies of alternatives:
      1       2       3       4 
0.21856 0.24635 0.25765 0.27744 

nr method
21 iterations, 0h:0m:0s 
g'(-H)^-1g = 9.24E-07 
gradient close to zero 

Coefficients :
                 Estimate  Std. Error z-value        Pr(>|z|)    
2:(intercept)    0.025190    0.100500  0.2507         0.80208    
3:(intercept)   -0.069515    0.103809 -0.6696         0.50308    
4:(intercept)   -0.066357    0.107482 -0.6174         0.53699    
pval             3.610880    0.564834  6.3928 0.0000000001629 ***
relt            -1.465070    0.280948 -5.2147 0.0000001840692 ***
currentd       -21.251133 1714.781548 -0.0124         0.99011    
lrn              0.133571    0.070663  1.8902         0.05873 .  
2:grp            0.142341    0.135979  1.0468         0.29520    
3:grp            0.329378    0.135881  2.4240         0.01535 *  
4:grp            0.284447    0.134800  2.1101         0.03485 *  
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Log-Likelihood: -2257.6
McFadden R^2:  0.23088 
Likelihood ratio test : chisq = 1355.4 (p.value = < 0.000000000000000222)
{% endraw %}
</pre>

<pre class='codeblock'>
{% raw %}
> cm$table
          Reference
Prediction   1   2   3   4
         1  74  37  42  45
         2 105 204  79  88
         3 123 112 279  97
         4 162 170 147 359

 Accuracy = 0.4314649 
{% endraw %}
</pre>

---

### Group F
<pre class='codeblock'>
{% raw %}
Frequencies of alternatives:
      1       2       3       4 
0.23093 0.24974 0.24765 0.27168 

nr method
21 iterations, 0h:0m:0s 
g'(-H)^-1g = 4.17E-07 
gradient close to zero 

Coefficients :
                 Estimate  Std. Error z-value  Pr(>|z|)    
2:(intercept)    0.042419    0.100993  0.4200 0.6744711    
3:(intercept)   -0.047004    0.107676 -0.4365 0.6624511    
4:(intercept)   -0.017691    0.116385 -0.1520 0.8791857    
pval             2.716531    0.826147  3.2882 0.0010083 ** 
relt            -1.548118    0.422359 -3.6654 0.0002469 ***
currentd       -21.252081 2552.818806 -0.0083 0.9933577    
lrn              0.189717    0.102371  1.8532 0.0638489 .  
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Log-Likelihood: -1024.3
McFadden R^2:  0.227 
Likelihood ratio test : chisq = 601.6 (p.value = < 0.000000000000000222)
{% endraw %}
</pre>

<pre class='codeblock'>
{% raw %}
> cm$table
          Reference
Prediction   1   2   3   4
         1  45  23  34  32
         2  55 102  47  50
         3  48  35  94  31
         4  73  79  62 147

 Accuracy = 0.4054336
{% endraw %}
</pre>

---

### Group S
<pre class='codeblock'>
{% raw %}
Frequencies of alternatives:
      1       2       3       4 
0.20840 0.24357 0.26587 0.28216 

nr method
21 iterations, 0h:0m:0s 
g'(-H)^-1g = 5.07E-07 
gradient close to zero 

Coefficients :
                 Estimate  Std. Error z-value      Pr(>|z|)    
2:(intercept)    0.159433    0.093621  1.7030     0.0885739 .  
3:(intercept)    0.244975    0.098500  2.4870     0.0128808 *  
4:(intercept)    0.182369    0.112038  1.6277     0.1035791    
pval             4.417456    0.776722  5.6873 0.00000001291 ***
relt            -1.428084    0.377489 -3.7831     0.0001549 ***
currentd       -21.247715 2314.425959 -0.0092     0.9926751    
lrn              0.085451    0.097943  0.8725     0.3829605    
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Log-Likelihood: -1232
McFadden R^2:  0.23436 
Likelihood ratio test : chisq = 754.24 (p.value = < 0.000000000000000222)
{% endraw %}
</pre>

<pre class='codeblock'>
{% raw %}
          Reference
Prediction   1   2   3   4
         1  32  13   8  17
         2  47 106  38  38
         3  80  75 190  63
         4  84  90  74 211

 Accuracy = 0.4622642
{% endraw %}
</pre>

---

### Baselines
<pre class='codeblock'>
{% raw %}
# Average accuracies across 100 random samples
accuracy = 0.248670668953688

# Baseline challenge predictions
accuracy = 0.327315914489311
{% endraw %}
</pre>

