---
title: Nummers voor ontvangstbewijzen opnieuw instellen
description: In dit artikel wordt beschreven hoe u de ontvangstbewijsnummers opnieuw kunt instellen die worden gebruikt voor verschillende acties op een gewenste datum (bijvoorbeeld het boekjaar of het kalenderjaar).
author: ShalabhjainMSFT
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Commerce
ms.author: asharchw
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Application update 10.0.9
ms.openlocfilehash: 5dc9f3f977e04866562781d9768141a4a96166f4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858851"
---
# <a name="reset-receipt-numbers"></a>Nummers voor ontvangstbewijzen opnieuw instellen 

[!include [banner](includes/banner.md)]

> [!NOTE]
> Selecteer de eigenschap **Onafhankelijk volgnummer** voor alle ontvangstbewijstypen in het functionaliteitsprofiel voordat u deze functie gebruikt. Daarnaast moet de systeemtijdzone van het apparaat, waar het POS wordt gebruikt, overeenkomen met de bijbehorende tijdzone van de winkel. Vanwege deze beperkingen wordt u aangeraden deze functie niet te gebruiken tijdens de productie terwijl wij proberen deze problemen in een toekomstige versie op te lossen. 

Detailhandelaren genereren ontvangstbewijsnummers voor verschillende acties in de winkel, zoals contante transacties, retourtransacties, klantorders, offertes en betalingen. Hoewel detailhandelaren hun eigen ontvangstbewijsindelingen definiëren, hebben sommige landen of regio's voorschriften die beperkingen opleggen aan de ontvangstbewijsindelingen. Deze voorschriften kunnen bijvoorbeeld het aantal tekens op het ontvangstbewijs beperken, opeenvolgende ontvangstbewijsnummers vereisen, het gebruik van bepaalde speciale tekens beperken of de eis stellen dat ontvangstbewijsnummers aan het begin van het jaar opnieuw worden ingesteld. Microsoft Dynamics 365 Commerce maakt het proces van het beheren van ontvangstbewijsnummers zeer flexibel, zodat detailhandelaren beter aan de wettelijke vereisten kunnen voldoen. In dit artikel wordt uitgelegd hoe u de functionaliteit gebruikt voor het opnieuw instellen van ontvangstbewijsnummers.

In Commerce kunnen ontvangstbewijsindelingen alfanumeriek zijn. U kunt hierin zowel statische inhoud als dynamische inhoud opnemen. Statische inhoud omvat alfabetische tekens, cijfers en speciale tekens. Dynamische inhoud omvat een of meer tekens die informatie vertegenwoordigen, zoals het winkelnummer, het terminalnummer, de datum, de maand, het jaar en nummerreeksen die automatisch worden verhoogd. De indelingen worden gedefinieerd in de sectie **Ontvangstbewijsnummering** van het functionaliteitsprofiel. In de volgende tabel worden de tekens beschreven die de dynamische inhoud vertegenwoordigen.

| Tekens | Beschrijving |
|------------|-------------|
| S          | Het teken **S** wordt gebruikt voor het winkelnummer. Als een winkel bijvoorbeeld het nummer HOUSTON1 heeft, geeft de notatie **SSS** de tekst "ON1" weer op het ontvangstbewijs. Met de notatie **SSSSS** wordt "STON1" weergegeven op het ontvangstbewijs. |
| T          | Het teken **T** wordt gebruikt voor het terminalnummer. Als een terminal bijvoorbeeld het nummer 0001 heeft, wordt met de notatie **TTTT** de tekst "0001" weergegeven op het ontvangstbewijs. |
| E          | Het teken **C** wordt gebruikt voor het personeels-id-nummer. Als een personeelslid bijvoorbeeld een id van 000160 heeft, wordt met de notatie **CCCC** de tekst "0160" op het ontvangstbewijs weergegeven. |
| ddd        | De tekens **ddd** komen overeen met de dag van het jaar, van 1 tot en met 366. Op 15 januari wordt met de notatie **ddd** bijvoorbeeld "015" weergegeven op het ontvangstbewijs. |
| MM         | De tekens **MM** worden gebruikt voor aanduiding van de maand met twee cijfers. In januari wordt met de notatie **MM** bijvoorbeeld "01" weergegeven op het ontvangstbewijs. |
| DD         | De tekens **DD** worden gebruikt voor aanduiding van de dag van de maand met twee cijfers. Op 15 januari wordt met de notatie **DD** bijvoorbeeld "15" weergegeven op het ontvangstbewijs. |
| YY         | De tekens **YY** worden gebruikt voor aanduiding van het jaar met twee cijfers. In een maand gedurende het jaar 2020 wordt met de notatie **JJ** bijvoorbeeld "20" weergegeven op het ontvangstbewijs. |
| \#         | Een hekje (**\#**) wordt gebruikt voor opeenvolgende nummering. Met de notatie **####** wordt bijvoorbeeld "0001", "0002", "0003" enzovoort weergegeven op het ontvangstbewijs. |

