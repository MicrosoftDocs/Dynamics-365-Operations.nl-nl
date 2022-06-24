---
title: Microsoft Power Apps-portals gebruiken met het gegevensmodel Partij
description: In dit artikel worden de wijzigingen in de webrollen voor Microsoft Power Apps-portals vanwege het partijgegevensmodel in Twee keer wegschrijven beschreven.
author: RamaKrishnamoorthy
ms.date: 03/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-22
ms.openlocfilehash: c2e9d0f47ef90167bf84bb5b20e6a7ad2d58ffd2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898941"
---
# <a name="using-microsoft-power-apps-portals-with-the-party-data-model"></a>Microsoft Power Apps-portals gebruiken met het gegevensmodel Partij

[!INCLUDE[banner](../../includes/banner.md)]



Orkestratieversie 2.0.999.0 en hoger van de oplossing Twee keer wegschrijven omvatten wijzigingen in het gegevensmodel voor partijen en het globale adresboek voor de tabellen Rekening en Contactpersoon. De wijzigingen maken veel-op-veel-relaties mogelijk die geavanceerde bedrijfsscenario's ondersteunen. Deze wijzigingen worden niet ondersteund door portalwebrollen, inclusief de klantportal, die out-of-the-box worden verzonden of die in uw omgeving bestonden voordat u Twee keer wegschrijven installeerde. Om de webrollen te laten werken zoals verwacht, moet u nieuwe webrollen maken met behulp van het nieuwe gegevensmodel. 

Samengevat is de manier waarop de tabellen samenwerken gewijzigd, maar de tabelmachtigingen in de klantportal zijn niet gewijzigd. In dit artikel wordt uitgelegd hoe u nieuwe webrollen maakt die werken met het nieuwe geavanceerde gegevensmodel.

Dit diagram toont de tabelrelatie **zonder** het gegevensmodel voor partijen en het globale adresboek:

   ![zonder partijmodel.](media/without-party-model.PNG)

Dit diagram toont de tabelrelatie **met** het gegevensmodel voor partijen en het globale adresboek:

   ![met partijmodel.](media/with-party-model.png)

## <a name="create-a-new-table-permission"></a>Een nieuwe tabelmachtiging maken

Voer de volgende stappen uit om deze nieuwe tabelmachtigingen te maken:

1. Meld u aan bij [Power Apps](https://make.powerapps.com) en ga naar uw apps.
2. Selecteer uw Portalbeheer-app.
3. Selecteer **Beveiliging > Tabelmachtigingen** in de zijbalk.

    U moet drie nieuwe machtigingen maken:

    + Verbinding van tabel **Contactpersoon** met **Partij**
    + Verbinding van tabel **Partij** met **Rekening**
    + Verbinding van tabel **Rekening** met **Order**

4. Maak met de volgende parameters een nieuwe machtiging voor de verbinding van contactpersoon met partij en sla deze op:

    + **Naam**: verbinding van tabel **Partij** met **Rekening** (of uw keuze)
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
