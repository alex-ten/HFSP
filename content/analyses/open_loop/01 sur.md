---
title: Multinomial logistic model
category: open_loop
doctype: entry
entrynum: 1
---

Switches to:

<pre class='codeblock'>
{% raw %}
  1   2   3   4 
464 523 547 589 
{% endraw %}
</pre>

Switches from:
<pre class='codeblock'>
{% raw %}
  1   2   3   4 
478 529 560 556 
{% endraw %}
</pre>

Switches from to:
<pre class='codeblock'>
{% raw %}
      1   2   3   4
  1   0 173 163 142
  2 163   0 167 199
  3 144 168   0 248
  4 157 182 217   0
{% endraw %}
</pre>

## Model A:
<pre class='codeblock'>
{% raw %}
  nxt ~ pval+relt+lrn+currentd|trial
{% endraw %}
</pre>

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
                   Estimate    Std. Error z-value  Pr(>|z|)    
2:(intercept)   -0.27684508    0.28543223 -0.9699 0.3320887    
3:(intercept)   -0.19192031    0.29010940 -0.6615 0.5082631    
4:(intercept)   -0.27873889    0.28740290 -0.9699 0.3321192    
pval             2.79168475    0.83635101  3.3379 0.0008440 ***
relt            -1.55093064    0.42493996 -3.6498 0.0002625 ***
lrn              0.18886202    0.10252118  1.8422 0.0654495 .  
currentd       -21.25518053 2552.52920871 -0.0083 0.9933560    
2:trial          0.00178361    0.00149432  1.1936 0.2326364    
3:trial          0.00078149    0.00150799  0.5182 0.6042949    
4:trial          0.00143862    0.00147486  0.9754 0.3293492    
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Log-Likelihood: -1023.4
McFadden R^2:  0.22764 
Likelihood ratio test : chisq = 603.27 (p.value = < 0.000000000000000222)
{% endraw %}
</pre>

<pre class='codeblock'>
{% raw %}
> cm$table
          Reference
Prediction   1   2   3   4
         1  47  21  28  30
         2  52 106  54  52
         3  50  35  92  36
         4  72  77  63 142

 Accuracy = 0.4043887 
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
g'(-H)^-1g = 5.08E-07 
gradient close to zero 

Coefficients :
                   Estimate    Std. Error z-value      Pr(>|z|)    
2:(intercept)    0.11616730    0.26017058  0.4465       0.65523    
3:(intercept)    0.12556572    0.26008962  0.4828       0.62925    
4:(intercept)   -0.20815270    0.26042791 -0.7993       0.42413    
pval             4.37583568    0.77772489  5.6265 0.00000001839 ***
relt            -1.53866523    0.38476109 -3.9990 0.00006360675 ***
lrn              0.08455331    0.09811352  0.8618       0.38880    
currentd       -21.24256717 2313.13771642 -0.0092       0.99267    
2:trial          0.00024099    0.00137566  0.1752       0.86094    
3:trial          0.00070042    0.00136929  0.5115       0.60898    
4:trial          0.00228214    0.00135556  1.6835       0.09227 .  
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Log-Likelihood: -1230.2
McFadden R^2:  0.23551 
Likelihood ratio test : chisq = 757.94 (p.value = < 0.000000000000000222)
{% endraw %}
</pre>

<pre class='codeblock'>
{% raw %}
          Reference
Prediction   1   2   3   4
         1  34  14   9  17
         2  47 108  40  41
         3  75  86 185  60
         4  87  76  76 211

 Accuracy = 0.4614065
{% endraw %}
</pre>

---

### Baselines
<pre class='codeblock'>
{% raw %}
# Sample random choices 100 times and average accuracies across samples
Random selection accuracy = 0.248670668953688

#
{% endraw %}
</pre>

