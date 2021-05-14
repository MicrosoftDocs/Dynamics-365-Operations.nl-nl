---
title: Niet-conformeringen maken en verwerken
description: In dit onderwerp wordt het beheer van niet-conformeringen, op basis van een bestaande kwaliteitsorder, beschreven.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 06a56a694f7a80d65cb46d08744e78d8361cee3b
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956201"
---
# <a name="create-and-process-nonconformances"></a>Niet-conformeringen maken en verwerken

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt het beheer van niet-conformeringen, op basis van een bestaande kwaliteitsorder, beschreven. Het beheer van niet-conformeringen wordt meestal uitgevoerd door een kwaliteitbewakingsmedewerker. Een voorwaarde hiervoor is dat een kwaliteitsorder beschikbaar is. (Zie voor informatie over het maken van een kwaliteitsorder [De kwaliteit van goederen inspecteren](inspect-quality-goods.md).)

Voordat een gebruiker de goedkeuring van een niet-conformering kan verwerken, moet een medewerker aan deze gebruiker zijn toegewezen in het veld **Persoon** op de pagina **Gebruikers**. Voordat de gebruiker de documentnotities kan gebruiken, moet bovendien de optie **Documentverwerking inschakelen** zijn ingesteld op *Ja* in diens gebruikersopties.

## <a name="create-a-nonconformance"></a>Een non-conformiteit maken

Volg deze stappen om een niet-conformering te maken.

1. Ga naar **Voorraadbeheer \> Periodieke taken \> Kwaliteitsbeheer \> Niet-conformeringen**.
1. Selecteer **Nieuw** in het actievenster.
1. Selecteer in het dialoogvenster **Niet-conformering maken** in het veld **Probleemtype** het type probleem dat is gevonden tijdens het inspectieproces.
1. Selecteer **OK**.

## <a name="approve-or-reject-a-nonconformance"></a>Een niet-conformering goedkeuren of afwijzen

Om een niet-conformering goed te keuren of af te wijzen, volgt u deze stappen:

1. Ga naar **Voorraadbeheer \> Periodieke taken \> Kwaliteitsbeheer \> Niet-conformeringen**.
1. Zoek en selecteer in de lijst de niet-conformering die u wilt bijwerken.

    > [!NOTE]
    > U kunt alleen een correctie toevoegen aan niet-conformeringen die zijn goedgekeurd.

1. Selecteer in het actievenster de optie **Functies \> Niet-conformering goedkeuren** om de niet-conformering goed te keuren of **Functies \> Niet-conformering weigeren** om deze af te wijzen. U kunt goedgekeurde niet-conformeringen aan [gerelateerde bewerkingen](../quality-operations.md) koppelen. Op deze manier kunt u werk registreren dat wordt uitgevoerd als onderdeel van de niet-conformeringsverwerking en de verwerking van correctieafhandeling.
1. U wordt gevraagd om de selectie te bevestigen. Selecteer **Ja** om door te gaan.

## <a name="add-operations-and-other-details-to-nonconformances"></a>Bewerkingen en andere details toevoegen aan niet-conformeringen

Nadat u een niet-conformering hebt gemaakt, kunt u gerelateerde bewerkingen gaan toevoegen en extra informatie over die bewerkingen opgeven. U kunt alleen gerelateerde bewerkingen toevoegen aan niet-conformeringen die zijn goedgekeurd.

Naast de basisgegevens kunt u de volgende details toevoegen aan een bewerking:

- **Artikelen**: U kunt een lijst met artikelen maken die worden verbruikt bij het uitvoeren van de correctie. De artikelen kunnen bijvoorbeeld producten zijn die vereist zijn om apparatuur te repareren of ingrediënten die nodig zijn om een eindproduct bij te werken.
- **Kwaliteitstoeslagen**: U kunt een lijst met toeslagen maken die worden gemaakt of naar externe bronnen worden gefactureerd.
- **Urenstaat**: U kunt een logboek maken waarind de tijd wordt vastgelegd die elke werknemer besteedt aan de bewerking.

De overige instellingen zijn optioneel. De kosten voor elk artikel, kwaliteitstoeslagen en de urenstaten worden opgeteld en weergegeven in de bewerking. U kunt het veld **Kosten** van de bewerking niet direct bewerken.

