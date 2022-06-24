---
title: Overzicht van Vergoedingenbeheer
description: In dit artikel wordt een overzicht gegeven van de functie Vergoedingenbeheer in Dynamics 365 Human Resources.
author: twheeloc
ms.date: 12/06/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f008c273a3088353c33ae8c4b0b3cbc6b274fbcf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901142"
---
# <a name="benefits-management-overview"></a>Overzicht van Vergoedingenbeheer


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Om concurrerend te blijven, moet u een uitgebreide reeks vergoedingen bieden om goede werknemers aan te trekken en te behouden. Naast standaardvergoedingen, zoals medische en tandheelkundige dekking, kunt u ook uitgebreide services aanbieden, zoals hulp bij adoptie, recreatieprogramma's en kledingtoelagen. De functie Vergoedingenbeheer in Microsoft Dynamics 365 Human Resources biedt een flexibele oplossing die een breed scala aan vergoedingsopties ondersteunt. Human Resources bevat ook een gebruiksvriendelijke werknemerservaring waarin uw aanbod wordt gepresenteerd.

- De verbeterde functionaliteit voor vergoedingsplannen biedt u de mogelijkheid om unieke vergoedingsplannen te maken en beheren en ondersteunt complexe vergoedingstarieftabellen en geneste niveaus. U kunt eenvoudig vergoedingsprogramma's, bundels en automatische inschrijvingsregels maken voor een gebruiksvriendelijker werknemerservaring.
- Via flex-kredietprogramma's kunt u zorgen voor een evenredige verdeling van kredieten voor ondersteuning bij pensioenering en andere levensgebeurtenissen.
- De uitgebreide regels om te controleren of iemand voor een bepaalde vergoeding in aanmerking komt, zorgen ervoor dat u de juiste vergoedingen voor de juiste werknemers kunt maken.
- U kunt werknemers een gebruiksvriendelijke optie bieden om zich online in te schrijven voor vergoedingen.
- De verwerking van gekwalificeerde levensgebeurtenissen ondersteunt toekomstige levensgebeurtenissen.

Als u toegang wilt tot de demogegevens, moet u de sandbox-omgeving opnieuw implementeren.

> [!NOTE]
> U kunt nu Vergoedingenbeheer-pagina's aanpassen. Aangepaste velden voor dekkingspercentages kunnen op de pagina **Dekkingsoptie** voor vergoedingsplannen worden toegevoegd. Meer informatie over werken met aangepaste velden vindt u in [Aangepaste velden](hr-developer-custom-fields.md).
>
> ![Aangepaste velden in Vergoedingenbeheer](media/hr-benefits-management-custom-fields.png)

## <a name="enable-benefits-management"></a>Vergoedingenbeheer inschakelen

In dit artikel wordt beschreven hoe u functies inschakelt in Human Resources. Ook wordt uitgelegd welke bestaande functies in Human Resources door Vergoedingenbeheer worden vervangen en welke functies worden uitgeschakeld nadat u Vergoedingenbeheer hebt ingeschakeld.

> [!IMPORTANT]
> Nadat u Vergoedingenbeheer in een **productieomgeving** hebt ingeschakeld, kunt u dit niet meer uitschakelen. U wordt aangeraden Vergoedingenbeheer in een **sandbox**-omgeving in te schakelen en te testen voordat u dit in een **productieomgeving** activeert. Er zijn belangrijke verschillen tussen de verouderde vergoedingsfunctionaliteit en de nieuwe functionaliteit voor Vergoedingenbeheer. Hiervoor zijn aanvullende instellingen nodig die moeten worden getest voordat ze in de productie worden gebracht.

Zie [Functies beheren](hr-admin-manage-features.md) voor meer informatie.

## <a name="process-overview"></a>Procesoverzicht

Het configureren van vergoedingen omvat de volgende taken:

1.  Vereiste vergoedingsinformatie instellen.
2.  Optionele vergoedingsinformatie instellen.
3.  Vergoedingsplannen instellen.
4.  Programma's voor flexibel krediet instellen (optioneel).
5.  Vereiste werknemersinformatie configureren.
6.  Optionele werknemersinformatie configureren.
7.  Werknemers verwerken om hun geschiktheid te bepalen.
8.  Werknemers selecteren plannen via Werknemerselfservice (optioneel).
9.  Werknemerplanselecties bevestigen.
10. Verwerking van levensgebeurtenissen (optioneel).
11. Tariefupdates (optioneel).

## <a name="set-up-required-benefit-information"></a>Vereiste vergoedingsinformatie instellen

Voordat werknemers bij de plannen kunnen worden ingeschreven, moeten er meerdere onderdelen worden ingesteld:

