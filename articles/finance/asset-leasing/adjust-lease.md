---
title: Leases aanpassen
description: In dit onderwerp wordt uitgelegd hoe u een lease kunt aanpassen. Aanpassingen kunnen nodig zijn als de leasetermijnen worden gewijzigd, de lease wordt verlengd of andere omstandigheden veranderen.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9d1c6e20e72fb2816c32e71e8921a94724ae5656
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4442175"
---
# <a name="adjust-leases"></a>Leases aanpassen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u een lease kunt aanpassen. Aanpassingen kunnen nodig zijn als de leasetermijnen worden gewijzigd, de lease wordt verlengd of andere omstandigheden veranderen. Het leasen van activa voldoet aan de richtlijnen die de Accounting Standards Codification Topic 842 (ASC 842) en International Financial Reporting Standard 16 (IFRS 16) bieden over leasewijzigingen. In ASC 842-20-15-1 wordt een wijziging in de lease gedefinieerd als elke wijziging in de voorwaarden van een contract waardoor een wijziging in de omvang of de interpretatie van de lease wordt veroorzaakt. In IFRS 39 van IFRS 16 wordt aangegeven dat een leasenemer de leaseverplichtingen moet herwaarderen, zodat deze wijzigingen in de leasebetalingen weerspiegelen.

Voor organisaties die zich houden aan ASC 842 of IFRS 16, wordt een lease aangepast om een wijziging in de contante waarde van de toekomstige minimale leasebetalingen (PVFMLP) aan te geven. Als de PVFMLP toeneemt, is de gemaakte journaalpost een debetpost voor het activum met gebruiksrecht en een creditpost voor de leaseverplichtingen om het verschil tussen de nieuwe PVFMLP en de vorige PVFMLP aan te geven. Als de PVFMLP afneemt, is de journaalpost voor het verschil een debetbedrag voor de leaseverplichtingen en een creditbedrag voor het RoU-activum.

Als door de correctie het RoU-activum onder 0 (nul) zakt, wordt het restbedrag bijgeschreven bij de winst op de boekingsrekening voor de leasewijziging die is opgegeven op de pagina **Leaseboekingsrekeningen**. De systeem geeft deze transacties en andere correctieposten weer, zoals classificatiewijzigingen, initiële directe kosten, leasebonussen, vooruitbetalingen en ontmantelingskosten die voortvloeien uit leasewijzigingen.

Voor specifieke richtlijnen voor het aanpassen van leasetransacties, raden we u aan IFRS 16 en ASC 842 te bekijken.

Volg deze stappen om een lease aan te passen: Door de gewijzigde gegevens worden de leaseschema's bijgewerkt nadat het proces Schema maken is uitgevoerd.

1. Ga naar **Activa leasen \> Leases \> Leaseoverzicht**.
2. Selecteer de lease die u wilt aanpassen, op de pagina **Lease-overzicht** en selecteer vervolgens **Lease aanpassen**.
3. Voer op de pagina **Lease aanpassen** de nieuwe gegevens in voor de gecorrigeerde lease.

    Zoals u ziet, is de pagina **Lease aanpassen** vergelijkbaar met de pagina **lease toevoegen**. Zoals de begindatum die u opgeeft wanneer u een lease toevoegt, bepaalt wanneer de nieuwe lease begint, geeft het veld **Wijzigingsdatum** op de pagina **Lease aanpassen** aan wanneer de gewijzigde lease ingaat. Deze datum kan niet na de begindatum op de regels in het betalingsschema vallen.

    > [!NOTE]
    > De velden **Overwegingen voor RoU** zijn van toepassing op de leasecorrectie. Als er geen initiële directe kosten, leasebonussen, vooruitbetalingen of ontmantelingskosten aan de gewijzigde lease worden gekoppeld, moet u deze velden leeg laten. De oorspronkelijke bedragen zijn niet van toepassing op de bijgewerkte lease. Eventuele extra kosten die worden gemaakt wanneer de lease wordt gewijzigd, moeten worden ingevoerd op de pagina **Lease aanpassen**.
    > 
    > Een leaseverstrekker biedt bijvoorbeeld een bonus van USD 1.000 om een leaseverlenging te accepteren. Wanneer u in dit geval de lease aanpast met de verlenging, geeft u **1.000** op in het veld **Leasebonussen**. Als er geen bonussen aan de leasewijziging zijn gekoppeld, wist u de waarden die eerder in dit veld zijn ingevoerd. Dezelfde logica wordt toegepast op andere RoU-overwegingen.

    De betalingsschemaregels van de gecorrigeerde lease moeten op een toekomstige basis worden gemaakt. Betalingsschemaregels die in een toekomstige basis worden gemaakt, kunnen niet worden gestart voordat de wijzigingen in de lease van kracht worden.

    De volgende stappen zijn vrijwel gelijk aan de stappen voor de eerste toerekening van een lease.

