Download Link: https://assignmentchef.com/product/solved-cpsc3300-project-3-speed-up-matrix-multiplication
<br>
This is an individual or team of two project assignment.

<u>An implementation that gives an incorrect product matrix gets 0 points for methodology on this project.</u>

<strong>Summary: </strong>In this project you are going to optimize an implementation of sequential Matrix Multiply provided in matmul_naive.c. The goal is to obtain a maximum <u>overall</u> speedup as you can with multiple optimization techniques. Note that you <u>can’t use parallel computing</u> for this project.

Start with the provided naïve implementation, and add optimization techniques one by one to hand tune the program and make it run faster. Common optimization techniques include register variable, loop interchanging, loop unrolling, blocking, prefetching. These techniques are commonly used by programmers and compilers.




Name the optimized code matmul_opt.c, compare the optimized code against the naïve implementation.

Submit matmul_opt.c and a report named “Matrix Multiplication Optimization.pdf” both to Canvas. The required sections and contents for the report is provided at the end of this document.

<strong>Matmul: </strong>C = A x B where A is a general m x k matrix, B is a general k x n matrix, and C is the product m x n matrix. For simplicity we assume m = k = n or square matrices in this project.

<strong>Compare hand-tuned program against naïve program.</strong> Always use -O0 (-[Big O][zero]) to turn off optimization in compilers when compiling the hand-tuned program and the naïve program. Compare the execution times of these two programs for various matrix sizes and calculate speedups, which is defined as Time<sub>naive</sub>/Time<sub>opt</sub>.

<strong>Timing: </strong>Use timing functions in the code to measure the performance. Example timing functions include gettimeofday and getrusage in Unix/Linux environments. Report the performances, speedups, and comparisons in figures or/and tables. Multiple matrix sizes should be examined in the experiments.

The timing and comparisons can be reported in a table as follows or in figures. In the table, T1 and T2 represent two different optimization techniques. Your method should include as many effective techniques as possible, so that the achieved speedup is the highest. Particularly, your method should include the blocking technique and use different block sizes. Assume that blocking is denoted as T4, the following table includes the timing info for two block sizes.




<table width="592">

 <tbody>

  <tr>

   <td width="262"><strong>Technique / Matrix Size</strong></td>

   <td width="66"><strong>1000</strong></td>

   <td width="66"><strong>2000</strong></td>

   <td width="66"><strong>3000</strong></td>

   <td width="66"><strong>4000</strong></td>

   <td width="66"><strong>5000</strong></td>

  </tr>

  <tr>

   <td width="262"><strong>Naïve + (-O0)   (</strong>Time<sub>naive</sub><strong>)</strong></td>

   <td width="66"> </td>

   <td width="66"> </td>

   <td width="66"> </td>

   <td width="66"> </td>

   <td width="66"> </td>

  </tr>

  <tr>

   <td width="262"><strong>Transformed code with T1 + </strong><strong>(-O0)     (</strong>Time<sub>opt</sub><strong>)</strong></td>

   <td width="66"> </td>

   <td width="66"> </td>

   <td width="66"> </td>

   <td width="66"> </td>

   <td width="66"> </td>

  </tr>

  <tr>

   <td width="262">Time<sub>naive</sub>/Time<sub>opt</sub></td>

   <td width="66"> </td>

   <td width="66"> </td>

   <td width="66"> </td>

   <td width="66"> </td>

   <td width="66"> </td>

  </tr>

  <tr>

   <td width="262"><strong>Transformed code with T1 &amp; T2 + (-O0)     (</strong>Time<sub>opt</sub><strong>)</strong></td>

   <td width="66"> </td>

   <td width="66"> </td>

   <td width="66"> </td>

   <td width="66"> </td>

   <td width="66"> </td>

  </tr>

  <tr>

   <td width="262">Time<sub>naive</sub>/Time<sub>opt</sub></td>

   <td width="66"> </td>

   <td width="66"> </td>

   <td width="66"> </td>

   <td width="66"> </td>

   <td width="66"> </td>

  </tr>

  <tr>

   <td width="262"><strong>…</strong></td>

   <td width="66"> </td>

   <td width="66"> </td>

   <td width="66"> </td>

   <td width="66"> </td>

   <td width="66"> </td>

  </tr>

  <tr>

   <td width="262"><strong>Transformed code with T1 &amp; T2 &amp; T3 &amp; T4 (blk=32) + (-O0)     (</strong>Time<sub>opt</sub><strong>)</strong></td>

   <td width="66"> </td>

   <td width="66"> </td>

   <td width="66"> </td>

   <td width="66"> </td>

   <td width="66"> </td>

  </tr>

  <tr>

   <td width="262">Time<sub>naive</sub>/Time<sub>opt</sub></td>

   <td width="66"> </td>

   <td width="66"> </td>

   <td width="66"> </td>

   <td width="66"> </td>

   <td width="66"> </td>

  </tr>

  <tr>

   <td width="262"><strong>Transformed code with T1 &amp; T2 &amp; T3 &amp; T4 (blk=48) + (-O0)     (</strong>Time<sub>opt</sub><strong>)</strong></td>

   <td width="66"> </td>

   <td width="66"> </td>

   <td width="66"> </td>

   <td width="66"> </td>

   <td width="66"> </td>

  </tr>

  <tr>

   <td width="262">Time<sub>naive</sub>/Time<sub>opt</sub></td>

   <td width="66"> </td>

   <td width="66"> </td>

   <td width="66"> </td>

   <td width="66"> </td>

   <td width="66"> </td>

  </tr>

 </tbody>

