# ShapesTopDownShooter
**Game Description**

Shapes RPG is a 2D isometric shooter that involves drawing shapes on screen 
to attack enemies. The game follows the main character, depicted as a square, on their 
journey to free their world of the dictators that currently rule. The game features a semiopen world map as well as unique world hazards and enemies. 
**Gameplay**

Movement: The character is moved using WASD keys or arrow keys.
Attacking: The user attacks by trapping enemies with shapes drawn by the player on 
screen.

• The player has a limit to the amount of line they can draw an attack with 
which increases with the number of bosses the player has defeated.
• The player has a limit to the length of the line that they can draw except 
for the final connecting line.
• The first and last line must connect to trigger an attack. 
• The player can cancel an attack at any point in the drawing by right 
clicking anywhere on screen. 
• The player can control click to bring back the previously drawn attack and 
place it for a quick attack.
Map: The game takes place on a single open map that is split into 3 zones with each 
zone having a unique theme. Each Zone also contains specific hazards according to the 
zone.

Enemies: There are 4 base enemies that exist in the game, and they are the triangle, 
pill, capsule, and circle. Each enemy has a unique style of attacking that adds extra 
challenge for the players.

Bosses: There are 3 bosses in the game, the bosses take on the models of the ordinary 
enemies but are much larger. The bosses’ attack behavior is also different from their
base models. 

**Implementation**

Shapes RPG was created using the unity game engine with extra packages 
including Input System and Cinemachine. The character sprites were created by Arthur 
Choy and many of the UI, maps and hazard assets were free assets of the unity asset 
store. Many of the tools used were already part of the standard unit package.

**Scripts**

Scripts can be broken down into 3 categories, these are player, enemies, UI.

Player Scripts: The player scripts involve player movement, player attack, and player 
attributes. The movement system makes use of the input system package which makes 
it so that movement with both WASD and arrow keys is possible with one line of code. 
Player attack involves the drawing mechanic that allows the player to attack and uses 
even-odd rule (more in algorithms) to detect player and enemies within the drawn 
shapes. The player attributes scripts that hold information about the player’s health as 
well as the relevant UI assets that are needed to display the health after taking damage. 
Enemies: The scripts relevant to enemies are movement behaviors, attack behaviors, 
and attributes. The movement behaviors scripts are divided into boss and normal 
enemies. The enemy attack behaviors are separated in a similar fashion however they 
are further divided into smaller scripts that take care of enemy projectiles. The projectile 
scripts handle the creation and deletion of the projectiles as well as the amount of 
damage and the path of the attack. The attributes work similarly to the player attributes 
in where it holds the general health, speed, and damage that each enemy needs. In 
addition to these scripts there is a set of scripts known as interaction scripts. These 
allow the player to interact with the enemy and vis versa. 

UI: The UI scripts are simple and include scripts that deal with the main menu, player 
health bar, end screen, and player attack count. A lot of the heaving lifting here is done 
by unity’s built in tools such as Text Mesh and Input System which will be described in 
detail in the next section. 

Even-Odd Rule: Even-Odd Rule is the most important algorithm featured in the game.
This is because we wanted to add a level of difficulty by making it so that attacks would 
also hurt the player. We also wanted it to be possible to draw shapes that make it so the 
player is safe within the attack. For example, a star pattern would have a safe zone in 
the center. Even-Odd Rule makes this possible.

**Unity Tools & Packages**

The Unity engine comes with many useful tools that made game making easy such as 
the 2D core package which lays out the general physics and camera setup for a 2D 
game. In the process of creating our game the most used packages include Text Mesh, 
Input System, Cinemachine, and the 2D core package.

Text Mesh: Text Mesh allows creators to type out text on screen and change elements 
like size, font, color, and intractability of created text. This in combination with the Input
System allowed for a simple start menu that would be easy to use and modify.

Input System: Input System is an updated version of Unity’s old package that lets users 
map buttons and keys, such as WASD, to actions. The new package lets you define 
actions and, for example W moving the character up, outside of a script using a dropdown menu. This is then converted into a script automatically and the user simply has to 
call a set grouping of predefined actions in a separate script, calling player movement in 
a movement script. This also allows buttons to be mapped to multiple different actions at 
the same time and makes switching between menu and gameplay controls easy.

Cinemachine: Cinemachine is a package that replaces the camera package already in 
Unity. It allows for the user to have more control over how the camera moves, the FOV, 
and perspective of the camera while also making it easy to place UI elements onto the 
screen. 

2D Core: The 2D core defines the physics, camera perspective and Unity components
that are available to the user. Components can be described as premade scripts that 
make elements like collision, drawing and script editing easier.

**Project Postmortem**

The games main mechanics were all completed, this includes boss fights, end 
screen, drawing on screen to attack and multiple zones. The game is missing a save 
and load mechanic, a town center with NPCs and general polish that would make the 
game look a lot better. The game is much smaller than we thought it would be. Each 
boss was going to have their own chamber to fight in and spawn in enemies as the fight 
went on. There were supposed to be NPCs with purchasable upgrades and storytelling. 
The number of zones on the map was also going to be 4, one for each enemy type.
Much of the lateness came down to the scrum sheet and our experience with it. 
Two of our group mates, being juniors, did not have a lot of experience with scrum. On 
top of this our seniors who did have more experience only had an extra quarter’s worth 
of experience with the scrum model. However, once we got comfortable with scrum a lot 
of the large aspects of the game got down quickly. We broke down tasks into doable 
components and weren’t struggling to get a final game together. Though the game is not 
perfect and requires many more features to be reasonably work playing, the game is 
something the team is still proud of. 

We will admit that the attacking mechanic does not match the game genre that 
we choose. The mechanic is much better suited for a wave based 2D game rather than 
a Zelda style exploration game. We would change this mechanic or the genre to
produce a better game if we could. Another changes the use of Discord as our way of 
sending files, we should have used GitHub or Unity’s built in file sharing
