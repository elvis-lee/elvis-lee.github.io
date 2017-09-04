---
layout: page
title: Resume
permalink: /resume/
---

<html xmlns="http://www.w3.org/1999/xhtml"><head>
  <meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
  <meta http-equiv="Content-Style-Type" content="text/css">
  <meta name="generator" content="pandoc">
  <title></title>
  <style type="text/css">code{white-space: pre;}</style>
  <style type="text/css">
  /*
   *  * Copyright 2013 Christophe-Marie Duquesne <chmd@chmd.fr>
   *   *
   *    * CSS for making a resume with pandoc. Inspired by moderncv.
   *     *
   *      * This CSS document is delivered to you under the CC BY-SA 3.0 License.
   *       * https://creativecommons.org/licenses/by-sa/3.0/deed.en_US
   *        */
  
  /* Whole document */
  body {
      font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
      /*width: 800px;
      margin: auto;
      background: #FFFFFF;
      padding: 10px 10px 10px 10px;*/
  }
  
  /* Title of the resume */
  h1 {
      font-size: 55px;
      color: #757575;
      text-align:center;
      margin-bottom:15px;
  }
  
  /* Titles of categories */
  h2 {
      color: #397249;
  }
  /* There is a bar just before each category */
  h2:before {
      content: "";
      display: inline-block;
      margin-right:1%;
      width: 16%;
      height: 10px;
      background-color: #9CB770;
  }
  
  /* Definitions */
  dt {
      float: left;
      clear: left;
      width: 12%;
      font-weight: bold;
  }
  dd {
      margin-left: 17%;
  }
  p {
      margin-top:0;
      margin-bottom:7px;
  }
  
  /* Blockquotes */
  blockquote {
      text-align: center
  }
  
  /* Links */
  a {
      text-decoration: none;
  }
  
  /* Horizontal separators */
  hr {
      color: #A6A6A6;
  }
  
  table {
      width: 100%;
      border-top: solid;
      border-bottom: solid;
      border-color:#999999;
  }
  </style>
