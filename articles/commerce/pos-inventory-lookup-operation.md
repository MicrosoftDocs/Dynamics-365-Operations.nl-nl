---
title: Voorraadzoekbewerking in POS
description: In dit onderwerp wordt beschreven hoe u de voorraadzoekbewerking in POS (Point of Sale) kunt gebruiken in Dynamics 365 Commerce om de beschikbaarheid van voorhanden voorraad van producten in winkels en magazijnen weer te geven.
author: boycezhu
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.openlocfilehash: 873c6413c14d2ee8315c149ee9c495bb59dbd930
ms.sourcegitcommit: 11ca5863175150b6c39f47a9322caa2186727a26
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025443"
---
# <a name="inventory-lookup-operation-in-pos"></a>Voorraadzoekbewerking in POS

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u de voorraadzoekbewerking in POS (Point of Sale) kunt gebruiken in Dynamics 365 Commerce om de beschikbaarheid van voorhanden voorraad van producten in winkels en magazijnen weer te geven.

Een nauwkeurige weergave van de voorraad binnen een organisatie helpt het winkelpersoneel om op tijd een effectieve klantenservice te bieden. Het moment dat er het meest toe doet, is het tijdstip waarop een klant is gereed om een aankoopbeslissing te nemen. Het is belangrijk dat kassamedewerkers in de detailhandel realtime of bijna realtime voorraadinformatie bij de hand hebben zodat ze correct een levering van producten kunnen beloven.

De voorraadzoekbewerking in Commerce POS helpt detailhandelaren operationele successen te behalen en inzichten te verkrijgen door winkels te koppelen aan het hoofdkantoor van Commerce. Deze functionaliteit biedt een voorraadbeschikbaarheidsweergave van producten in winkels en magazijnen. Het helpt detailhandelaren ook om de efficiëntie te vergroten en kosten te besparen door de voorraadplanning in realtime te verbeteren.

Wanneer de voorraadzoekbewerking wordt gestart vanuit de POS-toepassing, gebruikt de POS-kassamedewerker het numerieke toetsenbord om een productnummer in te voeren om de voorraadgegevens op te vragen. Als het ingevoerde product varianten heeft, kan de kassamedewerker optioneel dimensies of andere waarden selecteren om voorraadgegevens van een specifieke productvariant te controleren.

## <a name="inventory-lookup-list-view-for-individual-products"></a>Lijstweergave van Zoeken in voorraad voor afzonderlijke producten

Voor een afzonderlijk product biedt de voorraadzoekbewerking een voorraadzoeklijstweergave met de volgende productinformatie voor een lijst met locaties:

- **Voorraad**: verwijst naar de 'beschikbare fysieke' hoeveelheid van een product.
- **Gereserveerd**: verwijst naar de 'fysieke gereserveerde' hoeveelheid die is opgehaald van het hoofdkantoor.
- **Besteld**: verwijst naar de 'in totaal bestelde' hoeveelheid die is opgehaald van het hoofdkantoor.
- **Eenheid** : verwijst naar de voorraadmaateenheid die is geconfigureerd in het hoofdkantoor.

De lijstweergave met locaties bevat alle winkels en magazijnen die zijn geconfigureerd in de afhandelingsgroepen waaraan de huidige winkel is gekoppeld, zoals wordt weergegeven in de volgende voorbeeldafbeelding.

![Lijstweergave van voorraadzoekbewerking](media/inventory-lookup-list-view.png)

De volgende acties zijn beschikbaar op de appbalk in POS:

- **Sorteren**: met deze actie kan de POS-gebruiker de gegevens in de lijstweergave sorteren op basis van verschillende criteria. Sorteren op basis van locatie is de standaardsorteeroptie. 
  - **Geografische locatie** (van de dichtstbijzijnde locatie naar de verste locatie, vergeleken met de huidige winkel)
  - **Naam** (in oplopende of aflopende volgorde)
  - **Winkelnummer** (in oplopende of aflopende volgorde)
  - **Voorraad** (in aflopende volgorde)
  - **Gereserveerd** (in aflopende volgorde)
  - **Besteld** (in aflopende volgorde)
