---
title: Aanbevolen procedures voor het importeren van boekstukken die met behulp van de entiteit algemeen journaal
description: Dit onderwerp bevat tips voor het importeren van gegevens in het algemene journaal met behulp van het algemene journaal entiteit.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 94363
ms.assetid: 0b8149b5-32c5-4518-9ebd-09c9fd7f4cfc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 81a52acd1d9baa12fcfe9d848441901894fa5682
ms.lasthandoff: 03/31/2017


---

# <a name="best-practices-for-importing-vouchers-using-the-general-journal-entity"></a>Aanbevolen procedures voor het importeren van boekstukken die met behulp van de entiteit algemeen journaal

Dit onderwerp bevat tips voor het importeren van gegevens in het algemene journaal met behulp van het algemene journaal entiteit.  

U kunt de grootboek-entiteit importeren boekstukken die een rekening of tegenrekening rekeningtype **grootboek, klant, leverancier of Bank**. Het boekstuk kan worden ingevoerd als één regel, waarbij zowel **rekening** veld en de **tegenrekening** veld, of als een opmaak over meerdere regels van het boekstuk, waarbij er nog maar de **rekening** veld wordt gebruikt (en de **tegenrekening** leeg op elke regel). Het algemene journaal entiteit ondersteunt niet elk rekeningtype. In plaats daarvan bestaan andere entiteiten voor scenario's waarin verschillende combinaties van de rekeningtypen vereist zijn. Bijvoorbeeld voor het importeren van een projecttransactie de entiteit project onkosten journaal gebruiken. Elke entiteit is ontworpen ter ondersteuning van specifieke scenario's, wat betekent dat extra velden zijn mogelijk beschikbaar in entiteiten voor de scenario's, maar niet in de entiteiten voor een ander scenario.

## <a name="setup"></a>Instellen
Voordat u importeert met behulp van de entiteit algemeen journaal, Controleer de volgende instellingen:

-   **instellingen van de nummerreeks voor het journaalbatchnummer** - standaard wanneer u importeert met behulp van het algemene journaal entiteit, het journaal batch nummer gebruikt de nummerreeks die is gedefinieerd in de grootboekparameters. Als u de nummerreeks voor het journaalbatchnummer instelt op **Handmatig**, wordt geen standaardnummer toegepast. Deze instelling wordt niet ondersteund.
-   **Configuratie van de financiële dimensie** -elke organisatie moet de volgorde van financiële dimensies definiëren wanneer entiteiten worden gebruikt voor het importeren van transacties. De order is gedefinieerd voor de **integratie van grootboek dimensies** indeling, op **grootboek**&gt;**rekeningschema**&gt;**dimensies**&gt;**configuratie van de financiële dimensie voor de integratie van toepassingen**&gt;**gegevensentiteiten selecteren**. De segmenten van de grootboekrekening die is geïmporteerd, moeten dezelfde volgorde hebben. Anders treedt een fout op tijdens het importeren.

## <a name="general-journal-entity-setup"></a>Entiteit Algemeen journaal instellen
Twee instellingen in gegevensbeheer beïnvloeden hoe de standaard-journaalbatchnummer of boekstuknummer wordt toegepast:

-   **Verwerking op basis van een set** (voor de gegevensentiteit)
-   **Automatisch gegenereerde** (op het veldtoewijzing)

In de volgende secties wordt het effect van deze instellingen beschreven en wordt tevens uitgelegd hoejournaalbatchnummers en boekstuknummers worden gegenereerd.

### <a name="journal-batch-number"></a>Batchnummer journaal

-   De instelling **Op sets gebaseerde verwerking** in de entiteit Algemeen journaal heeft geen invloed op de manier waarop journaalbatchnummers worden gegenereerd.
-   Als het veld **Journaalbatchnummer** is ingesteld op **Automatisch gegenereerd**, wordt een nieuw journaalbatchnummer gemaakt voor elke regel die wordt geïmporteerd. Dit gedrag wordt niet aanbevolen. De instelling **Automatisch gegenereerd** is te vinden in het importproject, onder **Kaart weergeven**op het tabblad **Gegevens toewijzen**.
-   Als het veld **Journaalbatchnummer** niet is ingesteld op **Automatisch gegenereerd**, wordt het journaalbatchnummer als volgt gemaakt:
    -   Als het batchnummer van het journaal dat is gedefinieerd in het geïmporteerde bestand overeenkomt met een bestaande, niet-geboekte dagelijks journaal in Microsoft Dynamics 365 voor bewerkingen, worden alle regels met een overeenkomende journaalbatchnummer geïmporteerd in bestaand journaal. Regels worden nooit in een geboekt journaalbatchnummer geïmporteerd. In plaats daarvan wordt er een nieuw nummer gemaakt.
    -   Als het batchnummer van het journaal dat is gedefinieerd in het geïmporteerde bestand komt niet overeen met een bestaande, niet-geboekte dagelijks journaal in Dynamics 365 voor bewerkingen, worden alle regels met dezelfde journaalbatchnummer gegroepeerd op een nieuw journaal. Zo worden bijvoorbeeld alle regels met een journaalbatchnummer van 1 geïmporteerd in een nieuw journaal en worden alle regels met een journaalbatchnummer van 2 geïmporteerd in een tweede nieuw journaal. Het journaalbatchnummer wordt gemaakt met behulp van de nummerreeks die is gedefinieerd in de grootboekparameters.

