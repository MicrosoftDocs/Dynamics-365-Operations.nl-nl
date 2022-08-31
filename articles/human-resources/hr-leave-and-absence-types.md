---
title: Verlof- en verzuimtypen configureren
description: Typen verlof instellen die werknemers kunnen aanvragen in Dynamics 365 Human Resources.
author: twheeloc
ms.date: 09/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 982e5afe6442e038774d59419a7edc0a9ec5444c
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/23/2022
ms.locfileid: "9323953"
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

1. Selecteer in de werkruimte **Verlof en verzuim** het tabblad **Koppelingen**.
2. Selecteer onder **Instellingen** de optie **Verlof- en verzuimtypen**.
3. Selecteer **Nieuw**.
4. Voer een naam in voor het verloftype onder **Type**, selecteer een werkstroom bij **Werkstroom-id** en voer een beschrijving in onder **Beschrijving**.
5. Selecteer bij **Algemeen** de optie **Geen**, **Gepland** of **Ongepland** in de vervolgkeuzelijst **Categorie**.
6. Selecteer een inkomstencode in de vervolgkeuzelijst **Inkomstencode**.
7. Geef onder **Redencode vereist** aan of u een redencode wilt vereisen. Als u redencodes wilt vereisen, moet u deze mogelijk toevoegen. Selecteer onder **Redencodes** de optie **Toevoegen**, selecteer een redencode en schakel vervolgens het selectievakje **Ingeschakeld** hiernaast in.
8. Kies onder **Toegang tot geselecteerde rollen beperken** of u de toegang wilt beperken. Selecteer vervolgens de beveiligingsrollen onder **Beveiligingsrollen voor dit verloftype**. De beveiligingsrollen worden gedefinieerd in de werkstroom die u onder **Werkstroom-id** eerder in deze procedure hebt geselecteerd.
9. Kies onder **Agendakleur** welke kleur moet worden weergegeven agenda's voor verlof en verzuim voor dit verloftype. 
10. Geef onder **Uitstelrelaties** op of u wilt dat dit verloftype een ander verloftype uitstelt of door een ander verloftype wordt uitgesteld. Wanneer een verlofaanvraag wordt ingediend voor het uitstellende verloftype, wordt er automatisch een verlofuitstel gemaakt voor het uitgestelde verloftype. 
11. Selecteer **Opslaan**.

## <a name="configure-leave-type-rules"></a>Regels voor verloftypen configureren

1. Stel afrondingsopties in voor het type **Verlof en verzuim**. De beschikbare opties zijn **Geen**, **Naar boven**, **Naar beneden** en **Dichtstbijzijnde**. U kunt ook een afrondingsprecisie instellen voor het verloftype.

2. Stel **Feestdagcorrectie** in voor het verloftype. Wanneer u deze optie selecteert, wordt het aantal feestdagen dat op een werkdag valt, gebruikt om te bepalen hoe het verlof moet worden opgebouwd voor het verloftype. Als kerstdag bijvoorbeeld op een maandag valt, trekt Human Resources een dag af van het verloftype bij het verwerken van toerekeningen.

   U kunt feestdage instellen in de werktijdkalender. Zie [Een werktijdenkalender maken](hr-leave-and-absence-working-time-calendar.md) voor meer informatie.
   
 3. Stel **Verloftype voor transporteren** in voor het verloftype. Wanneer u deze optie selecteert, worden transportsaldi overgeboekt naar het opgegeven verloftype. Het verloftype voor transporteren moet ook worden opgenomen in het plan voor verlof en verzuim. 
 
4. Definieer **vervalregels** voor het verloftype. Wanneer u deze optie configureert, kunt u als eenheid voor dagen of maanden kiezen en de duur instellen voor de vervaldatum. De ingangsdatum van de vervaldatumregel wordt gebruikt om te bepalen wanneer moet worden begonnen met het uitvoeren van de batchtaak die de verlofvervaldatum verwerkt, of de datum waarop de regel van kracht wordt. De vervaldatum zelf is altijd op de begindatum van de toerekeningsperiode. Als de begindatum van de toerekeningsperiode bijvoorbeeld 3 augustus 2021 is en de vervaldatumregel is ingesteld op 6 maanden, wordt de regel verwerkt op basis van de vervaldatumverschuiving vanaf de begindatum van de toerekeningsperiode, zodat deze wordt uitgevoerd op 3 februari 2022. Alle verlofsaldi die aanwezig zijn op het tijdstip van de vervaldatum, worden afgetrokken van het verloftype en worden weergegeven in het verlofsaldo.
 
