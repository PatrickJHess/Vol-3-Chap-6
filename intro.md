# **Financial Python**

## **Volume: Basic Concepts of Fixed Income**

### **Chapter Six: Yield To Maturity**

Chapter Five introduced **par yields** as the coupon rates for bonds that sell at their par value, where these rates are determined by the term structure of interest rates.

This chapter shifts focus to **yields to maturity**. Unlike par yields, yields to maturity are *not* derived from the term structure. Instead, the yield to maturity is defined as the single discount rate that equates a bond's present value to its current market price. This rate is typically calculated using an iterative procedure to solve the bond's present value equation.

**The Relation Between Par Yields and Yields to Maturity**

Although generally different, par yields and yields to maturity are the same when bonds trade at par. A bond's par value is defined as the present value of its par value coupons and the principal payment at maturity.

Defining $\text{ytm}_c$ as the continuous compound yield to maturity, the par value is:

<br>

&emsp;&emsp;&emsp;&emsp;$\text{Par Value} = \text{Par Value}\times\sum_{t=1}^{T}\text{Par Yield }\times e^{-ytm_c\times t}+ \text{Par Value}\times e^{-ytm_c\times T}$

<br>

Simplifying by dividing by the discounted value of par value at maturity and subtracting one from both sides of the equation:

<br>

&emsp;&emsp;&emsp;&emsp;$\large e^{ytm_c\times T}-1 = e^{ytm_c\times T}\times\sum_{t=1}^{T} e^{-ytm_c\times t}\times \text{Par Yield }$

<br>

Define $\text{ytm}_d$ as the discrete value of the continuous compounded yield to maturity and using the annuity formula for for the sum of the present values of par yield:

<br>

&emsp;&emsp;&emsp;&emsp;$\large (1+ytm_d)^T -1 = (1+ytm_d)^T\times \frac{(1+ytm_d)^T -1}{ytm_d\times (1+ytm_d)^T }\times \text{Par Yield}$

<br>

Solving for the discrete compounded yield to maturity:

<br>

&emsp;&emsp;&emsp;&emsp;$\large 1 = \frac{1}{ytm_d}\times \text{Par Yield}$

<br>

&emsp;&emsp;&emsp;&emsp;$\large ytm_d = \text{Par Yield}$

<br>

The yield to maturity of a bond selling for par is its par yield.

It's important to note that the yield to maturity generally does not forecast future rates of return. Nevertheless, similar to par yields, yields to maturity provide valuable insights into the relative pricing of bonds.

### **Leapfroggging into the chapter**

You can begin with Chapter six even if you are unfamiliar with the content of the preceding chapters. This is possible because a custom module containing the functions developed earlier is imported directly into the chapter. There are no required dependencies between this chapter and previous ones.
