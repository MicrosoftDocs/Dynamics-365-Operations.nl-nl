---
title: Orderwachtstanden beheren
description: In deze procedure wordt uitgelegd hoe klantverkooporders in de wachtstand kunnen worden geplaatst, hoe u een order in de wachtstand uitcheckt en hoe u orderwachtstanden verwijdert.
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans, MCRHoldCheckOutOverride, MCRHoldCodeTable, MCRItemListCopying, MCRItemListTable, MCROMHoldList
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e9c91061b82b8e172d8b93e9b255d0c9f400b5b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254984"
---
# <a name="manage-order-holds"></a>Orderwachtstanden beheren

[!include [banner](../../includes/banner.md)]

In deze procedure wordt uitgelegd hoe klantverkooporders in de wachtstand kunnen worden geplaatst, hoe u een order in de wachtstand uitcheckt en hoe u orderwachtstanden verwijdert. Een order kan in wachtstand worden geplaatst om diverse redenen. U kunt bijvoorbeeld een order in de wachtstand plaatsen tot een klantadres of betalingsmethode kan worden geverifieerd of tot een manager de kredietlimiet van de klant kan controleren. Zolang de order in de wachtstand staat, kan deze niet worden verwerkt door het magazijn voor verzending. 

U kunt deze procedure uitvoeren in het demogegevensbedrijf USMF of met uw eigen gegevens.


## <a name="set-up-order-holds"></a>Order in wachtstand instellen
1. Ga naar **Navigatievenster > Modules > Verkoop en marketing > Instellen > Verkooporders > Orderwachtstandcodes**.
2. Klik op **Nieuw**.
3. Typ een waarde in het veld **Wachtstandcode**. Typ bijvoorbeeld 'Terugbellen.  
4. Typ een waarde in het veld **Beschrijving**.
    - Bijvoorbeeld: Order in wachtstand, wacht tot klant terugbelt.  
    - Schakel eventueel het selectievakje **Reserveringen verwijderen** in, zodat alle fysieke reserveringen uit de order worden verwijderd wanneer deze wachtstandcode wordt toegevoegd.  
5. Klik op **Opslaan**.

## <a name="place-order-on-hold"></a>Order in wachtstand plaatsen
1. Ga naar **Navigatievenster > Modules > Verkoop en marketing > Verkooporders > Alle verkooporders**.
2. Klik op **Nieuw**.
3. Typ of selecteer een waarde in het veld **Klantrekening**.
4. Klik op **OK**.
5. Typ of selecteer een waarde in het veld **Artikelnummer**.
6. Voer een getal in het veld **Hoeveelheid** in.
7. Klik in het **actievenster** op **Verkooporder**.
8. Klik op **Orderwachtstanden**.
9. Klik op **Nieuw**.
10. Selecteer in het veld **Orderwachtstand** de code die u hebt gemaakt in de vorige subtaak.
11. Klik op **Opslaan**.
12. Sluit de pagina.
13. Ga naar **Verkoop en marketing > Verkooporders > Alle verkooporders**.
14. Markeer in de lijst de geselecteerde rij. Bij orders die momenteel de status 'In wachtstand' hebben, zijn de velden 'Niet verwerken' en 'Wachtstand' gemarkeerd.
15. Klik in het actievenster op **Verzamelen en inpakken**.

## <a name="manage-order-holds"></a>Orderwachtstanden beheren
1. Ga naar **Verkoop en marketing > Verkooporders > Openstaande orders > Orderwachtstanden**. De pagina **Orderwachtstanden** fungeert als een workbench, waarin u een overzicht kunt krijgen van alle actuele en verwerkte wachtstanden en waar u deze en de bijbehorende verkooporders kunt afhandelen.     
2. Markeer in de lijst de geselecteerde rij.
3. Klik in het **actievenster** op **Uitchecken in wachtstand**.
4. Klik op **Uitchecken**.
5. Maak in de lijst de markering van de geselecteerde rij ongedaan. In het veld **Uitgecheckt naar** wordt nu uw gebruikers-id weergegeven.   
6. Klik op **Uitchecken wissen**.
7. Klik in het **actievenster** op **Wachtstand wissen**.
    - Als u de wachtstand wilt verwijderen zodat de order door kan gaan naar de volgende afhandelingsstap, moet u de wachtstand uitschakelen. Als de order geen aanpassing vereist, kunt u de actie Wachtstanden wissen uitvoeren. U kunt echter de actie Wissen en aanpassen gebruiken, als bij het wissen van een wachtstand de order moet worden bijgewerkt.      
    - De actie **Wissen en indienen** is alleen van toepassing wanneer u gebruik maakt van de Callcenterfunctionaliteit.  
8. Klik op **Wachtstanden wissen**. De wachtstand is nu van de order gewist en verwijderd uit de lijst met actieve wachtstanden. Als u alle wachtstanden wilt bekijken, of een subset daarvan op basis van een specifieke status, wijzigt u de waarde in het veld Weergeven.     



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]