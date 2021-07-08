---
title: Veelgestelde vragen over Financiële rapportage
description: Dit onderwerp biedt antwoorden op een aantal veelgestelde vragen over Financiële rapportage.
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e1b67f86446403933005008a9a1e2cc6739dc516
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266628"
---
# <a name="financial-reporting-faq"></a>Veelgestelde vragen over Financiële rapportage

Dit onderwerp biedt antwoorden op veelgestelde vragen over Financiële rapportage.

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

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
