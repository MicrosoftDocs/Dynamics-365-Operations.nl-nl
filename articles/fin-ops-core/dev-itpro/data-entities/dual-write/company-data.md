---
title: Bedrijfsconcept in Common Data Service
description: In dit onderwerp wordt de integratie van bedrijfsgegevens tussen Finance and Operations en Common Data Service beschreven.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/04/2020
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
ms.openlocfilehash: 444bfc1698a206ca34e67f742df63431a3b02649
ms.sourcegitcommit: 7da8811f1a7db858efb76edb0bdf857a47d07600
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/27/2020
ms.locfileid: "3728408"
---
# <a name="company-concept-in-common-data-service"></a>Bedrijfsconcept in Common Data Service

[!include [banner](../../includes/banner.md)]


In Finance and Operations is het concept *bedrijf* zowel een juridische constructie als een bedrijfsconstructie. Het is ook een beveiligings- en zichtbaarheidsgrens voor gegevens. Gebruikers werken altijd in de context van één bedrijf en de meeste gegevens zijn verdeeld per bedrijf.

Common Data Service heeft geen gelijkwaardig concept. Het concept dat het meest overeenkomt, is *bedrijfseenheid*, wat in de eerste plaats een beveiligings- en zichtbaarheidsgrens is voor gebruikersgegevens. Dit concept heeft niet dezelfde juridische of zakelijke implicaties als het bedrijfsconcept.

Omdat bedrijfseenheid en bedrijf geen gelijkwaardige concepten zijn, is het niet mogelijk om een 1:1-toewijzing (één-op-één) tussen beide te forceren met het oog op Common Data Service-integratie. Maar omdat gebruikers standaard in de toepassing dezelfde records moeten kunnen zien als in Common Data Service, heeft Microsoft een nieuwe entiteit in Common Data Service geïntroduceerd met de naam cdm\_Company. Deze entiteit is gelijk aan de entiteit Bedrijf in de toepassing. Om te garanderen dat de zichtbaarheid van records out of the box equivalent is tussen de toepassing en Common Data Service, raden we de volgende instellingen voor Common Data Service-gegevens aan:

+ Voor elke Finance and Operations-bedrijfsrecord die is ingeschakeld voor Twee keer wegschrijven, wordt een bijbehorende cdm\_Bedrijfsrecord gemaakt.
+ Wanneer een cdm\_Company-record is gemaakt en is ingeschakeld voor Twee keer wegschrijven, wordt er een standaardbedrijfseenheid met dezelfde naam gemaakt. Hoewel er automatisch een standaardteam voor die bedrijfseenheid wordt gemaakt, wordt de bedrijfseenheid niet gebruikt.
+ Er wordt een afzonderlijk eigenaarsteam gemaakt dat dezelfde naam heeft. Het wordt ook gekoppeld aan de bedrijfseenheid.
+ De eigenaar van een record die is gemaakt en twee keer wordt weggeschreven naar Common Data Service, wordt standaard ingesteld op het team 'DW eigenaar' dat is gekoppeld aan de betreffende bedrijfseenheid.

In de volgende afbeelding ziet u een voorbeeld van deze gegevensinstelling in Common Data Service.

![Gegevensinstelling in Common Data Service](media/dual-write-company-1.png)

Vanwege deze configuratie is elke record die is gerelateerd aan het bedrijf USMF, eigendom van een team dat is gekoppeld aan de bedrijfseenheid USMF in Common Data Service. Daarom kunnen gebruikers die toegang hebben tot die bedrijfseenheid via een beveiligingsrol die is ingesteld op zichtbaarheid op bedrijfseenheidsniveau, deze records nu zien. In het volgende voorbeeld ziet u hoe teams kunnen worden gebruikt om de juiste toegang tot deze records te bieden.

+ De rol Verkoopmanager wordt toegewezen aan leden van het team USMF Sales.
+ Gebruikers met de rol Verkoopmanager hebben toegang tot alle accountrecords die lid zijn van dezelfde bedrijfseenheid waarvan ze lid zijn.
+ Het team USMF Sales is gekoppeld aan de bedrijfseenheid USMF die eerder is vermeld.
+ Daarom kunnen leden van het team USMF Sales elk account zien dat eigendom is van de gebruiker USMF DW, die afkomstig zou zijn van de bedrijfsentiteit USMF in Finance and Operations.

![Hoe teams kunnen worden gebruikt](media/dual-write-company-2.png)

Zoals u in de voorgaande afbeelding kunt zien, is deze 1:1-toewijzing tussen bedrijfseenheid, bedrijf en team slechts een beginpunt. In dit voorbeeld wordt in Common Data Service handmatig een nieuwe bedrijfseenheid Europa gemaakt als bovenliggend element voor zowel DEMF als ESMF. Deze nieuwe bedrijfseenheid in de basismap is niet gerelateerd aan Twee keer wegschrijven. Deze kan echter worden gebruikt om leden van het team EUR Sales toegang te geven tot accountgegevens in zowel DEMF als ESMF, door de zichtbaarheid van gegevens in te stellen op **Bovenliggende/onderliggende bedrijfseenheid** in de bijbehorende beveiligingsrol.

