## Sentiment Analysis of the Portrayal of the Bombing of Hiroshima and Nagasaki in American Textbooks
# Allison Kerper, Elijah Kim, and Henry Chen

## Software and Platform
- Types of software used:
    - Python Jupyter Notebook
        - Done in Google Colab
    - Python Packages Used:
        - VADER
        - NumPy
        - Pandas
        - Seaborn
        - sklearn (scikit-learn)
- Platform:
    - Ubuntu distribution on Linux (ran on Google Colab)

## Documentation Map
- DATA/
    - CleanedData.csv
    - RawData.csv
    - DataProcess.md
- SCRIPTS/
    - SourceCode.ipynb
- OUTPUT/
    - Results.pdf
- README.md
- LISCENSE.md


## Instructions for Reproducing
- Acquire pdfs of 10 college-level and 10 high school-level history textbooks
- Extract text samples from each textbook that cover the bombing of Hiroshima and Nagasaki
- Create Google Sheets/Microsoft Excel file with 6 columns: ['Title', 'ISBN', 'Author(s)', 'Publisher', 'Level', 'Text'] and fill in with respective information for each textbook
- Export sheet as CSV file and upload to github
- In Google Collab notebook, clean the CSV file and append dataframe with ['Word Length'] column which contains the text sample length
- Using the VADER Python package, calculate the sentiment for each text sample with SentimentIntensityAnalyzer
- Append dataframe with ['Compound Sentiment'] column which contains each text samples compound sentiment value
- Average the compound sentiment value for high school-level and college-level textbooks
- Subtract the college average from the high school average to calculate the difference
- Calculate the correlation coefficient between 'Word Count' and 'Compound Sentiment' columns in order to identify if a relationship exists between those two variables

## References:
[1] C. J. Hutto and E. Gilbert, “Welcome to VaderSentiment’s documentation!¶,” Welcome to VaderSentiment’s documentation! - VaderSentiment 3.3.1 documentation, https://vadersentiment.readthedocs.io/en/latest/ (accessed Sep. 11, 2024).

[2] J. W. Loewen, Lies my teacher told me : everything your American history textbook got wrong. New York: The New Press, 2018.

[3] L. Geetha, “Vader: A Comprehensive Guide to Sentiment Analysis in Python,” Medium, Feb. 28, 2023. Available: https://medium.com/@rslavanyageetha/vader-a-comprehensive-guide-to-sentiment-analysis-in-python-c4f1868b0d2e

[4] M. Waskom, “Example gallery — seaborn 0.11.2 documentation,” seaborn.pydata.org, Jan. 2024. Available: https://seaborn.pydata.org/examples/index.html
