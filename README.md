# A/B Testing
<div class="Section1">

**<u><span style="font-size:14.0pt;line-height:115%;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
color:black;mso-themecolor:text1">UDACITY, UD257 A/B TESTING</span></u>**

**<u><span style="font-size:13.0pt;
mso-bidi-font-size:11.0pt;mso-fareast-font-family:&quot;Times New Roman&quot;;mso-bidi-font-family:
Calibri;mso-bidi-theme-font:minor-latin;color:black;mso-themecolor:text1">Experiment Overview:</span></u>****<u><span style="font-size:12.0pt;mso-fareast-font-family:
&quot;Times New Roman&quot;;mso-bidi-font-family:Calibri;mso-bidi-theme-font:minor-latin;
color:black;mso-themecolor:text1"></span></u>**

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
mso-fareast-font-family:&quot;Times New Roman&quot;;color:black;mso-themecolor:text1">Udacity courses currently have two options on the home page: "start free trial", and "access course materials". If the student clicks "start free trial", they will be asked to enter their credit card information, and then they will be enrolled in a free trial for the paid version of the course. After 14 days, they will automatically be charged unless they cancel first. If the student clicks "access course materials", they will be able to view the videos and take the quizzes for free, but they will not receive coaching support or a verified certificate, and they will not submit their final project for feedback.</span>

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
mso-fareast-font-family:&quot;Times New Roman&quot;;color:black;mso-themecolor:text1"></span>

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
mso-fareast-font-family:&quot;Times New Roman&quot;;color:black;mso-themecolor:text1">In the experiment, Udacity tested a change where if the student clicked "start free trial", they were asked how much time they had available to devote to the course. If the student indicated 5 or more hours per week, they would be taken through the checkout process as usual. If they indicated fewer than 5 hours per week, a message would appear indicating that Udacity courses usually require a greater time commitment for successful completion, and suggesting that the student might like to access the course materials for free. At this point, the student would have the option to continue enrolling in the free trial, or access the course materials for free instead. </span>[<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:&quot;Times New Roman&quot;;
color:black;mso-themecolor:text1">This screenshot</span>](https://www.google.com/url?q=https://drive.google.com/a/knowlabs.com/file/d/0ByAfiG8HpNUMakVrS0s4cGN2TjQ/view?usp%3Dsharing&sa=D&ust=1473770329688000&usg=AFQjCNGdFGwbkSS6G6ePE4BmCbPAVS28CA)<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:&quot;Times New Roman&quot;;
color:black;mso-themecolor:text1"> shows what the experiment looks like.</span>

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
mso-fareast-font-family:&quot;Times New Roman&quot;;color:black;mso-themecolor:text1"></span>

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
mso-fareast-font-family:&quot;Times New Roman&quot;;color:black;mso-themecolor:text1">The hypothesis was that this might set clearer expectations for students upfront, thus reducing the number of frustrated students who left the free trial because they didn't have enough time—without significantly reducing the number of students to continue past the free trial and eventually complete the course. If this hypothesis held true, Udacity could improve the overall student experience and improve coaches' capacity to support students who are likely to complete the course.</span>

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
mso-fareast-font-family:&quot;Times New Roman&quot;;color:black;mso-themecolor:text1"></span>

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
mso-fareast-font-family:&quot;Times New Roman&quot;;color:black;mso-themecolor:text1">The unit of diversion is a cookie, although if the student enrolls in the free trial, they are tracked by user-id from that point forward. The same user-id cannot enroll in the free trial twice. For users that do not enroll, their user-id is not tracked in the experiment, even if they were signed in when they visited the course overview page.</span>

**<u><span style="font-size:13.0pt;
mso-bidi-font-size:11.0pt;mso-fareast-font-family:&quot;Times New Roman&quot;;mso-bidi-font-family:
Calibri;mso-bidi-theme-font:minor-latin;color:black;mso-themecolor:text1">Metric Choice</span></u>****<u><span style="font-size:13.0pt;mso-fareast-font-family:
&quot;Times New Roman&quot;;mso-bidi-font-family:Calibri;mso-bidi-theme-font:minor-latin;
color:black;mso-themecolor:text1"></span></u>**

*   <span style="font-family:
         &quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:&quot;Times New Roman&quot;;
         mso-bidi-font-weight:bold">Number of cookies**:**</span><span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:&quot;Times New Roman&quot;"> That is, number of unique cookies to view the course overview page. (d<sub>min</sub>=3000)</span>
*   <span style="font-family:
         &quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:&quot;Times New Roman&quot;;
         mso-bidi-font-weight:bold">Number of user-ids**:**</span><span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:&quot;Times New Roman&quot;"> That is, number of users who enroll in the free trial. (d<sub>min</sub>=50)</span>
*   <span style="font-family:
         &quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:&quot;Times New Roman&quot;;
         mso-bidi-font-weight:bold">Number of clicks**: **</span><span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:&quot;Times New Roman&quot;">That is, number of unique cookies to click the "Start free trial" button (which happens before the free trial screener is trigger). (d<sub>min</sub>=240)</span>
*   <span style="font-family:
         &quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:&quot;Times New Roman&quot;;
         mso-bidi-font-weight:bold">Click-through-probability**:**</span><span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:&quot;Times New Roman&quot;"> That is, number of unique cookies to click the "Start free trial" button divided by number of unique cookies to view the course overview page.(d<sub>min</sub>=0.01)</span>
