|imgOpenair1| |imgOpenair2| |imgOpenairBeta|

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
`Openair 1.0.0`_ - Version initiale |imgOpenair1| ; puis une première extension `Openair 1.0.1`_
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Openair Extended** - Version étandue |imgOpenairBeta|
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Le format **OpenAir** a pris naissance dans les années 1990. Depuis 30 ans maintenant, ce langage perdure car il est encore utilisé par de nombreux outils cartographique ou appreils de géolocalisation de type GPS.
De nos jours; le besoin des pilotes a évolué. L'information aéronautique est maintenant digitalisée et les capcités informatique mis a disposition des pilotes n'a cessé de progresser.
Il est donc temps de faire évoluer ce format historique afin de répondre aux nouveaux enjeux ciblés. 

Pour ce faire, plusieurs informations ont étés ajoutés dans le format OpenAir.
Vous trouverez ci-dessous; la description historique du format 'Openair' ; complété des informations nouvellements ajoutées pour étendre ses capacités: 

1. **AC** Airspace Class - Classification des zones aériennes
	* |imgOpenair1| Liste initiale ['A'=Class A, 'B'=Class B, 'C'=Class C, 'D'=Class D, 'E'=Class E, 'G'=Class G, 'CTR'=Control-Traffic-Region, 'P'=Prohibited, 'R'=restricted, 'Q'=danger, 'GP'=Glider Prohibited, 'W'=Wave Window, 'Other'=Others classification]
	* |imgOpenair2| Complété par ['NOTAM'=NOTAM information]
	* |imgOpenairBeta| Complété par ['TMZ'=Transponder-Mandatory-Zone, 'RMZ'=Radio-Mandatory-Zone, 'ZSM'=Zone-Sensibilité-Majeur, 'FFVL'=FFVL-Protocole, 'FFVP'=FFVP-Protocole]
	
2. **AN** Airspace Class - Classification des zones aériennes



Official Data or Map
--------------------
* `Paragliding OpenAir French Files`_ - The single source of aeronautical information


Crédit
------
* `Pascal Bazile`_ main developer of `Paragliding OpenAir French Files`_



.. |imgOpenair1| image:: res/openair_v1.0.0.svg
   :target: `Openair v1.0.0`_
   :alt: `OpenAir`_ 1.0.0
.. |imgOpenair2| image:: res/openair_v1.0.1.svg
   :target: `Openair 1.0.1`_
   :alt: `OpenAir`_ v1.0.1
.. |imgOpenairBeta| image:: res/openair_betaVersion.svg
   :target: `Openair`_
   :alt: `Openair`_ beta

.. _Pascal Bazile: https://github.com/BPascal-91/
.. _Paragliding OpenAir French Files: http://pascal.bazile.free.fr/paraglidingFolder/divers/GPS/OpenAir-Format/

.. _Openair: `Openair (on GitHub)`_
.. _Openair (on GitHub): https://github.com/BPascal-91/eAirspacesFormats/tree/master/openair/#readme
.. _Openair 1.0.0: http://www.winpilot.com/UsersGuide/UserAirspace.asp
.. _Openair 1.0.1: https://notaminfo.com/exporthelp#stdopenair
.. _Openair Extended: http://pascal.bazile.free.fr/paraglidingFolder/divers/GPS/OpenAir-Format/