- **Filteren**: met deze actie kan de POS-gebruiker gefilterde gegevens voor een specifieke locatie bekijken.
- **Beschikbaarheid van winkel weergeven**: met deze actie kan de POS-gebruiker de ATP-hoeveelheden (Available To Promise) voor een product in de geselecteerde winkel bekijken.
- **Winkellocatie weergeven**: met deze actie wordt een afzonderlijke pagina geopend om de kaartweergave, het adres en de openingstijden voor de geselecteerde winkel weer te geven.
- **Ophalen in winkel**: met deze actie wordt een klantorder gemaakt voor het product dat wordt opgehaald bij de geselecteerde winkel en wordt de gebruiker doorgestuurd naar het transactiescherm.
- **Product verzenden**: met deze actie wordt een klantorder gemaakt voor het product dat wordt verzonden vanuit de geselecteerde winkel en wordt de gebruiker doorgestuurd naar het transactiescherm.
- **Alle varianten weergeven**: voor een product met varianten wordt met deze actie overgeschakeld van een lijstweergave naar een matrixweergave waarin voorraadgegevens voor alle varianten van het product worden weergegeven.
- **Toevoegen aan transactie**: met deze actie wordt het product aan de winkelwagen toegevoegd en wordt de gebruiker doorgestuurd naar het transactiescherm.

> [!NOTE]
> Voor een locatiegebaseerde sortering wordt de afstand tussen een locatie en de huidige winkel bepaald door de coördinaten (breedte- en lengtegraad) die zijn gedefinieerd in het hoofdkantoor van Commerce. Voor een winkel worden de locatiegegevens gedefinieerd in het primaire adres van de operationele eenheid die aan de winkel is gekoppeld. Voor een niet-magazijn worden de locatiegegevens gedefinieerd in het magazijnadres. Als voor de huidige winkel geen coördinaten correct zijn gedefinieerd, wordt met de sorteeroptie op locatie de huidige winkel boven aan de lijst weergegeven en worden andere locaties vervolgens op naam gesorteerd.

> [!NOTE]
> De acties **Beschikbaarheid van winkel weergeven**, **Winkellocatie weergeven**, **Ophalen in winkel** en **Product verzenden** zijn niet beschikbaar voor niet-winkellocaties.

## <a name="inventory-lookup-matrix-view-for-variants"></a>Matrixweergave voor varianten in voorraad zoeken

Voor een hoofdproduct met varianten biedt de voorraadzoekbewerking ook een op dimensies gebaseerde matrixweergave waarin voorraadbeschikbaarheidsinformatie wordt weergegeven voor alle varianten van het hoofdproduct op een geselecteerde locatie. Standaard worden in de matrixweergave gegevens getoond voor de huidige winkel. U kunt de actie **Winkel** op de app-balk gebruiken om voorraadgegevens te zoeken in andere winkels die zijn geconfigureerd in de afhandelingsgroepen waaraan de huidige winkel is gekoppeld.

In de volgende voorbeeldafbeelding ziet u de matrixweergave voor voorraad zoeken in POS.

![Matrixweergave van voorraadzoekbewerking](media/inventory-lookup-matrix-view.png)

In de matrixweergave vertegenwoordigt elke cel een afzonderlijke variant en wordt een voorhanden voorraadwaarde (fysiek beschikbaar) weergegeven in de rechterbenedenhoek, evenals de waarden **gereserveerd** (fysiek gereserveerd) en **besteld** (in totaal besteld) in de linkerbovenhoek. De volgende tabel beschrijft de betekenis van de verschillende waarden voor voorhanden voorraad.

| Waarde voorhanden voorraad                            | Beschrijving |
|------------------------------------------|-------------|
| Numerieke waarde die groter is dan 0 (nul) | Een variant is vrijgegeven voor de geselecteerde locatie en u kunt aanvullende acties uitvoeren in de cel. |
| **0** (nul)                             | Een variant is vrijgegeven voor de geselecteerde locatie, maar het artikel is niet beschikbaar op de geselecteerde locatie. U kunt aanvullende acties uitvoeren in de cel. |
| **n.v.t.** of een niet-actieve cel              | Een variant is niet vrijgegeven voor de geselecteerde locatie en u kunt geen aanvullende acties uitvoeren in de cel. |

De weergavevolgorde van de dimensiewaarden in de matrixweergave is gebaseerd op de configuratie van de dimensieweergaveorder in het hoofdkantoor van Commerce. U kunt de configuratie van de dimensieweergavevolgorde wijzigen door een nieuwe dimensie te selecteren die u wilt gebruiken. 

De volgende acties zijn beschikbaar in matrixweergavecel:

