--- 
title: Regels voor verkoopprovisie instellen
description: Deze procedure toont u hoe u het berekenen en bijhouden van verkoopprovisie instelt en inschakelt.
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8d81765884f741443d1c0f5b0cb8bc545945e1a1
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-sales-commission-rules"></a>Regels voor verkoopprovisie instellen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure toont u hoe u het berekenen en bijhouden van verkoopprovisie instelt en inschakelt. De procedure toont hoe u zowel klant- als artikelprovisiegroepen kunt maken en hoe u geselecteerde klanten en producten aan de respectievelijke groepen koppelt. Deze groepen worden dan gebruikt in de instellingen voor provisieberekening om een combinatie van klant, artikel en vertegenwoordiger te maken die moet overeenkomen met de verkooporder opdat de verkoper in aanmerking komt voor een provisie. Het maken van klant- en artikelprovisiegroepen is optioneel, zoals de berekening van provisie ook voor een afzonderlijk(e) klant en/of artikel kan worden uitgevoerd. U kunt deze procedure uitvoeren in het demogegevensbedrijf USMF of met uw eigen gegevens.


## <a name="set-up-commission-groups-and-commission-rates"></a>De provisiegroepen en provisietarieven instellen
1. Ga naar Verkoop en marketing > Provisies > Klantengroepen voor provisie.
2. Klik op Nieuw.
3. Typ een waarde in het veld Groep.
4. Typ een waarde in het veld Naam.
5. Klik op Opslaan.
6. Sluit de pagina.
7. Ga naar Verkoop en marketing > Provisies > Artikelgroepen.
8. Klik op Nieuw.
9. Typ een waarde in het veld Groep.
10. Typ een waarde in het veld Naam.
11. Sluit de pagina.
12. Ga naar Verkoop en marketing > Provisies > Verkoopgroepen.
    * Een provisieverkoopgroep geeft de werknemers in de rol van vertegenwoordiger op die in aanmerking komen voor het ontvangen van een provisie wanneer een klant die is gekoppeld aan de relevante verkoopgroep bepaalde artikelen koopt.  
    * In het USMF-demobedrijf is er een verkoopgroep met de naam 'Vertegenwoordigers USA'.  
13. Klik in het actievenster op Algemeen.
14. Klik op Vertegenwoordiger.
    * De pagina Verkoper bevat een lijst met de verkopers van het bedrijf die aan een specifieke provisiegroep zijn gekoppeld. U kunt meerdere vertegenwoordigers aan dezelfde groep toewijzen en hun respectievelijk aandeel van de totale provisie definiëren als procentuele waarde. Het totale provisieaandeel over alle werknemers mag niet hoger zijn dan 100.  
15. Markeer in de lijst de geselecteerde rij.
16. Klik op Bewerken.
17. Stel Provisieaandeel in op '50'.
18. Klik op Nieuw.
19. Klik in het veld Naam op de vervolgkeuzeknop om de zoekopdracht te openen.
20. Gebruik de snelfilter om records te zoeken. Filter bijvoorbeeld op het veld Naam met een waarde van 'Susan Burk'.
21. Klik op Selecteren.
22. Stel Provisieaandeel in op '50'.
23. Klik op Opslaan.
24. Ga naar Verkoop en marketing > Provisies > Provisieberekening.
    * Op de pagina Provisieberekening definieert u het provisietarief dat de werknemer zal ontvangen voor een verkooptransactie wanneer deze de vooraf ingestelde combinatie van klant en product bevat. Als onderdeel van de instellingen van het provisietarief moet u de basis voor de provisieberekening opgeven en of kortingen moeten worden opgenomen of uitgesloten. U kunt ook een geldigheidsperiode invoeren voor wanneer het provisietarief actief is.  
25. Klik op Nieuw.
26. Selecteer Groep in het veld Artikelcode.
27. Klik in het veld Artikelrelatie op de vervolgkeuzeknop om de zoekopdracht te openen.
28. Zoek en selecteer in de lijst de groep die u eerder hebt gemaakt.
29. Klik in de lijst op de koppeling in de geselecteerde rij.
30. Selecteer 'Groep' in het veld Klantcode.
31. Klik in het veld Klantrelatie op de vervolgkeuzeknop om de zoekopdracht te openen.
32. Selecteer in de lijst de groep die u eerder hebt ingesteld.
33. Klik in het veld Relatie vertegenwoordiger op de vervolgkeuzeknop om de zoekopdracht te openen.
34. Zoek en selecteer de gewenste record in de lijst.
    * Behoud de optie 'Regelkorting vooraf'.  
    * Behoud de optie 'Opbrengst' als basis voor de berekening van de provisiewaarde.    
35. Voer in het veld Provisiepercentage een getal in.
36. Klik op Opslaan.

## <a name="setting-up-commission-posting"></a>Provisieboeking instellen
1. Ga naar Verkoop en marketing > Provisies > Provisie boeken.
    * Provisies zijn te betalen aan de werknemers en moeten daarom worden ingesteld om juiste financiële boeking naar de juiste rekeningen in het grootboek te garanderen. Dit wordt uitgevoerd op de pagina Provisie boeken. Controleer de instelling die beschikbaar is voor het huidige bedrijf. Doorgaans worden de provisiebedragen geboekt naar een specifieke onkostenrekening en op een specifieke leveranciersrekening tegengeboekt. Als u de instellingen van boekingsregels voor provisie niet hebt, kan het systeem een verkooporder met gerechtigde provisies niet factureren.  
2. Sluit de pagina.

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a>Een provisiegroep toewijzen aan een klant en een product
1. Ga naar Verkoop en marketing > Klanten > Alle klanten.
2. Zoek en selecteer de gewenste record in de lijst.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
4. Klik op Bewerken.
5. Vouw de sectie Standaardwaarden verkooporders uit.
6. Klik in het veld Provisiegroep op de vervolgkeuzeknop om de zoekopdracht te openen.
7. Selecteer in de lijst de groep die u eerder hebt gemaakt.
8. Klik in het veld Verkoopgroep op de vervolgkeuzeknop om de zoekopdracht te openen.
9. Zoek en selecteer de gewenste record in de lijst.
10. Klik op Opslaan.
11. Ga naar Productgegevensbeheer > Producten > Vrijgegeven producten.
12. Gebruik de snelfilter om records te zoeken. Filter bijvoorbeeld op het Veld Artikelnummer met een waarde van 'T0020'.
13. Klik in de lijst op de koppeling in de geselecteerde rij.
14. Klik op Bewerken.
15. Vouw de sectie Verkopen uit.
16. Klik in het veld Provisiegroep op de vervolgkeuzeknop om de zoekopdracht te openen.
17. Selecteer in de lijst de provisiegroep die u eerder hebt gemaakt.


