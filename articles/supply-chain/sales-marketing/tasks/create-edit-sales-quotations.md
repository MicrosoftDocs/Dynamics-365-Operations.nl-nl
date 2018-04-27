--- 
title: Verkoopoffertes maken en bewerken
description: Deze procedure toont hoe u een verkoopofferte maakt en bijwerkt.
author: omulvad
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8e7d2198b4976a6f60f05690d7b6f11f3da55e28
ms.openlocfilehash: 7ffa4fe8d87db5b3f8293ec9dbc042496d09d6e3
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---
# <a name="create-and-edit-sales-quotations"></a>Verkoopoffertes maken en bewerken

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure toont hoe u een verkoopofferte maakt en bijwerkt. U kunt deze procedure uitvoeren met uw eigen gegevens of in het demogegevensbedrijf USMF.


## <a name="create-a-sales-quotation"></a>Een verkoopofferte maken
1. Ga naar Verkoop en marketing > Verkoopoffertes > Alle offertes.
2. Klik op Nieuw.
3. Selecteer 'Prospect' in het veld Bankrekening.
4. Typ of selecteer een waarde in het veld Prospect.
5. Vouw de sectie Algemeen uit.
    * Omdat u ervoor koos om een offerte te maken vanuit het gebied Verkoop en marketing, wordt het type automatisch ingesteld op Verkoopofferte. Om een offerte voor een project te maken, moet u deze openen vanuit de module Projectbeheer en boekhouding.   
6. Klik op OK.
    * De velden en acties op de offerteregels zijn vergelijkbaar met deze op de verkooporderregels.   Net als verkooporders kunnen de offertes voor een specifiek artikel wordt gemaakt of, wanneer het artikelnummer niet bekend is of niet bestaat op het moment waarop de offerte wordt gemaakt, kunnen offertes voor een verkoopcategorie worden gemaakt.  
7. Typ of selecteer een waarde in het veld Artikel.
8. Typ een waarde in het veld Artikel.
9. Sluit de pagina.
10. Voer in het veld Hoeveelheid een getal in.
    * Als er geldige handelsovereenkomsten zijn voor het geselecteerde artikel op de regel, worden de toepasselijke prijs en kortingen automatisch gekopieerd naar de offerteregel. Zorg ervoor dat het veld Eenheidsprijs een waarde bevat en u ook kortingwaarden kunt invoeren als u dat wilt.  
11. Klik op Opslaan.
12. Klik in het actievenster op Verkoopofferte.
13. Klik op Totalen.
14. Klik op OK.
15. Klik op Verkoopofferteregel.
16. Klik op Prijzen.
    * Op de pagina Prijssimulatie uitvoeren kunt u experimenteren bij het aanpassen van de verwachte omzet of rentabiliteit van uw offerte op basis van de gewenste eenheidsprijzen, kortingsbedragen, kortingspercentages, totale bedragen, marges of bijdrageverhoudingen.   Wanneer u tevreden bent met de streefcijfers, past u de suggestie op de offerteregel toe. De prijsgerelateerde velden worden overeenkomstig bijgewerkt.  
    * U kunt zoveel prijssimulaties maken als u nodig hebt. Wanneer u op Nieuw klikt, worden de prijscoorwaarden van de huidige offerteregel gekopieerd naar de pagina. U kunt dan in alle prijsgerelateerde velden waarden wijzigen in de doelwaarden. Door een wijziging in een van de velden worden alle andere velden herberekend. Opdat het systeem de verkoopmarge en bijdrageverhouding berekent, moeten de eenheidskosten van het product bekend zijn. Gebruik het tabblad Gesimuleerde prijzen voor een gedetailleerde weergave van de oorspronkelijke prijzen, de voorgestelde wijzigingen en hun effect op de totalen van de offerte.   In het algemeen geldt dat als een simulatie die een nieuw bedrag instelt wordt toegepast op de offerteregel, het systeem een nieuwe waarde berekent en invoert in het veld Eenheidsprijs. Als de simulatie is gebaseerd op een nieuwe marge of een nieuwe bijdrageverhouding, wordt alleen het veld Nettobedrag bijgewerkt en is de Eenheidsprijs leeg. In beide gevallen worden eventuele kortingen verwijderd die vóór de simulatie op de offerteregel waren toegepast.  
17. Sluit de pagina.
18. Klik in het actievenster op Offecte.
19. Klik op Offerte verzenden.
20. Selecteer Ja in het veld Offerte afdrukken.
21. Klik op OK.
    * Het kan enkele minuten duren om het rapport te genereren. Sluit de pagina niet voor dit is gebeurd.  
22. Sluit de pagina.

## <a name="update-a-sales-quotation"></a>Een verkoopofferte bijwerken
1. Klik in het actievenster op Opvolgen.
2. Klik op Omzetten in klant.
3. Typ een waarde in het veld Klantrekening.
4. Klik op Controleren.
    * Zorg ervoor u een bericht zeit dat het rekeningnummer dat u typte vrij is voor gebruik.  
5. Klik op OK.
    * Het systeem heeft nu een nieuwe klantrekening gemaakt voor de prospect op de offerte.  
6. Sluit de pagina.
7. Klik in het actievenster op Opvolgen.
8. Klik op Bevestigen.
9. Typ of selecteer een waarde in het veld Reden.
10. Klik op OK.
11. Klik in het actievenster op Algemeen.
12. Klik op Verkooporders.
13. Sluit de pagina.


