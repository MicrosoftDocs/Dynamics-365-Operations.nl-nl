---
title: Regels voor verkoopprovisie instellen
description: Deze procedure toont u hoe u het berekenen en bijhouden van verkoopprovisie instelt en inschakelt.
author: omulvad
manager: tfehr
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CommissionCustomerGroup, CommissionItemGroup, CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, CommissionCalc, InventPosting, CustTable, EcoResProductDetailsExtended, CommissionEmplSalesGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a109ca5cfaeb031b3b114bccca53804045f3101
ms.sourcegitcommit: 54da65a7da0efd4f0d9760c5b14ff785b28751c4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/22/2020
ms.locfileid: "3830030"
---
# <a name="set-up-sales-commission-rules"></a>Regels voor verkoopprovisie instellen

[!include [banner](../../includes/banner.md)]

Deze procedure toont u hoe u het berekenen en bijhouden van verkoopprovisie instelt en inschakelt. De procedure toont hoe u zowel klant- als artikelprovisiegroepen kunt maken en hoe u geselecteerde klanten en producten aan de respectievelijke groepen koppelt. Deze groepen worden dan gebruikt in de instellingen voor provisieberekening om een combinatie van klant, artikel en vertegenwoordiger te maken die moet overeenkomen met de verkooporder opdat de verkoper in aanmerking komt voor een provisie. Het maken van klant- en artikelprovisiegroepen is optioneel, zoals de berekening van provisie ook voor een afzonderlijk(e) klant en/of artikel kan worden uitgevoerd. U kunt deze procedure uitvoeren in het demogegevensbedrijf USMF of met uw eigen gegevens.


## <a name="set-up-commission-groups-and-commission-rates"></a>De provisiegroepen en provisietarieven instellen
1. Ga naar **Navigatievenster > Modules > Verkoop en marketing > Provisies > Klantengroepen voor provisie**.
2. Selecteer **Nieuw**.
3. Typ een waarde in het veld **Groep**.
4. Typ een waarde in het veld **Naam**.
5. Selecteer **Opslaan**.
6. Sluit de pagina.
7. Ga naar **Navigatievenster > Modules > Verkoop en marketing > Provisies > Artikelgroepen**.
8. Selecteer **Nieuw**.
9. Typ een waarde in het veld **Groep**.
10. Typ een waarde in het veld **Naam**.
11. Selecteer **Opslaan**.
12. Sluit de pagina.
13. Ga naar **Verkoop en marketing > Provisies > Verkoopgroepen**.
    - Een provisieverkoopgroep geeft de werknemers in de rol van vertegenwoordiger op die in aanmerking komen voor het ontvangen van een provisie wanneer een klant die is gekoppeld aan de relevante verkoopgroep bepaalde artikelen koopt.  
    - In het USMF-demobedrijf is er een verkoopgroep met de naam 'Vertegenwoordigers USA'.  
14. Selecteer **Algemeen** in het **Actievenster**.
15. Klik op **Vertegenwoordiger**. De pagina Verkoper bevat een lijst met de verkopers van het bedrijf die aan een specifieke provisiegroep zijn gekoppeld. U kunt meerdere vertegenwoordigers aan dezelfde groep toewijzen en hun respectievelijk aandeel van de totale provisie definiëren als procentuele waarde. Het totale provisieaandeel over alle werknemers mag niet hoger zijn dan 100. 
16. Markeer in de lijst de geselecteerde rij.
17. Selecteer **Bewerken**.
18. Stel **Provisieaandeel** in op '50'.
19. Klik op **Nieuw**.
20. Klik in het veld **Naam** op de vervolgkeuzeknop om de zoekopdracht te openen.
21. Gebruik het **Snelfilter** om records te zoeken. Filter bijvoorbeeld op het veld Naam met een waarde van 'Susan Burk'.
22. Klik op **Selecteren**.
23. Stel **Provisieaandeel** in op '50'.
24. Klik op **Opslaan**.
25. Ga naar **Verkoop en marketing > Provisies > Provisieberekening**. Op de pagina **Provisieberekening** definieert u het provisietarief dat de werknemer zal ontvangen voor een verkooptransactie wanneer deze de vooraf ingestelde combinatie van klant en product bevat. Als onderdeel van de instellingen van het provisietarief moet u de basis voor de provisieberekening opgeven en of kortingen moeten worden opgenomen of uitgesloten. U kunt ook een geldigheidsperiode invoeren voor wanneer het provisietarief actief is.  
26. Klik op **Nieuw**.
27. Selecteer 'Groep' in het veld **Artikelcode**.
28. Klik in het veld **Artikelrelatie** op de vervolgkeuzeknop om de zoekopdracht te openen.
29. Zoek en selecteer in de lijst de groep die u eerder hebt gemaakt.
30. Selecteer 'Groep' in het veld **Klantcode**.
31. Klik in het veld **Klantrelatie** op de vervolgkeuzeknop om de zoekopdracht te openen.
32. Selecteer in de lijst de groep die u eerder hebt ingesteld.
33. Klik in het veld **Relatievertegenwoordiger** op de vervolgkeuzeknop om de zoekopdracht te openen.
34. Zoek en selecteer de gewenste record in de lijst.
    - Behoud de optie 'Regelkorting vooraf'.  
    - Behoud de optie 'Opbrengst' als basis voor de berekening van de provisiewaarde.    
35. Voer in het veld Provisiepercentage een getal in.
36. Klik op **Opslaan**.

## <a name="setting-up-commission-posting"></a>Provisieboeking instellen
1. Ga naar **Navigatievenster > Verkoop en marketing > Provisies > Provisie boeken**. Provisies zijn te betalen aan de werknemers en moeten daarom worden ingesteld om juiste financiële boeking naar de juiste rekeningen in het **Grootboek** te garanderen. Dit wordt uitgevoerd op de pagina **Provisie boeken**. Controleer de instelling die beschikbaar is voor het huidige bedrijf. Doorgaans worden de provisiebedragen geboekt naar een specifieke onkostenrekening en op een specifieke leveranciersrekening tegengeboekt. Als u de instellingen van boekingsregels voor provisie niet hebt, kan het systeem een verkooporder met gerechtigde provisies niet factureren.  
2. Sluit de pagina.

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a>Een provisiegroep toewijzen aan een klant en een product
1. Ga naar **Navigatiedeelvenster > Modules > Verkoop en marketing > Klanten > Alle klanten**.
2. Zoek en selecteer de gewenste record in de lijst.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
4. Klik op **Bewerken**.
5. Vouw de sectie **Standaardwaarden verkooporders uit**.
6. Klik in het veld **Provisiegroep** op de vervolgkeuzeknop om de zoekopdracht te openen.
7. Selecteer in de lijst de groep die u eerder hebt gemaakt.
8. Klik in het veld **Verkoopgroep** op de vervolgkeuzeknop om de zoekopdracht te openen.
9. Zoek en selecteer de gewenste record in de lijst.
10. Klik op **Opslaan**.
11. Ga naar **Navigatievenster > Modules > Productgegevensbeheer > Producten > Vrijgegeven producten**.
12. Gebruik het **Filter** om records te zoeken. Filter bijvoorbeeld op het Veld Artikelnummer met een waarde van 'T0020'.
13. Klik in de lijst op de koppeling in de geselecteerde rij.
14. Klik op **Bewerken**.
15. Vouw de sectie **Verkopen** uit.
16. Klik in het veld **Provisiegroep** op de vervolgkeuzeknop om de zoekopdracht te openen.
17. Selecteer in de lijst de provisiegroep die u eerder hebt gemaakt.
18. Selecteer **Opslaan**.

