# cs-61---programming-assignment-4-solved
**TO GET THIS SOLUTION VISIT:** [CS 61 – Programming Assignment 4 Solved](https://www.ankitcodinghub.com/product/49443/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;49443&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;4&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (4 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS 61 - Programming Assignment 4 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (4 votes)    </div>
    </div>
<h1>Objective</h1>
The purpose of this assignment is to illustrate how the .FILL pseudo-op performs the task of translating textual decimal numbers (such as the string “+5392”) into actual numbers (i.e. five thousand three hundred and ninety two, represented of course as a 16-bit two’s complement binary value).

&nbsp;

<h1>High Level Description</h1>
Prompt the user to enter a signed multi-digit decimal number (max 5 digits) from the keyboard. Convert the string of decimal numeric digits into the corresponding 16-bit two’s complement number, stored in <strong>Rx</strong>​ <em>(i.e. one of the 8 registers: </em>​<em><u>you will be told which register at the start of the provided starter code</u></em>​<em>)</em>​.&nbsp; The range of acceptable values is [-32768, +32767]; the absence of a sign means the number is positive – i.e. the first character entered by the user may be ‘+’, ‘-‘, or a numeric digit – and nothing else.

&nbsp;

<h1>Your Tasks</h1>
Your program can be broken down into the following tasks:

<ol>
<li>​<u>Read in the initial character.</u>
<ul>
<li>If it is a ‘-‘, make the final result negative by setting a “flag” ​<em>(so if the “negative” flag is set, take the 2’s complement of </em>​<strong><em>Rx</em></strong>​<em> at the end). </em></li>
<li>If it is ‘+’ it can be ignored;</li>
<li>If it is a numeric digit, then the number is not negative, and the input is just the first numeric digit of the number.</li>
<li>In all three cases, you can then proceed to accept any remaining digits ​<em>(see item 2.)</em> If the initial character is a newline, the program can just terminate without any output. ● Any other initial character must be treated as an error ​<em>(see below)</em>​.</li>
</ul>
</li>
<li>​<u>Convert</u>​ the string of numeric digits input by the user into the binary number they represent <em>(</em>​ <em>see examples below)</em>​. To do this, you can follow this algorithm:
<ul>
<li>Initialize Rx (and any other registers as needed) to 0 – DO NOT do this by LD’ing 0 from memory!</li>
</ul>
</li>
</ol>
<em>There is a much simpler &amp; faster way – remember the “TIP” in your lab 1 notes! </em>

<ul>
<li>Convert each digit from ascii code to binary number as it is typed in, and add it to Rx; as each subsequent digit is entered, multiply Rx by #10, and repeat</li>
</ul>
<em>(go back to lab 1 &amp; assn 1 to recall how to multiply!)</em>

Stop when you detect the newline character (‘\n’ = x0A), ​<strong>or</strong>​ when you reach 5 input digits:

○ For example, if the user types ‘2’, then Rx will contain

#2 = b0000 0000 0000 0010

○ If the user then types ‘3’, making the string now read “23”, then Rx will contain&nbsp; 2 x #10 + 3 = #23 = b0000 0000 0001 0111

○ If the user then types ‘4’, making the string read “234”, then Rx will contain

#23 x #10 + 4 = #234 = b0000 0000 1110 1010

You must also perform ​<strong><em>input character validation</em></strong>​ with this assignment – i.e.&nbsp; reject any ​<em><u>non-numeric</u></em>​ input character. That is, if the user enters “+23g”, on detecting the non-numeric ‘g’, your program should output an error, discard all input, and&nbsp; ​<u>start over with the initial prompt</u>​ ​<em>(see sample output)</em>​.

&nbsp;

You must also ​<strong><em>count</em></strong>​ the number of characters entered – once it gets to 5 you should stop accepting new characters, and issue a newline (in this case, <u>​do not wait​</u> for the user to hit Enter).

&nbsp;

However, you do not have to detect overflow in this assignment – we will only test your code with inputs in the range [-32768, +32767].

<strong>&nbsp;</strong>

<h1>Expected / Sample output</h1>
<strong><em>Output </em></strong>

<ul>
<li>Prompt</li>
</ul>
○ “Input a positive or negative decimal number (max 5 digits), followed by ENTER\n” ● Error Message

○ “ERROR! invalid input\n”

&nbsp;

<strong><em>Example</em> </strong>

If the user enters “+7246”, your program should read the ‘+’, ‘7’, ‘2’, ‘4’, ‘6’ and end up with the value b0001 1100 0100 1110 ​<em>(which is the two’s complement representation of the number #7246, or x1C4E)</em> in ​<strong>the specified register</strong>​.

If the users enters “-14237”, your program should read the ‘-‘, ‘1’, ‘4’, ‘2’, ‘3’, ‘7’ and end up with the value #-14237 = xC863 = b11001000 01100011 in ​<strong>the specified register</strong>​.

&nbsp;

<strong><em><u>WARNING</u></em></strong><u>​</u><strong><em>: In the following examples, the final result is shown in R2, which may NOT be the one you will use. You will store your result in the register specified in the header in your starter code!! Make sure you get this right, or the grader will not work, and you will get 0/10! </em></strong>

&nbsp;

&nbsp;

<strong>&nbsp;</strong>

(Valid input with a negative sign)

&nbsp;

&nbsp;

(Valid input with a positive sign)

&nbsp;

&nbsp;

(Valid input with No sign)

&nbsp;

(Invalid initial input, followed by valid input)<strong> Note: </strong>

<ul>
<li>You must echo the digits as they are input (no “ghost writing”).</li>
<li>You do ​<strong>not</strong>​ have to output the converted binary number. It should simply be sitting happily in ​<strong>Rx</strong>​, where you can check it in the simpl interface.</li>
</ul>
<strong><em>Remember, the register in which to store your result is given to you in your code header. </em></strong>

<ul>
<li>What should happen when an error occurs?</li>
</ul>
○ Output “ERROR! invalid input” and start over,&nbsp; re-prompting the user for input ● Possible errors ​<em>(we will test for these!)</em>​:

○ Nothing entered before ENTER

<em>(this does not trigger an error message, it just terminates the program) </em>

○ only a sign is entered, no numeric digits – ​<em>error message, start over </em>

○ the first character entered is neither a sign nor a numeric digit – ​<em>error message, start over</em>

○ A subsequent character is not a digit – <em>error message, start over</em>​

– e.g. the sign character is entered twice, or a letter is entered in place of a digit ● <strong><em>The entire program must end with a </em></strong><u>​<strong><em>single</em></strong></u>​<strong><em> newline.</em></strong>

<em><u>EITHER</u></em>​ the user terminates digit entry with Enter ( &lt; 5 digits), <u>​<em>OR</em></u>​ the program issues its own newline after counting 5 digits – not both!

<strong>&nbsp;</strong>

Your code will obviously be tested with a range of different values:&nbsp; Make sure you do likewise!

&nbsp;

<strong>Uh</strong><u>…</u><strong>help? </strong>

Try writing this program out in C++/pseudocode before tackling it in LC3. Doing so often helps to simplify the process and usually only takes a few minutes if you think it through carefully.

To “flag”a negative number, initialize a designated register (say Ry) to 0, then set it to, say, -1 if the first character entered is a ‘-‘.

Treat the subsequent numeric digits as a positive number. Once you have translated that number into binary, test Ry and ​BRz MAKE_NEGATIVE​ to take the 2’s complement of the result if required.<strong> &nbsp; &nbsp;</strong>

<h1>Submission Instructions</h1>
Submit (“Upload”) your ​<strong>assignment4.asm</strong>​ file ​<em>(and ONLY that file!)</em>​ to the Programming Assignment 4 folder in Gradescope: the Autograder will run &amp; report your grade within a minute or so.

You may submit as many times as you like – your grade will be that of your last submission.

<em>If you wish to set your grade to a previous submission with a higher score, you may open your “Submission history” and “Activate” any other submission – that’s the one we will see.</em>

<strong>&nbsp;</strong>

<h1>Rubric</h1>
<ul>
<li>To pass the assignment, you need a score of &gt;= 80%.</li>
</ul>
The autograder will run several tests on your code, and assign a grade for each.

But certain errors ​<em>(run-time errors, incorrect usage of I/O routines, missing newlines, etc.)</em>​ may cause ALL tests to fail =&gt; 0/100! So submit early and study the autograder report carefully!!

&nbsp;

<ul>
<li><strong>You must use the template we provide</strong>​ – if you make ​<em><u>any</u></em>​ changes to the provided starter code, the autograder may not be able to interpret the output, resulting in a grade of 0.</li>
</ul>
<strong>&nbsp;</strong>

<strong>&nbsp;</strong>

<strong>&nbsp;</strong>

<strong>&nbsp;</strong>

&nbsp;

<strong>&nbsp;</strong>

<strong>&nbsp;</strong>

<strong>Comics?!Sweet!!</strong>

<strong>&nbsp;</strong>

Source:​ ​<a href="http://xkcd.com/237/">http://xkcd.com/237/</a>

<strong>&nbsp;</strong>
