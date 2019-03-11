---
title: Gegevensbronnen voor het hele bedrijf in de elektronische aangifte (ER)
description: In dit onderwerp wordt uitgelegd hoe u gegevensbronnen voor meerdere bedrijven kunt gebruiken in elektronische rapportage (ER).
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 3ff94c49eed378d92e995782e73d76d669b44292
ms.sourcegitcommit: 2ebea3cbddfa0a5ef0e0fd13d3693da6152bc288
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/30/2019
ms.locfileid: "351971"
---
# <a name="cross-company-data-sources-in-electronic-reporting-er"></a>Gegevensbronnen voor het hele bedrijf in de elektronische aangifte (ER)

[!include[banner](../includes/banner.md)]

U kunt ER-indelingen (elektronische rapportage) ontwerpen om uitgaande documenten te genereren in verschillende indelingen. Wanneer een document wordt gegenereerd, roept een ER-indeling gegevensbronnen aan die zijn geconfigureerd in een corresponderende ER-modeltoewijzing. Als u toegang wilt configureren tot toepassingstabellen voor het ophalen van records, kunt u ER-gegevensbronnen van het type **Tabelrecords** gebruiken. Wanneer de tabel die toegang krijgt een gedeelde tabel is (een tabel waarin gegevens worden opgeslagen zonder een bedrijfs-id), retourneert deze gegevensbron alle records. Wanneer de tabel die toegang krijgt, een bedrijfsafhankelijke tabel is (dat wil zeggen, een tabel waarin gegevens worden opgeslagen per bedrijf), retourneert deze gegevensbron alleen de records die zijn opgeslagen voor het huidige bedrijf (dat wil zeggen, de bedrijfscontext waaronder de ER-indeling wordt uitgevoerd).

Elke gegevensbron van het type **Tabelrecords** in een modeltoewijzing kan nu worden gemarkeerd als gegevensbron voor meerdere bedrijven. Daarom kunt u gegevensbronnen van het type **Tabelrecords** gebruiken om toegang te krijgen tot gegevens voor meerdere bedrijven in toepassingstabellen.

Als u een gegevensbron als voor meerdere bedrijven markeert, treedt het volgende gedrag op:

- Voor een gegevensbron die naar een gedeelde tabel verwijst, behalve CompanyInfo, retourneert de gegevensbron alle records die bestaan in de tabel waarnaar wordt verwezen. 
- Voor een gegevensbron die naar de tabel CompanyInfo verwijst, ook al is CompanyInfo een gedeelde tabel, retourneert de gegevensbron de records met de id van een bedrijf in het gedefinieerde bereik.
- Voor een bedrijfsafhankelijke tabel retourneert de gegevensbron de records van de tabel waarnaar wordt verwezen die de id bevatten van een bedrijf uit het gedefinieerde bereik.

In het systeemquerydialoogvenster, wanneer de optie **Vragen om query** is ingeschakeld voor een gegevensbron die is gemarkeerd als voor meerdere bedrijven, kunt u handmatig een of meer bedrijven selecteren om op te nemen op het tabblad **Bedrijfsbereik**.

> [!IMPORTANT]
> Net als andere filters blijft het bedrijfsfilter behouden als laatst gebruikte waarde voor query's wanneer u een ER-indeling uitvoert. Het filter wordt niet automatisch gewijzigd als u de waarde voor meerdere bedrijven voor een gegevensbron wijzigt. Als u een andere waarde voor meerdere bedrijven wilt gebruiken voor een andere gegevensbron, verwijdert u de corresponderende gebruikersspecifieke sectie.

Voor elke gegevensbron die is gemarkeerd als voor meerdere bedrijven, kunt u de gewenste records selecteren met behulp van de functies **FILTER** en **WHERE** in ER-expressies. Het veld **dataAreaID** veld kan ook worden gebruikt als een bedrijfs-id. Op dit moment is het veld **dataAreaID** beperkt tot de volgende typen voorwaarden wanneer de functie **FILTER** wordt gebruikt:

- Alleen voorwaarden die één veldvergelijking **dataAreaID** hebben, worden ondersteund.
- Alleen vergelijkingen met expressies die niet afhankelijk zijn van lijstitems van records zijn toegestaan.

