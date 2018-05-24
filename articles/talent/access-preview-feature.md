---
title: Toegang tot voorbeeldfuncties in Dynamics 365 for Talent
description: In dit onderwerp wordt beschreven hoe een beheerder de voorbeeldfuncties kan inschakelen en krijgt u een overzicht van de functies die momenteel zijn ingeschakeld voor het voorbeeld.
author: rschloma
manager: AnnBe
ms.date: 04/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.translationtype: HT
ms.sourcegitcommit: 2e5dd8f852ac1a6c2997a50a60f03db6adfd218c
ms.openlocfilehash: 5500bfc1cdd1949d301ae82fad5506dfdbeb59f3
ms.contentlocale: nl-nl
ms.lasthandoff: 05/01/2018

---

# <a name="access-preview-features-in-dynamics-365-for-talent"></a>Toegang tot voorbeeldfuncties in Dynamics 365 for Talent 

[!include[banner](../includes/banner.md)]

Als onderdeel van onze doorlopende implementatie van productmogelijkheden willen we klanten zo snel mogelijk laten kennismaken met nieuwe functies. Beheerders kunnen voorbeeldfuncties in hun omgevingen zien en gebruiken. Deze functies zijn bijna gereed voor algemene beschikbaarheid en zijn uitgebreid getest. Het enige wat we nog willen doen is een definitieve ronde van feedback van klanten en validatie voordat we de functies echt vrijgeven.

In dit onderwerp wordt beschreven hoe een beheerder voorbeeldfuncties kan inschakelen en krijgt u een overzicht van de functies die momenteel beschikbaar zijn als voorbeeld. Deze lijst wordt bijgewerkt wanneer functies algemeen beschikbaar worden en van nieuwe functies kan een voorbeeld worden bekeken. U ontvangt geen melding wanneer van nieuwe functies een voorbeeld kan worden bekeken. Gebruikers zien de functies gewoon verschijnen.

## <a name="enable-or-disable-preview-features"></a>Voorbeeldfuncties in- of uitschakelen

U kunt de instelling **Voorbeeldfuncties** in Microsoft Dynamics 365 voor Talent-beheercentrum gebruiken om voorbeeldfuncties in en uit te schakelen. De instelling is standaard uitgeschakeld. De actie om voorbeeldfuncties in of uit te schakelen is specifiek voor de omgeving.

> [!IMPORTANT]
> Als u de instelling **Voorbeeldfuncties** inschakelt, kunt u voorbeeldfuncties inschakelen voor alle gebruikers in uw organisatie die zich in die omgeving bevinden. Als u de instelling uitschakelt, schakelt u de voorbeeldfuncties uit en zijn ze niet toegankelijk voor uw gebruikers. Voorbeeldfuncties hebben beperkte ondersteuning in Talent. Ze hebben mogelijk minder privacy- en beveiligingsmaatregelen en zijn niet opgenomen in de serviceovereenkomst voor Talent. U moet de voorbeeldfuncties niet gebruiken voor de verwerking van persoonsgegevens (dat wil zeggen informatie die uw identiteit aangeeft) of andere gegevens die onderworpen zijn aan wettelijke of bestuursrechtelijke conformiteitsvereisten.

### <a name="enable-or-disable-preview-features-for-your-organization"></a>Voorbeeldfuncties voor uw organisatie in- of uitschakelen

#### <a name="attract"></a>Attract

1. Meld u aan bij Microsoft Dynamics 365 for Talent: Attract.
2. Selecteer in het menu **Instellen** (het tandwielsymbool) in de rechterbovenhoek **Beheerinstellingen**.
3. Selecteer op het tabblad **Functiebeheer** de optie naast **Voorbeeldfuncties** zodat deze blauw wordt.
4. Vernieuw uw browser om de nieuwe functies te zien. (Alle gebruikers die al zijn geregistreerd, zien de functies de volgende keer dat ze zich aanmelden. Ze kunnen ook hun browser vernieuwen om de functies direct te zien.)

#### <a name="core-hr"></a>Core HR

1. Aanmelden bij Talent De core Human resources-werkruimte wordt geopend, waar u de resterende stappen uitvoert. 
2. Selecteer **Systeembeheer \> Koppelingen Systeemparameters**.
3. Op de pagina **Systeemparameters** op het tabblad **Voorbeeldfuncties** stelt u de optie **Voorbeeldmodus voor alle gebruikers inschakelen** in op **Ja** om voorbeeldfuncties beschikbaar te maken.

> [!NOTE]
> Gebruik de dezelfde basisstappen om voorbeeldfuncties uit te schakelen. Wanneer u voorbeeldfuncties uitschakelt, zijn ze niet meer toegankelijk voor gebruikers en kunnen er fouten optreden in processen die gekoppeld zijn aan de functies.

## <a name="features-that-are-currently-in-preview"></a>Functies waarvan momenteel een voorbeeld kan worden bekeken

### <a name="attract"></a>Attract