In een laatste onderwerp wordt beschreven hoe Twee keer wegschrijven bepaalt aan welk eigenaarsteam records moeten worden toegewezen. Dit gedrag wordt bepaald met het veld **Standaardeigenaarsteam** van de record cdm\_Company. Wanneer een cdm\_Company-record is ingeschakeld voor Twee keer wegschrijven, maakt een invoegtoepassing automatisch de gekoppelde bedrijfseenheid en het eigenaarsteam (als dit nog niet bestaat) en wordt het veld **Standaardeigenaarsteam** ingesteld. De beheerder kan dit veld wijzigen in een andere waarde. De beheerder kan het veld echter niet wissen zolang de entiteit is ingeschakeld voor Twee keer wegschrijven.

> [!div class="mx-imgBorder"]
![Veld Standaardeigenaarsteam](media/dual-write-default-owning-team.jpg)

## <a name="company-striping-and-bootstrapping"></a>Bedrijfsstriping en -bootstrapping

Common Data Service-integratie bewerkstelligt bedrijfspariteit door een bedrijfs-id te gebruiken om gegevens te stripen. Zoals u in de volgende afbeelding kunt zien, worden alle bedrijfsspecifieke entiteiten uitgebreid zodat ze een N:1-relatie (veel-op-één) hebben met de entiteit cdm\_Company.

> [!div class="mx-imgBorder"]
![N:1-relatie tussen een bedrijfsspecifieke entiteit en de entiteit cdm_Company](media/dual-write-bootstrapping.png)

+ De waarde voor records wordt alleen-lezen nadat een bedrijf is toegevoegd en opgeslagen. Dat betekent dat gebruikers ervoor moeten zorgen dat ze het juiste bedrijf selecteren.
+ Alleen records met bedrijfsgegevens komen in aanmerking voor Twee keer wegschrijven tussen de toepassing en Common Data Service.
+ Voor bestaande Common Data Service-gegevens zal binnenkort een door de beheerder geleide bootstrap-ervaring beschikbaar zijn.


## <a name="autopopulate-company-name-in-customer-engagement-apps"></a>Bedrijfsnaam automatisch invullen in Customer Engagement-apps

Er zijn verschillende manieren waarop u de bedrijfsnaam in Customer Engagement-apps automatisch kunt laten invullen.

+ Als u een systeembeheerder bent, kunt u het standaardbedrijf instellen door te navigeren naar **Geavanceerde instellingen > Systeem > Beveiliging > Gebruikers**. Open het formulier **Gebruikers** en stel in de sectie **Organisatiegegevens** de waarde van **Standaardbedrijf in formulieren** in.

    :::image type="content" source="media/autopopulate-company-name-1.png" alt-text="Sectie Standaardbedrijf instellen in Organisatiegegevens.":::

+ Als u **schrijf**toegang hebt tot de entiteit **SystemUser** op het niveau van **Bedrijfseenheid**, kunt u het standaardbedrijf op elk willekeurig formulier wijzigen door een bedrijf te selecteren in de vervolgkeuzelijst **Bedrijf**.

    :::image type="content" source="media/autopopulate-company-name-2.png" alt-text="De bedrijfsnaam wijzigen voor een nieuw account.":::

+ Als u **schrijf**toegang hebt tot gegevens in meerdere bedrijven, kunt u het standaardbedrijf wijzigen door een record te kiezen die tot een ander bedrijf behoort.

    :::image type="content" source="media/autopopulate-company-name-3.png" alt-text="Als u een record kiest, wordt het standaardbedrijf gewijzigd.":::

+ Als u een systeemconfigurator of -beheerder bent en u de bedrijfsgegevens in een aangepast formulier automatisch wilt laten invullen, dan kunt u [formuliergebeurtenissen](https://docs.microsoft.com/powerapps/developer/model-driven-apps/clientapi/events-forms-grids) gebruiken. Voeg een JavaScript-verwijzing toe aan **msdyn_/DefaultCompany.js** en gebruik de volgende gebeurtenissen. U kunt elk kant-en-klaar formulier gebruiken, bijvoorbeeld het formulier **Account**.

    + **OnLoad**-gebeurtenissen voor het formulier: stel het veld **defaultCompany** in.
    + **OnChange**-gebeurtenis voor het veld **Bedrijf**: stel het veld **updateDefaultCompany** in.

## <a name="apply-filtering-based-on-the-company-context"></a>Filters toepassen op basis van de bedrijfscontext

Als u filters op basis van de bedrijfscontext wilt toepassen op uw aangepaste formulieren of op aangepaste opzoekvelden die zijn toegevoegd aan de standaardformulieren, open dan het formulier en gebruik de sectie **Gerelateerde records filteren** om het bedrijfsfilter toe te passen. U moet dit instellen voor elk opzoekveld dat een filter op basis van het onderliggende bedrijf voor een bepaalde record vereist. In de volgende afbeelding wordt de instelling weergegeven voor **Account**.

:::image type="content" source="media/apply-company-context.png" alt-text="Bedrijfscontext toepassen":::

