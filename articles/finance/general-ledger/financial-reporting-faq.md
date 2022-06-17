---
title: Veelgestelde vragen over Financiële rapportage
description: Dit artikel biedt antwoorden op een aantal veelgestelde vragen over Financiële rapportage.
author: jinniew
ms.date: 07/07/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 5981946a4bba2c58402f4cf566bfa008de67363b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901365"
---
# <a name="financial-reporting-faq"></a>Veelgestelde vragen over Financiële rapportage

Dit artikel biedt antwoorden op veelgestelde vragen over Financiële rapportage.

## <a name="how-do-i-restrict-access-to-a-report-by-using-tree-security"></a>Hoe beperk ik de toegang tot een rapport door middel van structuurbeveiliging?

In het volgende voorbeeld ziet u hoe u de toegang tot een rapport beperkt met structuurbeveiliging.

Het USMF-demobedrijf heeft een **balansrapport** waartoe niet alle gebruikers van Financiële rapportage toegang moeten krijgen. U kunt structuurbeveiliging gebruiken om de toegang tot één rapport te beperken, zodat alleen bepaalde gebruikers toegang hebben.

1. Meld u aan bij Financial Reporter Report Designer.
2. Selecteer **Bestand \> Nieuw \> Structuurdefinitie** om een nieuwe structuurdefinitie te maken.
3. Tik of klik twee keer op de regel **Samenvatting** in de kolom **Beveiliging van eenheid**.
4. Klik op **Gebruikers en groepen**.
5. Selecteer de gebruikers of groepen die toegang tot het rapport moeten krijgen.
6. Selecteer **Opslaan**.
7. Voeg in de rapportdefinitie uw nieuwe structuurdefinitie toe.
8. Selecteer **Instelling** in de structuurdefinitie. Selecteer vervolgens onder **Rapporteringseenheden selecteren** de optie **Alle eenheden opnemen**.

## <a name="how-do-i-identify-which-accounts-dont-match-my-balances"></a>Hoe bepaal ik welke rekeningen niet met mijn saldi overeenkomen?

Als u een niet-salderend rapport hebt, gebruikt u de volgende procedures om de rekeningen en afwijkingen te identificeren.

### <a name="in-financial-reporter-report-designer"></a>In Financial Reporter Report Designer

1. Maak een nieuwe rijdefinitie.
2. Selecteer **Bewerken \> Rijen invoegen uit dimensies**.
3. Selecteer **MainAccount**.
4. Selecteer **OK**.
5. Sla de rijdefinitie op.
6. Maak een nieuwe kolomdefinitie.
7. Maak een nieuwe rapportdefinitie.
8. Selecteer **Instellingen** en schakel deze optie uit.
9. Genereer het rapport. 
10. Exporteer het rapport naar Microsoft Excel.

### <a name="in-dynamics-365-finance"></a>In Dynamics 365 Finance

1. Ga naar **Grootboek \> Query's en rapporten \> Proefbalans**.
2. Stel de volgende velden in:

    - **Begindatum**: voer het begindatum van het fiscale jaar in.
    - **Einddatum**: voer de datum in waarvoor u het rapport genereert.
    - **Financiële dimensie**: stel dit veld in op **Hoofdrekening ingesteld**.

3. Selecteer **Berekenen**.
4. Exporteer het rapport naar Excel.

U kunt de gegevens nu uit het Excel-rapport in Financial Reporter kopiëren naar het **proefbalansrapport** zodat u de kolommen **Eindsaldo** kunt vergelijken.

## <a name="when-i-design-a-report-in-report-designer-or-when-i-generate-a-financial-report-i-received-the-following-message-the-operation-could-not-be-completed-due-to-a-problem-in-the-data-provider-framework-how-should-i-respond"></a>Als ik een rapport ontwerp in Report Designer of tijdens het genereren van een financieel rapport, zie ik het volgende bericht: "De bewerking kan niet worden voltooid vanwege een probleem in het gegevensproviderraamwerk." Hoe moet ik reageren?

Het bericht geeft aan dat er een probleem is opgetreden op het moment dat het systeem heeft geprobeerd om financiële metagegevens op te halen uit de datamart terwijl u Financiële rapportage gebruikte. U kunt op twee manieren op dit probleem reageren:

- Controleer de integratiestatus van de gegevens met **Hulpmiddelen \> Integratiestatus** in Report Designer. Als de integratie onvolledig is, moet u wachten tot deze is voltooid. Probeer vervolgens dezelfde actie opnieuw uit te voeren.
- Neem contact op met Ondersteuning om het probleem vast te stellen en op te lossen. Het systeem kan inconsistente gegevens bevatten. Ondersteuningsmedewerkers kunnen u helpen om dat probleem op de server te vinden en de specifieke gegevens te bepalen waarvoor een update nodig is.

## <a name="how-does-the-selection-of-historical-rate-translation-affect-report-performance"></a>Welke invloed heeft de selectie van historische koersomzettingen op de prestaties van het rapport?

