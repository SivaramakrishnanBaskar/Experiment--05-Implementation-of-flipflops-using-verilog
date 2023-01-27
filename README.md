# Experiment--05-Implementation-of-flipflops-using-verilog

# AIM:
To implement all the flipflops using verilog and validating their functionality using their functional tables

# HARDWARE REQUIRED: –
PC, Cyclone II , USB flasher

# SOFTWARE REQUIRED:
Quartus prime

# THEORY

# SR Flip-Flop

SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.


This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of SR flip-flop.


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop. Present Inputs Present State Next State



By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.



The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)

# D Flip-Flop

D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.

This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of D flip-flop. image

image

Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D

image

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.

# JK Flip-Flop

JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure. image

This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs. The following table shows the state table of JK flip-flop.

image

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop. Present Inputs Present State Next State

image

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

image

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)

# T Flip-Flop

T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

image

This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are co

mplement to each other in T flip-flop. The following table shows the state table of T flip-flop.

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop. Inputs Present State Next State

image

From the above characteristic table, we can directly write the next state equation as Q(t+1)=T′Q(t)+TQ(t)′ ⇒Q(t+1)=T⊕Q(t)

# Procedure
  # 1.Using nand gates and wires construct sr flip flop
  # 2.Repeat the same steps for JK,D,T flipflops.
  # 3.Find RTL logic and timing diagram for all flipflops
  # 4.End the program

# PROGRAM
```
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: Sivaramakrishnan B
RegisterNumber: 22006798

# SR flipflop

module FlipFlopSR(S,R,clock,Q,Qbar);
input S,R,clock;
output Q,Qbar;
wire X,Y;
nand(X,S,clock);
nand(Y,R,clock);
nand(Q,X,Qbar);
nand(Qbar,Y,Q);
endmodule

# JK flipflop

module FlipFlopJK(J,K,clock,Q,Qbar);
input J,K,clock;
output Q,Qbar;
wire P,S;
nand(P,J,clock,Qbar);
nand(S,K,clock,Q);
nand(Q,P,Qbar);
nand(Qbar,S,Q);
endmodule

# T flipflop

module FlipFlopT(T,clock,Q,Qbar);
input T,clock;
output Q,Qbar;
wire A,B;
nand(A,T,clock,Qbar);
nand(B,T,clock,Q);
nand(Q,A,Qbar);
nand(Qbar,B,Q);
endmodule

# D flipflop

module FlipFlopD(D,clock,Q,Qbar);
input D,clock;
output Q,Qbar;
assign Dbar=~D;
wire X,Y;
nand(X,D,clock);
nand(Y,Dbar,clock);
nand(Q,X,Qbar);
nand(Qbar,Y,Q);
endmodule
```

# OUTPUT

# RTL LOGIC FOR FLIPFLOPS

# SR Flipflop

images
# JK Flipflop

images
# T Flipflop

# TIMING DIGRAMS FOR FLIP FLOPS

# SR Flipflop

 images
# JK Flipflop

images
# T Flipflop

images
# D Flipflop

images
# RESULTS

Thus the flipflops circuit are designed and the truth table is verified using quartus software
