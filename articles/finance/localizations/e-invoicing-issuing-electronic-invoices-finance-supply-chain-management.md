---
title: Elektronische facturen uitgeven in Finance en Supply Chain Management
description: In dit onderwerp wordt uitgelegd hoe u elektronische facturen uitgeeft in Microsoft Dynamics 365 Finance en Dynamics 365 Supply Chain Management via de invoegtoepassing voor elektronisch factureren.
author: gionoder
manager: AnnBe
ms.date: 02/26/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 099ebb56710e920f7b1453f32f23f59a80486ebf
ms.sourcegitcommit: 105f65468b45799761c26e5d0ad9df4ff162c38d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/04/2021
ms.locfileid: "5486948"
---
# <a name="issue-electronic-invoices-in-finance-and-supply-chain-management"></a>Elektronische facturen uitgeven in Finance en Supply Chain Management

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

In dit onderwerp wordt uitgelegd hoe u elektronische facturen uitgeeft in Microsoft Dynamics 365 Finance en Dynamics 365 Supply Chain Management via de invoegtoepassing voor elektronisch factureren.


## <a name="feature-activation"></a>Functieactivering

Als u elektronische facturen wilt uitgeven via de invoegtoepassing voor elektronische facturering, moet u de functie activeren in Finance en Supply Chain Management.

Elke functie komt overeen met een specifieke elektronische factureringsfunctie die voldoet aan de vereisten voor elektronische facturering van een land/regio.

De volgende tabel toont de lijst met functies die mogelijk worden ondersteund door de invoegtoepassing voor elektronische facturering.

| Naam                                              | Land/regio |
|---------------------------------------------------|----------------|
|Oostenrijkse elektronische factuur                        |Oostenrijk         |
|Belgische elektronische factuur                         |België         |
|Federale NF-e - Braziliaanse elektronische factuur       |Brazilië          |
|NFS-e - Elektronische factuur voor Braziliaanse service (plaats)|Brazilië          |
|Deense elektronische factuur                          |Denemarken         |
|Egyptische elektronische factuur                        |Egypte           |
|Estse elektronische factuur                        |Estland         |
|Finse elektronische factuur                         |Finland         |
|Franse elektronische factuur                          |Frankrijk          |
|Duitse elektronische factuur                          |Duitsland         |
|PEPPOL - Wereldwijde elektronische factuur                 |Algemeen          |
|Italiaanse elektronische factuur                         |Italië           |
|CFDI - Mexicaanse elektronische factuur                  |Mexico          |
|Nederlandse elektronische factuur                           |Nederland     |
|Noorse elektronische factuur                       |Noorwegen          |
|Spaanse elektronische factuur                         |Spanje           |

Als er een oudere functie voor elektronische facturering is die wordt ondersteund door de lokalisatie van een land/regio, zorgt de activering van deze functies ervoor dat de oudere functie wordt uitgeschakeld en dat de uitgifte van elektronische facturen mogelijk wordt via de invoegtoepassing voor elektronische facturering.

> [!IMPORTANT]
> Nadat de functie voor het integreren van elektronische facturering is ingeschakeld, is de nieuwe elektronische factureringservaring standaard uitgeschakeld. U kunt het functieconcept gebruiken om selectief nieuwe ervaringen voor rechtspersonen in te schakelen met behulp van land-/regiospecifieke functionaliteit. Met de optie **Algemeen** wordt de nieuwe ervaring bepaald voor de resterende landen/regio's die niet specifiek in de tabel worden vermeld.

## <a name="submit-electronic-documents"></a>Elektronische documenten indienen

Het proces waarbij elektronische documenten worden ingediend, is het enige communicatiepunt tussen Finance en Supply Chain Management en de invoegtoepassing voor elektronische facturering. Tijdens elke indieningsgebeurtenis loopt de communicatie in beide richtingen:

- **Van Finance en Supply Chain Management naar de invoegtoepassing voor elektronische facturering** – Finance en Supply Chain Management verzenden de abstracte facturen naar de invoegtoepassing voor elektronische facturering. Ze verzenden zo nodig ook de inhoud van variabelen die als onderdeel van de elektronische factureringsfuncties zijn geconfigureerd.
- **Van de invoegtoepassing voor elektronische facturering naar Finance en Supply Chain Management** – Afhankelijk van de elektronische factureringsfunctie, ontvangen Finance en Supply Chain Management updates van de invoegtoepassing voor elektronische facturering over de verwerkingsresultaten van eerder ingediende facturen. Ze ontvangen ook de inhoud van variabelen die als onderdeel van de elektronische factureringsfuncties zijn geconfigureerd.

