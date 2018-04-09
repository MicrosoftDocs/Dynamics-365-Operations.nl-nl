---
title: "Financiële rapporten weergeven"
description: "In dit artikel wordt beschreven hoe u financiële rapporten kunt bekijken en verkennen in Microsoft Dynamics 365 for Finance and Operations. Het bevat informatie over de verschillende opties die u op financiële rapporten kunt toepassen om hun vormgeving en de gegevens die ze bevatten te wijzigen."
author: kweekley
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 10334
ms.assetid: d20f435f-fb65-4068-ab09-7efc7be683a6
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 055001c992e70ceacf57cf25a8bf83207d8d7334
ms.contentlocale: nl-nl
ms.lasthandoff: 03/26/2018

---

# <a name="view-financial-reports"></a>Financiële rapporten weergeven

[!include[banner](../includes/banner.md)]


In dit artikel wordt beschreven hoe u financiële rapporten kunt bekijken en verkennen in Microsoft Dynamics 365 for Finance and Operations. Het bevat informatie over de verschillende opties die u op financiële rapporten kunt toepassen om hun vormgeving en de gegevens die ze bevatten te wijzigen.

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
U kunt de rapportdatum wijzigen, kenmerk- en dimensiefilters toepassen of het budgetscenario wijzigen in een **Werkelijk versus budget**-rapport Klik in het actievenster op **Rapportopties** en voer vervolgens een of meer van de volgende stappen uit:

-   Als u de basisperiode en het basisjaar van een rapport wilt wijzigen, selecteert u een basisperiode en een basisjaar en klikt u vervolgens op **OK**.
-   Als u kenmerkfilters op een rapport wilt toepassen, selecteert u **Een kenmerkfilter toevoegen** Selecteer het kenmerk, typ de kenmerkwaarde en klik vervolgens op **OK**. Als u bijvoorbeeld het kenmerk **Rekeningcategorie** selecteert, voert u **VERKOOP** als de kenmerkwaarde in. Als u een kenmerkfilter wilt verwijderen, klikt u op **Wissen**.
-   Als u dimensiefilters op een rapport wilt toepassen, selecteert u **Een dimensiefilter toevoegen**. Selecteer de dimensie en typ vervolgens de dimensie-ID of selecteer de dimensie in de lijst. Als u een dimensiefilter wilt verwijderen, klikt u op **Wissen**.
-   Als u het scenario in een rapport **Werkelijk versus budget**-rapport wilt wijzigen, selecteert u een nieuw scenario en klikt u vervolgens op **OK**. Als het geselecteerde scenario voor een ander jaar is, moet u het basisjaar bijwerken. Als het huidige scenario bijvoorbeeld FY2015 is en u een nieuw scenario selecteert dat voor FY2016 is, moet u het basisjaar wijzigen in **2016**.

Wanneer u klikt op **OK**, worden alle door u geselecteerde opties toegepast op het rapport. Als u besluit dat u de geselecteerde opties niet wilt toepassen, klikt op **Annuleren**.

## <a name="update-a-financial-report"></a>Een financieel rapport bijwerken
U kunt een financieel rapport vernieuwen (bijwerken) zodat het de meest recente gegevens voor de periode en het jaar bevat waarvoor het rapport is gegenereerd. Als u bijvoorbeeld een financieel rapport bijwerkt dat voor oktober 2015 is gegenereerd, worden in het rapport alle nieuwe transacties weergegeven die voor oktober 2015 zijn geboekt. Als u een financieel rapport wilt bijwerken, klikt u in het actievenster op **Vernieuwen**. Een bijgewerkte rapport is alleen beschikbaar voor de persoon die het heeft bijgewerkt. Om ervoor te zorgen dat andere mensen dezelfde gegevens kunnen zien, moet het rapport worden gepubliceerd.

## <a name="publish-a-financial-report"></a>Een financieel rapport publiceren
Nadat u een financieel rapport hebt bijgewerkt, kunt u het publiceren. Andere personen in de organisatie kunnen het dan weergeven. Als u een rapport wilt publiceren, klikt u in het actievenster op **Publiceren**.