- **Vacaturesjablonen**: u kunt nu sjablonen voor het aanstellingsproces maken. Gebruikers kunnen het aanstellingsproces al voor een bepaalde vacature aanpassen. Ze kunnen echter nu sjablonen maken voor het proces en vervolgens de gewenste sjabloon selecteren wanneer een bepaalde vacature wordt gemaakt. Daarom helpt deze functie het vacature-instellingsproces te stroomlijnen.
- **Vacaturesite** : met de huidige versie van de vacaturesite worden alleen alle openstaande vacatures weergegeven. Er worden echter meer mogelijkheden aan de site toegevoegd in de toekomst. Vacatures kunnen als intern of extern worden gemarkeerd. Interne gebruikers die zich bij de site aanmelden, zien zowel interne als externe vacatures. Niet-interne gebruikers en gebruikers die niet zijn aangemeld, zien alleen externe vacatures.
- **Personeelsadvertentie plaatsen** : u kunt nu vacatures plaatsen op de vacaturesite.
- **LinkedIn-personeelsadvertentie plaatsen** : u kunt nu vacatures plaatsen op LinkedIn.

    > [!NOTE]
    > Vacatures die zijn geboekt, zijn alleen zichtbaar voor klanten die zich abonneren op een of meer producten voor het plaatsen van LinkedIn-personeelsadvertenties. Anders zien klanten een vacature alleen als ze er expliciet naar zoeken. Er is een vertraging wanneer taken naar LinkedIn worden geboekt. Het kan enkele uren duren voordat een vacature wordt weergegeven na plaatsing via Attract.

- **Kandidaatsollicitatie** : interne en externe kandidaten kunnen nu rechtstreeks solliciteren via de vacaturepagina op de vacaturesite.
- **Beoordelingen** : als onderdeel van het configureerbare aanstellingsproces kunnen gebruikers nu voor een specifieke vacature of wanneer een vacature wordt gebruikt, toegang krijgen tot een nieuw activiteitstype **Beoordeling**. Zij kunnen vervolgens de app Project: 'Gauge' in Talent gebruiken om algemene beoordelingen samen te stellen die zij aan kandidaten kunnen verzenden. Project: 'Gauge' is ook als openbaar voorbeeld beschikbaar. Aanvullende providers worden in de toekomst toegevoegd.
- **Project: 'Gauge'** : Project: 'Gauge' is een app in Talent waarmee gebruikers eenvoudig beoordelingen of enquêtes kunnen maken.
- **Aanbiedingsbeheer** : gebruikers kunnen nu aanbiedingsbrieven maken op basis van sjablonen met tijdelijke aanduidingen. Als kandidaten verdergaan naar de aanbiedingsfase, kunnen personeelswervings- en aanstellingsmanagers het hulpprogramma Aanbieding gebruiken om een formele aanbieding voor de kandidaat voor te bereiden via sjablonen, de aanbieding voor interne goedkeuring te verzenden en ten slotte de aanbieding te verzenden naar de kandidaat voor een handtekening. Vele nieuwe mogelijkheden zullen in de loop van de tijd worden toegevoegd aan het hulpprogramma Aanbieding en de voorbeeldfunctie wordt automatisch bijgewerkt met deze mogelijkheden als we klaar zijn om ze vrij te geven als voorbeeldfuncties.

### <a name="core-hr"></a>Core HR

- **Open inschrijving** : met open inschrijving voor vergoedingen kunnen werknemers eenvoudig zelf hun vergoedingen selecteren. Human Resource-beheerders (HR) kunnen het proces van de open inschrijving voor vergoedingen voor hun organisatie en de inschrijving voor werknemers configureren met behulp van een eenvoudig te volgen begeleide oplossing.

## <a name="feedback"></a>Feedback

Ongeacht of de feedback positief of negatief is, we willen horen wat uw ervaringen zijn met uw gebruik van de voorbeeldfuncties. We raden u aan uw feedback regelmatig op de volgende websites te plaatsen wanneer u deze of andere functies gebruikt.

- [Community](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) : deze site is een goede bron waar gebruikers gebruikstoepassingen kunnen bespreken, vragen kunnen stellen en hulp van de community kunnen krijgen.
- Gebruik de volgende websites om suggesties te doen voor productideeën. Laat ons weten welke functies u wilt zien in het product en ook eventuele wijzigingen die volgens u in de bestaande functies moeten worden aangebracht.

    - [Ideeën voor Attract](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [Core HR](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources)

Vermeld geen persoonlijke gegevens (gegevens die uw identiteit vrijgeven) als u feedback of een productbeoordeling indient. Verzamelde gegevens worden mogelijk verder geanalyseerd en worden niet gebruikt om verzoeken te beantwoorden krachtens van toepassing zijnde privacywetgeving. Persoonlijke gegevens die afzonderlijk voor deze programma's worden verzameld, zijn onderworpen aan de [privacyverklaring van Microsoft](https://privacy.microsoft.com/en-us/privacystatement).

> [!TIP]
> Maak een bladwijzer van dit onderwerp en controleer het regelmatig om op de hoogte te blijven van nieuwe voorbeeldfuncties die door ons worden uitgegeven.

