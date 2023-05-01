Download Link: https://assignmentchef.com/product/solved-cs2110-homework3-arithmetic-logic-units
<br>
All computer processors have a very important component known as the Arithmetic Logic Unit (ALU). This component allows the computer to do, as the name suggests, arithmetic and logical operations. For this assignment, you’re going to build an ALU of your own, along with creating some of the gates.

For this assignment you will:

<ol>

 <li>Create the standard logic gates (NAND, NOR, NOT, AND, OR)</li>

 <li>Create an 8-input multiplexer and an 8-output decoder</li>

 <li>Create a 1-bit full adder</li>

 <li>Create an 8-bit full adder using the 1-bit full adder</li>

 <li>Use your 8-bit full adder and other components to construct an 8-bit ALU</li>

</ol>

<strong>This assignment will be demoed alongside Homework 4. </strong>More information on this and the sign-up schedule will be posted on Canvas. An announcement will be sent out and it will also be announced in Lecture/Lab when the schedule is up. <strong>You have to be present for the demo in order to get credit for the demo-portion of the assignment.</strong>

<h1><a name="_Toc10729"></a>1           Instructions</h1>

<h2><a name="_Toc10730"></a>1.1         Requirements</h2>

For the first part of this assignment (the logic gates), you may use only those components found in the Wiring tab (being the input/output pins, constants, probes, clocks, splitters, tunnels, and transistors), along with any of the sub-circuits that you create or that already exist.

For the second part of this assignment (the multiplexer and decoder), you may use only those components found in the Wiring and Gates tabs along with any of the sub-circuits that you create or that already exist.

For the third part of this assignment, you may use only those components found in the Wiring and Gates tabs as well as any of the sub-circuits that you create or that already exist. <strong>For the ALU specifically, you may use the Plexer tab as well.</strong>

<strong>Use of anything not listed above will result in heavy deductions. </strong>Your need to have everything in their correctly named sub-circuit. More information on sub-circuits is given below.

Use tunnels where necessary to make your designs more readable, but do not overdo it! For gates, muxes, adders and decoders you can often get clean circuits just by placing your components well rather than using tunnels everywhere.

<h2><a name="_Toc10731"></a>1.2         Part 1: 1-Bit Logic Gates</h2>

All of the circuits in this file are in the <em>gates.sim </em>file, and you may use the <strong>Wiring </strong>tab for this part.

For this part of the assignment, you will create a transitor-level implementation of the NAND, NOT, NOR, AND, and OR logic gates.

Remember for this section that you are only allowed to use the components listed in the Wiring section, along with any of the logic gates you are implementing in CircuitSim. For example, once you implement the NOT gate you are free to use that subcircuit in implementing other logic gates. Implementing the gates in the order of the subcircuit tabs can be the easiest option.

As a brief summary of the behavior of each logic gate:

