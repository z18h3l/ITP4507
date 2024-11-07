java cP a g e | 1
HONG KONG INSTITUTE OF VOCATIONAL EDUCATION
DEPARTMENT OF INFORMATION TECHNOLOGY
HIGHER DIPLOMA IN SOFTWARE ENGINEERING (IT114105)
Module Name: Contemporary Topics in Software Engineering
Module Code: ITP4507
Assignment Number: One
Hand-in: Friday 15 November, 2024 (On or before 4:30 PM to Moodle)
Weighting of This Assignment: 66.67% of the End of Module Assessment
This assignment must be done by individual only. Plagiarism will be treated seriously. 
Any assignments that are found involved wholly or partly in plagiarism 
(no matter the assignments are from the original authors or from the plagiarists) 
will score Zero mark. Late submission will NOT be accepted.
Task Specification
Snow Storm Company develops an RPG game "Fantastic World (FW)" on the PC. The major characters in 
this game are known as HERO and they have various kinds of characteristic. For example, Warrior focus on 
defence and Warlock target on magic damage. Each player in this game can play more than one hero.
Currently, this game only has Warrior and Warlock. In the coming future, this game will be extended to 
support more kinds of hero such as healer. The following is the simplified class diagram of existing data 
maintained by FW.
P a g e | 2
As a system analyst of the Company, you are required to design and develop FW. You can get the source 
codes of above classes from Moodle.
FW should provide the following functions:
1. Create a Player.
2. Add a hero (Warrior or Warlock) to the current player.
3. Remove a hero from the current player.
4. Select a player by using a player ID.
5. Call a hero's skill by a hero ID.
6. Show the detail information of current player.
7. Change the player's name of the current player.
8. Show all players.
9. Set current player.
10. Undo last command.
11. Redo the last undone command.
12. Show undo/redo list.
13. Exit System.
Your system design should conform to the Open Closed Principle so that your design should easily be 
extended to support new heroes (for examples, healers, rangers etc..).
You MUST apply the following design patterns for your new system
 Command pattern to provide the “create player”, “set current player”, “add hero”, 
“call hero skill”, “delete hero”, “show current player”, “display all players”, “change player’s 
name”. “undo”, “redo” and “show undo/redo list” functions 
 Factory pattern or Abstract Factory Pattern to create different kinds of Command objects and 
different kinds of Player/Hero objects (e.g., Warrior object, Warlock object, Player object, etc.)
 Memento pattern to provide “Undo” and “Redo” functions on the “call hero skill” and “change 
player’s name” functions.
Assignment Report 
In addition to the system development, you are required to write up a Short Report covers the following 
sections:
 1. Assumptions regarding the problem context
 2. Application design with class diagram
 3. Discussion and explanation on each of the design patterns applied to the application
 4. Test Plan and Test Cases
 5. Well documented Source Code
P a g e | 3
Mark Allocation
Your assignment work will be marked according to the following criteria.
Work Mark Allocated
System Coding and Implementation
a) Implementation of the system and coding style
(Hard-coded output will result in zero mark.)
30%
b) Correctness of system functions *
(Hard-coded output will result in zero mark.)
15%
c) Test Plan and Test Cases
(Will be used in testing your own application.) 
10%
System Analysis and Design, and Discussion
d) Design of your system and correct use of design patterns 20%
e) Application design with class diagram 10%
f) Discussion and explanation on each of the design patterns 
applied to the application
15%
Total 100%
Note: * Please note that your source code will be recompiled and tested for the correctness of the system 
functions. Your implementation is required to support the 'Copy and Paste' method for testing which is 
described in page 16.
Submission of Assignment Work
1. The front page of your submission should include the programme title(code), module title(code), and 
student number and student name.
2. Submit your Java source code and your report to https://moodle.vtc.edu.hk .
 Well documented Source Code of your program.
 Report for analysis, design, discussion, user guide, test plan and test cases of your following work.
