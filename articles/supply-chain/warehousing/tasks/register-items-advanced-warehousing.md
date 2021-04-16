---
title: Artikelen registreren voor een artikel waarvoor geavanceerd magazijnbeheer mogelijk is met een artikelontvangstjournaal
description: In dit onderwerp wordt een scenario gepresenteerd dat laat zien hoe u artikelen registreert via het artikelontvangstjournaal wanneer u de geavanceerde magazijnbeheerprocessen gebruikt.
author: ShylaThompson
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c58aa1cec6c0bfe33fa1ef90267dcd8ac1218157
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830829"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a>Artikelen registreren voor een artikel waarvoor geavanceerd magazijnbeheer mogelijk is met een artikelontvangstjournaal

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt een scenario gepresenteerd dat laat zien hoe u artikelen registreert via het artikelontvangstjournaal wanneer u de geavanceerde magazijnbeheerprocessen gebruikt. Dit wordt gewoonlijk uitgevoerd door een ontvangstadministrateur.

## <a name="enable-sample-data"></a>Voorbeeldgegevens inschakelen

Als u dit scenario wilt doorwerken met behulp van de voorbeeldrecords en -waarden die in dit onderwerp zijn opgegeven, moet u een systeem gebruiken waarbij de standaarddemogegevens zijn geïnstalleerd en moet u de rechtspersoon *USMF* selecteren voordat u begint.

U kunt in plaats daarvan dit scenario doorwerken door waarden uit uw eigen gegevens te vervangen op voorwaarde dat u over de volgende gegevens beschikt:

- U moet een bevestigde inkooporder hebben met een openstaande inkooporderregel.
- Het artikel op de regel moet worden opgeslagen in voorraad. Het mag geen productvarianten gebruiken en mag geen traceringsdimensies hebben.
- Het artikel moet zijn gekoppeld aan een opslagdimensiegroep waarvoor het magazijnbeheerproces is ingeschakeld.
- Het magazijn dat wordt gebruikt, moet zijn ingeschakeld voor magazijnbeheerprocessen en de locatie die u voor het ontvangen gebruikt, moet worden gecontroleerd op nummerplaat.

## <a name="create-an-item-arrival-journal-header-that-uses-warehouse-management"></a>Een koptekst voor het artikelontvangstjournaal maken die gebruikmaakt van magazijnbeheer

Het volgende scenario laat zien hoe u een koptekst van een artikelontvangstjournaal maakt die magazijnbeheer gebruikt:

1. Controleer of uw systeem een bevestigde inkooporder bevat die voldoet aan de vereisten uit de vorige sectie. In dit scenario wordt een inkooporder gebruikt voor bedrijf *USMF*, leverancierrekening *1001*, magazijn *51*, met een orderregel voor *10 PL* (10 pallets) van artikelnummer *M9200*.
1. Noteer het nummer van de inkooporder die u gaat gebruiken.
1. Ga naar **Voorraadbeheer \> Journaalposten \> Artikelontvangst \> Artikelontvangst**.
1. Selecteer **Nieuw** in het actievenster.
1. Het dialoogvenster **Magazijnbeheerjournaal maken** wordt geopend. Selecteer een journaalnaam in het veld **Naam**.
    - Als u voorbeeldgegevens van *USMF* gebruikt, selecteert u *WHS*.
    - Als u uw eigen gegevens gebruikt, moet voor het journaal dat u kiest **Orderverzamellocatie controleren** worden ingesteld op *Nee* en **Quarantainebeheer** op *Nee*.
1. Stel **Verwijzing** in op *Inkooporder*.
1. Stel **Rekeningnummer** in op *1001*.
1. Stel **Nummer** in op het nummer van de inkooporder die u voor deze oefening hebt geïdentificeerd.

    ![Artikelontvangstjournaal](../media/item-arrival-journal-header.png "Artikelontvangstjournaal")

1. Selecteer **OK** om de journaalkop te maken.
1. Selecteer in de sectie **Journaalregels** de optie **Regels toevoegen** en voer de volgende gegevens in:
    - **Artikelnummer**: stel in op *M9200*. De opties **Site**, **Magazijn** en **Hoeveelheid** worden ingesteld op basis van de voorraadtransactiegegevens voor de 10 pallets (1000 artikelen).
    - **Locatie**: stel in op *001*. Deze specifieke locatie houdt geen nummerplaten bij.

    ![Artikelontvangstjournaalregel](../media/item-arrival-journal-line.png "Artikelontvangstjournaalregel")

    > [!NOTE]
    > Het veld **Datum** bepaalt de datum waarop de voorhanden hoeveelheid van het artikel in de voorraad wordt geregistreerd.  
    >
    > De **partij-id** wordt door het systeem ingevuld als deze uniek kan worden geïdentificeerd uit de opgegeven informatie. Anders moet u deze handmatig invoeren. Dit is een vereist veld, dat deze registratie aan een specifieke brondocumentregel koppelt.  

1. Selecteer **Valideren** in het actievenster. Dit controleert of het journaal gereed is om te worden geboekt. Als validatie mislukt, kunt u de fouten bevestigen voordat u het journaal kunt boeken.  
1. Het dialoogvenster **Journaal controleren** wordt geopend. Selecteer **OK**.
1. Controleer de berichtenbalk. Er zou een bericht moeten zijn dat aangeeft dat de bewerking is voltooid.  
1. Selecteer **Boeken** in het actievenster.
1. Het dialoogvenster **Journaal boeken** wordt geopend. Selecteer **OK**.
1. Controleer de berichtenbalk. Er zouden berichten moeten zijn die aangeven dat de bewerking is voltooid.
1. Selecteer **Functies > Productontvangstbon** in het actievenster om de inkooporderregel bij te werken en een productontvangstbon te boeken.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
