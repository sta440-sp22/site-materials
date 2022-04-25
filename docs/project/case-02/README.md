# Instructions

This README corresponds to Case Study 2 regarding the 18th Chopin Competition.
**Read this file carefully.**

### Deadline and submission

Report and reproducible code for the initial submission will be due on
**Friday, February 25**. Final case team submission and formal response 
to review will be due on **Friday, March 18**. You will be asked to 
anonymously evaluate your team members after the final case team submission.

There is a **length limit of 8 pages** (*including* tables and figures for the
report. Supplemental figures/tables and other information may be provided in an
appendix following the main text.

You must submit a .pdf document to Gradescope that corresponds to an .Rmd file
on your GitHub repository in order to receive credit for this case study. If one
is not uploaded to Gradescope by the submission deadline, your latest commit 
prior to the deadline will be used as your submission. 

Your team's GitHub repository and commit history will also be evaluated by the 
instructor. The GitHub repository must contain the reproducible R Markdown 
document corresponding to the submitted reports, and will be checked throughout 
the course of the case study to ensure all team members are making meaningful
contributions to the project. Insufficient individual contribution as based on
the anonymous case team review and commit history **will** result in grade
reductions.

### Guidelines

- This is an team assignment, with teams randomly assigned by the instructor.
- Everything in your repository is for your team's eyes only except for the 
instructor or TAs.
- As always, you must cite any code you use as inspiration. A failure to cite is
plagiarism.

### Academic integrity

By submitting an assignment, you pledge to uphold the Duke Community Standard:

- I will not lie, cheat, or steal in my academic endeavors;
- I will conduct myself honorably in all my endeavors; and
- I will act if the Standard is compromised.

# Data 

The data are in a single file, `chopin_2021.csv`, which contains the results 
and repertoire choices (in order) for each of the competitors in the 18th
International Chopin Competition.

The official rules to the competition are available online. However, I encourage you to read the Wikipedia page here (https://en.wikipedia.org/wiki/XVIII_International_Chopin_Piano_Competition), as it has a great summary of the rules and format of the competition.

**Of particular interest** are the rules regarding repertoire selection; competitors had to choose from specified lists at each stage, and there were also strict rules regarding repeating pieces across stages. The subsection titled **Program** on the Wikipedia page is of particular use.

A partial data dictionary and comments are as follows:

- `Piano`: S1 and S2 refer to two different Steinways; Y refers to a Yamaha, K refers to a Kawai, and F refers to a Fazioli. Note that in the preliminary round, all competitors who chose Steinways played on the S2 instrument. Competitors who did not progress past the preliminary round on a Steinway have `PS` marked for their instrument. Pianists who chose Yamahas in the preliminary round played a different instrument. Competitors who did not progress past the preliminary round on a Yama have `PY` marked for their instrument.
- `P_x`: refers to the piece played in the preliminary round, numbered in order of their performance. `bye` refers to a competitor who bypassed the preliminary round. 
- `S1_x`: refers to the piece played in stage 1, numbered in order of their performance.
- `S2_x`: refers to the piece played in stage 2, numbered in order of their performance. Note that the number of pieces played may vary.
- `S3_x`: refers to the piece played in stage 3, numbered in order of their performance. Note that the number of pieces played may vary.
- `F_1`: refers to the concero selected in the final stage.
- `Pass_x`: refers to whether the competitor passed the stage in question, where "x" can be `P` for preliminary, and `S1`, `S2`, and `S3` for stages 1, 2, and 3.
- `Yes_Sx`: refers to the proportion of the jury who voted to pass the competitor from stages 1, 2, and 3.
- `Pts_Sx`: refers to the average points awarded to the competitor in stages 1, 2, and 3.
- `Final`: refers to the final standing of the competitor. `F` refers to the four co-equal finalists who were not awarded a standing.

# Grading policy

Upon initial report submission, you will be provided feedback and a numeric
grade. You will receive feedback from the instructor and TAs regarding
your submission and have the opportunity to submit a final report. This
final submission must be accompanied by a formal response to the peer review. 
Your final assigned grade for Case 1 will be the average of your initial
submission and final submission.

The final report is worth 100 points, broken down as follows:

| Component    | Points |
|--------------|--------|
| Introduction | 20     |
| Methodology  | 30     |
| Results      | 20     |
| Discussion   | 30     |

You may create sub-headings as you like, but you must have these four 
components in your final report. 

Any grade deductions in appendices will be allocated to their appropriate
sections. For instance, appendix figures evaluating model assumptions may
impact points corresponding to Methodology and Results. Appendix figures 
displaying exploratory analyses or data cleaning steps may impact points
corresponding to Introduction, etc. Interpretation of model coefficients,
regardless of where they appear in the manuscript, will correspond to the
Results section.

There may additionally be grade deductions for overall paper issues. For  
instance, make sure the paper is professionally presented and free of 
distracting errors or other issues such as poor organization, problems 
with grammar, spelling, or punctuation, and layout concerns such as small 
font in visuals, excessive and inappropriate decimal points, etc. (this 
is not an exhaustive list!).

Submissions missing a formal response to peer review will receive an
automatic penalty of 20 points on the final submission. Any submissions 
missing code used for the manuscript in the GitHub repository will 
automatically receive a score of 0 points. Again, your individual grade 
may be modified due to team evaluation and instructor assessment of 
relative contribution to GitHub repository.

### Repository

The instructor will also evaluate whether the commit history is appropriate and
contains clear descriptions of each committed change. This repository must
contain all code used, as well as any ancillary external files which you may
have used in your analysis. All team members must make significant 
contributions to the GitHub repository; lack of contribution is grounds for
a potentially lower grade compared to other team members.

The final .pdf report must be typeset and reproducible from your analysis code
(end-to-end scripting). This .pdf must match your submission to Gradescope. As
well, any slides used for your video presentation should also be included. If
these slides were generated using a reproducible method (such as xaringan or
Beamer), you must include the code used as well.

**Unsatisfactory repositories may result in group and/or individual grade reductions.**

### Tips

- **Make sure you are addressing the case study goals.**
- Clearly state your hypothesis (or hypotheses) - think about how your paper
might create actionable insight for others.
- Make sure you use best visualization practices as discussed in class for all
visualizations and/or tables.
- Write clearly and effectively; confusing the reader is never a good thing!
- Quality over quantity - do not calculate every statistic and procedure you 
have learned for every variable, but rather choose the most *appropriate*
technique or set of techniques to address the goal at hand.
- Focus on methods that help you begin to answer your research questions.

# Grade considerations:

Note that simply “not making any errors” isn’t enough to get full points 
on an assignment - that is the baseline expectation! In line with Duke 
grade considerations, work earning an A is truly exceptional, and 
demonstrates fluent mastery of the statistical issues and presents 
convincing, well-organized results in a clear and appropriate way. Work
earning a B suggests superior understanding of the material, but may have 
some minor issues in its approach or communication. Work earning a C is
satisfactory and suggests adequate understanding - this is the baseline 
expectation. 

To use a statistical analogy in how I grade these assignments, I use sort 
of a forward/backward approach - there are aspects about each report which 
work well, and reports may “earn points” for that, and aspects which might 
be missing, insufficient, or incorrect (which correspondingly detract from 
the point total).  In order to earn additional points, I’m looking for a 
*comprehensive* treatment of the subject matter, well-justified statistical 
modeling choices with good explanation, clear and concise writing, and 
with a logical flow. 

To provide a concrete example, simply writing the correct model formulation 
for an appropriate model isn’t enough to get full credit - I *already expect* 
this of you! To earn full credit you must additionally justify the use of 
the model chosen in terms of its appropriateness, explain its use in context, 
and compare its strengths and weaknesses to other alternative methodologies.

Finally, I also expect you to learn from mistakes as the semester goes on. 
For instance, while including "p = 0.0000" is considered a minor mistake 
and result in a small deduction in the Results section (is the p-value 
*actually* zero? If not, provide it to the accuracy actually obtained, 
e.g., "p < 0.0001"), making this error on Case 3 would result in a larger 
grade penalty than on Case 1. 

I will go over common errors and mistakes in class, but using experience from 
previous semesters, common errors include the one above, having raw variable
names in the final manuscript or tables, misinterpreting regression 
coefficients (e.g., not conditionally on other variables in the model) or
p-values (e.g., affirming frequentist null hypotheses), or erroneous causal 
language given observational data.