</table>




The report should be at least 4 pages (2 ½ pages single spaced) or if working as a team of two, 8 pages (5 pages single spaced).




<strong>Required sections of the report: </strong>

<ol>

 <li><em>Title and author info: </em>Your name should appear towards the top of the first page of your report. I suggest 14-point font for title, and 12-­point font for the rest of your document. If you work in teams of two, include both names on the on the paper and both people should submit the same paper to Canvas. The document should use a single column with 12 point font. Margins should be 1 inch from all sides. Use numeric headings and subheadings as necessary.</li>

 <li><em>Abstract: </em>On the first page of your document, provide an abstract that summarizes your work, approach, and findings. This should include exact numbers for your achieved speedup. This should provide the reader with an overview of your contribution without having to read the paper. This should be no longer than 200 words.</li>

 <li><em>Related Work: </em>If you utilized algorithms or approaches that you did not invent, you should cite them accordingly in your paper. This is to be your own work, where you apply optimizations by hand to the code given by the instructor. You may use other algorithms and techniques provided you understand and can explain how they work, and you implement the code yourself. Here you should simply identify others’ work and discuss its relationship to your optimized matrix multiply. This section should be less than 300 words. Save the particulars of your approach for the next section.</li>

 <li><em>Methodology: </em>This section should describe exactly the method you used to optimize the application. You should provide a step-by-step accounting of your approach. Why you did what you did, and how it might be different or the same from previous approaches. You should discuss your methods for attempting to speed up the given code and how you believe they will affect the code generally. Save exact numbers for the next section.</li>

 <li><em>Results: </em>Here you should provide the empirical timing measurements for the matrix multiply you implemented verse the base version(s). You should summarize the details of the system upon which implementation took place (architecture, platform) and the timing methods you used (and why you chose both arch and timing method). You should provide charts and tables as necessary to show your results and discuss the results in the context of your methodology from the last section. This section should contain mostly tables or graphs (like those found at the end of this document) and some analysis of what worked, why you think it worked, and what didn’t work.</li>

 <li><em>References: </em>The IEEE Journal citation format is strongly recommended. You must cite all references. Plagiarism is unacceptable. Formatting details can be found at:</li>

</ol>




http://www.ece.uiuc.edu/pubs/ref_guides/ieee.html