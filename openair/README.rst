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
Un format ouvert pour l'encodage de données aéronautiques ; basé sur un format de fichier TEXTE (TEXT-file format) ; optimisé et utilisé par de nombreux logiciels.

Le format **OpenAir** a pris naissance dans les années 1990. Depuis 30 ans maintenant, ce langage perdure car il est utilisé par de nombreux outils cartographique ou appreils de géolocalisation de type GPS.
De nos jours; le besoin des pilotes a évolué. L'information aéronautique s'est grandement digitalisée et les capcités informatique mis à disposition des pilotes n'a cessé de progresser.
Il est donc temps de faire évoluer ce format historique afin de répondre aux nouveaux enjeux ciblés !

Depuis septembre 2019 ; `Pascal Bazile`_ s'attache à compléter se formalisme pour étendre ses capacités et y ajouter de nombreuses informations utiles à tous les piloltes...
Vous trouverez ci-dessous ; l'historique des évolutions ainsi que la description détaillée de ce formalisme `Openair`_


Exemples de contenus en version initiale |imgOpenair100|
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
	.. code::
	
		*** Tracé d'un rectangle, coordonnées précisées avec une taille-fixe
		AC D
		AN TMA ORLEANS 5.1
		AH FL065
		AL 3500FT AMSL
		DP 47:52:20 N 002:01:57 E
		DP 47:42:12 N 002:06:19 E
		DP 47:36:24 N 001:56:51 E
		DP 47:44:30 N 001:32:30 E
		DP 47:52:20 N 002:01:57 E

		*** Tracé d'un cercle, coordonnées précisées avec une taille-fixe
		AC P
		AN ZIT Luxeuil
		AH 500FT AGL
		AL SFC
		V X=47:47:20 N 006:21:20 E
		DC 1.1

		*** Tracé contenant Arc-horaire et Arc-AntiHoraire, coordonnées précisées avec une taille-fixe
		AC D
		AN TMA MONTPELLIER 2
		AH FL145
		AL 2000FT AMSL
		DP 43:29:20 N 003:50:39 E
		DP 43:34:12 N 003:43:40 E
		DP 43:38:27 N 003:39:40 E
		V X=43:34:49 N 003:58:16 E
		V D=+
		DB 43:38:27 N 003:39:40 E, 43:45:15 N 003:45:24 E
		DP 43:45:15 N 003:45:24 E
		DP 43:45:45 N 003:59:56 E
		DP 43:40:10 N 004:06:40 E
		V X=43:34:49 N 003:58:16 E
		V D=-
		DB 43:40:10 N 004:06:40 E, 43:29:20 N 003:50:39 E
		DP 43:29:20 N 003:50:39 E

