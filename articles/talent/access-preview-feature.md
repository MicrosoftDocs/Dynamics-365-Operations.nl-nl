---
title: Functies beheren
description: In dit onderwerp wordt beschreven hoe een beheerder de voorbeeldfuncties in Microsoft Dynamics 365 Talent kan inschakelen en krijgt u een overzicht van de functies die momenteel zijn ingeschakeld voor het voorbeeld.
author: tracykeya
manager: AnnBe
ms.date: 05/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: trkeya
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2019 update
ms.openlocfilehash: 9f1fb4b929660bbe9018fb98169b3cfddcaec547
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/25/2019
ms.locfileid: "2833295"
---
# <a name="manage-features"></a>Functies beheren

[!include [banner](includes/banner.md)]

Als onderdeel van onze doorlopende implementatie van HCM-mogelijkheden (human capital management) voor Microsoft Dynamics 365 Talent willen we klanten zo snel mogelijk laten kennismaken met nieuwe functies. Beheerders kunnen voorbeeldfuncties in hun omgevingen zien en gebruiken. Deze functies zijn bijna gereed voor algemene beschikbaarheid en zijn uitgebreid getest. Het enige wat we nog willen doen is een definitieve ronde van feedback van klanten en validatie voordat we de functies algemeen vrijgeven.

