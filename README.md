Download Link: https://assignmentchef.com/product/solved-cse3055-homework-3
<br>
Consider the <em>Turkish Super League</em> database accompanied with this homework.




<strong><em>Player</em></strong><em> (<u>PlayerID</u></em><em>: int</em><em>,   FirstName</em><em>: nvarchar(25)</em><em>,   LastName</em><em>: nvarchar(25)</em><em>,   Nationality</em><em>: varchar(25)</em><em>,   Birthdate</em><em>: </em>

<em>smalldatetime</em><em>,   Age</em><em>: smallint</em><em>,   Position</em><em>: varchar(25)</em><em>) </em>

<strong><em>Team</em></strong><em> (<u>TeamID</u></em><em>: int</em><em>,   Name</em><em>: nvarchar(50)</em><em>,   City</em><em>: nvarchar(25)</em><em>) </em>

<strong><em>PlayerTeam</em></strong><em> (<u>PlayerID</u></em><em>: int</em><em>,   <u>TeamID</u></em><em>: int</em><em>,   <u>Season</u></em><em>: varchar(5)</em><em>) </em>

<strong><em>Match</em></strong><em> (<u>MatchID</u></em><em>: int</em><em>,   HomeTeamID</em><em>: int</em><em>,   VisitingTeamID</em><em>: int</em><em>,   DateOfMatch</em><em>: smalldatetime</em><em>,   Week</em><em>: tinyint</em><em>) </em>

<strong><em>Goals</em></strong><em> (<u>MatchID</u></em><em>: int</em><em>,   <u>PlayerID</u></em><em>: int</em><em>,   IsOwnGoal</em><em>: bit</em><em>,   <u>Minute</u></em><em>: tinyint</em><em>) </em>




<u>Notes</u>:

<ul>

 <li>Table <em>Match</em> stores data only for season 2013-2014.</li>

 <li>Table <em>Goals</em> stores data only for season 2013-2014.</li>

</ul>
















<ul>

 <li>Using the backup file <em>bak</em> accompanied with this homework, restore the database <em>TurkishSuperLeague</em>. Write the following SQL queries, IN A SINGLE STATEMENT, using this database. For each of the following query; save your SQL statements in a text file and take a screenshot of both your SQL query and output of the query on MS SQL Server.</li>

</ul>




<ul>

 <li>Update the field <em>Age</em> for all players.</li>

</ul>




<ul>

 <li>List the “younger” players whose first name does not contain “nec” and play in “Beşiktaş”. “Younger” players are the ones whose ages are less than the average age of all players. Retrieve PlayerID, FirstName + ” “ + LastName.</li>

</ul>




<ul>

 <li>Update all <em>City</em> values of the table <em>Team</em> as: “City” + “ #p” + “Number of players” +” #g” + “Number of goals forward” (e.g. “İstanbul #p25 #g74”). Do not forget to consider own goals in your calculations.</li>

</ul>




<ul>

 <li>List the top 10 top scorers. Retrieve playerID, first name, last name, number of goals scored, number of matches that player did not score a goal, average number of goals per scored matches.</li>

</ul>




<ul>

 <li>Implement a stored procedure <em>sp_GetStandingsUpToDate (aDate)</em> such that <em>exec sp_GetStandingsUpToDate (aDate)</em> computes and shows the standings table, same as in the</li>

</ul>

following figure, up to the date <em>aDate</em> (inclusive).

Calling with any invalid date causes an error with a message “Invalid date!” All transactions that have been done will be rolled back and stop doing further operations.











