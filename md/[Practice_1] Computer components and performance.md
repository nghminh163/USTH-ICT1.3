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
\text{MIPS}_\text{average} = \frac{\text{clock rate}}{\text{CPI}_\text{average} \times 10^6} = \frac{200 \times 10^6}{2.4 \times 10^6} = 83.37
$$



## Exercise 3 (*)

![](https://github.com/nghminh163/USTH-ICT1.3/blob/main/assets/ex1-3.png?raw=true)

As mentioned above, the only limitation is the time it takes to send electronic signals from one edge of chip to the other. Because of the chip has disk-shaped, so, distance between 2 edges is diameter of a round chip. 

The chip has a clock rate of $1GHz$, so clock cycles is $1ns$ = $10^{-9}s$

Here, we can see the problem mentioned that electronic signals has the velocity is $300000 km/s$, so, the diameter of a round chip (or the travel distance between 2 edge, or the travel distance in $1ns$) is $s = v \times t = 300000 km/s \times 10^{-9}s = 0.0003 km = 300mm $ 

In the second case, the chip has a clock rate of $1THz = 10^{12}Hz $, so clock cycle is $10^{-12}s$, so, the diameter of a round chip (or the travel distance between 2 edge, or the travel distance in $1ns$) is $s = v \times t = 300000 km/s \times 10^{-12}s = 0.0000003 km = 0.3 mm $ 

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