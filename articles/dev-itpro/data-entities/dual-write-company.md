---
title: Bedrijfsconcept in Common Data Service
description: In dit onderwerp wordt de integratie van bedrijfsgegevens tussen Finance and Operations en Common Data Service beschreven.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 6eddd87c3ad3ea9de8aec2874b0514faa65374f1
ms.sourcegitcommit: 02c223b44ac7196df675afac61c6783f467d1983
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/24/2019
ms.locfileid: "1789174"
---
## <a name="company-concept-in-common-data-service"></a>Bedrijfsconcept in Common Data Service

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

In Microsoft Dynamics 365 for Finance and Operations is het concept *bedrijf* zowel een juridische constructie als een bedrijfsconstructie. Het is ook een beveiligings- en zichtbaarheidsgrens voor gegevens. Gebruikers werken altijd in de context van één bedrijf en de meeste gegevens zijn verdeeld per bedrijf.

Common Data Service heeft geen gelijkwaardig concept. Het concept dat het meest overeenkomt, is *bedrijfseenheid*, wat in de eerste plaats een beveiligings- en zichtbaarheidsgrens is voor gebruikersgegevens. Dit concept heeft niet dezelfde juridische of zakelijke implicaties als het bedrijfsconcept in Finance and Operations.

Omdat bedrijfseenheid en bedrijf geen gelijkwaardige concepten zijn, is het niet mogelijk om een 1:1-toewijzing (één-op-één) tussen beide te forceren met het oog op Common Data Service-integratie. Maar omdat gebruikers standaard in Finance and Operations dezelfde records moeten kunnen zien als in Common Data Service, heeft Microsoft een nieuwe entiteit in Common Data Service geïntroduceerd met de naam cdm\_Company. Deze entiteit is gelijk aan de entiteit Bedrijf in Finance and Operations. Om te garanderen dat de zichtbaarheid van records out of the box equivalent is tussen Finance and Operations en Common Data Service, raden we de volgende instellingen voor Common Data Service-gegevens aan:

+ Voor elke Finance and Operations-bedrijfsrecord die is ingeschakeld voor Twee keer wegschrijven, wordt een bijbehorende cdm\_Company-record gemaakt.
+ Wanneer een cdm\_Company-record is gemaakt en is ingeschakeld voor Twee keer wegschrijven, wordt er een standaardbedrijfseenheid met dezelfde naam gemaakt. Hoewel er automatisch een standaardteam voor die bedrijfseenheid wordt gemaakt, wordt de bedrijfseenheid niet gebruikt.
+ Er wordt een afzonderlijk eigenaarsteam gemaakt dat dezelfde naam heeft. Het wordt ook gekoppeld aan de bedrijfseenheid.
+ De eigenaar van een record die is gemaakt in Finance and Operations en twee keer wordt weggeschreven naar Common Data Service, wordt standaard ingesteld op het team 'DW eigenaar' dat is gekoppeld aan de betreffende bedrijfseenheid.

In de volgende afbeelding ziet u een voorbeeld van deze gegevensinstelling in Common Data Service.

![Gegevensinstelling in Common Data Service](media/dual-write-company-1.png)

Vanwege deze configuratie is elke Finance and Operations-record die is gerelateerd aan het bedrijf USMF, eigendom van een team dat is gekoppeld aan de bedrijfseenheid USMF in Common Data Service. Daarom kunnen gebruikers die toegang hebben tot die bedrijfseenheid via een beveiligingsrol die is ingesteld op zichtbaarheid op bedrijfseenheidsniveau, deze records nu zien. In het volgende voorbeeld ziet u hoe teams kunnen worden gebruikt om de juiste toegang tot deze records te bieden.

+ De rol Verkoopmanager wordt toegewezen aan leden van het team USMF Sales.
+ Gebruikers met de rol Verkoopmanager hebben toegang tot alle accountrecords die lid zijn van dezelfde bedrijfseenheid waarvan ze lid zijn.
+ Het team USMF Sales is gekoppeld aan de bedrijfseenheid USMF die eerder is vermeld.
+ Daarom kunnen leden van het team USMF Sales elk account zien dat eigendom is van de gebruiker USMF DW, die afkomstig zou zijn van de bedrijfsentiteit USMF in Finance and Operations.

![Hoe teams kunnen worden gebruikt](media/dual-write-company-2.png)

Zoals u in de voorgaande afbeelding kunt zien, is deze 1:1-toewijzing tussen bedrijfseenheid, bedrijf en team slechts een beginpunt. In dit voorbeeld wordt in Common Data Service handmatig een nieuwe bedrijfseenheid Europa gemaakt als bovenliggend element voor zowel DEMF als ESMF. Deze nieuwe bedrijfseenheid in de basismap is niet gerelateerd aan Twee keer wegschrijven. Deze kan echter worden gebruikt om leden van het team EUR Sales toegang te geven tot accountgegevens in zowel DEMF als ESMF, door de zichtbaarheid van gegevens in te stellen op **Bovenliggende/onderliggende bedrijfseenheid** in de bijbehorende beveiligingsrol.

In een laatste onderwerp wordt beschreven hoe Twee keer wegschrijven bepaalt aan welk eigenaarsteam records moeten worden toegewezen. Dit gedrag wordt bepaald met het veld **Standaardeigenaarsteam** van de record cdm\_Company. Wanneer een cdm\_Company-record is ingeschakeld voor Twee keer wegschrijven, maakt een invoegtoepassing automatisch de gekoppelde bedrijfseenheid en het eigenaarsteam (als dit nog niet bestaat) en wordt het veld **Standaardeigenaarsteam** ingesteld. De beheerder kan dit veld wijzigen in een andere waarde. De beheerder kan het veld echter niet wissen zolang de entiteit is ingeschakeld voor Twee keer wegschrijven.

![Veld Standaardeigenaarsteam](media/dual-write-default-owning-team.jpg)

## <a name="company-striping-and-bootstrapping"></a>Bedrijfsstriping en -bootstrapping

Common Data Service-integratie bewerkstelligt bedrijfspariteit door een bedrijfs-id te gebruiken om gegevens te stripen. Zoals u in de volgende afbeelding kunt zien, worden alle bedrijfsspecifieke entiteiten uitgebreid zodat ze een N:1-relatie (veel-op-één) hebben met de entiteit cdm\_Company.

![N:1-relatie tussen een bedrijfsspecifieke entiteit en de entiteit cdm_Company](media/dual-write-bootstrapping.png)

+ De waarde voor records wordt alleen-lezen nadat een bedrijf is toegevoegd en opgeslagen. Dat betekent dat gebruikers ervoor moeten zorgen dat ze het juiste bedrijf selecteren.
+ Alleen records met bedrijfsgegevens komen in aanmerking voor Twee keer wegschrijven tussen Finance and Operations en Common Data Service.
+ Voor bestaande Common Data Service-gegevens zal binnenkort een door de beheerder geleide bootstrap-ervaring beschikbaar zijn.
