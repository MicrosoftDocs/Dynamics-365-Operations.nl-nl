---
title: Plantypen maken
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c12eecb38bd943a9c604f878644da289783d3f74
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008626"
---
# <a name="create-plan-types"></a>Plantypen maken

[!include [banner](includes/preview-feature.md)]

Een plantype in Microsoft Dynamics 365 Human Resources is een groepering op hoog niveau van specifieke typen vergoedingen. Elk plantype heeft een plantypecode waarmee de regels voor het plantype worden bepaald. Het plantype Basis leven heeft bijvoorbeeld de plantypecode Leven, omdat het een type levensverzekering is en moet voldoen aan de regels die zijn vastgelegd voor de plantypecode Leven. Een ander plantype kan Aanvullend leven zijn, eveneens met plantypecode Leven.

Elk plantype geeft aan of een werknemer zich kan inschrijven voor een bepaald type plan of voor meerdere. Een werknemer kan zich bijvoorbeeld mogelijk inschrijven voor zowel de verzekeringspolis Basis leven als de verzekeringspolis Aanvullend leven van het plantype Leven. Een werknemer mag zich waarschijnlijk inschrijven voor één polis van het type Medisch.

Als bij een plantype contactpersonen zijn betrokken, geeft het plantype aan of contactpersonen begunstigden of gezinsleden zijn. Een plantype Basis leven zou bijvoorbeeld begunstigden hebben, terwijl een plantype Basis medisch gezinsleden zou hebben. In sommige gevallen kan een plan geen persoonlijke contactpersonen hebben. Bijvoorbeeld een flexibele bestedingsrekening of parkeervergoeding.

Een plantype kan dekkingsopties definiëren. De dekkingsopties worden gedefinieerd in het formulier van de optie Behoefteplanning. Een behoefteplanningsoptie kan het bedrag van de vergoeding aangeven of de contactpersonen die in aanmerking komen voor het plantype. Als het type contactpersoon bijvoorbeeld Begunstigde is, moet de dekkingsoptie de voorwaarden definiëren van waartoe de begunstigde gerechtigd is als de vergoeding wordt gebruikt. Als het contactpersoontype Gezinslid is, moet de dekkingsoptie de relatie tussen het gezinslid en de werknemer definiëren. 

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Plantypen**.

2. Selecteer **Nieuw**.

3. Geef de waarden op voor de volgende velden:

   | Veld | Beschrijving |
   | --- | --- |
   | Plantype | Een unieke naam die het plantype aanduidt. |
   | Beschrijving | Een beschrijving van het plantype. |
   | Plantypecode | Selecteer een plantypecode in de vervolgkeuzelijst met waarden. In de lijst met plantypecodes worden alle plantypen weergegeven die in de huidige versie worden ondersteund. |
   | Gelijktijdige inschrijving | Geeft aan of een werknemer zich kan inschrijven voor meerdere vergoedingsplannen van hetzelfde plantype of voor slechts één vergoedingsplan per plantype. |
   | Type contact | Hiermee wordt de rol van de persoonlijke contactpersoon opgegeven. De waarden zijn leeg, Gezinslid en Begunstigde. U kunt Type contact leeg laten als het plantype geen gezinslid of begunstigde vereist op basis van de dekkingsoptie. |

4. Als u opties voor levensgebeurtenissen wilt configureren, selecteert u **Acties** en vervolgens **Opties voor levensgebeurtenis**. Geef de waarden op voor de volgende velden:

   | Veld | Beschrijving |
   | --- | --- |
   | Plantype | Het plantype waarvoor u opties voor levensgebeurtenissen wilt configureren. |
   | Type-id van levensgebeurtenis | De id van het type levensgebeurtenis. |
   | Annulering toestaan | Hiermee wordt opgegeven of een werknemer een vergoedingsplan kan annuleren tijdens de levensgebeurtenis. |
   |Dekkingsoptie wijzigen | Hiermee wordt opgegeven of een werknemer dekkingsopties kan wijzigen tijdens de levensgebeurtenis. |
   | Wijzigen in een nieuw plan | Hiermee wordt opgegeven of een werknemer van plan kan veranderen tijdens de levensgebeurtenis. |
   | Plan automatisch annuleren |Hiermee wordt aangegeven of het plan automatisch wordt geannuleerd tijdens de levensgebeurtenis. |
   | Geschiktheidscontrole automatisch opnieuw openen | Hiermee wordt aangegeven of de geschiktheidscontrole voor de vergoedinginschrijving automatisch opnieuw wordt geopend tijdens de levensgebeurtenis. |
   | Tijdsvenster voor rapportage | Geeft het tijdsvenster in dagen op voor de rapportage van de levensgebeurtenis. **Opmerking**: als u geen tijdsduur invoert, wordt aangenomen dat het rapportagevenster nul is en wordt de levensgebeurtenis niet verwerkt. |

5. Selecteer **Opslaan**. 
