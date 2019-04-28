---
title: Functies maken, goedkeuren en boeken in Attract
description: Dit onderwerp beschrijft de elementen van een functie in Attract. Ook wordt uitgelegd hoe u een functie maakt.
author: hasrivas
manager: AnnBe
ms.date: 03/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: hasrivas
ms.search.validFrom: 2018-10-24
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 1e76572c1a843fe7abd515333d5b7cb03b91eb11
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/12/2019
ms.locfileid: "969344"
---
# <a name="create-approve-and-post-jobs-in-attract"></a>Functies maken, goedkeuren en boeken in Attract

[!include [banner](includes/banner.md)]

In dit onderwerp worden de elementen van een functie in Microsoft Dynamics 365 for Talent: Attract beschreven. Ook wordt uitgelegd hoe u een functie maakt.

## <a name="job-creation"></a>Taak maken

Beheerders, wervers en aanstellend managers kunnen functies maken. Wanneer u een functie maakt, wordt u gevraagd uw rol in het proces te selecteren: aanstellend manager of werver. Nadat u een rol hebt geselecteerd, wordt u gevraagd een processjabloon te selecteren. Als u **Overslaan** selecteert, wordt de standaardsjabloon gebruikt. Zie voor meer informatie over processjablonen [Een processjabloon maken in Attract](./process-templates-attract.md).

Een functie in Attract heeft functiedetails, een wervingsteam, een aanstellingsproces, vacatures en analyses.

## <a name="job-details"></a>Functiedetails

Het tabblad **Functiedetails** bevat details over de verantwoordelijkheden en kenmerken van de functie. De velden voor de functie, de functieomschrijving en de locatie van de functie zijn vereist. De overige velden zijn optioneel.

Standaard is het veld **Aantal personen** ingesteld op **1**. U kunt de waarde echter wijzigen. Wanneer een aanbieding is voorbereid voor een functie, wordt de waarde van het veld **Aantal personen** verlaagd.

Als positiebeheer is ingeschakeld in het beheercentrum, is de zoekopdracht **Posities bijwerken** beschikbaar. Met deze zoekopdracht wordt de entiteit JobPosition in Common Data Service gelezen en wordt een lijst geretourneerd met posities die kunnen worden geselecteerd voor de functie. Als het aantal posities dat u selecteert, het aantal vacatures overschrijdt, ontvangt u een waarschuwing. U krijgt ook een waarschuwing als een positie wordt gebruikt in meerdere functies.

> [!NOTE]
> Positiebeheer is beschikbaar met de Uitgebreide invoegtoepassing voor aanstellingen.

Afhankelijk van de instellingen in de aanbiedingsactiviteit van het aanstellingsproces kan een positienummer tweemaal in een aanbieding worden gebruikt. Zie [Aanstellingsproces](./activities-attract.md) voor meer informatie.

Attract bevat een standaardset met **vaardigheden**. Deze vaardigheden worden als suggesties weergegeven terwijl u typt. U kunt meer vaardigheden toevoegen door de nieuwe vaardigheidstekst in te voeren en vervolgens op Enter te drukken.

Attract bevat een standaardset met **functies**. U kunt maximaal nog drie taakfuncties toevoegen door de nieuwe taakfunctie in te voeren in het veld en vervolgens op Enter te drukken.

Attract bevat de standaardset **Bedrijfstak**. U kunt maximaal nog drie bedrijfstakken toevoegen door de nieuwe bedrijfstak in te voeren in het veld en vervolgens op Enter te drukken.

## <a name="hiring-team"></a>Wervingsteam

Het tabblad **Wervingsteam** bevat de lijst met personen die bij de functie zijn betrokken. Wanneer gebruikers worden toegevoegd aan een wervingsteam, moet aan hen een rol worden toegewezen in het wervingsteam. De rol bepaalt de gegevens waartoe de gebruikers toegang hebben en de meldingen die ze ontvangen. De rollen die kunnen worden geselecteerd, zijn **Werver**, **Aanstellend manager**, **Gemachtigde** en **Interviewer**. Zie voor meer informatie over rolbevoegdheden het document 'Rollenbeheer'. Wervers en aanstellend managers kunnen een of meer gemachtigden aanwijzen die namens hen werken. Zie voor meer informatie over gemachtigden [Beveiliging en rollenbeheer in Attract](./security-attract.md).

