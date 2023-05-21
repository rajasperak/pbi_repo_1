# pbi_repo_1
![data](https://github.com/rajasperak/kana_tools/blob/main/data.png)

**Exemple de dashboard sur des données réelles:** 
tips et astuces pour l'analyse de séries temporèlles sur powerBI.
On utilisera des données réelles anonymisés. L'analyse se portera sur l'analyse temporelle de log d'erreur.

**contenus**:
- Mise en place de suivi de volumétrie des logs d'erreurs dans le temps.     
![data](https://github.com/rajasperak/pbi_repo_1/blob/main/page1PNG.PNG)
![data](https://github.com/rajasperak/pbi_repo_1/blob/main/modele de donnee.PNG)
- Lissage des données sur 7jours. le choix du lissage se fera par un segment dans la version final
afin de visualiser de manière dynamique l'effet du lissage exponentiel.
![data](https://github.com/rajasperak/pbi_repo_1/blob/main/page2.PNG)
Obtenu grace au code dax ci-dessous:
![data](https://github.com/rajasperak/pbi_repo_1/blob/main/page2_1.PNG)
- Mise en place d'un monitoring d'alerting. La méthode choisi se base sur l'IIQ pour la détection de pic de log. facilement mis en
  place sur power BI.                
 ![data](https://github.com/rajasperak/pbi_repo_1/blob/main/page2_2.PNG)
 Le pic est déclaré quand on passe au dessus de la ligne Jaune. Pour rappel, l'objectif du dashboard est aussi de nous donner
 l'alerte quand la volumétrie lissée dépasse l'intervalle interquartile des 7 derniers jours. On aura deux alertes via power automate
 pour une alerte sur les dernieres 24h et la seconde sur la dernière semaine.
 ![data](https://github.com/rajasperak/pbi_repo_1/blob/main/pics.PNG)
- Etude de corrélation (avec normalisation des donnée pour l'afffichage et aussi afin de facilité la comparaison)                      
 ![data](https://github.com/rajasperak/pbi_repo_1/blob/main/page3.PNG)
- Sinon, nous avons, dans la dernière version de powerBI, à ce jour (Version : 2.115.842.0 64-bit (mars 2023)), on peut faire appel à
une nouvelle fonctionnalité pour la détection d'anomalie. Elle colle bien à notre usage.
