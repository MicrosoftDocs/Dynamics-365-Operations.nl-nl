---
title: Informatie over kredietbeheer voor klanten toevoegen
description: In dit onderwerp wordt uitgelegd hoe u informatie over kredietbeheer voor een klant toevoegt.
author: mikefalkner
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 080b1c4a3887aa5f354743315dc11ffd9f089e73350429d5e08710927f6b2454
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6724058"
---
# <a name="add-credit-management-information-for-customers"></a>Informatie over kredietbeheer voor klanten toevoegen

[!include [banner](../includes/banner.md)]

Nadat u de parameters voor kredietbeheer hebt ingesteld, kunt u meer informatie voor elke klant toevoegen. Deze gegevens sturen de kredietbeheerprocessen aan en bieden tevens aanvullende informatie die incassomedewerkers helpt klanten te beheren.

## <a name="customer-information"></a>Klantgegevens

U kunt de klantgegevens toevoegen op het sneltabblad **Krediet en incasso's** van de pagina **Alle klanten** (**Klant \> Klanten \> Alle klanten**).

1. Stel de optie **Onbeperkte kredietlimiet** in op **Ja** als de klant niet moet worden beperkt door eventuele kredietlimiettests.
2. Stel de optie **Uitsluiten van kredietbeheer** in op **Ja** als u de klant wilt uitsluiten van acties die normaal gesproken optreden tijdens kredietbeheerprocessen.
3. Selecteer de klantkredietbeheergroep voor de klant.
4. Als u de kredietlimiet in de valuta van de klant wilt berekenen, voert u in het veld **Kredietlimiet in valuta van de klant** de kredietlimiet van de klant in. De kredietlimiet in de bedrijfsvaluta wordt omgerekend met behulp van de wisselkoersen die zijn gedefinieerd door het wisselkoerstype voor de kredietlimiet, geselecteerd in de parameters voor kredietbeheer.
5. Voer in het veld **Laatste revisiedatum** de datum in waarop de kredietlimiet van de klant voor het laatst is gecontroleerd door een creditmanager.
6. Voer in het veld **Volgende geplande revisiedatum** de datum in waarop een kredietcontrole en -update voor de klant is gepland.
7. Voer in het veld **In aanmerking komende kredietlimiet** de hoogste kredietlimiet in die aan de klant kan worden toegewezen op basis van uw beoordeling van de kredietgeschiedenis van die klant. De in aanmerking komende kredietlimiet kan verschillen van de kredietlimiet die wordt weergegeven op het sneltabblad **Crediteringen en aanmaningen**.
8. Voer in het veld **Valuta van in aanmerking komende kredietlimiet** de valuta in van de in aanmerking komende kredietlimiet.
9. Voer in het veld **Datum voor in aanmerking komende kredietlimiet** de datum in waarop de kredietlimiet is gemaakt.
10. Voer in het veld **Status kredietrekening** de status in van de kredietrekening van de klant.
11. Voer in het veld **Statusreden** de reden van de betreffende rekeningstatus in.
12. Stel de optie **Met agentschap** in op **Ja** om aan te geven dat de klant momenteel is toegewezen aan een kredietinformatieverstrekker. Deze waarde is alleen bedoeld voor informatieve doeleinden. Deze wordt niet gebruikt in kredietbeheerprocessen.
13. Stel de optie **Titeldragend** in op **Ja** om aan te geven dat een titel voor het bedrijf wordt gedragen. Deze waarde is alleen bedoeld voor informatieve doeleinden. Deze wordt niet gebruikt in een kredietbeheerproces.
14. Voer in het veld **Bedrijf gestart op** de datum in waarop de klant is gestart met zakendoen. Deze informatie wordt gebruikt wanneer risicoscores worden gemaakt.
15. Voer in het veld **Klant sinds** de datum in waarop de eerste transacties voor de klant zijn verwerkt. Deze informatie wordt gebruikt wanneer risicoscores worden gemaakt.
16. Voer notities in die het kredietteam kan gebruiken om de kredietwaardigheid van de klant verder te evalueren.

Een deel van de informatie die op de pagina **Klant** wordt weergegeven, wordt gemaakt door een ander proces:

- Het veld **Vervaldatum kredietlimiet** toont de datum waarop de kredietlimiet vervalt. Als u dit veld niet instelt, vervalt de kredietlimiet van de klant niet.
- Het veld **Datum kredietlimiet** toont de datum waarop de kredietlimiet is gemaakt. Dit veld wordt bijgewerkt wanneer de kredietlimiet wordt aangepast.
- Tijdelijke kredietlimieten overschrijven de kredietlimiet van de klant gedurende een periode. Deze worden in plaats van de kredietlimiet gebruikt om de totale kredietlimiet te berekenen. Deze informatie wordt alleen weergegeven als er een kredietlimiet actief is. U kunt tijdelijke kredietlimieten toevoegen via kredietlimietcorrecties.
- Het veld **Verzekering en garanties** toont de totale waarde van verzekering en garanties die de kredietlimiet voor de klant mogelijk kunnen verhogen.
- Het veld **Totale kredietlimiet** toont de uiteindelijke kredietlimiet voor de klant. Bij de totale kredietlimiet is rekening gehouden met verzekering en garanties en tijdelijke kredietlimieten.