### <a name="create-an-operation-for-a-nonconformance"></a>Een bewerking maken voor een niet-conformering

Volg deze stappen om een bewerking voor een niet-conformering te maken.

1. Ga naar **Voorraadbeheer \> Periodieke taken \> Kwaliteitsbeheer \> Niet-conformeringen**.
1. Zoek en selecteer in de lijst de niet-conformering die u wilt bijwerken.

    > [!NOTE]
    > U kunt alleen bewerkingen toevoegen aan of bijwerken voor niet-conformeringen die zijn goedgekeurd.

1. Selecteer in het actievenster **Gerelateerde bewerkingen**.
1. Selecteer op de pagina **Gerelateerde bewerkingen** in het actievenster **Nieuw** om een rij aan het raster toe te voegen. Stel daarna de volgende velden in voor de nieuwe rij:

    - **Bewerking**: selecteer de code van de bewerking die voor de niet-conformering wordt uitgevoerd.
    - **Reden**: voer een gedetailleerde omschrijving in waarin u duidelijk maakt waarom de bewerking vereist is.
    - **Verkooporder**: als de geselecteerde bewerkingscode is gerelateerd aan het verkoopordertype, selecteert u de verkooporder die u aan de bewerking koppelt.
    - **Inkooporder**: als de geselecteerde bewerkingscode is gerelateerd aan het inkoopordertype, selecteert u de inkooporder die u aan de bewerking koppelt.

1. Sluit de pagina's.

### <a name="add-items-to-an-operation"></a>Artikelen aan een bewerking toevoegen

Volg deze stappen om artikelen aan een bewerking toe te voegen.

1. Ga naar **Voorraadbeheer \> Periodieke taken \> Kwaliteitsbeheer \> Niet-conformeringen**.
1. Zoek en selecteer in de lijst de niet-conformering die u wilt bijwerken.

    > [!NOTE]
    > U kunt alleen bewerkingen toevoegen aan of bijwerken voor niet-conformeringen die zijn goedgekeurd.

1. Selecteer in het actievenster **Gerelateerde bewerkingen**.
1. Selecteer op de pagina **Gerelateerde bewerkingen** de bewerking waaraan u artikelen wilt toevoegen.
1. Selecteer **Artikelen** in het actievenster.
1. Selecteer op de pagina **Gerelateerde bewerkingen** in het actievenster **Nieuw** om een rij aan het raster toe te voegen. Stel daarna de volgende velden in voor de nieuwe rij:

    - **Artikelnummer**: selecteer het product dat wordt verbruikt als onderdeel van de geselecteerde bewerking.
    - **Hoeveelheid**: voer het aantal artikelen in dat wordt verbruikt.

    > [!NOTE]
    > U kunt de kosten voor het artikel zien in het veld **Kosten** op het tabblad **Algemeen**. De kosten die hier worden weergegeven, zijn afkomstig van de kosten die zijn ingesteld op de pagina **Vrijgegeven product**. De kosten kunnen niet rechtstreeks worden bijgewerkt op de pagina **Artikelen voor gerelateerde bewerking**. De kosten van alle artikelen die zijn toegevoegd op de pagina **Artikelen voor gerelateerde bewerking** worden automatisch toegevoegd aan het veld **Kosten** op de pagina **Gerelateerde bewerkingen**.

1. Herhaal de vorige stap voor elk extra artikel dat u moet toevoegen.
1. Sluit de pagina's.

### <a name="add-quality-charges-to-an-operation"></a>Kwaliteitstoeslagen aan een bewerking toevoegen

Volg deze stappen om kwaliteitstoeslagen aan een bewerking toe te voegen.

1. Ga naar **Voorraadbeheer \> Periodieke taken \> Kwaliteitsbeheer \> Niet-conformeringen**.
1. Zoek en selecteer in de lijst de niet-conformering die u wilt bijwerken.

    > [!NOTE]
    > U kunt alleen bewerkingen toevoegen aan of bijwerken voor niet-conformeringen die zijn goedgekeurd.