Het wervingsteam kan worden bijgewerkt nadat de functie is geactiveerd.

## <a name="process"></a>Proces

Standaardgegevens over het aanstellingsproces zijn gebaseerd op de processjabloon die is geselecteerd toen de functie werd gemaakt. Als een specifieke sjabloon op dat moment niet was geselecteerd, wordt de standaardsjabloon gebruikt. Wanneer u het aanstellingsproces definieert, kunt u verschillende fasen toevoegen of verwijderen, met uitzondering van de fasen Prospect, Sollicitatie en Aanbieding. Hoewel de fase Prospect niet kan worden verwijderd, kan deze wel worden uitgeschakeld. U kunt in elke fase een of meer vooraf gedefinieerde activiteiten toevoegen of verwijderen.

Zie voor meer informatie over activiteiten die kunnen worden toegevoegd aan het aanstellingsproces, [Aanstellingsactiviteiten in Attract](./activities-attract.md).

> [!NOTE]
> Het aanstellingsproces kan niet worden bijgewerkt nadat een functie is geactiveerd.

## <a name="postings"></a>Boekingen

Nadat een functie is geactiveerd, kan deze worden geplaatst. Alleen wervers en beheerders kunnen functies plaatsen. De functie kan worden geplaatst op Talent Loopbanen (een Microsoft Dynamics 365 for Talent-vacaturesite) of LinkedIn. Het Attract-team werkt voortdurend aan partnerschappen met functiebordproviders. Deze lijst wordt in de loop van de tijd uitgebreid. Wanneer een functie als alleen intern wordt gepubliceerd, moeten kandidaten een AAD-account hebben om de functie te bekijken en erop te solliciteren. Als de functie als openbaar wordt weergegeven, kunnen de kandidaten functies bekijken en erop solliciteren met alle verificatieopties. 

Zie voor meer informatie over vacatures [Carrièresitefunctionaliteit in Attract](career-site.md).

> [!NOTE]
> De functionaliteit voor personeelsadvertenties is alleen beschikbaar met de Uitgebreide invoegtoepassing voor aanstellingen voor Attract.

### <a name="posting-jobs-to-linkedin"></a>Vacatures publiceren naar LinkedIn 

Voordat u een vacature vanuit Attract naar LinkedIn publiceert, moet de beheerder de bedrijfs-ID en de bedrijfsnaam van LinkedIn toevoegen in **Beheerinstellingen**. De bedrijfs-ID van LinkedIn is vereist om ervoor te zorgen dat uw vacatures die zijn gepubliceerd vanuit Attract, aan de juiste bedrijfspagina worden toegewezen.

