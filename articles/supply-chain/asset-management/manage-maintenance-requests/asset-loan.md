---
title: Geleende activa
description: In dit onderwerp wordt beschreven hoe u geleende activa registreert in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 07472188051aea7084142cc417c6d725462cf4f9
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205248"
---
# <a name="asset-loans"></a>Geleende activa

[!include [banner](../../includes/banner.md)]

 

Als uw bedrijf activa ontvangt voor reparatie- of onderhoudstaken van interne vestigingen of klanten, en als u activa tijdelijk uitleent aan die vestigingen of klanten, kan Activabeheer de geleende activa volgen.

## <a name="register-asset-loans-on-a-maintenance-request"></a>Geleende activa registreren op een onderhoudsverzoek

1. Selecteer **Activabeheer** \> **Algemeen** \> **Onderhoudsverzoeken** \> **Alle onderhoudsverzoeken** of **Actieve onderhoudsverzoeken**.
2. Selecteer het onderhoudsverzoek waarvoor u een geleend activum wilt registreren en selecteer **Bewerken**.
3. Op de pagina **Aanvragen** selecteert u **Geleend activum verzenden**.
4. Selecteer het activum en voer de verwachte retourdatum in.
5. Selecteer **OK**.

> [!NOTE]
> - U kunt een geleend activum alleen verzenden als een activum van hetzelfde type beschikbaar is.
> - Het activum dat u leent, moet een levenscyclusstatus hebben waarmee het als geleend activum kan worden gebruikt, zoals **InStorage**. Wanneer het geleende activum wordt geregistreerd, wordt de levenscyclusstatus van het activum automatisch bijgewerkt naar bijvoorbeeld **OnLoan**.

Als u een lijst wilt weergeven met alle activa die u hebt uitgeleend aan andere vestigingen of klanten, selecteert u **Activabeheer** \>**Algemeen** \>**Geleend activum** \>**Alle geleende activa**. Als het selectievakje **Beëindigd** is ingeschakeld voor een activum, is het activum geregistreerd als geretourneerd aan uw bedrijf.

![Onderhoudsaanvragen beheren](media/06-manage-maintenance-requests.png)

Op de pagina **Actieve geleende activa** kunt u een lijst weergeven met alle geleende activa die nog niet aan uw bedrijf zijn geretourneerd.

## <a name="register-loan-assets-as-returned"></a>Geleende activa als geretourneerd registreren

1. Selecteer **Activabeheer** \>**Algemeen** \> **Geleende activa** \> **Actieve geleende activa**. 
2. Selecteer het geleende activum dat u als geretourneerd wilt registreren en selecteer **Geleend activum retourneren**.
3. Voer de datum en de tijd in het veld **Geretourneerd** in.
4. Selecteer **OK**.
5. Vernieuw de pagina met de lijst **Actieve geleende activa** en u ziet dat het geleende activum niet meer op de lijst voorkomt.
