---
title: Leveranciersinstellingen toegevoegd voor francoprijzen
description: In dit onderwerp worden de nieuwe velden beschreven die aan de bestaande pagina Leveranciers worden toegevoegd wanneer u de module Francoprijzen inschakelt. U gebruikt deze velden om de leveranciers in te stellen die u samen met functies voor Francoprijzen zult gebruiken.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 94d6356df8414d1058c64bfc4692af4011b69e87
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021147"
---
# <a name="vendor-settings-added-for-landed-cost"></a>Leveranciersinstellingen toegevoegd voor francoprijzen

[!include [banner](../../includes/banner.md)]

Wanneer u de module **Francoprijzen** inschakelt, worden verschillende nieuwe velden toegevoegd aan de bestaande pagina **Leveranciers**. U gebruikt deze velden om de leveranciers in te stellen die u samen met functies voor Francoprijzen zult gebruiken.

U kunt de relevante velden instellen door naar **Inkoopbeheer \> Leveranciers \> Alle leveranciers** te gaan. Open een bestaande leverancier of maak een nieuwe leverancier en selecteer vervolgens het sneltabblad **Diverse details**. Alle nieuwe velden die met de module **Francoprijzen** worden toegevoegd, worden weergegeven onder de kop **Reizen**. In de volgende tabel worden deze velden beschreven.

| Veld | Beschrijving |
|---|---|
| Verzendtype | <p>Selecteer de rol van de leverancier met betrekking tot francoprijzen:</p><ul><li>**Geen**: de leverancier heeft geen specifieke rol die betrekking heeft op Francoprijzen. Dit is de standaardinstelling, omdat de meeste leveranciers waarschijnlijk geen specifieke rol hebben.</li><li>**Verzendbedrijf**: de leverancier is een verzendbedrijf. Leveranciers met dit type verzending kunnen worden geselecteerd in het veld **Verzendbedrijf** op de pagina **Reizen**.</li><li>**Douane-expediteur**: de leverancier is een douane-expediteur. Leveranciers met dit type verzending kunnen worden geselecteerd in het veld **Douane-expediteur** op de pagina **Folio's**.</li><li>**Agent**: de leverancier is een agent. Leveranciers met dit type verzending kunnen worden geselecteerd in het veld **Agent** op de pagina's **Leveranciers** en **Inkooporders**.</li></ul> |
| Kostentypegroep | Wijs de leverancier toe aan een kostentypegroep om [automatische kosten](auto-cost-setup.md) te selecteren. |
| Vertrekhaven | Selecteer de haven van herkomst voor de reis. |
| Agent | De standaardagent wanneer er aankopen worden gedaan bij de leverancier. |
| Leverancier voor kostprijsberekening importeren | <p>Geef aan of de leverancier een leverancier met francoprijzen is.</p><p>**Tip**: u kunt dit veld gebruiken samen met beveiliging op recordniveau om de inkooporders te beperken die worden weergegeven wanneer een reis wordt gemaakt.</p> |
| Verzendbedrijf | Het standaardbedrijf selecteren dat wordt gebruikt wanneer inkooporders worden gemaakt voor de leverancier. |
| Serviceprovider | Geef aan of de leverancier een serviceleverancier is. |
| Over-/ondertolerantiegroep | Selecteer de standaardgroep voor over-/ondertolerantie voor de leverancier. |
