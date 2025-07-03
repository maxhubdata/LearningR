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
- [ ] Chapter 7: [Data import]
- [ ] Chapter 8: [Workflow: getting help]

## ✅ Checklist

- [] Read all chapters listed above
- [] Coded along with examples
- [] Completed the practice exercises
- [] Explored concepts with my own dataset
- [] Summarized key takeaways

## 💡 Key Concepts Learned
- Bullet 1:

## 🛠️ Practice Dataset(s) Used
- billboard, who2

## 📊 Visuals / Plots Created
- <img width="434" alt="image" src="https://github.com/user-attachments/assets/89e3f5bb-9150-4530-a53a-ee909e3ead8b" />


## 🧪 Mini Project (Optional)
- n/a 

## 📝 Notes / Reflections
- what IS tidy data: each variable is a column and each column is a variable. each observation is a row and each row is an observation. each value is a cell and each cell is a single value. 
- data lengthening: use pivot_longer(), ex: billboard |> pivot_longer(cols = starts_with("wk"), names_to = "week", values_to = "rank"). {cols are what need to be pivoted (which columns aren't variables), names_to names the variable stored in the column names, and values_to names the variable stored in the cell values.}
- values can be dropped with values_drop_na=TRUE
- parse_number extracts the first number from a string, ignoring all other text
- review wtf .value actually does (5.3.4)
- data widening: use pivot_longer(): ex: cms_patient_experience |> pivot_wider(id_cols=starts_with("org"),names_from = measure_cd,values_from = prf_rate) {names_from takes the values of a column and makes them column names, values_from takes values from a column and makes them the values under the new columns you've made.}

## 📅 Dates
- Started: 2025-07-02
- Finished: 2025-07-09
