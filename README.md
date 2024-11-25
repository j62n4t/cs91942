java c
SP   and RO
Problem   1A company is considering producing a chemical C which can be manufactured with either process   II or process III, both of   which use as raw material chemical B.    B   can be purchased   from   another   company or manufactured with process I which uses A   as   a   raw   material.      Process   II   and   process   III are exclusive, i.e. at most one of   them can be built. There are five possible outcomes of   demand   and   selling   price   combination   for   chemical   C.   The   probability   of each   scenario,   as   well   as   the   corresponding demand and selling price are listed below:
   
Demand   of   C   (million   tons)
Selling Price ($/ton)Probability
Scenario   1
5
2000
10%
Scenario 2
8
1900
20%
Scenario   3
10
1800
40%
Scenario 4
12
1600
20%
Scenario   5
15
1000
10%
Given the specifications, formulate a two-stage stochastic MILP model   to maximize the   expected   profit   and solve it with GAMS/Pyomo to   determine:
a)      Which process to build and what would be the corresponding capacity?
b)      How to obtain chemical B and how much product C   should be   sold   in   each   scenario?
c)      What   would   be   the   “value   of   perfect   information” for   this   problem?
Hints:
a)          Facility    selection    (binary      0-1      decisions)      and      capacity      (continuous      decisions)      are      first-stage      decisions   (independent    of    demand/price    realization);    purchase,      production      and      sale      are      second-stage      decisions   (dependent on demand/price realization).
b)          The production is each scenario should not   exceed the   capacity, which   is   scenario   independent.
c)          If production/sale   exceeds   the   demand   for   a   certain   scenario,   unsold   product   cannot   generate   any   revenue   (but   incurs   production   cost).   The   sale   amount   should   not   exceed   the   demand   and   should   not   exceed   the   available/production amount.
Data:
Investment Costs
Fixed capital cost (million $)                                        Variable capital cost ($/ton   of   product)
Process   I
100250
Process   II
150400
Process III
200550
Operating Costs
Variable   operating/production   cost   ($/ton   of   product)


Process I                                       100
Process II                                       150
Process III                                                       200
Prices:          A:               $250/ton
B:               $450/ton




Conversions:
Process      I               90% of   A   to   B
Process   II                  82% of   B to   C
Process   III              95% of   B   to   C


Maximum supply of   A:      16 million tons
Problem 2Consider the newsboy problem: Newspaper unit   cost   is   $0.60/piece,   sel代 写SP and ROSQL
代做程序编程语言ling price   is   $1.50/piece;   the newsboy needs to order   the newspapers tonight, before knowing tomorrow’s demand. Assume   there   are   100   possible   outcomes   of demand,   ranging   from    1   piece   to    100   pieces   with   uniform   probability   distribution.   In   other   words,   there   are   100   scenarios   for   demand   and   1%   chance   for   each   scenario   (i.e.   1% chance for the   scenario of 1   piece,   1%   chance   for   the   scenario   of   2   pieces,   1% chance for the scenario of   3 pieces,   …   ,   1% chance for   the scenario of   99 pieces, and   1% chance   for   the   scenario   of   100   pieces).   The   objective   is   maximizing   the   expected   profit   over   these   100   demand scenarios while managing the risk.Formulate   the   following   four   risk   management   models   and   solve   them   with   GAMS/Pyomo   to   determine the optimal number of   newspapers that   should be ordered under each risk management strategy.
a)      Maximizing the mean/expected profit (i.e. risk-neural)
b)      Optimizing mean-variance (using equal weight for expectation and variance, i.e.   ρ   =-1)
c)      Minimizing probabilistic financial risk for the threshold of   0 profit (i.e.   Ω =   0)
d)      Minimizing downside risk for the threshold of   0 profit (i.e. Ω =   0)
e)       Minimizing CVaR for the 20% “loss” quantile (i.e.   α =   20%   for the   “low” profit)Hints:   The   example   in   lecture   slides   is   for   cost minimization, while   this problem   is   for profit   maximization.   Please   make sure to revise the model formulations accordingly to account for the “maximization” problem for low profit risk   (instead of   minimizing “high cost” risk).
Problem 3
Derive the robust counterpart for the following problem:
max    10x1   +   5x2   x1   ,   x2
s.t.       (6   +   u1 )x1   +   (2   +   u2   )x2      ≤   80,       ∀   (u1,   u2   )   ∈   U
a)       U   is   a ellipsoidal   uncertainty   set:    U =   {(u1   ,    u2   )   :          ≤1}.
b)       U   is a box uncertainty   set:    U =   {(u1,    u2   )   :      u1       ≤1,      u2         ≤1}.
Problem 4




Consider the following two-stage adaptive robust optimization (ARO) problem:


0.5x1   +100x2    +   max   u∈Ux1      ≤ 200x2            y1   + y2      ≤   x1   y1    ≤   u1
y2      ≤   u2
(−6y1   −   5y2   )


x1,   y1,   y2      ≥   0,   x2      ∈   {0,1}
where uncertainty set    U   =   
Use linear decision rule to solve the two-stage ARO problem.
Problem   5
Consider the following robust optimization problem with implementation errors.
mn   Δx(m)U(x)   f   (x   +   Δx)
where   f   is   a   nonconvex   function   defined   by,
a)       Find the robust optimal   solution x*   when    U = {Δx   −0.5 ≤ Δx ≤ 0.5   }.
b)      Find the robust optimal   solution x*   when    U = {Δx   −1.5 ≤ Δx ≤1.5   }.





         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