</head>
<body>
<h1 id="johnny-coder">Hao Li</h1>
<table>
<tbody>
<tr class="odd">
<td align="left">Linkedin: <a href="https://www.linkedin.com/in/hao-li-b1ab89107/">Hao Li</a></td>
<td align="right">Email: <a href="mailto:{{ site.email }}">{{ site.email }}</a></td>
</tr>
<tr class="even">
<td align="left">Personal Website: <a href="http://haoli.space">haoli.space</a></td>
<td align="right">Phone: +1 (510) 570-5088 </td>
</tr>
</tbody>
</table>
<h2 id="education">Education</h2>
<dl>
<dt>Aug 2017-May 2018</dt>
<dd><p><strong>University of California, Berkeley</strong>; M.Eng., Computer Science </p>
<p><em>Project: Scaling up Deep Learning and Reinforcement Learning</em></p>
<p><em>Concentration: Data Systems & Systems
</em></p>
</dd>
<br>
<dt>Sep 2013-Jun 2017</dt>
<dd><p><strong>Zhejiang University</strong>; B.Eng., Electronic and Information Engineering</p>
<p><em>GPA: 3.89/4.00 (rank 2/91); Dean’s List (1/462)</em></p>
</dd>
<br>
<dt>Sep 2007-Jun 2013</dt>
<dd><p><strong>The Affiliated High School of South China Normal University</strong></p>
<p><em>First Award in Chinese Physics Olympiad (Top 40 in Guangdong Province, China)</em></p>
</dd>
</dl>
<br>
<h2 id="experience">Experience</h2>
<dl>
<dt>Oct 2016-Apr 2017 </dt>
<dd><p><strong>Massachusetts Institute of Technology, MEG Lab</strong></p>
<p><em><strong>Research Intern</strong></em></p>
<p>Project: Mining Brain Cognitive Data for Visual Object Recognition</p>
<p>•	Used SVM and multivariate pattern classification to decode brain data and identified neural activities of visual processing</p>
<p>•	Applied Representational Similarity Analysis (RSA) by computing Spearman’s Rank-Order Correlation to characterize the temporal dynamics of feedforward and feedback processing of visual objects</p>
<p>•	Developed MATLAB, C and C++ code to effectively implement multiple pairwise data decoding, reduced runtime from weeks to only 3 hours</p>
</dd>
<dt>Jul 2016-Sep 2016</dt>
<dd><p><strong>University of California, Los Angeles, NESL</strong></p>
<p><em><strong>Research Intern</strong></em></p>
<p>Fully Automated Grading System for MOOC Embedded System </p>
<p>•	Designed the system architecture, laid out communication protocols, and implemented the system backend</p>
<p>•	Implemented and integrated the Testbed Controller in Python with Hardware Engine on STM32F407</p>
<p>•	Tested the system in CS213A: Embedded System Fall 2016 at UCLA and graded students’ submissions successfully</p>
</dd>
</dl>
<br>
<h2 id="technical-experience">Projects</h2>
<dl>
<dt>Sep 2017-May 2018 </dt>
<dd><p><strong>University of California, Berkeley</strong></p>
<p><em><strong>Scaling up Deep Learning and Reinforcement Learning</strong></em></p>
<p>•	To work on extending shared-nothing distributed ML focusing on error tolerance and distributed Monte-Carlo</p>
<p>•	To establish new performance benchmarks for a number of deep learning and reinforcement learning problems</p>
</dd>
<dt>Jan 2016-Feb 2016 </dt>
<dd><p><strong>2016 MCM (Mathematical Contest in Modeling)</strong></p>
<p><em><strong>Optimal Investment Strategy Based on Education Data Mining</strong></em></p>
<p>•	Developed two models to determine an optimal investment strategy based on information extracted from National Center on Education Statistics, awarded Meritorious Winner</p>
<p>•	Built a ranking model using Logistic Regression to compute competitiveness index for each institutions based on contributing variables, obtained weight vectors, applied Significance Analysis, improved the model by reducing Type II Error</p>
<p>•	Proposed a distribution model by establishing a non-linear combinational optimization model, determined number of institutions to invest and the exact amount of investment for each one to achieve maximum ROI (Return On Investment)</p>
</dd>
<dt>Aug 2015-Nov 2015 </dt>
<dd><p><strong>National University of Singapore</strong></p>
<p><em><strong>Message Deciphering Based on Metropolis-Hastings Algorithm</strong></em></p>
<p>•	Developed algorithms in MATLAB designed to decipher messages encrypted by means of character substitution</p>
<p>•	Generated mapping between character and double array, obtained transition matrix from training set, and used Metropolis-Hastings and Simulated Annealing algorithms to effectively obtain the most likely original message</p>
<p>•	Tested the prototype program and successfully deciphered lengthy encrypted natural languageamount of investment for each one to achieve maximum ROI (Return On Investment)</p>
</dd>
</dl>
<br>
<h2 id="Selected Awards">Selected Awards</h2>
<dl>
<dt>UCB</dt>
<dd>•	Fung Fellowship($20,000)</dd>
<br>
<dt>UCLA</dt>
<dd>•	Cross-disciplinary Scholars in Science and Technology($7,500)</dd>
<br>
<dt>NUS</dt>
<dd>•	TF LEaRN Scholar($6,500)</dd>
<br>
<dt>ZJU</dt>
<dd>•	Dean’s List, Scholarship for Excellence (Highest honor awarded by the Chu Kochen Honors College, 1/462)</dd>
<dd>•	Wang Guosong Scholarship (Highest honor awarded by the Department of Electrical Engineering)</dd>
<dd>•	Meritorious Winner of the Mathematical Contest in Modeling (MCM)</dd>
<dd>•	National Scholarship of China</dd>
<dd>•	Tang Lixin Scholarship</dd>
<dd>•	First Class Scholarship for Outstanding Students (awarded three times)</dd>
<br>
<dt>High School</dt>
<dd>•	First Award in Chinese Physics Olympiad (Top 40 in Guangdong Province, China)</dd>
</dl>
<br>
<br>
<h2 id="Language">Skills</h2>
<ul>
<li><p>Human Languages:</p>
<ul>
<li>Mandarin (native speaker)</li>
<li>Cantonese (native speaker)</li>
<li>English (Proficient)</li>
</ul></li>
<li><p>Programming Language</p>
<ul>
<li>Proficient: Java, C, MATLAB,Verilog, VHDL</li>
<li>Intermediate: Python, Shell, SQL</li>
</ul></li>
</ul>


</body></html>