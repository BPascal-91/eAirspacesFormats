|imgOpenair100| |imgOpenair101| |imgOpenairBeta|

`Openair`_ Format - Open Airspace and terrain description language
===================
Un format ouvert pour l'encodage de données aéronautiques.


**Table of Contents**

.. contents::
   :backlinks: none
   :local:


Description
-----------
Un format ouvert pour l'encodage de données aéronautiques ; basé sur un format de fichier TEXTE (TEXT-file format) ; optimisé et utilisé par de nombreux logiciels...

Documentation
-------------
`Openair Standard`_ - Version initiale |imgOpenair100| ; puis une première extension |imgOpenair101|
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

`Openair Extended`_ - Version étandue |imgOpenairBeta|
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Le format **OpenAir** a pris naissance dans les années 1990. Depuis 30 ans maintenant, ce langage perdure car il est encore utilisé par de nombreux outils cartographique ou appreils de géolocalisation de type GPS.
De nos jours; le besoin des pilotes a évolué. L'information aéronautique est maintenant digitalisée et les capcités informatique mis a disposition des pilotes n'a cessé de progresser.
Il est donc temps de faire évoluer ce format historique afin de répondre aux nouveaux enjeux ciblés. 

Pour ce faire, plusieurs informations ont étés ajoutés dans le format OpenAir.
Vous trouverez ci-dessous; la description historique du format 'Openair' ; complété des informations nouvellements ajoutées pour étendre ses capacités: 

1. **AC - Airspace Class** - Classification des zones aériennes
	* |imgOpenair100| Liste initiale ['A'=Class A, 'B'=Class B, 'C'=Class C, 'D'=Class D, 'E'=Class E, 'G'=Class G, 'CTR'=Control-Traffic-Region, 'P'=Prohibited, 'R'=restricted, 'Q'=danger, 'GP'=Glider Prohibited, 'W'=Wave Window, 'Other'=Others classification]
	* |imgOpenair101| Liste complétée ['NOTAM'=NOtice-To-AirMan, 'NOTAM ref'=NOTAM + référence]
	* |imgOpenairBeta| Liste complétée ['TMZ'=Transponder-Mandatory-Zone, 'RMZ'=Radio-Mandatory-Zone, 'ZSM'=Zone-Sensibilité-Majeur, 'FFVL'=FFVL-Protocole, 'FFVP'=FFVP-Protocole]
	
2. **AN - Airspace Name** - Libellé de la zone aérienne
	* |imgOpenair100| Texte libre, sans limitation de taille
	* |imgOpenair101| Texte structuré ['NOTAM ref'=pour préciser la référence du NOTAM dans le cas d'une Class 'AC NOTAM']
	* |imgOpenairBeta| Texte multi-structuré

	**AN 'Type' Nom-de-la-zone ['TypeMhz'(Freq-Principale)] [(['CodeActivity'] / [SeeNOTAM])] [Upper(Alt1/Alt2) et/ou Lower(Alt1/Alt2)]**
	
		- **'Type'** - Typage de la zone : parmis la liste ['TMA'=Terminal-Manoeuvring-Area, 'CTR'=Control-Traffic-Region, 'RTBA'=Reseau-Tres-Basse-Altitude, 'ZIT'=Zone-Interdite-Temporaire, 'CTA'=ConTrol-Area, 'CBA'=Cross-Boerder-Area, 'LTA'=Lower-Trafic-Area, 'FFVL-Prot'=FFVL-Protocole, 'FFVP-Prot'=FFVP-Protocole]
		- **'TypeMhz'** - Typage de la fréquence-radio-principale qui est affichée : parmis la liste ['App'=Approche, 'Twr'=Tower, 'FIS'=Flight-Information-Service, 'AFIS'=Automatic-Fligth-Information-Service, 'ATIS'=Automatic-Terminal-Information-Service, ...]
		- **'CodeActivity'** - Codification de l'activité de la zone : parmis la liste ['NUCLEAR', 'MILOPS', 'GLIDER', 'PARAGLIDER', 'PARACHUTE', 'BALOON', 'SPORT', ...]
		- **'SeeNOTAM'** - Affichage de l'information contenue dans le nouveau tag '*ASeeNOTAM' (décrit plus bas...)
		- **'Upper'** (Ceiling) - Affichage optionnel de la double-référence-altimétrique du plafond de la zone
		- **'Lower'** (Floor) - Affichage optionnel de la double-référence-altimétrique du plancher de la zone 

	**Exemples**
		- AN R KOKSIJDE (MILOPS)
		- AN RMZ MORLAIX Twr(118.500)
		- AN ZRT A400M Twr(124.800) (SeeNotam)
		- AN TMA ETAIN 1 App(120.125) (SeeNotam)
		- AN FFVL-Prot LE TOUQUET Twr(118.450) (PARAGLIDER)
		- AN CTR CHAMBERY 1 Twr(118.300) Upper(3500FT AMSL-1000FT AGL)
		- AN TMA CHAMBERY 1 App(123.700) (SeeNotam) Lower(1000FT AGL-3000FT AMSL)


Official Data or Map
--------------------
* `Paragliding OpenAir French Files`_ - The single source of aeronautical information


Crédit
------
* `Pascal Bazile`_ main developer of `Paragliding OpenAir French Files`_



.. |imgOpenair100| image:: res/openair_v1.0.0.svg
   :target: `Openair Standard`_
   :alt: `OpenAir`_ 1.0.0
.. |imgOpenair101| image:: res/openair_v1.0.1.svg
   :target: `Openair 101`_
   :alt: `OpenAir`_ v1.0.1
.. |imgOpenairBeta| image:: res/openair_betaVersion.svg
   :target: `Openair`_
   :alt: `Openair`_ beta

.. _Pascal Bazile: https://github.com/BPascal-91/
.. _Paragliding OpenAir French Files: http://pascal.bazile.free.fr/paraglidingFolder/divers/GPS/OpenAir-Format/

.. _Openair: `Openair (on GitHub)`_
.. _Openair (on GitHub): https://github.com/BPascal-91/eAirspacesFormats/tree/master/openair/#readme
.. _Openair Extended: https://github.com/BPascal-91/eAirspacesFormats/tree/master/openair/#openair-extended
.. _Openair Standard: http://www.winpilot.com/UsersGuide/UserAirspace.asp
.. _Openair 101: https://notaminfo.com/exporthelp#stdopenair
.. _Openair Extended: http://pascal.bazile.free.fr/paraglidingFolder/divers/GPS/OpenAir-Format/

