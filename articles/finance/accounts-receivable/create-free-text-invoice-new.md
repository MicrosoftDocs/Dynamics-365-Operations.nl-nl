---
title: Een vrije-tekstfactuur invoeren
description: In dit onderwerp wordt uitgelegd hoe u vrije-tekstfacturen maakt.
author: abruer
ms.date: 02/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 6e9578d9b2d61f241ab5e92fc9740b88b80969f6
ms.sourcegitcommit: 411874545d7c326fc4aa877948a059371f0ccb3c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/07/2022
ms.locfileid: "8392880"
---
# <a name="create-a-free-text-invoice"></a>Een vrije-tekstfactuur invoeren

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u vrije-tekstfacturen maakt. Gebruik voor de procedure het demobedrijf **USMF**.

## <a name="create-a-free-text-invoice"></a>Een vrije-tekstfactuur invoeren

1. Ga naar **Klanten (of Verkoopgrootboek) \> Facturen \> Alle vrije-tekstfacturen**.
2. Selecteer **Nieuw**.
3. Selecteer een waarde in het veld **Klantrekening**.

    * De rekening die als de klantrekening wordt geselecteerd, wordt standaard als de factuurrekening gebruikt.
    * De boekhoudstatus begint met **Onderhanden** als de factuur niet is geboekt.
    * Het factuurnummer wordt toegewezen wanneer de factuur wordt geboekt.
    * Als u SEPA-mandaten (Single Euro Payments Area) gebruikt, wordt het mandaat voor automatische afschrijving automatisch ingevoerd wanneer u de klantrekening selecteert.

4. Voer een waarde in het veld **Beschrijving** in.
5. Geef in het veld **Hoofdrekening** een rekeningnummer op dat geen dimensies heeft. Verderop in dit onderwerp gaat u dimensies invoeren.

    U kunt ook een of meerdere tekens voor de hoofdrekening invoeren en de zoekopdracht gebruiken om uw rekening te zoeken.

6. Selecteer het sneltabblad **Regeldetails** om dimensies aan de hoofdrekening toe te voegen.
7. Selecteer het tabblad **Financiële dimensieregel**.

    * De dimensies gelden uitsluitend voor de geselecteerde regel.
    * De btw-groep wordt overgenomen van de klant. Als de klant geen btw-groep heeft, wordt de btw-groep van de hoofdrekening gebruikt.
    * De btw-groep van het artikel wordt overgenomen van de hoofdrekening. Als de hoofdrekening geen btw-groep voor het artikel heeft, wordt de in de btw-parameters in het grootboek opgegeven btw-groep voor het artikel gebruikt.

8. Optioneel: voer in het veld **Hoeveelheid** een getal in.
9. Optioneel: voer een getal in het veld **Eenheidsprijs** in.

    Het bedrag wordt berekend als de hoeveelheid keer de eenheidsprijs. U kunt die berekening echter negeren door een bedrag in te voeren.

10. Selecteer **Btw** om de voor de factuur berekende btw te bekijken.

    U kunt de btw-bedragen op deze pagina bekijken of u kunt de bedragen op het tabblad **Correctie** negeren.

