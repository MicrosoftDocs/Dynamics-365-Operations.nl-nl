---
title: Verlof- en verzuimtypen configureren
description: Typen verlof instellen die werknemers kunnen aanvragen in Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 06/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 39e4c4b9c83ca648c21ac20bd20b739af8a6b9ed
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271122"
---
# <a name="configure-leave-and-absence-types"></a>Verlof- en verzuimtypen configureren

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

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

9. Kies onder **Agendakleur** welke kleur moet worden weergegeven agenda's voor verlof en verzuim voor dit verloftype. 

10. Geef onder **Uitstelrelaties** op of u wilt dat dit verloftype een ander verloftype uitstelt of door een ander verloftype wordt uitgesteld. Wanneer een verlofaanvraag wordt ingediend voor het uitstellende verloftype, wordt er automatisch een verlofuitstel gemaakt voor het uitgestelde verloftype. 

10. Selecteer **Opslaan**.

## <a name="configure-leave-type-rules"></a>Regels voor verloftypen configureren

1. Stel afrondingsopties in voor het verloftype. De beschikbare opties zijn **Geen**, **Naar boven**, **Naar beneden** en **Dichtstbijzijnde**. U kunt ook een afrondingsprecisie instellen voor het verloftype.

2. Stel **Feestdagcorrectie** in voor het verloftype. Wanneer u deze optie selecteert, gebruikt Human Resources het aantal feestdagen dat op een werkdag valt om te bepalen hoe het verlof moet worden opgebouwd voor het verloftype. Als kerstdag bijvoorbeeld op een maandag valt, trekt Human Resources een dag af van het verloftype bij het verwerken van toerekeningen.

   U kunt feestdage instellen in de werktijdkalender. Zie [Een werktijdenkalender maken](hr-leave-and-absence-working-time-calendar.md) voor meer informatie
   
 3. Stel **Verloftype voor transporteren** in voor het verloftype. Wanneer u deze optie selecteert, worden transportsaldi overgeboekt naar het opgegeven verloftype. Het verloftype voor transporteren moet ook worden opgenomen in het plan voor verlof en verzuim. 
 
4. Definieer **vervalregels** voor het verloftype. Wanneer u deze optie configureert, kunt u als eenheid voor dagen of maanden kiezen en de duur instellen voor de vervaldatum. De ingangsdatum van de vervaldatumregel wordt gebruikt om te bepalen wanneer moet worden begonnen met het uitvoeren van de batchtaak die de verlofvervaldatum verwerkt, of de datum waarop de regel van kracht wordt. De vervaldatum zelf is altijd op de begindatum van de toerekeningsperiode. Als de begindatum van de toerekeningsperiode bijvoorbeeld 3 augustus 2021 is en de vervaldatumregel is ingesteld op 6 maanden, wordt de regel verwerkt op basis van de vervaldatumverschuiving vanaf de begindatum van de toerekeningsperiode, zodat deze wordt uitgevoerd op 3 februari 2022. Alle verlofsaldi die aanwezig zijn op het tijdstip van de vervaldatum, worden afgetrokken van het verloftype en worden weergegeven in het verlofsaldo.
 
## <a name="see-also"></a>Zie ook

- [Overzicht van verlof en verzuim](hr-leave-and-absence-overview.md)
- [Een plan voor verlof en verzuim maken](hr-leave-and-absence-plans.md)
- [Een werktijdenkalender maken](hr-leave-and-absence-working-time-calendar.md)
- [Verlof uitstellen](hr-leave-and-absence-suspend-leave.md)
- [Een werkstroom maken voor het aanvragen voor het kopen en verkopen van verlof](hr-leave-and-absence-buy-sell-workflow.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
