Download Link: https://assignmentchef.com/product/solved-csci213-assignment-2-war-of-greek-gods-wgg-game
<br>
<ol>

 <li><strong> Overview </strong></li>

</ol>

This assignment aims to establish a basic familiarity with the JDK development system and its associated on-line Java API class documentation. Students should apply the appropriate fundamental programming concepts (such as variables, constants, arrays, strings, methods, selection and repetition constructs etc.) and make use of appropriate Java API classes (such as Scanner, PrintWriter, String etc.) that they have learnt to solve the given problem.




<ol start="2">

 <li><strong> Objectives </strong></li>

</ol>

On completion of this assignment a student should be able to write simple Java application

that:

<ul>

 <li>Makes use of selection and repetition constructs to achieve desired outcomes</li>

 <li>Stores data to and reads data from arrays</li>

 <li>Generates output to and reads input from the console window</li>

 <li>Reads data from and writes data to text file</li>

 <li>Manipulates string using Java API “String” class</li>

 <li>handles basic errors</li>

 <li>Applies object-oriented concepts</li>

</ul>




<ol start="3">

 <li><strong> Scope </strong></li>

</ol>

This assignment is based on individual effort. You are required to design, develop and test a one player Java game application named “War of Greek Gods”.

Besides providing the required functionalities, your program should incorporate appropriate error handling. Comments are also to be inserted to improve program clarity. Before you start coding your program, you are strongly advised to carry out proper problem analysis and program design.  You are required to use JDK 1.5 developer version or later.




<ol start="4">

 <li><strong> Requirements</strong></li>

</ol>

<strong> </strong>

<strong>4.1 Background</strong>

WGG is a turned based card game that can be played with two or more players.

One of the players will be the dealer.

In this assignment, there is only 1 dealer, that is the Java program, and a single human player.




The game uses a deck of game cards with the fields: Name, Description, Earth Element Power, Water Element Power, Air Element Power and Fire Element Power.







Since the dealer is “a type” of player, references to “player” may be to the dealer or the single human player.




<u>Game Procedure</u>

<u> </u>

When the game starts, the deck of game cards is loaded from the file (GameCards.dat). For example

<table>

 <tbody>

  <tr>

   <td width="561">Zeus|God of the Sky|30|15|40|15Poseidon|God of the Sea|20|50|15|15Demeter|Goddess of Agriculture|55|25|15|5Ares|God of War|20|10|10|60</td>

  </tr>

 </tbody>

</table>

There should be a minimum of 6 game cards for this game. You can make up the rest of the game cards information and add in more cards. (http://rickriordan.com/extra/meet-the-greek-gods/)




The dealer and player will be assigned randomly with 3 game cards each.

In this game there are four element pillars: Earth, Water, Air and Fire.

Each war will be hosted on one of the pillars.




The game starts with the Human Player.

The player chooses which pillar to host the war.

Then the dealer and player will each choose a game card for the war.




For example

Player chooses Air pillar

Player sent Zeus to the Air pillar

Player: Zeus Air element power – 40

Dealer sent Poseidon to the Air pillar.

Dealer: Pose AIR element power – 15




Since the war is hosted on the Air pillar, the current power for Zeus is 40 and Poseidon is 15.

For a round of war, the player and dealer will each roll a dice.

If dealer wins, the dice number different multiply by 10 Air power points will be transferred from the player to dealer




For example:

Player rolls dice: 2

Dealer rolls dice: 4

Dealer wins

20 Air element powers points transferred from Zeus to Poseidon

Player: Zeus Air element power – 20

Dealer: Poseidon Air element power – 35




The current round ends and the next round starts with the dealer.




A game card with 0 power for the element cannot be sent to the pillar for that element.




In a round, if the points to be transferred is more than the balance points. Then only the balance points will be transferred.




The game ends when the element power for a game card becomes zero for that round.




The new power points for all the element for each game card will be updated in GameCards.dat when the player choose to exit the game.













<strong>4.2 Minimum required </strong><strong>Functionalities</strong>




Develop a Java program for the <u>two-players</u> WGG game described above.




Sample run for the WGG game. (The texts in <strong>bold</strong> are data input by the player)

<table>

 <tbody>

  <tr>

   <td width="686">============================War of Greek Gods============================Dealer shuffle game cardsDealer distribute game cards============================Round 1 : Player’s turn============================Player game cardsZeus – God of the Sky E: 30 W:15 A:40 F:10 T:95Poseidon – God of the Sea E:20 W:50 A:15 F:20 T:105Demeter – Goddess of Agriculture E:55 W:25 A:15 F:15 T:110============================Dealer game cardsAres – God of War E:20 W:10 A:10 F:50 T:90Artemis – Goddess of the Moon E:40 W:20 A:55 F:5 T:120Hermes – God of the Roadways E:40 W:10 A:10 F:20 T:80============================Player choose a pillar for war (E/W/A/F) :<strong> E</strong>Player chooses Earth pillarPlayer game cards1 – Zeus – God of the Sky E: 30 W:15 A:40 F:10 T:952 – Poseidon – God of the Sea E:20 W:50 A:15 F:20 T:1053 – Demeter – Goddess of Agriculture E:55 W:25 A:15 F:15 T:110Choose a game card (1,2,3): <strong>3</strong>Player sent Demeter to the Earth PillarPlayer: Demeter Earth element power – 55============================Dealer sent Artemis to the Earth pillar.Dealer: Artemis Earth element power – 40============================Player rolls dice: 2Dealer rolls dice: 4Dealer wins============================20 Earth element powers points transferred from Demeter to ArtemisPlayer: Demeter Earth element power – 35Dealer: Artemis Earth element power – 60Round 1 Ends============================Round 2 : Dealer’s turn============================Player game cardsZeus – God of the Sky E: 30 W:15 A:40 F:10 T:95Poseidon – God of the Sea E:20 W:50 A:15 F:20 T:105Demeter – Goddess of Agriculture E:35 W:25 A:15 F:15 T:110============================Dealer game cardsAres – God of War E:20 W:10 A:10 F:50 T:90Artemis – Goddess of the Moon E:60 W:20 A:55 F:5 T:120Hermes – God of the Roadways E:40 W:10 A:10 F:20 T:80============================Dealer chooses Fire pillarDealer sent Ares to the Fire pillar.Dealer: Ares Fire element power – 50============================Player game cards1 – Zeus – God of the Sky E: 30 W:15 A:40 F:10 T:952 – Poseidon – God of the Sea E:20 W:50 A:15 F:20 T:1053 – Demeter – Goddess of Agriculture E:35 W:25 A:15 F:15 T:110Choose a game card (1,2,3): <strong>2</strong>Player sent Poseidon to the Fire PillarPlayer: Poseidon Fire element power – 20============================Player rolls dice: 2Dealer rolls dice: 5Dealer wins============================20 Fire element powers points transferred from Poseidon to AresPlayer: Poseidon Fire element power – 0Dealer: Ares Fire element power – 70============================Dealer WinsGame Ends============================Next game (Y/N)? <strong>Y</strong>……………….</td>

  </tr>

 </tbody>

</table>




And the game continues until the player exits the game.




<strong>Updates of game card information score</strong>




After each game, the program should update the game card information back to GameCards.dat

<strong> </strong>

<strong>Error Handling</strong>

<strong> </strong>

Your program should be able to handle error situations like where a player a wrong choice. You should look out for other possible exceptions and handle them too.





