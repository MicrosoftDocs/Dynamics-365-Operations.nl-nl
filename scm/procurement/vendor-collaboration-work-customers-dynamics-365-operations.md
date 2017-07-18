---
title: Leverancierssamenwerking met klanten
description: In dit onderwerp wordt beschreven hoe u leverancierssamenwerking in Finance and Operations kunt gebruiken om met inkooporders te werken en consignatievoorraad te bewaken.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ConsignmentProductReceiptLines, ConsignmentVendorPortalOnHand, PurchVendorPortalConfirmedOrders, PurchVendorPortalOriginalOrder, PurchVendorPortalResponsesHistoryList, PurchVendorPortalResponsesPart
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221234
ms.assetid: 6e69fb8b-6d3a-46ef-88cf-6d01212aa7c3
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 41436dab710a5fee0fe0800dff1ebefefa841afc
ms.contentlocale: nl-nl
ms.lasthandoff: 06/13/2017

---

# <a name="vendor-collaboration-with-customers"></a>Leverancierssamenwerking met klanten

[!include[banner](../includes/banner.md)]


In dit onderwerp wordt beschreven hoe u leverancierssamenwerking in Finance and Operations kunt gebruiken om met inkooporders te werken en consignatievoorraad te bewaken.

In dit onderwerp wordt beschreven hoe u leverancierssamenwerking kunt gebruiken om met klanten te werken in Microsoft Dynamics 365 for Finance and Operations. Hier wordt aangegeven hoe u inkooporders controleert en hierop reageert, en hoe u consignatievoorraad controleert. Het is ook mogelijk om leverancierssamenwerking te gebruiken om met facturen te werken. Zie [Werkgebied voor samenwerkingsfacturering van leveranciers](/dynamics365/unified-operations/financials/accounts-payable/vendor-portal-invoicing-workspace) voor meer informatie.

## <a name="working-with-purchase-orders"></a>Werken met inkooporders
In de werkruimte **Inkooporderbevestiging** kunt u reageren op de inkooporders die ter beoordeling naar u zijn verzonden. Daarnaast kunt u informatie weergeven over inkooporders die wachten op actie van de klant en inkooporders die zijn bevestigd, maar nog openstaan. Er zijn drie lijsten in de werkruimte **Inkooporderbevestiging**:

-   **Inkooporders ter beoordeling:** Deze lijst bevat inkooporders die aan u zijn verzonden en op een reactie van u wachten. Als u reageert, verdwijnt de inkooporder uit de lijst. Als de klant u een nieuwe versie van de inkooporder stuurt voordat u de vorige hebt beantwoord, wordt alleen de laatste versie weergegeven.
-   **In afwachting van actie van klant** - In deze lijst kunt u inkooporders bekijken waarop u hebt gereageerd, maar die nog niet door de klant zijn bevestigd. Als u de inkooporder hebt geaccepteerd, kunt u deze in deze lijst blijven controleren totdat de status in **Bevestigd** wordt gewijzigd. Als u de inkooporder hebt afgewezen of met wijzigingen hebt geaccepteerd, kunt u de inkooporder hier controleren tot de klant een nieuwe versie stuurt.
-   **Bevestigde inkooporders openen** - Deze lijst bevat alle inkooporders voor uw rekening die de status **Bevestigd** hebben. Wanneer IO-producten of -services volledig zijn ontvangen, verdwijnt de inkooporder uit de lijst.

In de volgende lijst worden de vier pagina's weergegeven die u kunt gebruiken om met inkooporders te werken. Twee van deze pagina's bevatten dezelfde informatie als de lijsten in de werkruimte:

-   **Inkooporders ter beoordeling** (zie hierboven)
-   **Historie van leveranciersbevestigingen van inkooporders** - Deze pagina bevat alle inkooporders en alle versies van inkooporders die naar de leverancier zijn verzonden en alle geretourneerde antwoorden van de leverancier.
-   **Bevestigde inkooporders openen** (zie hierboven)
-   **Alle bevestigde inkooporders** - Deze pagina bevat alle inkooporders die zijn bevestigd, inclusief de inkooporders waarvoor producten of services zijn ontvangen. U kunt deze lijst gebruiken om te controleren voor welke inkooporders u facturen kunt verzenden.

### <a name="responding-to-purchase-orders"></a>Reageren op inkooporders

De inkooporders die de klant ter beoordeling aan u stuurt, zijn alleen in de werkruimte **Inkooporderbevestiging** en op de pagina **Inkooporders ter beoordeling** zichtbaar. Als u een inkooporder opent, kunt u deze accepteren, afwijzen of accepteren met wijzigingen. De koptekst en/of afzonderlijke regels van de inkooporder kunnen bijlagen bevatten. Het is ook mogelijk voor u om informatie aan uw reactie toe te voegen, aan de koptekst of aan afzonderlijke regels. U kunt bijvoorbeeld een vervangingsitem voor een van de regels voorstellen. U kunt de inkooporder als PDF-bestand bekijken en afdrukken met de optie **Voorbeeld/afdrukken**. U kunt de volgende dimensiekolommen verbergen of weergeven met de actie **Dimensies weergeven**: Locatie, Magazijn, Kleur, Grootte, Stijl, Configuratie. Als u de optie **Accepteren met wijzigingen** gebruikt, kunt u afzonderlijke regels accepteren of afwijzen. U kunt ook de volgende wijzigingen aanbrengen aan regels:

-   Wijzig datums of hoeveelheden. Als u de bevestigde leveringsdatum op alle regels wilt bijwerken, gebruikt u de optie **Leveringsdatums bijwerken** voor de IO-koptekst.
-   Splits regels op voor verschillende leveringsdatums of -hoeveelheden.
-   Vervang een item. Voer hiervoor een itembeschrijving en uw itemnummer in het veld **Extern** in het gedeelte **Regeldetails** in.

U kunt prijsgegevens of toeslagen niet wijzigen, maar u kunt met notities wel suggesties voor wijzigingen geven. Als u van uw klant een nieuwe versie van een inkooporder ontvangt, bevat deze een versieachtervoegsel om aan te geven dat het om een gewijzigde versie van een inkooporder gaat die eerder is doorgegeven. Op de pagina **Historie van leveranciersbevestigingen van inkooporders** kunt u de historie van elke order volgen.

## <a name="monitoring-consignment-inventory"></a>Consignatievoorraad bewaken
Als u consignatievoorraad gebruikt, kunt u de interface voor leverancierssamenwerking gebruiken om informatie op de volgende pagina's te bekijken:

-   **Inkooporders die consignatievoorraad verbruiken:** Inkooporders voor consignatievoorraad worden gegenereerd wanneer de klant de voorraad in eigendom krijgt. Deze consignatie-inkooporders worden alleen weergegeven op de pagina **Inkooporders die consignatievoorraad verbruiken**. Ze worden niet opgenomen op de pagina **Alle bevestigde inkooporders**.
-   **Producten ontvangen uit consignatievoorraad** - Deze pagina bevat een overzicht van alle transacties waarvan het eigendom van producten is overgedragen aan het bedrijf dat de voorraad verbruikt. U kunt deze informatie gebruiken om de klant te factureren.
-   **Voorhanden consignatievoorraad** - Op deze pagina wordt de voorhanden consignatievoorraad weergegeven die het eigendom is van uw bedrijf en voorhanden is in het magazijn van de klant.


<a name="see-also"></a>Zie ook
--------

[Gebruikers van leverancierssamenwerking beheren](manage-vendor-collaboration-users.md)




