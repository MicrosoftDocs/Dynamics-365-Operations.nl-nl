---
title: Terugvalkostenreeks met zwevend gemiddelde
description: Dit onderwerp bevat informatie over terugvalkostenreeksen voor berekeningen met zwevend gemiddelde in Microsoft Dynamics 365 Supply Chain Management.
author: AndersGirke
manager: AnnBe
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-03-25
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: b2172dfbec0a7f0fa25a081e4d92635a09f00e46
ms.sourcegitcommit: 3a823444005d316bd95fc663e2dbc8252ac7d93a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261317"
---
# <a name="moving-average-fallback-cost-sequence"></a>Terugvalkostenreeks met zwevend gemiddelde

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

![Parameters voorraadboekhouding](media/inventory-accounting-parameters.png "Parameters voorraadboekhouding")