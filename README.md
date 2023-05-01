Download Link: https://assignmentchef.com/product/solved-c-project-a-logic-circuit
<br>
For this assignment, you are expected to write a program which simulates a logic circuit for a set of given inputs. In this assignment, you are going to use structure and dynamic memory allocation.

<strong>Be careful with file names. You won’t given a chance to correct any mistakes.</strong>

<ul>

 <li>Your program reads two files:

  <ul>

   <li>txt</li>

   <li>txt</li>

  </ul></li>

 <li>Your program creates a text file:

  <ul>

   <li>txt</li>

  </ul></li>

 <li>According to content in <sub>txt</sub>, the program <strong><sub>dynamically </sub></strong>creates necessary structures for a logic circuit and evaluates the cases listed in <sub>input.txt</sub>.</li>

 <li>Your program prints the output to <sub>txt</sub>. Each output step should be on a separate line. <strong>circuit.txt</strong></li>

 <li>Each line starts with a <sub>keyword</sub>. Possible <sub>keyword</sub>s:</li>

</ul>

INPUT

AND

OR

NOT

FLIPFLOP

<ul>

 <li>The first line specifies input labels. Labels are separated by spaces. Example:</li>

</ul>

INPUT a input2 c3 k

<ul>

 <li>Here there are <sub>4 </sub>inputs are defined. Each has an identifier. <sub>a</sub>, <sub>input2</sub>, <sub>c3</sub>, <sub>k</sub>.</li>

 <li><sub>AND </sub>keyword specifies that there is an <sub>and </sub>gate defined. <sub>AND </sub>keyword follows the identifier for the gate and two other identifiers for the inputs. Example:</li>

</ul>

AND gate_A c3 another_id

<ul>

 <li>Here the <sub>and </sub>gate is identified by the string <sub>gate_A</sub>. Its inputs are identified <sub>c3 </sub>and <sub>another_id</sub>. These identifiers can be input identifiers or identifiers for other gates.</li>

 <li><sub>OR </sub>keyword specifies that there is an <sub>or </sub>gate defined. <sub>OR </sub>keyword follows the identifier for the gate and two other identifiers for the inputs. Example:</li>

</ul>

OR gate_B ck id3

<ul>

 <li>Here the <sub>or </sub>gate is identified by the string <sub>gate_B</sub>. Its inputs are identified <sub>ck </sub>and <sub>id3</sub>. These identifiers can be input identifiers or identifiers for other gates.</li>

 <li><sub>NOT </sub>keyword specifies that there is an <sub>not </sub>gate defined. <sub>NOT </sub>keyword follows the identifier for the gate and one other identifier for its input. Example:</li>

</ul>

NOT gate_C c5

<ul>

 <li>Here the <sub>not </sub>gate is identified by the string <sub>gate_C</sub>. It has only one input an it is identified by the string <sub>c5</sub>.</li>

 <li><sub>FLIPFLOP </sub>keyword specifies that there is an <sub>flip-flop </sub>gate defined. <sub>FLIPFLOP </sub>keyword follows the identifier</li>

</ul>

for the gate and one other identifier for its input. Example:

FLIPFLOP gate_F c6

<ul>

 <li>Here the <sub>flip-flop </sub>gate is identified by the string <sub>gate_F</sub>. Its input is identified by <sub>c6</sub>. <strong>txt</strong></li>

 <li>Each line is a list of <sub>1 </sub>and <sub>0</sub>. Example:</li>

</ul>

1 0 1 1

0 1 1 1

<ul>

 <li>0 1 0</li>

 <li>0 0 1</li>

</ul>

<strong>Example:</strong>

<ul>

 <li>Suppose that <sub>txt </sub>is has the following content:</li>

</ul>

INPUT a b c d AND and1 a b

OR or1 and1 c

NOT n1 d

FLIPFLOP f1 n1

AND a2 or1 f1

<ul>

 <li><sub>txt </sub>has the following content:</li>

</ul>

1 1 0 1

1 0 1 0

1 1 1 0

