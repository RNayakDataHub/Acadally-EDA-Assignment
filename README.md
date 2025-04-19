# 📊 Exploratory Data Analysis – Acadally Assignment

This repository contains the solution to an Exploratory Data Analysis (EDA) assignment provided by **Acadally**. The analysis was conducted on educational data to understand student behavior, accuracy levels, and engagement patterns based on chapter and question-level information.

---

## 📁 Dataset

The dataset used is an Excel workbook with two sheets:
- **Attempts Data** – Information about student quiz attempts, including question status, Bloom's taxonomy level, section ID, etc.
- **Chapter Data** – Chapter-level metadata like section ID, start and end times.

---

## 🛠️ Tools & Libraries Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn

---

## 🔧 Data Cleaning Process

**For Attempts Data:**
- Checked for missing values — no nulls were found.
- Removed fully duplicated records with combination of these columns: `['user_id', 'qid', 'time']`.

**For Chapter Data:**
- Removed rows with null `end_time` values (~10% of data), since imputation was not feasible.
- No duplicates found post-cleaning.

---

## 🔑 Primary Keys Identified

- **Attempts Data**: Composite key — `user_id`, `qid`, `time`
- **Chapter Data**: Composite key — `section_id`, `chapter`

---

## 📌 Key Questions Answered

### 1. **Top 5 Sections with Highest Accuracy**
- Accuracy = correct attempts / total attempts
- Top 5 sections were identified based on the highest accuracy percentages.

### 2. **Bottom 2 Learning Units in Application-Level Questions**
- Filtered attempts at the "apply" Bloom taxonomy level.
- Identified the bottom 2 units with the lowest accuracy.

### 3. **Percentage of Questions Attempted Before Chapter Ended**
- Merged attempts and chapter data.
- Compared attempt `datetime` with chapter `end_time`.
- Result: **~41% of questions were attempted before chapter end**, indicating a delay in engagement.

### 4. **Attempt Behavior Across Time of Day**
- Extracted hour from attempt time.
- Visualized attempts distribution using a histogram.
- Peak activity observed around **2 PM to 3 PM**.

---

## 💡 Insights

- 📚 **Peak Attempt Time**: Most users are active post-school hours (around 14:00–15:00).
- ✅ **High Accuracy Sections**: Could indicate stronger understanding or easier question sets.
- ❌ **Low Accuracy Units (Application Level)**: Suggest the need for remedial efforts or better conceptual support.
- ⏰ **Timeliness**: Only ~41% of attempts happen before chapters end, which shows a lag in learning schedule adherence.

---

## Contact at 

For questions or collaborations, feel free to reach out!

---

