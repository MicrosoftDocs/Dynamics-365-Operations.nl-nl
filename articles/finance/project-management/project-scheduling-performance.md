---
title: Prestaties van projectresourceplanning
description: Dit onderwerp bevat informatie over het verbeteren van de prestaties van de resourceplanning voor een groot aantal projecten.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 988fc83230f08a6534caa7c37784757d73c1cc12
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760519"
---
# <a name="project-resource-scheduling-performance"></a>Prestaties van projectresourceplanning

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Prestatieproblemen met betrekking tot resourceplanning kunnen zich voordoen wanneer het aantal projecten in de duizenden loopt. Als u de prestaties van de resourceplanning wilt verbeteren, is er een functie beschikbaar waarmee gebruikers de tijd kunnen beperken die nodig is om het formulier voor resourcebeschikbaarheid te starten. Hiermee verwijdert u het synchronisatieproces voor de vergaarde resourcecapaciteit en u gebruikt de tabel **ResProjectResource** om het opzoeken van resources te versnellen. De tabel **ResRollup** wordt niet meer gebruikt.

> [!IMPORTANT]
> Als er een afhankelijkheid van het synchronisatieproces voor de vergaarde resourcecapaciteit of de tabel **ResprojectResource** bestaat, gebruikt u deze functie niet.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Prestatieverbetering voor resourceplanning inschakelen
Voer de volgende stappen uit om de prestatieverbetering voor resourceplanning in te schakelen.

1. Ga naar **Functiebeheer** > **Alle** en zoek in de lijst met functies naar **Functie voor verbetering van prestaties van projectresourceplanning inschakelen**.
2. Selecteer **Nu inschakelen**.

> [!NOTE]
> Als u de functie niet kunt vinden in de lijst, selecteert u **Controleren op updates** om de lijst te vernieuwen.

3. Vernieuw de browser en ga vervolgens naar **Projectbeheer en boekhouding** > **Periodiek** > **Projectresources** > **Capaciteit van resourcekalenders synchroniseren voor alle bedrijven**.
4. Stel **Bestaande capaciteitsrecords verwijderen** in op **Ja** als u eerdere gegevens wilt verwijderen. Als u incrementele gegevens wilt genereren, stelt u deze optie in op **Nee**.
5. Selecteer in het veld **Periodecode** de periode waarin gegevens moeten worden gegenereerd. Als u een periodecode selecteert, hoeft u geen begin- en einddatum te definiëren.
6. Als u het veld **Periodecode** leeg laat, selecteert u specifieke begin- en einddatums om gegevens te genereren.
7. Selecteer **OK**.

 > [!NOTE]
 > Er worden nu algemene gegevens naar de tabel **ResCalendarCapacity** gedistribueerd voor alle bedrijven in uw omgeving, zodat de batchtaak alleen in één rechtspersoon hoeft te worden uitgevoerd. De gegevens in deze batchtaak zijn nodig om de resourcecapaciteit te berekenen via de bijbehorende kalender.

8. Ga naar **Projectbeheer en boekhouding** > **Periodiek** > **Projectresources** > **Projectresources invullen voor alle bedrijven** en selecteer **OK**. Dit is het script voor gegevensupgrades voor algemene gegevens in de tabellen **ResProjectResource**, **ResCalendarDateTimeRange** en **ResEffectiveDateTimeRange**. Waarden voor het veld **PSAPRojSchedRole.RootActivity** worden ook bijgewerkt. Als deze bewerking niet wordt uitgevoerd, wordt een waarschuwing weergegeven wanneer u probeert om resourceplanningsbewerkingen uit te voeren.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Prestatieverbetering voor resourceplanning uitschakelen

1. Ga naar **Functiebeheer** > **Alle** en zoek naar **Functie voor verbetering van prestaties van projectresourceplanning inschakelen**.
2. Selecteer de functie en de knop **Uitschakelen**.
3. Vernieuw de browser.
4. Ga naar **Projectbeheer en boekhouding** > **Periodiek** > **Capaciteitsynchronisatie** > **Vergaarde resourcecapaciteit synchroniseren**.
5. Stel op de pagina **Synchronisatie van vergaarde capaciteit** de optie **Bestaande capaciteitsrecords verwijderen** in op **Ja** om eerdere gegevens te verwijderen. Als u incrementele gegevens wilt genereren, stelt u deze optie in op **Nee**.
6. Selecteer in het veld **Periodecode** de periode waarin gegevens moeten worden gegenereerd. Als u een periodecode selecteert, hoeft u geen begin- en einddatum te definiëren.
7. Als u het veld **Periodecode** leeg laat, selecteert u specifieke begin- en einddatums om gegevens te genereren.
8. Selecteer **OK**.

> [!NOTE]
> Er worden nu algemene gegevens naar de tabel **ResRollup** gedistribueerd voor alle bedrijven in uw omgeving, zodat de batchtaak alleen in één rechtspersoon hoeft te worden uitgevoerd. Deze batchtaak is nodig voor alle weergaven **Beschikbaarheid van resource**. Als deze batchtaak niet wordt uitgevoerd, worden de gegevens in **ResRollup** al doende gegenereerd. Dit kan tijd kosten.
