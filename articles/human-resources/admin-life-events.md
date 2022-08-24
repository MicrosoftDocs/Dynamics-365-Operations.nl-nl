---
title: Beheerdersrechten instellen voor levensgebeurtenissen
description: In dit artikel wordt uitgelegd hoe u beheerdersrechten configureert voor levensgebeurtenissen in Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9deed240977394667cee8b107397267b182d960b
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229892"
---
# <a name="set-administrator-rights-for-life-events"></a>Beheerdersrechten instellen voor levensgebeurtenissen

[!include [banner](../includes/preview-banner.md)]

Beheerders kunnen opties voor levensgebeurtenissen bijwerken, afhankelijk van de configuratie-instellingen. Op de pagina **Human resource-parameters** kunt u parameters configureren waarmee beheerders wijzigingen kunnen aanbrengen in planningsselecties. U kunt beheerders ook volledig beperken in het aanbrengen van wijzigingen.

Op de pagina **Human resources-parameters** kunt u beperkingen voor het wijzigen van plannen instellen voor opties voor bevestigde plannen en levensgebeurtenissen.

Als de optie **Bevestigde plannen** is geselecteerd, kunnen er alleen wijzigingen worden aangebracht als een inschrijvingsperiode actief is. (Voorbeelden van inschrijvingsperioden zijn openstaande inschrijvingsperioden, inschrijvingsperioden voor nieuw aangenomen werknemers en inschrijvingsperioden voor levensgebeurtenissen.) Als deze optie niet is geselecteerd, kunnen er op elk moment wijzigingen worden aangebracht.

Als de optie **Levensgebeurtenis-opties** is geselecteerd, worden planwijzigingen tijdens een levensgebeurtenis beperkt door de opties voor levensgebeurtenissen die zijn gedefinieerd in het plantype. Als deze optie niet is geselecteerd, kunnen planselecties tijdens een levensgebeurtenis worden gewijzigd.

## <a name="set-plan-change-restrictions"></a>Beperkingen voor planwijzigingen instellen

Op de pagina **Human resource-parameters**, op het tabblad **Vergoedingenbeheer**, zijn de volgende velden beschikbaar.

| Veld | Description |
|-------|-------------|
| Bevestigde plannen | Selecteer deze optie als wijzigingen in een plan alleen zijn toegestaan als een inschrijvingsperiode actief is. Als deze optie niet is geselecteerd, kunnen er op elk moment wijzigingen worden aangebracht. |
| Opties voor levensgebeurtenissen | Selecteer deze optie als planwijzigingen tijdens een levensgebeurtenis worden beperkt door de opties voor levensgebeurtenissen die zijn gedefinieerd in het plantype. Als deze optie niet is geselecteerd, kunnen planselecties tijdens een levensgebeurtenis worden gewijzigd. |