<table width="605">

 <tbody>

  <tr>

   <td width="27"><strong>A</strong></td>

   <td width="27"><strong>B</strong></td>

   <td colspan="2" width="96"><strong>A NAND B</strong></td>

   <td rowspan="5" width="18"> </td>

   <td width="27"><strong>A</strong></td>

   <td width="27"><strong>B</strong></td>

   <td width="83"><strong>A NOR B</strong></td>

   <td rowspan="5" width="18"> </td>

   <td width="27"><strong>A</strong></td>

   <td width="27"><strong>B</strong></td>

   <td width="84"><strong>A AND B</strong></td>

   <td rowspan="5" width="18"> </td>

   <td width="27"><strong>A</strong></td>

   <td width="27"><strong>B</strong></td>

   <td width="71"><strong>A OR B</strong></td>

  </tr>

  <tr>

   <td width="27">0</td>

   <td width="27">0</td>

   <td colspan="2" width="96">1</td>

   <td width="27">0</td>

   <td width="27">0</td>

   <td width="83">1</td>

   <td width="27">0</td>

   <td width="27">0</td>

   <td width="84">0</td>

   <td width="27">0</td>

   <td width="27">0</td>

   <td width="71">0</td>

  </tr>

  <tr>

   <td width="27">0</td>

   <td width="27">1</td>

   <td colspan="2" width="96">1</td>

   <td width="27">0</td>

   <td width="27">1</td>

   <td width="83">0</td>

   <td width="27">0</td>

   <td width="27">1</td>

   <td width="84">0</td>

   <td width="27">0</td>

   <td width="27">1</td>

   <td width="71">1</td>

  </tr>

  <tr>

   <td width="27">1</td>

   <td width="27">0</td>

   <td colspan="2" width="96">1</td>

   <td width="27">1</td>

   <td width="27">0</td>

   <td width="83">0</td>

   <td width="27">1</td>

   <td width="27">0</td>

   <td width="84">0</td>

   <td width="27">1</td>

   <td width="27">0</td>

   <td width="71">1</td>

  </tr>

  <tr>

   <td width="27">1</td>

   <td width="27">1</td>

   <td colspan="2" width="96">0</td>

   <td width="27">1</td>

   <td width="27">1</td>

   <td width="83">0</td>

   <td width="27">1</td>

   <td width="27">1</td>

   <td width="84">1</td>

   <td width="27">1</td>

   <td width="27">1</td>

   <td width="71">1</td>

  </tr>

  <tr>

   <td width="27"><strong>A</strong></td>

   <td colspan="2" width="67"><strong>NOT A</strong></td>

   <td colspan="13" width="510"> </td>

  </tr>

  <tr>

   <td width="27">0</td>

   <td colspan="2" width="67">1</td>

   <td colspan="13" width="510"> </td>

  </tr>

  <tr>

   <td width="27">1</td>

   <td colspan="2" width="67">0</td>

   <td colspan="13" width="510"> </td>

  </tr>

  <tr>

   <td width="28"></td>

   <td width="27"></td>

   <td width="40"></td>

   <td width="56"></td>

   <td width="18"></td>

   <td width="27"></td>

   <td width="27"></td>

   <td width="83"></td>

   <td width="18"></td>

   <td width="27"></td>

   <td width="27"></td>

   <td width="84"></td>

   <td width="18"></td>

   <td width="27"></td>

   <td width="27"></td>

   <td width="71"></td>

  </tr>

 </tbody>

</table>

Hint: Start by creating the NAND gate from transistors. Then use this gate as a subcircuit for implementing the others.

<strong>All of the logic gates must be within their named sub-circuits.</strong>

<h2><a name="_Toc10732"></a>1.3         Part 2: Plexers</h2>

All of the circuits in this file are in the <em>plexers.sim </em>file, and you may use the <strong>Wiring, Gates </strong>tabs for this part.

The multiplexer you will be creating has 8 1-bit inputs (labeled appropriately as A, B, C, …, H), a single 3-bit selection input (SEL), and one 1-bit output (OUT). The multiplexer uses the SEL input to choose a specific input line for forwarding to the output.

For example:

SEL = 000 ==&gt; OUT = A

SEL = 001 ==&gt; OUT = B

SEL = 010 ==&gt; OUT = C

SEL = 011 ==&gt; OUT = D

SEL = 100 ==&gt; OUT = E

SEL = 101 ==&gt; OUT = F

SEL = 110 ==&gt; OUT = G

SEL = 111 ==&gt; OUT = H

The decoder you will be creating has a single 3-bit selection input (SEL), and eight 1-bit output (labeled A, B, C, …, H). The decoder uses the SEL input to raise a specific output line, as seen below.

For example:

SEL = 000 ==&gt; A = 1, BCDEFGH = 0

SEL = 001 ==&gt; B = 1, ACDEFGH = 0

SEL = 010 ==&gt; C = 1, ABDEFGH = 0

SEL = 011 ==&gt; D = 1, ABCEFGH = 0

SEL = 100 ==&gt; E = 1, ABCDFGH = 0

SEL = 101 ==&gt; F = 1, ABCDEGH = 0

SEL = 110 ==&gt; G = 1, ABCDEFH = 0

SEL = 111 ==&gt; H = 1, ABCDEFG = 0

<h2><a name="_Toc10733"></a>1.4         Part 3: Adders &amp; ALUs</h2>

All of the circuits in this file are in the <em>alu.sim </em>file, and you may use the <strong>Wiring and Gates </strong>tabs for this part. <strong>For the ALU specifically, you may use the Plexer tab as well.</strong>

<h3><a name="_Toc10734"></a>1.4.1         1-Bit Adder</h3>

The full adder has three 1-bit inputs (A, B, and CIN), and two 1-bit outputs (SUM and COUT). The full adder adds A + B + CIN and places the sum in SUM and the carry-out in COUT.

