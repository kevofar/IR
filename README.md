[README.txt](https://github.com/user-attachments/files/27568876/README.txt)
This guide explains how to use the search engine. Because this system uses strict logic, you must type your inputs exactly as described below to get results.


1. THE "NUMBER" RULE

When the system asks you to "Choose (1, 2, 3, 4 or 5)", it ONLY understands digits.

* WRONG: Typing "one", "second option", or "I want 3".
* RIGHT: Typing "1", "2", "3", "4", or "5".

If you type the word "one", the system will say "Invalid choice, TRY AGAIN" because it is programmed to look only for the characters '1', '2', '3', or '4'.


2. SEARCH MODEL TYPES

You have four ways to search for information:


* OPTION 1: BOOLEAN (PLAIN)
Best for precise searches using logic words.

* You MUST use AND, OR, or NOT in ALL CAPS.

* Example: "RIMS AND password" finds docs with both words.

* Example: "GPA OR dismissal" finds docs with either word.


* OPTION 2: VSM (PLAIN)
Best for typing natural questions.

* Example: "How do I see my grades?"
* It ranks results by a "Score" (Relevance).


* OPTION 3 & 4: GENAI EXPANSION
This uses AI to help find more results.

* If you type "RIMS", the AI (Cerebras/Gemini) adds related words like "portal" or "login" automatically.

* This is the best choice if your first search doesn't find anything.


3. HOW THE SYSTEM "READS" YOUR WORDS

Before searching, the system cleans your text:

* LOWERCASE: "RIMS" becomes "rims".

* NOISY WORDS: It removes words like "the", "a", "is" (Stop Words).

* STEMMING: It chops words to their root. "Accounting" becomes "account", and "Studying" becomes "studi".

* SPECIAL CHARACTERS: It ignores punctuation like "?" or "!".


4. TROUBLESHOOTING

* NO RESULTS? If you search "RIMS" in Boolean and get nothing, ensure you didn't include a typo. Try using VSM (Option 2) instead, as it is more "forgiving" than Boolean.

* SCORE: In VSM, a higher score (e.g., 0.8500) means a better match than a low score (e.g., 0.1200).

* EXITING: To close the program, type "5" at the main menu or "exit" during a search.


5. INPUT EXAMPLES

* Query: rims AND password -> (Finds login help).

* Query: gpa -> (Finds grade requirements).

* Query: dismissal NOT rims -> (Finds academic exit info without portal info).

6. THE FILES
There is one folder, inside that there are 15 files and 1 folder.
Folder templates held the code/web development code for our website/web app, the UI.
app.py is the one that runs the website
Boolean.py is the Boolean model 
cerebras_integration.py is the Gen AI we added
combined.py is the combined that runs in the in console. It have 4 choices, vms, Boolean, and them integrated with AI.
config.py is to hold our API hashed, we used ord and chr to hash our API and make it invisible to users.
dataset.txt is the dataset which contains the 31 Questions and Answers
eval_result.txt is the code we used to evaluate the system, its precision and recall.
evaluation.py is the code we used to combine the two models so that it will be easy for use to evaluate the system using queries.
inverted_index.json is the index
inverted_index.py is the one that created us an index, the json
main.py is the one that preprocessed our dataset(tokenization, stemming...)
processed_data.txt is the processed dataset by main.py
stop_list.txt is the manually and automatically extracted stopwords
vsm.py is the second model.

THERE IS A MISSING FILE FROM THE ZIP, WHICH IS "config.py" it contain the API key for the GenAI, so,  it you want to access the API key(if you have the right to do so). contact me with https://t.me/kevofar
