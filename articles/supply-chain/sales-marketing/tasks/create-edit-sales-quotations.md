---
title: Verkoopoffertes maken en bewerken
description: Deze procedure toont hoe u een verkoopofferte maakt en bijwerkt.
author: omulvad
manager: tfehr
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SalesQuotationTotals, SalesQuotationPriceSimulation, SalesQuotationEditLines, SrsReportViewerForm, smmSetNumSeqIfManual, CustTable, SalesTable, CustQuotationConfirmationJournal, CustQuotationJournal, CustSalesLines, SalesQuotationCopying, SalesQuotationDeleteQuotations, SalesQuotationListPagePreviewPane, SalesQuotationTypeGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 73c15b41a4b0979ec79c8dbd8d88627bffcf6ed3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425249"
---
# <a name="create-and-edit-sales-quotations"></a>Verkoopoffertes maken en bewerken

[!include [banner](../../includes/banner.md)]

Deze procedure toont hoe u een verkoopofferte maakt en bijwerkt. U kunt deze procedure uitvoeren met uw eigen gegevens of in het demogegevensbedrijf USMF.


## <a name="create-a-sales-quotation"></a>Een verkoopofferte maken
1. Ga naar **Navigatievenster > Modules > Verkoop en marketing > Verkoopoffertes > Alle offertes**.
2. Klik op **Nieuw**.
3. Selecteer 'Prospect' in het veld **Rekeningtype**.
4. Typ of selecteer een waarde in het veld **Prospect**.
5. Vouw de sectie **Algemeen** uit. Omdat u ervoor koos om een offerte te maken vanuit het gebied Verkoop en marketing, wordt het type automatisch ingesteld op 'Verkoopofferte'. Om een offerte voor een project te maken, moet u deze openen vanuit de module **Projectbeheer en boekhouding**.
6. Klik op **OK**. De velden en acties op de offerteregels zijn vergelijkbaar met deze op de verkooporderregels.   Net als verkooporders kunnen de offertes voor een specifiek artikel wordt gemaakt of, wanneer het artikelnummer niet bekend is of niet bestaat op het moment waarop de offerte wordt gemaakt, kunnen offertes voor een verkoopcategorie worden gemaakt.     
7. Typ of selecteer een waarde in het veld **Artikel**.
8. Typ een waarde in het veld **Locatie**.
9. Voer een getal in het veld **Hoeveelheid** in. Als er geldige handelsovereenkomsten zijn voor het geselecteerde artikel op de regel, worden de toepasselijke prijs en kortingen automatisch gekopieerd naar de offerteregel. Zorg ervoor dat het veld Eenheidsprijs een waarde bevat en u ook kortingwaarden kunt invoeren als u dat wilt. 
10. Klik op **Opslaan**.
11. Klik in het **actievenster** op **Verkoopofferte**.
12. Klik op **Totalen**.
13. Klik op **OK**.
14. Selecteer de verkoopofferteregel.
15. Klik in het **actievenster** op **Offerte**.
16. Klik op **Prijssimulatie**.
    - Op de pagina **Prijssimulatie uitvoeren** kunt u experimenteren bij het aanpassen van de verwachte omzet of rentabiliteit van uw offerte op basis van de gewenste eenheidsprijzen, kortingsbedragen, kortingspercentages, totale bedragen, marges of bijdrageverhoudingen. Wanneer u tevreden bent met de streefcijfers, past u de suggestie op de offerteregel toe. De prijsgerelateerde velden worden overeenkomstig bijgewerkt.  
    - U kunt zoveel prijssimulaties maken als u nodig hebt. Wanneer u op **Nieuw** klikt, worden de prijsvoorwaarden van de huidige offerteregel gekopieerd naar de pagina. U kunt dan in alle prijsgerelateerde velden waarden wijzigen in de doelwaarden. Door een wijziging in een van de velden worden alle andere velden herberekend. Opdat het systeem de verkoopmarge en bijdrageverhouding berekent, moeten de eenheidskosten van het product bekend zijn. Gebruik het tabblad Gesimuleerde prijzen voor een gedetailleerde weergave van de oorspronkelijke prijzen, de voorgestelde wijzigingen en hun effect op de totalen van de offerte. In het algemeen geldt dat als een simulatie die een nieuw bedrag instelt wordt toegepast op de offerteregel, het systeem een nieuwe waarde berekent en invoert in het veld Eenheidsprijs. Als de simulatie is gebaseerd op een nieuwe marge of een nieuwe bijdrageverhouding, wordt alleen het veld Nettobedrag bijgewerkt en is de Eenheidsprijs leeg. In beide gevallen worden eventuele kortingen verwijderd die vóór de simulatie op de offerteregel waren toegepast.
17. Klik in het **actievenster** op **Offerte**.
18. Klik op **Offerte verzenden**.
19. Selecteer 'Ja' in het veld **Offerte afdrukken**.
20. Klik op **OK**. Het kan enkele minuten duren om het rapport te genereren. Sluit de pagina niet voor dit is gebeurd.

## <a name="update-a-sales-quotation"></a>Een verkoopofferte bijwerken
1. Ga naar **Navigatievenster > Modules > Verkoop en marketing > Verkoopoffertes > Alle offertes**.
2. Klik in het **actievenster** op **Opvolgen**.
3. Klik op **Omzetten in klant**.
4. Typ een waarde in het veld **Klantrekening**.
5. Klik op **Controleren**. Zorg ervoor u een bericht zeit dat het rekeningnummer dat u typte vrij is voor gebruik.  
6. Klik op **OK**. Het systeem heeft nu een nieuwe klantrekening gemaakt voor de prospect op de offerte.  
7. Sluit de pagina.
8. Klik in het **actievenster** op **Opvolgen**.
9. Klik op **Bevestigen**.
10. Typ of selecteer een waarde in het veld **Reden**.
11. Klik op **OK**.
12. Klik in het **actievenster** op **Algemeen**.
13. Klik op **Verkooporders**.
14. Sluit de pagina.

