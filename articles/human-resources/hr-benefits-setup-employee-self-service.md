---
title: Werknemerselfservice configureren
description: In Microsoft Dynamics 365 Human Resources kunt u tegels configureren voor navigatie op het hoogste niveau in Selfservice werknemer.
author: twheeloc
ms.date: 12/06/2021
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
ms.openlocfilehash: 83718856a864123d7941b21c078bcdb96a62cca8
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067574"
---
# <a name="configure-employee-self-service"></a>Werknemerselfservice configureren


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In Microsoft Dynamics 365 Human Resources kunt u tegels configureren voor navigatie op het hoogste niveau in **Selfservice werknemer**. Vergoedingsplantegels leiden gebruikers naar vergoedingsplannen waarvoor zij in aanmerking komen.

## <a name="set-up-a-benefit-plans-tile"></a>Een tegel voor vergoedingsplannen instellen

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Parameters voor Selfservice werknemer**.

2. Selecteer het tabblad **Tegel voor vergoedingsplannen instellen** en selecteer vervolgens **Nieuw**.

3. Geef de waarden op voor de volgende velden.

   | Veld | Description |
   | --- | --- |
   | **Code van plantype** | Het plantype dat wordt weergegeven wanneer deze tegel wordt geselecteerd in **Vergoedingen via selfservice**. |
   | **Tegel-id** | De unieke id voor de tegel. |
   | **Tekst van tegellabel** | De tekst die voor de tegel wordt weergegeven in **Vergoedingen via selfservice**. |
   | **Beschrijving** | Een beschrijving van de tegel. |
   | **Afbeelding voor tegelachtergrond** | De URL van de afbeelding die moet worden gebruikt voor de tegel (optioneel). |
   | **Openstaande inschrijving bijhouden** | U kunt deze optie gebruiken als u de voortgang van de openstaande inschrijving voor dit plantype wilt bijhouden. U kunt bijvoorbeeld plannen hebben gemaakt waarbij **Plantype = Overig** is. Deze plannen kunnen optionele plannen zijn waarvan u de voortgang van de inschrijvingsproces niet wilt bijhouden. Als u dit plantype niet selecteert, worden plannen van dit type genegeerd wanneer u de voortgang of voltooiing van de inschrijving op het tabblad **Inschrijving openen** volgt. Deze instelling is van toepassing op het plantype dat voor alle perioden en rechtspersonen is geselecteerd. |

4. Selecteer **Opslaan**.

## <a name="set-up-a-flex-credit-plan-tile"></a>Een tegel voor een flex-kredietplan instellen

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Parameters voor Selfservice werknemer**.

2. Selecteer het tabblad **Tegel voor flex-kredietplan instellen** en selecteer vervolgens **Nieuw**.

3. Geef de waarden op voor de volgende velden.

   | Veld | Description |
   | --- | --- |
   | **Vergoedingskrediet-id** | De programma's met flexibele kredieten die worden weergegeven wanneer deze tegel wordt geselecteerd in **Vergoedingen via selfservice**. |
   | **Tegel-id** | De unieke id voor de tegel. |
   | **Tekst van tegellabel** | De tekst die voor de tegel wordt weergegeven in **Vergoedingen via selfservice**. |
   | **Beschrijving** | Een beschrijving van de tegel. |
   | **Afbeelding voor tegelachtergrond** | De URL van de afbeelding die moet worden gebruikt voor de tegel (optioneel). |
   | **Openstaande inschrijving bijhouden** | U kunt deze optie gebruiken als u de voortgang van de openstaande inschrijving voor dit plantype wilt bijhouden. U kunt bijvoorbeeld plannen hebben gemaakt waarbij **Plantype = Overig** is. Deze plannen kunnen optionele plannen zijn waarvan u de voortgang van de inschrijvingsproces niet wilt bijhouden. Als u dit plantype niet selecteert, worden plannen van dit type genegeerd wanneer u de voortgang of voltooiing van de inschrijving op het tabblad **Inschrijving openen** volgt. Deze instelling is van toepassing op het plantype dat voor alle perioden en rechtspersonen is geselecteerd. |

4. Selecteer **Opslaan**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
