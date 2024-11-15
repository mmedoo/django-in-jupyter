![Django](https://img.shields.io/static/v1?label=Django&message=4.2.3&color=092E20&labelColor=white&logo=django&logoColor=092E20)
![Jupyter](https://img.shields.io/static/v1?label=Jupyter&message=1.0.0&color=orange&labelColor=white&logo=jupyter)


# Django in Jupyter

## Contents

- [📖 Introduction](#intro)
- [🚀 Use cases](#use-cases)
- [⚙️ Setup](#setup)



<h2 id="intro">📖 Introduction</h2> 

This Jupyter Notebook enables you to run Django code independently from the web application. It allows you to interact with your Django project's models, perform data analysis, and prototype features in an interactive and flexible environment.



<h2 id="use-cases">🚀 Use cases</h2>

Here are some scenarios where this can be particularly useful:

### 1. 📊 Data Analysis and Visualization:
- **Exploratory Data Analysis (EDA):** Use Jupyter notebooks to perform EDA on your Django models' data. You can run queries, clean data, and visualize it using libraries like pandas, matplotlib, and seaborn.

- **Reporting:** Create dynamic reports and dashboards using the data stored in your Django application. This can be useful for generating insights and making data-driven decisions.


### 2. 🔍 Prototyping and Testing:
- **Rapid Prototyping:** Quickly prototype new features or model changes. You can interactively test your ideas before integrating them into your Django application.

- **Testing Business Logic:** Test complex business logic in an interactive environment. This helps in understanding how different parts of your codebase interact with the data.


### 3. 🤖 Machine Learning and AI:
- **Model Training:** Train machine learning models using data from your Django application. You can load data, preprocess it, and train models all within the same notebook.

- **Predictive Analysis:** Use trained models to make predictions on new data. Integrate these predictions back into your Django application if needed.


### 4. 📦 Database Management:
- **Database Maintenance:** Perform maintenance tasks like data migrations, backups, and restorations interactively.

- **Data Import/Export:** Easily import data into your Django models or export data from your models to different formats (CSV, Excel, etc.).


### 5. 📚 Interactive Tutorials and Documentation:
- **Educational Purposes:** Create tutorials and documentation that include executable code. This is helpful for teaching others how to use your Django application or understand your data models.

- **Demo and Walkthroughs:** Provide interactive demos and walkthroughs of your application’s functionality.


### 6. 📜 Automation and Scripting:
- **Automate Repetitive Tasks:** Write scripts to automate repetitive tasks such as data cleansing, bulk updates, and other administrative tasks.

- **Batch Processing:** Process large batches of data and apply operations that might be too intensive for a real-time web application.


<h2 id="setup">⚙️ Setup</h2>

### You can download the Notebook in this repository by running this command:
```bash
wget https://raw.githubusercontent.com/mmedoo/django-in-jupyter/refs/heads/master/django.ipynb
```

### Or you can copy this cell to your Notebook:
```py
# You can put the Notebook file in the same directory as your project folder
# and keep the PROJECT_PATH as None.
# Otherwise, set the PROJECT_PATH, and you can run it anywhere.

PROJECT_PATH = None
PROJECT_NAME = "myapp"

# This block is necessary to run Django in Jupyter
# Do NOT touch if you don't want to encounter errors.
# Docs: https://docs.djangoproject.com/en/4.1/topics/async/#async-safety

import django
import os, sys

if PROJECT_PATH:
	sys.path.insert(0, PROJECT_PATH)
	os.chdir(PROJECT_PATH)

os.environ.setdefault("DJANGO_SETTINGS_MODULE", f"{PROJECT_PATH}.settings")
os.environ["DJANGO_ALLOW_ASYNC_UNSAFE"] = "true"

try:
	django.setup()
except ModuleNotFoundError as e:
	print(f"Error: {e}")
```

### Run this cell, and you can code ahead.
