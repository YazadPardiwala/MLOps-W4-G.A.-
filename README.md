# Read Me
Work done for this assignment
1. Created a Week 4 Github repo with an unchanged version of the 'Model Creator.py' script from week 2 (which trains a decision tree & saves it as a model.joblib file), & a script 'test_model.py' which contains model & data validation code in a function which can be invoked by pytest.
2. Opened Google Cloud shell, cloned the repo made in step 1, installed requirements.
3. Fixed cloud storage bucket as the default DVC remote. 
4. Used DVC to get version 1 of the data.csv file (from the week 1 graded assignment's repos)
5. trained & saved the model.
6. Pushed to branch main of the Github repo made in step 1 (creating branch main in the process)
7. Made new branch "development" in the shell environment.
8. Created a github workflow file runtest.yaml. Uploaded it to the cloud shell environment into the appropriate directory for workflow actions to function.
9. Updated GCS Bucket security settings to allow object access to the Github workflow.
10. Pushed local "development" branch to remote github repo; workflow configured to trigger on the push.

## Model Creator.py Script
Same script as submitted in week 2's assignment.

Tasks performed by the script :-

1. Data importing, train test split.
2. Model training.
3. Saving model as joblib object.

## test_model.py Script
Same script as submitted in week  2, only modified to be invokable by pytest.

Tasks performed by the script :-

1. Fetching the model.joblib file from the working directory & unpacking it.
2. Importing data/data.csv, performing a train-test split on data.
3. Getting model's precision score for both train & test splits of the dataset.
4. Saving precision score and no. of samples in the dataset as 'eval results.txt' file.
5. Assert that train precision is > 0.95 and test precision is > 0.9
