---
title: Werkgebied voor oplossing Invoice Capture
description: Dit artikel biedt informatie over het werkgebied voor de oplossing Invoice Capture.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4f3af7abf94542437be6132344d6bb7ffaf33d07
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691154"
---
# <a name="invoice-capture-solution-workspace"></a>Werkgebied voor oplossing Invoice Capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="side-by-side-viewer-for-the-invoice-capture-solution"></a>Viewer voor het naast elkaar weergeven van documenten voor de oplossing Invoice Capture

Het invoeren van facturen in het systeem is doorgaans een tijdrovend proces dat bovendien foutgevoelig is omdat medewerkers door meerdere bijlagebestanden en vensters moet navigeren om de juiste informatie te verzamelen. De viewer voor het naast elkaar weergeven van documenten verbetert uw ervaring bij het werken aan facturen door het proces eenvoudiger, efficiënter en nauwkeuriger te maken.

Met deze viewer kunnen gebruikers het oorspronkelijke document en de factuur naast elkaar in hetzelfde venster openen. De factuurpagina wordt gevuld met informatie uit het oorspronkelijke factuurdocument. De viewer maakt de verbinding tussen de velden van de factuurpagina en het oorspronkelijke factuurdocument. Daarnaast kunnen gebruikers met de viewer zoeken naar fouten op de factuurpagina.

### <a name="open-the-side-by-side-viewer"></a>De viewer voor het naast elkaar weergeven van documenten openen

In Microsoft Dynamics 365 Finance kunt u deze viewer openen vanuit de lijst op de overzichtspagina of vanuit de factuurlijstpagina. U kunt deze ook openen door te dubbeltikken of -klikken op een record of door het factuurnummer te selecteren.

### <a name="using-the-side-by-side-viewer"></a>De viewer voor het naast elkaar weergeven van documenten gebruiken

#### <a name="manually-review-an-invoice"></a>Een factuur handmatig controleren

Een factuurdocument dat is geïmporteerd, moet u mogelijk handmatig controleren vanwege fouten of waarschuwingen. In de viewer voor naast elkaar weergeven wordt voor de documentkoptekst de status **Geïmporteerd** weergegeven en de huidige versie is **Oorspronkelijke versie**.

Selecteer **Controle starten** om de factuur te controleren. Alle velden kunnen worden bewerkt. Het veld **Status** wordt bijgewerkt naar **Wordt gecontroleerd** en het veld **Huidige versie** wordt bijgewerkt naar **Gewijzigd versie**.

#### <a name="view-and-work-with-messages"></a>Berichten weergeven en ermee werken

Gebruikers moeten het controleproces starten vanuit het berichtvenster. Foutberichten worden aangeduid met een rode X, waarschuwingsberichten worden aangeduid met een driehoek en informatieve berichten worden met een cirkel aangeduid. Berichten met betrekking tot de betrouwbaarheidsscore kunnen worden geclassificeerd als waarschuwingen of fouten, afhankelijk van de drempelwaarde die is ingesteld door de configuratiegroep. Zie [Configuratiegroepen voor de oplossing Invoice Capture](invoice-capture-config-group.md) voor meer informatie.

Waarschuwings- en foutberichten kunnen worden genegeerd vanuit het berichtvenster, de factuurkoptekst of factuurregels. Wanneer een bericht wordt genegeerd, verschijnt deze niet meer als een fout of waarschuwing en mislukt de validatie van de factuur niet.

- Selecteer **Negeren** als u berichten in het berichtenvenster wilt negeren. Als u een genegeerd bericht opnieuw wilt instellen, selecteert u opnieuw **Negeren**. Het type van de fout of waarschuwing wordt vervolgens gewijzigd in informatie.
- Als u berichten vanuit de factuurkop of factuurregel wilt negeren, selecteert u **Negeren** in het veld. Het berichtsymbool verdwijnt. Dit wordt echter opnieuw weergegeven als het bericht opnieuw wordt ingesteld vanuit het berichtenvenster.

Bij berichten die betrekking hebben op factuurkoptekstvelden wordt de cursor, wanneer u het bericht selecteert in het berichtvenster, verplaatst naar het overeenkomstige veld in de koptekstsectie.

#### <a name="proofread-and-edit-fields"></a>Velden proeflezen en bewerken

Als de waarde van een veld vanuit de oorspronkelijke factuur via Optical Character Recognition (OCR) wordt gelezen, verschijnt er een symbool voor het veld. Als u het symbool selecteert, zoomt de documentviewer in en wordt de plaats gemarkeerd waar de veldwaarde wordt gelezen, zodat u factuurgegevens kunt controleren.

Als u de documentviewer weer wilt instellen op de oorspronkelijke vergroting, volgt u een van deze stappen:

- Selecteer hetzelfde symbool als u eerder hebt geselecteerd.
- Selecteer de knop in de rechterbovenhoek van de documentviewer.

Bewerk de velden waar nodig. Bewerkingen worden automatisch opgeslagen als de cursor een veld verlaat. Een symbool rechts van een veld geeft aan dat het veld handmatig is bijgewerkt. Wanneer de pagina wordt vernieuwd, wordt het symbool verwijderd.

