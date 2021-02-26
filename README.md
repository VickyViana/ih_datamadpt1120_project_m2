# ih_datamadpt1120_project_m2
Ironhack Madrid - Data Analytics Part Time - February 2021 - Project Module 2


## **Breaking into the diamond market**
This project consists of an analysis of the the dataset 'diamonds_train.csv' (included in data folder) in order to study the different features of the diamonds and how they affect in the price and between each other. The aim is to reach conclusions that will help us to understand the diamond market in terms of how to make the best deal. 

An extra bonus study has been performed, based on statistical hypotheses testing, comparing the different features of the diamonds in different samples.


<p align="center">
<img src="https://www.istockphoto.com/es/foto/diamantes-gm157338784-6240149">
</p>


## **First steps in the study**
Clone this repository to your local folders. 

:warning: Please be aware of the python version you are using and the libraries you need to have installed. See "Technology stack" section.

In console write down --> python main.py  --> You will get the result for all countries. Other way could be --> python main.py --country "all"

In console write down --> python main.py -co 'Country name' --> You will get the result for the country you wrote. 
Other way could be --> python main.py --country 'Country name'

Yo can choose any of the following countries: 'Belgium', 'Greece', 'Lithuania', 'Portugal', 'Bulgaria', 'Spain', 'Luxembourg', 'Romania', 'Czechia', 'France', 'Hungary', 'Slovenia', 'Denmark', 'Croatia', 'Malta', 'Slovakia', 'Germany', 'Italy', 'Netherlands', 'Finland', 'Estonia', 'Cyprus', 'Austria', 'Sweden', 'Ireland', 'Latvia', 'Poland' and 'Great Britain'. 
Don't forget to use ''!! 

The results would be printed in console as well as in a Table_'country'.csv file in Results folder, in order to use them for later analyses. The table obtained will be similar to this:

| Country | Job Title | Gender | Quantity | Percentage |
|---|---|---|---|---|
| Austria | Data Administrator| Male | 4 | 6% |
| Austria | Data Administrator| Female | 3 | 4% |
| ... | ... | ... | ... | ... |


To get the bonus information it is just needed to add the following command in console --> python main.py --country 'Country name' --bonus1 y . Other way could be --> python main.py --country 'Country name' -b1 y.

The rable resulted looks like this:

| Position | Number of Pro Arguments | Number of Cons Arguments |
|---|---|---|
| Against | 0 | 2 |
| In Favor | 1 | 1 |

## **Conclusions**

- The price of a diamond is lineal relationed with its carat (and consequently with the volume). This fact justifies why ordinary people consider the carat as the most important feature in a diamond.
- Diamonds with cut 'D' and clarity 'IF' are the most expensive, as they have mostly the best cut ('Ideal'), have a relatively high carat and a low quantity available.
- The table and the depth of a diamond has a inverse lineal relationship. This creates a perfect diamond shape to enhance the shine.


Here you can find the Tableau dashboard with a resume of the most important data achieved --> [Dashboard](https://public.tableau.com/profile/maria.victoria.viana.colino#!/vizhome/ih_datamadpt1120_project_m2-Diamonds/DashboardDiamonds?publish=yes)


## **Technology stack**

- **Programming Language**: Python 3.8
- **Libraries in Use**: pandas, numpy, argparse, sqlalchemy, requests, beautifulsoup4, functools.



## **Folder structure**
```
└── ih_datamadpt1120_project_m1
    ├── __trash__
    ├── .gitignore
    ├── requirements.txt
    ├── README.md
    ├── main.py
    ├── p_acquisition
    │   ├── __init__.py
    │   └── m_acquisition.py
    ├── p_analysis
    │   ├── __init__.py
    │   └── m_analysis.py
    ├── p_wrangling
    │   ├── __init__.py
    │   └── m_wrangling.py
    ├── Results
    │   ├── Table_all.csv  
    │   └── Table_b1_all.csv
    └── data
        └── raw_data_project_m1.db
```     
   
     
## **Next steps**
 - It would be a good upgrade to improve the loop of acquisition API data to get the information faster.
 - There is needed a modification of bonus 1 functions in order to avoid warnings and get a more efficient code.
 

 
