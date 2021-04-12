.. image:: https://github.com/BPascal-91/poaff/res/poaff_lastVersion.svg
   :target: `Paragliding OpenAir French Files`_
   :alt: `Paragliding OpenAir French Files (on GitHub)`_
.. image:: https://github.com/BPascal-91/poaff/res/poaff_lastVersion.svg
   :target: `Openair (on GitHub)`_
   :alt: `Openair (on GitHub)`_
.. image:: aixm/res/aixm_v4.5.0.svg
   :target: `AIXM`_
   :alt: `AIXM`_ v4.5.0
.. image:: aixm/res/aixm_v5.1.0.svg
   :target: `AIXM`_
   :alt: `AIXM`_ v5.1.0
.. image:: openair/res/poaff_lastVersion.svg
   :target: `Paragliding OpenAir French Files`_
   :alt: `Paragliding OpenAir French Files (on GitHub)`_
.. image:: openair/res/openair_v1.0.0.svg
   :target: `Openair`_
   :alt: `Openair`_
.. image:: openair/res/openair_betaVersion.svg
   :target: `Openair`_
   :alt: `Openair`_


eAirspacesFormats - Electreonic Airspaces Formats
==============

Présentation des formalismes électroniques utilisés pour la description des zones contituant l'espace-aérien ainsi que les infrastructures positionnées au sol.

Description des formalismes électroniques utilisés pour la description des espaces-aériens.
Ces formalismes sont ceux nécessaires pour la génération des cartographies publiées sur le blog `Paragliding OpenAir French Files`_.
Ces cartographies sdont référencées sur la Plateforme OpenData Française - `Paragliding OpenAir French Files (on OpenData)`_
Vous pouvez suivre les évolutions via la page `Paragliding OpenAir French Files (on Facebook)`_.

.. code::

	/!\ ATTENTION: Seules des données officielles doivent êtres utilisées pour la navigation aérienne.
	/!\ WARNING  : Only official data must be used for air navigation


**Table of Contents**

.. contents::
   :backlinks: none
   :local:


`AIXM`_ :code:`(Aeronautical Information Exchange Modele)` Format
--------------
.. image:: aixm/res/aixm_v4.5.0.svg
   :target: `AIXM`_
   :alt: `AIXM`_ v4.5.0
.. image:: aixm/res/aixm_v5.1.0.svg
   :target: `AIXM`_
   :alt: `AIXM`_ v5.1.0

Format normalisé d'échange d'information aéronautiques.

	The objective of the Aeronautical Information Exchange Model (AIXM) is to enable the provision in digital format of the aeronautical information that is in the scope of Aeronautical Information Services (AIS). The AIS information/data flows that are increasingly complex and made up of interconnected systems. They involve many actors including multiple suppliers and consumers. There is also a growing need in the global Air Traffic Management (ATM) system for high data quality and for cost efficiency.
	../..
	The following main information areas are in the scope of AIXM:
		Aerodrome/Heliport including movement areas, services, facilities, etc.
		Airspace structures
		Organisations and units, including services
		Points and Navaids
		Procedures
		Routes
		Flying restrictions
	../..


`Openair`_ Format - Open Airspace and terrain description language
--------------
.. image:: openair/res/openair_v1.0.0.svg
   :target: `Openair`_
   :alt: `Openair`_
.. image:: openair/res/openair_betaVersion.svg
   :target: `Openair`_
   :alt: `Openair`_
   
Un format ouvert pour l'encodage de données aéronautiques ; basé sur un format de fichier TEXTE (TEXT-file format) ; optimisé et utilisé par de nombreux logiciels...


`FAF`_ Format -  `Flytec`_ Airspace Formatted
--------------
.. image:: `FAF (on GitHub)`_/res/faf_lastVersion.svg
   :target: `FAF (on GitHub)`_
   :alt: `FAF (on GitHub)`_

Un format pour l'encodage de données aéronautiques définit par l'éditeur `Flytec`_ et utilisable pour les appareils Flytec ou Brauniger
Nota. Le fichier FAF doit généralement être copié dans le dossier 'CarteSD/CTR' de la carte SD

  
  

Official Data & Maps
--------------------
* `Eurocontrol`_ - A pan-European, civil-military organisation dedicated to supporting European aviation
* `France SIA`_ - Service de l'Information Aéronautique
* `France SIA-data`_
* `France DIRCAM`_
* `France DIRCAM-data`_
* `France Carte OACI`_ - Scan digitalisé


Licence
-------
`Licence-GPL3`_


Crédit
------
* `Pascal Bazile`_ main initiator




.. _Pascal Bazile: https://github.com/BPascal-91/
.. _POAFF (on GitHub): https://github.com/BPascal-91/poaff/
.. _Paragliding OpenAir French Files: http://pascal.bazile.free.fr/paraglidingFolder/divers/GPS/OpenAir-Format/
.. _aixmParser (on GitHub): https://github.com/BPascal-91/aixmParser/
.. _openairParser (on GitHub): https://github.com/BPascal-91/openairParser/

.. _AIXM: `AIXM (on GitHub)`_
.. _AIXM (on GitHub): https://github.com/BPascal-91/eAirspacesFormats/AIXM
.. _AIXM Standard: http://www.aixm.aero/
.. _Eurocontrol: https://www.eurocontrol.int/

.. _Openair: `Openair (on GitHub)`_
.. _Openair (on GitHub): https://github.com/BPascal-91/eAirspacesFormats/openair
.. _Openair Standard: http://www.winpilot.com/UsersGuide/UserAirspace.asp
.. _Openair Extended: http://pascal.bazile.free.fr/paraglidingFolder/divers/GPS/OpenAir-Format/

.. _FAF: `FAF (on GitHub)`_
.. _FAF (on GitHub): https://github.com/BPascal-91/eAirspacesFormats/faf
.. _Flytec: https://www.flytec.com/

.. _GeoJSON (on GitHub): `GeoJSON (on GitHub)`_
.. _GeoJSON (on GitHub): https://github.com/BPascal-91/eAirspacesFormats/geojson
.. _GeoJSON: http://geojson.org/

.. _KML: `KML (on GitHub)'_
.. _KML (on GitHub): https://github.com/BPascal-91/eAirspacesFormats/kml
.. _KML Documentation: https://developers.google.com/kml/documentation
.. _XML Documentation: https://www.w3.org/TR/xml/

.. _OACI (on GitHub): https://github.com/BPascal-91/eAirspacesFormats/OACI
.. _France Carte OACI: https://www.geoportail.gouv.fr/donnees/carte-oaci-vfr
.. _France SIA: https://www.sia.aviation-civile.gouv.fr/
.. _France SIA-data: https://www.sia.aviation-civile.gouv.fr/produits-numeriques-en-libre-disposition.html
.. _France DIRCAM: https://www.dircam.dsae.defense.gouv.fr/
.. _France DIRCAM-data: https://www.dircam.dsae.defense.gouv.fr/fr/documentation-4/supp

.. _pip: http://www.pip-installer.org
.. _Licence-GPL3: https://www.gnu.org/licenses/gpl-3.0.html