- **Vergoedingsbeheerparameters**: deze instellingen worden door bedrijven gedeeld. U kunt standaard redencodes instellen, de **Vergoedingen jaarsalaris** inschakelen, een standaardbetalingsfrequentie instellen voor nieuw aangenomen werknemers en levensgebeurtenissen inschakelen. Zie [Parameters voor Vergoedingenbeheer instellen](hr-benefits-setup-parameters.md) voor meer informatie.
- **Geschiktheidsopties van persoonlijke contactpersonen**: persoonlijke contactpersonen zijn de personen die afhankelijken of begunstigden zijn van de plannen die zijn ingesteld. Gewoonlijk zijn dit kinderen, echtgenoten/echtgenotes of vertrouwensorganisaties. Zie [Opties voor geschiktheid van persoonlijke contactpersonen configureren](hr-benefits-setup-contact-eligibility-options.md) voor meer informatie.
- **Dekkingsopties**: de typen dekking instellen die beschikbaar zullen zijn voor een plan. Definieer met name wie gedekt moet worden of hoeveel dekking er beschikbaar is. Zie [Opties voor dekking maken](hr-benefits-setup-coverage-options.md) voor meer informatie.
- **Plantypen**: de typen plannen instellen die beschikbaar zullen zijn wanneer u een vergoedingsplan maakt. Voorbeelden van plantypen zijn **Tandartsverzekering**, **Zicht** en **Spaarplan**. Bepaalde belangrijke instellingen voor het plantype bepalen de instellingen die beschikbaar zijn voor het vergoedingsplan. Zie [Plantypen maken](hr-benefits-setup-plan-types.md) voor meer informatie.
- **Geschiktheidsregels**: geschiktheidsregels worden gebruikt om te bepalen of een werknemer in aanmerking komt voor een regeling. Aan elk vergoedingsplan moet ten minste één geschiktheidsregel worden gekoppeld. Zie [Regels en opties voor geschiktheid configureren](hr-benefits-setup-eligibility-rules.md) voor meer informatie.
- **Betalingsfrequenties:** betalingsfrequenties zijn vereist wanneer vergoedingstarieven zijn geconfigureerd. De betalingsfrequentie die voor een tarief wordt gebruikt, helpt bij het bepalen hoeveel de werknemer en/of werkgever wekelijks, maandelijks of jaarlijks verschuldigd is. Zie [Betalingsfrequenties instellen](hr-benefits-setup-payment-frequencies.md) voor meer informatie.
- **Tarieven**: tarieven bepalen hoeveel een vergoeding de werknemer of de werkgever gaat kosten. Als geld moet worden terugbetalen aan een werknemer (bijvoorbeeld een krediet voor een lidmaatschap van een sportschool), wordt een negatief tarief ingevoerd. Zie [Tarieven configureren](hr-benefits-setup-rates.md) voor meer informatie.
- **Niveautarieven**: niveautarieven worden gebruikt wanneer een tarief moet worden gewijzigd op basis van bepaalde criteria. Het meest algemene niveautarief is een enkel niveau dat is gebaseerd op leeftijd. Er kunnen echter ook dubbele niveaus worden ingesteld, waarbij het tarief kan veranderen op basis van geslacht, leeftijd of andere criteria.
- **Inhoudingen**: de inhoudingen zijn in principe de koptekstgegevens/codes die aan de salarisadministratie worden doorgegeven om de inhouding voor de vergoeding te identificeren. U moet deze inhoudingen instellen, omdat deze vereist zijn voor de vergoedingsregeling. Zie [Inhoudingen configureren](hr-benefits-setup-deductions.md) voor meer informatie.
- **Vergoedingsperioden**: een vergoedingsperiode is de periode waarin werknemers vergoedingsdekking krijgen. Het wordt ook een planjaar genoemd. De openstaande inschrijvingsperioden worden hier eveneens ingesteld.

## <a name="set-up-optional-benefit-information"></a>Optionele vergoedingsinformatie instellen

U hoeft de volgende onderdelen niet in te stellen om een vergoedingsplan te maken:

