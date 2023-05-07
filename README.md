Download Link: https://assignmentchef.com/product/solved-me5404-project2-q-learning-for-world-grid-navigation
<br>
This project is designed for the student to demonstrate (through independent learning):

<ol>

 <li>Competence in implementing the <em>Q</em>-learning algorithm, and</li>

 <li>Understanding of the principles of, and implementation issues related to, the <em>Q</em>-learning algorithm.</li>

</ol>

<h2>II. PROBLEM STATEMENT</h2>

Suppose that a robot is to traverse on a 10×10 grid, with the top-left and bottom-right cells being the start state and the goal state respectively, as illustrated in Figure 1.

<table>

 <tbody>

  <tr>

   <td width="118"></td>

  </tr>

  <tr>

   <td></td>

   <td></td>

  </tr>

 </tbody>

</table>

Fig. 1: Illustration of a 10×10 world grid with start state and goal state. The index of each cell follows the MATLAB column-wise convention.

The robot is to reach the goal state by maximizing the total reward of the trip. Note that the numbers (from 1 to 100) assigned to the individual cells represent the states; they do not represent the reward for the cells. At a state, the robot can take one of four actions (as shown in Figure 2) to move up (<em>a</em>=1), right (<em>a</em>=2), down (<em>a</em>= 3), or left (<em>a</em>=4), into the corresponding adjacent state deterministically.

Fig. 2: Possible actions of the robot at a given state.

The learning process will consist of a series of trials. In a trial the robot starts at the initial state (<em>s</em>=1) and makes transitions, according to the algorithm for <em>Q</em>-learning with ε-greedy exploration, until it reaches the goal state (<em>s</em>=100), upon which the trial ends. The above process repeats until the values of the <em>Q</em>-function converge to the optimal values. An optimal policy can be then obtained.

<h2>III. REQUIREMENT</h2>

<ol>

 <li><em> What to be done</em></li>

</ol>

There are two main tasks to be completed for this project.

<strong>Task1: </strong>Write a MATLAB (M-file) program to implement the <em>Q</em>-learning algorithm, using the reward function as given in task1.mat and with the ε-greedy exploration algorithm by setting ε<em><sub>k</sub></em>, α<em><sub>k </sub></em>and γ as specified in Table I.

<table width="691">

 <tbody>

  <tr>

   <td width="691">PETER C. Y. CHEN, 2021                                                                                                                                                                                                                                                                                                                   2</td>

  </tr>

 </tbody>

</table>

The file task1.mat is included in the zipfile that also contains this document. It can be directly loaded into MATLAB and contains the matrix variable reward (dimension: 100×4), in which each column corresponds to an action and each row to a state. For example, the reward for taking action <em>a</em>=3 at state <em>s</em>=1 to enter state <em>s</em>=2 is given by the (1<em>,</em>3) entry of reward, i.e., ρ(1<em>,</em>3<em>,</em>2)= reward(1<em>,</em>3). Note that rewards can be negative.

TABLE I: Parameter values and performance of <em>Q</em>-Learning

<table width="304">

 <tbody>

  <tr>

   <td rowspan="2" width="54">ε<em>k</em><em>,</em>α<em>k</em></td>

   <td colspan="2" width="134">No. of goal-reached runs</td>

   <td colspan="2" width="116">Execution time (sec.)</td>

  </tr>

  <tr>

   <td width="48">γ=0<em>.</em>5</td>

   <td width="86">γ=0<em>.</em>9</td>

   <td width="48">γ=0<em>.</em>5</td>

   <td width="68">γ=0<em>.</em>9</td>

  </tr>

  <tr>

   <td width="54"><u>1 </u><em>k</em></td>

   <td width="48">?</td>

   <td width="86">?</td>

   <td width="48">?</td>

   <td width="68">?</td>

  </tr>

  <tr>

   <td width="54"><u>100</u>100+<em>k</em></td>

   <td width="48">?</td>

   <td width="86">?</td>

   <td width="48">?</td>

   <td width="68">?</td>

  </tr>

  <tr>

   <td width="54">1+<em>log</em>(<em>k</em>)<em>k</em></td>

   <td width="48">?</td>

   <td width="86">?</td>

   <td width="48">?</td>

   <td width="68">?</td>

  </tr>

  <tr>

   <td width="54">1+5<em>log</em>(<em>k</em>)<em>k</em></td>

   <td width="48">?</td>

   <td width="86">?</td>

   <td width="48">?</td>

   <td width="68">?</td>

  </tr>

 </tbody>

