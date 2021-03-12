---
title: Rechtspersonen maken
description: In dit onderwerp wordt beschreven hoe u rechtspersonen kunt maken in Microsoft Dynamics 365 Commerce. Deze moeten worden gemaakt en geconfigureerd voordat u afzetkanalen gaat maken.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9491feb004366a02155225bfb323773e130f3dc9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993598"
---
# <a name="create-legal-entities"></a>Rechtspersonen maken


[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u rechtspersonen kunt maken in Microsoft Dynamics 365 Commerce. Deze moeten worden gemaakt en geconfigureerd voordat u afzetkanalen gaat maken.

## <a name="overview"></a>Overzicht

Een rechtspersoon is een organisatie met een geregistreerde of wettelijke juridische structuur. Rechtspersonen kunnen wettelijk bindende overeenkomsten aangaan en zijn verplicht prestatieoverzichten te overleggen.

Een bedrijf is een type rechtspersoon. Momenteel zijn bedrijven het enige type rechtspersoon dat u kunt maken. Aan elke rechtspersoon is een bedrijfs-id gekoppeld. Deze koppeling bestaat omdat een aantal functionele gebieden in het programma een bedrijfs-id of *DataAreaId* in hun gegevensmodellen gebruiken. In deze functionele gebieden worden bedrijven gebruikt als begrenzing voor gegevensbeveiliging. Gebruikers hebben alleen toegang tot gegevens voor het bedrijf waarbij ze momenteel zijn aangemeld. 

Wanneer u een kanaal maakt, moet u opgeven tot welke rechtspersoon het afzetkanaal behoort.

## <a name="create-a-new-legal-entity"></a>Een nieuwe rechtspersoon maken

Ga als volgt te werk om een nieuwe rechtspersoon te maken in Dynamics 365 Commerce.

1. Ga in het navigatiedeelvenster naar **Modules \> Headquarters instellen \> Rechtspersonen**.
1. Selecteer **Nieuw** in het actievenster. Het deelvenster **Nieuwe rechtspersoon** verschijnt aan de rechterkant.
1. Voer een waarde in het veld **Naam** in.
1. Voer een waarde in het veld **Bedrijf** in.
1. Typ of selecteer een waarde in het **veld Land/regio**.
1. Selecteer **OK**. 

   ![Het maken van een rechtspersoon](media/legal-entities.png)

1. Geef in de sectie **Algemeen** de volgende algemene informatie op over de rechtspersoon: 
   1. Voer een zoeknaam in als een zoeknaam is vereist. Een zoeknaam is een alternatieve naam waarmee u naar deze rechtspersoon kunt zoeken. 
   1. Selecteer of deze rechtspersoon wordt gebruikt als consolidatiebedrijf.
   1. Selecteer of deze rechtspersoon wordt gebruikt als eliminatiebedrijf. 
   1. Selecteer de **standaardtaal** voor de rechtspersoon. 
   1. Selecteer de **tijdzone** voor de rechtspersoon.
1. Selecteer in de sectie **Adressen** de optie **Bewerken** om adresgegevens in te vullen, zoals straatnaam en -nummer, postcode en plaats.
1. Voer in de sectie **Contactgegevens** informatie in over communicatiemethoden, zoals e-mailadressen, URL's en telefoonnummers.
1. Voer in de sectie **Wettelijke rapportage** de registratienummers in die worden gebruikt voor wettelijke aangiften.
1. Voer in de sectie **Registratienummers** informatie in die door de rechtspersoon wordt vereist.
1. Voer in de sectie **Bankrekeninggegevens** bankrekeningen en routenummers in voor de rechtspersoon.
1. Voer in de sectie **Buitenlandse handel en logistiek** verzendingsgegevens voor de rechtspersoon in.
1. In de sectie **Nummerreeksen** kunt u de nummerreeksen weergeven die aan de rechtspersoon zijn gekoppeld. Deze is in eerste instantie leeg.
1. In de sectie **Dashboardafbeelding** kunt u het logo en/of de dashboardafbeelding bekijken of wijzigen die aan de rechtspersoon zijn gekoppeld.
1. Voer in de sectie **Belastingregistratie** de registratienummers in die worden gebruikt om te rapporteren aan de belastingdienst.
1. Voer in de **1099-belasting** 1099-gegevens voor de rechtspersoon in.
1. In de sectie **Belastinginformatie** voert u de belastinginformatie voor de rechtspersoon in.
1. Selecteer **Opslaan**.

In de volgende afbeelding ziet u voorbeeldgegevens van een rechtspersoon.

![Sectie Algemeen van rechtspersoon](media/legal-entities-general.png)
   
## <a name="additional-resources"></a>Aanvullende resources

[Overzicht van Organisaties en organisatiehiërarchieën](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Uw organisatiehiërarchie plannen](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[Organisatiehiërarchieën](channels-org-hierarchies.md)

[Overzicht van kanalen](channels-overview.md)

[Vereisten voor het instellen van kanalen](channels-prerequisites.md)