- **Programma's** : een programma is een set vergoedingen die worden geregeld door dezelfde geschiktheidsregels. Iedereen op de verkoopafdeling krijgt bijvoorbeeld een mobiele telefoon.
- **Bundels**: een bundel is een groep vergoedingen, waarbij één plan moet worden geselecteerd voordat de optie voor het selecteren van aanvullende plannen beschikbaar is. Een goed aftrekbaar medisch plan kan bijvoorbeeld worden gebundeld met een HSA-plan (Health Savings Account), oftewel een spaarrekening voor gezondheidszorg.
- **Typen levensgebeurtenissen**: levensgebeurtenissen zijn gebeurtenissen waarmee een wijziging in de dekking van een werknemer mogelijk is. Typen levensgebeurtenissen zijn aan een plantype gekoppeld. Een type medisch plan staat bijvoorbeeld wijzigingen in plannen toe vanwege een geboorte of adoptie, of vanwege een wijziging in de burgerlijke staat. In een verzekeringsplantype zijn echter mogelijk geen wijzigingen toegestaan als gevolg van levensgebeurtenissen. Zie [Typen levensgebeurtenissen configureren](hr-benefits-setup-life-event-types.md) voor meer informatie.
- **Wachtdagen en wachttijden**: er kan een dekkingsperiode voor een vergoedingsplan worden ingesteld. Een nieuw in dienst genomen werknemer kan bijvoorbeeld pas voor een 401(k) inschrijven na een dienstverband van drie maanden. In dit geval bedraagt de wachttijd drie maanden. Wachtdagen worden gebruikt in de wachttijd als nieuwe inschrijvingen alleen op een bepaalde dag van de maand kunnen worden verwerkt en ingediend bij de leverancier. Als 401(k)-inschrijvingen bijvoorbeeld alleen op de vijftiende van de maand kunnen worden verwerkt, na een dienstverband van drie maanden, bedraagt de wachttijd drie maanden en is de wachtdag de vijftiende. Zie [Wachtdagen configureren](hr-benefits-setup-waiting-days.md) en [Wachttijden configureren](hr-benefits-setup-waiting-periods.md) voor meer informatie.
- **Redencodes**: redencodes worden gebruikt om uit te leggen waarom een vergoeding voor een werknemer kan worden gewijzigd. Zie [Redencodes instellen](hr-benefits-setup-reason-codes.md) voor meer informatie.

## <a name="set-up-benefit-plans"></a>Vergoedingsplannen instellen

Wanneer u een vergoedingsplan instelt, moet u de volgende stappen voltooien voordat werknemers kunnen worden ingeschreven:

- Een vergoedingsperiode toewijzen.
- Dekkingsopties koppelen.
- Stel een geldige begin- en einddatum in op het tabblad **Algemeen**.
- Wijs ten minste één geschiktheidsregel toe.
- Stel het veld **Inschrijving toestaan/voortzetten** op het tabblad **Instellen** in.

Zie [Vergoedingsplannen instellen](hr-benefits-plans-setup.md) voor meer informatie over het instellen van vergoedingsplannen.

## <a name="set-up-flex-credit-programs-optional"></a>Programma's voor flexibel krediet instellen (optioneel)

U kunt flex-kredietprogramma's gebruiken om werknemers in te schrijven voor vergoedingen op basis van een vooraf bepaald aantal flex-kredieten. Werknemers kunnen kiezen hoe hun flex-kredieten worden toegewezen. Als werknemers bijvoorbeeld al onder de zorgverzekering van hun echtgenoot/echtgenote vallen, hoeven ze hun kredieten niet voor de zorgverzekering te gebruiken. Daarom willen ze deze mogelijk voor andere vergoedingen gebruiken. Zie [Programma's voor flexibel krediet instellen](hr-benefits-plans-flex-credit-programs.md)  voor meer informatie over flexkredietprogramma's.

## <a name="configure-required-employee-information"></a>Vereiste werknemersinformatie configureren

Voordat u werknemers voor vergoedingen kunt inschrijven, moet u de vereiste informatie voor hen opgeven. 

Aan de werknemer moet een **functie** zijn toegewezen. Een **functie** kan op de pagina **Werknemer** of **Functie** aan de werknemer worden toegewezen door de **medewerkerstoewijzing** bij te werken. 

Vervolgens moeten werknemers worden ingeschreven voor een plan voor vaste compensatie op de begindatum of ze moeten een **jaarlijks salarisbedrag voor vergoedingen** hebben. Voordat **vaste compensatie** aan een werknemer wordt toegewezen, moet een **functie** worden toegewezen. 

> [!NOTE] 
> De **begindatum voor vaste compensatie** kan niet vóór de **datum van de positietoewijzing** vallen.

Als u een werknemer hebt die een aanvullende vergoeding krijgt, zoals provisies, kunt u ook een **jaarlijks salarisbedrag voor vergoedingen** uit de werknemerrecord toevoegen. Human Resources gebruikt het **jaarlijkse salarisbedrag voor vergoedingen** om de dekkingsbedragen vast te stellen in plaats van het **vaste jaarlijkse compensatiebedrag**. Het **Jaarlijks salarisbedrag voor vergoedingen** moet geldig zijn vanaf de begindatum van de werknemer of het begin van de vergoedingsperiode, afhankelijk van het laatste. Een functie is echter niet vereist om het **jaarlijkse salarisbedrag** toe te wijzen. U schakelt de functie **Vergoedingen jaarsalaris** in op het tabblad **Vergoedingenbeheer** van de pagina **Gedeelde Human Resources-parameters**. Deze functie is standaard uitgeschakeld.

