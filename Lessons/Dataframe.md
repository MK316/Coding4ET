# Python dataframes and CSV file handling for beginners

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
import pandas as pd  # Import pandas library

# Example DataFrame
data = {'Word': ['apple', 'banana', 'cherry'],
        'Meaning': ['A fruit', 'Another fruit', 'A red fruit']}
df = pd.DataFrame(data)

print(df)  # Display the DataFrame

```

Output:

```
     Word         Meaning
0   apple        A fruit
1  banana   Another fruit
2  cherry     A red fruit

```

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

+ Download a CSV file with English words and their IPA transcriptions.
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
        'IPA': ['ˈæp.l̩', 'bəˈnænə', 'ˈʧɛri']}
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