*   <span style="font-family:
         &quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:&quot;Times New Roman&quot;;
         mso-bidi-font-weight:bold">Gross conversion**: **</span><span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:&quot;Times New Roman&quot;">That is, number of user-ids to complete checkout and enroll in the free trial divided by number of unique cookies to click the "Start free trial" button. (d<sub>min</sub>= 0.01)</span>
*   <span style="font-family:
         &quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:&quot;Times New Roman&quot;;
         mso-bidi-font-weight:bold">Retention**: **</span><span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:&quot;Times New Roman&quot;">That is, number of user-ids to remain enrolled past the 14-day boundary (and thus make at least one payment) divided by number of user-ids to complete checkout.(d<sub>min</sub>=0.01)</span>
*   <span style="font-family:
         &quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:&quot;Times New Roman&quot;;
         mso-bidi-font-weight:bold">Net conversion**: **</span><span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:&quot;Times New Roman&quot;">That is, number of user-ids to remain enrolled past the 14-day boundary (and thus make at least one payment) divided by the number of unique cookies to click the "Start free trial" button. (d<sub>min</sub>= 0.0075)</span>

**<u><span style="font-size:14.0pt;line-height:115%;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
color:black;mso-themecolor:text1"><o:p><span style="text-decoration:none"> </span></o:p></span></u>**

**<u><span style="font-size:13.0pt;line-height:115%;mso-bidi-font-family:
Calibri;mso-bidi-theme-font:minor-latin;color:black;mso-themecolor:text1">INVARIANT MERTICS</span></u>**

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
color:black;mso-themecolor:text1">An invariant metric should not change across experimental and control groups. After conducting the experiment, they are used to perform sanity check on results. Since screener pops up after clicking start free trial button. So **#page views /cookies**, #**clicks** & **click through rate** will remain unchanged. <span style="mso-spacerun:yes"> </span>_Gross Conversion, Retention, Net Conversion_ metrics get affected after screener so these should not be considered as Invariant metrics.</span><span style="color:black;mso-themecolor:text1"></span>

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:black;
mso-themecolor:text1">Therefore, invariant metrics chosen for the experiment are:</span>

<span style="font-size:12.0pt;
line-height:115%;font-family:Symbol;mso-fareast-font-family:Symbol;mso-bidi-font-family:
Symbol;color:black;mso-themecolor:text1"><span style="mso-list:Ignore">·<span style="font:7.0pt &quot;Times New Roman&quot;">        </span> </span></span><span style="font-size:12.0pt;line-height:115%;
font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:black;mso-themecolor:text1">Number of cookies</span>

<span style="font-size:12.0pt;
line-height:115%;font-family:Symbol;mso-fareast-font-family:Symbol;mso-bidi-font-family:
Symbol;color:black;mso-themecolor:text1"><span style="mso-list:Ignore">·<span style="font:7.0pt &quot;Times New Roman&quot;">        </span> </span></span><span style="font-size:12.0pt;line-height:115%;
font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:black;mso-themecolor:text1">Number of Clicks</span>

<span style="font-size:12.0pt;
line-height:115%;font-family:Symbol;mso-fareast-font-family:Symbol;mso-bidi-font-family:
Symbol;color:black;mso-themecolor:text1"><span style="mso-list:Ignore">·<span style="font:7.0pt &quot;Times New Roman&quot;">        </span> </span></span><span style="font-size:12.0pt;line-height:115%;
font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:black;mso-themecolor:text1">Click through Probability</span>

**<u><span style="font-size:13.0pt;line-height:115%;mso-bidi-font-family:
Calibri;mso-bidi-theme-font:minor-latin;color:black;mso-themecolor:text1">EVALUATION METRICS</span></u>**

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:black;
mso-themecolor:text1">Evaluation metrics are expected to change. Metrics which may help in evaluating the hypothesis should be considered as evaluation metrics.<span style="mso-spacerun:yes"> </span> They should occur after the screener.</span>

<span style="font-family:Symbol;
mso-fareast-font-family:Symbol;mso-bidi-font-family:Symbol;color:black;
mso-themecolor:text1"><span style="mso-list:Ignore">·<span style="font:7.0pt &quot;Times New Roman&quot;">        </span> </span></span><u><span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
color:black;mso-themecolor:text1">Number of<span style="mso-spacerun:yes"> </span> user-ids</span></u> <span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
color:black;mso-themecolor:text1">: It will not be considered as an evaluation metric as gross conversion is a fraction of<span style="mso-spacerun:yes"> </span> user-id and using gross conversion it’s a better way of tracking the effect of screener.</span>

<span style="font-family:Symbol;
mso-fareast-font-family:Symbol;mso-bidi-font-family:Symbol;color:black;
mso-themecolor:text1"><span style="mso-list:Ignore">·<span style="font:7.0pt &quot;Times New Roman&quot;">        </span> </span></span><u><span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
color:black;mso-themecolor:text1">Gross Conversion</span></u><span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:black;mso-themecolor:text1"><span style="mso-spacerun:yes">   </span> : It will be considered as an evaluation metric. It is the ratio of no. of user-ids & no. of unique clicks on “Start free trial”.</span>

<span style="font-family:Symbol;
mso-fareast-font-family:Symbol;mso-bidi-font-family:Symbol;color:black;
mso-themecolor:text1"><span style="mso-list:Ignore">·<span style="font:7.0pt &quot;Times New Roman&quot;">        </span> </span></span><u><span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
color:black;mso-themecolor:text1">Retention</span></u><span style="font-family:
&quot;Times New Roman&quot;,&quot;serif&quot;;color:black;mso-themecolor:text1"><span style="mso-spacerun:yes">     </span> : It will be considered as an evaluation metric. Since it is the ratio of no. of <span style="mso-spacerun:yes"> </span>people who made payments & no. of unique user-ids.</span>

