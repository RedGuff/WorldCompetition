# World Cup Software.

## Introduction
Ce logiciel d’organisation de compétitions organise des matchs d’équipes en fonction des stades disponibles et d’un tirage pseudo-aléatoire.

## Mode d’emploi 
Une fois les valeurs entrées dans le code, lancez-le : le planning doit être affiché. 

## Contraintes
Chaque match a un stade, un moment, deux équipes.
Chaque stade a besoin d’une journée de préparation avant le match (sécurité) et après (nettoyage), un lieu, un nom.
Les équipes ont besoin de repos : maximum 2 jours de matchs consécutifs.
4 matchs maximum par jour, 2 matchs maximum à la fois (2 le matin et 2 le soir par exemple).

## Composants
Date = moment du match (jour, heure).

Il y a un pays organisateur, qui a des stades disponibles.
Les stades sont créés dans la classe du pays organisateur.

Chaque équipe a un nom. 

availableMatch: Bool : indique si l’entité (stade ou équipe) est disponible pour un match en ces circonstances (date…).

## Diagramme
![Diagramme des classes](FootCompetition.png)
// TODO : à revoir.


# Classe HostCountry

### Fonctions 
## @Constructeur :
### Paramètres : 
|Nom           | Type   | Valeur |
|--------------| ------ | -------|
|+ stades      | Object | {}     |
|+ nameCountry | String |        |
|+ codeIso     | String |        |

#### getStade()
Affiche le pays organisateur.


# Classe PlanningCompetition

### Fonctions 
## @Constructeur :
### Paramètres : 
|Nom           | Type   | Valeur |
|--------------| ------ | -------|
|+ hostCountry      | String | {}     |
|+ teams | Object |        |


### Méthodes
### + run()

#### + initialize()


##### + countTeamAvailable() : Int
##### + countNbMatchsByRound() : Int

#### getStade()
Affiche le pays organisateur.


+ renderMatch()
Prend le score du match
+ setTeam(team1: Object, team2 : Object)
Indique les matches de l'équipe.
+ tplMatch() 
Templace du match (carré avec les traits)



# Classe Round
### Fonctions 
## @Constructeur :
### Paramètres : 
|Nom           | Type   | Valeur |
|--------------| ------ | -------|
|+ id| String||
|+ matchs | Object||

### Méthodes
### + run()
Lance le match.
#### + initialize()
Initialise le match
##### + createMatchs(Int)
Organise les matchs
##### + teamsForRound() : Object

##### + checkLastRound(): Bool


# Classe Team
### Fonctions 
## @Constructeur :
### Paramètres : 
|Nom           | Type   | Valeur |
|--------------| ------ | -------|
|+ name      | String | {}     |
|+ nbPlayers      | int | {}     |
|+ nameCountry      | String | {}     |
|+ available      | Bool | {}     |

### Méthodes
### + run()
#### + initialize()
##### + availableMatch(win: Bool): Bool

# Classe Stade
### Fonctions 
## @Constructeur :
### Paramètres : 
|Nom           | Type   | Valeur |
|--------------| ------ | -------|
|+ id  |-String||
|+ name| String||
|+ city| String||
|+ nbSeat| Int||
|+ available| Bool||
|+ lastDateUse | Date||


### Méthodes
### + run()
#### + initialize()
##### + setAvailable(available: Bool)
##### + getAvailable(): Bool
Indique si le stade est disponible.
##### + setId(id : String)
Identifie le stade.
##### + getId(): String
Identifie le stade.
##### + setName(name :String)
Identifie le stade.
##### + getName() : String
Identifie le stade.
##### + setNbSeat(nbSeat : Int)
Caractérise le stade.
##### + getNbSeat() : Int
Caractérise le stade.
##### + setLastDateUse( dateUse : Date) 
Dernier jour d'utilisation.
##### + getLastDateUse() : Date
Dernier jour d'utilisation.

# Classe Match
### Fonctions 
## @Constructeur :
### Paramètres : 
|Nom           | Type   | Valeur |
|--------------| ------ | -------|
|+ stade | Object||
|+ date|Date ||


### Méthodes
### + run()
#### + initialize()
##### + looser(teamLooser Object) : Object
##### + renderMatch()
##### + setTeam(team1: Object, team2 : Object)
##### + tplMatch() 



