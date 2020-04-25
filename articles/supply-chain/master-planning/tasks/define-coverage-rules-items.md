---
title: Behoefteplanningsregels voor artikelen definiëren
description: Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.
author: ShylaThompson
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fd44c458da03807ddc1dc9d652da29c1404dbe64
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209600"
---
# <a name="define-coverage-rules-for-items"></a>Behoefteplanningsregels voor artikelen definiëren

[!include [banner](../../includes/banner.md)]

Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. Deze procedure toont hoe u behoefteplanningsregels maakt en behoefteplanningsinstellingen voor een specifiek artikel overschrijft. Het toont ook hoe u standaardvoorraadinstellingen opgeeft.


## <a name="create-a-coverage-group"></a>Een behoefteplanningsgroep maken
1. Ga naar **Navigatievenster > Modules > Hoofdplanning > Instellen >Behoefteplanningsgroepen**.
2. Klik op **Nieuw**.
3. Typ een waarde in het veld **Behoefteplanningsgroep**.
4. Typ een waarde in het veld **Naam**.
5. Typ een waarde in het veld **Agenda**. Kies de agenda die tijdens hoofdplanning wordt gebruikt om aanvullingssuggesties te doen voor artikelen in deze groep.  
6. Selecteer een optie in het veld **Behoefteplanningscode**. Selecteer 'Vereiste' voor deze procedure.  
7. Voer 90 in het veld **Time fence behoefteplanning (dagen)** in. Voor artikelen in deze groep maakt de hoofdplanning aanvullingssuggesties tot maximaal 90 dagen in de toekomst.  
8. Voer 1 in het veld **Negatieve dagen** in.
9. Voer 1 in het veld **Positieve dagen** in.
10. Vouw de sectie **Overige** uit of samen.
11. Ga naar de sectie **Veiligheidsmarges in dagen** en voer in het veld **Ontvangstmarge toegevoegd aan behoeftedatum** 1 in. Als bijvoorbeeld de ontvangstmarge is ingesteld op 1 dag en een inkooporderregel is gepland voor ontvangst op 15 mei, berekent de hoofdplanning de aangepaste ontvangstdatum als 16 mei.  
12. Typ 1 in het veld **Uitgiftemarge afgetrokken van behoeftedatum**. Als bijvoorbeeld de veiligheidsmarge is ingesteld op 1 dag en een verkooporderregel is gepland voor levering op 15 mei, berekent de hoofdplanning de aangepaste leveringsdatum als 14 mei.  
13. Typ 1 in het veld **Bestelmarge opgeteld bij doorlooptijd van artikel**.
14. Klik op **Opslaan**.

## <a name="create-a-new-product"></a>Een nieuw product maken
1. Ga naar **Navigatievenster > Modules > Productgegevensbeheer > Producten > Vrijgegeven producten**.
2. Klik op **Nieuw**.
3. Typ een waarde in het veld **Productnummer**.
4. Typ een waarde in het veld **Productnaam**.
5. Klik in het veld **Artikelmodelgroep** op de vervolgkeuzeknop om de zoekopdracht te openen.
6. Zoek en selecteer het gewenste record in de lijst.
7. Klik in de lijst op de koppeling in de geselecteerde rij.
8. Klik in het veld **Artikelgroep** op de vervolgkeuzeknop om de zoekopdracht te openen.
9. Zoek en selecteer het gewenste record in de lijst.
10. Klik in de lijst op de koppeling in de geselecteerde rij.
11. Klik in het veld **Opslagdimensiegroep** op de vervolgkeuzeknop om de zoekopdracht te openen.
12. Zoek en selecteer het gewenste record in de lijst.
13. Klik in de lijst op de koppeling in de geselecteerde rij.
14. Klik in het veld **Traceringsdimensiegroep** op de vervolgkeuzeknop om de zoekopdracht te openen.
15. Zoek en selecteer de gewenste record in de lijst.
16. Klik in de lijst op de koppeling in de geselecteerde rij.
17. Klik op **OK**.

## <a name="setup-default-order-settings"></a>Standaard orderinstellingen instellen
1. Klik op **Plannen** in het **actievenster**.
2. Klik onder **Orderinstellingen** op **Standaardorderinstellingen**.
3. Ga naar **Inkooporder** en typ in het veld **Standaardvestiging** de vestiging die als standaard moet worden gebruikt wanneer de inkooporders worden gemaakt.
4. Typ in het veld **Standaardmagazijn** de vestiging waar het artikel is opgeslagen.
5. Vouw de sectie **Voorraad** uit of samen.
6. Typ 10 in het veld **Meerdere**.
7. Typ 10 in het veld **Min.bestelhoeveelheid**.
8. Typ 100 in het veld **Max.bestelhoeveelheid**.
9. Typ 10 in het veld **Standaardbestelhoeveelheid**.
10. Voer een numerieke waarde in het veld **Inkoopdoorlooptijd** in.
11. Schakel het selectievakje **Werkdagen** in of uit.
12. Klik op **Opslaan**.
13. Selecteer Inkooporder in het veld **Standaardordertype**.
14. Klik op **Opslaan**.
15. Sluit de pagina. Sluit de pagina Standaard orderinstellingen.  

## <a name="add-an-item-to-a-coverage-group"></a>Een artikel aan een behoefteplanningsgroep toevoegen
1. Vouw de sectie **Planning** uit of samen.
2. Klik in het veld **Behoefteplanningsgroep** op de vervolgkeuzeknop om de zoekopdracht te openen.
3. Zoek in de lijst de **Behoefteplanningssgroep** die u hebt gemaakt.
4. Klik in de lijst op de koppeling in de geselecteerde rij.

## <a name="create-item-coverage-rules"></a>Regels artikelbehoefteplanning maken
1. Klik op **Plannen** in het **actievenster**.
2. Klik onder **Behoefteplanning** op **Artikelbehoefteplanning**.
3. Klik op **Nieuw**.
4. Klik op het tabblad **Algemeen**.
5. Schakel het vakje in de kop van **Instellingen behoefteplanningsgroep overschrijven** in.
6. Voer 60 in het veld **Time fence behoefteplanning (dagen)** in. Hoewel artikelen in een behoefteplanningsgroep 90 dagen vooruit worden gepland, wordt dit artikel 60 dagen vooruit gepland.  
7. Voer 2 in het veld **Negatieve dagen** in.
8. Voer 2 in het veld **Positieve dagen** in.
9. Klik op het tabblad **Levertijd**.
10. Schakel het vakje in de kop van **Inkoop** in.
11. Voer in het veld **Inkooptijd** 5 in.
12. Klik op **Opslaan**.

