---
title: Overzicht Optimization advisor
description: In dit onderwerp wordt beschreven hoe u Optimization advisor gebruiken om een optimale configuratie van Microsoft Dynamics 365 Finance and Operations te garanderen
author: roxanadiaconu
manager: AnnBe
ms.date: 03/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SelfHealingWorkspace
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Operations, Core
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: roxanad
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c2a957038bfad065361b46e85b8195214779cc2d
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---

# <a name="optimization-advisor-overview"></a>Overzicht Optimization advisor

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u Optimization advisor gebruiken om een optimale configuratie van Microsoft Dynamics 365 Finance and Operations te garanderen

## <a name="overview"></a>Overzicht

Een onjuiste configuratie en instellingen van een module hebben een negatief effect op de beschikbaarheid van functies in Finance and Operations, op de systeemprestaties en de goede werking van bedrijfsprocessen. De kwaliteit van zakelijke gegevens (bijvoorbeeld juiste, nauwkeurige en opgeschoonde gegevens) is ook van invloed op de systeemprestaties, en op de besluitvormingsmogelijkheden, productiviteit, enzovoort van een organisatie.

Het werkgebied **Optimization advisor** is een hulpprogramma waarmee hoofdgebruikers, analisten, functionele consultants en IT-ondersteuning problemen in de moduleconfiguratie en zakelijke gegevens kunnen vaststellen. Optimization advisor suggereert aanbevolen procedures voor de configuratie van de module en zakelijke gegevens die verouderd of onjuist zijn.

