# Babies Names Recommender

## Aim
The recommender will give you 3 names that you might like according to you own input.

## Source
nat2022.csv: https://www.insee.fr/fr/statistiques/7633685?sommaire=7635552

## Datasets
names_per_year.csv: list of names and many features (see Features below)

data_tableau3.csv: re-arranged data from names_per_year.csv to use it in Tableau

nat2022.csv: (original dataset) list of name per year and the number of time it is given for the given year.

## Python
Babys_names_DATA: the notebook with cleaned data and where features (from calculations and web scraping) were added

Baby_names_MODEL: the notebook where the model and the recommender are build

Baby_names_TABLEAU: the notebook were the data are build to fit in Tableau

## Tableau
https://public.tableau.com/app/profile/cyrielle.mary/viz/End-Project2/evolmixed?publish=yes

## Presentation
https://docs.google.com/presentation/d/1xSQdHUB5vU8_BC79FR78y3M1EkUtxlx7ondPLuQd8zI/ 

## Recommender
The recommender works as the following:

1- ask for input genre: "boy or girl?"
    
    2- ask for input name: what name do you like ?

    3- if input name in names_cluster DF == F
    
        3a- search the cluster of input name 
          
        3b- give a recommandation from the same cluster
          
          4- input question: do you like the name?
          
              4a- if yes, give another name from the same cluster
          
              4b- if no, give a name from another cluster 
          
              5- input question: do you like the name?
              
                  5a- if yes, give another name from the same cluster
          
                  5b- if no, give a name from another cluster 
          
    6- if input name in names_cluster DF == M
    
        6a- search the cluster of input name
          
        6b- give a recommandation from the same cluster
          
        7- input question: do you like the name?
          
            7a- if yes, give another name from the same cluster
          
            7b- if no, give a name from another cluster 
          
             8- input question: do you like the name?
              
                  8a- if yes, give another name from the same cluster
          
                  8b- if no, give a name from another cluster 


### Here is an example of a try:
Are you looking for a recommandation for a girl or a boy? Please enter girl or boy: girl

Enter a name you like: CARLA

Our recommendation is AMEL.

Do you like this name? please answer yes or no: YES

Our next recommendation is HÉLOÏSE.

Do you like this name? please answer yes or no: NO

Our last recommendation is PRISCA. Thank you for using our recommender
