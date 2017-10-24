---
title: Overzicht van Personeelsbeheer
description: In dit onderwerp wordt beschreven hoe u de service Personeelsbeheer gebruikt om te profiteren van de vertrouwde POS-clients Modern POS en Cloud POS, zodat winkelmanagers hun personeel gemakkelijk kunnen beheren.
author: shalabhjainmsft
manager: AnnBe
ms.date: 7/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Core
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-07-30
ms.dyn365.ops.version: Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d67ad79c068651f32ce7dc776bc460698557bc29
ms.openlocfilehash: f747dce6b9595de50297cb5af7db523d5f26a844
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="workforce-management-overview"></a>Overzicht van Personeelsbeheer

[!include[banner](includes/banner.md)]
    
Met de service Personeelsbeheer profiteren winkelmanagers van de vertrouwde POS-clients Modern POS en Cloud POS om hun personeel gemakkelijk te kunnen beheren. De service Personeelsbeheer gebruikt het uitbreidingsframework voor het downloaden van de relevante pakketten in het POS-systeem. Deze pakketten worden gedownload wanneer het POS-systeem wordt gesloten en opnieuw wordt geopend. Dus wanneer Microsoft nieuwe functies uitbrengt voor Personeelsbeheer, moet de POS-app worden gesloten en opnieuw worden geopend.

Met deze service kunnen winkelmanagers eenvoudig wekelijkse werkschema's maken en publiceren voor hun winkels. Winkelmedewerkers kunnen hun eigen schema's en de schema's van hun collega' vervolgens snel bekijken. Op die manier kunnen ze zien met wie ze werken tijdens de toegewezen diensten. Winkelpersoneel kan ook verzuimaanvragen, verzoeken om diensten te ruilen en dienstaanbiedingen maken. Al deze aanvragen activeren een gedefinieerde workflow.

Tijdens een dienst kunnen winkelmedewerkers profiteren van de functie voor inklokken en uitklokken die is ingebouwd in de POS-clients. De gegevens worden vervolgens verzonden naar het hoofdkantoor voor loonadministratie. De functie voor in- en uitklokken is een bestaande functie van het POS-systeem. Zie [Inklokken en uitklokken](retail-time-attendance.md) voor meer informatie over het instellen en ondersteunde scenario's.

## <a name="supported-scenarios"></a>Ondersteunde scenario's
Deze sectie bevat meer informatie over de ondersteunde scenario's.

- **Schema's maken en publiceren**: de service Personeelsbeheer gebruikt de POS-machtigingen die zijn geconfigureerd in het hoofdkantoor om te bepalen of een werknemer over de bevoegdheden van een winkelmanager beschikt. Alleen winkelmanagers kunnen schema's maken en publiceren met de bewerking Beheer plannen. Ze kunnen snel een schema maken door een bestaande dienst van één werknemer naar een andere werknemer te kopiëren. Ze kunnen ook een schema maken door het schema van een vorige week te importeren naar de huidige week.

    Als een schema niet is gepubliceerd, heeft deze de conceptstatus en ziet deze er anders uit dan een gepubliceerd schema. Winkelmanagers kunnen een schema publiceren door te klikken op de knop **Publiceren** voor een week. Nadat het schema voor een week is gepubliceerd, worden eventuele wijzigingen automatisch gepubliceerd. Voorbeelden van wijzigingen zijn toevoegingen of verwijderingen van diensten of verzuim, of bewerkingen van diensten of verzuim. Winkelmedewerkers kunnen alleen de schema's weergeven die zijn gepubliceerd voor verschillende weken.
    
- **Aanvragen maken en goedkeuren**: winkelmedewerkers kunnen drie soorten aanvragen maken:

    - Verzuimaanvraag
    - Verzoek om diensten te ruilen
    - Diensten aanbieden

    Deze aanvragen kunnen worden gemaakt met de bewerking Aanvragen plannen. Elke aanvraag volgt een gedefinieerde workflow en werknemers kunnen eenvoudig de huidige status van hun aanvragen bekijken.
    
    Verzuimaanvragen worden ter goedkeuring automatisch naar de winkelmanager verzonden. Als er meerdere winkelmanagers zijn, kunnen alle managers een bepaalde aanvraag bekijken, maar kan slechts één manager de aanvraag goedkeuren of afwijzen. De verzuimtypen worden geconfigureerd in het hoofdkantoor van de detailhandel via de pagina **Typen verlof en verzuim** in de module **Detailhandel**. Als de winkelmanager een aanvraag goedkeurt of afwijst, wordt deze verplaatst naar het tabblad **Historie** voor de bewerking Aanvragen plannen.
    
    Een verzoek om een dienst te ruilen of aan te bieden, gaat eerst naar de werknemer aan wie het verzoek is gericht. De winkelmanager kan de aanvraag pas weergeven nadat de werknemer deze heeft goedgekeurd. Als de werknemer het verzoek om een dienst te ruilen of aan te bieden afwijst, kan de manager het verzoek niet bekijken. De werknemer die de aanvraag heeft gemaakt, kan de aanvraag ook annuleren voordat de manager deze goedkeurt of afwijst.

- **De actieve winkelmedewerkers weergeven in de schemaweergave**: wanneer een werknemer wordt toegevoegd aan een winkel, bijvoorbeeld door hem of haar te koppelen aan het werknemersadresboek van de winkel, wordt de werknemer beschikbaar voor planning in de service Personeelsbeheer. Een terugkerende batchtaak met de naam **Gegevens van medewerker verwerken voor personeelsbeheer** wordt uitgevoerd in het hoofdkantoor. Met deze taak worden koppelingen tussen winkel en werknemers voorbereid die naar Common Data Service (CDS) worden verzonden.

    Hetzelfde proces wordt gebruikt wanneer een werknemer wordt verwijderd uit een winkel. De werknemer die wordt verwijderd, wordt echter nog wel weergegeven voor eerdere, huidige en toekomstige weken als er een actieve dienst of een actief verzuim is toegewezen aan die werknemer. Tenzij deze diensten en dit verzuim worden verwijderd, wordt de verwijderde werknemer nog wel weergegeven voor deze weken.

