# MIST4610-Group-Project-1
Team Name: 29704 1

# Team Members
1. Jillian Bolgla [@jillianbolgla](https://github.com/jillianbolgla)
2. Conor Dillon [@cjdillon11](https://github.com/cjdillon11)
3. Brandon Hopper [@bhop19](https://github.com/bhop19)
4. Neha Panchal [@nehapanchal2001](https://github.com/nehapanchal2001)
5. Shrija Ramachandran Ganesh Mohan - [@shrija-27](https://github.com/shrija-27)
6. Alvin Vasanthakumar - [@alvinvasanth](https://github.com/alvinvasanth)

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

<img width="641" alt="Screenshot 2023-11-02 at 5 44 17 PM" src="https://github.com/shrija-27/MIST-4610-Project-1/assets/92402657/bbd056af-f8d9-49cf-be7b-3dd4ef7f6adf">

# SQL Queries

**TP_Q1**: Lists all the players whose position are strikers and defense
<img width="1110" alt="Screenshot 2023-11-02 at 5 38 25 PM" src="https://github.com/shrija-27/MIST-4610-Project-1/assets/92402657/0b62f319-b255-4667-8196-070c5fd653b8">
Explanation: Knowing the list of players who can perform as both strikers and defenders can have tactical, strategic, and managerial reasons. This list can be of interest to stakeholders, coaches and talent scouts to fans. 

**TP_Q2**: Write a query that lists what fans have attended more than 50 matches. Order the number of matches attended from least to greatest.
<img width="1056" alt="Screenshot 2023-11-02 at 12 51 24 PM" src="https://github.com/alvinvasanth/MIST4610-Group-Project-1/assets/92402657/7e6343f6-7c1e-4c1d-aa9a-2e31d923d00c">
Explanation: Marketing is essential to creating a strong fanbase. A manager might want to know how many fans have attended a certain amount of games to see loyalty. Having loyal fan feedback and input can help improve experiences, player performance, marketing data, and build a sense of community between the players and fans.

**TP_Q3**: Write a query that lists the total amount paid for each transaction type.
<img width="1060" alt="Screenshot 2023-11-02 at 1 15 09 PM" src="https://github.com/alvinvasanth/MIST4610-Group-Project-1/assets/92402657/6adb09cc-6ac5-4ea4-9889-b7675dccf8bc">
Explanation: A manager would want to know the total amount paid since it’s essential for financial analysis and make informed decisions about where to allocate revenues and control costs if over budget  

**TP_Q4**: list out each matchup that resulted in a Georgia United FC victory
<img width="1058" alt="Screenshot 2023-11-02 at 1 16 42 PM" src="https://github.com/alvinvasanth/MIST4610-Group-Project-1/assets/92402657/d4beef1c-b32b-4068-8311-d18d97a2b67c">
Explanation: Knowing the list of matchups that resulted in a Georgia United FC victory can be valuable reasons such as performance analysis where the coaches can identify strong strategies, team performance and player strength/weaknesses. A list can help coaches/managers go through each game to make future game plans for a victory.

**TP_Q5**: List the name of each coach, their specialty, and what team they belong to.
<img width="1159" alt="Screenshot 2023-11-02 at 1 17 41 PM" src="https://github.com/alvinvasanth/MIST4610-Group-Project-1/assets/92402657/d18edd81-21d4-4da3-8809-5655f88b7e90">
Explanation: A club manager would want to know the specific details of all the coaches that they employ. It is essential to keep track of coach details such as their speciality and the team they are associated with to perform thorough performance evaluations and track their success. 

**TP_Q6**: List the sponsor name and contact information for those sponsors whose payment is greater than the average payment
<img width="1167" alt="Screenshot 2023-11-02 at 1 18 37 PM" src="https://github.com/alvinvasanth/MIST4610-Group-Project-1/assets/92402657/e0a96676-dee9-4201-ab90-f624f1b4ff16">
Explanation: Keeping track of sponsors is a key component of a club because they provide a significant amount of funding to keep the club running. Monitoring sponsors ensures that the manager is aware of the financial commitments and support provided by sponsors. Sponsors who contribute amounts greater than the average payment should be noted as higher level sponsors and recognized by the manager. 


# Database information:
Name of the database: ns_29704_1

Additional information: Each query listed above is marked in the database using stored procedures which can be called using the following format: CALL TP_Q1();