11. Selecteer **OK**.
12. Selecteer **Toeslagen** om een toeslag aan de factuur toe te voegen.
13. Voer een waarde in het veld **Toeslagcode** in.
14. Voer een getal in het veld **Waarde van toeslagen** in.
15. Sluit de pagina.
16. Selecteer **Totalen** om een overzicht van de factuurdetails en -totalen weer te geven.
17. Selecteer **Sluiten**.
18. Selecteer **Boeken** om de factuur te boeken. U hebt nog altijd een mogelijkheid om te annuleren voordat u werkelijk boekt.

    * U kunt de timing van het afdrukken van facturen wijzigen. Selecteer **Huidige** om elke factuur af te drukken wanneer deze wordt bijgewerkt. Selecteer **Na** om af te drukken nadat alle facturen zijn bijgewerkt.
    * Als u wilt wijzigen hoe de kredietlimiet van de klant wordt gecontroleerd voordat de factuur wordt geboekt, wijzigt u de waarde in het veld **Kredietlimiettype**.
    * U kunt instellen dat het boeken van vrije-tekstfacturen wordt gestopt wanneer er een fout optreedt op het tabblad **Updates** op de pagina **Parameters van klanten** (**Klanten > Instellingen > Parameters van klanten**). Selecteer **Ja** voor de parameter **Boeken van vrije-tekstfacturen stoppen bij eerste fout** om het boeken van vrije-tekstfacturen te stoppen wanneer er een fout optreedt. Als er in een batch wordt geboekt, stopt een fout het boekingsproces en wordt de batchstatus ingesteld op **Fout**. Als deze optie niet is geselecteerd, slaat het boekingsproces een factuur met een boekingsfout over en blijft het extra facturen boeken. Als er in een batch wordt geboekt, kunnen er door een boekingsfout geen andere facturen worden geboekt. De batchstatus wordt **Beëindigd**. Er is een gedetailleerd boekingsprocesrapport beschikbaar voor evaluatie van de batchtaakhistorie.
    * Als u de factuur wilt afdrukken, stelt u de optie in op **Ja**.
    * Als u de factuur wilt boeken, stelt u de optie in op **Ja**. U kunt de factuur afdrukken zonder deze te boeken.

19. Selecteer **OK**.

## <a name="copy-lines"></a>Regels kopiëren
Als u regels in een vrije-tekstfactuur wilt kopiëren, selecteert u een of meer regels en selecteert u vervolgens **Geselecteerde regels kopiëren**. U kunt opgeven hoeveel kopieën u wilt maken en u kunt ook notities en bijlagen kopiëren. U kunt de verdelingen kopiëren of opnieuw laten maken wanneer u boekt.

Nadat u de regels hebt gekopieerd, kunt u de gegevens zo nodig bewerken.

## <a name="create-a-free-text-invoice-from-a-template"></a>Een vrije-tekstfactuur maken op basis van een sjabloon
U kunt een vrije-tekstfactuur maken op basis van een sjabloon. Wanneer u **Nieuw van sjabloon** op het tabblad **Factuur** selecteert, kunt u een sjabloonnaam en de klantrekening voor de nieuwe vrije-tekstfactuur selecteren. Standaardwaarden, zoals de betalingsvoorwaarden en betalingsmethode, kunnen automatisch van de klant worden overgenomen, of u kunt de waarden gebruiken die zijn opgeslagen in de sjabloon.

Er wordt een nieuwe vrije-tekstfactuur gemaakt en u kunt de waarden indien nodig bewerken.

## <a name="resetting-the-workflow-status-for-free-text-invoices-from-unrecoverable-to-draft"></a>De werkstroomstatus van vrije-tekstfacturen wordt opnieuw ingesteld van Onherstelbaar op Concept
Een workflowexemplaar dat is gestopt vanwege een onherstelbare fout, heeft een workflowstatus **Onherstelbaar**. Wanneer de status van een werkstroom voor vrije-tekstfacturen van klanten **Onherstelbaar** is, kunt u deze weer instellen op **Concept** door **Intrekken** te selecteren in de werkstroomacties. U kunt vervolgens de vrije-tekstfactuur van de klant bewerken. Deze functie is beschikbaar als de parameter **De workflowstatus voor vrije-tekstfacturen van Onherstelbaar wijzigen in Concept** op de pagina **Functiebeheer** is ingeschakeld.

U kunt de pagina **Workflowhistorie** voor leveranciersfacturen gebruiken om de workflowstatus in te stellen op **Concept**. U kunt deze pagina openen vanuit **Vrije-tekstfactuur** of via **Algemeen > Query's > Werkstroom**. Als u de workflowstatus terug wilt zetten op **Concept**, selecteert u **Intrekken**. U kunt de werkstroomstatus ook terugzetten op **Concept** door de actie **Intrekken** te selecteren op de pagina **Vrije-tekstfactuur** of **Alle vrije-tekstfacturen**. Als de workflowstatus is ingesteld op **Concept**, wordt deze beschikbaar voor bewerking op de pagina **Vrije-tekstfactuur**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
