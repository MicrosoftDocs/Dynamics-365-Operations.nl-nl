---
title: Financiële rapporten weergeven
description: In dit onderwerp wordt beschreven hoe u financiële rapporten in Microsoft Dynamics 365 Finance kunt bekijken en verkennen. Het bevat informatie over de verschillende opties die u op financiële rapporten kunt toepassen om hun vormgeving en de gegevens die ze bevatten te wijzigen.
author: kweekley
manager: AnnBe
ms.date: 03/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 10334
ms.assetid: d20f435f-fb65-4068-ab09-7efc7be683a6
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c368259af9454af94da217585b2a1d01ea75d834
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441964"
---
# <a name="view-financial-reports"></a>Financiële rapporten weergeven

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u financiële rapporten kunt bekijken en verkennen. Het bevat informatie over de verschillende opties die u op financiële rapporten kunt toepassen om hun vormgeving en de gegevens die ze bevatten te wijzigen.

<a name="financial-reporting-overview"></a>Overzicht van financiële rapportage
----------------------------

## <a name="open-a-financial-report"></a>Een financieel rapport openen
Als u een rapport wilt openen, selecteert u de rapportnaam. De eerste keer dat een rapport wordt geopend, wordt het automatisch gegenereerd voor de vorige maand. Als u bijvoorbeeld een rapport voor de eerste keer opent in augustus 2015, wordt het rapport gegenereerd voor 31 juli 2015. Nadat een rapport is geopend, kunt u beginnen met het verkennen ervan door in te zoomen op specifieke gegevensitems en rapportopties te wijzigen.

## <a name="drill-down-on-a-financial-report"></a>Inzoomen op een financieel rapport
Financiële rapporten kunnen meerdere detailniveaus bevatten. Het financiële niveau is het eerste niveau dat u ziet wanneer u een financieel rapport opent. Als u naar het rekeningniveau wilt gaan, selecteert u de gegevens waarop u wilt inzoomen. Als u bijvoorbeeld de rekeningdetails voor verkoop wilt weergeven, selecteert u de verkoopgegevens die u wilt bekijken. Via het rekeningniveau kunt u inzoomen om de transacties weer te geven waaruit het rekeningsaldo bestaat. Er zijn twee manieren om transacties weer te geven: rapporttransacties en boekstuktransacties.

-   **Rapporttransacties**: de transacties worden weergegeven in een opgemaakte weergave die in het financiële rapport is opgenomen. Als u transacties in de opgemaakte weergave wilt weergeven, selecteert u de gegevens waarop u wilt inzoomen en klikt u vervolgens op **Inzoomen op transactieniveau van rapport**.
-   **Boekstuktransacties**: er wordt een boekstuktransactiequery geopend, waarin u transacties kunt weergeven. Als u transacties in de boekstuktransactiequery wilt weergeven, selecteert u de gegevens waarop u wilt inzoomen en klikt u vervolgens op **Openstaande rekeningtransacties**.

Als de gegevens budgetgegevens betreffen, kunt u ervoor kiezen budgetjournaalregels te openen. Als u niveaus van het rapport wilt sluiten en wilt terugkeren naar waar u bent begonnen, kunt u op Esc drukken of klikken op de knop **Sluiten** (**X**) rechtsboven.

## <a name="change-report-options"></a>Rapportopties wijzigen
U kunt kenmerk- en dimensiefilters toepassen of het budgetscenario wijzigen in een **Werkelijk versus budget**-rapport Klik in het actievenster op **Rapportopties** en voer vervolgens een of meer van de volgende stappen uit:

-   Als u kenmerkfilters op een rapport wilt toepassen, selecteert u **Een kenmerkfilter toevoegen** Selecteer het kenmerk, typ de kenmerkwaarde en klik vervolgens op **OK**. Als u bijvoorbeeld het kenmerk **Rekeningcategorie** selecteert, voert u **VERKOOP** als de kenmerkwaarde in. Als u een kenmerkfilter wilt verwijderen, klikt u op **Wissen**.
-   Als u dimensiefilters op een rapport wilt toepassen, selecteert u **Een dimensiefilter toevoegen**. Selecteer de dimensie en typ vervolgens de dimensie-ID of selecteer de dimensie in de lijst. Als u een dimensiefilter wilt verwijderen, klikt u op **Wissen**.
-   Als u het scenario in een rapport **Werkelijk versus budget**-rapport wilt wijzigen, selecteert u een nieuw scenario en klikt u vervolgens op **OK**. Als het geselecteerde scenario voor een ander boekjaar geldt, worden er geen resultaten geretourneerd. Als er bijvoorbeeld een rapport wordt gegenereerd voor BJ2015 en het huidige scenario voor BJ2015 is en het nieuwe scenario is geselecteerd voor BJ2016, worden er geen resultaten geretourneerd. Als er een nieuw scenario voor een ander boekjaar nodig is, moet u een nieuwe versie van het rapport genereren voor het boekjaar dat is gerelateerd aan het scenario.

Wanneer u klikt op **OK**, worden alle door u geselecteerde opties toegepast op het rapport. Als u besluit dat u de geselecteerde opties niet wilt toepassen, klikt op **Annuleren**.

