# Structuring Your Codebase: To GitHub or Not
For this course, it is not strictly required to use GitHub. Regardless of whether you use GitHub or not, you just *need* to keep a good structure of your codebase with code that is documented and readable. 

```
.
├── data
│   └── raw_data.txt
├── plots
│   └── student_plot.png
├── README.md
├── requirements.txt
├── results
│   └── mBERT_all_metrics.txt
├── setup.sh
└── src
    ├── get_paths.py
    └── template.ipynb
```
*Example of a structure, but it can look in many different ways!*

## If You Don't Use GitHub
If you don't use GitHub, make sure to provide your code folder in a `zip file` with all that you would normally have in a GitHub repository (i.e., everything needed for the code to run).

## Template
I have been hestitant about whether to include a repository template as it is SO individual how to structure these things. However, if you want to see how your code repository *could* look, check out: 

<div style="text-align: center;">
  <a href="https://github.com/MinaAlmasi/nlp-template/tree/main">Template Repository</a>
</div>

:::{important} 
Don't take the template too seriously - play with it and find your style! The most important thing is that you tell us:

1. What is your code, data and results? And where are your files located?
2. How do we reproduce your code?
:::