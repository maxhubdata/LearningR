---
name: 📘 R4DS Weekly Progress 2
about: Track progress for a week of learning from "R for Data Science (2e)"
title: "[Week 2] Chapters 5-X"
labels: progress
assignees: maxhubdata
---


## 📚 Chapters Covered
- [x] Chapter 5: [Data Tidying]
- [x] Chapter 6: [Workflow: scripts and projects]
- [x] Chapter 7: [Data import]
- [x] Chapter 8: [Workflow: getting help]
- [x] Chapter 9: [Layers]
- [x] Chapter 10: [Exploratory data analysis]

## ✅ Checklist

- [x] Read all chapters listed above
- [x] Coded along with examples
- [x] Completed the practice exercises
- [x] Explored concepts with my own dataset
- [x] Summarized key takeaways

## 💡 Key Concepts Learned
- Bullet 1: not doing this

## 🛠️ Practice Dataset(s) Used
- also not doing this lol

## 📊 Visuals / Plots Created
- <img width="434" alt="image" src="https://github.com/user-attachments/assets/89e3f5bb-9150-4530-a53a-ee909e3ead8b" />
- <img width="953" alt="image" src="https://github.com/user-attachments/assets/2f560962-49c5-455e-8de1-79bb5a4e2078" />
- <img width="427" alt="image" src="https://github.com/user-attachments/assets/ebfcc693-74e9-4e58-9637-a41a40f5c32e" />
- <img width="431" alt="image" src="https://github.com/user-attachments/assets/06954779-f318-4547-bcdd-a372ed845bc7" />






## 🧪 Mini Project (Optional)
- pokemon tidy tuesday...

## 📝 Notes / Reflections
- what IS tidy data: each variable is a column and each column is a variable. each observation is a row and each row is an observation. each value is a cell and each cell is a single value. 
- data lengthening: use pivot_longer(), ex: billboard |> pivot_longer(cols = starts_with("wk"), names_to = "week", values_to = "rank"). {cols are what need to be pivoted (which columns aren't variables), names_to names the variable stored in the column names, and values_to names the variable stored in the cell values.}
- values can be dropped with values_drop_na=TRUE
- parse_number extracts the first number from a string, ignoring all other text
- review wtf .value actually does (5.3.4)
- data widening: use pivot_longer(): ex: cms_patient_experience |> pivot_wider(id_cols=starts_with("org"),names_from = measure_cd,values_from = prf_rate) {names_from takes the values of a column and makes them column names, values_from takes values from a column and makes them the values under the new columns you've made.}
- hotkeys: ctrl + shift + n opens R script. ctrl + enter runs the next line of code. ctrl + shift + s runs the full script. ctrl + shift + m for pipe (reminder for myself)
- only use relative paths inside a project!
- reading data types: for csv (comma seperated values) use read_csv("fileaddresshere"). R recognizes "na" to mean not available, sometimes you need to add code to get R to recognize what's supposed to be na in a data set, ex: students <- read_csv("data/students.csv", na = c("N/A", "")). when referring to variables with non-syntactic names (typically they have spaces inbetween instead of _) use backticks "`" to refer to them. use skip = n in the read_csv to skip n amount of lines. or comment = "whatever" to indicate that "whatever" is the start of a comment and those lines will be ignored. if there's no column names, then use col_names=FALSE. read_csv2 is for semicolon seperated files. read_tsv is for tab delimited files. read_delim guesses the delimiter if unspecified. read_fwf is for fixed width files. read_table reads a variation of fixed width files where the columns are seperated by white space. read_log reads apache-style log files. 
- to figure out more about why there's a problem, use problems()
- revisit chapter 7 in the future when encountering data errors
- save a bunch of data files in a vector so they can be read all at once with read_csv
- use write_csv(dataframe,"locationyouwanttosavethefile.csv") (or write_tsv for tab seperated values) to save data back into computer. when you save the data and load it back in from the CSV file, the information on the column types is lost (because a CSV file is plain text), so R has to guess column types again when you load it back in, ex: you set a column as a factor, R reads it and thinks it's actually a character. to fix this, write_rds() and read_rds() can be used because they use R's custom binary format to store the data, so the object will be the EXACT same that you stored (the only issue being... it's only usable in R)
- use tibble() or tribble() {transposed tibble} for data entry. basically, tibble does it by column, tribble does it by row. tibble ex: tibble(
  x = c(1, 2, 5), 
  y = c("h", "m", "g"),
  z = c(0.08, 0.83, 0.60)
).
tribble ex: tribble(
  ~x, ~y, ~z,
  1, "h", 0.08,
  2, "m", 0.83,
  5, "g", 0.60
).
- weekly readings?: https://www.tidyverse.org/blog/ and https://rweekly.org/
- i just tried participating in tidytuesday for the first time!! thats a big step forward. i dont think i actually found anything insightful in my plot... sort of meaningless, will reflect on how to make it less shitty lol. 
- in ggplot, you can use color =, size =, alpha = (transparency), and shape = as aesthetic mappings. (only 6 shapes though, rest are unplotted). you can also use these visual properties in the geom function
- don't do specific color mapping (like, color = "blue") inside the aes()
- stroke inside the aes controls the width of the border of the points
- linetype = as an aesthetic mapping changes how geom_smooth() {or whatever other lines there are presumably} look
- local mappings overwrite global mappings
- for geom_smooth, multiple lines will be created if theres multiple categorical groupings
- you can specify data in the geoms, like geom_point(data |> filter(whatever))
- <img width="467" alt="image" src="https://github.com/user-attachments/assets/4c336466-e71f-400c-a0ce-ea761812f054" />
- use facet_wrap(~categorical variable), to split the plot into subplots based on the categorical variable
- for two categorical variables use facet_grid(rows ~ columns) {tip, using "." is a filler that does nothing allowing you to treat facet_grid like facet_wrap, ex: facet_grind(rows~.)}
- setting scales = "free_x" allows different scales of x axis along the columns, "free_y" is the same but for y axis along the rows, "free" is both
- dont facet a continuous variable, too many plots will be created
- faceting a variable by columns makes the data easier to compare typically
- every geom has a default stat (algorithm used to calculate new values for a graph, like how bar graphs count), inside a geom (and aesthetic?) you can use stat = "insertvariable" to change it.
- stat_summary() summarizes the y value for each unique x value
- use coord_cartesian() to zoom in to a graph, with the argument inside xlim and ylim to zoom into the x and y axis respectively


## 📅 Dates
- Started: 2025-07-02
- Finished: 2025-07-09
