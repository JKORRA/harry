# Assignment Harry

# 1

Before reading: Distance (D) : N(μ = 98, σ^2 = 16)

After reading: 100 distance + Gaussian Noise : N(0,4)

Where N stands for Normal distribution

## a

PDF PRIOR ?

We can write the PDF for a Normal Distribution as:

    PDF = ( 1 / (σ * √2*π) ) * ( e^(-(D-μ)^2 ) / ( 2*σ^2 ) ) = 

    = ( 1 / ( 4 * √2*π ) ) * ( e^-(D-98)^2 / 32 )

## b

Here we have the true distance as T

X = 100 -> instrument reads 100 + Gaussian Noise N(0,4)

So we need to define the normal distribution of X given T, since we have
the true distance fixed as T

At this point we want to know the probability of seeing a measure of 100
given that the distance is T:

    P(100|T)

We also have the noise that we have to take into account:

    N(0,4) -> N(T,4) where T is the true distance and the variance is 4

New data:

    X = 100
    Expectation = T
    σ^2 = 4

So we can write:

    PDF(100|T) = ( 1 / (σ * √2*π) ) * ( e^(-(X-T)^2 ) / ( 2*σ^2 ) ) = 

    = ( 1 / ( 2 * √2*π ) ) * ( e^-(100-T)^2 / 8 )

## c

PRIOR

    Expectation = μ = 98

    σ^2= 16

POSTERIOR

100 distanza + Gaussian Noise N(0,4):

    Expectation = μ = D

    σ^2 = 4

PDF(POSTERIOR|PRIOR) ?

We have to find the new mean (μ) and the new variance (σ^2).

To find the mean we have just simply to sum the mean of the prior with the mean of the posterior:

..........incompleto............

----------------------------------------------------------------------------------------------------

# 2

μ = 5.5 Owls for minute

## a

Probability for more than (7) owls in the next (1) minute

Seeing this kind of problem my first think is to use Poisson.

We have basically to compute the probability that more than 7 owls arrive.

    P(X>7)

Since we cannot compute it in this way, we can rewrite it in a more efficient way:

    1 - P(X<=7)

This is the same thing.

In extended form we have to compute this:

    1 - ( P(X=7) - P(X=6) - P(X=5) - P(X=4) - P(X=3) - P(X=2) - P(X=1) - P(X=0) )

For example to compute P(X=7) we do:
    
    μ = 5.5

    P(X=7) = (5.5^7 * e^-5.5) / 7! = 0,12

Once we have compute all of those we have to subtract the result to 1 and the result is:

    1 - P(X<=7) = 0,19

## b

Probability for more than (13) owls in the next (2) minutes

Also in this case we have to use Poisson, but now we have different data.

+ di 13 gufi in 2 min

11 media in 2 minuti

μ = 11 because the average for a minute is 5.5

We have basically to compute the probability that more than 13 owls arrive.

    P(X>13)

Since we cannot compute it in this way, we can rewrite it in a more efficient way:

    1 - P(X<=13)

This is the same thing.

In extended form we have to compute this:

    1 - (  P(X=13) -  P(X=12) -  P(X=11) -  P(X=10) -  P(X=9) -  P(X=8) - P(X=7) - P(X=6) - P(X=5) - P(X=4) - P(X=3) - P(X=2) - P(X=1) - P(X=0) )

For example to compute P(X=13) we do:
    
    μ = 11

    P(X=7) = (11^7 * e^-11) / 7! = 0,064

Once we have compute all of those we have to subtract the result to 1 and the result is:

    1 - P(X<=13) = 0,22

## c

Probability for more than (15) owls in the next (3) minutes

Also in this case we have to use Poisson, but now we have different data.

16.5 media in 3 minuti

μ = 16 because the average for a minute is 5.5

We have basically to compute the probability that more than 15 owls arrive.

    P(X>15)

Since we cannot compute it in this way, we can rewrite it in a more efficient way:

    1 - P(X<=15)

This is the same thing.

In extended form we have to compute this:

    1 - (  P(X=15) -P(X=14) - P(X=13) -  P(X=12) -  P(X=11) -  P(X=10) -  P(X=9) -  P(X=8) - P(X=7) - P(X=6) - P(X=5) - P(X=4) - P(X=3) - P(X=2) - P(X=1) - P(X=0) )

For example to compute P(X=13) we do:
    
    μ = 16,5

    P(X=7) = (16,5^7 * e^-16,5) / 7! = 0,004

Once we have compute all of those we have to subtract the result to 1 and the result is:

    1 - P(X<=15) = 0,54

----------------------------------------------------------------------------------------------------

# 3

The median of a Cumulative distribution function is M, s.t.

F(M) = 0.5 

find the median of X (in terms of distribution parameters)

## a

X = Uni(a,b)

            0                    x < a
    CDF= {  1                    x > b
            x-a / b-a            x(a,b)

Since the median (0.5) is between (a) and (b) we have to use the CDF = x-a / b-a 

    F(M): x-a / b-a = 0.5

    x-a = 0.5*(b-a)

    x = 0.5b - 0.5a + a

    x = 0.5b + 0.5a = (a+b)/2

## b

X = N(μ, σ^2)

        
CDF = (x-μ/σ)

        x-0.5

...........incompleto...............

----------------------------------------------------------------------------------------------------

# 4

N(2200, 52900) in a week

μ = 2200
σ^2 = 52900

X(i) are independent

## a

exceed 5000 in the next 2 weeks

    μ = 2200*2 = 4400
    σ^2 = 52900*2 = 105800

    N(4400, 105800)

    P(X>5000) = P( (X-4400)/325 > (5000-4400)/325 ) = P( Z > 600/325 ) = P( Z > 1,84 ) = 1 - P(Z <= 1,84) = 1 - 0,9671 = 0,0329 = 3,29%

## b

exceed 2000 in at least 2 of the next 3 weeks

So we can first compute that 1 week exceed 2000:

    P(X>2000) = P( (X-2200)/230 > (2000-2200)/230 ) = P( Z > -200/230) = P( Z > -0,8695 ) = P( Z < 0.8695 ) = 0,8051 (P)
    
    1 - P = 1 - 0,8051 = 0,1949 (1-P)

At this point we can use Poisson to compute

----------------------------------------------------------------------------------------------------

# 5

X = N(μ1, σ1^2)

Y = N(μ2, σ2^2)

Z = N(μ3, σ3^2)

## a

    A = X + Y = (μ1+μ2, σ1^2+σ2^2)

    Since X and Y are indipendent we can just make this opearation

## b

    B = 5X + 2

First we multiply

    = (5*μ1, 5^2*σ1^2) = (5*μ1, 25*σ1^2)        

Then we sum

    = (2 + 5*μ1, 25*σ1^2)

## c

----------------------------------------------------------------------------------------------------

# 6

----------------------------------------------------------------------------------------------------

# 7

We have 2 numbers -> X e Y

X: random number from 1 to 6

Y: ranodm number from 1 to X

## a

We have to determine the Joint Probability mass function of X and Y

P(X ∩ B) = P(A) * P(B|A)

P(A) = 1/6

P(B) = 1/X

P(A ∩ B) = 1/6 * 1/X = 1/6X

## b

Conditional Mass Function

P(X=j | Y=i) = 1/j -> è la probabilità condizionata dal primo lancio, se nel primo lancio è uscito
il numero (j) allora la probabilità del secondo è (1/j)

## c

They are NOT indipendent, since the Y probability is conditioned by X

----------------------------------------------------------------------------------------------------
