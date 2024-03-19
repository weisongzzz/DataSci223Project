# DataSci223Project by Weisong Zhang

## Main Objective

Teach an English speaker Japanese kana & Train a model that can classify Japanese readings on a scale of N5 to N1 Japanese proficiency levels. 

## Setup

Run pip install -r requirements.txt

## Protocol of model creation

1. Train the person Hiragana, Katakana and Dakuten by running kana.ipynb and inputing answers
2. Create 5 txt files (N5.txt to N1.txt) and mannally copy vocabulary lists from [Wiktionary](https://en.wiktionary.org/wiki/Appendix:JLPT) to the respective files. (desire more vocabulary from other sources)
3. Run sort_dataframe.ipynb to obtain dictionary.csv
4. Mannualy download 5 pdf files (i.e. N5R.pdf), which are the reading sections of the past N5 to N1 levels of Japanese Proficiency Test from the "Test items" under JLPT Official Practice Workbook Vol. 2 from [website](https://www.jlpt.jp/e/samples/sampleindex.html)
5. Use pdf_to_txt.ipynb to extract all text from the downloaded pdf files and store in 5 txt files (i.e. N5R.txt)
6. Run parse_words.ipynb to count numbers of words belong to each level in levels N5 to N1 for each text file
3. Use a script to parse Japanese sentence to words as input (only extract the base form of nouns, verbs, and adjectives)
4. Download pdf of official JLPT tests and extract all texts into txt files (mannually done)
5. Mannualy change input file when run parse_words.ipynb
6. Take outputs from parse_words.ipynb to create_df.ipynb and run it

## For users

1. Access the kana.ipynb if practice of hiragana, katakana or dakuten is needed.
2. Once the model works, input new text as input the model and get the output.

## limitations

1. Very limited size of the training sample and testing sample results the accuracy of 0.
2. Some Japanese from the training text file has informal or formal writing of Japanese, meaning that some text does not have a match to what is in the dictionary because the dictionary contains formal writing. 

## Future direction

1. Better automation of the process
2. Input larger number of training text with labeled Japanese Proficiency levels
3. More sophisticated package to compare the unique tokens with dictionary