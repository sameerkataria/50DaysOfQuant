## Questions
### I am going to use various resources to come up with Practise questions

Q1: Two gamblers are playing a cpomg toss game. Gambler A has n+1 coins and gambler b has n fair coins. What is the Prob that A will have more heads than B if they flip all coins

Ans: 

One way to understand the situation above is this.
You can remove the first n coins from the equation. Given the random nature of the toss, it will only depend on the extra coin that A has.
So what is the prob that the last coin turns up heads i.e. 1/2

Other way is to do it by defining events 

$E{_1}$: A's n coins have more heads than B's n coins<br>
$E{_2}$: A's n coins has equal heads as B's n coins<br>
$E{_3}$: B's n coins have more heads than A's n coins<br>

$E{_1}$ and $E{_3}$ should have the same prob say $x$ due to symmetry <br>
$P(E{_1}) = P(E{_3}) = x$<br>
Assume $P(E{_2}) = y$ <br>
$2 \times x + y = 1$ <br>

For $E{_1}$, A will always have more heads on the n+1 toss. For $E{_3}$ the extreme case would be B has one more heads than A and in the last toss A gets a head. It still would not help our case. For $E{_2}$, the only case is when A turns up head on the n+1 toss and this is going to be with a probability of 1/2. 

So the Probability that A has more heads than B in n+1 toss is:

$x \times 1 + (1/2) \times y + 0 \times x$<br>
$x + (1/2) \times y = 0.5$<br>
Using the Total prob equation

Q2: Poker Questions
- Prob of four of a kind
- Prob of a full house
- Prob of Three of a kind

Ans:<br> 
<b>Four of a kind:<br></b>
For four of a kind we have to select from the 13 values i.e any card from 2 till ace. So that is going to be 13 choose 1: ${13 \choose 1}$. You also have to select all the suites and that can be done in ${4 \choose 4}$ ways<br>
Out of the 12 type of card left you can choose any value. That is ${12 \choose 1}$. Also for the card selected it can be of any suite. So that is going to be ${4 \choose 1}$.<br>
So the number of ways you can get a 4 of a kind is ${13 \choose 1} \times 1 \times {12 \choose 1} \times 4 $<br>
Total number of ways to select 5 cards out of 52 is ${52 \choose 5}$<br>
So Prob = $({13 \choose 1} \times 1 \times {12 \choose 1} \times 4 ) \div {52 \choose 5}$<br>
<b>Full house:<br></b>
For a full house three cards are of one values and two cards are of another value. So from 13 cards we have to select two values. This can be done in ${13 \choose 2}$ ways. From the two values selected one can be part of the three and one can be part of the two pair. This can be done in ${2!}$ factorial ways. <br>
For the first value, we have to choose three suites. This can be done in ${4 \choose 3}$ ways. Similarly for the second value we have to choose two suites. this can be done in ${4 \choose 2}$ ways. <br>
So Prob  = $({13 \choose 2} \times 2! \times {4 \choose 3} \times {4 \choose 2} ) \div {52 \choose 5}$<br>
<b>Three of a kind:<br></b>
For a three of a kind, three cards are of one values and two cards are of different values. So from 13 cards we have to select one value. This can be done in ${13 \choose 1}$ ways. These three cards are chosen from the 4 suites in ${4 \choose 3}$ ways. For the other two cards, they have to be of distinct value. This can be done in ${12 \choose 2}$ ways. For the two distinct cards they can be any of the four suites  i.e ${4 \choose 1}^2$<br>
So Prob  = $({13 \choose 1} \times {12 \choose 2} \times {4 \choose 3} \times {4 \choose 1}^2 ) \div {52 \choose 5}$<br>


Q3: You are given an urn with 100 balls (50 black and 50 white). You pick balls from urn one by one without replacements until all the balls are out. A black followed by a white or a white followed by a black is "a colour change". Calculate the expected number of colour-changes if the balls are being picked randomly from the urn.<br>
Ans: Let us define an event like this<br>
$A{_i}$: i_th ball and i+1_th ball is a color switch <br>

$A{_i}$ = 1 for a color switch<br>
$A{_i}$ = 0 for the same color<br>

So to understand $A{_i}$, the first ball can be black and the next one can be white or vice versa. 

$S = A_1 + A_2 + ..... +A_{99} $<br>
$E[S] = E[A_1] + E[A_2] + ..... +E[A_{99}] $ (distributive property of expectation)<br>
Each $A_i$ is identical in terms of prob-distribution and the expected value value of each $A_i$ will be same.<br>
It is easy for us to determine $E(A_1)$:<br>

$1 \times P(A_1 = 1) + 0 \times P(A_1 = 0)$<br>
$P(A_1 = 1)$ is black followed by white or white ball followed by black <br>
i.e. $\frac{50}{100} \times \frac{50}{99} \times 2$<br>
$1 \times \frac{50}{99} + 0 \times P(A_1 = 0) = \frac{50}{99}$<br>
Hence $S = A_1 + A_2 + ..... +A_{99} $<br> = $99 \times \frac{50}{99} = 50$

Note: $A_i$ 's are not independent, but since all the balls are drawn randomly, the probability-distribution is identical for each draw.