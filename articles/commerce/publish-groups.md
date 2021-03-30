---
title: Werken met publicatiegroepen
description: In dit onderwerp wordt de functie voor publicatiegroepen in Microsoft Dynamics 365 Commerce beschreven.
author: phinneyridge
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b623573f598f6b21291cafe95fa04e6777cffe11
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244834"
---
# <a name="work-with-publish-groups"></a>Werken met publicatiegroepen


[!include [banner](includes/banner.md)]

In dit onderwerp wordt de functie voor publicatiegroepen in Microsoft Dynamics 365 Commerce beschreven.

## <a name="overview"></a>Overzicht

E-commerce-websites worden gedurende het hele jaar bijgewerkt met nieuwe inhoud. Updates worden vaak gepubliceerd in batches rond drukke e-commerce-evenementen, zoals vakanties, seizoensgebonden marketingcampagnes of promotionele lanceringen. Deze updates vereisen vaak dat groepen website-inhoud (bijvoorbeeld pagina's, afbeeldingen, fragmenten en sjablonen) worden klaargezet, gevalideerd en gelijktijdig worden gepubliceerd in één actie.

De mogelijkheid om items te groeperen in logische sets om items samen te publiceren, waarbij elke set een eigen levenscyclus heeft, biedt auteurs van sites veel voordelen. In Commerce staan deze logische verzamelingen bekend als publicatiegroepen. Hiermee kunnen site-auteurs sets van updates bijhouden als hun eigen configureerbare, testbare en publiceerbaar entiteiten.

Auteurs kunnen updates bekijken in een klaargezette publicatiegroep zonder dat dit gevolgen heeft voor de live site of andere zelfstandige publicatiegroepen. Auteurs kunnen de publicatieactie vervolgens plannen om alle items in de publicatiegroep tegelijkertijd naar de live site te publiceren. De mogelijkheid om updates voor publicatie te groeperen, bekijken en plannen is belangrijk voor veel bedrijven op ondernemingsniveau die een aanzienlijke jaarlijkse omzet genereren rond op gebeurtenissen gebaseerde site-updatemijlpalen.

Bedrijven kunnen kosten maken door trage of ongeldige inhoudsimplementaties die niet soepel verlopen. Met publicatiegroepen kunt u er zeker van zijn dat lanceringen op tijd worden georganiseerd, gevalideerd en gepubliceerd. Of ze nu groot of klein zijn, publicatiegroepen bieden een waardevolle toolset waarmee auteurs doorlopende site-updatetaken kunnen organiseren en vereenvoudigen.

## <a name="when-to-use-publish-groups"></a>Wanneer u publicatiegroepen gebruikt

U kunt publicatiegroepen gebruiken wanneer u meerdere documenten tegelijk moet uitbrengen en publiceren. Als de inhoud van uw website bijvoorbeeld elk seizoen moet worden bijgewerkt, kunt u publicatiegroepen maken voor deze seizoensgebonden marketingbewegingen. De publicatiegroep Seizoensupdate herfst kan nieuwe seizoensgebonden afbeeldingen bevatten, fragmenten met seizoensgebonden marketingberichten, pagina's met seizoensgebonden verzamelingen van producten of andere seizoensgebonden website-updates.

Een voordeel van publicatiegroepen is dat u meerdere updates parallel kunt uitbrengen. Kort na de update voor de publicatiegroep Seizoensupdate herfst kan er bijvoorbeeld een inhoudsupdate voor een bepaald vakantieweekend beschikbaar zijn. In dit geval kunt u tegelijkertijd inhoud voor de publicatiegroepen Seizoensupdate herfst en Update herfstvakantie uitbrengen. Elke publicatiegroep bevat een eigen unieke set pagina's, afbeeldingen, fragmenten, sjablonen, enzovoort. U deze twee publicatiegroepen onafhankelijk van elkaar, maar gelijktijdig uitbrengen, bekijken en valideren. Elke publicatiegroep kan vervolgens worden gepland om op specifieke datums en tijdstippen live te gaan op uw site.

## <a name="turn-on-the-publish-groups-feature"></a>De functie voor publicatiegroepen inschakelen

De functie voor publicatiegroepen is optioneel en moet worden ingeschakeld voor uw site.

Ga als volgt te werk om de functie voor publicatiegroepen voor uw site in te schakelen in de Commerce-ontwerpfunctie.

1. Selecteer in het linkernavigatievenster de optie **Site-instellingen** om deze uit te vouwen.
1. Selecteer **Functies** onder **Site-instellingen**.
1. Stel de optie **Publicatiegroepen** in op **Aan**.

## <a name="create-a-publish-group"></a>Een publicatiegroep maken

Ga als volgt te werk om een publicatiegroep voor uw site te maken in de Commerce-ontwerpfunctie.

1. Selecteer **Publicatiegroepen** in het navigatievenster aan de linkerkant.
1. Selecteer **Nieuw** op de opdrachtbalk.
1. Voer in het dialoogvenster **Publicatiegroep maken** onder **Naam van publicatiegroep** een beschrijvende naam in. Selecteer vervolgens **OK**.

## <a name="set-the-publish-group-authoring-context"></a>De auteurscontext van de publicatiegroep instellen

In Commerce is de standaardauteurscontext de context van de live site. De auteurscontext van de live site is de standaardweergave waarin u uw website direct kunt bekijken en wijzigen zonder gebruik te hoeven maken van een publicatiegroep. De nieuwste directe updates voor de gepubliceerde versie van uw site worden hierin weergegeven. Als het contextbesturingselement onder **Publicatiegroepen** in het linkernavigatievenster de naam **Live site** bevat, werkt u in de auteurscontext van de live site. **Live site** is de standaardnaam van het contextbesturingselement. In het andere geval wordt de naam van een publicatiegroep weergegeven.

Als u in een publicatiegroep wilt werken, moet u hiervoor overschakelen naar de auteurscontext voor publicatiegroepen. Ga als volgt te werk om de context van de publicatiegroep in te stellen.

- Selecteer in het linkernavigatievenster het contextbesturingselement direct onder **Publicatiegroepen** en selecteer vervolgens de naam van de publicatiegroep in de lijst met opties die wordt weergegeven. De naam van het contextbesturingselement wordt gewijzigd in de naam van de publicatiegroep.
- Selecteer in het linkernavigatievenster de optie **Publicatiegroepen** en selecteer vervolgens onder **Publicatiegroepen** de naam van de publicatiegroep. De naam van het contextbesturingselement wordt gewijzigd in de naam van de publicatiegroep.

Nadat u de auteurscontext van de publicatiegroep hebt ingesteld, werkt u in de context van die publicatiegroep wanneer u site-inhoud bekijkt en bewerkt.

Als u wilt terugkeren naar de auteurscontext van de live site (standaard), selecteert u het contextbesturingselement en vervolgens **Live site**.

## <a name="add-pages-or-other-items-to-a-publish-group"></a>Pagina's of andere items toevoegen aan een publicatiegroep

Nadat u een auteurscontext voor publicatiegroepen hebt geselecteerd en de naam hiervan wordt weergegeven in het linkernavigatievenster, kunt u op dezelfde manier inhoud maken als in de standaard live-sitecontext. U kunt ook bestaande pagina's of andere items uit andere publicatiegroepen of via de live-sitecontext toevoegen.

Ga als volgt te werk om bestaande pagina's naar een publicatiegroep te kopiëren.

1. Selecteer de auteurscontext waaruit u wilt kopiëren en selecteer vervolgens in het linkernavigatievenster de optie **Pagina's**.
1. Selecteer de pagina die u aan een publicatiegroep wilt toevoegen.
1. Selecteer **Kopiëren naar publicatiegroep** op de opdrachtbalk.
1. Selecteer in het dialoogvenster **Een publicatiegroep selecteren** de publicatiegroep die u wilt toevoegen aan de pagina en selecteer vervolgens **OK**.

U kunt dezelfde basisstappen gebruiken om aangepaste productpagina's, URL's, sjablonen, lay-outs, fragmenten en mediabibliotheekelementen te maken of om bestaande items van deze typen toe te voegen aan een publicatiegroep.

## <a name="validate-a-publish-group"></a>Een publicatiegroep valideren

Om ervoor te zorgen dat alle afhankelijkheden in de inhoud van de publicatiegroep worden gerespecteerd zijn en alle validaties worden doorgegeven, kunt u een validatie uitvoeren om eventuele problemen te identificeren die moeten worden aangepakt voordat u een actie voor publiceren plant.

Ga als volgt te werk om uw publicatiegroep te valideren voordat u deze plant.

1. Selecteer **Publicatiegroepen** in het navigatievenster aan de linkerkant.
1. Selecteer de publicatiegroep die u wilt valideren.
1. Selecteer **Valideren** op de opdrachtbalk.

De validatie wordt uitgevoerd op alle inhoud in de publicatiegroep. Eventuele problemen die een geslaagde publicatieactie verhinderen, worden weergegeven in een meldingsvenster in de rechterbovenhoek.

> [!NOTE]
> Validatie wordt altijd automatisch uitgevoerd wanneer een publicatiegroep wordt gepland. De knop **Valideren** op de opdrachtbalk is echter handig, omdat hiermee problemen kunnen worden geïdentificeerd die u moet oplossen voordat u een publicatiegroep plant om live te gaan.

## <a name="schedule-a-publish-group-to-go-live"></a>Een publicatiegroep plannen om live te gaan

Ga als volgt te werk om een publicatiegroep te plannen om live te gaan op uw site.

1. Selecteer **Publicatiegroepen** in het navigatievenster aan de linkerkant.
1. Selecteer de publicatiegroep die u wilt plannen onder **Publicatiegroepen**.
1. Selecteer **Planning bewerken** op de opdrachtbalk. Het dialoogvenster **Planning bewerken** wordt weergegeven.
1. Selecteer de datum en tijd waarop uw publicatiegroep live moet gaan en selecteer vervolgens **OK**.

Als u de planning van een publicatiegroep ongedaan wilt maken, voert u dezelfde stappen uit, maar selecteert **Planning van publicatiegroep ongedaan maken** in het dialoogvenster **Planning bewerken**.

> [!NOTE]
> Voor zeer grote publicatiegroepen kan het op het geplande tijdstip een minuut of twee duren voordat ze zijn gepubliceerd. Houd er rekening mee dat een publicatieactie niet onmiddellijk wordt uitgevoerd en dat kleinere publicatiegroepen sneller worden gepubliceerd.

## <a name="publish-groups-faq"></a>Veelgestelde vragen over publicatiegroepen

**Hoeveel items kan een publicatiegroep bevatten?**

Momenteel bestaat er een limiet van 2000 items per publicatiegroep. Houd er rekening mee dat het voor zeer grote publicatiegroepen op het geplande tijdstip enkele minuten kan duren voordat ze zijn gepubliceerd.

**Zijn publicatiegroepen zoiets als codevertakkingen in de terminologie voor softwareontwikkeling?**

Ja en nee. Publicatiegroepen kunnen worden gezien als gevorkte versies van uw site. Op die manier fungeren ze als vertakkingen. Er is echter geen concept van een samenvoeging op het niveau van afzonderlijke items. Het artikel dat als laatste wordt gepubliceerd, overschrijft alleen wat eerder bestond en de meest recente publicatieactie vervangt altijd eerdere publicatieacties.

**Kan ik twee publicatiegroepen plannen om op hetzelfde moment live te gaan?**

Nr. Voor betere prestaties en om conflicten te voorkomen, kunt u publicatiegroepen niet binnen vijf minuten van elkaar plannen.

**Kan ik publicatiegroepen gebruiken voor het plannen van back-office-items voor meerdere kanalen, zoals kortingen en productupdates?**

De functie voor publicatie groepen ondersteunt momenteel alleen website-inhoud. Microsoft is zich er echter van bewust dat de integratie met merchandisingscenario's voor back-offices waardevol kan zijn voor de coördinatie en automatisering van lanceringen van campagnes via meerdere kanalen.

## <a name="additional-resources"></a>Aanvullende resources

[Manieren om inhoud toe te voegen](add-manage-content.md)

[Woordenlijst voor paginamodellen](page-elements-overview.md)

[Statussen en levenscyclus van document](document-states-overview.md)

[Het delen van inhoud door meerdere kanalen inschakelen en gebruiken](cross-channel-sharing.md)

[Werken met modules](work-with-modules.md)

[Werken met fragmenten](work-with-fragments.md)

[Overzicht sjablonen en indelingen](templates-layouts-overview.md)

[Sitenavigatie aanpassen](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]