#### <a name="check-an-invoice-to-get-up-to-date-messages"></a>Een factuur controleren om up-to-date berichten op te halen

Wanneer u een veld bewerkt, wordt de veldwaarde bijgewerkt, maar worden er geen nieuwe validatieberichten gegenereerd. Selecteer **Controleren** om up-to-date validatieberichten op te halen. De berichten in het berichtvenster, in de factuurkoptekst en op de factuurregels worden bijgewerkt.

#### <a name="complete-the-review"></a>De controle voltooien

Als u de controle wilt voltooien, selecteert u **Controle voltooien**. De facturen worden gevalideerd. Als er fouten worden gevonden, blijft de documentstatus **Wordt gecontroleerd** en wordt er een berichtbalk weergegeven. Alle berichten in het berichtvenster en de factuurkoptekst en -regels worden automatisch bijgewerkt om informatie over de oorzaken van de mislukte validatie te bieden.

Nadat alle blokkeringsfouten zijn opgelost, kan de controle worden voltooid. De documentstatus wordt bijgewerkt naar **Gecontroleerd** en de velden kunnen niet meer worden bewerkt. U kunt de controle opnieuw starten door **Controle starten** opnieuw te selecteren.

#### <a name="generate-a-pending-vendor-invoice-in-finance"></a>Een leveranciersfactuur in behandeling in Finance genereren

Als u het factuurdocument naar de verbonden Finance-omgeving wilt verzenden, selecteert u **Genereren**. Als het genereren van facturen mislukt, verschijnt er een foutbericht op een berichtbalk.

#### <a name="void-an-invoice"></a>Een factuur ongeldig maken

Als u een factuur ongeldig wilt maken, selecteert u **Ongeldig maken**. Ongeldig gemaakte facturen kunnen niet worden gecontroleerd en worden niet weergegeven in de lijst **Facturen moeten handmatig worden gecontroleerd**.

### <a name="validation-logic"></a>Validatielogica

Sommige belangrijke velden in de viewer voor het naast elkaar weergeven van documenten bestaan niet in de faseringsgegevens van de factuur, maar zijn vereist om facturen in behandeling te genereren in Finance. Deze velden worden afgeleid van een combinatie van de huidige factuurfaseringsgegevens en hoofdgegevens uit Finance.

De velden die moeten worden afgeleid, zijn **Rechtspersoon**, **Leverancierrekening** en **Artikelnummer**. Deze moeten in de volgende volgorde worden afgeleid. Als de afleiding van een veld mislukt, wordt het proces gestopt.

1. **Rechtspersoon**: de rechtspersoon wordt als eerste afgeleid. Als een actieve toewijzingsregel wordt gevonden voor de rechtspersoon, wordt de rechtspersoon afgeleid op basis van de bedrijfsnaam en het bedrijfsadres.
2. **Leverancierrekening**: vervolgens wordt de leverancierrekening afgeleid op basis van een actieve toewijzingsregel en een combinatie van de afgeleide rechtspersoon en de naam en het adres van de leverancier.
3. **Artikelnummer**: ten slotte wordt de artikelnaam afgeleid van de fasering, gebaseerd op de volgende drie typen informatie:

    - Een geconfigureerde toewijzingsregel
    - Een afgeleide rechtspersoon
    - De afgeleide leverancierrekening

Als u een validatie wilt uitvoeren, selecteert u **Controleren** in de viewer. Momenteel worden tijdens de validatie de volgende controles uitgevoerd:

- **Verplichte controle**: met deze controle worden de verplichte velden gevalideerd voor de viewer voor naast elkaar weergeven. Gebruikers kunnen op de pagina **Configuratie-instellingen** de velden selecteren die verplicht moeten zijn.
- **Betrouwbaarheidsscore**: gebruikers kunnen de waarschuwings- en foutdrempel voor de betrouwbaarheidsscore instellen. Bij deze controle wordt gekeken naar de betrouwbaarheidsscore van OCR die onder deze drempels ligt. Fout- of waarschuwingsberichten worden weergegeven op basis van het validatieresultaat.
- **Rechtspersoon**: hiermee wordt gevalideerd of een rechtspersoon zich in Financiën bevindt. Als de rechtspersoon niet bestaat in de Finance-omgeving, mislukt de validatie.

Wanneer de viewer voor naast elkaar weergeven voor het eerst wordt gebruikt en de gebruiker **Controleren** selecteert, worden de afleidings- en validatieprocessen uitgevoerd. Als de facturen kloppen, wordt het validatieproces uitgevoerd wanneer de gebruiker **Volledige controle** selecteert. Deze wordt ook uitgevoerd als de gebruiker **Leveranciersfactuur genereren** selecteert.

Het afleidingsproces vindt plaats vóór het validatieproces en alle waarschuwingen of fouten zijn afkomstig uit het validatieproces. De waarschuwingen en fouten worden vastgelegd in Finance.