## <a name="display-a-financial-report-in-a-different-currency"></a>Een financieel rapport in een andere valuta weergeven
Een financieel rapport kan op elk gewenst moment in een willekeurige valuta worden weergegeven. Als u een rapport in een andere valuta wilt weergeven, klikt u in het actievenster op **Valuta** en selecteert u vervolgens een valuta. Het rapport wordt in die valuta omgezet en de resultaten worden weergegeven. Alle valutacodes of symbolen die als onderdeel van het rapportontwerp zijn opgenomen, worden bijgewerkt om de nieuwe valuta weer te geven. De valuta's die in de lijst worden weergegeven, zijn de aangiftevaluta's die in Finance and Operations zijn geconfigureerd.

## <a name="display-a-summarized-view-of-the-financial-report"></a>Een overzichtsweergave van het financiële rapport weergeven
Een financieel rapport kan detailregels en overzichtsregels bevatten. De detailregels zijn regels die hoofdrekeningen of dimensies bevatten. De overzichtsregels zijn omschrijvings-, totaal- en berekeningsregels. Als u alleen de overzichtsregels van een rapport wilt weergeven, klikt u op **Weergeven** en vervolgens op **Alleen overzichtsregels**. Het rapport wordt samengevouwen en alleen de overzichtsregels worden weergegeven. Als u de detailregels samen met de overzichtsregels wilt weergeven, klik u op **Weergeven** en vervolgens op **Alleen overzichtsregels**.

## <a name="open-a-financial-report-from-a-previous-month"></a>Een financieel rapport van een vorige maand openen
U kunt rapporten voor de huidige maand of vorige maanden weergeven zonder het rapport opnieuw te genereren. Als u het rapport voor een vorige maand wilt openen, klikt u op **Weergeven** en vervolgens op **Vorige rapporten**. Er wordt een lijst van de vorige maanden weergegeven waarvoor het rapport is gegenereerd. Vouw de maand uit waarvoor u het rapport wilt weergeven, selecteer de datum en klik vervolgens op **OK**. Het rapport voor de vorige dag wordt weergegeven. Als u wilt terugkeren naar het rapport van de huidige maand, klikt u op **Annuleren**.

## <a name="print-a-financial-report"></a>Een financieel rapport afdrukken
Als u een financieel rapport wilt afdrukken, klikt u in het actievenster op **Afdrukken** en voert u vervolgens een of meer van de volgende stappen uit om de afdrukopties in te stellen:

-   Als u de verschillende detailniveaus in het afgedrukte rapport wilt opnemen, stelt u de schuifregelaar in op **Ja** of **Nee**. Als een rapportagestructuur wordt gebruikt in een rapport, kunt u ervoor kiezen alle rapportage-eenheden of alleen de huidige rapportage-eenheid op te nemen.
-   Als u het paginaformaat wilt instellen, selecteert u een paginaformaat in de lijst.
-   Als u de pagina-indeling wilt instellen, selecteert u een indeling in de lijst. Als u de rapportinhoud wilt aanpassen aan de door u geselecteerde breedte, stelt u de schuifregelaar in op **Ja**.
-   Als u de paginamarges wilt instellen, typt u de grootte van de boven-, onder-, linker- en rechtermarges in inches.

Wanneer u klaar bent met het instellen van de afdrukopties, klikt u op **Afdrukken** om het rapport af te drukken. Als u besluit het rapport niet af te drukken, klikt u in plaats daarvan op **Annuleren**. Een voorbeeld van het afgedrukte rapport wordt weergegeven. U kunt de printer selecteren waarnaar u het rapport wilt verzenden en u kunt ook de afdrukopties aanpassen.

## <a name="export-a-financial-report"></a>Een financieel rapport exporteren
Als u een financieel rapport wilt exporteren, klikt u in het actievenster op **Exporteren**. Het rapport wordt geëxporteerd naar Microsoft Excel en in uw browser wordt u gevraagd of u het geëxporteerde bestand wilt openen of opslaan. De exportinstellingen die in het rapportontwerp zijn gedefinieerd, worden toegepast op het geëxporteerde rapport.    

<a name="see-also"></a>Zie ook
--------

[Financiële rapportage voor Microsoft Dynamics AX](../../dev-itpro/analytics/financial-reporting-intro.md)





