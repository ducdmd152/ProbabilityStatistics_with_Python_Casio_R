# Probability & Statistics with Python.

> **Discrete Uniform Distribution:**
> 
> 
> Bài toán:
> 
> ![Untitled](Probability%20&%20Statistics%20with%20Python%20b00163d7bc794beb80e267e598a7ff9f/Untitled.png)
> 
> Code:
> 
> ```
> import math
> print("input interval [a,b]")
> a = int(input("input a:"))
> b = int(input("input b:"))
> choice = int(input("Choose: 1,P(X<k)   2,P(X >= k) "))
> if choice == 1:
>     k = int(input("P(X<k) replace k:"))
>     prob = 1/(k-a)
>     mean = (a+b)/2
>     sd = math.sqrt(((b-a+1)**2-1)/12)
>     print(f'P(X<{k})={round(prob, 2)}, Mean: {mean}, Standard deviation: {sd}')
> else:
>     k = int(input("P(X>=k) replace k:"))
>     prob = 1 -(1 / (k - a))
>     mean = (a + b) / 2
>     sd = math.sqrt(((b - a + 1) ** 2 - 1) / 12)
>     print(f'P(X>={k})={round(prob, 2)}, Mean: {mean}, Standard deviation: {sd}')
> ```
> 
> Output:
> 
> ![Untitled](Probability%20&%20Statistics%20with%20Python%20b00163d7bc794beb80e267e598a7ff9f/Untitled%201.png)
> 

> **Binomial Distribution:**
> 
> 
> 1:
> 
> Bài toán:
> 
> ![Untitled](Probability%20&%20Statistics%20with%20Python%20b00163d7bc794beb80e267e598a7ff9f/Untitled%202.png)
> 
> Code:
> 
> ```
> n = int(input("Enter numbers of random experiment:"))
> p = float(input("Enter the probability:"))
> mean = n*p
> variance = n*p*(1-p)
> print("the mean and variance is:",mean,"and",variance,"respectively.")
> ```
> 
> Output:
> 
> ![Untitled](Probability%20&%20Statistics%20with%20Python%20b00163d7bc794beb80e267e598a7ff9f/Untitled%203.png)
> 
> 2:
> 
> Bài toán:
> 
> ![Untitled](Probability%20&%20Statistics%20with%20Python%20b00163d7bc794beb80e267e598a7ff9f/Untitled%204.png)
> 
> Code:
> 
> ```
> import math
> n = int(input("Enter numbers of random experiment:"))
> p = float(input("Enter the probability:"))
> x = int(input(f"Number of event in {n} random experiment:"))
> result = math.comb(n,x)*p**x*(1-p)**(n-x)
> print("The probability is:", round(result,4))
> ```
> 
> Output:
> 
> ![Untitled](Probability%20&%20Statistics%20with%20Python%20b00163d7bc794beb80e267e598a7ff9f/Untitled%205.png)
> 

> **Geometric Distribution:**
> 
> 
> Bài toán:
> 
> ![Untitled](Probability%20&%20Statistics%20with%20Python%20b00163d7bc794beb80e267e598a7ff9f/Untitled%206.png)
> 
> Code:
> 
> ```
> k = int(input("Number of the random experiment until having the event:"))
> p = float(input("Probability of the event:"))
> result = (1-p)**(k-1) * p
> print(f"The probability that the the event appear after {k} times is: {round(result,4)}")
> ```
> 
> Output:
> 
> ![Untitled](Probability%20&%20Statistics%20with%20Python%20b00163d7bc794beb80e267e598a7ff9f/Untitled%207.png)
> 
> - **Negative Binomial Distribution:**
>     
>     Bài toán:
>     
>     ![Untitled](Probability%20&%20Statistics%20with%20Python%20b00163d7bc794beb80e267e598a7ff9f/Untitled%208.png)
>     
>     Code:
>     
>     ```
>     import math
>     p = float(input("Probability of the event:"))
>     r = int(input("Number of events:"))
>     k = int(input(f"Number of the random experiment until having {r} event:"))
>     result = math.comb(k-1,r-1)*p**r*(1-p)**(k-r)
>     print(f"Probability that in the next {k} samples, there is {r} events is: {round(result,4)}")
>     ```
>     
>     Output:
>     
>     ![Untitled](Probability%20&%20Statistics%20with%20Python%20b00163d7bc794beb80e267e598a7ff9f/Untitled%209.png)
>     
>     - **Poisson Distribution:**
>     
>     Bài toán:
>     
>     ![Untitled](Probability%20&%20Statistics%20with%20Python%20b00163d7bc794beb80e267e598a7ff9f/Untitled%2010.png)
>     
>     Code:
>     
>     ```
>     import math
>     mean = float(input("Enter the mean:"))
>     n = int(input("Numbers of k:"))
>     ask = input("Relationship of k(or/and):")
>     if ask == "or":
>         result = 0
>         for i in range (0,n):
>             k = int(input("Enter k:"))
>             result = (math.exp(-mean)*mean**k)/math.factorial(k) + result
>     else:
>         result = 0
>         for i in range(0, n):
>             k = int(input("Enter k:"))
>             result = (math.exp(-mean) * mean ** k) / math.factorial(k) * result
>     print(result)
>     
>     ```
>     
>     Output:
>     
> 
> ![Untitled](Probability%20&%20Statistics%20with%20Python%20b00163d7bc794beb80e267e598a7ff9f/Untitled%2011.png)
> 

