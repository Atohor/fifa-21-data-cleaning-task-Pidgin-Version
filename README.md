# fifa-21-data-cleaning-task-Pidgin-Version
### Note  

if u know say u nor sabi read pidgin English then this article nor be for you , jejely waka pass go look the oyibo version here [English Version](https://github.com/Atohor/fifa-21-data-cleaning-task)

![image](https://user-images.githubusercontent.com/99989624/225207183-90da42a8-4882-4a3b-ae06-9508c305f4ad.png)


Oyibo talk say person wen never fit clean d dirty wen dey for inside e house , how the outside compound won take clean ?  And for Data analysis , the inside house na be the data , while analysis/visualization na the outside compound . So follow me waka make we go clean our inside house 


<div>
    <h2>Introduction</h2>
</div>

this now how I take jejely clean the FIFA 21 dataset when some big names for the data industry drop ontop twitter , make omomo analyst and egbon analyst take try their hands, wether you sabi work or you be jjc .Dem tag the challenge #Datacleaningchallenge.

Omo The data sef nor be small data , e carry 77 columns and 18,980 rows on everything about many footballers for around 2021. The dataset dey where everybody go fit see am for [kaggle](https://www.kaggle.com/datasets/yagunnersya/fifa-21-messy-raw-dataset-for-cleaning-exploring) and the guy when run am  gather scrap the data from [sofifa](www.sofifa.com)

Them still drop dictionary about this data when go give you more expo about the footballers incase some things de miss from your data or you nor too understand some kind stuff for the data 

Many tools dey when person fit take tackle data cleaning .For me personally, Based on sability, I come choose Power Query editor when de ontop power query to take battle this challenge

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
this one mean say any column when too lean because e dey lack nutrient, we need give am vitamin boost make e for dey alright . I come reason am say the Age column still dey show their age for 2021 and we don enter 2023 . Na once I Nack +2 for all their age.
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

This two brothers when be Name and Longname column , I come separate the players name by how them take arrange (the oyibo word na to split by delimiter). I gats split them like 3 times and once you split any column , e don create new column be that . So some kind rows come de show empty but after I repackage everything, na only two columns when I call first name and last name come remain .

Some people when de answer 2 in 1 names like all those dem De Bruyne , Ter Stegan , Van Dijk .I still position dem well like that  

| Before | After |
|--------|-------|
![image](https://user-images.githubusercontent.com/99989624/224680924-00835e64-6273-4c6e-aab9-a472fe3cea3b.png)|![image](https://user-images.githubusercontent.com/99989624/224681183-81a31f33-425e-4105-a848-ebf7d3134ecc.png)


Wahala never finish o , if you click the filter button , e get some kind names with wicked pronunciation when them nor get English letter for, all these kind names like Spanish names de normally carry tribal marks for head ( when oyibo de call Diacritic names ).

And if we nor package them , when person one visualise the data now, you come say if your name start from A stand up, dem go sitdown , if your name start from B stand up , them go still sitdown oo, till you reach Z sef .Na after Z, them go come start to de stand up small small and this thing nor good for visualisation. 
So I come use another column “player url “ take extract the clean version of the names without this tribal marks to take package am well.

| Before | After |
|--------|-------|
![image](https://user-images.githubusercontent.com/99989624/224684006-6287fa7c-6d31-408c-99bd-95125ad152d5.png)|![image](https://user-images.githubusercontent.com/99989624/224684358-ea94ad53-b786-43db-8d29-38e647689471.png)

E never still finish ontop this names matter o, Wahala nor come too much like this ?.


some Names them wen carry dot, like C.Ronaldo , A.Benjamin , G.Paiva , I still package dem well make the complete name de show .


<div align="center">
    <h2>Percentages</h2>
</div>

When I read the data dictionary, them talk say these columns OVA and POT suppose be percentages . So I just use one sharp button when be “column from examples “. 
I use am add % for the first row number , this sharp button too know book so e just help me complete the rest .Then na to just the data type to percentage.

| Before | After |
|--------|-------|
![image](https://user-images.githubusercontent.com/99989624/224689449-f6a490f1-e016-4058-9373-71487095283d.png)|![image](https://user-images.githubusercontent.com/99989624/224689726-1884d63f-e22e-4b70-8a67-3dbead6aa4ed.png)


<div align="center">
    <h2>Clubs</h2>
</div>

E get some kind club when their names start with 1. Example 1. Fc koln , 1. Fc union Berlin. Nor be say na mistake o , truly truly na the name when their papa give them be that. But we de normally comot the number if not, just like the names column if I call A-Z sef dem nor go gree stand up and e nor good for visualisation so I package them well.


| Before | After |
|--------|-------|
![image](https://user-images.githubusercontent.com/99989624/224834902-356b3ed5-c7e0-489c-87d2-b3602bc91364.png)|![image](https://user-images.githubusercontent.com/99989624/224835627-e81bbc9a-7c95-41e9-a1e3-5be5cef1ac2c.png)


<div align="center">
    <h2>Contract</h2>
</div>

This column “contract “ scatter leg anyhow yafu-yafu, so I come call on e brothers “joined “ and “ loan end date “ make them help me run am well.

When I click filter ontop the contract column , I see say some kind players when dey on loan , na the same details dem get for the “loan end date “ column . Then for players when be free , dem nor get loan end date , them nor get club , them nor get wage , dem nor get value , dem nor get release clause, everything zero . So, I come replace all these free guys with null for my contract column and when I one visualise I gats drop them kpatakpata from the data cause dem useless for analysis .

Sha after I don clean , separate, and do somekind join join I come end up with only 2 columns “contract start and contract end “ when go show the year the player contract take start and the year e end 

| Before | After |
|--------|-------|
![image](https://user-images.githubusercontent.com/99989624/224838470-25cd2741-d7bf-479b-8ff7-14d2917f498c.png)|![image](https://user-images.githubusercontent.com/99989624/224838770-df41bf1a-5391-4bdd-8a17-99c4a7da1cb5.png)

If you look well the data type for my contract start and end date nor be date na ABC. This na because if I change am to date format , e go like show months and days and over sabi power query go dash all the rows first day and first month like this 1/1/2022 or 1/1/2020 throughout ,even though nor be the right day or month be that, well na because of lack of more info . So when time for visualisation don reach , when person change the data type to date , na to use only the year drill down nor add day or month.


<div align="center">
    <h2>Positions</h2>
</div>
 
**Separate am or leave am :?** This column na for the wing when the players de normally play . Some sabi play like 2 to 3 wings and dem jam everything together for one row. I come reason am say to split am na waste of Memory space since another column when be e brother “best position “ still de . And that best position column make sense die to take use analyse our data. So like this na to delete the column “positions” .,Make we leave only  the best position 

| Before | After |
|--------|-------|
![image](https://user-images.githubusercontent.com/99989624/224841755-aac24509-7c26-40e5-b46b-4cdc8ddca9e7.png)|![image](https://user-images.githubusercontent.com/99989624/224841978-f61c750b-4ae4-40fe-9af7-8f7208547b2b.png)


<div align="center">
    <h2>Height</h2>
</div>

Many players for here dem record their heights in centimetre (cm) , then some others na feet and inches them use . Like this 6’2” . At first, i reason say na to separate this thing ‘ “ comot then times the figure by 30.48 because that na be normal feet to cm conversion rate . But SeniorMan google say e nor correct like that , seniorMan google say the feet na to times am with feet rate and the inches I need to times am separate with inches rate . 

Who I be to follow SeniorMan google argue ? So after I split the columns, I times the feet by 30.48 , I come times the inches by 2.54. Las las,  I come add everything together for one column. 
The other guys when de in centimetre carry “cm “ join body like this 170cm So I come still drop the cm comot .Package everything well 

| Before | After |
|--------|-------|
![image](https://user-images.githubusercontent.com/99989624/224844971-31f4648e-2b1f-42d8-99b7-84e1a376a428.png)| ![image](https://user-images.githubusercontent.com/99989624/224845368-72935580-ede4-44b1-94bd-d5db1d4866e8.png)


<div align="center">
    <h2>Weight</h2>
</div>

My eagle eye tell me say like 60% of the players here them write their weight as lbs (this na another name for pounds but nor be the money £ pounds o, this na when some oyibo countries one talk about weight in pounds dem go write am as lbs ) like this 70lbs . While the rest na Kilogram them take code am like this 60kg.

E choke ? . Me personally I decide say na lbs I want make everything de cause na them many pass . So I come split the column with "digit to non -digit function". then i use the normal conversion rate of 2.205 take times the kg guys to give me the lbs version, then round am up make the figures nor carry decimals.

| Before | After |
|--------|-------|
![image](https://user-images.githubusercontent.com/99989624/224845690-2cb91c6f-bcf9-478f-b1d7-0dc5cc0e8b76.png)|![image](https://user-images.githubusercontent.com/99989624/224846437-d180ffa8-277e-400c-aa69-a2051aed01f5.png)


<div align="center">
    <h2>Value , Wage and release clause</h2>
</div>


This 3 columns dey in euros and na swagger them take write the values. For example 1,500 na like this €1.5k and 1,500,000 na €1.5m. This kind sexy swagger nor go fit work for analysis . So we first drop the € symbol with find and replace . Next we gats split the column by M and K , then create new custom column when go multiply K values with 1000 and M values with 1,000,000 . This formula go give us the full figure for this wage , value and release clause column .

But wait o ! story never finish , we still like convert this full form figures from €uro to dollar$ So we gats times this figures by 1.183 . This na be the average €uro to dollar$ conversion rate for around 2021 when them take create this data.

| Before | After |
|--------|-------|
![image](https://user-images.githubusercontent.com/99989624/224848874-1db3b234-8f91-4a58-8aa8-62e4db072d38.png)|![image](https://user-images.githubusercontent.com/99989624/224849112-0e74cdb0-ceb6-4a38-bc4d-4efc3f9ccf43.png)

<div align="center">
    <h2>W/F , SM , IR</h2>
</div>

 These three columns contain player ratings for different aspect , and na scale of 1-5 them use rank am . But them add star symbol to the coding.
 Wow! make I call these columns star boys cause E choke !.
 
 But we nor really need the stars cause e go scatter our visualisation. So Na to remove the stars using find and replace na sure pass, then change the data type from ABC to 123.

| Before | After |
|--------|-------|
![image](https://user-images.githubusercontent.com/99989624/224855858-546c4bdf-adb2-421a-a459-f799a7f1a241.png)|![image](https://user-images.githubusercontent.com/99989624/224855981-166a7132-bbb1-4451-89e5-62f9b43d66dd.png)

<div align="center">
    <h2>Hits</h2>
</div>

For the filter mode , you go see say some numbers for here na still swagger dem take write dem , 1500 na like this 1.5k. So I gats package am the way I take run the wages column when I don explain before so . 

| Before | After |
|--------|-------|
![image](https://user-images.githubusercontent.com/99989624/224856470-037630d2-1429-4644-b107-d5b88323fa32.png)|![image](https://user-images.githubusercontent.com/99989624/224856581-0ff90894-e6da-4edc-b25a-850a3b59e966.png)


<div align="center">
    <h2>CONCLUSION</h2>
</div>

Day don dark ontop this cleaning matter but las las we don run am, we come still use eagle eye observe say our data accurate , e complete , and e consistent . Na oyibo de call data validation .

At first when I use corner eye look this challenge , e be like say water go pass garri o , but I draw my trouser up , gather mind , use ginger complete this #Datacleaningchallenge . Even though I don go far small for this data industry , this challenge don still open my eye well well ,to some kind things when every analyst need to learn. 

Them never born the person when fit claim say e know everything for this data industry , so like this, if you get one or two when fit help my career , or you use okpolor eye take see some things when my eagle eye nor see , abeg let me know .

If you still de run kititi, de run katata like chicken when dem cut e head ontop this challenge , nor run again , come meet me, I go help you make we package am together .

Any day , any time , You fit holla @ your boy ontop twitter [@PidginAnalyst](https://twitter.com/Pidginanalyst) | Instagram  [@PidginAnalyst](https://Instagram.com/Pidginanalyst) 


#PS to speak or listen to pidgin English easy , to write am out hard small , but to come even fit read am well, understand-am well , That one na War oo . So if you really settle down read this whole thing from beginning to this ending , I carry hand give you ! NA YOU TRY PASS! i hail ooo !!!  
