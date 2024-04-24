⬅️ [Coding4ET](https://github.com/MK316/Coding4ET/blob/main/README.md) | [Part II.](https://github.com/MK316/Coding4ET/blob/main/Lessons/Lesson07b.md)	▶️ 

# 📙 Part 1: A Beginner's Manual to Handling DataFrames in Colab Using {Pandas} for Language Teachers

Welcome to this beginner-friendly manual designed specifically for language teachers who are stepping into the world of coding with the intention of leveraging data to enhance teaching and learning experiences. This manual will introduce you to the basics of handling data using Pandas in Google Colab, a free, cloud-based platform that allows you to write and execute Python code. Our focus will be on DataFrames, reading from and saving to CSV files—skills that will enable you to manipulate data sets related to language learning in an environment you're already familiar with, like Excel.

# [1] Introduction to DataFrame
A DataFrame is a two-dimensional, size-mutable, and potentially heterogeneous tabular data structure with labeled axes (rows and columns) in Pandas, a powerful and widely-used data manipulation library in Python. Think of a DataFrame as a spreadsheet or an Excel sheet, where data is neatly organized into rows and columns, making it easy to store, access, and manipulate language learning data such as vocabulary lists, quiz scores, or student feedback.

## Getting Started with Colab and Pandas
First, you need to access Google Colab:

1. Go to the Google Colab website (https://colab.research.google.com).
2. Sign in with your Google account.
3. Click on 'New Notebook' to create a new project.

Next, you'll want to import Pandas. At the beginning of your notebook, type and execute the following code to import the Pandas library:

```
import pandas as pd
```

## Reading CSV Files
CSV (Comma-Separated Values) files are a common format for storing tabular data. They can be easily created and edited in spreadsheet software like Excel.

To read a CSV file into a DataFrame in Colab, you can use the following syntax:

```
df = pd.read_csv('path/to/your/csvfile.csv')
```

If your CSV file is stored in Google Drive, you can mount your drive by following the Colab prompts after running:

```
from google.colab import drive
drive.mount('/content/drive')
```
Here's how to unmount Google Drive
```
from google.colab import drive
drive.flush_and_unmount()
print('Drive unmounted successfully.')
```
Then, adjust the path to where your CSV file is stored within your Google Drive.

### Example:
Imagine you have a CSV file named "vocabulary_list.csv" with columns "Word", "Meaning", and "Part of Speech". (You've uploaded this file on colab.) To read this file, you would use:

```
df = pd.read_csv('/content/vocabulary_list.csv')
```

##  Viewing Your DataFrame
To take a look at the first few rows of your DataFrame, use:

```
df.head()
```

```
df.tail()
```

This command displays the first 5 rows of your DataFrame, giving you a quick snapshot of your data.

## Saving a DataFrame to a CSV File
After manipulating or analyzing your data, you may want to save the results back into a CSV file. This is straightforward with Pandas:

```
df.to_csv('path/to/your/new_csvfile.csv', index=False)
```

Setting index=False ensures that Pandas does not write row indices into the CSV file. You can then open this CSV file in Excel or any other spreadsheet software for further editing or review.

### Example:
If you've added a new column to your "vocabulary_list.csv" DataFrame, say "Example Sentence", and want to save this updated DataFrame, you would use:

```
df.to_csv('/content/updated_vocabulary_list.csv', index=False)
```

This manual introduced you to the basics of using Pandas in Google Colab for handling data related to language teaching and learning. By learning how to read from and save data to CSV files, you're now equipped to perform basic data manipulation tasks that can significantly enhance your language teaching methodologies. Remember, practice is key to becoming proficient in these new skills, so don't hesitate to experiment with your datasets.

⬅️ [Coding4ET](https://github.com/MK316/Coding4ET/blob/main/README.md) | [Part II.](https://github.com/MK316/Coding4ET/blob/main/Lessons/Lesson07b.md)	▶️ 