Exemples de contenus dans la nouvelle version |imgOpenairBeta|
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
	.. code::
	
		*** Tracé d'un rectangle, taille des coordonnées optimisée + ajout des nouvelles informations (volontairement positionnées en commentaire ('*' en entête) afin d'assurer une 'compatibilité ascendante' pour les anciens-outillages...)
		AC D
		AN TMA ORLEANS 5.1 App(123.300) (FFVP-Prot)
		*AAlt ["3500FT AMSL/FL065", "1066m/1981m"]
		*AUID GUId=LFOJ5.1 UId=1563043 Id=LFOJ5.1
		*ADescr OAT/GAT procedures. Activity known on RAI 122.7, PARIS ACC/FIC or SEINE SIV. Except for: -LF-R 243 when active. - LF-P 34 SAINT LAURENT DES EAUX: entry prohibited, exception see AIP ENR 5.1
		*AMhz {"APP": ["123.300*", "Freq veillée/Monitored frequency"], "APP1": ["122.700*", "Freq veillée.RAI/Monitored frequency.Automatical information transmitter"], "TWR": ["121.500*", "Freq veillée/Monitored frequency"], "TWR1": ["124.800*", "Freq veillée/Monitored frequency"], "TWR2": ["122.100*", "Freq veillée/Monitored frequency"]}
		*AActiv [HX] (Pascal Bazile: Voir protocole https://federation.ffvl.fr/sites/ffvl.fr/files/Protocole_Orleans_2015-BA123.pdf) - Activable H24. Possible activation H24
		*ADecla Yes
		AH FL065
		AL 3500FT AMSL
		DP 47:52:20N 2:1:57E
		DP 47:42:12N 2:6:19E
		DP 47:36:24N 1:56:51E
		DP 47:44:30N 1:32:30E
		DP 47:52:20N 2:1:57E

		*** Tracé d'un cercle, taille des coordonnées optimisée + ajout des nouvelles informations
		AC P
		AN ZIT Luxeuil
		*AAlt ["SFC/500FT AGL", "0m/429m"]
		*AUID GUId=ZITLUXEUIL UId=BPa-FR-SIA-SUPAIP-2020-069-ZITLUXEUIL-ZIT Id=ZITLUXEUIL
		*ADescr (Pascal Bazile 15/01/2021 - Source SIA lf_sup_2020_069_fr.pdf) Interdiction de survol d’installations défense spécifiques
		*AActiv [TIMSH] (BPa: Activable du 01/01/2021 au 21/04/2021) Zone interdite temporaire active du 07/05/2020 au 21/04/2021
		*ATimes {"1": ["UTCW(01/01->21/04)", "ANY(00:00->23:59)"]}
		AH 500FT AGL
		AL SFC
		V X=47:47:20N 6:21:20E
		DC 1.1

		*** Tracé contenant Arc-horaire et Arc-AntiHoraire, taille des coordonnées optimisée + ajout des nouvelles informations
		AC D
		AN TMA MONTPELLIER 2 App(130.855)
		*AAlt ["2000FT AMSL/FL145", "609m/4419m"]
		*AUID GUId=LFMT2 UId=1566551 Id=LFMT2
		*ADescr Portions of this airspace coexist with LF- R 108 E1, 108 E2 and 108 C ISTRES, whose entry conditions are stated in part ENR 5.1.
		*AMhz {"APP": ["130.855", "- TMA Montpellier parties 7, 8, 9 et de 14 à 23 / TMA Montpellier parts 7, 8, 9 and from 14 to 23.# - Volumes des TMA 3, 4 et 5 inclus dans le SIV Montpellier partie 5 / Volumes of TMA 3, 4 and 5 included in FIS Montpellier part 5."], "APP1": ["120.375"], "APP2": ["131.055", "- TMA Montpellier parties 1, 2, 3.1, 4, 4.1, 6, 6.1 et de 10 à 13 / TMA Montpellier parts 1, 2, 3.1, 4, 4.1, 6, 6.1 and from 10 to 13#- Volumes des TMA Montpellier parties 3, 4, 5 inclus dans le SIV Montpellier partie 1 / Volumes of TMA Montpellier parts 3, 4, 5 included in FIS Montpellier part 1"], "APP3": ["127.280"], "TWR": ["118.200"], "TWR1": ["118.775"], "FIS": ["134.375", "SIV 1 et/and 2."], "FIS1": ["125.650", "SIV 3, 4 et/and 4.1."], "ATIS": ["124.130", "TEL ATIS: 04 67 13 11 70", "0467131170"]}
		*AActiv [H24]
		AH FL145
		AL 2000FT AMSL
		DP 43:29:2N 3:50:39E
		DP 43:34:12N 3:43:4E
		DP 43:38:27N 3:39:40E
		V X=43:34:49N 3:58:16E
		V D=+
		DB 43:38:27N 3:39:40E, 43:45:15N 3:45:24E
		DP 43:45:15N 3:45:24E
		DP 43:45:45N 3:59:56E
		DP 43:40:1N 4:6:40E
		V X=43:34:49N 3:58:16E
		V D=-
		DB 43:40:1N 4:6:40E, 43:29:2N 3:50:39E
		DP 43:29:2N 3:50:39E

Documentation
-------------

`Openair Standard`_ - Version initiale |imgOpenair100|
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

`Openair v1.0.1`_ - Une première extension du formalisme |imgOpenair101|
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

`Openair Extended`_ - Version actuelle étandue |imgOpenairBeta|
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
* **AC - Airspace Class** - Classification des zones aériennes
	1. |imgOpenair100| Liste initiale ['A'=Class A, 'B'=Class B, 'C'=Class C, 'D'=Class D, 'E'=Class E, 'G'=Class G, 'CTR'=Control-Traffic-Region, 'P'=Prohibited, 'R'=Restricted, 'Q'=danger, 'GP'=Glider-Prohibited, 'W'=Wave-Window, <Others>=Autres-classification]
	2. |imgOpenair101| Liste complétée par ['NOTAM'=NOtice-To-AirMan, 'NOTAM ref'=NOTAM-référence]
	3. |imgOpenairBeta| Liste complétée par ['TMZ'=Transponder-Mandatory-Zone, 'RMZ'=Radio-Mandatory-Zone, 'ZSM'=Zone-Sensibilité-Majeur, 'FFVL'=FFVL-Protocole, 'FFVP'=FFVP-Protocole]

* **AN - Airspace Name** - Libellé de la zone aérienne
	1. |imgOpenair100| Texte libre, sans limitation de taille [mais limité à 16 caractères pour un export sous (Flytec)FAF-format]
	2. |imgOpenair101| Texte libre, ou multi-structuré dans le cas d'une classe 'AC NOTAM':
	**AN NOTAM NOTAM-reference 'Full-type' 'Shorter-type' 'Yet-shorter-type' 'Shortest-type' 'Start-time' 'End-time' 'Schedule' 'Text'**
		- the literal text 'NOTAM'
		- the NOTAM reference
		- **'Full-type'** - The full NOTAM type
		- **'Shorter-type'** - A shorter NOTAM type restricted to 40 characters
		- **'Yet-shorter-type'** - A yet shorter NOTAM type restricted to 25 characters
		- **'Shortest-type'** - The shortest NOTAM type, restricted to 16 characters
		- **'Start-time'** - The NOTAM start
		- **'End-time'** - The NOTAM end
		- **'Schedule'** - The NOTAM schedule
		- **'Text'** - The NOTAM text
	.. code::
	
		*** Here's an example of a NOTAM exported to XCSoar:
		AC NOTAM
		AN NOTAM Air display 16Aug 12:30-16Aug 14:00 H3901/15 AIR DISPLAY/AEROBATICS WI 2NM RADIUS 511918N 0000431E (VCY BIGGIN HILL, KENT). OPS CTC 07803 713470. 15-08-0337/AS4.
		AL SFC
		AH 2400ALT
		V X=51:19:18 N 000:04:31 E
		DC 2

	3. |imgOpenairBeta| Texte libre, ou multi-structuré:
	**AN 'Type' Nom-de-la-zone ['TypeMhz'(Freq-Principale)] [(['CodeActivity'] / [SeeNOTAM])] [Upper(Alt1/Alt2) et/ou Lower(Alt1/Alt2)]**
		- **'Type'** - Typage de la zone : parmis la liste ['TMA'=Terminal-Manoeuvring-Area, 'CTR'=Control-Traffic-Region, 'RTBA'=Reseau-Tres-Basse-Altitude, 'ZIT'=Zone-Interdite-Temporaire, 'CTA'=ConTrol-Area, 'CBA'=Cross-Boerder-Area, 'LTA'=Lower-Trafic-Area, 'FFVL-Prot'=FFVL-Protocole, 'FFVP-Prot'=FFVP-Protocole]
		- **'TypeMhz'** - Typage de la fréquence-radio-principale qui est affichée : parmis la liste ['App'=Approche, 'Twr'=Tower, 'FIS'=Flight-Information-Service, 'AFIS'=Automatic-Fligth-Information-Service, 'ATIS'=Automatic-Terminal-Information-Service, ...]
		- **'CodeActivity'** - Codification de l'activité de la zone : parmis la liste ['NUCLEAR', 'MILOPS', 'GLIDER', 'PARAGLIDER', 'PARACHUTE', 'BALOON', 'SPORT', ...]
		- **'SeeNOTAM'** - Affichage de l'information contenue dans le nouveau tag '*ASeeNOTAM' (décrit plus bas...)
		- **'Upper'** (Ceiling) - Affichage optionnel de la double-référence-altimétrique du plafond de la zone
		- **'Lower'** (Floor) - Affichage optionnel de la double-référence-altimétrique du plancher de la zone 
	.. code::
	
		*** Quelques exemples
		- AN R KOKSIJDE (MILOPS)
		- AN R KOKSIJDE (MILOPS)
		- AN RMZ MORLAIX Twr(118.500)
		- AN ZRT A400M Twr(124.800) (SeeNotam)
		- AN TMA ETAIN 1 App(120.125) (SeeNotam)
		- AN FFVL-Prot LE TOUQUET Twr(118.450) (PARAGLIDER)
		- AN CTR CHAMBERY 1 Twr(118.300) Upper(3500FT AMSL-1000FT AGL)
		- AN TMA CHAMBERY 1 App(123.700) (SeeNotam) Lower(1000FT AGL-3000FT AMSL)

* **\*AH2 - Second Airspace Ceiling** - Seconde altitude du plafond de la zone
	* |imgOpenair100| ../..



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
   :target: `Openair v1.0.1`_
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
.. _Openair v1.0.1: https://notaminfo.com/exporthelp#stdopenair
.. _Openair Extended: http://pascal.bazile.free.fr/paraglidingFolder/divers/GPS/OpenAir-Format/

