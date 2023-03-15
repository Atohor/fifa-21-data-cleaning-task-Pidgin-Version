# fifa-21-data-cleaning-task-Pidgin-Version
### Note  

if u know say u nor sabi read pidgin English then this article nor be for you , jejely waka pass go look the oyibo version here [English Version](https://github.com/Atohor/fifa-21-data-cleaning-task)

![image](https://user-images.githubusercontent.com/99989624/225207183-90da42a8-4882-4a3b-ae06-9508c305f4ad.png)


Oyibo talk say person wen never fit clean d dirty wen dey for inside e house , how the outside compound won take clean ?  And for Data analysis , the inside house na be the data , while analysis/visualization na the outside compound . So follow me waka make we go clean our inside house 


<div>
    <h2>Introduction</h2>
</div>

this now how I take jejely clean the FIFA 21 dataset when some big names for the data industry drop ontop twitter , make omomo analyst and egbon analyst take try their hand wether dem sabi work to fit lick this dirty data plate make e de shine wella . Dem tag the challenge #Datacleaningchallenge.

Omo The data sef nor be small data , e carry 77 columns and 18,980 rows on everything about many footballers for around 2021. The dataset dey where everybody go fit see am for [kaggle](https://www.kaggle.com/datasets/yagunnersya/fifa-21-messy-raw-dataset-for-cleaning-exploring) and the guy when run am  gather scrap the data from [sofifa](www.sofifa.com)

Them still drop dictionary about this data when go give you more expo about the footballers incase some things de miss from your data or you nor too understand some kind stuff for the data 

Many tools dey when person fit take tackle data cleaning .For me personally, Based on sability, I come choose Power Bi editor when de ontop power query to take battle this challenge

## Data Cleaning process
![image](https://user-images.githubusercontent.com/99989624/225212198-d3deb93a-14d6-4a70-936f-76c674bf8645.png)

To make sure say my data na ogbonge quality , see how i take run am pass 


After I load the data , the space too much for inside so to remove the spaces ,na just one button I click for the view tab . Dem call the button “show white spaces “ . I say no nor show am , cause the spaces them too many, e almost reach one plot of land.


<div align="center">
    <h2>Whitespaces</h2>
</div>

| Before | After |
|--------|-------|
![image](https://user-images.githubusercontent.com/99989624/224610838-f6b78c4b-b204-42d9-b158-f7aeacb6cda8.png)| ![image](https://user-images.githubusercontent.com/99989624/224610689-763b528d-9eed-431a-8b7d-2d5a54abaa32.png)


**1. Data Auditing** :
this one mean say I use eagle eye take observe my data, make i for see all the dirty things when I need scrub well for my data. I see many columns when my broom of justice go touch ; name , longname , Age , OVA , POT , Club , contract , Positions , height , weight , Best position , Joined , Loan end date , value , wage , release clause , W/F , SM , IR , And hits .

**2. Data enrichment** : 
this one mean say any column when too lean because e dey lack nutrient we need give am vitamin boost make e for dey alright . I come reason and say the Age column still dey show their age for 2021 and we don enter 2023 . Na once I Nack +2 for all their age.
But I nor delete the first age column , I still leave am say person fit choose which one e go use wether na the 2021 age or na this new 2023 age when I just package .

<div align="center">
    <h2>Age</h2>
</div>


| Before | After |
|--------|-------|
|![image](https://user-images.githubusercontent.com/99989624/224671691-bc17297f-d433-42b2-801b-2a5c614b0fff.png)|![image](https://user-images.githubusercontent.com/99989624/224671895-e15292ce-058d-4fa1-a691-7a36ed032e3d.png)|


**3. Data Cleaning and Transformation** 
All those dirty columns when I mention before so , Oya make we start to de wash them one by one 

<div align="center">
    <h2>Names</h2>
</div>

This two brothers when be Name and Longname column , I come separate the players name by how them take arrange (the oyibo word na to split by delimiter). I gats split them like 3 times and once you split any column , e don create new column be that . So some kind rows come de show empty but after I repackage everything na only two columns when I call first name and last name come remain . Some people when de answer 2 in 1 names like all those dem De Bruyne , Ter Stegan , Van Dijk .I still position dem well like that  

| Before | After |
|--------|-------|
![image](https://user-images.githubusercontent.com/99989624/224680924-00835e64-6273-4c6e-aab9-a472fe3cea3b.png)|![image](https://user-images.githubusercontent.com/99989624/224681183-81a31f33-425e-4105-a848-ebf7d3134ecc.png)


Wahala never finish o , if you click the filter button , e get some kind names with wicked pronunciation when them nor get English letter for, all these kind names like Spanish names de normally carry tribal marks for head ( when oyibo de call Diacritic names ).

And if we nor package them , when person one visualise the data now, you come say if your name start from A stand up, dem go sitdown , if your name start from B stand up , them go still sitdown oo till you reach Z sef .Na after Z them go come start to de stand up small small and this thing nor good for visualisation . 
So I come use another column “player url “ take extract the clean version of the names without this tribal marks to take package am well.

| Before | After |
|--------|-------|
![image](https://user-images.githubusercontent.com/99989624/224684006-6287fa7c-6d31-408c-99bd-95125ad152d5.png)|![image](https://user-images.githubusercontent.com/99989624/224684358-ea94ad53-b786-43db-8d29-38e647689471.png)

E never still finish ontop this names matter o, Wahala nor come too much like this ?
some Names them wen carry dot, like C.Ronaldo , A.Benjamin , G.Paiva , I still package dem well make the complete name de show .

<div align="center">
    <h2>Percentages</h2>
</div>

When I read the data dictionary, them talk say these columns OVA and POT suppose be percentages . So I just use one sharp button when be “column from examples “. 
I use am add % for the first row number , this sharp button too know book so e just help me complete the rest , then na to just the data type to percentage.

| Before | After |
|--------|-------|
![image](https://user-images.githubusercontent.com/99989624/224689449-f6a490f1-e016-4058-9373-71487095283d.png)|![image](https://user-images.githubusercontent.com/99989624/224689726-1884d63f-e22e-4b70-8a67-3dbead6aa4ed.png)