<span style="font-family:Symbol;
mso-fareast-font-family:Symbol;mso-bidi-font-family:Symbol;color:black;
mso-themecolor:text1"><span style="mso-list:Ignore">·<span style="font:7.0pt &quot;Times New Roman&quot;">        </span> </span></span><u><span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
color:black;mso-themecolor:text1">Net Conversion</span></u><span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:black;mso-themecolor:text1">: It will be considered as an evaluation metric. Since it is the ratio of no. of people who made payments & no. of clicks on “Start free trial” button.</span>

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:black;
mso-themecolor:text1">Overall goal is to minimize student frustration that left free trial because they didn’t have enough time. For considering launch of this Test :</span>

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
mso-fareast-font-family:&quot;Times New Roman&quot;;color:black;mso-themecolor:text1"><span style="mso-list:Ignore">1.<span style="font:7.0pt &quot;Times New Roman&quot;">     </span> </span></span><span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
color:black;mso-themecolor:text1">Net Conversion should not decrease as students to continue past free trial would increase or remain same.</span>

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
mso-fareast-font-family:&quot;Times New Roman&quot;;color:black;mso-themecolor:text1"><span style="mso-list:Ignore">2.<span style="font:7.0pt &quot;Times New Roman&quot;">     </span> </span></span><span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
color:black;mso-themecolor:text1">Retention is students who stay after 14 days of trial. It should not be decreased.</span>

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
mso-fareast-font-family:&quot;Times New Roman&quot;;color:black;mso-themecolor:text1"><span style="mso-list:Ignore">3.<span style="font:7.0pt &quot;Times New Roman&quot;">     </span> </span></span><span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
color:black;mso-themecolor:text1">Gross Conversion should decrease as screener will filter out the students.</span>

**<u><span style="font-size:13.0pt;
mso-fareast-font-family:&quot;Times New Roman&quot;;mso-bidi-font-family:Calibri;
mso-bidi-theme-font:minor-latin;color:black;mso-themecolor:text1">MEASURING STANDARD DEVIATION</span></u>**

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
mso-fareast-font-family:&quot;Times New Roman&quot;;color:black;mso-themecolor:text1">Using the rough estimates of the</span> [<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:&quot;Times New Roman&quot;;
color:black;mso-themecolor:text1">baseline values</span>](https://www.google.com/url?q=https://docs.google.com/a/knowlabs.com/spreadsheets/d/1MYNUtC47Pg8hdoCjOXaHqF-thheGpUshrFA21BAJnNc/edit%23gid%3D0&sa=D&ust=1473820552534000&usg=AFQjCNGwSQH8MskY1k6flVxDVcP3-U2yLw) <span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:&quot;Times New Roman&quot;;
color:black;mso-themecolor:text1">for the metrics, we have calculated Standard Deviation of evaluation metrics analytically.</span>

| 

**<span style="font-size:13.0pt;font-family:&quot;Roboto&quot;,&quot;serif&quot;;mso-fareast-font-family:
  &quot;Times New Roman&quot;;mso-bidi-font-family:&quot;Times New Roman&quot;;color:black;
  mso-themecolor:text1">Gross Conversion</span>**

 | 

**<span style="font-size:13.0pt;font-family:&quot;Roboto&quot;,&quot;serif&quot;;mso-fareast-font-family:
  &quot;Times New Roman&quot;;mso-bidi-font-family:&quot;Times New Roman&quot;;color:black;
  mso-themecolor:text1">0.0202</span>**

 |
| 

**<span style="font-size:13.0pt;font-family:&quot;Roboto&quot;,&quot;serif&quot;;mso-fareast-font-family:
  &quot;Times New Roman&quot;;mso-bidi-font-family:&quot;Times New Roman&quot;;color:black;
  mso-themecolor:text1">Retention</span>**

 | 

**<span style="font-size:13.0pt;font-family:&quot;Roboto&quot;,&quot;serif&quot;;
  mso-fareast-font-family:&quot;Times New Roman&quot;;mso-bidi-font-family:&quot;Times New Roman&quot;;
  color:black;mso-themecolor:text1">0.0549</span>**

 |
| 

**<span style="font-size:13.0pt;font-family:&quot;Roboto&quot;,&quot;serif&quot;;mso-fareast-font-family:
  &quot;Times New Roman&quot;;mso-bidi-font-family:&quot;Times New Roman&quot;;color:black;
  mso-themecolor:text1">Net Conversion</span>**

 | 

**<span style="font-size:13.0pt;font-family:&quot;Roboto&quot;,&quot;serif&quot;;mso-fareast-font-family:
  &quot;Times New Roman&quot;;mso-bidi-font-family:&quot;Times New Roman&quot;;color:black;
  mso-themecolor:text1">0.0156</span>**

 |

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
mso-fareast-font-family:&quot;Times New Roman&quot;;color:black;mso-themecolor:text1">For Gross Conversion & Net Conversion, the unit of diversion is equal to unit of analysis. So, the analytical estimate of S.D. tends to be empirical estimate of S.D. But in case of Retention Unit of diversion is not same as unit of analysis. After calculating cookies, duration & exposure, if we decide keep retention, we have to calculate empirical variability of retention.</span>

