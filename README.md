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


**1. Data Auditing**
this one mean say I use eagle eye take observe my data, make i for see all the dirty things when I need scrub well for my data. I see many columns when my broom of justice go touch ; name , longname , Age , OVA , POT , Club , contract , Positions , height , weight , Best position , Joined , Loan end date , value , wage , release clause , W/F , SM , IR , And hits .
