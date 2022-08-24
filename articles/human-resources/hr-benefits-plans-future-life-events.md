---
title: Toekomstige levensgebeurtenissen configureren
description: In dit artikel wordt beschreven hoe u toekomstige levensgebeurtenissen in Dynamics 365 Human Resources kunt plannen.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitFutureLifeEvents, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2cb3ca03e0d9d7e5423a405f1eb0372e1c19588d
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2022
ms.locfileid: "9227980"
---
# <a name="configure-future-life-events"></a>Toekomstige levensgebeurtenissen configureren

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [banner](../includes/preview-banner.md)]

U kunt toekomstige levensgebeurtenissen plannen in Dynamics 365 Human Resources.

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Toekomstige levensgebeurtenissen**.

2. Selecteer **Nieuw**.

3. Geef de waarden op voor de volgende velden:

   | Veld | Beschrijving |
   | --- | --- |
   | Datum van levensgebeurtenis | Het systeem verwerkt alle gebeurtenissen tijdens de inschrijvingsperiode die plaatsvinden tot en met deze datum. |
   | Levensgebeurtenis vastgelegd | De datum en het tijdstip waarop de levensgebeurtenis in het logboek is geregistreerd. |
   | Logboektype | Hier ziet u of de actie een van de volgende acties is:</br></br>- **Bijwerken** – een wijziging aanbrengen in een bestaande record die levensgebeurtenissen bijhoudt</br></br>- **Invoegen** – een nieuwe levensgebeurtenisrecord maken |
   | Type-id van levensgebeurtenis | De unieke id voor het type levensgebeurtenis. |
   | Type levensgebeurtenis | Een katalysator om de inschrijving van een werknemer voor vergoedingen bij te werken. Raadpleeg het gedeelte Triggers voor levensgebeurtenissen voor meer informatie. |
   | Status | Of de levensgebeurtenis wel of niet is verwerkt. |
   | Regel | Het regelnummer van de toekomstige levensgebeurtenis. |

4. Selecteer **Opslaan**. 

U kunt toekomstige levensgebeurtenissen verwijderen. Als een verwerkte levensgebeurtenis in de toekomst wordt verwijderd, wordt de toekomstige record ook verwijderd. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
