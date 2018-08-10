--- 
title: Een aanmaningsreeks maken
description: Gebruik deze taakhandleiding om een aanmaningsreeks te maken.
author: mikefalkner
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6331c3680169b305c4bfbfada4ba106b619be092
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-collection-letter-sequence"></a>Een aanmaningsreeks maken

[!include [task guide banner](../../includes/task-guide-banner.md)]

Gebruik deze taakhandleiding om een aanmaningsreeks te maken. Bij deze taak wordt het demobedrijf USMF gebruikt.

1. Ga naar Crediteren en aanmaningen > Instellingen > Aanmaningsreeks instellen.
2. Klik op Nieuw.
3. Voer in het veld Aanmaningsreeks een volgordeid in die de volgorde zal aangeven. Deze wordt gebruikt bij het instellen van een boekingsprofiel.
4. Typ een waarde in het veld Omschrijving.
    * De betalingsvoorwaarden zijn optioneel. Als u hier een waarde invoert, gebruikt de factuur voor de aanmaningskosten deze betalingsvoorwaarden in plaats van de betalingsvoorwaarden die zijn opgeslagen met de klant.  
5. Selecteer in het veld van de aanmaningscode de code voor de eerste aanmaning die u wilt verzenden.
    * De eerste aanmaning wordt gemaakt aan de hand van de vervaldatum op de factuur, die waarde die u invoert voor de respijtperiode in het veld Dagen op deze regel en andere gegevens die u in deze regel invoert.  
6. Typ een waarde in het veld Omschrijving.
    * De valuta voor de bijzondere kosten is standaard in de valuta van de klant. Deze valutacode kan verschillen van de factuurvaluta.  
7. Klik op Toevoegen om de volgende aanmaning toe te voegen die in de reeks wordt verzonden
    * In veel gevallen is de eerste aanmaning enkel een waarschuwing. U kunt indien nodig bijzondere kosten toevoegen.  
8. Selecteer in het veld van de aanmaningscode de volgende aanmaning die wordt verzonden in de reeks.
9. Typ een waarde in het veld Omschrijving.
10. Selecteer in het hoofdrekeningveld de opbrengstrekening die voor bijzondere kosten wordt gebruikt.
11. Voer de kosten in die worden doorberekend bij het maken van deze aanmaning.
12. Klik in het veld Btw-groep van artikel op de vervolgkeuzeknop om de zoekopdracht te openen.
    * Selecteer een btw-groep voor artikel als btw op de kosten moet worden berekend.  
13. Klik in de lijst op de koppeling in de geselecteerde rij.
14. Voer het minimale achterstallige saldo dat is vereist voordat een aanmaning wordt verzonden.
15. Voer het aantal respijtdagen in dat u zult toestaan.
    * Dit is het aantal dagen na de vervaldatum waarop een aanmaning kan worden gegenereerd. De vervaldatum die voor de berekening wordt gebruikt, is afhankelijk van de positie van de aanmaning in de aanmaningsreeks: ⦁ de respijtperiode voor aanmaning 1 is gerelateerd aan de vervaldatum van de factuur.  ⦁ De respijtperiode voor aanmaning 2 en hoger is gerelateerd aan de datum waarop de vorige aanmaning is geboekt of afgedrukt, afhankelijk van de selectie in het veld Aanmaningscode bijwerken op de pagina Parameters van de module Klanten.  
16. Klik op Toevoegen om de laatste aanmaning in de reeks toe te voegen.
    * U kunt tot vijf aanmaningscodes toevoegen voor een aanmaningsreeks.  
17. Selecteer in het veld van de aanmaningscode de volgende aanmaning die wordt verzonden in de reeks.
18. Typ een waarde in het veld Omschrijving.
19. Geef in het veld Hoofdrekening de gewenste waarden op.
20. Voer in het veld Bijzondere kosten in valuta een getal in.
21. Klik in het veld Btw-groep van artikel op de vervolgkeuzeknop om de zoekopdracht te openen.
22. Klik in de lijst op de koppeling in de geselecteerde rij.
23. Voer in het veld Minimum achterstallig saldo een getal in.
24. Voer een getal in het veld Dagen in.
25. Schakel dit selectievakje in om ervoor te zorgen dat de klant geen leveringen en facturen meer ontvangt.
    * Als u de rekening wilt deblokkeren, selecteert u Nee in het veld Geblokkeerde facturering en levering op de pagina Klanten.  
26. Vouw het sneltabblad Notitie uit.
27. Voer de tekst in die op de aanmaning moet worden weergegeven voor de geselecteerde aanmaningscode.
    * Deze tekst kunt u in meerdere talen vertalen via het menu Vertalingen boven het notitievakje.  


