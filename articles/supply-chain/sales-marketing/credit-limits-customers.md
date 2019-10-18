---
title: Kredietlimieten voor klanten
description: Dit artikel geeft een overzicht van de werking van kredietlimieten in Dynamics 365 Supply Chain Management.
author: omulvad
manager: AnnBe
ms.date: 09/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7be4ab297293bf1c9f720c2c16b2720afdfe771
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/24/2019
ms.locfileid: "2026458"
---
# <a name="credit-limits-for-customers"></a>Kredietlimieten voor klanten

[!include [banner](../includes/banner.md)]

Als u een kredietlimiet instelt, kunt u opgeven hoeveel krediet u maximaal voor uw klanten toestaat. Als er een kredietlimiet is opgegeven, wordt deze automatisch gecontroleerd wanneer een gebruiker een document probeert bij te werken. Als de kredietlimiet is overschreden, wordt er een bericht weergegeven voor de gebruiker. Dit artikel biedt een overzicht van de werking van kredietlimieten en beantwoordt de volgende vragen:

-   Voor welke documenten en processen kan ik kredietlimieten controleren?

-   Waar kan ik de manier configureren waarop het resterende krediet van de klant wordt berekend?

-   Waar vindt u informatie over het resterende krediet van een klant?

-   Waar geef ik op of identificatie is vereist voor om meer krediet aan een klant te verstrekken en om de kredietlimiet te verhogen die identificatie vereist?

-   Waar kan ik opgeven of een waarschuwing of fout wordt weergegeven als de kredietlimiet is overschreden?

-   Hoe geef ik de kredietlimiet voor een bepaalde klant op?

-   Hoe controleer ik kredietlimieten handmatig op verkooporders?

**Voor welke documenten en processen kan ik kredietlimieten controleren?**

Gebruik het formulier **Parameters van module Klanten** om op te geven voor welke documenten u kredietlimieten wilt controleren. U moet lid zijn van de beveiligingsrol Systeembeheerder (-SYSADMIN-) om wijzigingen aan te brengen in dit formulier. U kunt de kredietlimieten van de volgende documenten en processen controleren:

-   Facturen voor verkooporders, wanneer u de facturen boekt

-   Pakbonnen voor verkooporders, wanneer u pakbonnen bijwerkt

-   Verkooporders, bij het toevoegen van regels in het formulier **Verkooporder**

-   Verkooporders, wanneer ze worden gemaakt via een service

-   Vrije-tekstfacturen, wanneer u de facturen boekt

Kredietlimieten worden automatisch gecontroleerd als een van de volgende opties is ingesteld:

-   In het formulier **Parameters van module Klanten** is het veld **Kredietlimiettype** ingesteld op iets anders dan **Geen**. Kredietlimieten worden gecontroleerd voor alle klanten.

-   In het formulier **Parameters van module Klanten** is het veld **kredietlimiettype** ingesteld op **Geen**, maar **Verplichte kredietlimiet** is ingeschakeld voor een klant in het formulier **Klanten**. Kredietlimieten worden alleen voor bepaalde klanten gecontroleerd.

Om de kredietlimieten van de volgende documenten te controleren, moet u extra instellingen opgeven.

|    Document                                    |    Aanvullende instelling                                                                                                             |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|    Vrije-tekstfactuur                         |    Selecteer in het formulier Parameters van module Klanten in het gedeelte Creditnotering de optie Kredietlimiet controleren op vrije-tekstfactuur.     |
|    Verkooporder (handmatig ingevoerd)            |    Selecteer in het formulier Parameters van module Klanten in het gedeelte Creditnotering de optie Kredietlimiet op verkooporder controleren.           |
|    Verkooporder (elektronisch ontvangen)     |    Selecteer in het formulier Parameters van module Klanten in het gedeelte AIF de optie Kredietlimiet voor verkooporders controleren.                     |

**Waar kan ik de manier configureren waarop het resterende krediet van de klant wordt berekend?**

U kunt Dynamics 365 configureren om het resterende krediet van een klant op een van de volgende manieren te berekenen:

-   Vergelijk de kredietlimiet met het klantsaldo.

-   Vergelijk de kredietlimiet met het saldo van de klant en de pakbonbedragen.

