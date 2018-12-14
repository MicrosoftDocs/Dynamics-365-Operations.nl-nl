---
title: Functies maken, goedkeuren en boeken in Attract
description: Dit onderwerp beschrijft de elementen van een functie in Attract. Ook wordt uitgelegd hoe u een functie maakt.
author: josaw
manager: AnnBe
ms.date: 10/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: 
ms.author: josaw
ms.search.validFrom: 2018-10-24
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: 2fc6bf25d303d7d8de8002a923a080b90dcfbeab
ms.openlocfilehash: af945042c150fff1a95cdb046f2a712cb2c2c061
ms.contentlocale: nl-nl
ms.lasthandoff: 10/24/2018

---

# <a name="create-approve-and-post-jobs-in-attract"></a>Functies maken, goedkeuren en boeken in Attract

[!include [banner](includes/banner.md)]

Dit onderwerp beschrijft de elementen van een functie in Microsoft Dynamics 365 for Talent: Attract. Ook wordt uitgelegd hoe u een functie maakt.

## <a name="job-creation"></a>Functies maken

Beheerders, wervers en aanstellend managers kunnen functies maken. Wanneer u een functie maakt, wordt u gevraagd uw rol in het proces te selecteren: aanstellend manager of werver. Nadat u een rol hebt geselecteerd, wordt u gevraagd een processjabloon te selecteren. Als u **Overslaan** selecteert, wordt de standaardsjabloon gebruikt. Zie voor meer informatie over processjablonen [Een processjabloon maken in Attract](./process-templates-attract.md).

Een functie in Attract heeft functiedetails, een wervingsteam, een aanstellingsproces, vacatures en analyses.

## <a name="job-details"></a>Functiedetails

Het tabblad **Functiedetails** bevat details over de verantwoordelijkheden en kenmerken van de functie. De velden voor de functie, de functieomschrijving en de locatie van de functie zijn vereist. De overige velden zijn optioneel.

Standaard is het veld **Aantal personen** ingesteld op **1**. U kunt de waarde echter wijzigen. Wanneer een aanbieding is voorbereid voor een functie, wordt de waarde van het veld **Aantal personen** verlaagd.

Als positiebeheer is ingeschakeld in het beheercentrum, is de zoekopdracht **Posities bijwerken** beschikbaar. Deze zoekactie leest de entiteit JobPosition in de Common Data Service voor Apps en retourneert een lijst met posities die kunnen worden geselecteerd voor de functie. Als het aantal posities dat u selecteert, het aantal vacatures overschrijdt, ontvangt u een waarschuwing. U krijgt ook een waarschuwing als een positie wordt gebruikt in meerdere functies.

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

Nadat een functie is geactiveerd, kan deze worden geplaatst. Alleen wervers en beheerders kunnen functies plaatsen. De functie kan worden geplaatst op Talent Loopbanen (een Microsoft Dynamics 365 for Talent-carrièresite) of LinkedIn. Het Attract-team werkt voortdurend aan partnerschappen met functiebordproviders. Deze lijst wordt daarom in de loop van de tijd uitgebreid.

Zie voor meer informatie over vacatures [Carrièresitefunctionaliteit in Attract](./career-site.md).

> [!NOTE]
> De functionaliteit voor personeelsadvertenties is alleen beschikbaar met de Uitgebreide invoegtoepassing voor aanstellingen voor Attract.

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

Goedkeuringen kunnen worden verzonden naar alle Microsoft Azure Active Directory (Azure AD)-gebruikers in het bedrijf. De goedkeuringen worden parallel verzonden naar alle personen die zijn vermeld als fiatteurs. Nadat een functie is goedgekeurd, kan deze worden geactiveerd.

De mensen die worden vermeld als fiatteurs, ontvangen een melding in Attract om hen te informeren dat er een item moet worden goedgekeurd. Er wordt ook een goedkeuringsitem weergegeven in de sectie **Aan u toegewezen** op het dashboard. Nadat iemand een functie accepteert of goedkeurt, ontvangt het aanstellend team een melding. Ten slotte ontvangt het aanstellend team een melding wanneer de functie is goedgekeurd.

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