Daarom is de volgende expressie geldig.

```
FILTER (MyTable, MyTable.dataAreaID = $StringUserInputParameter)
While shown below expressions will not pass the validation:
FILTER (MyTable, MyTable.dataAreaID = MyTable2RecordsList.MyField)
FILTER (MyTable, 
    OR(
        MyTable.dataAreaID = $StringUserInputParameter1,
        MyTable.dataAreaID = $StringUserInputParameter2
    )
)
```

Het bereik omvat standaard alle bedrijven van de huidige toepassing. Het kan echter worden beperkt. Als u het bereik van toegang tot gegevens voor meerdere bedrijven voor één ER-indeling wilt beperken, wijst u een specifieke organisatiehiërarchie aan de indeling toe. Wanneer een hiërarchie is gedefinieerd voor een ER-indeling, worden alleen records voor rechtspersonen die worden vertegenwoordigd in de hiërarchie, geretourneerd, zelfs als de indeling gegevensbronnen voor meerdere bedrijven aanroept. Wanneer een verwijzing naar een hiërarchie die niet meer bestaat, wordt gedefinieerd voor een ER-indeling, wordt het standaardbereik toegepast en roept de indeling gegevensbronnen voor meerdere bedrijven aan. In deze situatie worden records voor alle toepassingsbedrijven geretourneerd.

Houd er rekening mee dat wanneer de optie **Concept gebruiken** is ingeschakeld voor de toegewezene aan een enkele ER-indeling-organisatiehiërarchie, de rechtspersonen uit de conceptversie van deze hiërarchie worden gebruikt om het bereik te identificeren voor gegevensbronnen voor meerdere bedrijven. Als de conceptversie niet bestaat, worden de rechtspersonen uit de laatst gepubliceerde versie van deze organisatiehiërarchie hiervoor gebruikt.

Houd er rekening mee dat wanneer de optie **Concept gebruiken** is uitgeschakeld voor de toegewezene aan een enkele ER-indeling-organisatiehiërarchie, de rechtspersonen uit de laatst gepubliceerde versie van deze hiërarchie worden gebruikt om het bereik te identificeren voor gegevensbronnen voor meerdere bedrijven. Datumeffectiviteit van organisatiehiërarchieën wordt nog niet ondersteund in het ER-raamwerk.

De hiërarchie kan worden toegewezen aan een indeling op een bepaalde pagina die kan worden geopend vanuit het ER-werkgebied of met behulp van de menuoptie **Organisatiebeheer \> Elektronische rapportage \> Filter voor indelingen rechtspersoon**. Voor toegang tot de pagina moet de bevoegdheid , de **Filters voor indelingen van rechtspersonen onderhouden** (ERMaintainFormatMappingLegalEntityFilters) worden verleend aan een gebruiker. De bereikbeperking van op hiërarchie gebaseerde rechtspersonen voor de indeling wordt toegepast naast de beperking die de gebruiker handmatig kan opgeven in het systeemquerydialoogvenster. Het snijpunt van deze beperkingen wordt gebruikt wanneer de indeling wordt uitgevoerd.

Voor meer informatie over deze functie speelt u de taakbegeleiding **ER-toegang tot records van bedrijfsafhankelijke tabellen in de modus voor meerdere bedrijven** af, die deel uitmaakt van het bedrijfsproces 7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677) en kan worden gedownload uit het [Microsoft Downloadcentrum](https://go.microsoft.com/fwlink/?linkid=874684). Deze taakbegeleiding begeleidt u door het proces van het configureren van een ER-modeltoewijzing en ER-indeling om toegang tot toepassingstabellen te krijgen in de modus voor meerdere bedrijven.

Download de volgende bestanden om de taakbegeleiding te voltooien:

- [ER-modelconfiguratie - CrossCompanyDataAccessModel.xml](https://go.microsoft.com/fwlink/?linkid=874111)
- [ER-indelingsconfiguratie - CrossCompanyDataAccessFormat.xml](https://go.microsoft.com/fwlink/?linkid=874111)
