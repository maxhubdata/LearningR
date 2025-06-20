---
name: 📘 R4DS Weekly Progress
about: Track progress for a week of learning from "R for Data Science (2e)"
title: "[Week 1] Chapters 1–X Progress"
labels: progress
assignees: maxhubdata
---

## Chapter 1 and 2 (also some of 3) will be review (I did them before)

## 📚 Chapters Covered
- [x ] Chapter 1: [Data Visualization]
- [ ] Chapter 2: [Workflow: Basics]
- [ ] Chapter 3: [Data Transformations]

## ✅ Checklist

- [x ] Read all chapters listed above
- [x ] Coded along with examples
- [x ] Completed the practice exercises
- [n/a ] Explored concepts with my own dataset
- [ x] Summarized key takeaways

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
  - Columns: mutate() {


## 📅 Dates
- Started: 2025-06-19
- Finished: 2025-06-26
