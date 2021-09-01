---
title: Producteigenaren
description: Dit onderwerp biedt informatie over producteigenaren. Een producteigenaar is een groep gebruikers die verantwoordelijk is voor specifieke producten. Alleen leden van de groep kunnen deze producten vrijgeven. De producteigenaar kan ook worden gebruikt in de goedkeuringswerkstroom.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgProductOwner
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 4de6399f83eeb0b0e1ea6fb13e86fb6dca456ff1c9b113e024afec97cc5b68af
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766722"
---
# <a name="product-owners"></a>Producteigenaren

[!include [banner](../includes/banner.md)]

De producteigenaar is een groep gebruikers die verantwoordelijk is voor specifieke producten. Wanneer een producteigenaarsgroep aan een product wordt toegewezen, kunnen alleen de leden van die groep het product vrijgeven. De producteigenaar kan ook worden gebruikt in de goedkeuringswerkstroom voor het beheer van technische wijzigingen.

Producteigenaren zijn algemene instellingen. Deze zijn daarom beschikbaar voor alle rechtspersonen.

## <a name="create-a-product-owner-group"></a>Een producteigenaarsgroep maken

Voer de volgende stappen uit om een producteigenaarsgroep te maken en hier leden aan toe te voegen.

1. Ga naar **Beheer van technische wijzigingen \> Instellingen \> Producteigenaren**.
2. Selecteer **Nieuw** in het actievenster.
3. Voer een naam in voor de groep in het veld **Producteigenaar**.
4. Voer in het veld **Naam** een omschrijving in van de groep.
5. Voeg in sneltabblad **Leden** de werknemers toe die lid moeten zijn van de groep.

## <a name="assign-a-product-owner-to-a-product"></a>Een producteigenaar toewijzen aan een product

Om een producteigenaar aan een product toe te wijzen, volgt u deze stappen.

1. Open de pagina **Productgegevens** voor het relevante product of productmodel.
1. Op het sneltabblad **Algemeen** stelt u het veld **Producteigenaar** in op de naam van de relevante producteigenaarsgroep.

Terwijl een producteigenaar aan een product is toegewezen, kunnen alleen de leden van de producteigenaarsgroep de instelling **Producteigenaar** bewerken.

De product eigenaar wordt ook weergegeven op de pagina **Vrijgegeven producten**.

## <a name="product-owners-and-product-releases"></a>Producteigenaars en productvrijgaves

Alleen gebruikers uit de producteigenaarsgroep van een product kunnen dat product vrijgeven. Er is echter een uitzondering wanneer het product een onderliggend artikel is en het bovenliggende artikel wordt vrijgegeven door de eigenaar van het bovenliggende artikel. Met andere woorden, als het product deel uitmaakt van de stuklijst van een ander product, controleert het systeem de producteigenaar van elk artikel in de stuklijst niet. Alleen de producteigenaar van het bovenliggende artikel wordt gecontroleerd.

Product X wordt bijvoorbeeld toegewezen aan de producteigenaarsgroep *Designkasten*. Product X maakt ook deel uit van de stuklijst van product Y, dat is toegewezen aan de producteigenaarsgroep *Designluidsprekers*. Als een gebruiker in de producteigenaarsgroep *Designluidsprekers* product Y en de bijbehorende stuklijst vrijgeeft, wordt product X samen met product Y vrijgegeven.

## <a name="product-owners-and-approvals"></a>Producteigenaren en goedkeuringen

Omdat de producteigenaren weten of hun producten baat hebben bij specifieke technische wijzigingen, is het vaak zinvol om hen op te nemen als onderdeel van het goedkeuringsproces in het beheer technische wijzigingen. U kunt deze aanpak implementeren door de producteigenaren in te stellen als deelnemende leveranciers in de workflows die worden gebruikt voor het beheer van technische wijzigingen. Het systeem wijst vervolgens goedkeuringstaken toe in de werkstromen, op basis van de producten in de aanvragen voor technische wijzigingen en de orders voor technische wijzigingen. Zie [Wijzigingen in technische producten beheren](engineering-change-management.md) voor meer informatie.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]