**<u><span style="font-size:14.0pt;
mso-fareast-font-family:&quot;Times New Roman&quot;;mso-bidi-font-family:Calibri;
mso-bidi-theme-font:minor-latin;color:black;mso-themecolor:text1">SIZING</span></u>****<u><span style="font-size:13.0pt;
mso-fareast-font-family:&quot;Times New Roman&quot;;mso-bidi-font-family:Calibri;
mso-bidi-theme-font:minor-latin;color:black;mso-themecolor:text1"></span></u>**

### <u><span style="font-size:13.0pt;line-height:115%;font-family:&quot;Calibri&quot;,&quot;sans-serif&quot;;
mso-ascii-theme-font:minor-latin;mso-hansi-theme-font:minor-latin;mso-bidi-theme-font:
minor-latin;color:black;mso-themecolor:text1">NUMBER OF SAMPLES VS. POWER</span></u>

<span style="color:black;mso-themecolor:text1">We are not using Bonferroni correction. Bonferroni correction is too conservative for these metrics. I want all my metrics to be significant.</span>

**<span style="font-size:12.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
color:black;mso-themecolor:text1">α = 0.05</span>** <span style="font-size:12.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:black;
mso-themecolor:text1">& **β= 0.2**</span>

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
color:black;mso-themecolor:text1">Ratio of page views to clicks =<span style="mso-spacerun:yes"> </span> </span><span style="font-size:11.0pt;line-height:115%;font-family:&quot;Calibri&quot;,&quot;sans-serif&quot;;
mso-ascii-theme-font:minor-latin;mso-fareast-font-family:Calibri;mso-fareast-theme-font:
minor-latin;mso-hansi-theme-font:minor-latin;mso-bidi-font-family:&quot;Times New Roman&quot;;
mso-bidi-theme-font:minor-bidi;position:relative;top:8.5pt;mso-text-raise:-8.5pt;
mso-ansi-language:EN-US;mso-fareast-language:EN-US;mso-bidi-language:AR-SA">![](UDACITY-AB_Testing_files/image002.gif)</span><span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:&quot;Times New Roman&quot;;
mso-fareast-theme-font:minor-fareast;color:black;mso-themecolor:text1"><span style="mso-spacerun:yes"> </span>= 0.08</span>

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
mso-fareast-font-family:&quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;
color:black;mso-themecolor:text1">Ratio of page views to enrollments =<span style="mso-spacerun:yes"> </span> </span><span style="font-size:11.0pt;line-height:115%;font-family:&quot;Calibri&quot;,&quot;sans-serif&quot;;
mso-ascii-theme-font:minor-latin;mso-fareast-font-family:Calibri;mso-fareast-theme-font:
minor-latin;mso-hansi-theme-font:minor-latin;mso-bidi-font-family:&quot;Times New Roman&quot;;
mso-bidi-theme-font:minor-bidi;position:relative;top:8.5pt;mso-text-raise:-8.5pt;
mso-ansi-language:EN-US;mso-fareast-language:EN-US;mso-bidi-language:AR-SA">![](UDACITY-AB_Testing_files/image004.gif)</span><span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:&quot;Times New Roman&quot;;
mso-fareast-theme-font:minor-fareast;color:black;mso-themecolor:text1"><span style="mso-spacerun:yes"> </span>= 0.0165</span><span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
color:black;mso-themecolor:text1"></span>

<span style="color:black;mso-themecolor:text1">No. of page views for Gross Conversion =</span> <span style="font-size:11.0pt;line-height:115%;font-family:&quot;Calibri&quot;,&quot;sans-serif&quot;;
mso-ascii-theme-font:minor-latin;mso-fareast-font-family:Calibri;mso-fareast-theme-font:
minor-latin;mso-hansi-theme-font:minor-latin;mso-bidi-font-family:&quot;Times New Roman&quot;;
mso-bidi-theme-font:minor-bidi;position:relative;top:8.5pt;mso-text-raise:-8.5pt;
mso-ansi-language:EN-US;mso-fareast-language:EN-US;mso-bidi-language:AR-SA">![](UDACITY-AB_Testing_files/image006.gif)</span><span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:&quot;Times New Roman&quot;;
mso-fareast-theme-font:minor-fareast;color:black;mso-themecolor:text1"><span style="mso-spacerun:yes"> </span> =645875</span>

<span style="color:black;mso-themecolor:text1">No. of page views for Retention =<span style="mso-spacerun:yes"> </span> </span><span style="font-size:11.0pt;line-height:115%;font-family:&quot;Calibri&quot;,&quot;sans-serif&quot;;
mso-ascii-theme-font:minor-latin;mso-fareast-font-family:Calibri;mso-fareast-theme-font:
minor-latin;mso-hansi-theme-font:minor-latin;mso-bidi-font-family:&quot;Times New Roman&quot;;
mso-bidi-theme-font:minor-bidi;position:relative;top:8.5pt;mso-text-raise:-8.5pt;
mso-ansi-language:EN-US;mso-fareast-language:EN-US;mso-bidi-language:AR-SA">![](UDACITY-AB_Testing_files/image008.gif)</span><span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:&quot;Times New Roman&quot;;
mso-fareast-theme-font:minor-fareast;color:black;mso-themecolor:text1"><span style="mso-spacerun:yes"> </span> = 4741212</span>

