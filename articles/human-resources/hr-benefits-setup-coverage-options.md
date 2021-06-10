---
title: Opties voor dekking maken
description: Dekkingsopties in Microsoft Dynamics 365 Human Resources zijn dekkingsniveaus voor de selectie van een deelnemer in een vergoedingsplan of -programma.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d9f67a97ec57bade840e1035c6011b94427a77c4
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055575"
---
# <a name="create-coverage-options"></a>Opties voor dekking maken

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dekkingsopties in Microsoft Dynamics 365 Human Resources zijn dekkingsniveaus voor de selectie van een deelnemer in een vergoedingsplan of -programma. Dekkingsopties kunnen bijvoorbeeld **Alleen werknemer** zijn voor een medisch plan of **2x salaris** voor een levensverzekeringsplan. Nadat u dit hebt gedefinieerd, kunt u de dekkingsopties voor vergoedingen opnieuw gebruiken. U kunt een optie aan een of meer plannen koppelen.

Nadat u de dekkingsopties hebt gedefinieerd, koppelt u de dekkingsopties aan een type vergoedingsplan. Het plantype wordt vervolgens gekoppeld aan een vergoedingsplan of -programma. De dekkingsopties die aan een plantype zijn gekoppeld, zijn beschikbaar voor alle plannen die met dat plantype worden gemaakt. 

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Dekkingsopties**.

2. Selecteer **Nieuw**.

3. Geef de waarden op voor de volgende velden:

   | Veld | Beschrijving |
   | --- | --- |
   | **Dekkingsoptie** | Een unieke naam voor de dekkingsoptie. |
   | **Beschrijving** | Een omschrijving van de dekkingsoptie. |
   | **Dekkingscode** | Met dekkingscodes worden minimum- en maximumbedragen toegewezen aan elk in type persoon dat in aanmerking komt voor de dekking. Een dekkingscode geeft aan wie is gedekt of hoeveel dekking er voor een plantype is toegestaan. U kunt het bedrag van de dekking uitdrukken als een bedrag in euro's of een percentage. Bijvoorbeeld:</br></br>- **Werknemer+1** – om hiervoor in aanmerking te komen, moet de werknemer één gezinslid hebben geselecteerd (als er meer dan één persoon wordt geselecteerd, komt de werknemer niet meer in aanmerking).</br></br>- **Werknemer+familie** - om hiervoor in aanmerking te komen, moet de werknemer ten minste twee gezinsleden hebben geselecteerd. |
   | **Maximum aantal** | Het maximale aantal gezinsleden. |
   | **Status** | De status van de dekkingsoptie. Als de status van de dekkingsoptie is ingesteld op Inactief, kan de dekkingsoptie niet worden geselecteerd voor plantypen. |
   | **Percentage** | Het percentage. Dit veld is alleen actief als '% x salaris' is geselecteerd in het veld Dekkingscode. |
   | **Deler** | De deler die bij de berekening moet worden gebruikt wanneer u de dekkingscode '% x salaris' selecteert. |
   | **Minimumpercentage** | Het minimumpercentage wanneer u de dekkingscode Percentage selecteert. |
   | **Maximumpercentage** | Het maximumpercentage wanneer u de dekkingscode Percentage selecteert. |

4. Koppel onder **Geschiktheidsopties voor persoonlijke contactpersonen** de juiste geschiktheidsoptie voor persoonlijke contactpersonen aan elke dekkingsoptie.

5. Geef onder **Selfservice** waarden op voor de volgende velden:

   | Veld | Beschrijving |
   | --- | --- |
   | **Bijdragebedrag werknemer toestaan** | Geeft aan of werknemers het bijdragebedrag voor vergoedingen via selfservice mogen wijzigen wanneer ze vergoedingen selecteren. Als u dit selectievakje inschakelt, worden de parameters van het vergoedingsplan berekend op basis van het bijdragebedrag dat de werknemer invoert via de selfservice voor vergoedingen. |
   | **Dekkingsbedrag werknemer toestaan** | Geeft aan of werknemers het dekkingsbedrag voor vergoedingen via selfservice mogen wijzigen wanneer ze vergoedingen selecteren. Als u dit selectievakje inschakelt, worden de parameters van het vergoedingsplan berekend op basis van het dekkingsbedrag dat de werknemer invoert in Werknemerselfservice. |

6. Selecteer **Opslaan**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]