---
title: Verkooporders verzenden zonder magazijn
description: In dit onderwerp wordt aangegeven hoe u een verkooporder bijwerkt wanneer producten naar de klant zijn verzonden.
author: Henrikan
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 10e21bcdef22caf4f4d97ba7dd36ebf1a6e6e055
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578867"
---
# <a name="ship-sales-orders-without-warehousing"></a>Verkooporders verzenden zonder magazijn

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt aangegeven hoe u een verkooporder bijwerkt wanneer producten naar de klant zijn verzonden. De guide is van toepassing op de vervullingsstroom die niet is ingesteld voor magazijnbeheer (geen basale of geavanceerd magazijnen) en vereist daarom niet dat productorderverzameling vóór zending wordt geregistreerd. U kunt deze procedure uitvoeren met uw eigen gegevens of in het demogegevensbedrijf USMF. In beide gevallen maakt u voordat u deze taak start, een verkooporder voor een voorraadproduct met een hoeveelheid die groter is dan 1. Als u een boekingsfout wilt voorkomen, moet u controleren of de voorhanden hoeveelheid van het product op de site en in het magazijn dat u hebt geselecteerd op de order, de orderhoeveelheid dekt.

## <a name="post-packing-slip-for-an-order"></a>Een pakbon boeken voor een order
1. Ga in het navigatievenster naar **Modules > Verkoop en marketing > Verkooporders > Alle verkooporders**.
2. Zoek en selecteer in de lijst de order die u voor deze taak hebt gemaakt.
3. Selecteer in het actievenster de optie **Verzamelen en inpakken**.
4. Selecteer **Pakbon boeken**.
5. Vouw de sectie **Parameters** uit of samen.
6. Selecteer in het veld **Hoeveelheid** de optie **Alle**.
    - Andere opties zijn **Nu leveren** en **Verzameld**. Als de orderregel gedeeltelijk moet worden verzonden en het veld **Nu leveren** op de orderregel een hoeveelheid bevat, selecteert u **Nu leveren**. Als orderverzameling in de vervullingsstroom van uw organisatie een afzonderlijk proces is dat wordt beheerd door en is geregistreerd met een orderverzamellijst, selecteert u **Verzameld**.  
    - Controleer of de optie **Boeking** op **Ja** is ingesteld.  
7. Stel de optie **Pakbon afdrukken** in op **Ja**. Het tabblad **Overzicht** bevat een lijst met pakbonnen die in deze boeking moeten worden gegenereerd. Als u een afzonderlijk order verzendt, is er meestal één pakbon. Echter, als de regels van die order vanaf verschillende locaties moeten worden verzonden, wordt het boeken automatisch opgesplitst in het juiste aantal documenten. Dit is een verplichte voorwaarde die niet kan worden gewijzigd. Op dezelfde manier wordt de boeking ook in meerdere documenten opgesplitst als de regels van de order naar verschillende afleveradressen moeten worden verzonden. Volgens het verzendbeleid is dan een splitsing vereist.  
8. Selecteer op het tabblad **Regels** de rij voor de orderregel die moet worden verzonden.
9. Voer in het veld **Bijwerken** een cijfer in dat lager is dan de oorspronkelijke hoeveelheid.
10. Selecteer **OK**.
11. Selecteer **Ja**.
12. Sluit de pagina.
13. Selecteer **Opties** in het actievenster.
14. Selecteer **Weergave wijzigen**.
15. Selecteer **Weergave kopteksten**.
    - Als alle regels op de order volledig zijn verzonden, wijzigt de orderstatus van Open naar Geleverd.  
    - In dit voorbeeld is de orderregel gedeeltelijk verzonden. Daarom blijft de orderstatus Open.     
    - Het veld **Documentstatus** is ingesteld op Pakbon omdat minstens een van de orderregels is verzonden.  
16. Selecteer **Algemeen** in het actievenster.
17. Selecteer **Regelhoeveelheid**.
18. Sluit de pagina.
19. Selecteer in het actievenster de optie **Verzamelen en inpakken**.
20. Selecteer **Pakbon**. De pagina **Pakbonjournaal** bevat alle pakbondocumenten die voor uw order zijn gegenereerd. U kunt details van elk document controleren en deze desgewenst afdrukken.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]