<span style="color:black;mso-themecolor:text1">No. of page views for Net Conversion =</span> <span style="font-size:11.0pt;line-height:115%;font-family:&quot;Calibri&quot;,&quot;sans-serif&quot;;
mso-ascii-theme-font:minor-latin;mso-fareast-font-family:Calibri;mso-fareast-theme-font:
minor-latin;mso-hansi-theme-font:minor-latin;mso-bidi-font-family:&quot;Times New Roman&quot;;
mso-bidi-theme-font:minor-bidi;position:relative;top:8.5pt;mso-text-raise:-8.5pt;
mso-ansi-language:EN-US;mso-fareast-language:EN-US;mso-bidi-language:AR-SA">![](UDACITY-AB_Testing_files/image010.gif)</span><span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:&quot;Times New Roman&quot;;
mso-fareast-theme-font:minor-fareast;color:black;mso-themecolor:text1"><span style="mso-spacerun:yes"> </span> =685325</span>

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
mso-fareast-font-family:&quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;
color:black;mso-themecolor:text1">We will have to satisfy all our conditions so, will select maximum no. of pageviews.</span>

| 

**<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  mso-fareast-font-family:&quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;
  color:black;mso-themecolor:text1">No of Page Views</span> **<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:&quot;Times New Roman&quot;;
  mso-fareast-theme-font:minor-fareast;color:black;mso-themecolor:text1">=</span>

 | 

**<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  mso-fareast-font-family:&quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;
  color:black;mso-themecolor:text1">4741212</span>**

 |

### <span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
mso-fareast-font-family:&quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;
color:black;mso-themecolor:text1;font-weight:normal"></span>

### <u><span style="font-size:13.0pt;line-height:115%;font-family:&quot;Calibri&quot;,&quot;sans-serif&quot;;
mso-ascii-theme-font:minor-latin;mso-hansi-theme-font:minor-latin;mso-bidi-theme-font:
minor-latin;color:black;mso-themecolor:text1">DURATION vs EXPOSURE</span></u>

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
color:black;mso-themecolor:text1">Duration can be calculated based upon the exposure which is inversely proportional to the Risk involved. Here, the screener is reminder about time commitment, it constitutes minimal risk. None of the participants will suffer from physical harm nor is the data too sensitive, so even if we will give more than 50% exposure it will be okay.<span style="mso-spacerun:yes"> </span> I am considering 75% exposure.</span>

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
color:black;mso-themecolor:text1">No. of days for 4741212 page views with 75% exposure =<span style="mso-spacerun:yes"> </span> </span><span style="font-size:11.0pt;line-height:115%;font-family:&quot;Calibri&quot;,&quot;sans-serif&quot;;
mso-ascii-theme-font:minor-latin;mso-fareast-font-family:Calibri;mso-fareast-theme-font:
minor-latin;mso-hansi-theme-font:minor-latin;mso-bidi-font-family:&quot;Times New Roman&quot;;
mso-bidi-theme-font:minor-bidi;position:relative;top:8.5pt;mso-text-raise:-8.5pt;
mso-ansi-language:EN-US;mso-fareast-language:EN-US;mso-bidi-language:AR-SA">![](UDACITY-AB_Testing_files/image012.gif)</span><span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:&quot;Times New Roman&quot;;
mso-fareast-theme-font:minor-fareast;color:black;mso-themecolor:text1"><span style="mso-spacerun:yes"> </span> ~ 158 days</span>

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
mso-fareast-font-family:&quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;
color:black;mso-themecolor:text1">It’s a long time period and we should reduce the time duration.<span style="mso-spacerun:yes"> </span> We can exclude Retention as an evaluation metric and will consider Net conversion, with revised no. of page views as 685325.</span>

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
color:black;mso-themecolor:text1">No. of days for</span> <span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:&quot;Times New Roman&quot;;
mso-fareast-theme-font:minor-fareast;color:black;mso-themecolor:text1">685325</span><span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:black;mso-themecolor:text1">page views with 75% exposure =<span style="mso-spacerun:yes"> </span> </span><span style="font-size:11.0pt;line-height:115%;font-family:&quot;Calibri&quot;,&quot;sans-serif&quot;;
mso-ascii-theme-font:minor-latin;mso-fareast-font-family:Calibri;mso-fareast-theme-font:
minor-latin;mso-hansi-theme-font:minor-latin;mso-bidi-font-family:&quot;Times New Roman&quot;;
mso-bidi-theme-font:minor-bidi;position:relative;top:8.5pt;mso-text-raise:-8.5pt;
mso-ansi-language:EN-US;mso-fareast-language:EN-US;mso-bidi-language:AR-SA">![](UDACITY-AB_Testing_files/image014.gif)</span><span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:&quot;Times New Roman&quot;;
mso-fareast-theme-font:minor-fareast;color:black;mso-themecolor:text1"><span style="mso-spacerun:yes"> </span> ~ 23 days</span>

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
mso-fareast-font-family:&quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;
color:black;mso-themecolor:text1">Excluding retention as a metric still allows us to test our hypothesis with net conversion. The two metrics are correlated. Retention measures the difference in the rate at which people drops from enroll to completion of trial. Net conversion uses the no. of users to complete the trial and retains even after the trail. So there is no such issue even after excluding Retention as a metric.</span>

<span style="color:black;mso-themecolor:text1"></span>

<span style="color:black;mso-themecolor:text1"></span>

## <u><span style="font-size:14.0pt;font-family:&quot;Calibri&quot;,&quot;sans-serif&quot;;mso-ascii-theme-font:
minor-latin;mso-hansi-theme-font:minor-latin;mso-bidi-theme-font:minor-latin;
color:black;mso-themecolor:text1;mso-bidi-font-weight:normal">EXPERIMENT ANALYSIS</span></u><u><span style="font-size:13.0pt;font-family:&quot;Calibri&quot;,&quot;sans-serif&quot;;
mso-ascii-theme-font:minor-latin;mso-hansi-theme-font:minor-latin;mso-bidi-theme-font:
minor-latin;color:black;mso-themecolor:text1">: SANITY CHECKS</span></u><u><span style="font-family:&quot;Calibri&quot;,&quot;sans-serif&quot;;mso-ascii-theme-font:minor-latin;
mso-hansi-theme-font:minor-latin;mso-bidi-theme-font:minor-latin;color:black;
mso-themecolor:text1"></span></u>

