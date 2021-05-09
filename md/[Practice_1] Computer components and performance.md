# Computer components and performance

<u>Note: Some exercises I mark (*) because I'm not sure :sob:, I will update later</u>

## Exercise 1

![](https://github.com/nghminh163/USTH-ICT1.3/blob/main/assets/ex1-1.png?raw=true)

In the lecture summary sheet, we have 2 formula are:
$$
\text{CPI} = \frac{\text{Clock Cycles}}{\text{Instruction Count}} = \sum_{i=1}^{n} (\text{CPI}_i \times \frac{\text{Instruction Count}_i}{\text{Instruction Count}} )
$$
and
$$
\text{MIPS} = \frac{\text{instruction count}}{\text{execution time} \times 10^6} = \frac{\text{clock rate}}{\text{CPI} \times 10^6}
$$
From question, we have:

- Clock rate: 200MHz
- Instruction Count: 100 instructions
- And data in table :disappointed_relieved: with CPI and relative frequency

So,apply the above formula the overall CPI can be computed as:
$$
\text{CPI}_\text{average} = \sum_{i=1}^{n} (\text{CPI}_i \times \frac{\text{Instruction Count}_i}{\text{Instruction Count}} ) = \frac{1 \times 38 + 3 \times 15 + 4 \times 42 + 5 \times 5}{100} = 2.76
$$
and MIPS can be computed as:
$$
\text{MIPS}_\text{average} = \frac{\text{clock rate}}{\text{CPI}_\text{average} \times 10^6} = \frac{200 \times 10^6}{2.76 \times 10^6} = 70.24
$$


## Exercise 2

![](https://github.com/nghminh163/USTH-ICT1.3/blob/main/assets/ex1-2.png?raw=true)

The overall CPI of machine B can be computed as:
$$
\text{CPI}_\text{a_average} = \sum_{i=1}^{n} (\text{CPI}_i \times \frac{\text{Instruction Count}_i}{\text{Instruction Count}} ) = \frac{1 \times 35 + 2 \times 30 + 3 \times 15 + 5 \times 20}{100} = 2.4
$$
and MIPS can be computed as:
$$
\text{MIPS}_\text{b} = \frac{\text{clock rate}}{\text{CPI}_\text{average} \times 10^6} = \frac{400 \times 10^6}{2.4 \times 10^6} = 166.67 
$$

So, MISP of A less than MISP of B

## Exercise 3 (*)

![](https://github.com/nghminh163/USTH-ICT1.3/blob/main/assets/ex1-3.png?raw=true)

As mentioned above, the only limitation is the time it takes to send electronic signals from one edge of chip to the other. Because of the chip has disk-shaped, so, distance between 2 edges is diameter of a round chip. 

The chip has a clock rate of $1GHz$, so clock cycles is $1ns$ = $10^{-9}s$

Here, we can see the problem mentioned that electronic signals has the velocity is $300000 km/s$, so, the diameter of a round chip (or the travel distance between 2 edge, or the travel distance in $1ns$) is $s = v \times t = 300000 km/s \times 10^{-9}s = 0.0003 km = 300mm $ 

In the second case, the chip has a clock rate of $1THz = 10^{12}Hz $, so clock cycle is $10^{-12}s$, so, the diameter of a round chip (or the travel distance between 2 edge, or the travel distance in $1ns$) is $s = v \times t = 300000 km/s \times 10^{-12}s = 0.0000003 km = 0.3 mm $ 



**The diameter of this chip is too small. It is not feasible in near future**

**<u>*MAYBE WRONG*</u>**

In my viewpoint, **I think a chip is feasible** 

Imagine, we have a disk-shaped chip and a diameter is $0.3mm = 0.3 \times 10^6nm$, so, the area of the chip is $ (\frac{d}{2})^2 \times \pi = (\frac{0.3 \times 10^6}{2})^2 \times \pi \ nm^2$

In 2020, the smallest transistors is $5nm$, so we can calculate the number of transistors by $\frac{\text{Area of Chip}}{\text{Area of transistor}}$. Here we have the number of transistors is  $28 \times 10^8$ transistors. Now, by Moore's law we can have $50 \times 10^9$ transistors, so $28 \times 10^8$ transistors in a chip is possible

You can refer bellow graph

![Moore's_Law_Transistor_Count_1970-2020.png](https://github.com/nghminh163/USTH-ICT1.3/blob/main/assets/Moore's_Law_Transistor_Count_1970-2020.png?raw=true)

<center>Graph shows the number of transitors of microchips from 1970 to 2020 (Moore's Law)</center>

*Note*: You can find Moore's Law in Zero Lecture (I call 0 because lecturer called it `0-Introduction.pdf`) 



## Exercise 4

![](https://github.com/nghminh163/USTH-ICT1.3/blob/main/assets/ex1-4.png?raw=true)

In lecture 1 summary, I mentioned
$$
\text{CPU execution time}_{\text{ for a program}} = \text{CPU clock cycle}_{\text{ for a program}} \times \text{Clock cycle time}
$$
and 
$$
\text{CPU execution time}_{\text{ for a program}} = \frac{\text{CPU clock cycle}_{\text{ for a program}}} {\text{Clock rate}}
$$
Let CPU clock cycle is $X$ and the clock rate we must machine B have is $Y$, so

On computer A, we have 
$$
50s = \frac{X}{5 \times 10^8}
$$
On computer B, we have 
$$
20s = \frac{2.5 \times \text{X}}{Y}
$$
Now, we have
$$
\frac{X}{5 \times 10^8} : \frac{2.5 \times \text{X}}{Y} = \frac{50s}{20s} = \frac{Y}{5 \times 10^8 \times 2.5} \Longrightarrow \text{Y} = 3.125 \times 10^9 Hz = 3125Mhz
$$


## Exercise 5

![](https://github.com/nghminh163/USTH-ICT1.3/blob/main/assets/ex1-5.png?raw=true)

In lecture 1 summary, I mentioned
$$
\text{CPU time} =  \text{Instruction count} \times \text{CPI} \times \text{Clock cycle time}
$$
Assume that Instruction count is $10^9$, so

On machine A, we have **clock cycle time** is $50ns$ and **CPI** is 4.0, so CPU time is
$$
\text{CPU time}_A =  10^9 \times 4.0 \times 50 \times 10^{-9} = 200s
$$
On machine B, we have **clock cycle time** is $65ns$ and **CPI** is 2.5, so CPU time is
$$
\text{CPU time}_B =  10^9 \times 2.5 \times 65 \times 10^{-9} = 162.5s
$$
So, the machine B is faster and faster than $\frac{\text{CPU time}_A}{\text{CPU time}_B} = \frac{16}{13} = 1.23$ times



## Exercise 6

![](https://github.com/nghminh163/USTH-ICT1.3/blob/main/assets/ex1-6.png?raw=true)

a) First of all, we have
$$
\text{CPU Time} = \frac{\text{Instructions Count} \times \text{CPI}}{\text{Clock rate}}
$$
So, 
$$
\frac{\text{Instructions Count}}{\text{CPU Time}} = \frac{\text{Clock rate}}{\text{CPI}}
$$
Now, we notice that $\text{IPS} = \frac{\text{Instructions Count}}{\text{CPU Time}}$, so $\text{IPS}= \frac{\text{Clock rate}}{\text{CPI}} $

We have,
$$
\text{IPS}_\text{P1} = \frac{\text{Clock rate}_1}{\text{CPI}_1} = \frac{3\text{GHz}}{1.5} = 2 \times 10^9
$$

$$
\text{IPS}_\text{P2} = \frac{\text{Clock rate}_2}{\text{CPI}_2} = \frac{2.5\text{GHz}}{1} = 2.5 \times 10^9
$$

$$
\text{IPS}_\text{P3} = \frac{\text{Clock rate}_3}{\text{CPI}_3} = \frac{4\text{GHz}}{2.2} = 1.82 \times 10^9
$$

So, processor 2 has the highest performance in instructions per second

b) Here, we have CPU time = 10 seconds, and we have $\text{instructions} = \text{IPS} \times \text{CPU time}$

Also, we have $\text{CPU Time} = \frac{\text{clock cycles}}{\text{clock rate}}$, so $\text{Clock cycles} = \text{CPU Time} \times \text{Clock rate}$

- For processor 1
  $$
  \text{instructions}_1 = \text{IPS}_1 \times \text{CPU time}_1 = 2 \times 10^9 \times 10 = 2 \times 10^{10}
  $$

$$
\text{Clock cycles}_1 = \text{CPU Time}_1 \times \text{Clock rate}_1 = 10 \times 3 \text{GHz} = 10 \times 3 \times 10^9 = 3 \times 10^{10}
$$



- For processor 2
  $$
  \text{instructions}_2 = \text{IPS}_2 \times \text{CPU time}_2 = 2.5 \times 10^9 \times 10 = 2.5 \times 10^{10}
  $$

$$
\text{Clock cycles}_2 = \text{CPU Time}_2 \times \text{Clock rate}_2 = 10 \times 2.5 \text{GHz} = 10 \times 2.5 \times 10^9 = 2.5 \times 10^{10}
$$



- For processor 3
  $$
  \text{instructions}_3 = \text{IPS}_3 \times \text{CPU time}_3 = 1.82 \times 10^9 \times 10 = 1.82 \times 10^{10}
  $$

$$
\text{Clock cycles}_3 = \text{CPU Time}_3 \times \text{Clock rate}_3 = 10 \times 4 \text{GHz} = 10 \times 4 \times 10^9 = 4 \times 10^{10}
$$



c) First of all, we have that, 
$$
\text{Execute time} = \frac{\text{clock cycles}}{\text{clock rate}}
$$
also $\text{Clock cycles} = \text{Instructions} \times \text{CPI}$

Therefore, 
$$
\text{Execute time} = \frac{\text{Instructions} \times \text{CPI}}{\text{clock rate}}
$$
Now, if we want to find new clock rate such that
$$
\text{Execute time}_{\text{new}} = 0.7 \times \text{Execute time}_{\text{old}}
$$
so, 
$$
\frac{\text{Instructions}_{\text{new}} \times \text{CPI}_{\text{new}}}{\text{clock rate}_{\text{new}}} = 0.7 \times \frac{\text{Instructions}_{\text{old}} \times \text{CPI}_{\text{old}}}{\text{clock rate}_{\text{old}}}
$$
But, $\text{Instructions}_{\text{new}} = \text{Instructions}_{\text{old}}$, so
$$
\frac{\text{CPI}_{\text{new}}}{\text{clock rate}_{\text{new}}} = 0.7 \times \frac{\text{CPI}_{\text{old}}}{\text{clock rate}_{\text{old}}}
$$
Now, we have $\text{CPI}_{\text{new}} = 1.2 \times \text{CPI}_{\text{old}}$, so
$$
\frac{1.2}{\text{clock rate}_{\text{new}}} = 0.7 \times \frac{1}{\text{clock rate}_{\text{old}}}
$$
and
$$
\text{clock rate}_{\text{new}} = \frac{1.2}{0.7} \times \text{clock rate}_{\text{old}} = 1.71 \times \text{clock rate}_{\text{old}}
$$
So, the clock rate must increase by apprx 71%



## Exercise 7

![](https://github.com/nghminh163/USTH-ICT1.3/blob/main/assets/ex1-7.png?raw=true)

Firstly, we have
$$
\text{CPU Time} = \frac{\text{clock cycles}}{\text{clock rate}}
$$
But, in first lecture, they mention since we know the clock rates of each processor, we need to find out how many clock cycles it takes each processor to execute program by below formula
$$
\text{CPU clock cycles} =  \sum_{i=1}^{n} (\text{CPI}_i \times \text{Instruction Count}_i )
$$
We also calculate, $10^6 \times 10\% = 10^5$ instructions of class A;  $10^6 \times 20\% = 2\times 10^5$ instructions of class B; $10^6 \times 50\% = 5 \times 10^5$ instructions of class C; $10^6 \times 20\% = 2\times 10^5$ instructions of class D

So, 
$$
\text{CPU clock cycles}_1 = (1\times 10^5) + (2\times 2\times 10^5) + (3\times 5\times 10^5) = 2.6 \times 10^6
$$
and
$$
\text{CPU clock cycles}_2 = (2\times 10^5) + (2\times 2\times 10^5) + (2\times 5\times 10^5) = 2 \times 10^6
$$
Hence, 
$$
\text{CPU Time}_1 = \frac{2.6\times 10^6}{2.5 \text{GHz}} = 1.04s
$$
and
$$
\text{CPU Time}_2 = \frac{2\times 10^6}{3 \text{GHz}} = 0.667s
$$
Therefore, processor 2 is faster

a)
$$
\text{CPI}_1 = \frac{\text{Clock Cycles}_1}{\text{Total number of instructions}} = \frac{2.6\times 10^6}{10^6} = 2.6
$$

$$
\text{CPI}_2 = \frac{\text{Clock Cycles}_2}{\text{Total number of instructions}} = \frac{2\times 10^6}{10^6} = 2
$$

b) We have
$$
\text{CPU clock cycles}_1 = 2.6 \times 10^6
$$
and
$$
\text{CPU clock cycles}_2 = 2 \times 10^6
$$


## Exercise 8

![](https://github.com/nghminh163/USTH-ICT1.3/blob/main/assets/ex1-8.png?raw=true)

a) Recall that
$$
\text{CPU time} =  \text{Instruction count} \times \text{CPI} \times \text{Clock cycle time}
$$
thus
$$
\text{CPI} = \frac{\text{CPU time}}{\text{Instruction count}\times \text{Clock cycle time}}
$$
So,
$$
\text{CPI}_{\text{a}} = \frac{\text{CPU time}_{\text{a}}}{\text{Instruction count}_{\text{a}}\times \text{Clock cycle time}} = \frac{1.1s}{10^9 \times 10^{-9}s} = 1.1
$$

$$
\text{CPI}_{\text{b}} = \frac{\text{CPU time}_{\text{b}}}{\text{Instruction count}_{\text{b}}\times \text{Clock cycle time}} = \frac{1.5s}{1.2\times10^9 \times 10^{-9}s} = 1.25
$$



b) Recall that
$$
\text{Execute time} = \text{CPU Time} = \frac{\text{Instructions Count} \times \text{CPI}}{\text{Clock rate}}
$$
So, if execute times in both cases are the same,
$$
\text{Execute time}_1 = \text{Execute time}_2
$$
which yields
$$
\frac{\text{Instructions Count}_1 \times \text{CPI}_1}{\text{Clock rate}_1} = \frac{\text{Instructions Count}_2 \times \text{CPI}_2}{\text{Clock rate}_2}
$$
Therefore, after rearranging
$$
\text{clock rate}_1 =\frac{\text{Instructions Count}_1 \times \text{CPI}_1}{\text{Instructions Count}_1 \times \text{CPI}_2} \times \text{clock rate}_2 = \frac{10^9 \times 1.1}{1.2 \times 10^9 \times 1.25} \times \text{clock rate}_2
$$
So, 
$$
\text{clock rate}_1 = 0.73 \times \text{clock rate}_2
$$
So, the clock rate of processor 1 is actually apprx 27% slower than the clock rate of processor 2



c) We have
$$
\text{CPU time}_{\text{c}} =  \text{Instruction count}_{\text{c}} \times \text{CPI}_{\text{c}} \times \text{Clock cycle time} = 6 \times 10^8 \times 1.1 \times 10^{-9} = 0.66s
$$
So,
$$
\frac{\text{performance}_\text{C}}{\text{performance}_\text{A}} = \frac{\text{CPU Time}_\text{A}}{\text{CPU Time}_\text{C}} = \frac{1.1s}{0.66s} = 1.67
$$

$$
\frac{\text{performance}_\text{C}}{\text{performance}_\text{B}} = \frac{\text{CPU Time}_\text{B}}{\text{CPU Time}_\text{C}} = \frac{1.5s}{0.66s} = 2.27
$$

So, C is faster than A apprx 1.67 times and faster than B apprx 2.27 times



## Exercise 9

![](https://github.com/nghminh163/USTH-ICT1.3/blob/main/assets/ex1-9.png?raw=true)

a) Recall that
$$
\text{Clock cycle} = \text{Number of instruction} \times \text{CPI}
$$
But, we have 3 different types of instructions, so
$$
\text{Clock cycle} =  \sum_{i=1}^{3} (\text{CPI}_i \times \text{Instruction Count}_i )
$$
So, for one processor, we have
$$
\text{Clock cycle} = (2.56 \times 10^9) \times 1 + (1.28 \times 10^9) \times 12 + (256 \times 10^6) \times 5 = 1.92 \times 10^{10}
$$
And
$$
\text{Execute Time} = \frac{\text{Clock cycles}}{\text{Clock rate}} = \frac{1.92 \times 10^{10}}{2 \times 10^9} = 9.6s
$$
Let $p >1$ be the number of processor. Then we have
$$
\text{Clock cycle}_p = \frac{2.56 \times 10^9}{0.7p} \times 1 + \frac{1.28 \times 10^9}{0.7p}\times 12 + (256 \times 10^6) \times 5 = \frac{2.56 \times 10^{10}}{p} + 1.28 \times 10^9
$$
So, 
$$
\text{Execute time}_p = \frac{\text{Clock cycles}_p}{\text{Clock rate}} = \frac{\frac{2.56 \times 10^{10}}{p} + 1.28 \times 10^9}{2 \times 10^9} = \frac{12.8}{p} + 0.64
$$
Now, we have below table

|            p            |  1   |  2   |  4   |  8   |
| :---------------------: | :--: | :--: | :--: | :--: |
| execute time in seconds | 9.6  | 7.04 | 3.84 | 2.24 |
|        speed-up         |  1   | 1.36 | 2.5  | 4.29 |



b) So, for one processor, we have
$$
\text{Clock cycle} = (2.56 \times 10^9) \times 2 + (1.28 \times 10^9) \times 12 + (256 \times 10^6) \times 5 = 2.176 \times 10^{10}
$$
And
$$
\text{Execute Time} = \frac{\text{Clock cycles}}{\text{Clock rate}} = \frac{2.176 \times 10^{10}}{2 \times 10^9} = 10.88s
$$
Let $p >1$ be the number of processor. Then we have
$$
\text{Clock cycle}_p = \frac{2.56 \times 10^9}{0.7p} \times 2 + \frac{1.28 \times 10^9}{0.7p}\times 12 + (256 \times 10^6) \times 5 = \frac{2.93 \times 10^{10}}{p} + 1.28 \times 10^9
$$
So, 
$$
\text{Execute time}_p = \frac{\text{Clock cycles}_p}{\text{Clock rate}} = \frac{\frac{2.93 \times 10^{10}}{p} + 1.28 \times 10^9}{2 \times 10^9} = \frac{14.65}{p} + 0.64
$$
Now, we have below table

