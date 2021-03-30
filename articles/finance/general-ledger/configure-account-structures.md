---
title: Rekeningstructuren configureren
description: Dit onderwerp biedt informatie over rekeningstructuren en financiële dimensies.
author: aprilolson
manager: AnnBe
ms.date: 06/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: roschlom
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9c7fd8fcad7de3ec8b4b23d5c5e6456ae3ef372
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212344"
---
# <a name="configure-account-structures"></a>Rekeningstructuren configureren

[!include[banner](../includes/banner.md)]

Rekeningstructuren maken gebruik van de hoofdrekening en financiële dimensies om een set regels te maken die de volgorde en de waarden bepalen die worden gebruikt bij het invoeren van het rekeningnummer. U kunt zoveel rekeningstructuren instellen als noodzakelijk is voor uw bedrijf. De rekeningstructuren worden toegewezen aan de grootboekinstellingen van een bedrijf, zodat ze kunnen worden gedeeld.

Wanneer u een rekeningstructuur maakt, is het maximumaantal segmenten 11. Als u meer segmenten nodig hebt, evalueert u uw instellingen en vereisten, want dat heeft invloed op de gebruikerservaring. Overweeg of een segment kan worden afgeleid in een rapportagescenario met behulp van een hiërarchie, in plaats van tijdens gegevensinvoer of door een door de gebruiker gedefinieerd veld te gebruiken. Als u bijvoorbeeld wilt rapporteren op locatie, maar de locatie kunt bepalen op basis van afdeling of kostenplaats, zou u geen locatie als financiële dimensie nodig hebben. Als u na evaluatie bepaalt dat er meer dan 11 segmenten nodig zijn, kunt u extra segmenten met behulp van geavanceerde regels toevoegen.

Rekeningstructuren vereisen de hoofdrekening. De hoofdrekening hoeft niet het eerste segment in de structuur te zijn, maar bepaalt welke rekeningstructuur wordt gebruikt tijdens invoer van het rekeningnummer. Als gevolg hiervan kan een waarde van de hoofdrekening alleen bestaan in één structuur die is toegewezen aan het grootboek, zodat ze elkaar niet overlappen. Nadat de rekeningstructuur is geïdentificeerd, wordt de lijst met toegestane waarden gefilterd, zodat de gebruiker alleen uit geldige dimensiewaarden kan kiezen, wat de mogelijkheid van een onjuiste journaalpost verkleint.

> [!NOTE] 
> Als u van plan bent te budgetteren ten opzichte van een financiële dimensie, moet deze deel uitmaken van een rekeningstructuur. Budgettering gebruikt momenteel geen geavanceerde regels.

## <a name="example"></a>Voorbeeld
Stel ter illustratie van een best practice voor het instellen van een rekeningstructuur dat een bedrijf de balansrekeningen (100000..399999) wil bijhouden op het niveau van de financiële dimensies rekening en bedrijfseenheid. Voor opbrengsten- en onkostenrekeningen (400000..999999) houden ze de financiële dimensies Bedrijfseenheid, Afdeling en Kostenplaats bij. Als ze iets verkopen, willen ze ook Klant bijhouden. Met behulp van dit scenario zou het aanbevolen worden twee rekeningstructuren te hebben die zijn toegewezen aan het grootboek van het bedrijf: een voor balansrekeningen en een voor winst- en verliesrekeningen. Als u de gebruikerservaring en validatie wilt optimaliseren, moet Klant een geavanceerde regel zijn die alleen wordt gebruikt wanneer een verkoopaccount wordt gebruikt.

**Balansrekeningstructuur**

|Hoofdrekening          | Bedrijfseenheid    |
|----------------------|-----------|
|100000..399999 | *;” “|

**Winst- en verliesrekeningstructuur**

|Hoofdrekening          | Bedrijfseenheid    |Departement          | Kostenplaats    |
|----------------------|-----------|----------------------|-----------|
|400000..999999 | *;” “|*;” “|*;” “|*;” “|

**Geavanceerde regel voor het toevoegen van een klant**

Criteria: als hoofdrekening tussen 400000 en 499999 ligt, klant invoegen. Het kan niet leeg worden gelaten.

|Klant         |
|-----------------|
|* |

In dit vereenvoudigde voorbeeld zijn alle waarden en lege waarden toegestaan, dus worden * en ' ' gebruikt.