-   Vergelijk de kredietlimiet met het saldo van de klant en alle opende transactieactiviteit. Dit omvat onder andere bedragen op de pakbon en bedragen op de verkooporder.

Gebruik het formulier **Parameters van module Klanten** om de vergelijkingsinformatie op te geven. U moet lid zijn van de beveiligingsrol Systeembeheerder (-SYSADMIN-) om wijzigingen aan te brengen in dit formulier. Selecteer in het veld **Kredietlimiettype** of kredietlimietcontroles moeten worden uitgevoerd en welke transactie-informatie u wilt opnemen wanneer de kredietlimiet wordt gecontroleerd. Selecteer een van de volgende opties:

-   **Geen**: kredietlimieten niet controleren. U kunt deze optie overschrijven voor een bepaalde klant door het selectievakje **Verplichte kredietlimiet** in het formulier **Klanten** in te schakelen. Als u dit doet, wordt de kredietlimiet vergeleken met het klantsaldo.

-   **Saldo**: de kredietlimiet wordt gecontroleerd op basis van het saldo van de klant.

-   **Saldo+Pakbon of productontvangstbon**: de kredietlimiet wordt vergeleken met het saldo van de klant en de leveringen.

-   **Saldo+Alle**: de kredietlimiet wordt vergeleken met het saldo, de leveringen en de openstaande orders van de klant.

**Waar vindt u informatie over het resterende krediet van een klant?**