## <u><span style="font-size:13.0pt;font-family:&quot;Calibri&quot;,&quot;sans-serif&quot;;mso-ascii-theme-font:
minor-latin;mso-hansi-theme-font:minor-latin;mso-bidi-theme-font:minor-latin;
color:black;mso-themecolor:text1"><o:p><span style="text-decoration:none"> </span></o:p></span></u>

| 

**<span style="font-size:12.0pt;
  line-height:150%;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:
  &quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;color:black;
  mso-themecolor:text1">Metric</span>**

 | 

**<span style="font-size:12.0pt;
  line-height:150%;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:
  &quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;color:black;
  mso-themecolor:text1">Lower Bound</span>**

 | 

**<span style="font-size:12.0pt;
  line-height:150%;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:
  &quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;color:black;
  mso-themecolor:text1">Upper Bound</span>**

 | 

**<span style="font-size:12.0pt;
  line-height:150%;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:
  &quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;color:black;
  mso-themecolor:text1">Observed Value</span>**

 | 

**<span style="font-size:12.0pt;
  line-height:150%;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:
  &quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;color:black;
  mso-themecolor:text1">Result</span>**

 |
| 

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:
  &quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;color:black;
  mso-themecolor:text1">No. of Cookies</span>

 | 

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:
  &quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;color:black;
  mso-themecolor:text1">0.4988203921</span>

 | 

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:
  &quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;color:black;
  mso-themecolor:text1">0.5011796079</span>

 | 

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:
  &quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;color:black;
  mso-themecolor:text1">0.5006396669</span>

 | 

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:
  &quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;color:black;
  mso-themecolor:text1">Pass</span>

 |
| 

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:
  &quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;color:black;
  mso-themecolor:text1">No. Clicks</span>

 | 

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:
  &quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;color:black;
  mso-themecolor:text1">0.4958844957</span>

 | 

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:
  &quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;color:black;
  mso-themecolor:text1">0.5041155043</span>

 | 

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:
  &quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;color:black;
  mso-themecolor:text1">0.5004673474</span>

 | 

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:
  &quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;color:black;
  mso-themecolor:text1">Pass</span>

 |
| 

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:
  &quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;color:black;
  mso-themecolor:text1">Click through probability</span>

 | 

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:
  &quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;color:black;
  mso-themecolor:text1">0.08121035975</span>

 | 

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:
  &quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;color:black;
  mso-themecolor:text1">0.0830412674</span>

 | 

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:
  &quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;color:black;
  mso-themecolor:text1">0.08212581357</span>

 | 

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:
  &quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;color:black;
  mso-themecolor:text1">Pass</span>

 |

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
mso-fareast-font-family:&quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;
color:black;mso-themecolor:text1"></span>

### <u><span style="font-size:14.0pt;line-height:115%;font-family:&quot;Calibri&quot;,&quot;sans-serif&quot;;
mso-ascii-theme-font:minor-latin;mso-hansi-theme-font:minor-latin;mso-bidi-theme-font:
minor-latin;color:black;mso-themecolor:text1">RESULT ANALYSIS</span></u>

### <u><span style="font-size:13.0pt;line-height:115%;font-family:&quot;Calibri&quot;,&quot;sans-serif&quot;;
mso-ascii-theme-font:minor-latin;mso-hansi-theme-font:minor-latin;mso-bidi-theme-font:
minor-latin;color:black;mso-themecolor:text1"><o:p><span style="text-decoration:
 none"> </span></o:p></span></u>

### <u><span style="font-size:13.0pt;line-height:115%;font-family:&quot;Calibri&quot;,&quot;sans-serif&quot;;
mso-ascii-theme-font:minor-latin;mso-hansi-theme-font:minor-latin;mso-bidi-theme-font:
minor-latin;color:black;mso-themecolor:text1">EFFECT SIZE TESTS</span></u>

<span style="font-size:11.0pt;color:black;mso-themecolor:text1">95% Confidence interval around the difference between the experiment and control group for evaluation metrics.</span>

| 

**<span style="color:black;mso-themecolor:text1">Metric</span>**

 | 

**<span style="color:black;mso-themecolor:text1">d<sub>min</sub></span>**

 | 

**<span style="color:black;mso-themecolor:text1">LB</span>**

 | 

**<span style="color:black;mso-themecolor:text1">UB</span>**

 | 

**<span style="color:black;mso-themecolor:text1">Statistical Sign</span>**

 | 

**<span style="color:black;mso-themecolor:text1">Practical Sign</span>**

 |
| 

<span style="font-size:11.0pt;color:black;mso-themecolor:
  text1">Gross Conv</span>

 | 

<span style="font-size:11.0pt;color:black;mso-themecolor:
  text1">0.01</span>

 | 

<span style="font-size:11.0pt;color:black;mso-themecolor:
  text1">-0.029123358</span>

 | 

<span style="font-size:11.0pt;color:black;mso-themecolor:
  text1">-0.011986390</span>

 | 

<span style="font-size:11.0pt;color:black;mso-themecolor:
  text1">True</span>

 | 

<span style="font-size:11.0pt;color:black;mso-themecolor:
  text1">True</span>

 |