<ul>

 <li>Assume that initially former-out of any FLIPFLOP is 0.</li>

 <li>Any <sub>FLIPFLOP</sub>s should preserve the state throughout the evaluation of the whole <sub>txt</sub>.</li>

 <li>Each line in <sub>txt </sub>is assigned to identifiers <sub>a</sub>, <sub>b</sub>, <sub>c</sub>, <sub>d</sub>, defined in <sub>circuit.txt</sub>. According to the truth tables, outputs of gates are calculated.</li>

 <li>For the input.txt given, the contents of output.txt should be:</li>

</ul>

0

1

0

<strong>Remarks</strong>

<ul>

 <li>Output is not defined explicitly. It is your job to figure out the output pin. There will always going to be one output pin.</li>

 <li>Each identifier is unique. Max length of each identifier is <sub>10 </sub></li>

 <li>Assume there won’t be multiple spaces separating the identifiers, keywords or data. Tokenize it according to this assumption.</li>

 <li>There won’t be any errors in the files.</li>

 <li>You <strong>have to </strong>use dynamical memory allocation and struct. You <strong>have to </strong>use struct in order to represent the gates of the circuit.</li>

 <li>Do not submit your code without testing it with several different scenarios. Try cases with multiple gates of the same type. Try cases with single gate. Try <sub>txt </sub>with thousands of lines. Try cases with many gates. Try cases where there are many inputs.</li>

 <li>You can use <sub>c structs</sub>, unions, arrays, c strings, pointers, recursion.</li>

 <li>Write comments in your code.</li>

 <li>Do not print anything to <sub>stdout </sub>and <sub>stderr</sub>.</li>

 <li>Do not submit any of the files you used for testing.</li>

 <li>Do not submit your output file.</li>

</ul>

<strong>Truth Tables:</strong>

<ul>

 <li>AND</li>

</ul>

<table width="65">

 <tbody>

  <tr>

   <td width="23">a</td>

   <td width="23">b</td>

   <td width="19">out</td>

  </tr>

  <tr>

   <td width="23">0</td>

   <td width="23">0</td>

   <td width="19">0</td>

  </tr>

  <tr>

   <td width="23">0</td>

   <td width="23">1</td>

   <td width="19">0</td>

  </tr>

  <tr>

   <td width="23">1</td>

   <td width="23">0</td>

   <td width="19">0</td>

  </tr>

  <tr>

   <td width="23">1</td>

   <td width="23">1</td>

   <td width="19">1</td>

  </tr>

  <tr>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="19"> </td>

  </tr>

  <tr>

   <td width="23">a</td>

   <td width="23">b</td>

   <td width="19">out</td>

  </tr>

  <tr>

   <td width="23">0</td>

   <td width="23">0</td>

   <td width="19">0</td>

  </tr>

  <tr>

   <td width="23">0</td>

   <td width="23">1</td>

   <td width="19">1</td>

  </tr>

  <tr>

   <td width="23">1</td>

   <td width="23">0</td>

   <td width="19">1</td>

  </tr>

  <tr>

   <td width="23">1</td>

   <td width="23">1</td>

   <td width="19">1</td>

  </tr>

 </tbody>

</table>

<ul>

 <li>OR</li>

 <li>NOT</li>

</ul>

<table width="42">

 <tbody>

  <tr>

   <td width="23">a</td>

   <td width="19">out</td>

  </tr>

  <tr>

   <td width="23">0</td>

   <td width="19">1</td>

  </tr>

  <tr>

   <td width="23">1</td>

   <td width="19">0</td>

  </tr>

 </tbody>

</table>

<ul>

 <li>FLIPFLOP</li>

</ul>

<table width="125">

 <tbody>

  <tr>

   <td width="23">a</td>

   <td width="83">former_out</td>

   <td width="19">out</td>

  </tr>

  <tr>

   <td width="23">0</td>

   <td width="83">0</td>

   <td width="19">0</td>

  </tr>

  <tr>

   <td width="23">0</td>

   <td width="83">1</td>

   <td width="19">1</td>

  </tr>

  <tr>

   <td width="23">1</td>

   <td width="83">0</td>

   <td width="19">1</td>

  </tr>

  <tr>

   <td width="23">1</td>

   <td width="83">1</td>

   <td width="19">0</td>

  </tr>

 </tbody>

</table>


