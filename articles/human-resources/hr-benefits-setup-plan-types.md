---
title: Overzicht plantype
description: Een plantype in Microsoft Dynamics 365 Human Resources is een groepering op hoog niveau van specifieke typen vergoedingen.
author: twheeloc
ms.date: 08/24/2021
ms.topic: overview
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
ms.openlocfilehash: 6ca14156c165ca3f536fc0120ebd03883284eb18
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336887"
---
# <a name="plan-type-overview"></a>Overzicht plantype

[!include [banner](../includes/preview-banner.md)]

Een plantype is een groepering op hoog niveau van specifieke typen vergoedingen. Elk plantype heeft een plantypecode waarmee de regels voor het plantype worden bepaald. Het plantype **Basis leven** heeft bijvoorbeeld de plantypecode **Leven**, omdat het een type levensverzekering is en moet voldoen aan de regels die zijn vastgelegd voor de plantypecode **Leven**. Een ander plantype kan **Aanvullend leven** zijn. Dit plantype heeft ook de plantypecode **Leven**.

Elk plantype geeft aan of een werknemer zich kan inschrijven voor een bepaald type plan of voor meerdere. Een werknemer kan zich bijvoorbeeld mogelijk inschrijven voor zowel de verzekeringspolis **Basis leven** als de verzekeringspolis **Aanvullend leven** van het plantype Leven. Een werknemer mag zich waarschijnlijk inschrijven voor één polis van het type Medisch.

Als bij een plantype contactpersonen zijn betrokken, geeft het plantype aan of contactpersonen begunstigden of gezinsleden zijn. Een plantype **Basis leven** zou bijvoorbeeld begunstigden hebben, terwijl een plantype Basis medisch afhankelijken zou hebben. In sommige gevallen kan een plan geen persoonlijke contactpersonen hebben. Bijvoorbeeld een flexibele bestedingsrekening of parkeervergoeding.


Een plantype kan dekkingsopties definiëren. De dekkingsopties worden gedefinieerd op de pagina **Behoefteopties**. Een behoefteplanningsoptie kan het bedrag van de vergoeding aangeven of de contactpersonen die in aanmerking komen voor het plantype. Als het type contactpersoon bijvoorbeeld **Begunstigde** is, moet de dekkingsoptie de voorwaarden definiëren van datgene waartoe de begunstigde gerechtigd is als de vergoeding wordt gebruikt. Als het type contactpersoon **Afhankelijke** is, moet de dekkingsoptie de relatie tussen de afhankelijke en de werknemer definiëren. 

> [!IMPORTANT]
> De pagina **Plantypen** bevat belangrijke gegevens die van invloed zijn op de opties die beschikbaar zijn wanneer een nieuw vergoedingenplan wordt gemaakt:
>
> - **Code van plantype**: dit veld beïnvloedt wat er wordt weergegeven op het tabblad **Configuratie** wanneer de werkelijke vergoeding wordt ingesteld.  
> - **Gelijktijdige inschrijving**: dit veld bepaalt of meerdere inschrijvingen zijn toegestaan. (Voor een medisch plan is dit veld meestal ingesteld op **Eén inschrijving**.)
> - **Type contactpersoon**: dit veld maakt het mogelijk afhankelijken of begunstigden aan een plan toe te voegen. Als het is ingesteld op **Geen**, hebben werknemers die zich inschrijven voor vergoedingen geen optie om een begunstigde of afhankelijke te selecteren.
> - **Dekkingsopties**: gebruik dit veld om de opties voor de dekking te koppelen aan de plantypen. Het definieert de personen die onder dit plantype vallen of de dekkingsbedragen die beschikbaar zijn voor dit plantype. U kunt bijvoorbeeld opgeven dat de dekking voor een medische plantype alleen beschikbaar is voor de werknemer, de werknemer en één andere persoon of de werknemer en zijn/haar gezin.

## <a name="create-plan-types"></a>Plantypen maken

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Plantypen**.

2. Selecteer **Nieuw**.

3. Geef de waarden op voor de volgende velden:

   | Veld | Beschrijving |
   | --- | --- |
   | **Plantype** | Een unieke naam die het plantype aanduidt. |
   | **Beschrijving** | Een beschrijving van het plantype. |
   | **Code van plantype** | Selecteer een plantypecode in de vervolgkeuzelijst met waarden. In de lijst met plantypecodes worden alle plantypen weergegeven die in de huidige versie worden ondersteund. |
   | **Gelijktijdige inschrijving** | Geeft aan of een werknemer zich kan inschrijven voor meerdere vergoedingsplannen van hetzelfde plantype of voor slechts één vergoedingsplan per plantype. |
   | **Type contact** | Hiermee wordt de rol van de persoonlijke contactpersoon opgegeven. De waarden zijn leeg, Gezinslid en Begunstigde. U kunt **Type contact** leeg laten als het plantype geen gezinslid of begunstigde vereist op basis van de dekkingsoptie. |

4. Als u opties voor levensgebeurtenissen wilt configureren, selecteert u **Acties** en vervolgens **Opties voor levensgebeurtenis**. Geef de waarden op voor de volgende velden:

   | Veld | Beschrijving |
   | --- | --- |
   | **Plantype** | Het plantype waarvoor u opties voor levensgebeurtenissen wilt configureren. |
   | **Type-id van levensgebeurtenis** | De id van het type levensgebeurtenis. |
   | **Dekkingsoptie wijzigen** | Hiermee wordt opgegeven of een werknemer dekkingsopties kan wijzigen tijdens de levensgebeurtenis. |
   | **Wijzigen in een nieuw plan** | Hiermee wordt opgegeven of een werknemer van plan kan veranderen tijdens de levensgebeurtenis. |
   | **Geschiktheidscontrole automatisch opnieuw openen** | Geeft aan of de geschiktheidscontrole voor de vergoedinginschrijving automatisch opnieuw wordt geopend tijdens de levensgebeurtenis. |
   | **Inschrijvingsperiode levensgebeurtenis** | Geeft het tijdsvenster in dagen op voor de rapportage van de levensgebeurtenis. **Opmerking**: als u geen tijdsduur invoert, wordt aangenomen dat het rapportagevenster nul is en wordt de levensgebeurtenis niet verwerkt. |
   | **Kan alleen worden bewerkt door beheerders** | Geeft aan of beheerders een plan kan annuleren of bewerken tijdens een levensgebeurtenis. De werknemer kan geen wijzigingen aanbrengen in de werkruimte **selfservice werknemer**. |
   | **Plan automatisch annuleren** | Hiermee wordt aangegeven of het plan automatisch moet worden geannuleerd tijdens een levensgebeurtenis. Nadat de wijzigingen in de levensgebeurtenis zijn verwerkt, blijft de optie **Plan automatisch annuleren** behouden. Alleen de status **Bevestigd** of **Uitgecheckt** wordt verwijderd. Het plan blijft geselecteerd. Dat wil zeggen dat werknemers die geen planningsselecties maken tijdens de inschrijvingsperiode voor een levensgebeurtenis, de selectie van het plan niet verliezen. 

5. Selecteer **Opslaan**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
