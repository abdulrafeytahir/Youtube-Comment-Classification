# Youtube-Comment-Classification (POC)
The project is developed for Youtube content creators who don't have the time to scroll through all of the comments on every single video on their channel and filter out the ones that are requests from their viewers and subscribers.

This project solves the problem by scrapping comments data through a channel and building/training a machine learning classifier to predict whether a comment is a reqeust from a viewer/subsriber or not. The more channels it is trained on the better it gets in terms of precision.

## Packages Required:

beautifulsoup4            4.8.1                    
gensim                    3.8.1                    
jupyter                   1.0.0                    
lxml                      4.4.2                    
matplotlib                3.1.2                    
nltk                      3.4.5                    
notebook                  6.0.2                    
numpy                     1.17.4                   
pandas                    0.25.3                   
pip                       19.3.1                     
scikit-learn              0.22.1                   
scipy                     1.4.1                    
seaborn                   0.9.0                    
selenium                  3.141.0                  
urllib3                   1.25.7                   
xgboost                   0.90                  

## Scrapping:

1) Open Scrapping.ipynb and run the first cell to import libraries.
2) Set the value of url variable to the url string of the channel from which you want scrape data and run the cell.
3) Run the next two cells and the scrapper will start scraping comments from that channel.
4) Finally run the last cell to save all comments in a csv file.

Note: The format of the data should be same accross all files. There should only be 3 columns with the following column names: Username, Comment, Label. The spelling should be exactly the same.


## Model Training:

1) Open Comment Classification notebook and run the first cell to import libraries.
2) Add names of all files in files list in second cell and run it.
3) Run all subsequent cells right until the last so that the data is preprocessed, model is trained and saved in a pickle file.

Note: In cell 21 right below the first visualization, there's a variable called ratio which is set to 0.3. This means that we are taking 30% of all not-request comments/data to balance the distribution. This can be changed when we add more correctly labelled data.

## Predictions from Model:

1) Open Comment Predictions from Model notebook and run the first cell to import libraries.
2) Provide filename for file variable for which you want to get predictions.
3) Run all subsequent cells so that model is loaded from svm.pkl file and you get predictions from model saved in a separate csv file.




