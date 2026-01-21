

# What Is The Yield To Maturity And Why It Matters


The Yield to Maturity ($\text{ytm}$) of a bond is defined as the single discount rate ($\text{ytm}$) that equates the present value of the bond's expected future cash flows (coupons and principal) to its current market value.


## Formula and Calculation:


The general formula for a bond's value is:


&emsp;&emsp;&emsp;&emsp;&emsp;$\text{Bond Value} = \sum_{t=1}^{T}\text{Cash Flow}_{t}\times e^{-r_t\times t}$

<br>

The discount rate at $\text{t}$ is $\text{r}_t$. Substituting the yield to maturity ($\text{ytm}$) for each discount rate:


&emsp;&emsp;&emsp;&emsp;&emsp;$\text{Bond Value} = \sum_{t=1}^{T}\text{Cash Flow}_{t}\times e^{-\text{ytm}\times t}$
<br>

For a zero-coupon bond (a bond making a single payment at maturity), $\text{ytm}$ can be calculated directly:


&emsp;&emsp;&emsp;&emsp;&emsp;$ \text{P(t)} = e^{-\text{ytm}\times t}\times \text{Cash Flow}_t$


## Limitations of Yield To Maturity

The yield to maturity ($\text{ytm}$) is often, but incorrectly, assumed to be the actual internal rate of return (IRR) an investor will earn by holding a bond until maturity. This assumption holds true only for default-free bonds that involve a single payment at maturity.

For bonds with multiple cash flows (i.e., coupon payments), the $\text{ytm}$ is merely an approximation because the reinvestment rates for these payments are uncertain and are unlikely to equal the yield to maturity. This uncertainty parallels the limitations investors encounter when using IRR in capital budgeting. Furthermore, the promised payments for bonds with default risk add an additional level of uncertainty.

Despite these limitations, it is important to recognize that bond pricing inherently incorporates the prevailing term structure of interest rates and reflects forward rates, that are indicative of future reinvestment returns.

## Calculating The Yield To Maturity
As noted above, the $\text{ytm}$ of a bond making a single payment may be directly calculated. There is no simple calculation for bonds that make multiple payments.  A trial and error process is required.  A practical way to implement the technique is a comparison of the errors of two initial guesses and then adjusting subsequent guesses based on the average rate of change between the errors and the guesses.

For functions that are differentiable, a more mathematically efficient version of this trial-and-error technique exists: the Newton-Raphson method, that utilizes a first-order Taylor series approximation of the function.
<br><br>

 &emsp;&emsp;&emsp;&emsp;&emsp;  $\text{f}(x+\Delta x) \thickapprox \text{f}(x) +\large\frac{d\text{f}(x)}{dx}\times\Delta x$

<br>

The first derivative of the function is $\Large\frac{d\text{f}(x)}{dx}$ at $x$, and $\Delta x$ is the change in $x$.

<br>

As $\large\Delta \text{x}$ goes to zero, the error of the approximation goes to zero.

<br>

The Newton-Raphson method improves each guess by scaling the error by the first derivative of the function at the previous guess:


&emsp;&emsp;&emsp;&emsp;&emsp;$\text{next guess} =\text{previous guess}+\Large \frac{\text{f}(x)-\text{f}(\text{previous guess})}{\frac{df(\text{previous guess})}{dx}}$


## A three bond example

The yield to maturity on all three bonds is assumed to be 5% per annum. Coupon payments are semi-annual. The initial guess for each bond is 4%.
<br>

The prices of the bonds at the actual spot rate of 5% and the initial guess of 4% are calculated and shown in the following table.


<br>

|Bond|Price At 5%|Price At 4%|
|----|-----------| ----------|
|&nbsp;&nbsp;&nbsp;**six-month zero coupon**|&emsp;&emsp;**\$97.53**|&emsp;&emsp;**\$98.02**|
|&nbsp;&nbsp;&nbsp;**one-year zero coupon**|&emsp;&emsp;**\$95.12**|&emsp;&emsp;**\$96.08**|
|&nbsp;&nbsp;&nbsp;**one-year coupon rate 5**|&emsp;&emsp;**\$99.94**|&emsp;&emsp;**\$100.93**|

<br>

The pricing errors are scaled by the derivatives evaluated at the initial guess of 4%.  The next guess is augmented by the scaled pricing errors.

<br>

|Bond|Pricing Error|Derivative|Delta Guess|Updated Guess|
|----|-----------| ---------- |-----------|-------------|
|&nbsp;&nbsp;&nbsp;**six-month zero coupon**|&emsp;&emsp;**-\$0.49**|&emsp;&emsp;**-49.00**|&emsp;&emsp;**1.0%**|&emsp;&emsp;**5.0%**|
|&nbsp;&nbsp;&nbsp;**one-year zero coupon**|&emsp;&emsp;**-\$0.96**|&emsp;&emsp;**-96.88**|&emsp;&emsp;**1.0%**|&emsp;&emsp;**5.0%**|
|&nbsp;&nbsp;&nbsp;**one-year coupon rate 5**|&emsp;&emsp;**-\$0.99**|&emsp;&emsp;**-99.71**|&emsp;&emsp;**1.0%**|&emsp;&emsp;**5.0%**|

<br>

For all three bonds a solution is reached within one iteration.

## <font color='green'>Application: Make the initial guess 7% and calculate two new guesses for the following bonds:</font>


<div style="
    border-left: 12px solid green;
    line-height: 1.5;
    padding: 15px">
<br>



|Maturity|Coupon|Spot Rate|
|-------|-------|---------|
|&nbsp;&nbsp;&nbsp;Six Months|&nbsp;&nbsp;&nbsp;0|&emsp;4%|
|&nbsp;&nbsp;&nbsp;One Year|&nbsp;&nbsp;&nbsp;0|&emsp;5%|
|&nbsp;&nbsp;&nbsp;One Year|&nbsp;&nbsp;&nbsp;5|






 see [Chapter Six Hints: Make the initial quess 7%](https://colab.research.google.com/drive/1ZMO2gJ56kCFUXS4zUhljrW5Cj6GESuKp), and check the [expected results here](https://colab.research.google.com/drive/1VJzd020F3lfs-1cP2EAS2fBSKazIPYOC#scrollTo=vnPEV819ilWL).

</div>

## <font color='green'>Take a deeper dive with AI</font>


#### Some suggestions to get you started with Gemini.

1.   **What's the relation between the yield to maturity and the rate return earned from holding a bond until it matures?**

2.   **Is it OK to use the Newton-Raphson technique to solve for the yield to maturity of a Treasury bill?**

3.  **Can the Newton-Raphson technique be used to solve for the yield to maturity with both continuous and discrete compounding?** 

#### [Copy and paste the questions here](https://gemini.google.com)