A. The assumption made during analysis and design of the application
B. System design on your application with class diagram 
C. Discussion on the design patterns that applied on your program
D. Test Plan with Test Cases (Design your own test plan and corresponding test cases for each 
function. For each test case, you should provide a SCREEN CAPTURE for test result).
3. Submit according to the guideline on the top part of cover page. Late submission will NOT be 
accepted.
P a g e | 4
Extra Reference: Sample Test
Testing Method
This sample run is served for reference only. You are free to design your own user interface. But to make 
the testing environment simple and to apply the "Copy and Paste" testing method described on page 16
easily, you are advised to accept user input at the command prompt as shown in the sample run below.
Sample Run of assignment
You may follow the design of user interface shown in this sample run in DOS command prompt. 
For following examples, character(s) with underline is user's input.
1. Create player
Fantastic World (FW)
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-c
Player ID:- P001
Player Name:- Thomas Yiu
Player Thomas Yiu is created.
Current player is changed to P001.
2. Add heroes to the player
Fantastic World (FW)
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system
The current player is P001 Thomas Yiu.
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-a
Please input hero information (id, name):- H001, peter pang
Hero Type (1 = Warrior | 2 = Warlock ):- 1
Hero is added.
Fantastic World (FW)
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system
The current player is P001 Thomas Yiu.
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-a
P a g e | 5
Please input hero information (id, name):- H002, john wick
Hero Type (1 = Warrior | 2 = Warlock ):- 2
Hero is added.
3. Show the current player
Fantastic World (FW)
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system
The current player is P001 Thomas Yiu.
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-s
Player Thomas Yiu (P001)
Heroes:
H001, peter pang, Warrior, Hp: 500, Damage: 0, Defence Point: 500
H002, john wick, Warlock, Hp: 100, Damage: 200, Mp: 500
4. Create another player and display all players
Fantastic World (FW)
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system
The current player is P001 Thomas Yiu.
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-c
Player ID:- P002
Player Name:- Stan Lee
Player Stan Lee is created.
Current player is changed to P002.
Fantastic World (FW)
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system
The current player is P002 Stan Lee.
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-p
Player Thomas Yiu (P001)
Player Stan Lee (P002)
P a g e | 6
5. Add heroes to the player P002
Fantastic World (FW)
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system
The current player is P002 Stan Lee.
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-a
Please input hero information (id, name):- H003, scarlet witch
Hero Type (1 = Warrior | 2 = Warlock ):- 2
Hero is added.
Fantastic World (FW)
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system
The current player is P002 Stan Lee
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-a
Please input hero information (id, name):- H004, tony stark
Hero Type (1 = Warrior | 2 = Warlock ):- 1
Hero is added.
6. Show the current player
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system
The current player is P002 Stan Lee.
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-s
Player Stan Lee (P002)
Heroes:
H003, scarlet witch, Warlock, Hp: 100, Damage: 200, Mp: 500
H004, tony stark, Warrior, Hp: 500, Damage: 0, Defence Point: 500
7. Set the current player by Player ID
Fantastic World (FW)
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system
The current player is P002 Stan Lee.
P a g e | 7
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-g
Please input player ID:- P001
Changed current player to P001. 
10. Call hero skill
Fantastic World (FW)
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system
The current player is P001 Thomas Yiu.
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-m
Please input hero ID:- H001
H001 peter pang’s attributes are changed to:
H001, peter pang, Hp: 500, Damage: 250, Defence Point: 400
Fantastic World (FW)
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system
The current player is P001 Thomas Yiu.
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-s
Player Thomas Yiu (P001)
Heroes:
H001, peter pang, Warrior, Hp: 500, Damage: 250, Defence Point: 400
H002, john wick, Warlock, Hp: 100, Damage: 200, Mp: 500
11. Delete hero
Fantastic World (FW)
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system
The current player is P001 Thomas Yiu.
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-d
Please input hero ID:- H002
H002 john wick is deleted.
P a g e | 8
12. Change the name of the current player
Fantastic World (FW)
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system
The current player is P001 Thomas Yiu.
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-t
Please input new name of the current player:- Russo Brothers
Player’s name is updated.
Fantastic World (FW)
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system
The current player is P001 Russo Brothers.
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-s
Player Russo Brothers (P001)
Heroes:
H001, peter pang, Warrior, Hp: 500, Damage: 250, Defence Point: 400
13. Show undo/redo list
Fantastic World (FW)
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system
The current player is P001 Russo Brothers.
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-l
Undo List
Change player’s name, P001, Russo Brothers
Delete hero, H002
Call hero skill, H001, peter pang, Warrior, Hp: 500, Damage: 250, Defence 
Point: 400
Add hero, H004, tony stark, Warrior
Add hero, H003, scarlet witch, Warlock
Create player, P002, Stan Lee
Add hero, H002, john wick, Warlock
Add hero, H001, peter pang, Warrior
P a g e | 9
Create player, P001, Thomas Yiu
-- End of undo list --
Redo List
-- End of redo list –
14. UNDO actions in UNDO list
Fantastic World (FW)
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system
The current player is P001 Russo Brothers.
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-u
Command (Change player’s name, P001, Russo Brothers) is undone.
Fantastic World (FW)
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system
The current player is P001 Thomas Yiu.
Fantastic World (FW)
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system
The current player is P001 Thomas Yiu.
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-u
Command (Delete hero, H002) is undone.
Fantastic World (FW)
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system
The current player is P001 Thomas Yiu.
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-u
Command (Call hero skill, H001, peter pang, Warrior, Hp: 500, Damage: 250, 
Defence Point: 400) is undone.
P a g e | 10
Fantastic World (FW)
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system
The current player is P001 Thomas Yiu.
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-s
Player Thomas Yiu (P0代 写ITP4507、java
代做程序编程语言01)
Heroes:
H001, peter pang, Warrior, Hp: 500, Damage: 0, Defence Point: 500
H002, john wick, Warlock, Hp: 100, Damage: 200, Mp: 500
Fantastic World (FW)
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system
The current player is P001 Thomas Yiu.
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-u
Command (Add hero, H004, tony stark, Warrior) is undone.
Fantastic World (FW)
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system
The current player is P001 Thomas Yiu.
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-u
Command (Add hero, H003, scarlet witch, Warlock) is undone.
Fantastic World (FW)
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system
The current player is P001 Thomas Yiu.
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-g
Please input player ID:- P002
Changed current player to P002.
P a g e | 11
Fantastic World (FW)
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system
The current player is P002 Stan Lee.
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-s
Player Stan Lee (P002)
Heroes:
Fantastic World (FW)
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system
The current player is P002 Stan Lee.
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-u
Command (Create player, P002, Stan Lee) is undone.
Current player is changed to P001.
Fantastic World (FW)
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system
The current player is P001 Thomas Yiu.
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-g
Please input player ID:- P002
Player P002 is not found!!
Fantastic World (FW)
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system
The current player is P001 Thomas Yiu.
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-l
Undo List
Add hero, H002, john wick, Warlock
Add hero, H001, peter pang, Warrior
Create player, P001, Thomas Yiu
-- End of undo list --
P a g e | 12
Redo List
Create player, P002, Stan Lee
Add hero, H003, scarlet witch, Warlock
Add hero, H004, tony stark, Warrior
Call hero skill, H001, peter pang, Warrior, Hp: 1000, Damage: 500, Defence 
Point: 400
Delete hero, H002
Change player’s name, P001, Russo Brothers
-- End of redo list –
15. REDO actions in REDO list
Fantastic World (FW)
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system
The current player is P001 Thomas Yiu.
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-r
Command (Create player, P002, Stan Lee) is redone. 
The current player is changed to P002.
Fantastic World (FW)
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system
The current player is P002 Stan Lee.
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-r
Command (Add hero, H003, scarlet witch, Warlock) is redone. 
Fantastic World (FW)
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system
The current player is P002 Stan Lee.
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-r
Command (Add hero, H004, tony stark, Warrior) is redone.
Fantastic World (FW)
P a g e | 13
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system
The current player is P002 Stan Lee.
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-s
Player Stan Lee (P002)
Heroes:
H003, scarlet witch, Warlock, Hp: 100, Damage: 200, Mp: 500
H004, tony stark, Warrior, Hp: 500, Damage: 0, Defence Point: 500
Fantastic World (FW)
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system
The current player is P002 Stan Lee.
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-r
Command (Call hero skill, H001, peter pang, Warrior, Hp: 500, Damage: 250, 
Defence Point: 400) is redone. 
Fantastic World (FW)
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system
The current player is P001 Thomas Yiu.
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-g
Please input player ID:- P001
Changed current player to P001.
Fantastic World (FW)
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s
name, u = undo, r = redo, l = list undo/redo, x = exit system
The current player is P001 Russo Brothers.
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-s
Player Russo Brothers (P001)
Heroes:
H001, peter pang, Warrior, Hp: 500, Damage: 250, Defence Point: 400
H002, john wick, Warlock, Hp: 100, Damage: 200, Mp: 500
P a g e | 14
Fantastic World (FW)
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system
The current player is P002 Stan Lee.
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-l
Undo List
Call hero skill, H001, peter pang, Warrior, Hp: 1000, Damage: 500, Defence 
Point: 400
Add hero, H004, tony stark, Warrior 
Add hero, H003, scarlet witch, Warlock 
Create player, P002, Stan Lee
Add hero, H002, john wick, Warlock
Add hero, H001, peter pang, Warrior
Create player, P001, Thomas Yiu
-- End of undo list --
Redo List
Delete hero, H002
Change player’s name, P001, Russo Brothers
-- End of redo list –
- END OF SAMPLE TEST –
P a g e | 15
You can ease the testing by using the 'Copy and Paste' method rather than inputting data manually. Prepare a text file, 
which includes all user inputs in a test run. By using the 'Copy and Paste' method, you can automatically input in the 
command prompt window and then get the result automatically (without the input data echoed). The following is an 
example of the text file for user inputs. 
Sample User Inputs for a Test Run
c
P001
Thomas Yiu
a
H001, peter pang
1
a
H002, john wick
2
s
c
P002
Stan Lee
p
a
H003, scarlet witch
a
H004, tony stark
1
s
g
P001
m
H001
s
d
H002
t
Russo Brothers
s
l
u
u
u
s
u
u
g
P002
s
u
g
P002
l
r
r
r
s
P a g e | 16
r
g
P001
s
l
x
Expected Output of the Test Run
Fantastic World (FW) 
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system 
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :Player 
ID:- Player Name:-
Player Thomas Yiu is created. 
Current player is changed to P001. 
Fantastic World (FW) 
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system 
The current player is P001 Thomas Yiu. 
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-
Please input hero information (id, name):- Hero Type (1 = Warrior | 2 = Warlock 
):- 
Hero is added. 
Fantastic World (FW) 
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system 
The current player is P001 Thomas Yiu. 
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-Please 
input hero information (id, name):- Hero Type (1 = Warrior | 2 = Warlock ):-
Hero is added. 
Fantastic World (FW) 
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system 
The current player is P001 Thomas Yiu. 
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-Player 
Thomas Yiu (P001) 
Heroes: 
H001, peter pang, Warrior, Hp: 500, Damage: 0, Defence Point: 500 
H002, john wick, Warlock, Hp: 100, Damage: 200, Mp: 500 
Fantastic World (FW) 
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system 
The current player is P001 Thomas Yiu. 
P a g e | 17
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-Player 
ID:- Player Name:- 
Player Stan Lee is created. 
Current player is changed to P002. 
Fantastic World (FW) 
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system
The current player is P002 Stan Lee. 
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-Player 
Thomas Yiu (P001) 
Player Stan Lee (P002) 
Fantastic World (FW) 
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system 
The current player is P002 Stan Lee. 
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-Please 
input hero information (id, name):- H003, scarlet witch 
Hero Type (1 = Warrior | 2 = Warlock ):- 2 
Hero is added. 
Fantastic World (FW) 
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system 
The current player is P002 Silent Hill. 
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-
aPlease input hero information (id, name):- H004, tony stark 
Hero Type (1 = Warrior | 2 = Warlock ):- 1 
Hero is added. 
Fantastic World (FW) 
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system 
The current player is P002 Stan Lee. 
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-Player 
Stan Lee (P002) 
Heroes: 
H003, scarlet witch, Warlock, Hp: 100, Damage: 200, Mp: 500 
H004, tony stark, Warrior, Hp: 500, Damage: 0, Defence Point: 500 
Fantastic World (FW) 
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system 
The current player is P002 Stan Lee.
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-Please 
input player ID:- P001 
Changed current player to P001. 
P a g e | 18
Fantastic World (FW) 
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system 
The current player is P001 Thomas Yiu. 
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-Please 
input hero ID:- H001 
H001 peter pang’s attributes are changed to: 
H001, peter pang, Hp: 500, Damage: 250, Defence Point: 400 
Fantastic World (FW) 
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system 
The current player is P001 Thomas Yiu. 
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-Player 
Thomas Yiu (P001) 
Heroes: 
H001, peter pang, Warrior, Hp: 500, Damage: 250, Defence Point: 400 
H002, john wick, Warlock, Hp: 100, Damage: 200, Mp: 500 
11. Delete hero 
Fantastic World (FW) 
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system 
The current player is P001 Thomas Yiu. 
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-Please 
input hero ID:- H002 
H002 john wick is deleted. 
12. Change the name of the current player 
Fantastic World (FW) 
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system 
The current player is P001 Thomas Yiu. 
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-Please 
input new name of the current player:- Russo Brothers
Player’s name is updated. 
Fantastic World (FW) 
c = create player, g = set current player, a = add hero, m = call hero skill, d 
= delete hero, s = show player, p = display all players, t = change player’s 
name, u = undo, r = redo, l = list undo/redo, x = exit system 
The current player is P001 Russo Brothers. 
Please enter command [ c | g | a | m | d | s | p | t | u | r | l | x ] :-Player 
Russo Brothers (P001) 
Heroes: 
H001, peter pang, Warrior, Hp: 500, Damage: 250, Defence Point: 400 
Fantastic World (FW) 
c = create player, g = set curren         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