U kunt de opeenvolgende nummering van het ontvangstbewijs op een bepaalde datum opnieuw instellen. Voor de eerste transactie die plaatsvindt na 12:00 AM op de geselecteerde datum voor nieuwe instellen, stelt het systeem de nummerreeks van het ontvangstbewijs opnieuw in op 1. U kunt ook opgeven of het opnieuw instellen van de waarde slechts één keer moet gebeuren of dat deze elk jaar plaatsvindt. Als een jaarlijks terugkeerpatroon wordt opgegeven, wordt de waarde automatisch elke jaar opnieuw ingesteld totdat die detailhandelaren hier een einde aan maakt. 

Voer de volgende stappen uit om het opnieuw instellen in te schakelen.

1. Ga naar **Retail en Commerce \> Kanaalinstellingen \> POS-instellingen \> POS-profielen \> Functionaliteitsprofielen**.
1. Selecteer op het sneltabblad **Ontvangstbewijsnummering** de optie **Datum voor opnieuw instellen van nummer instellen**.
1. Selecteer in het vervolgkeuzemenu in het veld **Datum voor opnieuw instellen** een toekomstige datum waarop de nieuwe instelling moet worden uitgevoerd.
1. Selecteer in het veld **Type voor opnieuw instellen van ontvangstbewijs** de optie **Eenmalig** of **Jaarlijks**.
1. Selecteer **OK**.

![Een datum voor het opnieuw instellen van een ontvangstbewijs selecteren.](media/Enable_receipt_reset.png "Een datum voor het opnieuw instellen van een ontvangstbewijs selecteren")

Nadat u een datum hebt geselecteerd, wordt deze weergegeven in de kolom **Volgende datum voor opnieuw instellen van ontvangstbewijsnummer**. De datum voor opnieuw instellen is van toepassing op alle typen ontvangsttransacties. Daarom wordt de reeks ontvangstbewijsnummers opnieuw ingesteld voor alle typen ontvangstbewijzen.

Wanneer de begindatum wordt bereikt, wordt het ontvangstbewijsnummer opnieuw ingesteld voor de eerste transactie van elk type. Bovendien wordt in het functionaliteitsprofiel de datum voor opnieuw instellen verplaatst van de kolom **Volgende datum voor opnieuw instellen van ontvangstbewijsnummer** naar de kolom **Huidige datum voor opnieuw instellen van ontvangstbewijsnummer**. Deze wijziging geeft aan dat als een kassa niet wordt gebruikt op de datum voor opnieuw instellen, het ontvangstbewijsnummer opnieuw wordt ingesteld wanneer de *kassa* de volgende keer wordt gebruikt. Op 3 december 2019 selecteert u bijvoorbeeld **1 januari 2020** als datum voor opnieuw instellen. Op 1 januari wordt het ontvangstbewijsnummer opnieuw ingesteld wanneer de kassa's hun eerste transactie uitvoeren. In december en januari wordt één kassa echter helemaal niet gebruikt, terwijl deze vervolgens in februari voor het eerst opnieuw wordt gebruikt. In dit geval wordt, omdat er een actie voor opnieuw instellen is gedefinieerd, het ontvangstbewijsnummer voor die kassa opnieuw ingesteld wanneer de kassa de eerste transactie in februari uitvoert.

Met de functie **Datum voor opnieuw instellen** kunt u toekomstige datums voor opnieuw instellen wissen. Als de datum voor opnieuw instellen echter in het verleden lag, kan deze niet ongedaan worden gemaakt. Daarom wordt het opnieuw instellen nog steeds uitgevoerd voor alle kassa's waarbij het opnieuw instellen nog niet heeft plaatsgevonden.

> [!NOTE]
> Afhankelijk van de datum voor opnieuw instellen die u selecteert en de ontvangstbewijsindeling, hebt u mogelijk dubbele ontvangstbewijsnummers. Hoewel het verkooppunt (POS) deze situaties kan verwerken, is er hierdoor meer tijd nodig voor het verwerken van retouren, aangezien verkoopmedewerkers moeten kiezen uit dubbele ontvangstbewijzen. Andere complicaties met betrekking tot het opschonen van gegevens kunnen zich voordoen als de dubbele ontvangstbewijzen geen gepland gevolg hebben. Daarom raden we aan om dynamische datumtekens (bijvoorbeeld **ddd**, **MM**, **DD** en **YY**) te gebruiken om dubbele ontvangstbewijsnummers na opnieuw instellen te voorkomen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]