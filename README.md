# 🗺️ Telangana District Map Coloring Using AC-3

## 📌 Project Title

**Telangana District Map Coloring Using AC-3 Algorithm**

---

## 📖 Project Description

This project implements the **Map Coloring Problem** for all **33 districts of Telangana** using the **AC-3 (Arc Consistency 3) algorithm**.

The problem is formulated as a **Constraint Satisfaction Problem (CSP)**. Each Telangana district is treated as a variable, and each variable is assigned a color. The main constraint is:

> **Two geographically adjacent districts must not have the same color.**

Four colors are used:

```text
Red
Green
Blue
Yellow
```

AC-3 is used for constraint propagation, followed by **backtracking search** to obtain a complete valid coloring.

---

## 🎯 Objectives

- Represent all 33 Telangana districts as CSP variables.
- Define neighbouring districts as constraints.
- Assign a domain of colors to every district.
- Apply the AC-3 algorithm.
- Use backtracking when necessary.
- Ensure adjacent districts have different colors.
- Verify the final solution.
- Visualize the Telangana district constraint graph.

---

## 🧠 Problem Formulation

The map-coloring problem consists of:

### Variables

The 33 Telangana districts are the variables.

### Domains

Every district initially has four possible colors:

```python
["Red", "Green", "Blue", "Yellow"]
```

### Constraints

For every pair of adjacent districts:

```text
Color(District A) ≠ Color(District B)
```

Example:

```text
Hyderabad ≠ Rangareddy
```

---

## 🔄 AC-3 Algorithm

AC-3 stands for **Arc Consistency Algorithm 3**.

It maintains a queue of arcs representing district-to-district constraints. For an arc `Xi → Xj`, AC-3 checks whether every color available for `Xi` has a compatible value in `Xj`.

If a color has no possible supporting value, it is removed.

The process continues until:

- The queue becomes empty, or
- A district has an empty domain.

---

## 🔧 AC-3 + Backtracking

AC-3 performs **constraint propagation**, but it may not assign exactly one color to every district.

Therefore, this project combines:

```text
AC-3
  ↓
Constraint Propagation
  ↓
Backtracking Search
  ↓
Complete Coloring
```

This combination produces a complete solution for the 33-district problem.

---

## 🗺️ Districts Included

All 33 Telangana districts are included:

1. Adilabad
2. Bhadradri Kothagudem
3. Hanumakonda
4. Hyderabad
5. Jagtial
6. Jangaon
7. Jayashankar Bhupalpally
8. Jogulamba Gadwal
9. Kamareddy
10. Karimnagar
11. Khammam
12. Kumuram Bheem
13. Mahabubabad
14. Mahabubnagar
15. Mancherial
16. Medak
17. Medchal-Malkajgiri
18. Mulugu
19. Nagarkurnool
20. Nalgonda
21. Narayanpet
22. Nirmal
23. Nizamabad
24. Peddapalli
25. Rajanna Sircilla
26. Rangareddy
27. Sangareddy
28. Siddipet
29. Suryapet
30. Vikarabad
31. Wanaparthy
32. Warangal
33. Yadadri Bhuvanagiri

---

## 💻 Technologies Used

- Python
- Google Colab
- NetworkX
- Matplotlib
- Collections / `deque`

---

## 📂 Project Structure

```text
Telangana-AC3-Map-Coloring/
│
├── Telangana_AC3_Map_Coloring.ipynb
├── README.md
└── DOCUMENTATION.md
```

---

## ▶️ How to Run

### Step 1

Open the notebook in **Google Colab**.

### Step 2

Run the import and district-definition cells.

### Step 3

Create the district adjacency graph.

### Step 4

Define the color domains.

### Step 5

Run the AC-3 algorithm.

### Step 6

Run the backtracking search.

### Step 7

Verify the solution.

### Step 8

Generate the district graph visualization.

---

## 📊 Expected Output

The program should display:

```text
🎉 SUCCESS!
All 33 Telangana districts have been colored.
```

The verification should produce:

```text
✅ VALID MAP COLORING
No adjacent districts have the same color.
```

A graph visualization is also generated with:

- Districts as nodes
- Neighbouring relationships as edges
- Different colors representing assigned colors

---

## ✅ Solution Verification

The program checks every adjacency constraint:

```python
if solution[district] == solution[neighbour]:
    # Conflict
```

If no conflicts are found:

```text
VALID MAP COLORING
```

This confirms that adjacent districts have different colors.

---

## ⭐ Key Features

- 33 Telangana districts
- CSP formulation
- Four-color domain
- AC-3 constraint propagation
- Backtracking search
- Automatic conflict checking
- NetworkX visualization
- Google Colab compatible
- No dependency on an external GIS API

---

## 🎓 Learning Outcomes

After completing this project, the learner understands:

- Constraint Satisfaction Problems
- Variables and domains
- Binary constraints
- Arc consistency
- AC-3 algorithm
- Backtracking search
- Map coloring
- Graph representation
- AI-based problem solving

---

## 📝 Conclusion

This project demonstrates how the **Map Coloring Problem can be solved as a Constraint Satisfaction Problem using AC-3 and backtracking**.

The 33 Telangana districts are represented as variables, their neighbouring relationships form the constraints, and four colors are used as possible domain values.

The final solution ensures that **no two adjacent districts receive the same color**.

---

## 🔑 Keywords

`AC-3` · `Arc Consistency` · `CSP` · `Constraint Satisfaction Problem` · `Map Coloring` · `Telangana` · `Artificial Intelligence` · `Backtracking` · `Graph Coloring` · `Python` · `Google Colab`
