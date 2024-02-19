⬅️ [Back to Basics](https://github.com/MK316/Coding4ET/blob/main/Lessons/Lesson07a.md) | [Next: Practice](https://github.com/MK316/Coding4ET/blob/main/Lessons/Lesson07c.md)

# 📕 Intermediate Manual: Enhancing Data Handling Skills
This intermediate manual is designed to build upon your foundational knowledge and introduce you to more powerful features of Pandas that can further enhance your language teaching methodologies. You will learn how to manipulate and analyze language learning data more efficiently, including filtering data, handling missing values, and performing basic data analysis.

# 🔲 Advanced Data Manipulation
## [1] Filtering Data
Filtering allows you to view or manipulate a subset of your data based on certain criteria, which is useful for focusing on specific groups of language learners or types of vocabulary.

### 🔆 Example: Filtering Words by Part of Speech
Imagine you want to focus on verbs from your vocabulary list. Assuming you have a column named "Part of Speech", you can filter your DataFrame as follows:

```
verbs_df = df[df['Part of Speech'] == 'Verb']
```

This code snippet creates a new DataFrame verbs_df that contains only the rows where the "Part of Speech" is 'Verb'.

## [2] Handling Missing Values
Missing data is common in real-world datasets. Pandas provides several methods to deal with missing values, such as filling them with a specific value or dropping them altogether.

### 🔆 Example: Filling Missing Example Sentences
If your "Example Sentence" column has missing values, you can fill them with a placeholder text like "No example available":

```
df['Example Sentence'].fillna('No example available', inplace=True)
```

## [3] Basic Data Analysis
Performing basic data analysis can provide insights into your language learning data, such as the distribution of words across parts of speech or the average quiz scores of students.

### 🔆 Example: Counting Words by Part of Speech
To see how many words you have for each part of speech:

```
parts_of_speech_counts = df['Part of Speech'].value_counts()
```

This line of code will give you a series where each index is a part of speech and each value is the count of words belonging to that part of speech.

# 🔲 Advanced Data Visualization
Visualization is a powerful tool for understanding and presenting data. Pandas integrates with Matplotlib, a Python plotting library, to enable easy visualization of data directly from DataFrames.

### 🔆 Example: Visualizing Word Counts by Part of Speech
You can create a bar chart to visualize the distribution of words across different parts of speech:

```
import matplotlib.pyplot as plt

parts_of_speech_counts.plot(kind='bar')
plt.xlabel('Part of Speech')
plt.ylabel('Count')
plt.title('Word Counts by Part of Speech')
plt.show()
```

This code plots a bar chart where each bar represents a part of speech, and the height of the bar indicates the number of words in that category.

# 🔲 Saving and Sharing Your Notebooks
Google Colab allows you to save your notebooks directly to Google Drive or export them in various formats, such as .ipynb (Jupyter Notebook) or .pdf, making it easy to share your analyses and findings with colleagues or students.

To save your notebook:

🔸 **Go to "File: > "Save a copy in github"** (Select repository on your github)

🔸 **Go to "File" > "Save" or "Save a copy in Drive" to save your work in Google Drive.**

To download the notebook, go to "File" > "Download" and select your preferred format.



⬅️ [Back to Basics](https://github.com/MK316/Coding4ET/blob/main/Lessons/Lesson07a.md) | [Next: Practice](https://github.com/MK316/Coding4ET/blob/main/Lessons/Lesson07c.md)