## <a name="segments-and-allowed-values"></a>Segmenten en toegestane waarden
De sectie **Segmenten** en **Details van toegestane waarden** biedt een rasterachtige ervaring voor het invoeren van regels die worden gevolgd bij validatie tijdens boeking. U kunt rechtstreeks in de cellen in het typen, importeren uit Excel of de sectie **Details van toegestane waarden** gebruiken om u te begeleiden.

De sectie **Details van toegestane waarden** begeleidt u bij het maken van criteria met **Operatoren**, zoals begint met, valt tussen, omvat en vele andere.

[![Waarden toestaan](./media/account.png)](./media/account.png) 

Toegestane waarden worden standaard opgenomen op een invoerpagina voor journalen of boekhoudingsverdeling als er geen andere mogelijke waarden om te selecteren zijn op basis van de ingestelde rekeningstructuur.

Hier volgt een voorbeeld van de **winst- en verliesrekeningstructuur**.

|Hoofdrekening          | Bedrijfseenheid    |Departement          | Kostenplaats    |
|----------------------|-----------|----------------------|-----------|
|400000..999999 | 002 | 022 | 014 |

Wanneer u een journaal invoert en een rekening selecteert in het winst- en verliesbereik, worden de waarden 022 en 014 standaard ingevoerd voor de rekeningoptie als u Bedrijfseenheid 002 selecteert. Dit gedrag doet zich ook voor op de pagina voor boekhoudingsverdeling. 

## <a name="more-than-7-criteria-needed"></a>Meer dan 7 criteria nodig

Als u meer dan 7 criteria hebt die nodig zijn, kunt u doorgaan met ze toe te voegen op de volgende regel. U zult zien wanneer u werkt met de sectie **Details van toegestane waarden** dat het criterium **+Nieuwe toevoegen** niet meer actief is nadat het zevende criterium is ingevoerd. Dit is het gevolg van diverse factoren, zoals: 
 - Kolombreedte 
 - Hoe de gegevens worden opgeslagen 
 - Prestaties van het besturingselement **Details van toegestane waarden**
 - Bruikbaarheid  
 
Als u wilt doorgaan met het toevoegen van extra criteria, klikt u op **Dupliceren in het segment** en **Sectie toegestane waarden**. Hiermee wordt het criterium naar een nieuwe regel gekopieerd. U kunt vervolgens de sectie **Details van toegestane waarden** overschrijven of wijzigen.

## <a name="best-practices"></a> aanbevolen procedures
Bij het instellen van uw rekeningstructuren zijn er enkele aanbevelingen die u kunt volgen. Dit is echter alleen een richtlijn zodat een holistische discussie over uw bedrijf, groeiplan en onderhoudsplan moet worden beschouwd als onderdeel van die discussie.

- Maak de hoofdrekening de eerste of zo dicht mogelijk bij de voorzijde van de rekeningstructuur, zodat gebruikers de best mogelijke begeleide ervaring krijgen tijdens rekeninginvoer.

- Hergebruik rekeningstructuren zo veel mogelijk om onderhoud te beperken in uw rechtspersonen.

- Overweeg voor variaties tussen rechtspersonen geavanceerde regels te gebruiken, zodat rekeningstructuren opnieuw kunnen worden gebruikt.

- Gebruik bij het definiëren van toegestane waarden bereiken en jokertekens zo veel mogelijk. Hiermee kunt u niet alleen groeien en evolueren zonder onderhoud, maar het systeem presteert ook beter met deze configuratie.

- U moet niet gewoon een asterisk voor elk segment in de rekeningstructuur plaatsen en vervolgens uitsluitend vertrouwen op de geavanceerde regels. Dit kan moeilijk te beheren zijn en leidt vaak tot gebruikersfouten tijdens onderhoud, waardoor het systeem onstabiel voor boeken kan worden.

## <a name="account-structure-activation"></a>Activering van rekeningstructuur
Wanneer u tevreden bent met uw nieuwe instellingen of een wijziging in de rekeningstructuur, moet u deze activeren. Als een rekeningstructuur is toegewezen aan een grootboek, kan deze activering een langdurig proces zijn, omdat alle niet-geboekte transacties in het systeem moeten worden gesynchroniseerd met de nieuwe structuur. Geboekte transacties worden niet beïnvloed door wijzigingen in de rekeningstructuur.

Zie voor meer informatie [Uw rekeningschema plannen](plan-chart-of-accounts.md), [Financiële dimensies](financial-dimensions.md) en [Rekening- en dimensiecombinaties invoeren (gesegmenteerd invoerbesturingselement)](enter-account-dimension-combinations-segmented-entry-control.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]