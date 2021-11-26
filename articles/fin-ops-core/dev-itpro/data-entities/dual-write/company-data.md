---
title: Bedrijfsconcept in Dataverse
description: In dit onderwerp wordt de integratie van bedrijfsgegevens tussen Finance and Operations en Dataverse beschreven.
author: RamaKrishnamoorthy
ms.date: 08/04/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 25bd2cc0df4940f02313b3a61f69b2273e835639
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782080"
---
# <a name="company-concept-in-dataverse"></a>Bedrijfsconcept in Dataverse

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


In Finance and Operations is het concept *bedrijf* zowel een juridische constructie als een bedrijfsconstructie. Het is ook een beveiligings- en zichtbaarheidsgrens voor gegevens. Gebruikers werken altijd in de context van één bedrijf en de meeste gegevens zijn verdeeld per bedrijf.

Dataverse heeft geen gelijkwaardig concept. Het concept dat het meest overeenkomt, is *bedrijfseenheid*, wat in de eerste plaats een beveiligings- en zichtbaarheidsgrens is voor gebruikersgegevens. Dit concept heeft niet dezelfde juridische of zakelijke implicaties als het bedrijfsconcept.

Omdat bedrijfseenheid en bedrijf geen gelijkwaardige concepten zijn, is het niet mogelijk om een 1:1-toewijzing (één-op-één) tussen beide te forceren met het oog op Dataverse-integratie. Maar omdat gebruikers standaard in de toepassing dezelfde rijen moeten kunnen zien als in Dataverse, heeft Microsoft een nieuwe tabel in Dataverse geïntroduceerd met de naam cdm\_Company. Deze tabel is gelijk aan de tabel Bedrijf in de toepassing. Om te garanderen dat de zichtbaarheid van rijen standaard equivalent is tussen de toepassing en Dataverse, raden we de volgende instellingen voor Dataverse-gegevens aan:

+ Voor elke Finance and Operations-bedrijfsrij die is ingeschakeld voor Twee keer wegschrijven, wordt een bijbehorende cdm\_Bedrijfsrij gemaakt.
+ Wanneer een cdm\_Company-rij is gemaakt en is ingeschakeld voor Twee keer wegschrijven, wordt er een standaardbedrijfseenheid met dezelfde naam gemaakt. Hoewel er automatisch een standaardteam voor die bedrijfseenheid wordt gemaakt, wordt de bedrijfseenheid niet gebruikt.
+ Er wordt een afzonderlijk eigenaarsteam gemaakt dat dezelfde naam heeft. Het wordt ook gekoppeld aan de bedrijfseenheid.
+ De eigenaar van een rij die is gemaakt en twee keer wordt weggeschreven naar Dataverse, wordt standaard ingesteld op het team 'DW eigenaar' dat is gekoppeld aan de betreffende bedrijfseenheid.

In de volgende afbeelding ziet u een voorbeeld van deze gegevensinstelling in Dataverse.

![Gegevensinstelling in Dataverse.](media/dual-write-company-1.png)

Vanwege deze configuratie is elke rij die is gerelateerd aan het bedrijf USMF, eigendom van een team dat is gekoppeld aan de bedrijfseenheid USMF in Dataverse. Daarom kunnen gebruikers die toegang hebben tot die bedrijfseenheid via een beveiligingsrol die is ingesteld op zichtbaarheid op bedrijfseenheidsniveau, deze rijen nu zien. In het volgende voorbeeld ziet u hoe teams kunnen worden gebruikt om de juiste toegang tot deze rijen te bieden.

+ De rol Verkoopmanager wordt toegewezen aan leden van het team USMF Sales.
+ Gebruikers met de rol Verkoopmanager hebben toegang tot alle accountrijen die lid zijn van dezelfde bedrijfseenheid waarvan ze lid zijn.
+ Het team USMF Sales is gekoppeld aan de bedrijfseenheid USMF die eerder is vermeld.
+ Daarom kunnen leden van het team USMF Sales elk account zien dat eigendom is van de gebruiker USMF DW, die afkomstig zou zijn van de bedrijfstabel USMF in Finance and Operations.

![Hoe teams kunnen worden gebruikt.](media/dual-write-company-2.png)

Zoals u in de voorgaande afbeelding kunt zien, is deze 1:1-toewijzing tussen bedrijfseenheid, bedrijf en team slechts een beginpunt. In dit voorbeeld wordt in Dataverse handmatig een nieuwe bedrijfseenheid Europa gemaakt als bovenliggend element voor zowel DEMF als ESMF. Deze nieuwe bedrijfseenheid in de basismap is niet gerelateerd aan Twee keer wegschrijven. Deze kan echter worden gebruikt om leden van het team EUR Sales toegang te geven tot accountgegevens in zowel DEMF als ESMF, door de zichtbaarheid van gegevens in te stellen op **Bovenliggende/onderliggende bedrijfseenheid** in de bijbehorende beveiligingsrol.

