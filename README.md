# MIST4610-Group-Project-1
Team Name: 29704 1

# Team Members
1. Jillian Bolgla [@jillianbolgla](https://github.com/jillianbolgla)
2. Conor Dillon [@cjdillon11](https://github.com/cjdillon11)
3. Brandon Hopper [@bhop19](https://github.com/bhop19)
4. Neha Panchal [@nehapanchal2001](https://github.com/nehapanchal2001)
5. Shrija Ramachandran Ganesh Mohan - [@shrija-27](https://github.com/shrija-27)
6. Alvin Vasanthakumar - [@alvinvasanth](https://github.com/alvinvasanth)

# ChatGPT Response
https://docs.google.com/document/d/1RU8uZK5zfxMJaa5XlytWOYu2rA_4dH5KpP6m32WwGoM/edit?usp=sharing 

# Problem Description
We are tasked with creating a relational database and data model for the owner of a football club. In our model the central entity is the Club. Each club has teams that operate in different divisions and in various locations. The club operates in conjunction with matches, training sessions, ticket sales, etc. that it offers to fans who support the teams.We want to accurately model these relationships, generating sample data, and populating entities and queries with the sample data. Additionally, we are planning on performing functioning queries on this data so that they can provide us with valuable player and coach statistics as well as the overall club performance. 



# Data Model

Explanation of the data model: 

The data model that was created is based on a theoretical football club. The Teams entity is a representation of all of the teams within the club (professional league, 16U, 12U, etc). Within the team, there are several players which are represented with one to many relationships between the Teams and Players entities. Hence, there are several players that belong to a single team. These players also have many stats as a result of the games they participate in. For example, their overall rating, number of goals scored, number of pass attempts, their position rating and so on. Therefore, this is represented with a one to many relationship between the Players and Stats entity. Additionally, Teams also have many coaches but a coach may only instruct one team at a time. For that reason, a one to many relationship between the Teams and Coaches entity was created.  

There are also many matches that a team may play and matches may be played by many teams, which is why there is a many to many relationship between Teams and Matches. As a result we created an associative entity labeled Matchup. This entity stores information when two teams are playing each other within a game. For example, the table allows users to see what teams are playing and the number of goals scored by both the team and opponent. Subsequently, matches require tickets for individuals to attend. A one to many relationship was placed between Matches and Tickets due to the fact that a match has several tickets for individuals to attend. 

There are also many training schedules that a team may have so we established an entity called TrainingSchedules. This is a one to many relationship between Teams and TrainingSchedules. 

On the other end of our data model we have the relationships between the Team and its corresponding fans and sponsors. The first relationship is one between Teams and Fans. This is a many to many relationship due to the fact that teams can have many fans supporting them and fans can support more than one team at a time. As a result, an associative entity was created labeled Fanbase, which stores information regarding who the fan is and what teams they support. Secondly, the relationship between Teams and Sponsors was created as a many to many relationship. Teams can have many sponsors while sponsors can sponsor several teams.  Therefore, another associative entity was created which stores information regarding the team and sponsor which was given the title Funding. 

Lastly, there is a Club entity created that represents the club associated with the respective teams. This entity, Club, stores information about the club name, description, and specific ID. There are 3 relationships associated with the Club entity. First, we created a one to many relationship with the Facilities entity since clubs can have access to several facilities. Secondly, a one to many relationship was created with the Transactions entity. A club can have several transactions such as rent, utilities, supplies, etc. Finally, the relationship between Club and Teams was created as a one to many relationship. There is one club, Georgia United FC, that houses all of the teams associated with the Club. However, a team may only belong to one club, Georgia United FC. 

![Screen Shot 2023-11-01 at 2 20 27 PM](https://github.com/alvinvasanth/MIST4610-Group-Project-1/assets/92402657/97ea47e2-1371-41b3-b8f0-f35bf5aae9ba)

# Data Dictionary 
<img width="659" alt="Screenshot 2023-11-02 at 12 11 31 PM" src="https://github.com/alvinvasanth/MIST4610-Group-Project-1/assets/92402657/6a6202b8-6802-43f6-9a56-12f0bf1db024">

<img width="643" alt="Screenshot 2023-11-02 at 12 11 41 PM" src="https://github.com/alvinvasanth/MIST4610-Group-Project-1/assets/92402657/6c03e6b7-ab3a-4d64-8cac-a47492bb98cc">

<img width="649" alt="Screenshot 2023-11-02 at 12 11 57 PM" src="https://github.com/alvinvasanth/MIST4610-Group-Project-1/assets/92402657/38e0c95d-80c9-4d0c-a366-a08e65e8b629">

<img width="694" alt="Screenshot 2023-11-02 at 12 22 29 PM" src="https://github.com/alvinvasanth/MIST4610-Group-Project-1/assets/92402657/b5935132-5bd1-49e5-ab36-574fdc9fb80c">

<img width="658" alt="Screenshot 2023-11-02 at 12 27 14 PM" src="https://github.com/alvinvasanth/MIST4610-Group-Project-1/assets/92402657/e55c352d-ec2a-4a18-ba22-6f81ed3f35a6">

<img width="653" alt="Screenshot 2023-11-02 at 12 27 36 PM" src="https://github.com/alvinvasanth/MIST4610-Group-Project-1/assets/92402657/a5da40cd-fb61-4ddd-9cdb-dd4ca5a34827">

<img width="643" alt="Screenshot 2023-11-02 at 12 27 41 PM" src="https://github.com/alvinvasanth/MIST4610-Group-Project-1/assets/92402657/0262d146-ddda-4cdd-9da4-435f05755d84">

<img width="666" alt="Screenshot 2023-11-02 at 12 28 47 PM" src="https://github.com/alvinvasanth/MIST4610-Group-Project-1/assets/92402657/4255efb3-6e16-4935-a4ea-686a8d0f8bdb">

<img width="684" alt="Screenshot 2023-11-02 at 12 32 24 PM" src="https://github.com/alvinvasanth/MIST4610-Group-Project-1/assets/92402657/0b833c1f-4265-403d-9ca4-b73bec40b021">

<img width="595" alt="Screenshot 2023-11-02 at 12 34 03 PM" src="https://github.com/alvinvasanth/MIST4610-Group-Project-1/assets/92402657/a7958568-a11f-4a93-9a05-bcc102c590bd">

<img width="619" alt="Screenshot 2023-11-02 at 12 39 48 PM" src="https://github.com/alvinvasanth/MIST4610-Group-Project-1/assets/92402657/69588489-ecc0-4926-8461-cf9f5284605d">

<img width="619" alt="Screenshot 2023-11-02 at 12 40 48 PM" src="https://github.com/alvinvasanth/MIST4610-Group-Project-1/assets/92402657/267646a0-d2e3-41fe-a134-2fcfe3b5ac4d">

<img width="633" alt="Screenshot 2023-11-02 at 12 41 14 PM" src="https://github.com/alvinvasanth/MIST4610-Group-Project-1/assets/92402657/c3f1b1b3-c377-4001-bfb3-23406c915394">

<img width="615" alt="Screenshot 2023-11-02 at 12 41 30 PM" src="https://github.com/alvinvasanth/MIST4610-Group-Project-1/assets/92402657/e89f5ec2-612a-4463-b616-62c2da112c47">

<img width="744" alt="Tickets" src="https://github.com/alvinvasanth/MIST4610-Group-Project-1/assets/148080560/26d0f184-0beb-4472-a311-5c958692fc42">

# Queries Chart
<img width="747" alt="Queries Table" src="https://github.com/alvinvasanth/MIST4610-Group-Project-1/assets/148080560/9e6d5b94-9b8c-4ca0-8bd5-55d9f45b93aa">


# SQL Queries


**TP_Q1**: Write a query that lists all the players and their positons
<img width="1026" alt="Query 1" src="https://github.com/alvinvasanth/MIST4610-Group-Project-1/assets/148080560/25e4381e-8b63-4253-9b42-2298613e921c">
Explanation: Knowing the list of players and their positions can have tactical, strategic, and managerial reasons. This list can be of interest to stakeholders, coaches and talent scouts to fans. 
 

**TP_Q2**: Write a query that lists what fans have attended more than 50 matches. Order the number of matches attended from least to greatest.
<img width="1034" alt="Query 2" src="https://github.com/alvinvasanth/MIST4610-Group-Project-1/assets/148080560/d3508af6-9b87-499f-9f91-a9ad366d2a16">
Explanation: Marketing is essential to creating a strong fanbase. A manager might want to know how many fans have attended a certain amount of games to see loyalty. Having loyal fan feedback and input can help improve experiences, player performance, marketing data, and build a sense of community between the players and fans.


**TP_Q3**: Write a query that lists the total amount paid for each transaction type.
<img width="951" alt="Query 3" src="https://github.com/alvinvasanth/MIST4610-Group-Project-1/assets/148080560/df8fd427-2e77-4cd5-b579-8ff6084035e1">
Explanation: A manager would want to know the total amount paid since it’s essential for financial analysis and make informed decisions about where to allocate revenues and control costs if over budget  


**TP_Q4**: list out each matchup that resulted in a Georgia United FC victory
<img width="1003" alt="Query 4" src="https://github.com/alvinvasanth/MIST4610-Group-Project-1/assets/148080560/58112ad5-32e8-4b1b-810c-cfe25bdf27dc">
Explanation: Knowing the list of matchups that resulted in a Georgia United FC victory can be valuable reasons such as performance analysis where the coaches can identify strong strategies, team performance and player strength/weaknesses. A list can help coaches/managers go through each game to make future game plans for a victory.


**TP_Q5**: List the name of each coach, their specialty, and what team they belong to. Order the results in descending order for team name and coach speciality. 
<img width="960" alt="Query 5" src="https://github.com/alvinvasanth/MIST4610-Group-Project-1/assets/148080560/fa3a8106-be54-407a-bf5e-8d9a223bf576">
Explanation: A club manager would want to know the specific details of all the coaches that they employ. It is essential to keep track of coach details such as their speciality and the team they are associated with to perform thorough performance evaluations and track their success. 


**TP_Q6**: List the sponsor name and contact information for those sponsors whose payment is greater than the average payment
<img width="1076" alt="Query 6" src="https://github.com/alvinvasanth/MIST4610-Group-Project-1/assets/148080560/5b635666-56f1-4ed7-a2d2-e958d7ab6fe8">
Explanation: Keeping track of sponsors is a key component of a club because they provide a significant amount of funding to keep the club running. Monitoring sponsors ensures that the manager is aware of the financial commitments and support provided by sponsors. Sponsors who contribute amounts greater than the average payment should be noted as higher level sponsors and recognized by the manager. 


**TP_Q7**: List the different teams, their coaches who specialize in defense, and the players whose position is defense
<img width="1038" alt="Query 7" src="https://github.com/alvinvasanth/MIST4610-Group-Project-1/assets/148080560/3187306b-572f-4f0a-b2fa-f547b12d8e5d">
Explanation: Defense is an important aspect of any sport. This query allows for managers and coaches to have accessible data for the players who play defense and the coaches that specialize in defense. Having this information can be useful when managers are looking at their roster assessing the makeup of each team.


**TP_Q8**:Write a query that lists each player and their skill level, determined by their overall rating. Order the results by 'talent level.'
<img width="1086" alt="Query 8" src="https://github.com/alvinvasanth/MIST4610-Group-Project-1/assets/148080560/494d554e-3487-4d71-8eb4-40420950bd3c">
Explanation: Player performance is critical in a team's success. This query allows managers and coaches to see how players are performing based on their overall rating. Coaches and managers can see what players need more practice and can use that to better equip their teams for success. 


**TP_Q9**: Write a query to list out players for ____ (specific team) who make more than ____ (certain amount so we can use the having clause). Order the results in descending order.
<img width="1088" alt="Query 9" src="https://github.com/alvinvasanth/MIST4610-Group-Project-1/assets/148080560/4de5730a-2811-44ba-b6e3-fc0da93e61f0">
Explanation: Salary is a huge component of teams, however teams only have so much money they can hand out. Therefore, this query allows managers to evaluate how their budget is being allocated. It’s important to note that managers can input any team name and any salary depending on their needs. We used the team “Lions” and the salary “$200,000” as an example.


**TP_Q10**: Write a query to list out average price of tickets that are ____ (certain ticket type) where the match opponent was ______ (certain match opponent)
<img width="1103" alt="Query 10" src="https://github.com/alvinvasanth/MIST4610-Group-Project-1/assets/148080560/4904885a-daa6-49b4-b4bc-896be0aeef13">
Explanation: This query allows the club executives and high level managers to see which type of seats are being sold out in accordance with which match opponents are playing in order to gain a better understanding of where people desire to watch their favorite teams play. This helps them not only to structure their stadium seats to gain more viewership profit, but also see how the pricing of tickets is being affected by which teams play. With this information, they can see which teams playing against each other elicit higher ticket prices, and create matchups for better profit. Again, it is important to note that managers can input any type of seat and opponent they choose, adding flexibility for the managers. We chose Box seats and Franecki-O’Reilly for purposes of output.



# Database information:
Name of the database: ns_29704_1

Additional information: Each query listed above is marked in the database using stored procedures which can be called using the following format: CALL TP_Q1();
