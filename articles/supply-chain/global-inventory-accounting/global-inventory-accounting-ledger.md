---
title: Grootboek voor Algemene voorraadboekhouding (Global Inventory Accounting)
description: Dit artikel beschrijft grootboeken voor Algemene voorraadboekhouding, die worden gedefinieerd door een combinatie van een valuta, een kalender, een conventie en een koppeling met een rechtspersoon.
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4d3779d7d335a903d7eabfadfed79e47652c6835
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897656"
---
# <a name="global-inventory-accounting-ledger"></a>Grootboek voor Algemene voorraadboekhouding (Global Inventory Accounting)

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until 4/30/2022 -->

Algemene voorraadboekhouding heeft een eigen set grootboeken. Telkens wanneer een voorraadgerelateerde transactie wordt verwerkt voor een relevante rechtspersoon, kan het systeem die transactie in elk gewenst aantal grootboeken voor Algemene voorraadboekhouding verantwoorden.

Een grootboek is een register met debet- en crediteenheden. Deze eenheden worden geclassificeerd met behulp van kostenelementen en subadministratierekeningen. Een grootboek van Algemene voorraadboekhouding wordt gedefinieerd door de combinatie van een valuta, een kalender, een conventie en een koppeling met een rechtspersoon.

Als u grootboeken voor Algemene voorraadboekhouding wilt instellen, gaat u naar **Algemene voorraadboekhouding \> Instellingen \> Grootboeken voor Algemene voorraadboekhouding**. Stel voor elk grootboek de volgende velden in:

- **Naam**: voer de naam van het grootboek in.
- **Beschrijving**: voer een beschrijving van het grootboek in.
- **Fiscale kalender**: geef de fiscale kalender voor het grootboek op.
- **Valuta en wisselkoerstype**: gebruik de velden op dit sneltabblad om de boekhoudingvaluta te selecteren die in het grootboek wordt gebruikt en het wisselkoerstype. De valuta die u selecteert, kan verschillen van de valuta die de rechtspersoon gebruikt. In Global Inventory Accounting kunnen gebruikers zoveel kostprijsboekhoudingsgrootboeken definiëren als nodig is. Global Inventory Accounting ondersteunt voorraadboekhouding in meerdere valuta's en in meerdere waarderingen. Stel de volgende velden in:

    - **Valuta**: selecteer de kostprijsprijsvaluta waarin voorraadgerelateerde waarden worden onderhouden. Deze waarden omvatten de voorraadwaarde, de kosten van de verkochte goederen, de transitvoorraad en alle soorten afwijkingen.
    - **Type wisselkoers**: selecteer de wisselkoers die het systeem moet gebruiken om het transactiebedrag in de transactievaluta en de standaardkosten van de artikelen naar de kostprijsprijsvaluta te converteren.

- **Conventienaam**: geef een conventie op. Een conventie is een verzameling beleidsregels die bepalen hoe kosten in dit grootboek worden vastgelegd.
- **Rechtspersoon**: de documenten die naar de geselecteerde rechtspersoon zijn geboekt, worden in het grootboek vastgelegd.
- **Priming**: bepaal of voorraadtransacties die zijn gemaakt voordat het grootboek werd gemaakt, moeten worden verwerkt volgens de valuta en conventie in het grootboek. Selecteer een van de volgende waarden:

    - **Geactiveerd**: het grootboek moet transacties verwerken die zijn gemaakt voordat het grootboek werd gemaakt.
    - **Gedeactiveerd**: het grootboek moet alleen transacties verwerken die zijn gemaakt na dat het grootboek werd gemaakt.

    > [!IMPORTANT]
    > U kunt **niet meer** terug naar dit veld om het in te stellen nadat u nieuwe documenten hebt ingevoerd.

- **Status**: de status van de nieuwe grootboeken wordt automatisch op *Voorbereiden* ingesteld door het systeem.
