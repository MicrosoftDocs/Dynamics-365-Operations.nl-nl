---
title: Integratie van notities
description: In dit artikel wordt de integratie van notitiegegevens bij twee keer wegschrijven beschreven.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: f09d455181b7929e25d5238949a0236ac60d457b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289011"
---
# <a name="note-integration"></a>Integratie van notities

[!include [banner](../../includes/banner.md)]



Tijdens bedrijfsprocessen verzamelen Microsoft Dynamics 365-gebruikers vaak informatie over hun klanten. Deze informatie wordt geregistreerd als activiteiten en notities. In dit artikel wordt de integratie van notitiegegevens bij twee keer wegschrijven beschreven.

Klantgegevens kunnen op de volgende manieren worden geclassificeerd:

+ **Bruikbare informatie die een Dynamics 365-gebruiker namens een klant verwerkt**: Contoso (een Dynamics 365-gebruiker) organiseert bijvoorbeeld een spelprogramma. Een van de klanten van Contoso (een klant) wil het spelprogramma bijwonen. De klant vraagt een Contoso-werknemer om een plekje in het spelprogramma voor hen te boeken. De boeking vindt plaats in de kalender van de gebeurtenisdeelnemer van Contoso.
+ **Bruikbare informatie voor een Dynamics 365-gebruiker**: een klant die een Surface-eenheid aanschaft, voert bijvoorbeeld speciale instructies in om aan te geven dat het apparaat als geschenk moet worden ingepakt voordat het wordt afgeleverd. Deze instructies zijn bruikbare gegevens die moeten worden verwerkt door de Contoso-werknemer die verantwoordelijk is voor de verpakking.
+ **Niet-bruikbare informatie**: een klant bezoekt bijvoorbeeld de Contoso-winkel en toont tijdens het gesprek met een winkelmedewerker interesse in *Halo*-games en gamingaccessoires. De winkelmedewerker maakt een notitie van deze informatie. De engine voor productaanbevelingen gebruikt deze dan om aanbevelingen te doen aan de klant.

Bruikbare informatie wordt over het algemeen vastgelegd als *activiteiten* in apps voor financiën en bedrijfsactiviteiten en Customer Engagement-apps. Niet-bruikbare informatie wordt vastgelegd als *notities* in apps voor financiën en bedrijfsactiviteiten en als *aantekeningen* in Customer Engagement-apps.

> [!TIP]
> Hoewel notities zijn bedoeld voor niet-bruikbare informatie, kunnen de apps wel worden gebruikt voor het opslaan en verwerken van bruikbare informatie als u deze op die manier wilt gebruiken.

Microsoft brengt momenteel functionaliteit voor integratie van notities uit. (Functionaliteit voor activiteitsintegratie wordt later vrijgegeven.) Integratie van notities is beschikbaar voor klanten, leveranciers, verkooporders en inkooporders.

## <a name="create-a-note-in-a-customer-engagement-app"></a>Een notitie maken in een app voor klantbetrokkenheid

Voer de volgende stappen uit om een notitie te maken in een Customer Engagement-app en deze vervolgens te synchroniseren met een app voor financiën en bedrijfsactiviteiten.

1. Open in de app voor klantbetrokkenheid de rekeningrecord voor een klant.
2. Selecteer in het deelvenster **Tijdlijn** het plusteken (**+**) en selecteer vervolgens **Notitie** om een notitie te maken.

    ![Een notitie maken in de app voor klantbetrokkenheid.](media/notes-ce-1.png)

3. Voer een titel en beschrijving in en selecteer vervolgens **Notitie toevoegen**.

    ![Een titel en beschrijving invoeren.](media/notes-ce-2.png)

    De nieuwe notitie wordt toegevoegd aan de tijdlijn van de klant.

    ![Nieuwe notitie op de tijdlijn van klant.](media/notes-ce-3.png)

4. Meld u aan bij de app voor financiën en bedrijfsactiviteiten en open dezelfde klantrecord. De knop **Bijlagen** (paperclipsymbool) rechtsboven geeft aan dat de record een bijlage heeft.

    ![Melding over een bijlage.](media/notes-ce-4.png)

