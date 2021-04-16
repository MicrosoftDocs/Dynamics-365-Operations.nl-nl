---
title: Power Portal gebruiken met het gegevensmodel van partij
description: In dit onderwerp worden de wijzigingen in de Power Portal-webrollen vanwege het partijgegevensmodel in Twee keer wegschrijven beschreven.
author: RamaKrishnamoorthy
ms.date: 03/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-22
ms.openlocfilehash: a2ea914344341ee26138e853727c551bdd5d733e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833085"
---
# <a name="using-power-portal-with-the-party-data-model"></a>Power Portal gebruiken met het gegevensmodel van partij

[!INCLUDE[banner](../../includes/banner.md)]

[!INCLUDE[rename-banner](~/includes/cc-data-platform-banner.md)]

Orkestratieversie 2.0.999.0 en hoger van de oplossing Twee keer wegschrijven omvatten wijzigingen in het gegevensmodel voor partijen en het globale adresboek voor de tabellen Rekening en Contactpersoon. De wijzigingen maken veel-op-veel-relaties mogelijk die geavanceerde bedrijfsscenario's ondersteunen. Deze wijzigingen worden niet ondersteund door portalwebrollen, inclusief de klantportal, die out-of-the-box worden verzonden of die in uw omgeving bestonden voordat u Twee keer wegschrijven installeerde. Om de webrollen te laten werken zoals verwacht, moet u nieuwe webrollen maken met behulp van het nieuwe gegevensmodel. 

Samengevat is de manier waarop de tabellen samenwerken gewijzigd, maar de tabelmachtigingen in de klantportal zijn niet gewijzigd. In dit onderwerp wordt uitgelegd hoe u nieuwe webrollen maakt die werken met het nieuwe geavanceerde gegevensmodel.

Dit diagram toont de tabelrelatie **zonder** het gegevensmodel voor partijen en het globale adresboek:

   ![zonder partijmodel](media/without-party-model.PNG)

Dit diagram toont de tabelrelatie **met** het gegevensmodel voor partijen en het globale adresboek:

   ![met partijmodel](media/with-party-model.png)

## <a name="create-a-new-table-permission"></a>Een nieuwe tabelmachtiging maken

Voer de volgende stappen uit om deze nieuwe tabelmachtigingen te maken:

1. Meld u aan bij [Power Apps](https://make.powerapps.com) en ga naar uw apps.
2. Selecteer uw Portalbeheer-app.
3. Selecteer **Beveiliging > Tabelmachtigingen** in de zijbalk.

    U moet drie nieuwe machtigingen maken:

    + Verbinding van contactpersoon met partij
    + Verbinding van partij met contactpersoon
    + Verbinding van rekening met order

4. Maak met de volgende parameters een nieuwe machtiging voor de verbinding van contactpersoon met partij en sla deze op:

    + **Naam**: verbinding van partij met rekening (of uw keuze)
    + **Tabelnaam**: msdyn_contactforparty
    + **Website**: klantportal
    + **Bereik**: contactpersoon
    + **Bevoegdheden**: alles selecteren
    + **Webrollen**: geverifieerde gebruikers, klantvertegenwoordiger (of uw keuze)

5. Maak met de volgende parameters een nieuwe machtiging voor de verbinding van partij met rekening en sla deze op:

    + **Naam**: verbinding van partij met rekening (of uw keuze)
    + **Tabelnaam**: rekening
    + **Website**: klantportal
    + **Bereik**: bovenliggend
    + **Bevoegdheden**: alles selecteren
    + **Machtiging bovenliggende tabel**: verbinding van contactpersoon met partij

6. Maak met de volgende parameters een nieuwe machtiging voor de verbinding van rekening met order en sla deze op:

    + **Naam**: verbinding van rekening met order (of uw keuze)
    + **Tabelnaam**: verkooporder
    + **Website**: klantportal
    + **Bereik**: bovenliggend
    + **Bevoegdheden**: alles selecteren
    + **Machtiging bovenliggende tabel**: verbinding van partij met rekening

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
