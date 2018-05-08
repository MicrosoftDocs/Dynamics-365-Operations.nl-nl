---
title: Een catalogus maken voor het call center
description: Dit artikel geeft een overzicht van het proces voor de aanmaak van een catalogus voor een callcenter.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailMCRChannelDetailPage, RetailCatalogDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16212
ms.assetid: c9d1b9df-82e8-4b3a-a13c-166df8b9718e
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 29d005655856fd1eb0f1490c45e07649465539f2
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="create-a-call-center-catalog"></a>Een catalogus maken voor het call center

[!include [banner](includes/banner.md)]

Dit artikel geeft een overzicht van het proces voor de aanmaak van een catalogus voor een callcenter. 

In een callcenter kunt u productcatalogi gebruiken voor de identificatie van de producten die u aan klanten wilt aanbieden. Callcenters gebruiken meestal afgedrukte catalogi. Het ontwerp en de productie van een afgedrukte catalogus worden buiten Microsoft Dynamics 365 for Retail uitgevoerd. U kunt echter een digitaal formulier van een catalogus maken en opslaan met dezelfde formulieren die u gebruikt om online detailhandelcatalogi in te stellen. Voordat u een catalogus kunt maken, moet u de productassortimenten instellen en de assortimenten toewijzen aan een callcenter. U voegt vervolgens producten toe aan de catalogus door producten uit deze assortimenten te selecteren. Nadat de producten aan de catalogus zijn toegevoegd, en de catalogus is voltooid, moet u de catalogus valideren om de gegevens te controleren. U moet vervolgens de catalogus indienen ter beoordeling en goedkeuring. Nadat de catalogus is goedgekeurd, kan deze worden gepubliceerd. Wanneer een callcentercatalogus wordt gemaakt, kunt u een momentopname van de catalogusgegevens nemen op het moment dat de catalogus wordt gepubliceerd. Met deze momentopnamefunctionaliteit kunt u een bepaalde versie van de catalogus openen, zelfs als de catalogus later wordt gewijzigd en bijgewerkt. De callcentercatalogi kunnen ook worden ingesteld om de volgende optionele functies te bevatten.

-   **Broncodes** – Codes die worden gebruikt om de klantrespons op bepaalde catalogusmailings bij te houden.
-   **Gratis producten** – Producten die in een klantorder zijn opgenomen zonder extra kosten. Deze producten worden automatisch aan de order toegevoegd wanneer de broncode voor de catalogus in de order wordt ingevoerd.
-   **Scripts** – Teksten die een callcenterwerknemer voorleest aan een klant wanneer een verkooporder wordt gemaakt. Scripts kunnen groeten of aankoopsuggesties omvatten.
-   **Bijverkoop- of kruisverkoopartikelen** - Artikelen die als voorstel worden weergegeven wanneer een bepaald product aan de order wordt toegevoegd.

Deze opties moeten worden ingesteld voordat de catalogus wordt goedgekeurd en gepubliceerd.

## <a name="prerequisites"></a>Vereisten
De volgende taken moeten zijn voltooid voordat u deze start:

-   Producten en productassortimenten instellen.
-   Detailhandelproducten instellen.
-   Een assortiment instellen.
-   Een callcenter maken.
-   Een call center instellen.
-   Het call center toevoegen aan een organisatiehiërarchie.
-   Een organisatiehiërarchie maken of wijzigen.

## <a name="create-a-catalog"></a>Een catalogus maken
U moet eerst een catalogus maken, producten toevoegen aan de catalogus en vervolgens de kenmerken voor de producten bekijken en aanpassen.

## <a name="validate-the-catalog"></a>De catalogus valideren
Nadat u het instellen van de catalogus hebt voltooid, moet u het validatieproces uitvoeren. Dit proces controleert of de gegevens die voor kanaalkenmerken en productkenmerken zijn vereist, volledig en geldig zijn, en dat de catalogus kan worden gepubliceerd.

## <a name="submit-the-catalog-for-review-and-approval"></a>De catalogus indienen ter beoordeling en goedkeuring
Nadat een catalogus is gevalideerd, kunt u de catalogus voor revisie en goedkeuring indienen. Een catalogus moet worden goedgekeurd voordat deze kan worden gepubliceerd. U kunt een werkstroom configureren zodat catalogi automatisch worden goedgekeurd of dat ze handmatige goedkeuring vereisen.

## <a name="optional-add-source-codes-free-products-and-scripts"></a>Optioneel: Voeg broncodes, gratis producten en scripts toe
U kunt ook de volgende artikelen aan een callcentercatalogus toevoegen. Deze artikelen zijn optioneel.

-   **Broncodes** kunnen door bedrijven die gedrukte catalogi leveren, worden gebruikt om de klantrespons voor bepaalde catalogi te volgen. Broncodes worden vaak op de achterzijde van een catalogus afgedrukt en worden ingevoerd in de verkooporder wanneer een klant een inkoop doet. Als u een broncode aan de catalogus wilt toevoegen, moet u eerst een doelmarkt maken. De doelmarkt wordt meestal toegewezen aan een eigen of gehuurde mailinglijst.
-   **Vrije producten** zijn promotieartikelen die zonder toeslagen zijn opgenomen bij de order van de klant wanneer naar de catalogus wordt verwezen.
-   **Scripts** kunnen worden gebruikt om de interacties van de werknemer met klanten in de context van een catalogus of product in een catalogus te begeleiden.

## <a name="publish-the-catalog"></a>De catalogus publiceren
Door een catalogus voor een callcenter te publiceren, werkt u de productinformatie in de catalogus af. Publicatie geeft ook aan dat de catalogus klaar is voor eventuele aanvullende acties die u wilt uitvoeren. U kunt bijvoorbeeld een afgedrukte catalogus maken. U kunt uw catalogi handmatig publiceren of u kunt een batchproces gebruiken om te publiceren op basis van een planning. Voordat u een catalogus kunt publiceren, moet de catalogus worden gevalideerd en goedgekeurd. Om de catalogus te wijzigen nadat deze is gepubliceerd, kunt u de catalogus intrekken en vervolgens opnieuw publiceren.




