# Yields To Maturity

**Chapter Six of the volume Basic Concepts of Fixed Income**

**Key Topics Covered**

* **What is the yield to maturity and how is it calculated**  
  * Define the yield to maturity   
  * For bonds with multiple payment dates, no simple formula
  * Using Newton-Raphson method to find a value
  * Limitations of yeild to maturity 
 
* **Python concepts:**  
  * NumPy arrays   
  * Pandas 
  * Custom modules.  
    * <font color='green'>accrued_interest</font>  
    * <font color='green'>bond_pay_data</font>  
    * <font color='green'>create_payoff_matrix</font>
    * <font color='green'>one_y_axis</font>

    

## **Background**

This chapter's examples and discussions rely on the **Pandas** and **NumPy** libraries.

* **Pandas** is introduced in [*A Quick Introduction to Pandas*](https://patrickjhess.github.io/Introduction-To-Python-For-Financial-Python/An_Introduction_To_Pandas.html#a-quick-introduction-to-pandas).  
* **NumPy** is introduced in [*A Quick Introduction to NumPy*](https://patrickjhess.github.io/Introduction-To-Python-For-Financial-Python/An_Introduction_To_NumPy.html#a-quick-introduction-to-numpy). 
* The <font color='green'>accrued_interest</font> function is imported from [Chapter Two](https://patrickjhess.github.io/Vol-3-Chap-2-Chap-3/Chapter_Two_Highlights.html#accrued-interest)
* The <font color='green'>bond_pay_data</font> function is imported from [Chapter Three](https://patrickjhess.github.io/Vol-3-Chap-2-Chap-3/Chapter_Three_Highlights.html)  
* The <font color='green'>create_payoff_matrix</font> function is imported from [Chapter Four](https://patrickjhess.github.io/Vol-3-Chap-4/Creating_The_Payoff_Matrix.html#creating-the-payoff-matrix)  
* The <font color='green'>one_y_axis</font> function is imported from [Chapter One](https://patrickjhess.github.io/Vol-3-Chap-1/Calculating_And_Graphing_The_Term_Structure_Of_Interest_Rates.html#graphing-the-spot-and-forward-rates-for-september-15-2022)  
* Additional relevant Python concepts can be found in the introductory volume, [*Background Material: An Introduction to Python for Financial Python*](https://patrickjhess.github.io/Introduction-To-Python-For-Financial-Python/intro.html), that relate to this and other chapters of *Basic Concepts of Fixed Income*.

**The chapter includes four  sections:**

1. *What Is The Yield To Maturity and Why It Matters*
   *  defines and demonstrates how yield to maturity is calculated from bond prices.
   *  an application applying the iterative search procedure.
   *  an invitation to use AI to develop a deeper understnading about yield to maturity. 
2. The  Jupyter notebook *Calculating Yields To Maturity*
   * develops three new functions:
        * <font color='green'>bond_pv</font> calculating the present value of a bond
        * <font color='green'>single_newton_raphson</font> finds the root of the present value function used to calculate yield to maturity
        * <font color='green'>calc_ytm</font> calulates the yield to maturity of bonds 
   * an exercise asking you to calculate the yields to maturity of three bonds
   * an invitation to use AI to expolre more concepts about yield to maturity.
3. *Summarizing The Results of Calculating Yields To Maturity* summarizes the uses of yield to maturity.  
4. *Functions Imported by Calculating Calculating Yield To Maturity*  describes the function imported from DropBox (*module_basic_concepts_fixed_income*).
```{tableofcontents}
```