- **Nu verkopen**: met deze actie wordt de geselecteerde variant aan de winkelwagen toegevoegd en wordt de gebruiker doorgestuurd naar het transactiescherm.
- **Ophalen in winkel**: met deze actie wordt een klantorder gemaakt voor de geselecteerde variant die wordt opgehaald bij de geselecteerde winkel en wordt de gebruiker doorgestuurd naar het transactiescherm.
- **Product verzenden**: met deze actie wordt een klantorder gemaakt voor de geselecteerde variant die wordt verzonden vanuit de geselecteerde winkel en wordt de gebruiker doorgestuurd naar het transactiescherm.
- **Beschikbaarheid:**: met deze actie wordt de gebruiker naar een afzonderlijke pagina geleid met de ATP-hoeveelheden voor de geselecteerde variant in de geselecteerde winkel.
- **Alle locaties weergeven**: met deze actie wordt overgeschakeld naar de lijstweergave voor beschikbare standaardvoorraad met de voorraadgegevens voor de geselecteerde variant.
- **Productgegevens weergeven**: met deze actie wordt de gebruiker doorgestuurd naar de pagina met productgegevens (PDP, product details page) van de geselecteerde variant.

## <a name="access-inventory-lookup-from-other-pages-in-pos"></a>Toegang tot voorraad zoeken vanuit andere pagina's in POS

POS-gebruikers hebben toegang tot de voorraadzoekbewerking vanuit andere pagina's in POS.

In de volgende voorbeeldafbeelding ziet u de resultaten van voorraad zoeken vanuit een pagina met productgegevens in POS.

![Voorraad zoeken vanaf de pagina met productgegevens](media/inventory-lookup-from-product-details-page.png)

In de pagina met productgegevens van een hoofdproduct kunt u de actie **Alle varianten weergeven** op de appbalk gebruiken om de matrixweergave voor voorraad zoeken te starten waarin voorraadbeschikbaarheidsinformatie voor de huidige winkel voor alle varianten van een product wordt weergegeven. Voor een afzonderlijk product geeft de pagina met productgegevens de voorhanden-voorraadwaarde (fysiek beschikbaar) van dat product voor de huidige winkel weer. Daarnaast kunt u de koppeling **Voorraad overige winkels** selecteren om de voorraadzoekbewerking te starten om de voorraadbeschikbaarheid van een product in andere winkels of magazijnen te controleren.

> [!NOTE]
> De actie **Alle varianten weergeven** op de pagina met productgegevens is alleen beschikbaar voor hoofdproducten met varianten. De actie is niet beschikbaar voor specifieke producten of kits.

U kunt de voorraadzoekbewerking configureren om te worden weergegeven als een koppeling in het knoppenraster op het POS-transactiescherm. Wanneer de gebruiker na de configuratie een winkelwagenregel selecteert en vervolgens de knop **Zoeken in voorraad** selecteert, wordt de lijstweergave voor voorraad zoeken voor het geselecteerde product weergegeven. Zie [Weergaveconfiguraties van POS-gebruikersinterface](pos-screen-layouts.md) voor meer informatie over het configureren van knoppenrasters met behulp van de POS-schermindelingsontwerper.

## <a name="inventory-lookup-with-channel-side-calculation"></a>Voorraad zoeken met berekening aan kanaalzijde

In Commerce release 10.0.9 en eerder wordt de waarde **fysiek beschikbaar** in de voorraadzoekbewerking opgehaald van het hoofdkantoor van Commerce via een realtime serviceoproep. In Commerce release 10.0.10 en hoger kunt u de POS-voorraadzoekbewerking configureren om berekening aan kanaalzijde op de Commerce-server te gebruiken om de waarde van de fysiek beschikbare voorraad te bepalen. Deze kan een betrouwbaardere en nauwkeurigere schatting geven van de voorhanden voorraad door rekening te houden met de transactiegegevens die nog niet zijn gesynchroniseerd met het hoofdkantoor. Zie [Voorraadbeschikbaarheid voor Retail-kanalen berekenen](calculated-inventory-retail-channels.md) voor meer informatie over voorraadberekening aan kanaalzijde en gerelateerde POS-configuratie in het hoofdkantoor.

## <a name="additional-resources"></a>Aanvullende bronnen

[Weergaveconfiguraties van POS-gebruikersinterface](pos-screen-layouts.md)

[Voorraadbeschikbaarheid voor Retail-kanalen berekenen](calculated-inventory-retail-channels.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