For example:

A = 0, B = 1, CIN = 0 ==&gt; SUM = 1, COUT = 0

A = 1, B = 0, CIN = 1 ==&gt; SUM = 0, COUT = 1

A = 1, B = 1, CIN = 1 ==&gt; SUM = 1, COUT = 1

Hint: Making a truth table of the inputs will help you.

<h3><a name="_Toc10735"></a>1.4.2         8-Bit Adder</h3>

For this part of the assignment, you will daisy-chain 8 of your 1-bit full adders together in order to make an 8-bit full adder.

This circuit should have two 8-bit inputs (A and B) for the numbers you’re adding, and one 1-bit input for CIN. The reason for the CIN has to do with using the adder for purposes other than adding the two inputs.

There should be one 8-bit output for SUM and one 1-bit output for COUT.

<h3><a name="_Toc10736"></a>1.4.3         8-Bit ALU</h3>

You will create an 8-bit ALU with the following operations, using the 8-bit full adder you created in for

2.4.2:

<ol>

 <li>Addition [A + B]</li>

 <li>Subtraction [A – B]</li>

 <li>2’s Complement Negation [-A]</li>

 <li>Multiply by 13 [A * 13]</li>

 <li>isMultipleOf8 [A % 8 == 0]</li>

 <li>isPowerOf2 [<em>A </em>== 2<em><sup>n </sup></em>for some <em>n</em>∈<em>N</em>, including 2<sup>0 </sup>= 1]</li>

 <li>XOR [A XOR B]</li>

 <li>Constant Output [0x69]</li>

</ol>

Notice that 2’s Complement Negation, Multiply by 13, isMultipleOf8, and isPowerOf2 only operate on the A input. <strong>They should NOT rely on </strong>B <strong>being a particular value. </strong>Likewise, Constant Output does not use either input and should not rely on their value.

This ALU has two <strong>8-bit </strong>inputs for A and B and one <strong>3-bit </strong>input for OP, the op-code for the operation in the list above. It has one <strong>8-bit </strong>output named OUT.

The provided autograder will check the op-codes according to the order listed above (Addition (000), Subtraction (001), etc.) and thus it is important that the operations are in this exact order.

<strong>Hint: </strong>For check if a number is a power of two, remember your implementation in Homework 2. The best implementation of this is the expression (<em>a&gt; </em>0&amp;&amp;((<em>a</em>&amp;(<em>a</em>−1)) == 0)) which is easy to implement in digital logic.

<h1><a name="_Toc10737"></a>2           Deliverables</h1>

Please upload the following files onto the assignment on Gradescope:

<ol>

 <li>sim</li>

 <li>sim</li>

 <li>sim</li>

</ol>

<strong>Be sure to check your score to see if you submitted the right files, as well as your email frequently until the due date of the assignment for any potential updates.</strong>

<strong>No partial credit will be given for incorrect outputs for Part 1, Part 2, and the adder-portion of Part 3. For the ALU, partial credit will be awarded on a per-operation basis, wherein each operation must perform successfully to be awarded credit. Because of this, we urge you to check your score before the due date.</strong>

<strong>Once again, this assignment will be demoed alongside Homework 4! </strong>More information on this and the sign-up schedule will be posted on Canvas. An announcement will be sent out and it will also be announced in Lecture/Lab when the schedule is up. <strong>You have to be present for the demo in order to get credit for the demo-portion of the assignment.</strong>

<h1><a name="_Toc10738"></a>3           Sub-Circuit Tutorial</h1>

As you build circuits that are more and more sophisticated, you will want to build smaller circuits that you can use multiple times within larger circuits. Sub-circuits behave like classes in Object-Oriented languages. Any changes made in the design of a sub-circuit are automatically reflected wherever it is used. The direction of the IO pins in the sub-circuit correspond to their locations on the representation of the sub-circuit.

<strong>To create a sub-circuit:</strong>

<ol>

 <li>Go to the “Circuits” menu and choose “New circuit”</li>

 <li>Name your circuit by right-clicking on the “New circuit” item and selecting “Rename”</li>

</ol>

<strong>To use a sub-circuit:</strong>

<ol>

 <li>Click the “Circuits” tab next to the “Misc” tab</li>

 <li>Select the circuit you wish to use and place it in your design</li>

</ol>