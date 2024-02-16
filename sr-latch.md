# SR Latch

> In sequential circuits, the present output depends on the present input as well as past output/outputs.

The past outputs are stored in memory.
<figure><img src=".gitbook/assets/sr-latch/sequential-circuit.png" alt=""><figcaption><p>Sequential Circuit</p></figcaption></figure>

A latch is a memory device that stores the data in the form of 0s and 1s. It is a bistable device, i.e., it has two stable states. It can store one bit of data. The stored data can be changed by applying the appropriate inputs.

The SR latch is a circuit with two cross-coupled NOR gates or two cross-coupled NAND gates, and two inputs S(for set) and R(for reset). The output of one gate is connected to the input of the other gate and vice versa. The output of the first gate is Q and the output of the second gate is Q'. 

## SR Latch using NOR gates

<figure><img src=".gitbook/assets/sr-latch/sr-latch.png" alt=""><figcaption><p>SR Latch</p></figcaption></figure>

The reset input will reset the latch to 0 and the set input will set the latch to 1.

Truth Table for NOR gate:
$$
\begin{array}{|cc|c|}
\hline
A & B & Y \\
\hline
0 & 0 & 1 \\
0 & 1 & 0 \\
1 & 0 & 0 \\
1 & 1 & 0 \\
\hline
\end{array}
$$

Case 1: When S=0 and R=1, the output Q=0 and Q'=1. This is the reset condition. The latch is reset to 0.
After the reset, if S=0 and R=0, the output Q=0 and Q'=1. The data is stored in the latch.

Case 2: When S=1 and R=0, the output Q=1 and Q'=0. This is the set condition. The latch is set to 1.
After the set, if S=0 and R=0, the output Q=1 and Q'=0. The data is stored in the latch.

Case 3: When S=1 and R=1, the output Q=0 and Q'=0. This is the invalid condition. The output is unpredictable.
After the invalid condition, if S=0 and R=0, the output Q=0 and Q'=1(if we start from reset condition) or Q=1 and Q'=0(if we start from set condition). Both the outputs are different and unpredictable.

So,
$$
\begin{array}{|cc|c|c|}
\hline
S & R & Q & Q' \\
\hline
0 & 0 & \text{Not changed} & \text{Not changed} \\
0 & 1 & 0 & 1 \\
1 & 0 & 1 & 0 \\
1 & 1 & \text{Invalid} & \text{Invalid} \\
\hline
\end{array}
$$

## SR Latch using NAND gates

For NAND gate, the truth table will be:
$$
\begin{array}{|cc|c|c|}
\hline
S & R & Q & Q' \\
\hline
0 & 0 & \text{Invalid} & \text{Invalid} \\
0 & 1 & 1 & 0 \\
1 & 0 & 0 & 1 \\
1 & 1 & \text{Not changed} & \text{Not changed} \\
\hline
\end{array}
$$

Q. Difference between latch and flip-flop?

A. Latch is level triggered and flip-flop is edge triggered. Latch is faster than flip-flop. Flip-flop is more reliable than latch. Flip-flop is used in synchronous circuits and latch is used in asynchronous circuits.

## Clock signal

The clock signal is used to synchronize the operation of the sequential circuits. The clock signal is a square wave signal. The clock signal is used to trigger the flip-flops. It is a periodic train of pulses which changes its states between the logic 1 and logic 0.
