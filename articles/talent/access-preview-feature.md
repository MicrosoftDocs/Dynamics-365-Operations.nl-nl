---
title: Toegang tot voorbeeldfuncties in Talent
description: In dit onderwerp wordt beschreven hoe een beheerder de voorbeeldfuncties kan inschakelen en krijgt u een overzicht van de functies die momenteel zijn ingeschakeld voor het voorbeeld.
author: rschloma
manager: AnnBe
ms.date: 04/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.openlocfilehash: cd738cafc97477182e574ee0f363fdcf1df7da7a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "303877"
---
# <a name="access-preview-features-in-talent"></a>Toegang tot voorbeeldfuncties in Talent

[!include[banner](../includes/banner.md)]

Als onderdeel van onze doorlopende implementatie van productmogelijkheden willen we klanten zo snel mogelijk laten kennismaken met nieuwe functies. Beheerders kunnen voorbeeldfuncties in hun omgevingen zien en gebruiken. Deze functies zijn bijna gereed voor algemene beschikbaarheid en zijn uitgebreid getest. Het enige wat we nog willen doen is een definitieve ronde van feedback van klanten en validatie voordat we de functies echt vrijgeven.

In dit onderwerp wordt beschreven hoe een beheerder voorbeeldfuncties kan inschakelen en krijgt u een overzicht van de functies die momenteel beschikbaar zijn als voorbeeld. Deze lijst wordt bijgewerkt wanneer functies algemeen beschikbaar worden en van nieuwe functies kan een voorbeeld worden bekeken. U ontvangt geen melding wanneer van nieuwe functies een voorbeeld kan worden bekeken. Gebruikers zien de functies gewoon verschijnen.

## <a name="enable-or-disable-preview-features"></a>Voorbeeldfuncties in- of uitschakelen

U kunt de instelling **Voorbeeldfuncties** in het Microsoft Dynamics 365 for Talent-beheercentrum gebruiken om voorbeeldfuncties in en uit te schakelen. De instelling is standaard uitgeschakeld. De actie om voorbeeldfuncties in of uit te schakelen is specifiek voor de omgeving.

> [!IMPORTANT]
> Als u de instelling **Voorbeeldfuncties** inschakelt, kunt u voorbeeldfuncties inschakelen voor alle gebruikers in uw organisatie die zich in die omgeving bevinden. Als u de instelling uitschakelt, schakelt u de voorbeeldfuncties uit en zijn ze niet toegankelijk voor uw gebruikers. Voorbeeldfuncties hebben beperkte ondersteuning in Talent. Ze hebben mogelijk minder privacy- en beveiligingsmaatregelen en zijn niet opgenomen in de serviceovereenkomst voor Talent. U moet de voorbeeldfuncties niet gebruiken voor de verwerking van persoonsgegevens (dat wil zeggen informatie die uw identiteit aangeeft) of andere gegevens die onderworpen zijn aan wettelijke of bestuursrechtelijke conformiteitsvereisten.

### <a name="enable-or-disable-preview-features-for-your-organization"></a>Voorbeeldfuncties voor uw organisatie in- of uitschakelen

#### <a name="attract"></a>Aantrekken

1. Aanmelden bij Microsoft Dynamics 365 for Talent: Attract.
2. Selecteer in het menu **Instellen** (het tandwielsymbool) in de rechterbovenhoek **Beheerinstellingen**.
3. Selecteer op het tabblad **Functiebeheer** de optie naast **Voorbeeldfuncties** zodat deze blauw wordt.
4. Desgewenst kunt u afzonderlijke functies beheren door specifieke functies in of uit te schakelen op deze pagina.
5. Vernieuw uw browser om de nieuwe functies te zien. (Alle gebruikers die al zijn geregistreerd, zien de functies de volgende keer dat ze zich aanmelden. Ze kunnen ook hun browser vernieuwen om de functies direct te zien.)

#### <a name="core-hr"></a>Core HR

1. Aanmelden bij Talent De core Human resources-werkruimte wordt geopend, waar u de resterende stappen uitvoert. 
2. Selecteer **Systeembeheer \> Koppelingen Systeemparameters**.
3. Op de pagina **Systeemparameters** op het tabblad **Voorbeeldfuncties** stelt u de optie **Voorbeeldmodus voor alle gebruikers inschakelen** in op **Ja** om voorbeeldfuncties beschikbaar te maken.

> [!NOTE]
> Gebruik de dezelfde basisstappen om voorbeeldfuncties uit te schakelen. Wanneer u voorbeeldfuncties uitschakelt, zijn ze niet meer toegankelijk voor gebruikers en kunnen er fouten optreden in processen die gekoppeld zijn aan de functies.

