# RPG game
##### RPG game where hero discover locations and needs to kill Armored dwarf as last boss. Locations are picked randomly and hero cannot go twice to same location

# Content of Readme:
* [Technology](#technology)
* [Solutions](#solutions)
* [Content of game](#content-of-game)
* [Future upgades](#future-upgrades)
* [Inspiration](#inspiration)

## Technology:
* Python 3.11

## Solutions:
* Create dictionary for weared equipment, where key is defense, damage and hp. Defense and damage are separate dictionaries witl key name of item, value is a list with better name and attack/defense. Example below:

possible_defense_item = {
    "small_shield": ("Small shield", 5),
    "medium_shield": ("Medium shield", 10),
    "big_shield": ("Big shield", 15),
}

equipment = {
    "damage": "small_sword",
    "defense": "small_shield",
    "health_point": max_hp
}

* Locations are functions, where user needs to input if he want to fight, or run away. If run away then proceed with other location. If fight then open another funtion with calculations if Hero will win or lose fight. If lose, then end game (because Hero is dead), if win then receive new item or other bonus. If item then ask if user want to wear this item, or not. If yes, then remove current item in this category (defense or damage) and wear new by pop function and add in dictionary new key with values from other dictionary. After this, location needs to be removed from possible locations (hero can visit any location only once). 

* When user visit location and receive any bonus (like increase hp or new item) user should be able to see new stats - attack, defense and max hp
* Fight function to remove rows in evey location

## Content of game:
* [Equipment](#equipment)
* [Locations](#locations)
* [Enemies](#enemies)


### Equipment:
* [Attack](#attack)
* [Defense](#defense)
* [HP](#hp)



#### Attack:
In game we got 3 swords, hero can equip only one sword, so pick best sword if You can!
* Small sword - 10 attack
* Medium sword - 20 attack
* Big sword - 30 attack
 
#### Defense:
In game we got 3 shields, same as swords, hero can equip only one shield:
* Small shield - 5 defense
* Medium shield - 10 defense
* Big shield - 15 attack

#### HP:
Hero starts with 100 health points. But it can increase if he goes to specific locations. 

### Locations
In locations Hero will have to fight with enemies or run out of fight. Some locations does not require to fight, in those places hero will receive some kind of bonuses.

Current location list:
* [Tavern](#tavern)
* [Cave](#cave)
* [Forest](#forest)
* [Pyramid](#pyramid)
* [City](#city)



##### Tavern:
In tavern hero will rest. It will increase max HP by 50. No fight necessary.

##### Cave:
[Werewolf](#werewolf) is guarding Cave. If You want to get any item from this location, first You need to kill guardian.

##### Forest:
In Forest [Small pixies](#small-pixies) got their camp. Hero can greet pixies or run away. Beware, not all of pixies are friendly.

##### Pyramid:
Hero found sarcophagus in Pyramid. Old [Mummy](#mummy) wake up and attack You. Try to kill enemy if You want to find new item, or run away if You are too weak. 

##### City:
In city You will spot [Armored Dwarf](#armored-dwarf). Boss of this game. Do not fight untill You are 100% sure You will win, or it will be end of the game for You! 


### Enemies:
In journey hero will spot few enemies. One of them are easy to kill, another one impossible to defeat. Try to run away, if You cannot beat your enemy. 

* [Werewolf](#werewolf)
* [Small pixies](#small-pixies)
* [Mummy](#mummy)
* [Armored Dwarf](#armored-dwarf)


##### Werewolf:
Hero can find this enemy in [Cave](#cave). Werewolf stat:
HP: 50
Attack: 2
Defense: 0

##### Small pixies:
Hero can find this enemy in [Forest](#forest). Pixie stat:
HP: 250
Attack: 200
Defense: 100

##### Mummy:
Hero can find this enemy in [Pyramid](#pyramid). Mummy stat:
HP: 75
Attack: 10
Defense: 10

##### Armored Dwarf:
Hero can find this enemy in [City](#city). Dwarf stat:
HP: 100
Attack: 10
Defense: 15


## Future upgrades:
* After dying ask user if he want to play again
* Add new locations
* Upgrade enemies
* Add levels to hero and calculations in fight functions 
* Add magic atack and magic defense, and calculations with those stats (e.g. Werewolf will be easier to defeat with magic atack than with normal atack)


## Inspiration
Excercise from CODE:ME courses Basic python - Hackaton_01 (https://github.com/ritaly/CODEME-python23/tree/main/hackaton_01_
