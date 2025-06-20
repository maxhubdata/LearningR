---
name: 📘 R4DS Weekly Progress
about: Track progress for a week of learning from "R for Data Science (2e)"
title: "[Week 1] Chapters 1–X Progress"
labels: progress
assignees: maxhubdata
---

## Chapter 1 and 2 will be review (I did them before)

## 📚 Chapters Covered
- [x ] Chapter 1: [Data Visualization]
- [ ] Chapter 2: [Workflow: Basics]
- [ ] Chapter 3: [Data Transformations]

## ✅ Checklist

- [x ] Read all chapters listed above
- [x ] Coded along with examples
- [x ] Completed the practice exercises
- [ ] Explored concepts with my own dataset
- [ x] Summarized key takeaways

## 💡 Key Concepts Learned
- Bullet 1: plotting datasets using ggplot2
- Bullet 2:
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


## 📅 Dates
- Started: 2025-06-19
- Finished: 2025-06-26