## <a name="temporary-credit-limits"></a>Tijdelijke kredietlimieten

Tijdelijke kredietlimieten overschrijven de kredietlimieten van de klant gedurende een vastgestelde periode. U kunt tijdelijke kredietlimieten toevoegen door middel van kredietlimietcorrecties. Met kredietlimietcorrecties kunnen creditmanagers de kredietlimieten en vervaldatums van één klant, een groep klanten of alle klanten bijwerken via een boekingsproces.

U kunt posten voor kredietlimietcorrecties maken op de pagina **Kredietlimietcorrecties** (**Kredietbeheer \> Kredietlimietcorrecties \> Kredietlimietcorrecties**).

## <a name="create-insurance-policies-and-guarantees"></a>Verzekeringspolissen en garanties maken

U kunt een of meer verzekeringspolissen en garanties voor elke klant maken. U kunt deze dan gebruiken om het risico voor uw bedrijf te berekenen wanneer het een klant krediet verstrekt. Verzekeringspolissen en garanties kunnen ook worden opgenomen in de kredietlimiet voor een klant.

U kunt verzekeringspolissen en garanties maken op de pagina **Alle klanten** (**Klanten \> Klanten \> Alle klanten**). Selecteer een klant en selecteer vervolgens in het actievenster op het tabblad **Kredietbeheer** de optie **Verzekering en garanties**.

> [!NOTE]
> In de volgende procedure selecteert u een verzekeraar of borgsteller in het globale adresboek. Voordat u met deze procedure begint, moet u er dus voor zorgen dat de verzekeraars en borgstellers zijn toegevoegd aan het globale adresboek.

1. Voer in het veld **Id** de **Borgsteller** of **Verzekering** in.
2. Selecteer in het veld **Type borgsteller/verzekering** een van de typen borgstellers of verzekeringen die u eerder hebt ingesteld.
3. Selecteer in het veld **Verzekeraar/Borgsteller** de verzekeraar of borgsteller in het globale adresboek. 
4. Als u **Verzekering** hebt geselecteerd in het veld **Id**, selecteert u in het veld **Dekkingstype polis** een van de dekkingstypen die u eerder hebt ingesteld. Het is niet mogelijk om een type polisdekking te selecteren voor een borgsteller.
5. Voer in het veld **Id** de id van de polis in. Deze id is meestal een polisnummer.
6. Voer in het veld **Ingangsdatum** de begindatum in van de verzekeringspolis of garantie.
7. Voer in het veld **Vervaldatum** de einddatum in waarop de verzekeringspolis of garantie. vervalt.
8. Voer in het veld **Waarde** de waarde in van de verzekeringspolis of garantie. Deze waarde is de volledige waarde van de polis.
9. Selecteer in het veld **Valuta** de valuta van de poliswaarde. 
10. Geef in het veld **Kredietlimiet bijwerken** een percentage op tussen **0** en **100**. Dit percentage wordt toegepast op de poliswaarde en het resulterende bedrag wordt gebruikt om de kredietlimiet te verhogen die wordt gebruikt voor berekeningen van de kredietlimiet. De berekende waarde wordt weergegeven onder **Totale kredietlimiet, verzekering en garanties** op het sneltabblad **Krediet en incasso's** op de pagina **Klanten**.

    Dit is een voorbeeld:

    - De kredietlimiet (A) is 100.000.
    - De poliswaarde (B) is 50.000.
    - Het percentage voor **Kredietlimiet bijwerken** (C) is 50,00.
    
    In dit geval is de effectieve kredietlimiet 125.000 (= A + \[B × C\]).

11. Schakel het selectievakje **Opgenomen in risico** in als u de kredietlimiet die in berekeningen van de kredietlimiet wordt gebruikt, wilt verlagen met de volledige waarde van de polis. Als dit selectievakje is ingeschakeld, wordt de waarde die wordt berekend wanneer het percentage voor **Kredietlimiet bijwerken** is opgegeven, niet gebruikt in de berekeningen van de kredietlimiet.

    Dit is een voorbeeld:

    - De kredietlimiet (A) is 100.000.
    - De poliswaarde (B) is 50.000.
    - Het percentage voor **Kredietlimiet bijwerken** (C) is 50,00.

    In dit geval is de effectieve kredietlimiet 125.000 (= A + \[B × C\]).
    
    Als u het selectievakje **Opgenomen in risico** echter inschakelt, wordt de waarde **Kredietlimiet bijwerken** van 50.000 (= 50 procent van 100.000) verwijderd en is de risicowaarde 75.000 (= A + \[B × C\] – B).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]