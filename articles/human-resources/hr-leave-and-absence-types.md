---
title: Verlof- en verzuimtypen configureren
description: Typen verlof instellen die werknemers kunnen aanvragen in Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
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
ms.openlocfilehash: df6e34fe6a23e6f0a8307a035752a35a15a3431c
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2020
ms.locfileid: "3198045"
---
# <a name="configure-leave-and-absence-types"></a>Verlof- en verzuimtypen configureren

Verloftypen in Dynamics 365 Human Resources geven de typen verlof aan die werknemers kunnen rapporteren. U kunt de typen verlof aanpassen op basis van de behoeften van uw organisatie. Voorbeelden van verloftypen zijn:

- Betaald verlof
- Onbetaald verlof
- Betaalde vakantie
- Ziekteverlof
- Medisch verlof
- Familieverlof
- Kortdurende arbeidsongeschiktheid
- Verlof bij sterfgeval

## <a name="add-a-leave-type"></a>Een verloftype toevoegen

1. Selecteer op de pagina **Verlof en verzuim** het tabblad **Koppelingen**.

2. Selecteer onder **Instellingen** de optie **Verlof- en verzuimtypen**.

3. Selecteer **Nieuw**.

4. Voer een naam in voor het verloftype onder **Type**, selecteer een werkstroom bij **Werkstroom-id** en voer een beschrijving in onder **Beschrijving**.

5. Selecteer bij **Algemeen** de optie **Geen**, **Gepland** of **Ongepland** in de vervolgkeuzelijst **Categorie**.

6. Selecteer een inkomstencode in de vervolgkeuzelijst **Inkomstencode**.

7. Geef onder **Redencode vereist** aan of u een redencode wilt vereisen. Als u redencodes wilt vereisen, moet u deze mogelijk toevoegen. Selecteer onder **Redencodes** de optie **Toevoegen**, selecteer een redencode en schakel vervolgens het selectievakje **Ingeschakeld** hiernaast in.

8. Kies onder **Toegang tot geselecteerde rollen beperken** of u de toegang wilt beperken. Selecteer vervolgens de beveiligingsrollen onder **Beveiligingsrollen voor dit verloftype**. De beveiligingsrollen worden gedefinieerd in de werkstroom die u onder **Werkstroom-id** eerder in deze procedure hebt geselecteerd.

9. Selecteer **Opslaan**.

## <a name="configure-leave-type-rules"></a>Regels voor verloftypen configureren

1. Stel afrondingsopties in voor het verloftype. De beschikbare opties zijn **Geen**, **Naar boven**, **Naar beneden** en **Dichtstbijzijnde**. U kunt ook een afrondingsprecisie instellen voor het verloftype.

2. Stel **Feestdagcorrectie** in voor het verloftype. Wanneer u deze optie selecteert, gebruikt Human Resources het aantal feestdagen dat op een werkdag valt om te bepalen hoe het verlof moet worden opgebouwd voor het verloftype. Als kerstdag bijvoorbeeld op een maandag valt, trekt Human Resources een dag af van het verloftype bij het verwerken van toerekeningen.

   U kunt feestdage instellen in de werktijdkalender. Zie [Een werktijdenkalender maken](hr-leave-and-absence-working-time-calendar.md) voor meer informatie
   
## <a name="configure-preview-features"></a>Voorbeeldfuncties configureren

Als u de voorbeeldfuncties voor verlof en verzuim hebt ingeschakeld, moet u ook de instellingen hiervoor configureren.

[!include [banner](includes/preview-feature-leave-absence.md)]

1. Kies het verloftype waarnaar transportsaldi moeten worden overgeboekt. U kunt ook een nieuw verloftype maken voor transporteren. 

## <a name="see-also"></a>Zie ook

- [Overzicht van verlof en verzuim](hr-leave-and-absence-overview.md)
- [Een plan voor verlof en verzuim maken](hr-leave-and-absence-plans.md)
- [Een werktijdkalender maken](hr-leave-and-absence-working-time-calendar.md)
