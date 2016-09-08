Initial strategy: (largely processing with js interfaces)
1) run a minimal sweep to eliminate variations on 'digitized by google'
2) consolidate existing town paragraphs into a continuous line, copy line to end of exisiting line if no starting spc
3) run split ; on this blocks to break into relative objects & prices....
4) use crazy reg ex to recognize and sort (this was nasty work, also required extensive manual checks, run at county scale for benefit of processing)
5)    see initialdata/workingdata for the file structure and resultant two tables - labor vs. goods
6)    also did not initially include cluster info/analytic tables from the back of reports

Revised strategy: (likely a bit of python with js interfaces - more robust)
1-3) seems perfectly fine
4a) let numbers be while working with rollup functions... making working table to catch/replace reg ex slips, iterate through to clean text data
4b) 
