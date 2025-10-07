# ReadMe - Chat Reply Recommendation System

## Project Overview

Offline chat-reply recommendation system designed to predict User A’s next response based on User B’s message and the previous conversation. The model uses a fine-tuned T5-small Transformer and runs fully offline.

## Folder Structure


chatrec_output/
│── t5_chatrec_model/
│── Model.joblib
│── Report.txt
│── ReadMe.txt


## Requirements

* Python 3.10 or later
* PyTorch
* Transformers
* Numpy, Pandas, Joblib, NLTK

## Steps to Use the Project

1. *Prepare Datasets*
   Place userA_chats.csv and userB_chats.csv in the /Desktop/Dataset/ directory.

2. *Open the Notebook*
   Launch ChatRec_Model.ipynb in Jupyter Notebook or any Python IDE.

3. *Run the Notebook*
   Execute each cell to:

   * Preprocess and merge chat data.
   * Fine-tune the T5-small model.
   * Evaluate performance and generate results.

4. *Check Output Folder*
   After successful execution, all generated files will appear in the ./chatrec_output/ folder. This includes:

   * The fine-tuned model and tokenizer (t5_chatrec_model/)
   * The metadata reference file (Model.joblib)
   * Evaluation summary (Report.txt)
   * This ReadMe file (ReadMe.txt)

5. *Use the Model for Reply Generation*
   Once trained, load the model from chatrec_output/ to generate context-based replies. Provide a conversation snippet as input to receive a predicted response.

6. *Offline Execution*
   The entire process works without an internet connection once dependencies and model weights are locally available.

## Notes

* Use smaller batch sizes if running on CPU.
* The quality of responses improves with longer and cleaner chat data.

## Author

Developed for the *AI/ML Developer Intern (Round 4)* challenge.