Informatie over het saldo en het resterende kredietbedrag van de klant wordt berekend en opgeslagen wanneer u een ouderdomsmomentopname maakt, en wordt weergegeven in het formulier **Aanmaningen**. De bedragen in het formulier **Aanmaningen** bevatten mogelijk niet alle transactieactiviteiten totdat een nieuwe ouderdomsmomentopname wordt gemaakt. Zie [Aanmaningen en crediteringen in Klanten](https://technet.microsoft.com/library/hh209221.aspx) voor meer informatie.

Informatie over het saldo en het resterende kredietbedrag van de klant wordt afhankelijk van de geselecteerde documenten berekend wanneer verkooporders, pakbonnen en klantfacturen worden bijgewerkt. Als het bedrag van het document waarin u werkt de kredietlimiet overschrijdt, wordt een bericht weergegeven.

**Waar geef ik op of identificatie is vereist voor om meer krediet aan een klant te verstrekken en om de kredietlimiet te verhogen die identificatie vereist?**

Gebruik het formulier **Parameters van module Klanten** om op te geven of identificatie vereist is en om het bedrag van de kredietlimiet op te geven waarvoor identificatie vereist is.
U moet lid zijn van de beveiligingsrol Systeembeheerder (-SYSADMIN-) om wijzigingen aan te brengen in dit formulier.

|    Veld                                    |    Omschrijving                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    Identificatie bij krediet vereist     |    Selecteer het type identificatie dat moet worden ingevoerd voor klanten waaraan uw rechtspersoon krediet heeft verleend. De optie die u in dit veld selecteert, bepaalt wanneer welk type gegevens moet worden ingevoerd in de velden Overheidsidentificatie in het formulier Klanten:        Nee: er is geen overheidsidentificatie nodig, ongeacht de kredietlimiet van de klant.     Ja: er is een door de overheid uitgegeven licentienummer of een andere overheidsidentificatie nodig als de kredietlimiet van de klant hoger dan of gelijk is aan nul.     Ondergrens: er is een door de overheid uitgegeven licentienummer of een andere overheidsidentificatie nodig als de kredietlimiet van de klant hoger dan of gelijk is aan de limiet die u in het veld Grenswaarde op dit formulier hebt opgegeven.        |
|    Grenswaarde                                    |    Geef de kredietlimiet op waarvoor klanten een overheidslicentienummer of een overheidsidentificatie nodig hebben.    Typ bijvoorbeeld 2000 als u wilt dat klanten vanaf deze limiet een legitimatiebewijs moeten kunnen overleggen, zoals een rijbewijs. Voor klanten met een kredietlimiet van 2000 euro of hoger moet de klant zijn rijbewijsnummer opgeven.    Dit veld is beschikbaar als u Ondergrens hebt geselecteerd in het veld Identificatie bij krediet vereist.                                                                                                                                                                                                                                                                                                                                                                                                                                         |

**Waar kan ik opgeven of een waarschuwing of fout wordt weergegeven als de kredietlimiet is overschreden?**

Gebruik het formulier **Parameters van module Klanten** om op te geven of een waarschuwing of fout wordt weergegeven als de kredietlimiet is overschreden. Deze waarschuwing of fout wordt weergegeven wanneer een gebruiker informatie invoert of boekt, of wordt opgenomen in een logbestand als de documenten worden verwerkt door een elektronische service. U moet lid zijn van de beveiligingsrol Systeembeheerder (-SYSADMIN-) om wijzigingen aan te brengen in dit formulier.

|    Veld                                                               |    Omschrijving                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    Bericht bij overschrijding van de kredietlimiet (in het gebied Creditnotering)     |    Selecteer hoe meldingen met betrekking tot het overschrijden van de kredietlimiet worden weergegeven aan gebruikers. Selecteer een van de volgende opties:        Fout: er wordt een foutbericht weergegeven. Hierdoor wordt de huidige bewerking meestal gestopt en moet het conflict worden opgelost voordat het proces kan doorgaan.     Waarschuwing: er wordt een waarschuwingsbericht weergegeven, maar het proces kan verder worden uitgevoerd.                     |
|    Bericht bij overschrijding van de kredietlimiet (in het gebied AIF)               |    Selecteer hoe meldingen met betrekking tot het overschrijden van de kredietlimiet in een logbestand worden opgenomen. Selecteer een van de volgende opties:        Fout: er wordt een foutbericht weergegeven in het formulier Uitzonderingen en het document wordt niet verwerkt totdat de fout is opgelost.     Waarschuwing: er wordt een waarschuwingsbericht weergegeven in het formulier Uitzonderingen, maar het proces kan verder worden uitgevoerd.        |

**Hoe geef ik het kredietlimietbedrag voor een bepaalde klant op?**

Gebruik het formulier **Klanten** om het bedrag van de kredietlimiet op te geven voor een bepaalde klant. U moet lid zijn van een beveiligingsrol met de taak Klantmodel onderhouden (CustCustomersMaintain) toegewezen om wijzigingen aan te brengen in dit formulier.

1.  Klik op **Klanten** \> **Algemeen** \> **Klanten** \> **Alle klanten**. Dubbelklik op een klantrekening.

2.  Klik in het formulier **Klanten** in het actievenster op **Bewerken**.

3.  Voer een valutabedrag in het veld **Kredietlimiet** in. Deze waarde moet hoger zijn dan nul (0) en deze wordt gebruikt als kredietlimietbedrag.

4.  Voer indien nodig het licentienummer of een andere overheidsidentificatie in het veld **Overheidsidentificatie** in.

> [!NOTE]
> In het formulier **Parameters van module Klanten** is doorgaans een kredietlimiettype geselecteerd. Als het type kredietlimiet echter is ingesteld op **Geen**, moet u ook het selectievakje **Verplichte kredietlimiet** in het formulier **Klanten** inschakelen zodat u de kredietlimiet van de klant kunt vergelijken met het saldo van de klant. Zie 'Voor welke documenten en processen kan ik kredietlimieten controleren?' in dit onderwerp voor meer informatie over kredietlimiettypes. 

**Hoe controleer ik kredietlimieten handmatig op verkooporders?**

Soms moet u de kredietlimiet van de klant handmatig controleren. U zou bijvoorbeeld de kredietlimiet van de klant handmatig kunnen controleren voordat u een verkooporder invoert. U kunt het formulier **Verkooporder** gebruiken om kredietlimieten handmatig te controleren. U moet lid zijn van een beveiligingsrol met de taak Verkooporder onderhouden (SalesOrderMaintain) toegewezen om wijzigingen aan te brengen in dit formulier.

1.  Klik op **Verkoop en marketing** \> **Algemeen** \> **Verkooporders** \> **Alle verkooporders**. Dubbelklik op een verkooporder.

2.  Klik in het formulier **Verkooporder** in het actievenster op het tabblad **Beheren** op **Kredietlimiet controleren**.
