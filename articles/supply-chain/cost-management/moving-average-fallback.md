---
title: Zwevend gemiddelde terugvalkostenreeks
description: Dit artikel bevat informatie over terugvalkostenreeksen voor berekeningen met zwevend gemiddelde in Microsoft Dynamics 365 Supply Chain Management.
author: JennySong-SH
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2020-03-25
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: ad67828e2608f4754a3dffd76c64292f6a91e95f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868009"
---
# <a name="moving-average-fallback-cost-sequence"></a>Terugvalkostenreeks met zwevend gemiddelde

[!include [banner](../includes/banner.md)]

Eén manier waarop u de voorraadkosten kunt berekenen, is door een _zwevend gemiddelde_ te gebruiken. U kunt maximaal drie kostenwaarden koppelen aan elk voorraadartikel:

- **Laatste uitgifte**: de laatste uitgiftekosten die zijn toegewezen voordat de voorraad negatief werd
- **Actieve kosten**: de laatste kosten die in een kostprijsberekeningsversie zijn geactiveerd
- **Artikelprijs**: de kosten die zijn opgegeven voor het vrijgegeven product

Om te bepalen welke van deze kostenwaarden moet worden gebruikt bij berekeningen van het zwevend gemiddelde, gebruikt het systeem een _terugvalkostenreeks_ om de voorkeursvolgorde voor de waarden in te stellen. Als de gewenste kostenwaarde niet beschikbaar is, wordt de volgende voorkeurswaarde van het systeem gebruikt, enzovoort.

In eerdere versies van Microsoft Dynamics 365 Supply Chain Management heeft het systeem een vaste terugvalkostenreeks gebruikt (_Laatste uitgifte – Actieve kosten – Artikelprijs_). In versie 10.0.11 is dit nog steeds de standaardvolgorde. U kunt echter ook een functie inschakelen waarmee u kunt kiezen uit drie beschikbare terugvalkostencombinaties. Deze functie kan vooral nuttig zijn voor organisaties die regelmatig negatieve voorraadwaarden gebruiken.

Als u de selector voor de terugvalkostenreeks beschikbaar wilt maken, moet u (of een beheerder) [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de functie _Terugvalkostenreeks met zwevend gemiddelde_ te activeren.

Ga als volgt te werk om de terugvalkostenreeks voor de berekening van het zwevende gemiddelde te selecteren.

1. De pagina **Parameters** openen.
2. Stel op het tabblad **Voorraadboekhouding** in het gedeelte **Zwevend gemiddelde** het veld **Terugvalkostenreeks** in op een van de volgende waarden:

    - **Laatste uitgifte – Actieve kosten – Artikelprijs**: deze volgorde is de standaardvolgorde. Dit is de dezelfde reeks die wordt gebruikt als de functie _Terugvalkostenreeks met zwevend gemiddelde_ niet is ingeschakeld.
    - **Actieve kosten - laatste uitgifte**
    - **Actieve kosten – Artikelprijs**: organisaties kunnen prestatieproblemen ondervinden als ze bedrijfsprocessen gebruiken waarbij de voorraadregel negatief wordt en tegelijkertijd het transactievolume hoog is. Met deze instelling beperken ze de prestatieproblemen.

![Parameters voorraadboekhouding.](media/inventory-accounting-parameters.png "Parameters voorraadboekhouding")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]