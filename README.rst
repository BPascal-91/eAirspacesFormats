.. image:: openair/res/openair_v1.0.0.svg
   :target: `OpenAir`_
   :alt: `OpenAir`_
.. image:: openair/res/openair_betaVersion.svg
   :target: `Openair`_
   :alt: `Openair`_
.. image:: faf/res/faf_v1.0.0.svg
   :target: `FAF`_
   :alt: `FAF`_
.. image:: aixm/res/aixm_v4.5.0.svg
   :target: `AIXM`_
   :alt: `AIXM`_ v4.5.0
.. image:: aixm/res/aixm_v5.1.0.svg
   :target: `AIXM`_
   :alt: `AIXM`_ v5.1.0
.. image:: ofmx/res/ofmx_v-.-.-.svg
   :target: `OFMX`_
   :alt: `OFMX`_ v?.?.?


`eAirspacesFormats`_ - Electreonic Airspaces Formats
====================================================
Présentation des formalismes électroniques utilisés pour la description des espaces-aériens et infrastructures positionnées au sol.

Ces formalismes sont ceux nécessaires pour la génération des cartographies publiées sur le blog `Paragliding OpenAir French Files`_.
Ces cartographies sont référencées sur la plateforme OpenData Française - `Paragliding OpenAir French Files (on OpenData)`_.
Vous pouvez également suivre les évolutions via la page de communication `Paragliding OpenAir French Files (on Facebook)`_.

.. code::

	/!\ ATTENTION: Seules des données officielles doivent êtres utilisées pour la navigation aérienne.
	/!\ WARNING  : Only official data must be used for air navigation.


**Table of Contents**

.. contents::
   :backlinks: none
   :local:


--------------------


Formatismes
-----------

`Openair`_ Format - Open Airspace and terrain description language
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: openair/res/openair_v1.0.0.svg
   :target: `Openair`_
   :alt: `Openair`_
.. image:: openair/res/openair_betaVersion.svg
   :target: `Openair`_
   :alt: `Openair`_  
.. code::

	Un format ouvert pour l'encodage de données aéronautiques ; basé sur un format de fichier TEXTE (TEXT-file format) ; optimisé et utilisé par de nombreux logiciels...
	Description complète -> `Openair`_


`FAF`_ Format - `Flytec`_ Airspace Formatted
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: faf/res/faf_v1.0.0.svg
   :target: `FAF`_
   :alt: `FAF`_
.. code::

	Un format pour l'encodage de données aéronautiques définit par l'éditeur `Flytec`_ ; utilisable pour appareils Flytec ou Brauniger.
	Description complète -> `FAF`_
	*Nota. Le fichier FAF doit généralement être copié dans le dossier 'CarteSD/CTR' de la carte SD.*


`AIXM`_ Format - Aeronautical Information Exchange Modele
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: aixm/res/aixm_v4.5.0.svg
   :target: `AIXM`_
   :alt: `AIXM`_ v4.5.0
.. image:: aixm/res/aixm_v5.1.0.svg
   :target: `AIXM`_
   :alt: `AIXM`_ v5.1.0
.. code::

	Format normalisé d'échange d'information aéronautiques ../..
	Description complète -> `AIXM`_


`OFMX`_ Format - Open FlightMaps eXchange
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: ofmx/res/ofmx_v-.-.-.svg
   :target: `OFMX`_
   :alt: `OFMX`_ v?.?.?
.. code::

	OFMX (Open FlightMaps eXchange) is a suite of well-defined data formats to validate and exchange aeronautical data with open flightmaps (OFM).
	Description complète -> `OFMX`_


`GeoJSON`_ Format - GeoJSON Documentation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. code::

	Description complète -> `GeoJSON`_


`KML`_ Format - KML Documentation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. code::

	Description complète -> `KML`_

   
`XML`_ Format - XML Documentation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. code::

	Description complète -> `XML`_



--------------------


