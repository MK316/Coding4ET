# 🍃 Dataframes and CSV file handling for beginners

+ Using Colab and Gradio
+ This manual introduces DataFrame basics, CSV handling in Colab, and builds toward creating a simple Gradio-based language application. Each section progressively increases in complexity, with hands-on coding examples and practice questions.

## 1. Introduction to DataFrames
A DataFrame is a 2D data structure, like a table, with rows and columns. It is part of the pandas library in Python.

For instance,

|ID|Name|Music|Math|
|--|--|--|--|
|1|Mary|87|80|
|2|Tom|67|87|
|3|Jane|90|70|
|...|...|...|...|
|100|Elliot|89|95|

```
# Create a dataframe
import pandas as pd  # Import pandas library

# Example DataFrame
data = {
    'Name': ['Mary', 'Tom', 'Jane'],
    'Music': [87, 67, 90],
    'Math': [80, 87, 70]
}

df = pd.DataFrame(data)  # Create a DataFrame from the dictionary
print(df)  # Display the DataFrame
```
#### Applied: Dictionary sample

```
import pandas as pd  # Import pandas library

# Example DataFrame
data = {
    'Word': ['apple', 'banana', 'cherry'],
    'Meaning': [
        'A round fruit with red, green, or yellow skin, and a crisp white interior.',
        'A long, curved fruit with a soft, starchy interior, typically yellow when ripe.',
        'A small, round, red fruit with a juicy interior and a pit in the center.'
    ]
}

df = pd.DataFrame(data)

print(df)  # Display the DataFrame

```

Output:

```
     Word   Meaning
0   apple   A round fruit with red, green, or yellow skin, and a crisp white interior.
1  banana   A long, curved fruit with a soft, starchy interior, typically yellow when ripe.
2  cherry   A small, round, red fruit with a juicy interior and a pit in the center.

```

Output in csv file:

|  |Word|Meaning|
|--|--|--|
|0|   apple|   A round fruit with red, green, or yellow skin, and a crisp white interior.|
|1|  banana|   A long, curved fruit with a soft, starchy interior, typically yellow when ripe.|
|2|  cherry|   A small, round, red fruit with a juicy interior and a pit in the center.|



## 2. Loading and Saving CSV Files in Colab
CSV files are common for storing data. Here's how to handle them in Google Colab.

+ Upload a CSV File:
  
```
from google.colab import files

uploaded = files.upload()  # Upload a CSV file manually

```

+ Read CSV into a DataFrame:

```
df = pd.read_csv('your_file.csv')  # Replace 'your_file.csv' with the file name
print(df.head())  # Show the first few rows

```
+ Save a DataFrame to a CSV:

```
df.to_csv('output.csv', index=False)
from google.colab import files
files.download('output.csv')  # Download the CSV file

```
## 3. Basic DataFrame Operations

+ Access Columns:

```
print(df['Word'])  # Access the 'Word' column
```

+ Filter Rows:

```
filtered = df[df['Word'] == 'apple']  # Filter rows where 'Word' is 'apple'
print(filtered)
```
+ Add a New Column:

```
df['Length'] = df['Word'].apply(len)  # Add a column with word lengths
print(df)
```

+ Sort Data:

```
df = df.sort_values(by='Length', ascending=True)  # Sort by the 'Length' column
print(df)
```

## 4. Gradio Integration
Gradio helps create interactive applications.

+ Install Gradio:

```
!pip install gradio
```

+ Sample Application

```
import gradio as gr

def search_meaning(word):
    result = df[df['Word'].str.contains(word, case=False)]
    if not result.empty:
        return result['Meaning'].values[0]
    else:
        return "Word not found."

interface = gr.Interface(
    fn=search_meaning,
    inputs=gr.Textbox(label="Enter a word"),
    outputs=gr.Textbox(label="Meaning")
)

interface.launch()
```

## 5. Practice Questions

1. Load and Explore a CSV:

+ Download a CSV file with English words and their IPA transcriptions. 💾 [File to download](https://raw.githubusercontent.com/MK316/Coding4ET/refs/heads/main/data/word_transcriptions.csv)
+ Load the CSV file into a DataFrame in Colab and display the first five rows.

2. Modify the DataFrame:

+ Add a column that shows the number of characters in each word.
+ Sort the words by the number of characters.

3. Filter Data:

+ Filter and display all words that start with the letter "a".

4. Build an Application:

+ Using Gradio, create an app where users can input a word, and the app displays its IPA transcription.

## 6. Sample Language Application

```
import pandas as pd
import gradio as gr

# Example Data
data = {'Word': ['apple', 'banana', 'cherry'],
        'IPA': ['ˈæppl̩', 'bəˈnænə', 'ˈʧɛri']}
df = pd.DataFrame(data)

def ipa_transcription(word):
    result = df[df['Word'].str.contains(word, case=False)]
    if not result.empty:
        return result['IPA'].values[0]
    else:
        return "Transcription not available."

interface = gr.Interface(
    fn=ipa_transcription,
    inputs=gr.Textbox(label="Enter a word"),
    outputs=gr.Textbox(label="IPA Transcription")
)

interface.launch()

```
### More samples

+ 🐥 [Quiz making using Gradio](https://github.com/MK316/Coding4ET/blob/main/Lessons/gradioAPP_sample_1120.ipynb)

