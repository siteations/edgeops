Initial strategy: (largely processing with js interfaces)
1) run a minimal sweep to eliminate variations on 'digitized by google'
2) consolidate existing town paragraphs into a continuous line, copy line to end of exisiting line if no starting spc
3) run split ; on this blocks to break into relative objects & prices....(town: name, goods: [array])
4) use crazy reg ex to recognize and sort (this was nasty work, also required extensive manual checks, run at county scale for benefit of processing)
5)    see initialdata/workingdata for the file structure and resultant two tables - labor vs. goods
6)    also did not initially include cluster info/analytic tables from the back of reports

Revised strategy: (likely a bit of python and js interfaces - more robust options)
1-3) seems perfectly fine... perhaps split after or internally to keep each town as an js object
4a) leave number alone while working with text rollup functions... making working table to catch/replace reg ex slips, iterate through to clean text data (will need a table per decade: 32, 37, 45, 55, 65 given conventions/structure.... and a table to convert between those years as a group) - CLEAN ORC FIRST
    test for likely integers?
4b) ? employee handling ? some sort of json structure: county: name, town: name, page: x, year: 18xx, entries: {site: factoryType or none, employees: m/f/total, produced:{ goods: [object, cost, amount, unit], etc.
    - THEN FIGURE OUT REG EX PATTERN TO SORT INTO JSON -
4c) what else is required? to reach into and develop timelines/geographic comparisons
4d) what are check procedure ideas for overall structure, manual confirmations?

