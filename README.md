# World Cup Software.

## Introduction
Ce logiciel génère un arble des matches de la compétition, en fonction des stades disponibles et d’un tirage pseudo-aléatoire.

## Mode d’emploi 
Une fois les valeurs entrées dans le code, lancez-le : le planning doit être affiché. 

## Contraintes
Un match doit avoir un stade, deux équipes, une date.
Un stade ne peut pas être utilisé 2 jours de suite.
Il y a 4 matchs par jour.

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
lance le programme

#### + initialize()
initialize la vu de l'arbre entirer sans les equipe à l'interieur

##### + countTeamAvailable()
  combient d'equipe encore , dans le tournoi

##### + countNbMatchsByRound() : Int

combient de match par phase

#### checkWinner()
verifie qui est le gagnat


# Classe Round
### Fonctions 
## @Constructeur :
### Paramètres : 
|Nom           | Type   | Valeur |
|--------------| ------ | -------|
|+ id| String||
|+ matchs | Object||

### Méthodes

### + createMatchs()
 crée un match 

### + teamsForRound() 
### + checkLastRound()


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



