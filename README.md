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
| **Student ID** | |
| **Name** | |
| **What part of the lab did you personally contribute to (provide a link to the branch(es)), and what did you learn from it?** | |

### Member 3

| Details | Comment |
|---|---|
| **Student ID** |166918 |
| **Name** |Kariuki Irene Wanjiru |
| **What part of the lab did you personally contribute to (provide a link to the branch(es)), and what did you learn from it?** | I did Section 5 (Choosing Thresholds) and Section 6 (Redundancy Removal): I examined the distribution of confidence and lift across the 138 rules generated in Section 4 before selecting thresholds, rather than using arbitrary round numbers. Confidence ≥ 0.4 was chosen at a visible break in the distribution, and lift ≥ 1.5 to exclude rules with near-independence signal. This reduced the rule set to 59. I then removed redundant rules, cutting the set to 30, and bidirectional duplicates, leaving a final set of 22 non-redundant, practically meaningful rules.|

### Member 4

| Details | Comment |
|---|---|
| **Student ID** | 164430|
| **Name** | Maxwell Gitonga|
| **What part of the lab did you personally contribute to (provide a link to the branch(es)), and what did you learn from it?** | I did Section 4: Interpreting the rule set and validating it on a held-out period.<br>I translated the final rule set from item IDs to item names and found that the strongest patterns clustered within a single cuisine category rather than across categories, e.g. Chicken Biryani + Naan Bread → Raita (confidence 92.84%, lift 5.12) reflecting a near-automatic accompaniment pattern in Indian cuisine ordering. I also learnt that association rule mining has no held-out metric the way a predictive model does, so the closest equivalent is temporal validation: mining rules on an earlier period of transaction_date and re-checking their confidence against a later, unseen period. This showed me that a rule's strength on the data it was mined from isn't proof it reflects real customer behaviour — it could just be noise specific to that time window — and re-testing it on later transactions is what actually builds confidence the pattern generalizes.<br>Link to the branch: https://github.com/tanuiivy/bbt4106-202604-D4-association-rules/tree/feature/validation-maxwell |

### Member 5

| Details | Comment |
|---|---|
| **Student ID** |153130 |
| **Name** |Ivy Tanui |
| **What part of the lab did you personally contribute to (provide a link to the branch(es)), and what did you learn from it?** | I did Sections 9 through 12: the recommender function, model persistence, the code quality review, and the final report. Building the recommender taught me that "considers all matching rules" is an actual requirement, not just a formality. <br>For persistence, I learned that saving a model isn't the same as saving everything it needs to be useful; the rules alone are just item IDs without the lookup table.<br>Writing the report taught me that reporting means explaining the story the numbers tell, in this case, that the strongest rules cluster within a single cuisine rather than crossing categories. <br>Link to the branch:https://github.com/tanuiivy/bbt4106-202604-D4-association-rules/tree/feature/recommender-ivy|

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