Official Data or Map
--------------------
* `OACI Abreviation`_ - Abréviations officielles OACI
* `European AIS Database`_ - The single source of aeronautical information
* `Eurocontrol (Data availability)`_ - (from `Eurocontrol`_ - A pan-European, civil-military organisation dedicated to supporting European aviation)
* `AIXM Eurocontrol Confluence Invotory`_ - (or `AIXM Eurocontrol Confluence Invotory Map`_)
* `France SIA-data`_ - Produits numériques en libre disposition (`France SIA`_ - Service de l'Information Aéronautique)
* `France DIRCAM-data`_ - SUPAIP (via `France DIRCAM`_ - DIRection de la Circulation Aérienne Militaire)
* `France OACI Map`_ - Cartographie officielle OACI pour l'information aéronautique en France



Crédit
---------
* `Pascal Bazile`_ main initiator




.. _Pascal Bazile: https://github.com/BPascal-91/
.. _eAirspacesFormats: https://github.com/BPascal-91/eAirspacesFormats/#readme
.. _Paragliding OpenAir French Files: http://pascal.bazile.free.fr/paraglidingFolder/divers/GPS/OpenAir-Format/
.. _Paragliding OpenAir French Files (on OpenData): https://www.data.gouv.fr/fr/datasets/cartographies-aeriennes-dediees-a-la-pratique-du-vol-libre/
.. _Paragliding OpenAir French Files (on Facebook): https://www.facebook.com/Paragliding-OpenAir-FrenchFiles-102040114894513
.. _POAFF (on GitHub): https://github.com/BPascal-91/poaff/#readme
.. _aixmParser (on GitHub): https://github.com/BPascal-91/aixmParser/#readme
.. _openairParser (on GitHub): https://github.com/BPascal-91/openairParser/#readme

.. _Openair: `Openair (on GitHub)`_
.. _Openair (on GitHub): https://github.com/BPascal-91/eAirspacesFormats/tree/master/openair/#readme
.. _Openair Standard: http://www.winpilot.com/UsersGuide/UserAirspace.asp
.. _Openair Extended: http://pascal.bazile.free.fr/paraglidingFolder/divers/GPS/OpenAir-Format/

.. _FAF: `FAF (on GitHub)`_
.. _FAF (on GitHub): https://github.com/BPascal-91/eAirspacesFormats/tree/master/faf/#readme
.. _Flytec: https://www.flytec.com/

.. _AIXM: `AIXM (on GitHub)`_
.. _AIXM (on GitHub): https://github.com/BPascal-91/eAirspacesFormats/tree/master/aixm/#readme
.. _AIXM Standard: http://www.aixm.aero/
.. _AIXM Eurocontrol Confluence Invotory: https://ext.eurocontrol.int/aixm_confluence/display/AIX/Inventory
.. _AIXM Eurocontrol Confluence Invotory Map: https://ext.eurocontrol.int/aixm_confluence/display/AIX/Overview

.. _OFMX: https://gitlab.com/openflightmaps/ofmx/-/wikis/home
.. _GeoJSON: http://geojson.org/
.. _KML: https://developers.google.com/kml/documentation/
.. _XML: https://www.w3.org/TR/xml/

.. _Eurocontrol: https://www.eurocontrol.int/
.. _European AIS Database: https://www.eurocontrol.int/service/european-ais-database
.. _Eurocontrol (Data availability): https://www.eurocontrol.int/service/static-data-operations

.. _France SIA: https://www.sia.aviation-civile.gouv.fr/
.. _France SIA-data: https://www.sia.aviation-civile.gouv.fr/produits-numeriques-en-libre-disposition.html

.. _France DIRCAM: https://www.dircam.dsae.defense.gouv.fr/
.. _France DIRCAM-data: https://www.dircam.dsae.defense.gouv.fr/fr/documentation-4/supp

.. _OACI (on GitHub): https://github.com/BPascal-91/eAirspacesFormats/tree/master/oaci
.. _OACI Abreviation: https://github.com/BPascal-91/eAirspacesFormats/tree/master/oaci/res/20100101_DEF_ABRV.pdf
.. _France OACI Map: https://www.geoportail.gouv.fr/donnees/carte-oaci-vfr

.. _pip: http://www.pip-installer.org
.. _Licence-GPL3: https://www.gnu.org/licenses/gpl-3.0.html

