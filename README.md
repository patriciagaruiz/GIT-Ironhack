# GIT-Ironhack
Repositório de projetos da Ironhack

<h1 align="center"> SHARK ATTACK </h1>
<h1 align="center"> Data Cleaning and Manipulation </h1>




![ec108e76abc8ba235183e1043243f8c7](https://user-images.githubusercontent.com/99502330/161838073-aa87e39a-1afc-4459-9d06-b6a556085659.jpg)


<h1 align="left"> Main Objectives </h1>

Apply the different cleaning and manipulation techniques to generate a cleaner CSV version of this data.
Look for something you want to answer about shark attacks and try to answer that using data.

![Humans are friends!](https://user-images.githubusercontent.com/99502330/161834340-92521684-877f-495d-8df9-ec22bfacb2fc.jpg)

<h1 align="left"> The Datasets </h1>

The mission of the Global Shark Attack File is to provide current and historical data on shark/human interactions for those who seek accurate and meaningful information and verifiable references.
Dataset available at: https://www.kaggle.com/datasets/teajay/global-shark-attacks.


<h1 align="left"> Import File </h1>

The dataset has 25.723 lines and 24 columns.

<h1 align="left"> Heatmap before dropping duplicate values </h1>

![Heatmap_before](https://user-images.githubusercontent.com/99502330/161841837-245a2a81-1254-468b-85cd-5caeb78c776a.png)

<h1 align="left"> Heatmap after dropping duplicate values </h1>

![Heatmap_after](https://user-images.githubusercontent.com/99502330/161843475-aaa14977-13fe-4672-b22b-6c18c98d915e.png)


Cleanned Dataset has 6.302 lines and 23 columns.

<h1 align="left"> 1. Are there more fatal than non-fatal attacks? </h1>

This answer needs a clean column called: Fatal (Y/N).
First of all, I used 'groupby' to discover the number of lines per value. Here the results: 2017, N, M, Y, y, UNKOWN.
I read the lines with values different from Y or N and changed the wrong values by Y, N or X (for unclear cases where the identification was not possible).

CONCLUSION: There are more non-fatal attacks according to the data.

Total Shark Attacks with Known Results: 5692 attacks

Fatal Shark Attacks: 1389 attacks / 24.4 %

Non Fatal Shark Attacks: 4303 attacks / 75.6 %

*** Attacks with Unknown Results: 71 attacks / 1.23 % (disregarded in the previous analysis)

![shaaark183](https://user-images.githubusercontent.com/99502330/161834643-751fe82d-f9d7-4b89-8836-52da63639d59.jpg)




<h1 align="left"> 2. Are there more attacks for male or female? </h1>

This answer needs a clean column called: Sex.
First of all, I used 'groupby' to discover the number of lines per value. Here the results: . , F, M, N, lli.
I read the lines with values different from M or F and changed the wrong values by M, F or X (for unclear cases where the identification was not possible).

CONCLUSION: There are more attacks to male according to the data.


Total Shark Attacks with Known Gender: 5735

Male Shark Attacks: 5098 attacks / 88.89 %

Female Shark Attacks: 637 attacks / 11.11 %

*** Attacks with Unknown Results: 71 attacks / 1.23 % (disregarded in the previous analysis)




![shark_boat_men](https://user-images.githubusercontent.com/99502330/161890970-fcc257d9-9f09-42db-b784-7946a1875867.gif)


<h2 align="left"> OTHERS CONCLUSIONS </h2>
Crossing valid lines related to fatal attacks (5.692) and attacks by gender (5.735) I extracted a double groupby:

![Graf2](https://user-images.githubusercontent.com/99502330/161891257-bbde61ee-30f4-455f-be43-e5904ce6ce8f.png)

<h1 align="left"> 3. Are shark attacks influenced by hemisphere? </h1>

This answer needs a clean column from main database called: Country.
Even though this column does not provide the information needed to answer the question because it doesn’t tell in which hemisphere the country is, I used a database of coordinates (latitude/longitude) to find out this information. I used a database of coordinates (latitude/longitude) for countries to find out this information. Dataset available at: https://www.kaggle.com/datasets/max-mind/world-cities-database.

![sharks-swimming](https://user-images.githubusercontent.com/99502330/161890934-c355c48d-616a-4ac3-aa84-67fa93ead0bc.gif)

I used 'unique' to discover the values into the main database (199 countries) and compared with the database of coordinates.
Countries after cleanning database: 142

CONCLUSION: There are more shark attacks in Northern Hemisphere

Total Shark Attacks with Known Hemisphere: 6183 attacks

Hemisphere Northern: 3409 attacks / 55.14 %

Hemisphere Southern: 2774 attacks / 44.86 %

*** Attacks with Unknown Hemisphere: 119 attacks / 1.89 % (disregarded in the previous analysis)