1. Selecteer in het actievenster **Gerelateerde bewerkingen**.
1. Selecteer op de pagina **Gerelateerde bewerkingen** de bewerking waaraan u kwaliteitstoeslagen wilt toevoegen.
1. Selecteer in het actievenster **Kwaliteitstoeslagen**.
1. Selecteer op de pagina **Gerelateerde kwaliteitstoeslagen** in het actievenster **Nieuw** om een rij aan het raster toe te voegen. Stel daarna de volgende velden in voor de nieuwe rij:

    - **Toeslagcode**: selecteer de kwaliteitstoeslagen die u wilt toevoegen.
    - **Beschrijving**: voer een gedetailleerde beschrijving van de toeslag in.
    - **Waarde van toeslagen**: Voer het bedrag van de toeslag in.

1. Herhaal de vorige stap voor elke extra toeslag die u moet toevoegen.
1. Sluit de pagina's.

> [!NOTE]
> Het bedrag in het veld **Waarde van toeslagen** wordt automatisch opgeteld voor alle kwaliteitstoeslagen en opgeteld bij andere bedragen in het veld **Kosten** op de pagina **Gerelateerde bewerkingen**.

### <a name="create-a-timesheet-on-an-operation"></a>Een urenstaat maken voor een bewerking

Volg deze stappen om een urenstaat aan een bewerking toe te voegen.

1. Ga naar **Voorraadbeheer \> Periodieke taken \> Kwaliteitsbeheer \> Niet-conformeringen**.
1. Zoek en selecteer in de lijst de niet-conformering die u wilt bijwerken.

    > [!NOTE]
    > U kunt alleen bewerkingen toevoegen aan of bijwerken voor niet-conformeringen die zijn goedgekeurd.

1. Selecteer in het actievenster **Gerelateerde bewerkingen**.
1. Selecteer op de pagina **Gerelateerde bewerkingen** de bewerking waaraan u een urenstaat wilt toevoegen.
1. Selecteer in het actievenster de optie **Urenstaat**.
1. Selecteer op de pagina **Gerelateerde urenstaten** in het actievenster **Nieuw** om een rij aan het raster toe te voegen. Stel daarna de volgende velden in voor de nieuwe rij:

    - **Datum**: Geef de datum op waarop het werk is uitgevoerd. Dit veld is standaard ingesteld op de huidige datum.
    - **Medewerker**: Selecteer de medewerker die het werk heeft uitgevoerd. Dit veld is standaard ingesteld op de medewerker die aan de huidige gebruiker is toegewezen.
    - **Bewerkingstijd**: voer het aantal uren in dat aan de geselecteerde bewerking is besteed.
    - **Gefactureerd**: Schakel dit selectievakje in als de tijd op een factuur in rekening is gebracht aan een klant of leverancier.

    > [!NOTE]
    > U kunt de kosten bekijken in het veld **Kosten** op het tabblad **Algemeen**. De kosten worden berekend op basis van het tarief dat u definieert op de pagina **Parameters voor voorraadbeheer**.

1. Herhaal de vorige stap voor elke extra urenstaatregel die u moet toevoegen.
1. Sluit de pagina's.

> [!NOTE]
> Het bedrag in het veld **Kosten** wordt automatisch opgeteld voor alle urenstaatregels en opgeteld bij andere bedragen in het veld **Kosten** op de pagina **Gerelateerde bewerkingen**.

## <a name="add-a-correction-to-a-nonconformance"></a>Een correctie aan een niet-conformering toevoegen

Om een correctie aan een niet-conformering toe te voegen, volgt u deze stappen.

1. Ga naar **Voorraadbeheer \> Periodieke taken \> Kwaliteitsbeheer \> Niet-conformeringen**.
1. Zoek en selecteer in de lijst de niet-conformering die u wilt bijwerken.

    > [!NOTE]
    > U kunt alleen een correctie toevoegen aan niet-conformeringen die zijn goedgekeurd.