### <a name="voucher-number"></a>Boekstuknummer

-   Als u de instelling **Op sets gebaseerde verwerking** gebruikt in de entiteit Algemeen journaal, moet het boekstuknummer worden opgegeven in het geïmporteerde bestand. Aan elke transactie in het algemeen journaal wordt het boekstuknummer toegewezen dat is verstrekt in het geïmporteerde bestand, zelfs als het boekstuk niet in evenwicht is. Als u wilt gebruiken op basis van een set verwerking, maar u ook wilt gebruiken van de nummerreeks die is gedefinieerd voor de boekstuknummers in Dynamics 365 voor bewerkingen, een hotfix is opgegeven voor de vrijgave februari 2016. Het nummer van de hotfix is 3170316 en deze kan worden gedownload vanuit Lifecycle Services (LCS). Zie voor meer informatie [Hotfixes downloaden vanuit Lifecycle Services](..\migration-upgrade\download-hotfix-lcs.md).
    -   Deze functionaliteit van de journaalnaam die wordt gebruikt voor de invoer in Dynamics 365 voor bewerkingen, stellen **de nummertoewijzing tijdens boeking** naar **Ja**.
    -   Er moet nog steeds een boekstuknummer worden gedefinieerd in het geïmporteerde bestand. Maar dit nummer is tijdelijk en wordt overschreven door de Dynamics 365 voor bewerkingen boekstuknummer wanneer het journaal wordt geboekt. U moet ervoor zorgen dat de regels van het journaal juist zijn gegroepeerd op tijdelijk boekstuknummer. Bijvoorbeeld tijdens het boeken worden drie regels gevonden die een tijdelijke boekstuknummer 1 hebben. Het tijdelijke boekstuknummer van alle drie de regels wordt overschreven door het volgende nummer uit de nummerreeks. Als deze drie regels geen evenwichtige vermelding zijn, wordt het boekstuk niet geboekt. Vervolgens geldt dat, als er regels worden gevonden die een tijdelijk boekstuknummer van 2 hebben, dit nummer wordt overschreven door het volgende boekstuknummer in de nummerreeks enzovoort.

<!-- -->

-   Wanneer u geen gebruikmaakt van de **verwerking op basis van een Set** instelt, u hoeft niet te bieden een boekstuknummer in het geïmporteerde bestand. De boekstuknummers worden gemaakt tijdens het importeren, op basis van de instellingen van de journaalnaam (**Maximaal één boekstuknummer**, **In samenhang met saldo** enzovoort). Als bijvoorbeeld de journaalnaam is gedefinieerd als **In samenhang met saldo**, ontvangt de eerste regel een nieuw standaard boekstuknummer. Het systeem evalueert vervolgens de lijn om te bepalen of de debetbedragen gelijk zijn aan de creditbedragen. Als een tegenrekening voor de regel bestaat, ontvangt de volgende regel die wordt geïmporteerd in een nieuw boekstuknummer. Als er geen tegenrekening bestaat, evalueert het systeem of de debetbedragen gelijk zijn aan de creditbedragen bij het importeren van elke nieuwe regel.
-   Als het veld **Boekstuknummer** is ingesteld op **Automatisch gegenereerd**, mislukt het importeren. De instelling **Automatisch gegenereerd** voor het veld **Boekstuknummer** wordt niet ondersteund.

Standaard gebruikt de entiteit Algemeen journaal verwerking op basis van sets. Nadat u de zakelijke vereisten voor uw organisatie hebt beoordeeld, kunt u de instelling **Op sets gebaseerde verwerking** wijzigen door te klikken op **Gegevensentiteiten** in de werkruimte **Gegevensbeheer**. Op sets gebaseerde verwerking wordt gebruikt om het importproces te versnellen. Als u geen gebruikmaakt van op sets gebaseerde verwerking, verloopt het importeren van de entiteit Algemeen journaal langzamer.