In een laatste onderwerp wordt beschreven hoe Twee keer wegschrijven bepaalt aan welk eigenaarsteam rijen moeten worden toegewezen. Dit gedrag wordt bepaald met de kolom **Standaardeigenaarsteam** van de cdm\_Company-rij. Wanneer een cdm\_Company-rij is ingeschakeld voor Twee keer wegschrijven, maakt een invoegtoepassing automatisch de gekoppelde bedrijfseenheid en het eigenaarsteam (als dit nog niet bestaat) en wordt de kolom **Standaardeigenaarsteam** ingesteld. De beheerder kan deze kolom wijzigen in een andere waarde. De beheerder kan de kolom echter niet wissen zolang de tabel is ingeschakeld voor Twee keer wegschrijven.

> [!div class="mx-imgBorder"]
![Kolom Standaardeigenaarsteam.](media/dual-write-default-owning-team.jpg)

## <a name="company-striping-and-bootstrapping"></a>Bedrijfsstriping en -bootstrapping

Dataverse-integratie bewerkstelligt bedrijfspariteit door een bedrijfs-id te gebruiken om gegevens te stripen. Zoals u in de volgende afbeelding kunt zien, worden alle bedrijfsspecifieke tabellen uitgebreid zodat ze een N:1-relatie (veel-op-één) hebben met de tabel cdm\_Company.

> [!div class="mx-imgBorder"]
![N:1-relatie tussen een bedrijfsspecifieke tabel en de tabel cdm_Company.](media/dual-write-bootstrapping.png)

+ De waarde voor rijen wordt alleen-lezen nadat een bedrijf is toegevoegd en opgeslagen. Dat betekent dat gebruikers ervoor moeten zorgen dat ze het juiste bedrijf selecteren.
+ Alleen rijen met bedrijfsgegevens komen in aanmerking voor Twee keer wegschrijven tussen de toepassing en Dataverse.
+ Voor bestaande Dataverse-gegevens zal binnenkort een door de beheerder geleide bootstrap-ervaring beschikbaar zijn.


## <a name="autopopulate-company-name-in-customer-engagement-apps"></a>Bedrijfsnaam automatisch invullen in Customer Engagement-apps

Er zijn verschillende manieren waarop u de bedrijfsnaam in Customer Engagement-apps automatisch kunt laten invullen.

+ Als u een systeembeheerder bent, kunt u het standaardbedrijf instellen door te navigeren naar **Geavanceerde instellingen > Systeem > Beveiliging > Gebruikers**. Open het formulier **Gebruikers** en stel in de sectie **Organisatiegegevens** de waarde van **Standaardbedrijf in formulieren** in.

    :::image type="content" source="media/autopopulate-company-name-1.png" alt-text="Sectie Standaardbedrijf instellen in Organisatiegegevens.":::

+ Als u **schrijf** toegang hebt tot de tabel **SystemUser** op het niveau van **Bedrijfseenheid**, kunt u het standaardbedrijf op elk willekeurig formulier wijzigen door een bedrijf te selecteren in de vervolgkeuzelijst **Bedrijf**.

    :::image type="content" source="media/autopopulate-company-name-2.png" alt-text="De bedrijfsnaam wijzigen voor een nieuw account.":::

+ Als u **schrijf** toegang hebt tot gegevens in meerdere bedrijven, kunt u het standaardbedrijf wijzigen door een rij te kiezen die tot een ander bedrijf behoort.

    :::image type="content" source="media/autopopulate-company-name-3.png" alt-text="Als u een rij kiest, wordt het standaardbedrijf gewijzigd.":::

+ Als u een systeemconfigurator of -beheerder bent en u de bedrijfsgegevens in een aangepast formulier automatisch wilt laten invullen, dan kunt u [formuliergebeurtenissen](/powerapps/developer/model-driven-apps/clientapi/events-forms-grids) gebruiken. Voeg een JavaScript-verwijzing toe aan **msdyn_/DefaultCompany.js** en gebruik de volgende gebeurtenissen. U kunt elk kant-en-klaar formulier gebruiken, bijvoorbeeld het formulier **Account**.

    + **OnLoad**-gebeurtenis voor het formulier: stel de kolom **defaultCompany** in.
    + **OnChange**-gebeurtenis voor de kolom **Bedrijf**: stel de kolom **updateDefaultCompany** in.

## <a name="apply-filtering-based-on-the-company-context"></a>Filters toepassen op basis van de bedrijfscontext

Als u filters op basis van de bedrijfscontext wilt toepassen op uw aangepaste formulieren of op aangepaste opzoekkolommen die zijn toegevoegd aan de standaardformulieren, open dan het formulier en gebruik de sectie **Gerelateerde records filteren** om het bedrijfsfilter toe te passen. U moet dit instellen voor elke opzoekkolom die een filter op basis van het onderliggende bedrijf voor een bepaalde rij vereist. In de volgende afbeelding wordt de instelling weergegeven voor **Account**.

:::image type="content" source="media/apply-company-context.png" alt-text="Bedrijfscontext toepassen.":::



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]