| 

<span style="font-size:11.0pt;color:black;mso-themecolor:
  text1">Net Conv</span>

 | 

<span style="font-size:11.0pt;color:black;mso-themecolor:
  text1">0.01</span>

 | 

<span style="font-size:11.0pt;color:black;mso-themecolor:
  text1">-0.0116046244</span>

 | 

<span style="font-size:11.0pt;color:black;mso-themecolor:
  text1">0.001857178971</span>

 | 

<span style="font-size:11.0pt;color:black;mso-themecolor:
  text1">False</span>

 | 

<span style="font-size:11.0pt;color:black;mso-themecolor:
  text1">False</span>

 |

<span style="font-size:11.0pt;
color:black;mso-themecolor:text1"></span>

<span style="font-size:11.0pt;
color:black;mso-themecolor:text1">Gross Conversion is both Statistical Significant and Practical Significant</span>

<span style="font-size:11.0pt;
color:black;mso-themecolor:text1">Net Conversion is neither Statistical Significant nor Practical Significant</span>

<span style="font-size:11.0pt;
color:black;mso-themecolor:text1"></span>

### <u><span style="font-size:13.0pt;line-height:115%;font-family:&quot;Calibri&quot;,&quot;sans-serif&quot;;
mso-ascii-theme-font:minor-latin;mso-hansi-theme-font:minor-latin;mso-bidi-theme-font:
minor-latin;color:black;mso-themecolor:text1">SIGN TESTS</span></u>

| 

**<span style="font-size:12.0pt;
  line-height:150%;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:
  &quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;color:black;
  mso-themecolor:text1">Metric</span>**

 | 

**<span style="font-size:12.0pt;
  line-height:150%;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:
  &quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;color:black;
  mso-themecolor:text1">p-value</span>**

 | 

**<span style="font-size:12.0pt;
  line-height:150%;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:
  &quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;color:black;
  mso-themecolor:text1">Statistically Significant</span>**

 |
| 

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:
  &quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;color:black;
  mso-themecolor:text1">Gross Conversion</span>

 | 

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:
  &quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;color:black;
  mso-themecolor:text1">0.0026</span>

 | 

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:
  &quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;color:black;
  mso-themecolor:text1">Yes</span>

 |
| 

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:
  &quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;color:black;
  mso-themecolor:text1">Net Conversion</span>

 | 

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:
  &quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;color:black;
  mso-themecolor:text1">0.6776</span>

 | 

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:
  &quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;color:black;
  mso-themecolor:text1">No</span>

 |

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
mso-fareast-font-family:&quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;
color:black;mso-themecolor:text1"></span>

**<u><span style="font-size:14.0pt;line-height:150%;mso-fareast-font-family:&quot;Times New Roman&quot;;
mso-fareast-theme-font:minor-fareast;mso-bidi-font-family:Calibri;mso-bidi-theme-font:
minor-latin;color:black;mso-themecolor:text1">SUMMARY</span></u>**

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
color:black;mso-themecolor:text1"><span style="mso-spacerun:yes"> </span>Bonferroni correction is not used here because our launch decision is based upon two metrics Gross Conversion & Net Conversion. In order to launch, we need both the metrics to match our expectation. We risk not launching as if at least one metric (out of 2) fail to reject null, when null is not the true effect.</span>

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
color:black;mso-themecolor:text1">If we were to launch the experiment when any metric would match our expectations, then we would have to use Bonferroni correction</span><span style="font-size:10.5pt;line-height:115%;font-family:
&quot;Arial&quot;,&quot;sans-serif&quot;;color:#58646D;background:white">.</span> <span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:black;mso-themecolor:text1">Bonferroni is used to reduce risk but can only be used conditionally.</span>

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:black;mso-themecolor:text1">The sign test mirrors that of size test, that gross conversion is significant but net conversion is not. Both the tests are giving same results on being metrics to significant, so no further study is required.</span><span style="font-size:
13.0pt;line-height:115%;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:black;
mso-themecolor:text1">
</span>**<span style="font-size:13.0pt;line-height:115%;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
mso-fareast-font-family:&quot;Times New Roman&quot;;color:black;mso-themecolor:text1"></span>**

## <u><span style="font-size:14.0pt;font-family:&quot;Calibri&quot;,&quot;sans-serif&quot;;mso-ascii-theme-font:
minor-latin;mso-hansi-theme-font:minor-latin;mso-bidi-theme-font:minor-latin;
color:black;mso-themecolor:text1">RECOMMENDATION</span></u>

<span style="color:black;mso-themecolor:text1">
</span><span style="font-size:11.0pt;color:black;mso-themecolor:text1">For making a recommendation on whether to launch screener or not, we need to check evaluation metrics.</span>

<span style="font-size:11.0pt;color:black;mso-themecolor:
text1">Gross Conversion is both statistically & practically significant; it means we are successful in decreasing the no. of enrollments.</span>

<span style="font-size:11.0pt;color:black;mso-themecolor:
text1">Net Conversion is neither statistically nor practically significant. The CI of Netconversion includes negative of practical significance boundary. So, the no. of people who will stay past trial could reduce. This is risky & not a good change according to this metric.</span>

<span style="font-size:11.0pt;color:black;mso-themecolor:
text1">Considering both the points, we should not launch the experiment.</span>

**<u><span style="font-size:14.0pt;font-family:&quot;Calibri&quot;,&quot;sans-serif&quot;;
mso-ascii-theme-font:minor-latin;mso-hansi-theme-font:minor-latin;mso-bidi-theme-font:
minor-latin;color:black;mso-themecolor:text1"><o:p><span style="text-decoration:
 none"> </span></o:p></span></u>**

