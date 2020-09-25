---
title: Projectresources instellen
description: Dit onderwerp bevat informatie over het instellen of aanvragen van projectresources.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c882e23794e3937f85b3e73774b36deaf28ac3ed
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760518"
---
# <a name="set-up-project-resources"></a>Projectresources instellen

[!include [banner](../includes/banner.md)]

U moet een kalender configureren en deze aan een werknemer of een medewerker (uitvoerende) koppelen. De kalender wordt gebruikt om het project en de werktijd van de resources te plannen, die voor het project zijn gereserveerd. Tijdens het configureren van de kalender kunnen projectmanagers resources herverdelen in het kader van optimalisatie van de resources. Op basis van het kalenderplan kunnen beperkingen aan resources worden opgelegd. U kunt een kalender instellen op de pagina **Kalenders**.

Wanneer u een werknemer als een projectresource instelt, u kunt kiezen uit de werknemers die werken in het bedrijf waarvoor u resources instelt. U kunt ook werknemers selecteren van andere bedrijven binnen uw organisatie. Dit zijn intercompany-resources.

In de volgende procedures wordt beschreven hoe u een werknemer configureert als een projectresource binnen uw bedrijf en hoe u een intercompany-projectresource configureert.

## <a name="set-up-a-worker-as-a-project-resource"></a>Een medewerker instellen als een projectresource

1. Selecteer op de pagina **Medewerkers** in de lijst **Medewerkers** de medewerker die u als projectresource toevoegt en open de record van de medewerker.
2. In het actievenster selecteert u **Project** &gt; **Instellen** &gt; **Projectinstellingen**.
3. Selecteer een kalender en sluit vervolgens de pagina.

U kunt ook standaardprojecten voor een resource opgeven als een type toewijzing vooraf. Voorafgaande toewijzingen kunnen worden gebruikt wanneer de resource- of projectmanager van tevoren al weet aan welke projecten de resource zal gaan werken. Voorafgaande toewijzingen kunnen plaatsvinden op basis van aanvragen van een projectsponsor of klant. Als u voorafgaande toewijzingen wilt uitvoeren voor een project, selecteert u het gewenste project op de pagina **Projecten toewijzen** op het tabblad **Projecten** in de lijst **Resterende projecten**.

## <a name="set-up-an-intercompany-resource"></a>Een intercompany-resource instellen

Wanneer u een werknemer als een intercompany-resource instelt, moet u de instellingen uitvoeren in het bedrijf dat de werknemer uitleent en in het bedrijf dat de werknemer leent.

### <a name="in-the-lending-company"></a>In het uitlenende bedrijf

1. Controleer in Finance of het uitlenende bedrijf is geselecteerd en voer de bovenstaande procedure Een werknemer instellen als een projectresource uit.
2. Selecteer op de pagina **Intercompany-boekhouding** de optie **Nieuw**.
3. Selecteer in het veld **Rechtspersoon-ID** het uitlenende bedrijf. Vul de resterende velden in met de vereiste waarden en selecteer **Opslaan**.
4. Selecteer op de pagina **Prijs overboeken** de optie **Nieuw**.
5. Selecteer in het veld **Lenende rechtspersoon** het betreffende bedrijf.
6. Als u aan het lenende bedrijf alleen de resource wilt uitlenen die u hebt gemaakt aan het begin van deze sectie, selecteert u in het veld **Resource** de naam van de resource die u hebt gemaakt. Als u alle resources in het uitlenende bedrijf beschikbaar wilt stellen voor het lenende bedrijf, laat u het veld **Resource** leeg.
7. Stel op de pagina **Projectbeheer- en boekhoudingsparameters** op het tabblad **Intercompany** de optie **Intercompany-resourceplanning en urenstaten inschakelen** in op **Ja**.

### <a name="in-the-borrowing-company"></a>In het lenende bedrijf

- Voer op de pagina **Resourcelijst** in het zoekfilter de naam in van de resource die u hebt gemaakt in de vorige procedure voor het uitlenende bedrijf, om te controleren of de naam voorkomt in de lijst met resources voor het lenende bedrijf.

## <a name="request-project-resources"></a>Projectresources aanvragen
De planningsfunctionaliteit voor projectresources biedt resourcemanagers alleen de mogelijkheid om bemande resources te distribueren voor taken of projecten. Als u deze functionaliteit wilt inschakelen, voert u de volgende taken uit of controleert u of ze zijn voltooid:

- Nummerreeksen instellen.
- Workflows voor projectbeheer en boekhouding instellen.
- Workflows voor resourceaanvraag inschakelen.

Nadat u deze taken hebt voltooid, kunt u zo nodig de volgende taken uitvoeren:

- Een resourceaanvraag maken op basis van een variabel geboekte bemande resource.
- Resourceaanvragen bewaken.
- Resourceaanvragen vervullen.
- Een bemande resource aanvragen vanuit een projectstructuur.
- Resources boeken voor een project zonder een aanvraag voor een bemande resource.
