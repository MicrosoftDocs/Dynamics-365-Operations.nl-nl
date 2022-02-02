---
title: Rekeningen voor automatische transacties
description: In dit onderwerp wordt uitgelegd hoe rekeningen voor automatische transacties worden gebruikt voor het boeken via Microsoft Dynamics 365 en worden voorbeelden gegevens voor belangrijke rekeningen voor automatische transacties.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cecbeb769235e525390cc7a66800a9b0d55d78a9
ms.sourcegitcommit: 5bfd6511d710deb539b4030eb0e9c48d25513595
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/19/2022
ms.locfileid: "8014040"
---
# <a name="accounts-for-automatic-transactions"></a>Rekeningen voor automatische transacties

De pagina **Rekeningen voor automatische transacties** (**Grootboek &gt; Boekingsinstellingen &gt; Rekeningen voor automatische transacties**) wordt gebruikt om de standaard hoofdrekening te definiëren die voor elk boekingstype in het systeem wordt gebruikt. De meeste boekingstypen kunnen worden geconfigureerd op een modulespecifieke of functiespecifieke pagina, maar sommige boekingstypen alleen op de pagina **Rekeningen voor automatische transacties**.

U kunt bijvoorbeeld de hoofdrekening opgeven die wordt gebruikt voor het boekingstype **Klantsaldo** in het veld **Overzicht** op de pagina **Boekingsprofiel van klant** en een andere hoofdrekening gebruiken voor elk klantprofiel. Op deze manier hebt u meer gedetailleerde controle over de boekingen. U kunt ook alleen de foutrekening opgeven op de pagina **Rekeningen voor automatische transacties**.

Wanneer u de pagina **Rekeningen voor automatische transacties** in een nieuwe rechtspersoon opent, is de lijst met rekeningen leeg. U kunt de meest algemene boekingstypen die op de pagina moeten worden geconfigureerd, toevoegen met de knop **Standaardtypen maken**. Vervolgens kunt u voor elke rij de hoofdrekening selecteren in het veld **Hoofdrekening**. Als u het veld **Hoofdrekening** leeglaat voor een boekingstype en u geen hoofdrekening hebt geconfigureerd op een modulespecifieke of functiespecifieke pagina, ontvangt u een foutbericht wanneer u een transactie boekt die het boekingstype gebruikt. Normaal is het bericht "De rekening voor \[het boekingstype\] kan niet worden gevonden".

## <a name="default-posting-types"></a>Standaardboekingstypen

In de volgende tabel ziet u voorbeelden van de standaardboekingstypen die worden gemaakt wanneer u **Standaardtypen maken** selecteert op de pagina **Rekeningen voor automatische transacties**. Hier worden voorbeeld hoofdrekeningen en omschrijvingen weergegeven. De kolom Debet/Credit? geeft aan of de transactie meestal een debet- of credittransactie betreft. In sommige gevallen kan een transactie een debet- of een credittransactie boeken. De kolom Vereffeningsrekening geeft aan of het boekingstype een vereffeningsrekening is. Als het boekingstype een vereffeningsrekening is, wordt het bedrag dat op de rekening wordt geboekt, automatisch teruggeboekt wanneer een latere transactie wordt geboekt.

| Boekingstype | Voorbeeld van hoofdrekening | Voorbeeld van hoofdrekeningnaam | Rekeningtype | Debet/Credit? | Vereffeningsrekening | Description |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Afronding in aangiftevaluta | 618160 | Diverse onkosten | Onkosten | Beide | Nee | Dit boekingstype wordt gebruikt wanneer een afrondingsverschil optreedt wanneer een transactiebedrag in een vreemde valuta naar de aangiftevaluta wordt omgerekend. |
| Afronding in valuta voor boekhouding | 618160 | Diverse onkosten | Onkosten | Beide | Nee | Dit boekingstype wordt gebruikt wanneer een afrondingsverschil optreedt wanneer een transactiebedrag in een vreemde valuta naar de boekhoudvaluta wordt omgerekend. |
| Foutrekening | 999999 | Foutrekening | Onkosten | Beide | Nee | Dit boekingstype wordt gebruikt wanneer er een fout optreedt in het systeem. De rekening moet elke periode worden gevalideerd en eventuele fouten moeten worden opgelost. |
| Resultaat per jaareinde | 300160 | Ingehouden winst | Eigen vermogen | Beide | Nee | Dit boekingstype wordt gebruikt wanneer het eindejaarsproces wordt uitgevoerd om het rekeningsaldo van het type **Winst en verlies** te verplaatsen naar de hoofdrekening die voor het eindejaarsresultaat is geselecteerd. |
| Contantkorting van klant | Niet van toepassing | Niet van toepassing | Niet van toepassing | Niet van toepassing | Nee | Het boekingstype dat is gedefinieerd op de pagina **Rekeningen voor automatische transacties** wordt niet gebruikt. Er is een hoofdrekening vereist wanneer contantkortingen worden geconfigureerd in Klanten.|
| Contantkorting van leverancier | Niet van toepassing | Niet van toepassing | Niet van toepassing | Niet van toepassing | Nee | Het boekingstype dat is gedefinieerd op de pagina **Rekeningen voor automatische transacties** wordt niet gebruikt. Er is een hoofdrekening vereist wanneer contantkortingen worden geconfigureerd in Leveranciers. |

## <a name="additional-posting-types"></a>Aanvullende boekingstypen

In de volgende tabel ziet u voorbeelden van extra boekingstypen die moeten worden geconfigureerd als u van plan bent om de gerelateerde functies te gebruiken. Voor deze boekingstypen is er geen boekingsprofielconfiguratie beschikbaar in een andere module. De kolom Debet/Credit? geeft aan of de transactie meestal een debet- of credittransactie betreft. In sommige gevallen kan een transactie een debet- of een credittransactie boeken. De kolom Vereffeningsrekening geeft aan of het boekingstype een vereffeningsrekening is. Als het boekingstype een vereffeningsrekening is, wordt het bedrag dat op de rekening wordt geboekt, automatisch teruggeboekt wanneer een latere transactie wordt geboekt.

| Boekingstype | Voorbeeld van hoofdrekening | Voorbeeld van hoofdrekeningnaam | Rekeningtype | Debet/Credit? | Vereffeningsrekening | Description |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Saldorekening voor consolidatieverschil | 801200 | Winst en verlies - herwaardering | Onkosten | Beide | Nee | Dit boekingstype wordt gebruikt bij het uitvoeren van een consolidatie waarbij een valutaherwaardering wordt uitgevoerd waarbij er sprake is van verschillen in valuta's tijdens de herwaardering. |
| Verlies-en-winst-rekening voor consolidatieverschillen | 801200 | Winst en verlies - herwaardering | Onkosten | Beide | Nee | Dit boekingstype wordt gebruikt bij het uitvoeren van een consolidatie waarbij een valutaherwaardering wordt uitgevoerd waarbij er sprake is van verschillen in valuta's tijdens de herwaardering. |
| Inter-unit - debet | 133500 | Interunit debiteuren | Activum | Debet | Nee | Dit boekingstype wordt gebruikt wanneer u een salderingsdimensie selecteert op de **grootboekpagina** en de dimensie niet saldeert met een geboekte transactie. |
| Inter-unit - credit | 233500 | Inter-unit crediteuren | Aansprakelijkheid | Krediet | Nee | Dit boekingstype wordt gebruikt wanneer u een salderingsdimensie selecteert op de **grootboekpagina** en de dimensie niet saldeert met een geboekte transactie. |