In dit onderwerp wordt beschreven hoe u voorbeeldfuncties kunt inschakelen en krijgt u een overzicht van de functies die momenteel beschikbaar zijn als voorbeeld. Deze lijst wordt bijgewerkt wanneer functies algemeen beschikbaar worden en van nieuwe functies kan een voorbeeld worden bekeken. U ontvangt geen melding wanneer van nieuwe functies een voorbeeld kan worden bekeken. Gebruikers zien de functies gewoon verschijnen. Zie [Nieuwe of gewijzigde functies in Dynamics 365 Talent](./whats-new.md) en [Dynamics 365- en Power Platform-releaseopmerkingen](https://docs.microsoft.com/business-applications-release-notes) voor meer informatie over nieuwe functies in Talent.

## <a name="enable-or-disable-preview-features"></a>Voorbeeldfuncties in- of uitschakelen

Als u toegang tot voorbeeldfuncties wilt hebben, moet u deze eerst in uw omgeving inschakelen. Het in- of uitschakelen van voorbeeldfuncties is omgevingsspecifiek.

> [!IMPORTANT]
> Als u de instelling **Voorbeeldfuncties** inschakelt, kunt u voorbeeldfuncties inschakelen voor alle gebruikers in uw organisatie die zich in die omgeving bevinden. Als u de instelling uitschakelt, schakelt u de voorbeeldfuncties uit en zijn ze niet toegankelijk voor uw gebruikers. Voorbeeldfuncties hebben beperkte ondersteuning in Talent. Ze hebben mogelijk minder privacy- en beveiligingsmaatregelen en zijn niet opgenomen in de serviceovereenkomst voor Talent. U moet de voorbeeldfuncties niet gebruiken voor de verwerking van persoonsgegevens (dat wil zeggen informatie die uw identiteit aangeeft) of andere gegevens die onderworpen zijn aan wettelijke of bestuursrechtelijke conformiteitsvereisten.

### <a name="attract"></a>Attract

1. Meld u aan bij Microsoft Dynamics 365 Talent: Attract.
2. Selecteer in het menu **Instellen** (het tandwielsymbool) in de rechterbovenhoek de optie **Beheercentrum**.
3. Selecteer op het tabblad **Functiebeheer** de optie naast **Voorbeeldfuncties** zodat deze blauw wordt en wordt ingesteld op **Aan**.

    ![Voorbeeldfuncties inschakelen in Attract](./media/attract-enable-preview-features.png)

4. Selecteer of annuleer de selectie van afzonderlijke voorbeeldfuncties. Als u niets doet, worden alle beschikbare voorbeeldfuncties ingeschakeld.
5. Vernieuw uw browser om de nieuwe functies te zien. Alle gebruikers die al zijn geregistreerd, zien de functies de volgende keer dat ze zich aanmelden. Ze kunnen ook hun browser vernieuwen om de functies direct te zien.

> [!NOTE]
> Voor sommige voorbeeldfuncties is mogelijk extra configuratie vereist. Volg de koppelingen naast de voorbeeldfuncties om de instellingen voor de functies te voltooien.

### <a name="core-hr"></a>Core HR

1. Aanmelden bij Talent
2. Selecteer **Systeembeheer**en selecteer vervolgens het tabblad **Koppelingen**.
3. Selecteer op de pagina **Systeembeheer** onder **Instellen** de optie **Systeemparameters**.
4. Selecteer op de pagina **Systeemparameters** het tabblad **Voorbeeldfuncties**.
5. Stel de optie **Voorbeeldmodus voor alle gebruikers inschakelen** in op **Ja** als u voorbeeldfuncties beschikbaar wilt maken.

    ![Voorbeeldfuncties inschakelen in Core HR](./media/corehr-enable-preview-features.png)

> [!NOTE]
> Om voorbeeldfuncties uit te schakelen, gebruikt u dezelfde stappen, maar stelt u de optie **Voorbeeldmodus voor alle gebruikers inschakelen** in op **Nee**. Wanneer u voorbeeldfuncties uitschakelt, zijn ze niet meer toegankelijk voor gebruikers en kunnen er fouten optreden in processen die gekoppeld zijn aan de functies.

### <a name="onboard"></a>Onboarden

Er zijn momenteel geen voorbeeldfuncties beschikbaar voor Microsoft Dynamics 365 Talent: Onboard.

## <a name="features-that-are-currently-in-preview"></a>Functies waarvan momenteel een voorbeeld kan worden bekeken

### <a name="attract"></a>Attract

- [Aanbeveling voor kandidaat](./intelligent-recommendations.md#candidate-recommendations): als er meer dan tien kandidaten met cv's of volledige profielen zijn, worden de kandidaten die het best overeenkomen met de vereisten van de functie, weergegeven in de sectie **Te overwegen sollicitanten** op de pagina voor die functie.
- [Aanbeveling voor functie](./intelligent-recommendations.md#job-recommendations): Attract biedt functieaanbevelingen aan prospects als meer dan tien functies zijn geplaatst op uw vacaturesite.
- [Broadbean-integratie](./posting-jobs-external.md#post-jobs-to-broadbean): u kunt functies vanuit Attract plaatsen op Broadbean, een externe vacaturesite. Nadat u deze voorbeeldfunctie hebt ingeschakeld, moet u de instellingen voltooien door uw gebruikersnaam, client-id en coderingstoken voor Broadbean in te voeren.
- [Analyses](./analytic-reports.md): aanstellingsteams kunnen belangrijke metrische gegevens voor één functie en samengevoegde meetgegevens voor alle functies weergeven in de Analysehub.
- [EEO](./activities-attract.md): met nieuwe activiteitstypen kunt u een vooraf gedefinieerd formulier voor het verzamelen van EEO- (Equal Employment Opportunity) en OFCCP-gegevens (Office of Federal Contract Compliance Program) van de kandidaat gebruiken. Het vooraf gedefinieerde formulier kan niet worden bewerkt.
- [Prospectaanbeveling](./intelligent-recommendations.md#prospect-recommendations): in Attract worden eerdere sollicitanten en huidige kandidaten beoordeeld om een lijst met prospects samen te stellen die in aanmerking komen voor uw functie.
- [Relevante zoekopdracht](./attract-talent-pools.md#search-and-view-candidate-profiles): u kunt nu in uw gehele database met kandidaten zoeken naar bepaalde vaardigheden, namen of opleidingsachtergrond. Attract zoekt in het gehele profiel en markeert alle gevonden overeenkomsten. Attract zoekt ook in alle documenten die beschikbaar zijn voor een kandidaat en rangschikt de zoekresultaten op intelligente wijze.
- [Doelgroep voor activiteit](./whats-new-talent-march-20.md#setting-the-audience-on-activities): u kunt de doelgroep voor activiteiten (zoals sollicitatiegesprek, planning of feedback) instellen op **Alle kandidaten**, **Interne kandidaten** of **Externe kandidaten**. U kunt aangepaste activiteiten, zoals YouTube-video's, webinhoud en Microsoft Forms, leveren aan alle kandidaten, interne kandidaten, externe kandidaten of het aanstellingsteam.
- [Solliciteren met LinkedIn](./career-site.md#enable-applying-for-jobs-with-linkedin-profiles): u kunt een optie op uw Attract-vacaturesite instellen waarmee kandidaten kunnen solliciteren via LinkedIn. Deze functie stroomlijnt het sollicitatieproces voor uw kandidaten omdat ze hun LinkedIn-profiel kunnen gebruiken om hun sollicitaties op uw vacaturesite automatisch in te vullen.
- [Brontracering](./source-tracking.md): in Attract wordt automatisch de bron van sollicitaties van kandidaten bijgehouden. Zo beschikt u over waardevolle informatie waarmee u uw inspanningen met betrekking tot personeelswerving beter kunt inzetten. U kunt ook een sollicitatiebron selecteren als u een kandidaat aan een functie of talentenpool toevoegt.
- [Tweede plaats](./whats-new-talent-march-20.md#designate-silver-medalists-to-assign-high-value-applicants-for-future-positions): als kandidaten zeer geschikt zijn voor uw organisatie, maar u nu geen positie kunt aanbieden, kunt u deze kandidaten de status Tweede plaats geven. Wanneer dan een vergelijkbare positie beschikbaar komt, hebt u met deze functie minder tijd nodig om deze positie in te vullen.

### <a name="core-hr"></a>Core HR

- [Validatie van positiehiërarchiegegevens](./whats-new-talent-may-13-2019.md#new-page-to-validate-position-hierarchy-data): u kunt de hiërarchie van leidinggevenden valideren voor alle kringverwijzingen die per ongeluk zijn geïmporteerd.
- [Redencodes opgeven voor verloftypen](./whats-new-talent-may-13-2019.md#specify-reason-codes-on-leave-types): u kunt redencodes opgeven voor verloftypen.
- [Redencodes vereisen voor verlofaanvragen](./whats-new-talent-may-13-2019.md#require-reason-codes-for-specific-leave-types-on-time-off-requests): u kunt niet alleen redencodes voor verloftypen opgeven, maar ook redencodes voor verlofaanvragen vereisen.
- [Een lijst met verlof- en afwezigheidstransacties verschaffen voor HR](./whats-new-talent-may-13-2019.md#provide-a-leave-and-absence-transaction-list-for-hr): u kunt een lijst met verlof- en verzuimtransacties weergeven om inzicht te krijgen in verlofsaldi.

### <a name="onboard"></a>Onboarden

Er zijn momenteel geen voorbeeldfuncties beschikbaar voor Onboard.

## <a name="feedback"></a>Feedback

Wij horen graag over uw ervaringen met deze voorbeeldfuncties. We raden u aan uw feedback regelmatig op de volgende websites te plaatsen wanneer u deze of andere functies gebruikt:

- [Community](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) : deze site is een goede bron waar gebruikers gebruikstoepassingen kunnen bespreken, vragen kunnen stellen en hulp van de community kunnen krijgen.
- Laat ons weten welke functies u wilt zien in het product en ook eventuele wijzigingen die volgens u in de bestaande functies moeten worden aangebracht. Op de volgende websites kunt u uw suggesties voor productideeën kwijt:

    - [Ideeën voor Attract](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [Ideeën voor Core HR](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources)
    - [Ideeën voor Onboard](https://powerusers.microsoft.com/t5/Ideas-for-Onboard/idb-p/Onboard)

Vermeld geen persoonlijke gegevens (gegevens die uw identiteit vrijgeven) als u feedback of een productbeoordeling indient. Verzamelde gegevens worden mogelijk verder geanalyseerd en worden niet gebruikt om verzoeken te beantwoorden krachtens van toepassing zijnde privacywetgeving. Persoonlijke gegevens die afzonderlijk voor deze programma's worden verzameld, zijn onderworpen aan de [privacyverklaring van Microsoft](https://privacy.microsoft.com/privacystatement).

> [!TIP]
> Maak een bladwijzer van dit onderwerp en controleer het regelmatig om op de hoogte te blijven van nieuwe voorbeeldfuncties die door ons worden uitgegeven.

## <a name="see-also"></a>Zie ook

- [Talent-apps proberen of kopen](https://dynamics.microsoft.com/talent/overview/)
- [Nieuwe of gewijzigde functies in Dynamics 365 Talent](./whats-new.md)
- [Vrijgaveplannen](https://docs.microsoft.com/business-applications-release-notes/index)
- [Ondersteuning voor Microsoft Dynamics 365 Talent](./talent-support.md)
