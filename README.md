This README provides instructions on running the provided code. Follow the steps below to execute the code and generate prediction files.

### Setup Instructions
1. Ensure all required dependency files are present in the same directory:
   - train, dev, test datasets
   - eval.py script
   - CSCI544_HW3.ipynb notebook
2. Update the file paths inside the file if needed to match your local setup. Key variables handling file paths include:
   - train, dev, test for datasets
   - output for writing prediction files

### Generating Predictions

#### Running Greedy Decoding
Predictions will be generated for Task 1:
- `dev1.out` (Predictions on dev set)
- `test1.out` (Predictions on test set)
Predictions will be generated for Task 2:
- `dev2.out` (Predictions on dev set)
- `test2.out` (Predictions on test set)
Predictions will be generated for Bonus:
- `dev_bonus.out` (Predictions on dev set)
- `pred` (Predictions on test set)


### Evaluation Instructions
To evaluate the predictions against the gold-standard dataset, use the `eval.py` script outlined below for task1, task2, and bonus task.
Replace the file names in these commands with your exact file path.

#### Evaluating Task 1 Accuracy

python eval.py -p dev1.out -g dev


#### Evaluating Task2 Accuracy

python eval.py -p dev2.out -g dev

#### Evaluating Bonus Task Accuracy

python eval.py -p dev_bonus.out -g dev

#### Test Sets
Use the test1.out, test2.out, and pred files for test sets:

python eval.py -p test1.out -g {your Task 1 test file}
python eval.py -p test2.out -g {your Task 2 test file}
python eval.py -p pred -g {your Bonus Task test file}


### File Handling Notes
- All input files are expected to be in the same working directory as the notebook.
- Output files (`*.out`) are stored in the same directory and must match the format of the training data.
- Ensure that the correct dataset (dev or test) is being used when generating predictions.
