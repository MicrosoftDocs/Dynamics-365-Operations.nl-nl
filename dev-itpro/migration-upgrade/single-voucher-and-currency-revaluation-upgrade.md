---
title: Upgrade voor enkel boekstuk en herwaardering van valuta voor Microsoft Dynamics 365 for Operations, versie 1611
description: "Sommige organisaties voeren journalen in met een enkel boekstuk dat meer dan één klant of leverancier bevat, waarbij ze ook het herwaarderingsproces voor vreemde valuta voor klanten of leveranciers uitvoeren. In dit onderwerp worden de stappen beschreven die deze organisaties moeten volgen wanneer ze een upgrade uitvoeren naar Microsoft Dynamics 365 for Operations, versie 1611."
author: twheeloc
manager: AnnBe
ms.date: 2016-12-28 16 - 04 - 17
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: d42c753d0dc8b8efc2a0d2a26da32a4951d85503
ms.lasthandoff: 03/31/2017


---

# <a name="single-voucher-and-currency-revaluation-upgrade-for-microsoft-dynamics-365-for-operations-version-1611"></a>Upgrade voor enkel boekstuk en herwaardering van valuta voor Microsoft Dynamics 365 for Operations, versie 1611

Sommige organisaties voeren journalen in met een enkel boekstuk dat meer dan één klant of leverancier bevat, waarbij ze ook het herwaarderingsproces voor vreemde valuta voor klanten of leveranciers uitvoeren. In dit onderwerp worden de stappen beschreven die deze organisaties moeten volgen wanneer ze een upgrade uitvoeren naar Microsoft Dynamics 365 for Operations, versie 1611.

Voer deze stappen uit als u een upgrade uitvoert naar Microsoft Dynamics 365 for Operations, versie 1611.

1.  Voordat u een upgrade naar Dynamics 365 for Operations uitvoert, moet u de processen voor herwaardering van vreemde valuta uitvoeren voor klanten en leveranciers. Stel het veld **Methode** in op **Factuurdatum**. Een herwaarderingstransactie wordt gemaakt waarin de laatste herwaardering van vreemde valuta wordt omgekeerd. Daarom worden de openstaande transacties gewaardeerd tegen hun oorspronkelijke boekhoudingsvaluta.
2.  Voer een upgrade uit naar Dynamics 365 for Operations, versie 1611.
3.  Voer de herwaardering van vreemde valuta voor zowel Leveranciers als Klanten opnieuw uit. Stel deze keer het veld **Methode** in op **Standaard**. Een nieuwe herwaarderingstransactie wordt gemaakt op basis van de huidige wisselkoersen. Deze transactie legt de niet-gerealiseerde winst/verlies vast en het juiste bedrag in het totaalgrootboek.