</table>

In this task, ε<em><sub>k </sub></em>and α<em><sub>k </sub></em>are set to the same value. You are required to run your program 10 times (i.e., 10 runs) for each set of parameter values and record the number of times the goal state is reached. (<em>Note: It is possible that some of the runs may not yield an optimal policy that results in the robot reaching the goal state; these runs are not to be counted.</em>) The maximum number of trials in each run is set to 3000. The average program execution time of the “goal-reaching” runs is to be calculated and entered into the table (as indicated by “?”). The final output of your program should be an optimal policy (if the goal state is reached in any of the 10 runs), and the reward associated with this optimal policy. The optimal policy is to be expressed as a column vector containing the state transitions, and also illustrated (in your report) on a 10×10 grid with arrows marking the trajectory of the robot moving from state <em>s</em>=1 to state <em>s</em>=100.

<strong>Task 2: </strong>Write a MATLAB (M-file) program to implement <em>Q</em>-learning using your own values of the relevant parameters. Assume that the grid size is 10×10 and implement your program in a MATLAB M-file. This M-file will be used to find the optimal policy using a reward function not provided to the students, as part of the assessment

scheme discussed in Section V.

<ol>

 <li><em> What to submit</em></li>

 <li>A report (in a PDF file) describing the implementation and the results. It must contain a cover page showing:

  <ul>

   <li><em>student’s name,</em></li>

   <li><em>student number,</em></li>

   <li><em>student’s email address, </em>(iv) <em>name of module, and</em></li>

  </ul></li>

</ol>

(v) <em>project title.</em>

The report should be in PDF format and <u>no more </u>than ten pages (excluding the cover page). The name of the PDF file must be in the format:

StudentNumber_RL.pdf

<ol start="2">

 <li>The M-file programs as specified in the description of Task 1 and Task 2 in Section III-A above.</li>

 <li><em> How to submit</em></li>

</ol>

Only softcopy of the report (in PDF) and the MATLAB Mfile programs are to be submitted. Please put the report and the M-file programs in a folder. Use your student number as the folder name. Generate a non-passwordprotected zipfile of this folder and upload this zipfile to LumiNUS at:




Note: Make sure to upload your report into the correct folder as specified above.

<h2>IV. DEMO SESSION</h2>

A demo session, to be conducted by the teaching assistant, on the use of MATLAB for implementing the <em>Q</em>learning algorithm will be held during one of the lectures. Please check the schedule in the lecture slides for the specific date. Students are strongly advised to attend this

session.

<h2>V. ASSESSMENT</h2>

The project will be assessed based on the following criteria:

<ol>

 <li><em>Comments (with supporting argument) on the results obtained in </em>Task 1.</li>

 <li><em>Presentation</em>. This includes good report style, clarity, and conciseness.</li>

 <li><em>Performance of your M-file program for </em>Task 2 <em>(as described in Section III-A) in finding an optimal policy based on the reward function specified in a file </em>mat<em>. </em>Your M-file program must be workable in MATLAB</li>

</ol>

under the Windows environment. When qeval.mat is loaded into MATLAB, the MATLAB workspace will have a variable named qevalreward whose dimension is 100×4, with each column corresponding to an action and each row to a state (similar to the variable reward described above in Task 1). Your M-file program must be able to process and generate as fast as possible a column vector named qevalstates as output, whose <em>n<sup>th </sup></em>element is the state visited in the <em>n<sup>th </sup></em>transition. Also output a 10×10 grid showing the trajectory of the robot, along with the total reward. You can assume that the variable qevalreward is available in the MATLAB workspace when your M-file is run during assessment. When writing your M-file program, you can test its execution on your own by making up a qeval.mat file containing dummy sample values.