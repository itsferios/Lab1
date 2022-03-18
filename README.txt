LAB1 
MICHELA PIROZZI - 732531
FERIOLI SARA - 733105

You can find here the links of the datasets we used. We couldn't upload them in the Github repository as they are too big (even the zipper file was too big).
https://www.dati.lombardia.it/Attivit-Produttive/Rapporti-di-lavoro-attivati/qbau-cyuc
https://www.dati.lombardia.it/Attivit-Produttive/Rapporti-di-lavoro-prorogati/chng-cman
https://www.dati.lombardia.it/Attivit-Produttive/Rapporti-di-lavoro-cessati/nwz3-p6vm

The datasets we used are on the various types of contracts for people living in Lombardy. In particular, we focused on the pre and post covid years (2018, 2019, 2020, 2021). 

1. Analysis with “Rapporti_di_lavoro_di_attivati.csv”

1.1 How has covid affected the types of activated contracts?
At this point, we analyzed the numbers of contracts activated in the various years, checking the trend of the main types of contract (extracted according to frequency).  
We noted that in the years 2018, 2019, 2020 and 2021, “Lavoro Domestico” has increased, while contracts for “Tirocinio” decreased. 

1.2 Which sectors have been most affected by covid? 
We have extracted the sectors most affected in the covid years, in terms of contracts activated in this period. Also in this case, we preferred to select some of the most present sectors within the dataset (to avoid visual problems in our graphs), always according to their occurrence.
What is noticeable is that the hotel (“Alberghi”) and catering (“Ristorazione con somministrazione”)  sector has decreased, while the “Attività di famiglie e convivenze come datori di lavoro per personale domestico”.
												
1.3 How are changed the work opportunities before and after covid? 
We only considered 2019 and 2021, in order to make a comparison between the values of the pre and post covid years.  
At this point, we have analyzed the different values of the types of contracts activated over the years, depending on the city. These values are shown in the first (map) and second graph.
Furthermore, in the third graph, we have considered the sectors (and not the provinces as in the previous graphs) in the years considered, noting a decrease in the numbers of active contracts in 2021, post covid. 

1.4 How covid has affected the active contract according to age and gender?
In this case, we split the covid years, into before and after, putting the values into two different DataFrames (datibefore and datiafter), then creating other DataFrames depending on the genre. These new 4 DataFrames were then used for the graphical representation. 
It is noticeable that male contracts are always greater than those of females, but that however in proportion to pre covid data, both gender categories have decreased. 

2. Analysis with “Rapporti_di_lavoro_di_prorogati.csv” + “Rapporti_di_lavoro_di_cessati.csv”

2.1 Comparison between extended and terminated contracts during covid.
We only considered the date and province of the company, for both the extended and terminated contracts datasets, and considered the post covid 2020 and 2021 years. 
After having created two datasets specifically for the two types of contracts ("selectedprorogati", "selectedcessati"), we have created a new DataFrame (“union”), which is the union of the two. 
This has been done in order to represent the data in the pie chart, where we can see the number of contracts extended is greater than those terminated, despite the end of covid and the removal of “Blocco dei licenziamenti”. For each of the categories of contract, one can also see the relationship between the various provinces.
In the second graph, considering 2018-2019-2020-2021, you can see that during the lockdown period, the number of both contract categories decreased dramatically. But as soon as the period ended (between the green lines), they increased again. 

3. Analysis with all 3 dataset

3.1 Which sectors have more or less active, extended or terminated contracts, during covid?
At this point, all three datasets were considered, to assess which sectors were most affected during the covid. To find our result, we used the max() and min() operators, applied on DataFrames divided by category (activated, extended, and terminated) and divided by year (activated20, activated21, extended20, etc.).

3.2 For the sectors of the previous point, what is the average/median age?
This point is related to the previous one, because we take the sectors with the highest values, and calculate the average age. We see that the average age for activated and extended contracts decreased in 2021, compared to 2020, but the average age for terminated contracts remained the same. 