De historische koers wordt meestal gebruikt bij rekeningen voor ingehouden winsten, materiële vaste activa en eigen vermogen. De historische koers kan vereist zijn op basis van richtlijnen van de Financial Accounting Standards Board (FASB) of algemeen aanvaarde boekhoudbeginselen (GAAP). Zie voor meer informatie [Valutamogelijkheden in financiële rapportage](financial-reporting-currency-capability.md).

## <a name="how-many-types-of-currency-rate-are-there"></a>Hoeveel soorten valutakoersen zijn er?

Er zijn drie typen:

- **Huidige koers**: dit type wordt meestal gebruikt bij balansrekeningen. Dit wordt meestal de *spotkoers* genoemd en kan de koers zijn op de laatste dag van de maand of een andere vooraf bepaalde datum.
- **Gemiddelde koers**: dit type wordt meestal gebruikt bij winst-en-verliesrekeningen met een inkomstenoverzicht. U kunt de gemiddelde koers instellen om een eenvoudig of een gewogen gemiddelde toe te passen.
- **Historische koers**: dit type wordt meestal gebruikt bij rekeningen voor ingehouden winsten, materiële vaste activa en eigen vermogen. Deze rekeningen kunnen vereist zijn op basis van FASB- of GAAP-richtlijnen.

## <a name="how-does-historical-currency-translation-work"></a>Hoe werkt historische valutaomrekening?

De koersen zijn specifiek voor de transactiedatum. Daarom wordt elke transactie afzonderlijk omgerekend, op basis van de dichtstbijzijnde wisselkoers.

Voor historische valutaomrekening kunnen de vooraf berekende periodesaldi worden gebruikt in plaats van afzonderlijke transactiegegevens. Dit gedrag verschilt van het gedrag voor huidige koersomzetting.

## <a name="how-does-historical-currency-translation-affect-performance"></a>Wat is de invloed van de historische valutaomrekening op de prestaties?

Wanneer gegevens in de rapporten worden bijgewerkt, kan er vertraging optreden omdat bedragen opnieuw moeten worden berekend met controle van de transactiegegevens. Deze vertraging is elke keer van toepassing wanneer de tarieven worden bijgewerkt of meer transacties worden geboekt. Als er bijvoorbeeld een paar keer per dag duizenden rekeningen worden ingesteld voor historische omzetting, kan er een vertraging van maximaal een uur optreden voordat de gegevens in het rapport zijn bijgewerkt. Als er een kleiner aantal specifieke rekeningen is, kunnen de verwerkingstijden voor het bijwerken van rapportgegevens teruglopen tot een paar minuten of minder.

Wanneer rapporten worden gegenereerd met behulp van valutaomzetting voor rekeningen met een historische koers, worden er ook extra berekeningen per transactie uitgevoerd. Afhankelijk van het aantal rekeningen kan de tijd voor het genereren van de rapporten meer dan verdubbelen.

## <a name="what-are-the-estimated-data-mart-integration-intervals"></a>Wat zijn de geschatte intervallen voor datamart-integratie?

Financial Reporter gebruikt zestien taken om gegevens van Dynamics 365 Finance te kopiëren naar de Financial Reporter-database. In de volgende tabel worden deze zestien taken vermeld en wordt het interval aangegeven dat aangeeft hoe vaak elke taak wordt uitgevoerd. De intervallen kunnen niet worden gewijzigd.

| Naam                                                       | Interval | Intervaltiming |
|------------------------------------------------------------|----------|-----------------|
| AX 2012-rekeningcategorieën naar rekeningcategorie            | 41       | Minuten         |
| AX 2012-rekeningen naar rekening                                | 7        | Minuten         |
| AX 2012-bedrijven naar bedrijf                               | 300      | Seconden         |
| AX 2012-bedrijven naar organisatie                          | 23       | Minuten         |
| AX 2012-dimensiecombinaties naar dimensiecombinatie    | 1        | Minuten         |
| AX 2012-dimensiewaarden naar dimensiewaarde                | 11       | Minuten         |
| AX 2012-dimensies naar dimensie                            | 31       | Minuten         |
| AX 2012-wisselkoersen naar wisselkoers                    | 17       | Minuten         |
| AX 2012-boekjaren naar boekjaar                        | 13       | Minuten         |
| AX 2012-grootboektransacties naar feit                | 1        | Minuten         |
| AX 2012-organisatiehiërarchieën naar structuur                   | 3600    | Seconden         |
| AX 2012-scenario's naar scenario                              | 29       | Minuten         |
| AX 2012-kwalificaties van transactietypen naar kwalificatie van feittype | 19       | Minuten         |
| Onderhoudstaak                                           | 1        | Minuten         |
| MR-rapportdefinities naar financiële rapporten in AX7             | 45       | Seconden         |
| Rapportversies in MR naar versies van financiële rapporten in AX         | 45       | Seconden         |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
