---
name: 📘 R4DS Weekly Progress
about: Track progress for a week of learning from "R for Data Science (2e)"
title: "[Week 1] Chapters 1–X Progress"
labels: progress
assignees: maxhubdata
---

## Chapter 1 and 2 (also some of 3) will be review (I did them before)

## 📚 Chapters Covered
- [x] Chapter 1: [Data Visualization]
- [x] Chapter 2: [Workflow: Basics]
- [x] Chapter 3: [Data Transformations]
- [ ] Chapter 4: [Workflow: code style]
- [ ] Chapter 5: [Data Tidying]
- [ ] Chapter 6: [Workflow: scripts and projects]

## ✅ Checklist

- [x] Read all chapters listed above
- [x] Coded along with examples
- [x] Completed the practice exercises
- [ ] Explored concepts with my own dataset
- [x] Summarized key takeaways

## 💡 Key Concepts Learned
- Bullet 1: plotting datasets using ggplot2
- Bullet 2: transforming data using the dplyr package
- Bullet 3:

## 🛠️ Practice Dataset(s) Used
- penguins, flights

## 📊 Visuals / Plots Created
- not necessary tbh, all is pretty simple

## 🧪 Mini Project (Optional)
- n/a 

## 📝 Notes / Reflections
- To view datasets, use View(dataset) or glimpse(dataset)
- With ggplot2, you can use the function ggplot(dataset, aes(x,y,color=variable,shape=variable) {this part is formally called the mapping}) to graph plots!
  - tack on + geom_whatever() to add data to the graph (points or lines... or bars...)
    - if you want a line you put in to be linear (not curvy), then add (method = "lm") inside it
    - you can instead do some aesthetics {not mapping the x or y} inside the geoms, like
      geom_whatever(aes(shape,color))
  - we can do + labs() to add labels! 
    - for example +labs(title="blahblahblah", subtitle="bleh")
      - note to self, for the color and shape sidebar, make sure color and shape are named the same thing or         there will be 2 sidebars
- variables come in different types (duh): categorical variables can only take one of a few values, for       instance a bird's color is a categorical variable. numerical variables are numbers (also duh), they are      also referred to as quantitative variables, an example being someones weight. boxplots can be used to show   the relationship between the variables (density plots are also okay)
- create new objects with <-, like: x <-1. for vectors with multiple elements, use c()
- when we need to be precise about which package a function comes from, we’ll use the same syntax as R:       packagename::functionname()
- think of the pipe "|>" as saying "then" (speak code like english, it helps)
- sidenote, for dplyr the first argument is the data frame like "flights", afterwards use the pipe to          transition into future arguments. 
- sidenote 2, for conditions, | represents "or", & represents "and". ex: filter(month==1|day==1)
- sidenote 3, dplyr functions never modify their inputs, use an assignment operator "<-" to save them
- important verbs for dplyr (categorized by what they operate on):
  - Rows: filter() {keeps rows based on values of columns}, arrange() {changes order of rows based on the      value of columns, if more than one column name is provided then the additional column names are used to       break ties in sorting. also, you can use desc() inside arrange() to order it big to small, ex:               arrange(desc(dep_delay)), distinct() {finds unique rows of the dataset, for distinct combinations of         variables you supply column names (this gets rid of the other unnamed columns, to not have this happen       use .keep_all = TRUE), count() {to find number of occurences, essentially same as distinct() but gives       number of times the unique combination happens, use sort = TRUE to have it in descending order}.
  - Columns: mutate() {adds new columns, use .before or .after to position it, ex: .before=1 to put it in       front (note, the "." indicates that its an argument, not the name of another variable). .keep can be used    to choose which variables to keep, the argument "used" is useful because it will only keep whats used in     the mutate step, ex: .keep = "used")}, select() {lets you focus on a subset of variables. either: by name    (select(year,month day)), all between (select(year:day)) {inclusive}, all except(select(!year:day))         {inclusive}} (sidenote, select() has helper functions that can be used inside it: starts_with(""),           ends_with(""), contains(""), num_range("",?:?) num_range confuses me, revisit later using ?select in         RStudio), rename() {renames an existing variable, ex: rename(newname=oldname)}, relocate() {moves           variables to the front by default... .before and .after can be used to alter this}.
  - Grouping: group_by() {divides the dataset into groups!.. then future applied operations will be onto the new group. Ex: group_by(months) |> infosummarizingthingy() (this will return the info summarized divided into the 12 months if that makes sense. A useful hotkey when in an operation is .by. also, for grouping by multiple variables, you group the consecutive variables within the previous. intuitively think of grouping as sorting values into boxes, with more variables adding boxes inside the already existing boxes}, summarize() {calculates a summary statistic after grouping... like the mean, multiple summaries can be created in a single call, also n=n() is useful inside an operation to print the number of rows}, slice_head/tail/whatever(n=?) {takes only the row(s) of your choosing... more n means more rows. -n subtracts from total rows. can only be done for groups}, ungroup() {ungroups data from a dataframe}, sidenote but count() is basically just group_by()|>summarize(n=n()) but a shortcut.
- review mutate() and summarize()... reflect on chapter 3 heavily to ensure understanding.
- read these two articles: http://varianceexplained.org/r/empirical_bayes_baseball/ and https://www.evanmiller.org/how-not-to-sort-by-average-rating.html
- Style tips: for names use only lower case and _ to seperate words in a name. put spaces on both sides of mathematical operators and the assignment operator (<-). for function calls don't put spaces before the bracket. always put a space after a comma. adding extra spaces is okay to improve alignment... make sure code is easy to read! pipes should always have a space before them and be the last thing on a line (then double indent the line after them). for functions with named arguments, put each argument on a new line, if arguments are unnamed then all in the same line is okay. if a named argument has its own line, make sure they're indented by an extra two spaces. give the end of brackets their own line for named argument functions. break super long pipes into smaller pipes with informative names. for ggplot2, treat the + the same as |> for the style rules. add sectioning comments for long files. example of pretty code:
 <img width="335" alt="image" src="https://github.com/user-attachments/assets/6df937a8-11a7-4635-815d-8d61ae905d6e" />
 
## 📅 Dates
- Started: 2025-06-19
- Finished: 2025-06-26