> **Continuous Uniform Distribution:**
> 
> 
> Bài toán:
> 
> ![Untitled](Probability%20&%20Statistics%20with%20Python%20b00163d7bc794beb80e267e598a7ff9f/Untitled%2012.png)
> 
> Code:
> 
> ```
> import math
> print("input interval [a,b] and x where a < b")
> a = int(input("input a:"))
> b = int(input("input b:"))
> x = int(input("input x:"))
> if a <= x <= b:
>     p = 1/(b-a)
> else:
>     p = 0
> mean = (a+b)/2
> sd = math.sqrt(((b-a)**2)/12)
> print(f"The probability is: {p}. The mean is: {mean}. The standard deviation is: {sd}")
> ```
> 
> Output:
> 
> ![Untitled](Probability%20&%20Statistics%20with%20Python%20b00163d7bc794beb80e267e598a7ff9f/Untitled%2013.png)
> 

> **Standard Normal Distribution:**
> 
> 
> Bài toán:
> 
> ![Untitled](Probability%20&%20Statistics%20with%20Python%20b00163d7bc794beb80e267e598a7ff9f/Untitled%2014.png)
> 
> Code:
> 
> ```
> from statistics import NormalDist
> mean = float(input("Enter your mean:"))
> sd = float(input("Enter your standard deviation:"))
> choice = int(input("Choose: 1, P(X < a) 2, P(X > a) 3,P(a < X < B)"))
> if choice == 1:
>     a = int(input("input a:"))
>     result = NormalDist(mu=mean, sigma=sd).cdf(a)
> elif choice == 2:
>     a = int(input("input a:"))
>     result = 1 - NormalDist(mu=mean, sigma=sd).cdf(a)
> else:
>     a = int(input("input a:"))
>     b = int(input("input b:"))
>     result = NormalDist(mu=mean, sigma=sd).cdf(b)- NormalDist(mu=mean, sigma=sd).cdf(a)
> print("The probability is:", result)
> ```
> 
> Output:
> 
> ![Untitled](Probability%20&%20Statistics%20with%20Python%20b00163d7bc794beb80e267e598a7ff9f/Untitled%2015.png)
> 

> **Central Limit Theorem:**
> 
> 
> Bài toán:
> 
> ![Untitled](Probability%20&%20Statistics%20with%20Python%20b00163d7bc794beb80e267e598a7ff9f/Untitled%2016.png)
> 
> Code:
> 
> ```
> import math
> from statistics import NormalDist
> mean = float(input("Enter your mean:"))
> sd = float(input("Enter your standard deviation:"))
> n = int(input("Enter your statistical sample number:"))
> choice = int(input("Choose: 1, P(X < a) 2, P(X > a)"))
> if choice == 1:
>     a = int(input("input a:"))
>     ssd = sd/math.sqrt(n) #sample standard deviation
>     result = NormalDist(mu=mean, sigma=ssd).cdf(a)
> elif choice == 2:
>     a = int(input("input a:"))
>     ssd = sd / math.sqrt(n)
>     result = 1 - NormalDist(mu=mean, sigma=ssd).cdf(a)
> print("The probability is:", result)
> ```
> 
> Output:
> 
> ![Untitled](Probability%20&%20Statistics%20with%20Python%20b00163d7bc794beb80e267e598a7ff9f/Untitled%2017.png)
>