
# Task 3: Natural Language Processing with spaCy
# Author: Obinwa Ogechi Perpetual

import spacy

# Load English language model
nlp = spacy.load("en_core_web_sm")

# Sample text
text = "Apple was founded by Steve Jobs in California and it is now one of the biggest tech companies in the world."

# Process text
doc = nlp(text)

# Print named entities (NER)
print("Named Entities, Phrases, and Concepts:")
for entity in doc.ents:
    print(f"{entity.text} ({entity.label_})")

# Print nouns and verbs
print("\nNouns and Verbs:")
for token in doc:
    if token.pos_ in ["NOUN", "VERB"]:
        print(f"{token.text} ({token.pos_})")

# Sentiment or keyword insights could be added here in future versions
print("\nTask Complete: NLP processing done using spaCy.")
