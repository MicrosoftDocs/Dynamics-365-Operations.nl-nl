---
title: Opties voor dekking maken
description: In dit onderwerp worden de dekkingsopties in Microsoft Dynamics 365 Human Resources beschreven voor de selectie van een deelnemer in een vergoedingsplan of -programma.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a553fa1aa4bac0d2fb11b87ee05e4e52c019411d
ms.sourcegitcommit: 8592c661b41f9cef8b7ef2863a3b97bf49a4e6f9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/26/2021
ms.locfileid: "7423515"
---
# <a name="create-coverage-options"></a>Opties voor dekking maken

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Opties voor dekking bepalen wie gedekt moet worden of hoeveel dekking er in een verzekeringsplan beschikbaar is. Voor een medische planning hebt u bijvoorbeeld een optie **Alleen-werknemer**, een optie **Werknemer + 1** en een optie **Familie**. Voor levensverzekering kunt u een dekking bieden van **1 x salaris** of **2 x salaris**.

Nadat opties voor vergoedingsdekking zijn gedefinieerd, kunt u deze opnieuw gebruiken. U kunt een optie aan een of meer plannen koppelen.

> [!IMPORTANT]
> Nadat u de dekkingsopties hebt gedefinieerd, koppelt u ze aan een type vergoedingsplan. Het plantype wordt vervolgens gekoppeld aan een vergoedingsplan of -programma. De dekkingsopties die aan een plantype zijn gekoppeld, zijn beschikbaar voor alle plannen van dat type die worden gemaakt.

## <a name="create-coverage-options"></a>Opties voor dekking maken
1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Dekkingsopties**.

2. Selecteer **Nieuw**.

3. Geef de waarden op voor de volgende velden:

   | Veld | Beschrijving |
   | --- | --- |
   | **Dekkingsoptie** | Een unieke naam voor de dekkingsoptie. |
   | **Beschrijving** | Een omschrijving van de dekkingsoptie. |
   | **Dekkingscode** | Met dekkingscodes worden minimum- en maximumbedragen toegewezen aan elk in type persoon dat in aanmerking komt voor de dekking. Een dekkingscode geeft aan wie is gedekt of hoeveel dekking er voor een plantype is toegestaan. U kunt het bedrag van de dekking uitdrukken als een bedrag in euro's of een percentage. Bijvoorbeeld:<ul><li>**Werknemer+1**: om hiervoor in aanmerking te komen, moet de werknemer één gezinslid hebben geselecteerd (als er meer dan één persoon wordt geselecteerd, komt de werknemer niet meer in aanmerking).</li><li>**Werknemer+familie**: om hiervoor in aanmerking te komen, moet de werknemer ten minste twee gezinsleden hebben geselecteerd.</li></ul> |
   | **Maximum aantal** | Het maximale aantal gezinsleden. |
   | **Status** | De status van de dekkingsoptie. Als de status van de dekkingsoptie is ingesteld op **Inactief**, kan de dekkingsoptie niet worden geselecteerd voor plantypen. |
   | **Percentage** | Het percentage. Dit veld is alleen actief als '% x salaris' is geselecteerd in het veld Dekkingscode. |
   | **Deler** | De deler die bij de berekening moet worden gebruikt wanneer u de dekkingscode '% x salaris' selecteert. |
   | **Minimumpercentage** | Het minimumpercentage wanneer u de dekkingscode Percentage selecteert. |
   | **Maximumpercentage** | Het maximumpercentage wanneer u de dekkingscode Percentage selecteert. |

4. Koppel onder **Geschiktheidsopties voor persoonlijke contactpersonen** de juiste geschiktheidsoptie voor persoonlijke contactpersonen aan elke dekkingsoptie.

5. Geef onder **Selfservice** waarden op voor de volgende velden:

   | Veld | Beschrijving |
   | --- | --- |
   | **Bijdragebedrag werknemer toestaan** | Geeft aan of werknemers het bijdragebedrag In Vergoedingen via selfservice mogen wijzigen wanneer ze vergoedingen selecteren. Als u dit selectievakje inschakelt, worden de parameters van het vergoedingsplan berekend op basis van het bijdragebedrag dat de werknemer invoert bij Selfservice voor vergoedingen. |
   | **Dekkingsbedrag werknemer toestaan** | Geeft aan of werknemers het dekkingsbedrag in Vergoedingen via selfservice mogen wijzigen wanneer ze vergoedingen selecteren. Als u dit selectievakje inschakelt, worden de parameters van het vergoedingsplan berekend op basis van het dekkingsbedrag dat de werknemer invoert in Werknemerselfservice. |

6. Selecteer **Opslaan**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
