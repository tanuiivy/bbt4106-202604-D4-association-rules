# bbt4106-202604-D4-association-rules

Group D submission for the association rule mining lab, BBT4106: Business
Intelligence I.

## Assignment

- **Dataset**: `food_delivery_orders.csv`
- **Task**: build a full association rule mining pipeline, from installing
  dependencies to a working recommender function and a written report.
- **Submission**: one Jupyter notebook, in `lab_submission/`.

## Team

**Name of the team on GitHub Classroom:**

### Member 1

| Details | Comment |
|---|---|
| **Student ID** | 168825 |
| **Name** | Wanyingi Shirleen Muthoni |
| **What part of the lab did you personally contribute to (provide a link to the branch(es)), and what did you learn from it?** | I did Section 1: Data loading and EDA and Section 2: Building transactions.<br>I learnt that a row is one item in an order and order_id helps group items into baskets. Also, orders with one item cannot be used to form a rule but they are not removed because the support value would look higher than it actually is which is not accurate. I also learnt how to interpret a basket matrix. A basket matrix has one row per order and one column per item. True means the item was in that order and false means that the item was not in that order. <br>Link to the branch: https://github.com/tanuiivy/bbt4106-202604-D4-association-rules/tree/feature/eda-shirleen|

### Member 2

| Details | Comment |
|---|---|
| **Student ID** |166076|
| **Name** |Angela Faith|
| **What part of the lab did you personally contribute to (provide a link to the branch(es)), and what did you learn from it?** |I did section 3: Choosing min_support and section 4: Frequent itemset generation. I learned how to and the importance of choosing and appropriate support level and what it actually means to do so in practical terms. I also learned how to generate frequent itemsets and to interpret the outputs after having done so. I understood how these concepts can also be applied practically in the real world and the kinds of problems they can solve.Github branch link: https://github.com/tanuiivy/bbt4106-202604-D4-association-rules/tree/feature/-itemsets---Angela|

### Member 3

| Details | Comment |
|---|---|
| **Student ID** | |
| **Name** | |
| **What part of the lab did you personally contribute to (provide a link to the branch(es)), and what did you learn from it?** | |

### Member 4

| Details | Comment |
|---|---|
| **Student ID** | |
| **Name** | |
| **What part of the lab did you personally contribute to (provide a link to the branch(es)), and what did you learn from it?** | |

### Member 5

| Details | Comment |
|---|---|
| **Student ID** | |
| **Name** | |
| **What part of the lab did you personally contribute to (provide a link to the branch(es)), and what did you learn from it?** | |

## Video demonstration

Submit a link to a short video (5 minutes or less) demonstrating the
solution. Give the lecturer rights to view it. Submit the link only. Don't
upload the video file to the repository.

**Link to the video:**

## Repository structure

```
.
├── data/
│   └── food_delivery_orders.csv
├── lab_submission/
│   └── bbt4106-202604-D4-association-rules.ipynb
└── README.md
```

## Branch workflow

1. Create a branch from `main`, using the pattern `feature/<section>-<name>`.
   For example, `feature/eda-ivy`.
2. Commit your section's work to your branch.
3. Open a pull request into `main` when your section is complete.
4. Read the full notebook after every merge. The individual defense can ask
   about any section, not only the one you wrote.

## Submission checklist

- [ ] Notebook runs top to bottom with no errors.
- [ ] Every member's contribution is recorded in the team table above, with a
      link to their branch.
- [ ] Demo video recorded (5 minutes or less) and the link added to the
      submission.
- [ ] Individual defenses scheduled for each member.
- [ ] Three-part report (limitations, academic statement, business analysis)
      written using real figures from this notebook.