## <a name="features-that-are-currently-in-preview"></a>Functies waarvan momenteel een voorbeeld kan worden bekeken

### <a name="attract"></a>Aantrekken

- **Relevante kandidaten voor een functie**: wervers en aanstellend managers kunnen eenvoudig zien welke kandidaten het meest relevant zijn voor de functie. De top 5 sollicitanten worden weergegeven op basis van de relevantie van hun cv/profiel voor de functieomschrijving.
- **Relevante functies** : kandidaten zien nu een overzicht van andere functies die relevant voor hen zijn op basis van hun cv/profiel en de functieomschrijvingen.  Dit wordt momenteel weergegeven aan kandidaten zodra deze van toepassing zijn als een suggestie voor andere mogelijkheden.
- **Ondersteuning voor EEO/OFCCP**: nieuwe activiteitstypen maken het gebruik mogelijk van een vooraf gedefinieerd formulier voor het verzamelen van EEO- (Equal Employment Opportunity) en OFCCP-gegevens (Office of Federal Contract Compliance Program) van de kandidaat.  Dit is een vooraf gedefinieerd formulier en kan niet worden bewerkt.

    > [!NOTE]
    > Vacatures die zijn geboekt, zijn alleen zichtbaar voor klanten die zich abonneren op een of meer producten voor het plaatsen van LinkedIn-personeelsadvertenties. Anders zien klanten een vacature alleen als ze er expliciet naar zoeken. Er is een vertraging wanneer taken naar LinkedIn worden geboekt. Het kan enkele uren duren voordat een vacature wordt weergegeven na plaatsing via Attract.

- **Kandidaatsollicitatie** : interne en externe kandidaten kunnen nu rechtstreeks solliciteren via de vacaturepagina op de vacaturesite.
- **Aanbiedingsbeheer** : gebruikers kunnen nu aanbiedingsbrieven maken op basis van sjablonen met tijdelijke aanduidingen. Als kandidaten verdergaan naar de aanbiedingsfase, kunnen personeelswervings- en aanstellingsmanagers het hulpprogramma Aanbieding gebruiken om een formele aanbieding voor de kandidaat voor te bereiden via sjablonen, de aanbieding voor interne goedkeuring te verzenden en ten slotte de aanbieding te verzenden naar de kandidaat voor een handtekening. Vele nieuwe mogelijkheden zullen in de loop van de tijd worden toegevoegd aan het hulpprogramma Aanbieding en de voorbeeldfunctie wordt automatisch bijgewerkt met deze mogelijkheden als we klaar zijn om ze vrij te geven als voorbeeldfuncties.

### <a name="core-hr"></a>Core HR

- **Open inschrijving** : met open inschrijving voor vergoedingen kunnen werknemers eenvoudig zelf hun vergoedingen selecteren. Human Resource-beheerders (HR) kunnen het proces van de open inschrijving voor vergoedingen voor hun organisatie en de inschrijving voor werknemers configureren met behulp van een eenvoudig te volgen begeleide oplossing.

## <a name="feedback"></a>Feedback

Ongeacht of de feedback positief of negatief is, we willen horen wat uw ervaringen zijn met uw gebruik van de voorbeeldfuncties. We raden u aan uw feedback regelmatig op de volgende websites te plaatsen wanneer u deze of andere functies gebruikt.

- [Community](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) : deze site is een goede bron waar gebruikers gebruikstoepassingen kunnen bespreken, vragen kunnen stellen en hulp van de community kunnen krijgen.
- Gebruik de volgende websites om suggesties te doen voor productideeën. Laat ons weten welke functies u wilt zien in het product en ook eventuele wijzigingen die volgens u in de bestaande functies moeten worden aangebracht.

    - [Ideeën voor Attract](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [Core HR](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources)

Vermeld geen persoonlijke gegevens (gegevens die uw identiteit vrijgeven) als u feedback of een productbeoordeling indient. Verzamelde gegevens worden mogelijk verder geanalyseerd en worden niet gebruikt om verzoeken te beantwoorden krachtens van toepassing zijnde privacywetgeving. Persoonlijke gegevens die afzonderlijk voor deze programma's worden verzameld, zijn onderworpen aan de [privacyverklaring van Microsoft](https://privacy.microsoft.com/privacystatement).

> [!TIP]
> Maak een bladwijzer van dit onderwerp en controleer het regelmatig om op de hoogte te blijven van nieuwe voorbeeldfuncties die door ons worden uitgegeven.