1. Selecteer in het actievenster de optie **Correcties**.
1. Selecteer op de pagina **Correcties** in het actievenster de optie **Nieuw** om een rij aan het raster toe te voegen. Stel daarna de volgende velden in voor de nieuwe rij:

    - **Diagnose**: selecteer het type diagnose dat het type correctie aangeeft dat u maakt.
    - **Medewerker**: selecteer de persoon die verantwoordelijk is voor de correctie.
    - **Correctieprioriteit**: selecteer een optie om aan te geven wat de prioriteit van de correctie is (*Laag*, *Normaal* of *Hoog*).
    - **Gevraagde datum**: voer de datum in waarop de corrigerende actie is aangevraagd.
    - **Geplande datum**: voer de datum in waarop de correctie naar verwachting is voltooid.
    - **Kortetermijnoplossing**: schakel dit selectievakje in als de corrigerende actie de niet-conformering slechts voor korte tijd corrigeert.

1. Sluit de pagina's.

## <a name="mark-a-correction-as-completed"></a>Een correctie als voltooid markeren

Om een correctie van een niet-conformering te markeren als voltooid, volgt u deze stappen.

1. Ga naar **Voorraadbeheer \> Periodieke taken \> Kwaliteitsbeheer \> Niet-conformeringen**.
1. Zoek en selecteer in de lijst de niet-conformering die u wilt bijwerken.

    > [!NOTE]
    > U kunt alleen een correctie toevoegen aan niet-conformeringen die zijn goedgekeurd.

1. Selecteer in het actievenster de optie **Correcties**.
1. Selecteer op de pagina **Correcties** in het raster de correctie die u wilt markeren als voltooid.
1. Selecteer in het actievenster **Als voltooid markeren**.
1. U wordt gevraagd om de selectie te bevestigen. Selecteer **OK** om door te gaan. Het veld **Datum en tijd voltooiing** is ingesteld op de huidige datum en tijd en het selectievakje **Voltooid** is ingeschakeld.
1. Sluit de pagina.

## <a name="reopen-a-completed-correction"></a>Een voltooide correctie opnieuw openen

Om een voltooide correctie opnieuw te openen, volgt u deze stappen.

1. Ga naar **Voorraadbeheer \> Periodieke taken \> Kwaliteitsbeheer \> Niet-conformeringen**.
1. Zoek en selecteer in de lijst de niet-conformering die u wilt bijwerken.
1. Selecteer in het actievenster de optie **Correcties**.
1. Selecteer op de pagina **Correcties** in het raster de correctie die u opnieuw wilt openen.
1. Selecteer **Opnieuw openen** in het actievenster.
1. U wordt gevraagd om de selectie te bevestigen. Selecteer **OK** om door te gaan. De waarde wordt gewist uit het veld **Datum en tijd voltooiing** en het selectievakje **Voltooid** wordt uitgeschakeld.
1. Sluit de pagina.

U kunt nu extra bewerkingen of updates aan de correctie toevoegen. Wanneer u klaar bent, kunt u de correctie opnieuw markeren als voltooid.

## <a name="close-a-nonconformance"></a>Een niet-conformering sluiten

Volg deze stappen om een niet-conformering te sluiten.

1. Ga naar **Voorraadbeheer \> Periodieke taken \> Kwaliteitsbeheer \> Kwaliteitsorders**.
1. Selecteer een kwaliteitsorder in het raster.
1. Selecteer **Query's \> Niet-conformeringen** in het actievenster.
1. Selecteer op de pagina **Niet-conformeringen** de gewenste niet-conformering in het raster.
1. Selecteer in het actievenster **Functies \> Niet-conformering sluiten**.
1. U wordt gevraagd om de selectie te bevestigen. Selecteer **Ja** om door te gaan.
1. Sluit de pagina's.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Overzicht van kwaliteitsbeheer](../quality-management-processes.md)
- [Beheer van kwaliteit en niet-conformeringen inschakelen](../enable-quality-management.md)
- [Medewerkers die verantwoordelijk zijn voor het goedkeuren van niet-conformeringen](../quality-responsible-workers.md)
- [Quarantainezones voor niet-conformeringen](../quality-quarantine-zones.md)
- [Typen diagnosen voor niet-conformeringen](../quality-diagnostic-types.md)
- [Kwaliteitstoeslagen voor niet-conformeringen](../quality-charges.md)
- [Bewerkingen voor niet-conformeringen](../quality-operations.md)
- [Kwaliteitsbeheer voor magazijnprocessen](../quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