Als u elektronische documenten wilt indienen in de invoegtoepassing voor elektronische facturering, gaat u in Finance en Supply Chain Management naar **Organisatieadministratie &gt; Periodiek &gt; Elektronische documenten &gt; Elektronische documenten indienen**.

Het beginpunt is een geboekte factuur. Deze factuur kan van verschillende oorsprong zijn, zoals verkooporders, projectfacturen of vrije-tekstfacturen.

Het indieningsproces kan handmatig of op de achtergrond worden uitgevoerd.

- **Handmatige uitvoering**: voor handmatige uitvoering moet u de optie **Filter** gebruiken om het bereik van documenten te definiëren dat moet worden ingediend. Op de pagina **Filters** kunt u uw eigen query configureren om de geboekte facturen te selecteren die moeten worden ingediend. Nadat u de selectie hebt gemaakt, moet u handmatig de verwerking starten en wachten tot deze is voltooid. Wanneer de verwerking is voltooid, wordt in een bericht in het actiecentrum het aantal elektronische documenten weergegeven dat is ingediend.
- **Uitvoering op de achtergrond**: uitvoering op de achtergrond zonder dat u hoeft te zijn aangemeld of het dialoogvenster voor verzending open hoeft te houden. U kunt het proces inplannen en de uitvoeringsfrequentie definiëren.

## <a name="view-the-submission-logs"></a>De indieningslogboeken weergeven

In Finance en Supply Chain Management kunt u de indieningslogboeken gebruiken om de resultaten van de verwerking van de verzending naar de invoegtoepassing voor elektronische facturering weer te geven. Ga naar **Organisatieadministratie &gt; Periodiek &gt; Elektronische documenten &gt; Elektronische documenten indienen** en selecteer in het veld **Documenttype** een waarde om het type facturen te filteren dat in de logboeken moet worden weergegeven.

Er zijn drie mogelijke indieningsstatussen:

- **Gepland**: de invoegtoepassing voor elektronische facturering heeft het ingediende document ontvangen van Finance en Supply Chain Management en de elektronische factureringsfunctie wordt verwerkt.
- **Voltooid**: de invoegtoepassing voor elektronische facturering heeft de functie voor elektronische facturering verwerkt zoals deze was geconfigureerd.
- **Mislukt**: er is een fout opgetreden bij de invoegtoepassing voor elektronische facturering of deze is gestopt door een uitzondering tijdens de verwerking van de elektronische factureringsfunctie.

> [!IMPORTANT]
> De indieningsstatus verwijst naar de status van de verwerking die de invoegtoepassing voor elektronische facturering met de elektronische factureringsfunctie doet. Het verwijst niet naar de eindstatus van de elektronische factuur zelf.
>
> Als een elektronische factuur bijvoorbeeld ter goedkeuring naar een externe webservice moet worden verzonden, kan de indieningsstatus **Voltooid** zijn, maar kan de status van de elektronische factuur **Afgewezen** zijn. In dit geval kon de invoegtoepassing voor elektronisch factureren de functie Elektronisch factureren verwerken, omdat deze is daarvoor is geconfigureerd. De elektronische factuur is echter afgewezen omdat deze niet aan de criteria voldoet die de webservice heeft vastgesteld voor factuurgoedkeuring.

De indieningslogboeken bevatten de volgende extra functies:

- **Indieningsdetails**: - de details van de belangrijkste indiening weergeven. De visualisatie geeft het volledige uitvoeringslogboek weer van de acties die in de elektronische factureringsfunctie zijn geconfigureerd. Gebruikers kunnen hiermee ook de bestanden downloaden die tijdens de verwerking zijn gemaakt. In scenario's waarin de factuur moet worden goedgekeurd door een externe webservice, kunnen gebruikers de status van de factuur bekijken.
- **Verwante indieningen**: de details van onderliggende indieningen weergeven.
- **Indieningen annuleren**: - deze functie maakt een speciaal indieningsproces mogelijk in scenario's waarin de elektronische factuur moet worden goedgekeurd door een externe webservice. Het geeft de invoegtoepassing voor elektronische facturering de opdracht om een specifiek bericht van de webservice te verzenden dat is bedoeld om de status van een goedgekeurde elektronische factuur in de webservicedatabase te annuleren.
- **Document opnieuw indienen**: - een elektronisch document opnieuw indienen dat reeds is verzonden naar de invoegtoepassing voor elektronische facturering. Er wordt een geheel nieuw logboek gemaakt op de pagina **Indieningsdetails**.
- **Gerelateerde indiening verzenden**


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
