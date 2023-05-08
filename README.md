Download Link: https://assignmentchef.com/product/solved-ve492-homework-7
<br>
<h1>Question 1: Rejection Sampling</h1>

We will work with a Bayes’ net of the following structure.

In this question, we will perform rejection sampling to estimate P(C=1|B=1,E=1). Perform one round of rejection sampling, using the random samples given in the table below. Variables are sampled in the order A,B,C,D,E. In the boxes below, choose the value (0 or 1) that each variable gets assigned to. Note that the sampling attempt should stop as soon as you discover that the sample will be rejected. In that case mark the assignment of that variable.

When generating random samples, use as many values as needed from the table below, which we generated independently and uniformly at random from [0,1). Use numbers from left to right. To sample a binary variable <em>W </em>with probability <em>P(W=0)=p </em>and <em>P(W=1)=1-p </em>using a value <em>a </em>from the table, choose <em>W=0 </em>if a&lt;p and <em>W=1 </em>if <em>a&gt;=p</em>

Enter either a 0 or 1 for each variable that you assign a value to. Upon rejecting a sample, enter its assigned value, and leave the fields for the remaining variables blank (use “b” for blank). For example, if C gets rejected, fill in “b” for D and E.

A____B____C____D____E____

Which variable will get rejected? If no variables will get rejected, leave the field below blank.

____

<strong>Sample answer:</strong>

<strong>01bbbB</strong>

<h1>Question 2: Estimating Probabilities from Samples</h1>

Below are a set of samples obtained by running rejection sampling for the Bayes’ net from the previous question. Use them to estimate <em>P(C=1|B=1,E=1) </em>. The estimation cannot be made whenever all samples were rejected. In this case, input -1.

<strong>Sample answer:</strong>

<strong>0.2</strong>

<strong>Likelihood Weighting</strong>

We will work with a Bayes’ net of the following structure.

In this question, we will perform likelihood weighting to estimate P(C=1|B=1,E=1). Generate a sample and its weight, using the random samples given in the table below. Variables are sampled in the order . In the table below, select the assignments to the variables you sampled.

When generating random samples, use as many values as needed from the table below, which we generated independently and uniformly at random from [0,1). Use numbers from left to right. To sample a binary variable <em>W </em>with probability <em>P(W=0)=p </em>and <em>P(W=1)=1-p </em>using a value <em>a </em>from the table, choose <em>W=0 </em>if a&lt;p and <em>W=1 </em>if <em>a&gt;=p</em>

Enter either a 0 or 1 for each variable assigned by a pass of likelihood weighting with the generated samples above.

A____B____C____D____E____

What is the weight for the sample you obtained above? (Keep 2 decimal places)

____

<strong>Sample answer: 011010.16</strong>




<h1>Estimating Probabilities from Weighted Samples</h1>

Below are a set of weighted samples obtained by running likelihood weighting for the Bayes’ net from the previous question. Use them to estimate <em>P(C=1|B=1,E=1)</em>. Input -1 in the box below if the estimation cannot be made.

____ (Keep 2 decimal places) <strong>Sample answer:</strong>

<strong>0.25</strong>

<h1>HMMs, Part I</h1>

Consider the HMM shown below.

The prior probability <sub>0</sub>) , dynamics model <sub>t1 </sub>) , and sensor model ) are as follows:

We perform a first dynamics update, and fill in the resulting belief distribution        <sub>1</sub>).

We incorporate the evidence <sub>1 </sub>. We fill in the evidence-weighted distribution <sub>1 </sub>1) <sub>1</sub>), and the (normalized) belief distribution <sub>1</sub>).

<strong><em>Note: Please write your answer for each table in one row, that is, there will be 3 rows for this question. Besides, please use values rounded to 3 decimal places.</em></strong>

<strong><em>Sample Answer:</em></strong>

<strong><em>0.160,0.170</em></strong>

<strong><em>0.200,0.211</em></strong>

<strong><em>0.222,0.180</em></strong>

<ul>

 <li>You get to perform the second dynamics update. Write your answer to fill in the resulting belief distribution ).</li>

</ul>

<table width="215">

 <tbody>

  <tr>

   <td width="47"> </td>

   <td width="168">)</td>

  </tr>

  <tr>

   <td width="47">0</td>

   <td width="168"> </td>

  </tr>

  <tr>

   <td width="47">1</td>

   <td width="168"> </td>

  </tr>

 </tbody>

</table>

<ul>

 <li>Now incorporate the evidence ‸ . Write your answer to fill in the evidence-weighted distribution ‸ ) ), and the (normalized) belief distribution ).</li>

</ul>

<table width="215">

 <tbody>

  <tr>

   <td width="47"> </td>

   <td width="97">‸</td>

   <td width="45">)</td>

   <td colspan="2" width="26">)</td>

  </tr>

  <tr>

   <td width="47">0</td>

   <td width="97"> </td>

   <td width="45"> </td>

   <td colspan="2" width="26"> </td>

  </tr>

  <tr>

   <td width="47">1</td>

   <td width="97"> </td>

   <td width="45"> </td>

   <td colspan="2" width="26"> </td>

  </tr>

  <tr>

   <td width="47"> </td>

   <td colspan="3" width="166">)</td>

   <td width="1"> </td>

  </tr>

  <tr>

   <td width="47">0</td>

   <td colspan="3" width="166"> </td>

   <td width="1"> </td>

  </tr>

  <tr>

   <td width="47">1</td>

   <td colspan="3" width="166"> </td>

   <td width="1"> </td>

  </tr>

  <tr>

   <td width="47"></td>

   <td width="97"></td>

   <td width="45"></td>

   <td width="25"></td>

   <td width="1"></td>

  </tr>

 </tbody>

</table>




<h1>Question 6: HMMs, Part II</h1>

Consider the same HMM.

The prior probability <sub>0</sub>) , dynamics model <sub>t1 </sub>) , and sensor model ) are as follows:

In this question we’ll assume the sensor is broken and we get no more evidence readings. We are forced to rely on dynamics updates only going forward. In the limit as , our belief about should converge to a stationary distribution ) defined as follows:

Recall that the stationary distribution satisfies the equation

for all values in the domain of   .

In the case of this problem, we can write these relations as a set of linear equations of the form

In the spaces below, fill in the coefficients of the linear system. The system you have written has many solutions (consider (0,0), for example), but to get a probability distribution we want the solution that sums to one. Write your answer to fill in the table below.

(Hint: to check your answer, you can also write some code and run till convergence.)

<strong><em>Note: Please write your answer for each table in one row, that is, there will be 2 rows for this question. Besides, please use values rounded to 3 decimal places.</em></strong>

<strong><em>Sample Answer:</em></strong>

<strong><em>0.160,0.170,0.160,0.170</em></strong>

<strong><em>0.200,0.211</em></strong>

<table width="202">

 <tbody>

  <tr>

   <td width="101">coefficient</td>

   <td width="101">value</td>

  </tr>

  <tr>

   <td width="101">a</td>

   <td width="101"> </td>

  </tr>

  <tr>

   <td width="101">b</td>

   <td width="101"> </td>

  </tr>

  <tr>

   <td width="101">c</td>

   <td width="101"> </td>

  </tr>

  <tr>

   <td width="101">d</td>

   <td width="101"> </td>

  </tr>

  <tr>

   <td width="101"> </td>

   <td width="101">)</td>

  </tr>

  <tr>

   <td width="101">0</td>

   <td width="101"> </td>

  </tr>

  <tr>

   <td width="101">1</td>

   <td width="101"> </td>

  </tr>

 </tbody>

</table>


