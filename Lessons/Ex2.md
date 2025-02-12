## 🌀 Assignment01 (Lesson 2)

### DIY Setting Up GitHub and Google Colab

* **Objectives: you'll be practicing the following**

    * Create a GitHub account.
    * Create a new repository named 'Practice' in your Github account.
    * Create your first notebook using Google Colab.
    * Save this notebook to your GitHub repository as **"assign01.ipynb"** under the repository "Practice".

* **Goal:**
By completing this assignment, you will gain hands-on experience in setting up a GitHub account, creating repositories, and integrating GitHub with Google Colab. This will lay the foundation for future projects involving code sharing and collaboration.

### Part 1: Create a GitHub Account
* Visit GitHub: Go to github.com and click on “Sign up”.
* Account Setup: Fill in your details (username, email address, and password) and follow the prompts to complete the account creation process.
* Verify Email: Check your email inbox and click on the verification link sent by GitHub.
* Visit [here](https://docs.google.com/spreadsheets/d/1z2uYvH-foo3BZ6a4_T80TK7HOQbIJIYIUe5SWOEaGyk/edit?usp=sharing) to notify your Github account.

### Part 2: Create a Repository
* Log In to GitHub: Log in to your new GitHub account.
* Create New Repository: Click on the "+" icon in the upper-right corner and select "New repository".
* Repository Details:
* Name your repository **"Practice"**.
* Choose “Public” to make it visible to others.
* Initialize with a README (optional).
* Create Repository: Click the “Create repository” button.

### Part 3: Start with Google Colab
* Access Google Colab: Go to Google Colab.
* Google Account: Log in with your Google account.
* Create New Notebook: Click on “File” > “New notebook”.

### Part 4: Save Notebook to GitHub
* Prepare a new python Notebook: In the Colab notebook, write a simple Python code as follows, and run the code.:

```
# Simple code to print the current time in Seoul
from datetime import datetime
import pytz  # Import the pytz module for timezone calculations

# Define the timezone for Seoul
seoul_timezone = pytz.timezone('Asia/Seoul')

# Get current time in Seoul's timezone
now_seoul = datetime.now(seoul_timezone)

# Format the time
current_time_seoul = now_seoul.strftime("%H:%M:%S")

# Print the current time in Seoul
print("Current Time in Seoul:", current_time_seoul)


```

* Save it to your GitHub:
    * Click on “File” in your notebook.
    * Select “Save a copy in GitHub”.
    * Authorize Colab to access your GitHub account, if prompted.
    * Choose the "Practice" repository.
    * Name the file “assign01.ipynb”.
    * Click “OK” to save.
    * Visit your Github repository and check whether the file is saved in the designated repository.