5. Selecteer de knop **Bijlagen** om de pagina **Bijlagen** te openen. U zou de notitie moeten vinden die u hebt gemaakt in de app voor klantbetrokkenheid.

    ![Notitie vanuit de app voor klantbetrokkenheid.](media/notes-ce-5.png)

Alle updates van de notitie worden steeds gesynchroniseerd tussen de app voor financiën en bedrijfsactiviteiten en de Customer Engagement-app.

## <a name="create-a-note-in-a-finance-and-operations-app"></a>Een notitie maken in een app voor financiën en bedrijfsactiviteiten

U kunt ook een notitie maken in een app voor financiën en bedrijfsactiviteiten. Deze wordt vervolgens gesynchroniseerd met een Customer Engagement-app.

Voer de volgende stappen uit om een notitie te maken in een app voor financiën en bedrijfsactiviteiten en deze vervolgens te synchroniseren met een Customer Engagement-app.

1. Selecteer in de app voor financiën en bedrijfsactiviteiten op de pagina **Bijlagen** **Nieuw** \> **Notitie**.

    ![Een notitie in de app voor financiën en bedrijfsactiviteiten maken.](media/notes-fo-1.png)

2. Voer een titel en een korte reeks instructies in en selecteer **Opslaan**.

    ![Een titel en instructies invoeren.](media/notes-fo-2.png)

3. Werk de record bij in de app voor klantbetrokkenheid. U zou de nieuwe notitie op de tijdlijn moeten vinden.

    ![Nieuwe notitie op de tijdlijn in de app voor klantbetrokkenheid.](media/notes-fo-3.png)

U kunt een notitie classificeren als intern of extern.

- Open de notitie in de app voor financiën en bedrijfsactiviteiten op de pagina **Bijlagen** en selecteer vervolgens in het veld **Beperking** de optie **Intern** of **Extern**.

    ![Beperkingsveld.](media/notes-fo-4.png)

U kunt ook een URL maken.

1. Selecteer in de app voor financiën en bedrijfsactiviteiten op de pagina **Bijlagen** **Nieuw** \> **URL**.
2. Voer een titel en de URL in.
3. Selecteer in het veld **Beperking** de optie **Intern** of **Extern**.

    ![Een URL in de app voor financiën en bedrijfsactiviteiten maken.](media/notes-fo-5.png)

4. Selecteer **Opslaan**.

    Omdat apps voor klantbetrokkenheid geen URL-type hebben, wordt de URL met twee keer wegschrijven als notitie geïntegreerd.

    ![URL die wordt weergegeven als notitie maken in de app voor klantbetrokkenheid.](media/notes-ce-6.png)

> [!NOTE]
> Bestandsbijlagen worden niet ondersteund.

## <a name="templates"></a>Sjablonen

Integratie van notities omvat een verzameling tabeltoewijzingen die samenwerken tijdens de interactie van gegevens, zoals in de volgende tabel wordt weergegeven.

| App voor financiële en bedrijfsactiviteiten | Customer Engagement-app | Description |
|----------------------------|-------------------------|-------------|
| [Klantbijlagen](mapping-reference.md#230) | Aantekeningen | Bedrijven die tekst zonder opmaak en URL's gebruiken om klantspecifieke informatie (voor organisaties en personen) vast te leggen. |
| [Bijlagen van leveranciersdocument](mapping-reference.md#231) | Aantekeningen | Bedrijven die tekst zonder opmaak en URL's gebruiken om leverancierspecifieke informatie (voor organisaties en personen) vast te leggen. |
| [Documentbijlagen van verkooporderkoptekst](mapping-reference.md#229) | Aantekeningen | Bedrijven die tekst zonder opmaak en URL's gebruiken om specifieke informatie over verkooporders vast te leggen. |
| [Documentbijlagen van inkooporderkoptekst](mapping-reference.md#232) | Aantekeningen | Bedrijven die tekst zonder opmaak en URL's gebruiken om specifieke informatie over inkooporders vast te leggen. |

## <a name="limitations"></a>Beperkingen

Zodra u de oplossing voor notities hebt geïnstalleerd, kunt u deze niet meer verwijderen. 

Zie [Toewijzingsverwijzing voor twee keer wegschrijven](mapping-reference.md) voor meer informatie.