> [!IMPORTANT]
> Als er voor een werknemer zowel een **vast compensatiebedrag** als een **jaarlijks salarisbedrag voor vergoedingen** is ingevoerd, wordt het **jaarlijkse salarisbedrag voor vergoedingen** gebruikt bij het bepalen van de bedragen van de dekking. In de sectie **Details dienstverband** van de pagina **Werknemer** moet u een waarde selecteren in het veld **Vergoedingsfrequentie**.

## <a name="configure-optional-employee-information"></a>Optionele werknemersinformatie configureren
Wanneer u een vergoedingsplan maakt dat tarieven op basis van geslacht of leeftijd gebruikt, moet u een geboortedatum en geslacht invoeren voor de werknemer om de kosten van de vergoeding te berekenen.

## <a name="process-employees-to-determine-eligibility"></a>Werknemers verwerken om hun geschiktheid te bepalen
Voordat werknemers bij een regeling kunnen worden ingeschreven, wordt er een geschiktheidsverwerking uitgevoerd om te bepalen voor welke plannen zij in aanmerking komen. U kunt de resultaten van het geschiktheidsproces weergeven in de **viewer voor procesresultaten**. Zie [Geschiktheid voor inschrijving verwerken](hr-benefits-process-enrollment-eligibility.md) voor meer informatie.

## <a name="employees-select-plans-using-employee-self-service-optional"></a>Werknemers selecteren plannen via **Werknemerselfservice** (optioneel)

Wanneer openstaande inschrijving plaatsvindt, werknemers pas in dienst zijn genomen of een levensgebeurtenis plaatsvindt, kunnen werknemers hun vergoedingen selecteren of bijwerken via **Werknemerselfservice**. Zie [Werknemerselfservice configureren](hr-benefits-setup-employee-self-service.md) voor meer informatie.

## <a name="confirm-employee-plan-selections"></a>Werknemerplanselecties bevestigen

De vergoedingen die werknemers selecteren, moeten worden bevestigd voordat de werknemers als ingeschreven worden beschouwd. Vergoedingen kunnen ook namens een werknemer worden geselecteerd. Als u vergoedingen wilt selecteren of bevestigen, selecteert u op de pagina **Werknemer** op het tabblad **Vergoedingen** de optie **Vergoedingsplannen voor werknemers**. Als u vergoedingen voor meerdere werknemers wilt selecteren of bevestigen, gebruikt u de pagina **Bulkupdate van vergoedingsplannen voor medewerkers**.

## <a name="life-event-processing-optional"></a>Verwerking van levensgebeurtenissen (optioneel)

Tijdens de levenscyclus van de werknemer kan elke werknemer verschillende levensgebeurtenissen meemaken, zoals huwelijk, wijzigingen in dienstverband of wijzigingen in afhankelijken of begunstigden. Als u levensgebeurtenissen wilt gebruiken, moet u deze inschakelen op de pagina **Gedeelde Human Resources-parameters**. Stel typen levensgebeurtenissen en opties voor levensgebeurtenissen voor plantypen in.

Voordat u de levensgebeurtenissen kunt verwerken, moet u minimaal eenmaal een open inschrijving hebben uitgevoerd tijdens een aanstellingstijdvak. In de Verenigde Staten vindt open inschrijving meestal eenmaal per jaar plaats. Buiten de Verenigde Staten kan open inschrijving worden uitgevoerd op het moment van de aanstelling. Voor de verwerking van levensgebeurtenissen hoeven werknemers geen vergoedingsplan te selecteren. De werknemers moeten echter zijn opgenomen in de verwerking van openstaande inschrijvingen. Zie de volgende onderwerpen voor meer informatie:

- [Levensgebeurtenissen verwerken](hr-benefits-process-life-events.md)
- [Wijzigingen in levensgebeurtenissen verwerken](hr-benefits-process-life-event-changes.md)
- [Geschiktheid voor levensgebeurtenissen verwerken](hr-benefits-process-life-event-eligibility.md)

## <a name="rate-updates-optional"></a>Tariefupdates (optioneel)

Soms verandert het percentage van een vergoeding tijdens de planperiode. Als u de tarieven wilt bijwerken voor werknemers die al zijn ingeschreven voor de planning, moet u de tariefwijzigingen verwerken. Zie [Wijzigingen in tarieven verwerken](hr-benefits-process-rate-changes.md) voor meer informatie.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
