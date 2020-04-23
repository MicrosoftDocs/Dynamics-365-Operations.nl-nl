---
title: Toestandsbeoordeling
description: In dit onderwerp wordt uitgelegd hoe u een sjabloon voor toestandsbeoordeling en registratie voor een activum in Activabeheer maakt.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2694b3ee51e2619a94e7ea2f4039fb52adddbbc
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208910"
---
# <a name="condition-assessment"></a>Toestandsbeoordeling

[!include [banner](../../includes/banner.md)]

 

In dit onderwerp wordt uitgelegd hoe u een sjabloon voor toestandsbeoordeling en registratie voor een activum in Activabeheer maakt. Een toestandsbeoordeling wordt met regelmatige tussenpozen uitgevoerd en het primaire doel is het maken en onderhouden van toestandsgegevens voor activa. Gezien vanuit preventief onderhoud, is het belangrijk om belangrijke informatie te bewaken, zoals de huidige toestand en de resterende levensduur. Bovendien kunt u, als u regelmatig een toestandsbeoordeling uitvoert, de omstandigheden op de machine in uw fabriek bewaken en vergelijken.

Toestandsbeoordeling kan worden gebruikt om veel omstandigheden op uw apparatuur te meten en te bewaken. Voorbeeld: u zou trillingen op uw machines kunnen meten. Nadat u trillingsmetingen hebt vastgelegd in Activabeheer voor verschillende soorten apparatuur, kunt u zoeken naar de meest recengte geregistreerde beoordeling en trillingsmetingen bekijken.

Toestandsbeoordeling wordt uitgevoerd voor activa. U stelt een sjabloon voor toestandsbeoordeling in op een type activum voordat u de procedure voor toestandsbeoordeling gaat uitvoeren. De reden voor het gebruik van sjablonen voor toestandsbeoordeling is om variatie van toestandsgegevens voor vergelijkbare activa te voorkomen. De volgorde voor het instellen en gebruiken van toestandsbeoordeling in Activabeheer is: eerst stelt u de vereiste sjablonen voor toestandsbeoordeling in. Vervolgens koppelt u sjablonen aan activatypen in het formulier **Activatypen**. Tot slot kunt registraties voor toestandsbeoordeling maken voor een activum in het formulier **Activum**.

## <a name="create-a-condition-assessment-template"></a>Een sjabloon voor toestandsbeoordeling maken

1. Selecteer **Activabeheer** > **Instellingen** > **Activatypen** > **Toestandsbeoordeling**.
2. Selecteer **Nieuw** om een nieuwe sjabloon te maken.
3. Typ een id voor de sjabloon in het veld **Sjabloon**.
4. Typ een naam voor de sjabloon in het veld **Naam**.
5. Voeg op het sneltabblad **Toestandsbeoordelingsregels** de regels toe die nodig zijn voor de toestandsbeoordeling, inclusief de selectie van het juiste toestandstype en de maateenheid.
6. Voeg op het sneltabblad **Activatypen** de activatypen toe die gebruik moeten maken van de sjabloon voor toestandsbeoordeling.
7. In de velden **Regels** en **Activatypen** in de groep **Details** boven aan het scherm ziet u het aantal beoordelingsregels en activatypen die zijn gerelateerd aan de geselecteerde sjabloon voor toestandsbeoordeling.


## <a name="create-condition-assessment-registration-on-an-asset"></a>Registratie van toestandsbeoordeling maken voor een activum

1. Selecteer **Activabeheer** > **Algemeen** > **Activa** > **Alle activa**.
2. Selecteer in de lijst het activum waarvoor u een registratie van toestandsbeoordeling wilt maken.
3. Klik op het tabblad **Algemeen** op **Toestandsbeoordeling**.
4. Klik op **Nieuw** om een nieuwe registratie te maken.
5. Selecteer de datum voor de toestandsbeoordeling in het veld **Datum**.
6. Selecteer de naam van de medewerker die de registratie van de toestandsbeoordeling heeft uitgevoerd in het veld **Medewerker**.
7. In het veld **Regels** ziet u het aantal beoordelingsregels dat is ingesteld voor de toestandsbeoordeling.
8. Selecteer een sjabloon voor de toestandsbeoordeling in het veld **Sjabloon**. De naam van de sjabloon wordt automatisch ingevoegd in het veld **Naam** en de gerelateerde registratieregels worden ingevoegd op het sneltabblad **Toestandsbeoordelingsregels**.
9. U kunt notities invoegen die betrekking hebben op de geselecteerde toestandsbeoordeling op het sneltabblad **Notities**.
10. Voeg voor elke toestandsbeoordelingsregel meetgegevens in het veld **Waarde** in.
11. U kunt een opmerking met betrekking tot de geselecteerde registratieregel invoegen op het sneltabblad **Toestandsbeoordelingsregels** > veld **Opmerkingen**. Als u een opmerking op een regel toevoegt, wordt het selectievakje **Opmerking** automatisch ingeschakeld.

Nadat u een toestandsbeoordelingsregistratie voor een activum hebt gemaakt, kunt u een rapport voor toestandsbeoordeling afdrukken.

>[!NOTE]
>U kunt ook de toestandsbeoordeling voor een werkorder registreren (**Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** > knop **Toestandsbeoordeling**).