|            p            |   1   |   2   |   4    |  8   |
| :---------------------: | :---: | :---: | :----: | :--: |
| execute time in seconds | 10.88 | 7.965 | 4.3025 | 2.47 |
|        speed-up         | 1.13  | 1.13  |  1.12  | 1.1  |



c) This mean that the execution time of one processor will be the same as the execution time of four processors, so we have $\text{execution time}_{\text{new}} = 3.84s$

But, we have $\text{Execute Time} = \frac{\text{Clock cycles}}{\text{Clock rate}}$, thus $3.84s = \frac{\text{Clock cycles}_{\text{new}}}{2\text{GHz}}$, so $\text{Clock cycles}_{\text{new}}= 2 \times 10^9 \times 3.84 = 7.68 \times 10^9 $

Furthermore,

$\text{Clock cycles}_{\text{new}}= (2.56 \times 10^9) \times 1 + (1.28 \times 10^9) \times \text{CPI}_{2, \text{new}} + (256 \times 10^6) \times 5$

So, after simplifying and plugging in the new number of clock cycles
$$
3.84 \times 10^9 + 1.28 \times 10^9 \times \text{CPI}_{2, \text{new}} = 7.68 \times 10^9
$$
Therefore,
$$
\text{CPI}_{2, \text{new}} = \frac{7.68 \times 10^9 - 3.84 \times 10^9}{1.28 \times 10^9} = 3
$$


## Exercise 10

![](https://github.com/nghminh163/USTH-ICT1.3/blob/main/assets/ex1-10.png?raw=true)

a) The change of clock rate affects the clock cycle time, so
$$
\text{cycle time } = \frac{1}{\text{clock rate}} = \frac{1}{4\text{GHz}} = 0.25 \times 10^{-9}s
$$
We also have
$$
\text{execute time} = \text{clock cycles} \times \text{cycle time}
$$
so, 
$$
\text{clock cycles} = \frac{\text{execute time}}{\text{cycle time}} = \frac{700}{0.25 \times 10^{-9}} = 2.8 \times 10^{12}
$$
The new number of instructions is 