4. Selecteer **Schema's maken** om het aangepaste betalingsschema te genereren. U ontvangt een bericht waarin wordt gemeld dat het betalingsschema is gemaakt voor de lease.

    > [!IMPORTANT]
    > Voordat u **Schema's maken** selecteert, moet u controleren of de wijzigingsdatum en de regels van het betalingsschema kloppen. Controleer ook of alle initiële directe kosten, leasebonussen, vooruitbetalingen of ontmantelingskosten alleen overeenkomen met de kosten die voortvloeien uit de correctie.

5. Als u het nieuwe betalingsschema wilt weergeven, selecteert u **Boeken** en opent u de pagina **Betalingsschema**.
6. Op de pagina **Betalingsschema** kunt u de gecorrigeerde betalingsbedragen bewerken voordat u het betalingsschema bevestigt. Selecteer **Schema bevestigen** om de planning te bevestigen.

    Wanneer het betalingsschema is bevestigd, worden de nieuwe schema's voor afschrijving en leaseverplichtingen gemaakt.

7. Als u het nieuwe afschrijvingsschema voor de leaseverplichtingen wilt weergeven dat is gegenereerd op basis van de nieuwe invoer, sluit u de pagina **Betalingsschema** en opent u de pagina **Afschrijvingsschema**.
8. Als u het zojuist gegenereerde afschrijvingsschema voor het activum wilt weergeven, opent u de pagina **Afschrijvingsschema voor activa** via de pagina **Boekdetails**.
9. Als u de correctiejournaalpost wilt genereren, selecteert u **Functie \> Lease aanpassen**. U ontvangt een bericht waarin wordt gemeld dat een correctiejournaalpost is gemaakt. 
10. Selecteer **Journalen \> Activaleasejournaal** om de boeking in journaal weer te geven.
11. Als u de boeking in journaal wilt uitvoeren, selecteert u de regel en vervolgens **Boeken**.

## <a name="view-lease-versions"></a>Leaseversies weergeven

Als een lease is gewijzigd, kunt u de verschillende versies ervan weergeven. U kunt ook de historische schema's en eerdere leasegegevens weergeven.

1. Selecteer op de pagina **Leaseoverzicht** de lease en vervolgens in het actievenster **Historie van leaseversie**.

    Als de geselecteerde lease is aangepast, worden op de pagina **Historie van leaseversie** de verschillende versies weergegeven. De oorspronkelijke lease wordt aangeduid met **1** en de volgende versies hebben een oplopende numerieke volgorde.

    Voor een geselecteerde leaseversie kunt u de financiële dimensies, contractgegevens, locatie en betalingsschemaregels weergeven.

2. Als u historische planningen wilt weergeven, opent u de gewijzigde lease op de pagina **Leaseoverzicht**, selecteert u het gewenste boek en vervolgens in het actievenster **Historie van boekversie**.
3. Selecteer op de pagina **Historie van boekversie** de gewenste versie en het gewenste schema.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]