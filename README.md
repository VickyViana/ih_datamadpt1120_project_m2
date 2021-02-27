# ih_datamadpt1120_project_m2
Ironhack Madrid - Data Analytics Part Time - February 2021 - Project Module 2


# **Breaking into the diamond market**
This project consists of an analysis of the the dataset 'diamonds_train.csv' (included in 'data' folder) in order to study the different features of the diamonds and how they affect in the price and between each other. The aim is to reach conclusions that will help us to understand the diamond market in terms of how to make the best deal. 

An extra bonus study has been performed, based on statistical hypotheses testing, comparing the different features of the diamonds in different samples.


<p align="center"><img src="https://raw.githubusercontent.com/VickyViana/ih_datamadpt1120_project_m2/main/__trash__/diamonds.jpg"></p>


## **First steps in the study**
The dataset 'diamonds_train.csv' contains 40454 rows of different diamonds and 10 columns with the following features:

- **Carat**: The weight of the diamond.
- **Cut**: Quality of the angles, proportions, facets, and finishing details. The cuts are classified from worst to best quality as: Fair --> Good --> Very Good --> Premium --> Ideal.
- **Color**: How colorless the diamond is. They are classified from less to more colourless as: J --> I --> H --> G --> F --> E --> D.
- **Clarity**: How clean the diamond is of inclusions and blemishes. They are classified from wort to best as: I1 --> SI2 --> SI1 --> VS2 --> VS1 --> VVS2 --> VVS1 --> IF

The meaning of these acronyms is:

	FL (Flawless)
	
	IF (Internally Flawless)
	
	VVS1 (Very, Very Slightly Included 1)
	
	VVS2 (Very, Very Slightly Included 2)
	VS1 (Very Slightly Included 1)
	
	VS2 (Very Slightly Included 2)
	
	SI1 (Slightly Included 1)
	
	SI2 (Slightly Included 2)
	
	I1 (Inclusions 1)
	
	I2 (Inclusions 2)
	
- **Depth**: Measurement from top to bottom, expressed as a percentage.
- **Table**: It is the width of the flat facet on its surface, expressed as a percentage.
- **Price**: Price in USD
- **x, y, z**: measures of the diamond in mm

A new column **'volume'** is created, multiplying measures x·y·z to obtain the relative volume of the diamond in mm3


First of all, to get an slight view of the dataset, we create a table with some basic statistical details of the data, like maximum, minimum, percentile, mean, std etc. You can see it below.

<p align="center"><img src="https://raw.githubusercontent.com/VickyViana/ih_datamadpt1120_project_m2/main/__trash__/resume_table.png"></p>



## **Price, what matters?**

For diamonds, as everything in the world, what matters most is the price. We want to center our analysis in how the price of the diamonds varies according to their characteristics, and which of these features has the most influence.

After comparing every feature with the price in a group of bar and scatter graphs, the only features that show a clear lineal relationship with the price are carat and the measures x, y and z (and consequently the volume). 

<p align="center"><img src="https://raw.githubusercontent.com/VickyViana/ih_datamadpt1120_project_m2/main/__trash__/carat_lineal.png"></p>

This fact suggests that the most influent feature how big the carat is (the size of  the diamond is proportional to weight).

Althougth this is a decisive discovery, further analyses are necessary to ensure the statement.

## **Analysis between features**

A comparation between two of the most important features is done, facing color with cut and seeing how their combiantion affects the price. The following bar graph has been done showing the average price and the count of diamonds of every combiantion.

<p align="center"><img src="https://raw.githubusercontent.com/VickyViana/ih_datamadpt1120_project_m2/main/__trash__/Color-Cut_Analysis.PNG"></p>

In general, it seems that the fact to have some color makes the diamond more valuable than the colorless (D). The second best cut (Premium) and the worst (Fair) in all categories of color have the highest average price, instead of cut 'Ideal', that is supposed to be the best. 
Maybe related with their rarity, as this type has the lower quantity. All these observations do not make much sense, so it is possible that another factor is at play.

Other comparation could be done, facing color with clarity and observing how the average price and the counting varies.

<p align="center"><img src="https://raw.githubusercontent.com/VickyViana/ih_datamadpt1120_project_m2/main/__trash__/Color-Clarity_Analysis.PNG"></p>
 
In the previous graph it can be seen that diamonds with color 'D' and clarity 'IF' are the most expensive from far. Is not a strange statement, as color 'D' and clarity 'IF' are the most flawless features. However, other types as colour 'I' or 'J' with clarity 'SI2' that are not very apreciate have high prices too, what is very strange.

At this point, the only thing that we have clear is that the carat influence the price, so the most logical thing to do is to compare them with these characteristics as well. Some box graphs have been done comparing the carat with the cut and with the clarity.

<p align="center"><img src="https://raw.githubusercontent.com/VickyViana/ih_datamadpt1120_project_m2/main/__trash__/box_cut.png"></p>
 
<p align="center"><img src="https://raw.githubusercontent.com/VickyViana/ih_datamadpt1120_project_m2/main/__trash__/box_clarity.png"></p>
 
 With these graphs it is clear that carat is a determining factor, because even if diamonds have features of low quality, the carats make their price rise considerably. In the end, **it was all in the carat!**


## **Other analysis: Table and Depth**

We wanted to carry out a small study to observe the Table and Depth features. At a first sight, the table does not seem to be a determining factor to choose a diamond. 
However, for professionals in the field it is well known that each cut has a specific table that makes them more brilliant.

<p align="center"><img src="https://raw.githubusercontent.com/VickyViana/ih_datamadpt1120_project_m2/main/__trash__/table_depth.png"></p>

This graph represents an inverse lineal relationship between table and depth, when the table is increased the depth decreases. 
This inverse formula is used to difine the diamond shape in order to archive the best reflection of light, a more beautiful sparkle and better visual balance.


## **Conclusions**

- The price of a diamond is lineal relationed with its carat (and consequently with the volume). Altough a diamon has not the best features, a big carat will make it very valuable. This fact justifies why ordinary people consider the carat as the most important feature in a diamond.
- Diamonds with cut 'D' and clarity 'IF' are the most expensive, as they have mostly the best cut ('Ideal'), have a relatively high carat and a low quantity available.
- The table and the depth of a diamond has a inverse lineal relationship. This creates a perfect diamond shape to enhance the shine.


:bell: Here you can find the Tableau dashboard with a resume of the most important data achieved --> [Dashboard](https://public.tableau.com/profile/maria.victoria.viana.colino#!/vizhome/ih_datamadpt1120_project_m2-Diamonds/DashboardDiamonds?publish=yes)


## **Technology stack**

- **Programming Language**: Python 3.8
- **Libraries in Use**: pandas, numpy, matplotlib, seaborn, scipy.stats.



## **Folder structure**
```
└── ih_datamadpt1120_project_m2
    ├── __trash__
    ├── .gitignore
    ├── README.md
    ├── Notebooks
    │   └── data_analysis_report.ipynb
    └── data
        └── diamonds_train.db
```     
   
     
:gem: :gem: :gem: :gem: :gem: :gem: :gem: :gem: :gem: :gem: :gem: :gem: :gem: :gem: :gem: :gem: :gem: 
:gem: :gem: :gem: :gem: :gem: :gem: :gem: :gem: :gem: :gem: :gem: :gem: :gem: :gem: :gem: :gem: :gem:
:gem: :gem: :gem: :gem: :gem: :gem:

 
