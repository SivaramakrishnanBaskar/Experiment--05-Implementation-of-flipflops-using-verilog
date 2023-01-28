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

![Screenshot (94)](https://user-images.githubusercontent.com/119476322/215174080-9f5b0899-21d8-4511-85a4-e7f3ea18914a.png)

This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of SR flip-flop.

![Screenshot (95)](https://user-images.githubusercontent.com/119476322/215174167-faf56733-9a41-4f05-a402-ed09e3dd1b6f.png)

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop. Present Inputs Present State Next State

![Screenshot (96)](https://user-images.githubusercontent.com/119476322/215174222-bf556804-3e28-4e08-8559-dca3e0524fa9.png)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![Screenshot (97)](https://user-images.githubusercontent.com/119476322/215174337-57cc4d1b-01d0-407e-b9ae-539b1443ccc9.png)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)

# D Flip-Flop

D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.

This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of D flip-flop. 

![Screenshot (98)](https://user-images.githubusercontent.com/119476322/215174536-e73335bd-5e47-4f1b-a56b-74c2d42e4f01.png)

![Screenshot (99)](https://user-images.githubusercontent.com/119476322/215174683-6f370291-07aa-46f2-aba6-fd3337328eaa.png)

Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D

![Screenshot (100)](https://user-images.githubusercontent.com/119476322/215174865-86662b08-f6e7-4a76-95ae-3939abbfc70c.png)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.

# JK Flip-Flop

![Screenshot (101)](https://user-images.githubusercontent.com/119476322/215175086-eee150c6-b422-4cdf-9aa3-bd4e7cf389bf.png)

JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure. image

This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs. The following table shows the state table of JK flip-flop.

![Screenshot (102)](https://user-images.githubusercontent.com/119476322/215175249-8f73427a-aae1-4129-b1b6-1d0cadcdad06.png)

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop. Present Inputs Present State Next State

![Screenshot (103)](https://user-images.githubusercontent.com/119476322/215175421-48aac507-3906-4a4c-8244-2549b55b68dc.png)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![Screenshot (104)](https://user-images.githubusercontent.com/119476322/215178351-3ef4ad95-d6ff-4a2f-9e0f-74f3296c7cd7.png)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)

# T Flip-Flop

T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![Screenshot (105)](https://user-images.githubusercontent.com/119476322/215175998-5338072d-50bf-4d22-999f-68bcf21b3e54.png)

This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are co

mplement to each other in T flip-flop. The following table shows the state table of T flip-flop.

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop. Inputs Present State Next State

![Screenshot (106)](https://user-images.githubusercontent.com/119476322/215176161-fc3e0e31-b78e-4f4d-b5c0-751c3302ad60.png)

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
```

# SR flipflop
```
module FlipFlopSR(S,R,clock,Q,Qbar);
input S,R,clock;
output Q,Qbar;
wire X,Y;
nand(X,S,clock);
nand(Y,R,clock);
nand(Q,X,Qbar);
nand(Qbar,Y,Q);
endmodule
```

# JK flipflop
```
module FlipFlopJK(J,K,clock,Q,Qbar);
input J,K,clock;
output Q,Qbar;
wire P,S;
nand(P,J,clock,Qbar);
nand(S,K,clock,Q);
nand(Q,P,Qbar);
nand(Qbar,S,Q);
endmodule
```

# T flipflop
```
module FlipFlopT(T,clock,Q,Qbar);
input T,clock;
output Q,Qbar;
wire A,B;
nand(A,T,clock,Qbar);
nand(B,T,clock,Q);
nand(Q,A,Qbar);
nand(Qbar,B,Q);
endmodule
```

# D flipflop
```
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

![Screenshot (107)](https://user-images.githubusercontent.com/119476322/215176381-ed76912e-8429-456a-b315-45cb3f2d6f84.png)

# JK Flipflop

![Screenshot (108)](https://user-images.githubusercontent.com/119476322/215176481-e3987163-49a5-48bf-b6d3-0a1acfe2d266.png)


# T Flipflop

![Screenshot (109)](https://user-images.githubusercontent.com/119476322/215176595-afe71509-5645-4f15-85dc-da9a48d2afac.png)

# D Flipflop 

![Screenshot (110)](https://user-images.githubusercontent.com/119476322/215176880-01baa9b1-4415-4111-b43d-9d1f7d9d5ef8.png)

# TIMING DIGRAMS FOR FLIP FLOPS

# SR Flipflop

![Screenshot (111)](https://user-images.githubusercontent.com/119476322/215177111-e8afe418-7fe2-4f4a-a927-63a52f418503.png)

# JK Flipflop

![Screenshot (112)](https://user-images.githubusercontent.com/119476322/215177180-dfdbe1b5-cd2e-4786-922d-ec556fb395a2.png)

# T Flipflop

![Screenshot (113)](https://user-images.githubusercontent.com/119476322/215177239-2fcca4c2-b836-4c23-84c7-a2d160821e8b.png)

# D Flipflop

![Screenshot (114)](https://user-images.githubusercontent.com/119476322/215177329-db00708b-cb87-4333-88f9-3a2574e83c74.png)

# RESULTS
Thus the flipflops circuit are designed and the truth table is verified using quartus software