## <a name="update-a-financial-report"></a>Een financieel rapport bijwerken
U kunt een financieel rapport vernieuwen (bijwerken) zodat het de meest recente gegevens voor de periode en het jaar bevat waarvoor het rapport is gegenereerd. Als u bijvoorbeeld een financieel rapport bijwerkt dat voor oktober 2015 is gegenereerd, worden in het rapport alle nieuwe transacties weergegeven die voor oktober 2015 zijn geboekt. Als u een financieel rapport wilt bijwerken, klikt u in het actievenster op **Vernieuwen**. Een bijgewerkte rapport is alleen beschikbaar voor de persoon die het heeft bijgewerkt. Om ervoor te zorgen dat andere mensen dezelfde gegevens kunnen zien, moet het rapport worden gepubliceerd.

## <a name="publish-a-financial-report"></a>Een financieel rapport publiceren
Nadat u een financieel rapport hebt bijgewerkt, kunt u het publiceren. Andere personen in de organisatie kunnen het dan weergeven. Als u een rapport wilt publiceren, klikt u in het actievenster op **Publiceren**.

## <a name="display-a-financial-report-in-a-different-currency"></a>Een financieel rapport in een andere valuta weergeven
Een financieel rapport kan op elk gewenst moment in een willekeurige valuta worden weergegeven. Als u een rapport in een andere valuta wilt weergeven, klikt u in het actievenster op **Valuta** en selecteert u vervolgens een valuta. Het rapport wordt in die valuta omgezet en de resultaten worden weergegeven. Alle valutacodes of symbolen die als onderdeel van het rapportontwerp zijn opgenomen, worden bijgewerkt om de nieuwe valuta weer te geven. De valuta's die in de lijst worden weergegeven, zijn de aangiftevaluta's die in Finance zijn geconfigureerd.

## <a name="display-a-summarized-view-of-the-financial-report"></a>Een overzichtsweergave van het financiële rapport weergeven
Een financieel rapport kan detailregels en overzichtsregels bevatten. De detailregels zijn regels die hoofdrekeningen of dimensies bevatten. De overzichtsregels zijn omschrijvings-, totaal- en berekeningsregels. Als u alleen de overzichtsregels van een rapport wilt weergeven, klikt u op **Weergeven** en vervolgens op **Alleen overzichtsregels**. Het rapport wordt samengevouwen en alleen de overzichtsregels worden weergegeven. Als u de detailregels samen met de overzichtsregels wilt weergeven, klik u op **Weergeven** en vervolgens op **Alleen overzichtsregels**.

## <a name="print-a-financial-report"></a>Een financieel rapport afdrukken
Als een financieel rapport wordt afgedrukt, wordt een PDF-bestand gemaakt dat vervolgens handmatig kan worden afgedrukt. Als u een afdrukbaar financieel rapport wilt maken, klikt u in het actievenster op **Afdrukken** en voert u vervolgens een of meer van de volgende stappen uit om de afdrukopties in te stellen:

-   Als u de verschillende detailniveaus in het afgedrukte rapport wilt opnemen, stelt u de schuifregelaar in op **Ja** of **Nee**. Als een rapportagestructuur wordt gebruikt in een rapport, kunt u ervoor kiezen alle rapportage-eenheden of alleen de huidige rapportage-eenheid op te nemen.
-   Als u het paginaformaat wilt instellen, selecteert u een paginaformaat in de lijst.
-   Als u de pagina-indeling wilt instellen, selecteert u een indeling in de lijst. Als u de rapportinhoud wilt aanpassen aan de door u geselecteerde breedte, stelt u de schuifregelaar in op **Ja**.
-   Als u de paginamarges wilt instellen, typt u de grootte van de boven-, onder-, linker- en rechtermarges in inches.

Nadat u klaar bent met het instellen van de afdrukopties, klikt u op **Afdrukken** om door te gaan en wordt u gevraagd of u het bestand wilt downloaden of het bestand wilt opslaan naar OneDrive of SharePoint. Als u besluit dat u niet wilt doorgaan, klikt u in plaats daarvan op **Annuleren**. Als u doorgaat, wordt het rapport op de server weergegeven en wordt u gevraagd het rapport in PDF-indeling te downloaden. Nu kunt u het rapport weergeven in uw PDF-viewer en hier kunt u de printer selecteren waarnaar u het rapport wilt verzenden en kunt u eventuele verdere aanpassingen doorvoeren voor de afdrukopties.

## <a name="export-a-financial-report"></a>Een financieel rapport exporteren
Als u een financieel rapport wilt exporteren, klikt u in het actievenster op **Exporteren**. Het rapport wordt geëxporteerd naar Microsoft Excel en in uw browser wordt u gevraagd of u het geëxporteerde bestand wilt openen of opslaan. De exportinstellingen die in het rapportontwerp zijn gedefinieerd, worden toegepast op het geëxporteerde rapport.    

<a name="additional-resources"></a>Aanvullende bronnen
--------

[Financiële rapportage](../../dev-itpro/analytics/financial-reporting-intro.md)




