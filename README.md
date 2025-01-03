# T-FLIPFLOP-POSEDGE

**AIM:**

To implement  T flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure

**T Flip-Flop**

T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/T-FLIPFLOP-POSEDGE/assets/154305477/458a68fe-2d08-4a9d-ac4f-7ae0480ce0bd)

 
This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop. The following table shows the state table of T flip-flop.

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop. Inputs Present State Next State

![image](https://github.com/naavaneetha/T-FLIPFLOP-POSEDGE/assets/154305477/cdd7fb32-539f-4b66-bb8d-f305a153c886)

 
From the above characteristic table, we can directly write the next state equation as Q(t+1)=T′Q(t)+TQ(t)′ ⇒Q(t+1)=T⊕Q(t)

**Procedure**

1.Define Inputs/Outputs: Inputs: T (toggle), clk (clock); Outputs: Q, Qbar (~Q). 

2.Initialize: Set Q = 0 and Qbar = 1 at the start of simulation. 

3.Toggle Logic: On posedge clk, update Q 

4.Complementary Output: Set Qbar = ~Q to maintain complementarity. 

5.Testbench: Simulate with various T and clk values to verify toggle functionality.

**PROGRAM**

        module t_ff_ (t, clk, rst, q);
      input t, clk, rst;
      output reg q;
      always @(posedge clk or posedge rst) 
    begin
        if (rst)
          q <= 0; // Reset the flip-flop
        else if (t==0)
          q <= q; 
         else
            q<=~q;
      end
     endmodule
Developed by: pothu sumanth
RegisterNumber: 24000831
*/

**RTL LOGIC FOR FLIPFLOPS**


![Screenshot 2025-01-03 135707](https://github.com/user-attachments/assets/1ba70880-6e32-4918-aaf7-dc43ac68a802)



**TIMING DIAGRAMS FOR FLIP FLOPS**


![WhatsApp Image 2024-12-27 at 13 38 18_63c4eb15](https://github.com/user-attachments/assets/20c15128-4cde-45a1-942d-01158d0961a4)




**RESULTS**
Thus the program to implement T flipflop using verilog and validating their
 functionality using their functional tables has been verified successfully