Optimization advisor voert regelmatig een set best practice-regels uit. Een standaardset met regels wordt samen met Microsoft Dynamics 365 for Finance and Operations versie 8.0 (april 2018) uitgebracht. Gebruikers kunnen echter ook regels maken die specifiek zijn voor hun aanpassingen, oplossingen van onafhankelijke softwareleveranciers (ISV's) en hun zakelijke gegevens. Zie [Nieuwe regels maken](./create-rules-optimization-advisor.md) voor meer informatie over het maken van regels.

Wanneer een overtreding van een regel wordt gevonden, wordt een optimalisatiemogelijkheid gegenereerd die wordt weergegeven in het werkgebied **Optimization advisor**. Een gebruiker kan correctieve actie ondernemen vanuit het werkgebied **Optimization advisor**.

De kansen kunnen bedrijfsspecifiek en bedrijfsbreed zijn, afhankelijk van het type instellingen en gegevens die worden gecontroleerd. Bedrijfsbrede kansen kunnen worden weergegeven via alle bedrijven. Selecteer eerst een bedrijf als u de kansen voor een specifiek bedrijf wilt weergeven.

Standaardbeveiligingsbeleid is van toepassing op optimalisatiemogelijkheden. Bijvoorbeeld: de optimalisatiemogelijkheden die betrekking hebben op de configuratie van de module **Magazijnbeheer** zijn alleen zichtbaar voor gebruikers die toegang hebben tot Magazijnbeheer en die de instellingen kunnen wijzigen.

Wanneer u actie onderneemt voor sommige verkoopkansen, berekent het systeem de impact van de mogelijkheid als vermindering van de runtime van bedrijfsprocessen. Helaas is deze functie niet beschikbaar voor alle optimalisatiemogelijkheden.

Voor meer informatie over Optimization advisor, bekijkt u de korte video [Optimization advisor in Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ).

## <a name="optimization-rules"></a>Optimalisatieregels

Als u de volledige lijst met Optimization advisor-regels wilt weergeven en wilt zien hoe vaak de regels worden beoordeeld, gaat u naar **Systeembeheer** &gt; **Periodieke taken** &gt; **Validatieregel van diagnose onderhouden**. Alleen regels met de status **Actief** worden geëvalueerd. De frequentie van de evaluatie kan worden ingesteld op **Dagelijks**, **Wekelijks**, **Maandelijks** of **Niet-gepland**.

Als u de beoordeling van niet-geplande regels wilt activeren of periodieke regels buiten hun vooraf bepaalde planning opnieuw wilt beoordelen, gaat u naar **Systeembeheer** &gt; **Periodieke taken** &gt; **Validatieregel van diagnose plannen**. Selecteer in het dialoogvenster **Validatie diagnoseregel** een evaluatiefrequentie. Alle regels met de opgegeven frequentie worden opnieuw beoordeeld.

De huidige set met optimalisatieregels kan worden verdeeld in de volgende categorieën.

### <a name="module-configuration-and-setup"></a>Moduleconfiguratie en instellingen

Het instellen van Magazijnbeheer is een complex proces. Om het proces gemakkelijker te maken zijn een aantal regels geïntroduceerd om de juistheid van de instellingen te valideren. Bijvoorbeeld valideert u met één regel de instellingen voor magazijnlocatierichtlijnen voor vaste productvariantlocaties voor verkooporders en transferorders.

Ook zijn er regels die controleren of de functies die zijn geactiveerd, werkelijk worden gebruikt. Eén regel bepaalt bijvoorbeeld of u de module **Hoofdplanning** gebruikt. Als de regel vaststelt dat u de module niet gebruikt, wordt een optimalisatiemogelijkheid gegenereerd met het voorstel dat u de planningsprocessen uitschakelt.

### <a name="system-configuration"></a>Systeemconfiguratie

Als bepaalde functionaliteit die wordt beheerd door een configuratiesleutel niet wordt gebruikt, wordt een optimalisatiemogelijkheid gegenereerd met het voorstel de configuratiesleutel uit te schakelen. Voorbeelden van configuratiesleutels zijn **Catch weight**, **Budgetplanning**, **Project** en **Lijst met goedgekeurde leveranciers**.

### <a name="business-data-consistency-and-cleanup"></a>Consistentie van zakelijke gegevens en opschonen

Als de hoofdgegevens niet correct zijn (bijvoorbeeld als er maateenheidconversies zijn voor eenheden die niet zijn gedefinieerd, of als u maateenheidconversie hebt die deelbaar zijn door 0 \[nul\]), wordt een optimalisatiemogelijkheid gegenereerd met het voorstel dat u de gegevens corrigeert. 

Als er te veel historische batchtaakvermeldingen, verouderde artikelen, afgesloten voorhanden voorraadgegevens voor magazijnartikelen zijn, of als deze vermeldingen en artikelen te oud zijn, worden optimalisatiemogelijkheden gegenereerd met het voorstel om de gegevens op te schonen. Door uw gegevens op te schonen kunt u de algehele systeemprestaties verbeteren.

### <a name="best-practices"></a>Aanbevolen procedures

Als bepaalde bedrijfsprocessen niet de beste methoden volgen (bijvoorbeeld als u de voorafsluiting van de voorraad uitvoert voordat de voorraad is afgesloten of als u de geplande batch gebruikt voor batchoverboeking voor subadministratiejournalen), wordt u met optimalisatiemogelijkheden geïnformeerd over de beste methoden en kunt u deze volgen.

## <a name="optimization-opportunities"></a>Optimalisatiemogelijkheden

Als u de optimalisatiemogelijkheden wilt weergeven die zijn gegenereerd tijdens de evaluatie van optimalisatieregels, opent u het werkgebied **Optimization advisor**.

In dit werkgebied kunt u meer informatie over een mogelijkheid weergeven door **Meer informatie** te selecteren. Als u het systeem actie wilt laten ondernemen om de instelling te corrigeren, de gegevens op te schonen, enzovoort, zodat u niet zelf de bijbehorende pagina's hoeft te openen, selecteert u **Actie ondernemen**.

Er is geen werkstroom voor optimalisatiemogelijkheden. Nadat u **Actie ondernemen** hebt geselecteerd of een navigatiepad gebruikt dat is opgegeven in het dialoogvenster **Meer informatie**, verdwijnt de optimalisatiemogelijkheid uit de lijst. Als met de correctieve actie het probleem niet is opgelost, wordt de mogelijkheid opnieuw gegenereerd als de regel de volgende keer wordt geëvalueerd.

Als u een mogelijkheid niet van toepassing is op uw rol, selecteert u **Verbergen in mijn lijst**. Zelfs als de regel achter deze mogelijkheid later opnieuw wordt geactiveerd, ziet u deze niet in de lijst.

Als u de evaluatie van specifieke regels wilt deactiveren, selecteert u de mogelijkheid die is gegenereerd door de regel en vervolgens **Analyse deactiveren**.

## <a name="additional-resources"></a>Aanvullende resources

[Nieuwe regels maken](./create-rules-optimization-advisor.md)

[Optimization advisor in Dynamics 365 for Finance and Operations (Video)](https://www.youtube.com/watch?v=MRsAzgFCUSQ)