## <a name="configure-the-required-attachment-per-leave-type"></a>De vereiste bijlage per verloftype configureren

> [!NOTE]
> Als u gebruik wilt maken van het veld **Bijlage vereist**, moet u eerst de functie **Vereiste bijlage voor verlofaanvragen configureren** in Functiebeheer uitvoeren. Zie [Functies beheren](hr-admin-manage-features.md) voor meer informatie over het inschakelen van functies.

1. Selecteer **Verlof- en verzuimtypen** op de pagina **Verlof en verzuim** op het tabblad **Koppelingen** onder **Instellingen**.

2. Selecteer een verlof- en verzuimtype in de lijst. Gebruik vervolgens in de sectie **Algemeen** het veld **Bijlage vereist** om op te geven of een bijlage moet worden geüpload wanneer een werknemer een nieuwe verlofaanvraag voor het geselecteerde verloftype indient. 

Werknemers moeten een bijlage uploaden wanneer ze een nieuwe verlofaanvraag indienen met een verloftype waarop het veld **Bijlage vereist** is ingeschakeld. Als u de bijlage wilt weergeven die als onderdeel van een verlofaanvraag is geüpload, kunnen de goedkeurders van verlofaanvragen de optie **Bijlagen** gebruiken voor de werkitems die aan hen zijn toegewezen. Als een verlofaanvraag wordt toegankelijk gemaakt via de app Human Resources in Microsoft Teams, kunt u de optie **Details weergeven** voor de verlofaanvraag gebruiken om de details en eventuele bijlagen weer te geven.

## <a name="configure-leave-units-hoursdays-per-leave-type"></a>Verlofeenheden (uren/dagen) per verloftype configureren

> [!NOTE]
> Als u de verlofeenheden per verloftypefunctionaliteit wilt gebruiken, moet u de functie **Verlofeenheden configureren per verloftype** in Functiebeheer inschakelen. Zie [Functies beheren](hr-admin-manage-features.md) voor meer informatie over het inschakelen van functies.

> [!IMPORTANT]
> De verloftypen in een rechtspersoon gebruiken standaard de verlofeenheden uit de configuratie van verlofparameters op het niveau van de rechtspersoon.
> 
> De verlofeenheid van het type verlof en verzuim kan alleen worden gewijzigd als er geen verloftransacties voor dat verloftype zijn.
> 
> De functie kan niet meer worden uitgeschakeld wanneer deze eenmaal is ingeschakeld.

1. Selecteer **Verlof- en verzuimtypen** op de pagina **Verlof en verzuim** op het tabblad **Koppelingen** onder **Instellingen**.

2. Selecteer een verlof- en verzuimtype in de lijst. Selecteer vervolgens de verlofeenheid in de sectie **Algemeen** in het veld **Eenheid**. U kunt **Uren** of **Dagen** selecteren.

3. Optioneel: als u **Uren** hebt geselecteerd in het veld **Eenheid**, kunt u het veld **Halve dagdefinitie inschakelen** gebruiken om op te geven of werknemers de eerste halve dag of de tweede helft van de dag vrij kunnen nemen als ze een half dag verlof aanvragen.

Werknemers die een nieuwe verlofaanvraag indienen, kunnen voor het maken van hun verlofaanvraag verschillende verloftypen selecteren. Alle verloftypen die zijn geselecteerd als onderdeel van een verlofaanvraag, moeten echter dezelfde verlofeenheid hebben. Werknemers kunnen de verlofeenheid voor elk verloftype weergeven via het formulier **Verlofaanvragen**.

## <a name="see-also"></a>Zie ook

- [Overzicht van verlof en verzuim](hr-leave-and-absence-overview.md)
- [Een plan voor verlof en verzuim maken](hr-leave-and-absence-plans.md)
- [Een werktijdenkalender maken](hr-leave-and-absence-working-time-calendar.md)
- [Verlof uitstellen](hr-leave-and-absence-suspend-leave.md)
- [Een werkstroom maken voor het aanvragen voor het kopen en verkopen van verlof](hr-leave-and-absence-buy-sell-workflow.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
