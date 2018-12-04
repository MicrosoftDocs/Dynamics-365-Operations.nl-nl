--- 
title: "Behoefteplanningsregels voor artikelen definiëren"
description: Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 14f56c30753da9458d66a46da8935305619fd0b8
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="define-coverage-rules-for-items"></a>Behoefteplanningsregels voor artikelen definiëren

[!include [task guide banner](../../includes/task-guide-banner.md)]

Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. Deze procedure toont hoe u behoefteplanningsregels maakt en behoefteplanningsinstellingen voor een specifiek artikel overschrijft. Het toont ook hoe u standaardvoorraadinstellingen opgeeft.


## <a name="create-a-coverage-group"></a>Een behoefteplanningsgroep maken
1. Ga naar Behoefteplanningsgroepen.
2. Klik op Nieuw.
3. Typ een waarde in het veld Dekkingsgroep.
4. Typ een waarde in het veld Naam.
5. Typ een waarde in het veld Agenda.
    * Kies de agenda die tijdens hoofdplanning wordt gebruikt om aanvullingssuggesties te doen voor artikelen in deze groep.  
6. Selecteer een optie in het veld Bestelmethode.
    * Selecteer Vereisten voor deze procedure.  
7. Voer 90 in het veld Time fence dekking (dagen) in.
    * Voor artikelen in deze groep maakt de hoofdplanning aanvullingssuggesties tot maximaal 90 dagen in de toekomst.  
8. Voer 1 in het veld Negatieve dagen in.
9. Voer 1 in het veld Positieve dagen in.
10. Vouw de sectie Overige uit of samen.
11. Typ 1 in het veld Ontvangstmarge opgeteld bij behoeftedatum.
    * Als bijvoorbeeld de ontvangstmarge is ingesteld op 1 dag en een inkooporderregel is gepland voor ontvangst op 15 mei, berekent de hoofdplanning de aangepaste ontvangstdatum als 16 mei.  
12. Typ 1 in het veld Uitgiftemarge afgetrokken van behoeftedatum.
    * Als bijvoorbeeld de veiligheidsmarge is ingesteld op 1 dag en een verkooporderregel is gepland voor levering op 15 mei, berekent de hoofdplanning de aangepaste leveringsdatum als 14 mei.  
13. Typ 1 in het veld Bestelmarge opgeteld bij doorlooptijd van artikel.
14. Klik op Opslaan.

## <a name="create-a-new-product"></a>Een nieuw product maken
1. Ga naar Vrijgegeven producten.
2. Klik op Nieuw.
3. Typ een waarde in het veld Productnummer.
4. Typ een waarde in het veld Productnaam.
5. Klik in het veld Artikelmodelgroep op de vervolgkeuzeknop om de zoekopdracht te openen.
6. Zoek en selecteer het gewenste record in de lijst.
7. Klik in de lijst op de koppeling in de geselecteerde rij.
8. Klik in het veld Artikelgroep op de vervolgkeuzeknop om de zoekopdracht te openen.
9. Zoek en selecteer het gewenste record in de lijst.
10. Klik in de lijst op de koppeling in de geselecteerde rij.
11. Klik in het veld Opslagdimensiegroep op de vervolgkeuzeknop om de zoekopdracht te openen.
12. Zoek en selecteer het gewenste record in de lijst.
13. Klik in de lijst op de koppeling in de geselecteerde rij.
14. Klik in het veld Traceringsdimensiegroep op de vervolgkeuzeknop om de zoekopdracht te openen.
15. Zoek en selecteer de gewenste record in de lijst.
16. Klik in de lijst op de koppeling in de geselecteerde rij.
17. Klik op OK.

## <a name="setup-default-order-settings"></a>Standaard orderinstellingen instellen
1. Klik in het actievenster op Plannen.
2. Klik op Standaardorderinstellingen.
3. Typ in het veld Inkoopvestiging de locatie die als standaard wordt gebruikt wanneer de inkooporders worden gemaakt.
4. Typ in het veld Voorraadvestiging de locatie waar het artikel wordt opgeslagen.
5. Vouw de sectie Voorraad uit of samen.
6. Stel Meerdere in op 10.
7. Stel Min. bestelhoeveelheid in op 10.
8. Stel Max. bestelhoeveelheid in op 100.
9. Stel Standaardbestelhoeveelheid in op 10.
10. Voer een nummer in het veld Inkoopdoorlooptijd in.
11. Schakel het selectievakje Werkdagen in of uit.
12. Klik op Opslaan.
13. Selecteer Inkooporder in het veld Standaardordertype.
14. Klik op Opslaan.
15. Sluit de pagina.
    * Sluit de pagina Standaard orderinstellingen.  

## <a name="add-an-item-to-a-coverage-group"></a>Een artikel aan een dekkingsgroep toevoegen
1. Vouw de sectie Planning uit of samen.
2. Klik in het veld Dekkingsgroep op de vervolgkeuzeknop om de zoekopdracht te openen.
3. Zoek in de lijst de Dekkingsgroep die u hebt gemaakt.
4. Klik in de lijst op de koppeling in de geselecteerde rij.

## <a name="create-item-coverage-rules"></a>Regels artikelbehoefteplanning maken
1. Klik in het actievenster op Plannen.
2. Klik op Artikelbehoefteplanning.
3. Klik op Nieuw.
4. Klik op het tabblad Algemeen.
5. Schakel het vakje in de kop van Instellingen behoefteplanningsgroep overschrijven in.
6. Voer 60 in het veld Time fence dekking (dagen) in.
    * Hoewel artikelen in een behoefteplanningsgroep 90 dagen vooruit worden gepland, wordt dit artikel 60 dagen vooruit gepland.  
7. Voer 2 in het veld Negatieve dagen in.
8. Voer 2 in het veld Positieve dagen in.
9. Klik op het tabblad Levertijd.
10. Schakel het vakje in de kop van Inkoop in.
11. Voer in het veld Inkooptijd 5 in.
12. Klik op Opslaan.