**<u><span style="font-size:14.0pt;font-family:&quot;Calibri&quot;,&quot;sans-serif&quot;;
mso-ascii-theme-font:minor-latin;mso-hansi-theme-font:minor-latin;mso-bidi-theme-font:
minor-latin;color:black;mso-themecolor:text1">FOLLOW-UP EXPERIMENT</span></u>**

<span style="font-size:11.0pt;
color:black;mso-themecolor:text1">We can perform another experiment by changing the number of hours from screener to prerequisite knowledge required to pursue that course. This screener may help students to get an idea about what knowledge they should have before joining Udacity course. If the student does not have that knowledge, he/she may click on suggested courses that are listed in prerequisites and can join those particular courses.</span>

**<span style="font-size:11.0pt;color:black;
mso-themecolor:text1">Null Hypothesis:</span>**<span class="apple-converted-space"><span style="font-size:11.0pt;color:black;
mso-themecolor:text1"> </span></span><span style="font-size:11.0pt;
color:black;mso-themecolor:text1">No significant difference between control and experiment groups.</span>

**<span style="font-size:11.0pt;color:black;mso-themecolor:text1">Unit of diversion</span>** <span style="font-size:11.0pt;color:black;mso-themecolor:text1">= Cookie</span>

<span style="font-size:11.0pt;color:black;mso-themecolor:
text1">For testing this hypothesis, we have to measure #cookies, #clicks , #enrollments, #Payments and from these we will calculate Gross Conversion & Net Conversion.</span>

<span style="font-size:11.0pt;color:black;mso-themecolor:
text1">If Gross Conversion & Net Conversion will result to be statistically & practically significant then we will be able to launch our test.</span>

<span style="font-size:16.0pt;font-family:&quot;Roboto&quot;,&quot;serif&quot;;
color:black;mso-themecolor:text1"></span>

<span style="color:black;mso-themecolor:text1"></span>

**<u><span style="font-size:13.0pt;
line-height:150%;mso-fareast-font-family:&quot;Times New Roman&quot;;mso-fareast-theme-font:
minor-fareast;mso-bidi-font-family:Calibri;mso-bidi-theme-font:minor-latin;
color:black;mso-themecolor:text1">REFERENCES:</span></u>****<u><span style="font-size:12.0pt;
line-height:150%;mso-fareast-font-family:&quot;Times New Roman&quot;;mso-fareast-theme-font:
minor-fareast;mso-bidi-font-family:Calibri;mso-bidi-theme-font:minor-latin;
color:black;mso-themecolor:text1"></span></u>**

<span style="font-size:12.0pt;line-height:150%;mso-bidi-font-family:Calibri;
mso-bidi-theme-font:minor-latin"><span style="mso-list:Ignore">1.<span style="font:7.0pt &quot;Times New Roman&quot;">     </span> </span></span><span style="font-size:12.0pt;line-height:150%;mso-fareast-font-family:&quot;Times New Roman&quot;;
mso-fareast-theme-font:minor-fareast;mso-bidi-font-family:Calibri;mso-bidi-theme-font:
minor-latin;color:black;mso-themecolor:text1">Udacity Discussion forum</span><span style="font-size:12.0pt;line-height:150%;mso-fareast-font-family:&quot;Times New Roman&quot;;
mso-fareast-theme-font:minor-fareast;mso-bidi-font-family:Calibri;mso-bidi-theme-font:
minor-latin;color:#548DD4;mso-themecolor:text2;mso-themetint:153"></span>

<span style="font-size:12.0pt;line-height:150%;mso-bidi-font-family:Calibri;
mso-bidi-theme-font:minor-latin"><span style="mso-list:Ignore">2.<span style="font:7.0pt &quot;Times New Roman&quot;">     </span> </span></span>[<span style="font-size:12.0pt;line-height:150%;mso-fareast-font-family:&quot;Times New Roman&quot;;
mso-fareast-theme-font:minor-fareast;mso-bidi-font-family:Calibri;mso-bidi-theme-font:
minor-latin;color:#365F91;mso-themecolor:accent1;mso-themeshade:191">http://www.exp-platform.com/Documents/controlledExperimentDMKD.pdf</span>](http://www.exp-platform.com/Documents/controlledExperimentDMKD.pdf)<span style="font-size:12.0pt;line-height:150%;mso-fareast-font-family:&quot;Times New Roman&quot;;
mso-fareast-theme-font:minor-fareast;mso-bidi-font-family:Calibri;mso-bidi-theme-font:
minor-latin;color:#365F91;mso-themecolor:accent1;mso-themeshade:191"></span>

<span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:&quot;Times New Roman&quot;"><span style="mso-list:Ignore">3.<span style="font:7.0pt &quot;Times New Roman&quot;">     </span> </span></span><u><span style="font-size:12.0pt;line-height:
150%;mso-fareast-font-family:&quot;Times New Roman&quot;;mso-fareast-theme-font:minor-fareast;
mso-bidi-font-family:Calibri;mso-bidi-theme-font:minor-latin;color:#365F91;
mso-themecolor:accent1;mso-themeshade:191">http://support.minitab.com/en-us/minitab/17/topic-library/basic-statistics-and-graphs/hypothesis-tests/basics/type-i-and-type-ii-error/</span></u><span style="font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-fareast-font-family:&quot;Times New Roman&quot;;
mso-fareast-theme-font:minor-fareast;color:black;mso-themecolor:text1"></span>

</div>