Uw bedrijfs-ID voor LinkedIn is een reeks cijfers die een unieke identificatie vormen van uw bedrijf in LinkedIn. Ga voor meer informatie over hoe u de bedrijfs-ID voor LinkedIn vindt naar de [LinkedIn-site](https://aka.ms/findID).

Als u uw LinkedIn-bedrijf wilt bijwerken, selecteert u **Beheercentrum**  in het menu **Instellingen**  (het tandwielsymbool) en selecteert u vervolgens het tabblad **LinkedIn-integratie** . Voer onder de sectie **Verbinding maken met LinkedIn** uw bedrijfsnaam en bedrijfs-ID voor LinkedIn in en sla vervolgens de instellingen op.

> [!NOTE]
> U moet met vier belangrijke dingen rekening houden met betrekking tot het publiceren van vacatures naar LinkedIn.
> 1. Vacatures op LinkedIn worden op LinkedIn gepubliceerd als 'limited listings'. Dergelijke vacatures kunnen niet worden gepromoot op de LinkedIn-site. Als u vacatures met limited listing gepubliceerd op LinkedIn vanuit Attract wilt promoten, moet u ervoor zorgen dat de functie 'Job Wrapping' in LinkedIn wordt ingeschakeld. Raadpleeg de onderstaande koppelingen en neem contact op met de ondersteuning van LinkedIn voor meer informatie.
>
>    [Limited Listings vs Premium Job Slots for Job Wrapping](https://www.linkedin.com/help/recruiter/answer/79049/limited-listings-vs-premium-job-slots-for-job-wrapping)
>
>    [Job Wrapping FAQ](https://www.linkedin.com/help/recruiter/answer/79050/job-wrapping-frequently-asked-questions)
>
> 1. Bij het publiceren van vacatures op LinkedIn geeft Attract de naam van de Microsoft 365-organisatie voor de vacature door. LinkedIn koppelt de vacatures aan een bedrijf aan de LinkedIn-site op basis van de naam van de organisatie die wordt doorgegeven. Als uw vacature wordt weergegeven niet voor het juiste bedrijf wordt weergegeven op LinkedIn, moet u controleren of de naam van uw Microsoft 365-organisatie overeenkomt met de naam van het bedrijf op LinkedIn.  
>
>    [Het adres en de technische contactpersoon van uw organisatie en meer wijzigen](https://docs.microsoft.com/en-us/office365/admin/manage/change-address-contact-and-more)
>
>    Als u problemen ondervindt na deze stap, neemt u contact op met de ondersteuning van LinkedIn. 
> 
> 1. Vacatures die zijn gepubliceerd naar LinkedIn, worden weergegeven op de live LinkedIn-site. Er is geen testomgeving voor het publiceren van vacatures naar LinkedIn. 
>
> 1. Het kan maximaal 24 uur duren voordat vacatures gepubliceerd op LinkedIn zichtbaar zijn voor kandidaten vanuit LinkedIn, vanwege het huidige proces voor het batchgewijs publiceren van vacatures in LinkedIn.


## <a name="activate"></a>Activeren

Nadat een functie is geactiveerd, kan deze worden geboekt en kunnen er prospects en sollicitanten aan worden toegevoegd. De optie om prospects aan een functie toe te voegen wordt ingesteld in de activiteit Prospect in het aanstellingsproces.

> [!NOTE]
> Het aanstellingsproces kan niet worden bijgewerkt nadat een functie is geactiveerd.

## <a name="prospects-and-applicants"></a>Prospects en sollicitanten

De optie om prospects aan een functie toe te voegen wordt ingesteld in de [activiteit Prospect](./activities-attract.md#prospect-activity) in het aanstellingsproces. Deze optie moet worden ingesteld voordat u de functie activeert. Nadat een functie is geactiveerd, kunnen er prospects en sollicitanten aan worden toegevoegd.

## <a name="approvals"></a>Goedkeuringen

Attract-functies kunnen worden ingediend voor goedkeuring. Niet alle functies hoeven te worden goedgekeurd. De vereiste wordt ingesteld op het sjabloonniveau. Goedkeuringen zijn standaard uitgeschakeld in de sjabloon. Als u goedkeuringen wilt instellen, gaat u naar een processjabloon en stelt u het veld **Goedkeuring** in op Standaard. Selecteer vervolgens deze sjabloon wanneer u de functie maakt.

Nadat een functie is opgeslagen, kan deze ter goedkeuring worden ingediend. De volgende tabel bevat de mogelijke statuswaarden van een document dat goedkeuringen gebruikt.

| Status   | Provincie                                                               |
|----------|---------------------------------------------------------------------|
| Concept    | De functie is opgeslagen, maar is nog niet ingediend bij een werkstroom. |
| In behandeling  | De functie is ingediend bij fiatteurs.                            |
| Goedgekeurd | De functie is goedgekeurd, maar nog niet geactiveerd.            |
| Afgewezen | De functie is geweigerd en kan niet worden geactiveerd.               |
| Actief   | De functie is goedgekeurd en geactiveerd.                            |

In de functielijst kunt u filteren op de status van de functie.

Goedkeuringen kunnen worden verzonden naar elke Microsoft Azure Active Directory-gebruiker (Azure AD) in het bedrijf. De goedkeuringen worden parallel verzonden naar alle personen die zijn vermeld als fiatteurs. Alle fiatteurs moeten de functie goedkeuren voordat er verder mee kan worden gegaan. Als één fiatteur de functie afwijst, wordt de functie weergegeven met de status **Afgewezen**. Nadat een functie is goedgekeurd, kan deze worden geactiveerd.

Als een gebruiker de functie bewerkt nadat deze is goedgekeurd, maar niet geactiveerd, wordt de functiestatus teruggezet op **Concept** en moet de functie opnieuw ter goedkeuring worden ingediend. Nadat een goedgekeurde functie is geactiveerd, kunt u deze niet bewerken.

De personen die worden vermeld als fiatteurs, ontvangen een melding in Attract en een e-mail om hen te informeren dat er een item is dat moet worden goedgekeurd.  In de e-mail kunnen de fiatteurs op de koppeling klikken om de functie te openen, de details te bekijken en de functie goed te keuren of af te wijzen. Nadat de status van de functie is ingesteld op **Goedgekeurd** of **Afgewezen**, wordt de indiener op de hoogte gebracht in Attract en ontvangt deze persoon een e-mailbericht. De fiatteurs ontvangen ook een e-mail ter herinnering als ze niet op de aanvraag tot goedkeuring hebben geantwoord binnen 24 uur.

> [!NOTE]
> U kunt aangepaste e-mailsjablonen voor goedkeuringse-mails maken. Zie voor meer informatie [E-mailsjablonen maken en beheren](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/email-templates).

## <a name="create-a-job"></a>Een taak maken

Volg deze stappen om een functie te maken.

1. Ga naar **Functies**.
2. Selecteer **Nieuw**.
3. Voer in het veld **Functie** de functie in. Voer in het veld **Rol** uw rol in.
4. Selecteer in het veld **Sjabloon** een sjabloon. Of selecteer **Overslaan**. Als u **Overslaan** selecteert, wordt de sjabloon die is gemarkeerd als de standaardsjabloon, gebruikt.

    Als het document een goedkeuringsproces doorlopen moet, selecteert u een sjabloon waarbij het veld **Goedkeuringsproces** is ingesteld op **Standaard**.

5. Voer op het tabblad **Details** de details van de functie in. De velden **Titel**, **Functieomschrijving** en **Locatie** zijn vereist.
6. Selecteer **Opslaan**.
7. Voeg op het tabblad **Wervingsteam** een aanstellend manager, werver of interviewer in.
8. Selecteer **Opslaan**.
9. Voeg op het tabblad **Proces** fasen toe of verwijder ze indien nodig:

    - Als u een fase wilt toevoegen, selecteert u **+ Nieuwe fase**.
    - Als u een fase wilt verwijderen, plaatst u de aanwijzer boven de fase die u wilt verwijderen en selecteert u vervolgens de prullenbakknop die wordt weergegeven.

        > [!NOTE]
        > De fasen Prospect, Sollicitatie en Aanbieding kunnen niet worden verwijderd.

10. Voeg indien nodig activiteiten toe of verwijder ze:

    - Als u een activiteit wilt toevoegen, sleept u deze van de lijst aan de rechterkant naar de gewenste fase. Of dubbelklik op de activiteit en selecteer vervolgens de fase waaraan u deze wilt toevoegen.
    - Als u een activiteit wilt verwijderen, vouwt u de activiteit uit en selecteert u de prullenbakknop in de koptekst van de activiteit.

11. Selecteer **Opslaan**.
12. Als u hebt gekozen een goedkeuringsproces te gebruiken, volgt u deze stappen:

    1. Selecteer **+ Goedkeurder toevoegen** en voer een gebruiker in die een Azure AD-account heeft. U kunt meerdere fiatteurs toevoegen.
    2. Selecteer **Verzenden naar fiatteurs**.

    Het veld **Taakstatus** van de functie wordt ingesteld op **In behandeling**. Als de waarde van het veld **Taakstatus** verandert in **Goedgekeurd**, kan de functie worden geactiveerd.

13. Als u de functie wilt activeren, selecteert u **Activeren**.
14. Als u de functie wilt plaatsen, gaat u naar **Boekingen** en selecteert u vervolgens **Nu plaatsen** onder Talent Loopbanen of LinkedIn.
