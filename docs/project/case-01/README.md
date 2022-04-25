# Instructions

This README corresponds to Case Study 1 regarding Lega Serie A.
**Read this file carefully. It's long, I know.**

### Deadline and submission

Report and reproducible code for the initial submission will be due on
**Friday, January 21**. Final case team submission and formal response 
to review will be due on **Friday, February 4**. You will be asked to 
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

There are thirteen total files of interest. The twelve files `season-xxyy.csv`
contain Serie A match data from 2009 through 2021 released by Football--Data, 
where `xx` and `yy` denote the year of the season. These files were compiled
by the instructor but have *not* been cleaned. The variables contained in 
these datasets are:

- `Date` = Date of the match 
- `HomeTeam` = Home team
- `AwayTeam` = Away team
- `FTHG` = Full time home team goals
- `FTAG` = Full time away team goals
- `FTR` = Full time result (H=Home Win, D=Draw, A=Away Win)
- `HTHG` = Half time home team goals
- `HTAG` = Half time away team goals
- `HTR` = Half time result (H=Home Win, D=Draw, A=Away Win)
- `HS` = Home team shots
- `AS` = Away team shots
- `HST` = Home team shots on target
- `AST` = Away team shots on target
- `HF` = Home team hit woodwork
- `AF` = Away team hit woodwork
- `HC` = Home team corners
- `AC` = Away team corners
- `HY` = Home team yellow cards
- `AY` = Away team yellow cards
- `HR` = Home team red cards
- `AR` = Away team red cards

The last file, `serie_a_standings.csv`, contains information regarding the 
teams across seasons and contains the following variables:

- `Season` = Serie A season
- `Club` = Football club
- `Capacity` = Capacity of club's home stadium (note: capacity may change 
from season to season)
- `Pts` Points used in the league table to calculate current season standing
- `CurrentResult` = Result from *current* season season (numeric rank from 
1 -- 20 based on placement in league table) 
- `PriorResult` = Result from \textit{prior} season (numeric rank from 1 -- 20 
based on placement in league tables from prior season; 1 -- 17 are placements 
from the previous Serie A; 18 denotes the previous Serie B champion, 19 denotes 
the previous Serie B second place, and 20 denotes the previous playoff 
tournament winner of the next highest placing Serie B teams)

# Grading policy

Upon initial report submission, you will be provided feedback and a numeric
grade. You will receive feedback from the instructor and TAs regarding
your submission and have the opportunity to submit a final report. This
final submission must be accompanied by a formal response to the peer review. 
Your final assigned grade for Case 1 will be the average of your initial
submission and final submission.

A more detailed discussion of grading considerations is available after this
overview. The final report is worth 100 points, broken down as follows:

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

### Introduction

The introduction should introduce your general research question and your data
(where it came from, how it was collected, what the observational unit is, 
which variables were used in the analysis, etc. Feel free to create subsections 
as needed (for instance, for the dataset, any exploratory visualizations, etc.). 

In evaluating your introduction, I will be evaluating the following points:

- Is/are the main goal(s) of the analysis easy to identify and appropriate for
addressing the overall research problem?
- Is the rationale for the data analysis explained well?
- Does the manuscript describe the context/background of the work and its 
relation to existing literature?
- Are the variables (response and predictors) clearly identified and discussed?
- Does the manuscript explain how the data were collected and/or how they were
derived?
- If provided, is any EDA helpful and informative in addressing the main 
project goal(s)?

### Methodology

The methodology section should clearly explain the model(s) used in your 
analysis. You must clearly state your model formulation using appropriate
mathematical notation and justify their use, and address any model assumptions 
or diagnostics needed. 

In evaluating your methodology, I will be evaluating the following points:

- Is the proposed analysis appropriate given the main goal(s) and dataset?
- Why was this particular methodology chosen over competing choices?
- Are the specific methods described in enough detail that the work could be
replicated by other researchers *without* access to the original analysis code?
- Is it clear which approaches/models were used to evaluate specific goals?
- What assumptions are needed for the model(s), and how do you plan to assess
whether they hold?
- What sensitivity analyses, if any, are planned, and how do they relate to your
analysis approach?

You may include technical derivations and evaluation of model diagnostics and
assumptions in the appendix to your manuscript; they do not belong in the body
of your work.

### Results

Showcase your results! Provide model output (such as coefficient estimates and
quantification of uncertainty) in tabular and/or visual format. Make sure that
each set of results presented supports the goal(s) of your manuscript.

In evaluating your results, I will be evaluating the following points:
 
- Are tables formatted cleanly and precisely? Do visualizations follow good
practices (e.g., clean axis labels, clear titles, appropriate figures given
data types, etc.)?
- Do tables/figures refer to raw variable names, or are all references clearly
made in context of the data?
- Are appropriate conventions re: formatting (e.g., an acceptable number of
decimal places, table/figure captions, etc.) followed when displaying results?
- Is there an appropriate quantification of uncertainty of estimates?
- Are all results interpreted correctly? 

### Discussion

Discuss the implications your results have in terms of your goal(s) and research
question(s). As well, provide a reasoned critique of your methodology and 
provide suggestions for improving the analysis or what additional data might
have strengthened the paper. 

In evaluating your discussion, I will be evaluating the following points:

- How do your results address or fail to address the goal(s) of your manuscript?
- Does the manuscript provide clear, correct, and effective interpretation of
the analysis results?
- Are all conclusions made directly supported by the results?
- Was your methodology fully appropriate? What alternative techniques might have
been useful?
- Are there any issues with reliability or validity of the data?
- What would you do differently if you had to approach the study again? What
additional data sources, variables, or techniques might help you create a 
stronger manuscript?

### Appendix

This is where you present any technical derivations (if needed) and demonstrate
that the assumptions for your models are met. Examples of derivations might
include explicit variance terms of frequentist estimators or derivation of
full conditional distributions for Gibbs samplers, etc.

As for examples of assumptions, if you are creating a linear model, this would be
a good place to discuss the assumptions (e.g., by providing residual plots and
comments); if you are performing a Bayesian analysis, this would be a good place
to show diagnostic plots (e.g., trace plots, etc.). This section may be as long 
or as short as needed. 

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
