# Python-Based-Named-Entity-Recognition-with-spaCy

In this project, we utilize Python along with the powerful spaCy library to perform Named Entity Recognition (NER) on financial news headlines. By leveraging spaCy's pre-trained English language model, we extract important entities such as company names, locations, and monetary values from the headlines. This analysis provides valuable insights into the key entities mentioned in financial news, aiding in understanding market trends, potential investments, and economic indicators.

Let's break down the code step by step:

1. **Install spaCy and Download English Language Model**:
   ```python
   !pip install spacy
   !python -m spacy download en_core_web_sm
   ```
   - This part of the code installs the spaCy library using pip and then downloads the English language model (`en_core_web_sm`) required for natural language processing tasks.

2. **Import spaCy**:
   ```python
   import spacy
   ```
   - Imports the spaCy library into the Python environment, allowing us to utilize its functionalities.

3. **Load English Language Model**:
   ```python
   nlp = spacy.load("en_core_web_sm")
   ```
   - Loads the English language model (`en_core_web_sm`) into the variable `nlp`, enabling us to perform various natural language processing tasks such as tokenization, part-of-speech tagging, and named entity recognition.

4. **Define Sample Text**:
   ```python
   text = "Apple is looking at buying U.K. startup for $1 billion"
   ```
   - Assigns a sample text, a financial news headline, to the variable `text`. This text will be used for named entity recognition (NER).

5. **Perform Named Entity Recognition (NER)**:
   ```python
   doc = nlp(text)
   ```
   - Processes the sample text using the loaded spaCy language model (`nlp`) to perform named entity recognition. The result is stored in the variable `doc`.

6. **Extract Entities and Print**:
   ```python
   for ent in doc.ents:
       print(ent.text, ent.label_)
   ```
   - Iterates over each entity (`ent`) identified in the processed text (`doc`) and prints both the text of the entity (`ent.text`) and its associated entity label (`ent.label_`). This provides information about the recognized entities and their types, such as organization names, locations, and monetary values.

Overall, this code demonstrates a basic example of using spaCy for named entity recognition on a sample financial news headline, extracting entities like company names ("Apple"), locations ("U.K."), and monetary values ("$1 billion").
