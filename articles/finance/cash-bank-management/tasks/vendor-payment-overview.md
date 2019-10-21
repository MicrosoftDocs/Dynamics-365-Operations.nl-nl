---
title: Overzicht van leveranciersbetaling
description: Deze taakhandleiding leidt u door verschillende methoden die worden gebruikt voor het maken van leveranciersbetalingen, inclusief het gebruiken van een betalingsvoorstel of het handmatig invoeren van een eenmalige betaling.
author: kweekley
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fcf22a3e9564f991b0cb5ebbd6a2282e3e749990
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177174"
---
# <a name="vendor-payment-overview"></a>Overzicht van leveranciersbetaling

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze taakhandleiding leidt u door verschillende methoden die worden gebruikt voor het maken van leveranciersbetalingen, inclusief het gebruiken van een betalingsvoorstel of het handmatig invoeren van een eenmalige betaling. Bij deze procedure wordt het demobedrijf USMF gebruikt.

1. Ga naar het **Navigatiedeelvenster > Modules > Klanten > Betalingen > Betalingsjournaal**.
2. Klik op **Nieuw**.
3. Selecteer het betalingsjournaal waarin de leveranciersbetalingen moeten worden opgeslagen. 
4. Selecteer het journaal of voer dit handmatig in.
5. Klik op **Regels**.
6. Klik **Actievenster** op **Betalingsvoorstel**.
7. Klik op **Betalingsvoorstel maken**. Het betalingsvoorstel is een query die wordt gebruikt om facturen voor betaling te selecteren. U kunt de lijst met facturen om te betalen bewerken voordat u de leveranciersbetalingen maakt of genereert.
8. Selecteer facturen voor betaling op vervaldatum, contantkorting of beide. 
9. Voer de datum in voor vergelijking met de vervaldatum of de contantkorting. 
10. Optioneel: Voer een betalingsdatum in die wordt gebruikt voor alle betalingen. De hier ingevoerde datum wordt de betalingsdatum voor alle betalingen die zijn gemaakt, ongeacht de vervaldatum of contantkortingsdatum.  
11. Optioneel: Voer een minimumbetalingsdatum in die kan worden gebruikt als de betalingsdatum. De minimumbetalingsdatum is de eerste datum die wordt gebruikt bij het maken van betalingen. Als een factuur bijvoorbeeld een vervaldatum na de minimumbetalingsdatum heeft, wordt de vervaldatum de betalingsdatum in plaats van de minimumbetalingsdatum om de factuur op de laatst mogelijke datum te betalen.
12. Voer aanvullende querybeperkingen in onder de sectie **Op te nemen records**. Het filter wordt vaak gebruikt om de facturen te beperken die zijn geselecteerd voor betaling op basis van leveranciersgroep of betalingsmethode. Zo kunt u bijvoorbeeld een filter toevoegen om alleen facturen per cheque te betalen tijdens deze salarisverwerking.
13. Voer aanvullende querybeperkingen of standaardwaarden voor betalingen in. De extra parameters kunnen worden gebruikt om de betalingsvaluta te definiëren of om gecentraliseerde betalingen voor deze salarisverwerking in te schakelen.  
14. Klik op **OK**. Nadat u op **OK** hebt geklikt, worden de resultaten van de query weergegeven. Als u niet een voorbeeld van de lijst met facturen die zijn geselecteerd voor betaling wilt bekijken, kunt u teruggaan naar het sneltabblad **Parameters** en de instelling **Betalingen maken zonder factuurvoorbeeld** wijzigen in ¨Ja¨.  
15. Kies de knop **Betalingsoverzicht weergeven** om de betalingen te bekijken die worden gemaakt voor de leverancier op de geselecteerde factuur.
16. Kies de knop **Betalingsoverzicht verbergen** om de betalingen te verbergen. 
17. Klik op **Betalingen maken**. Voordat u **Betalingen maken** kiest, kunt u met de rechtermuisknop op het raster klikken en de lijst met facturen naar Excel exporteren. Met de knop **Betalingen maken** worden de leveranciersbetalingen in het betalingsjournaal gemaakt.  
18. Scan uw betalingen en zorg ervoor dat de betalingsmethode is gedefinieerd voor alle betalingen. Als u de betalingen genereert, zoals het afdrukken van een cheque of het maken van een elektronische betaling, moet de betalingsmethode worden gedefinieerd. De betalingsmethode wordt tevens standaard gebruikt voor de bankrekening waarvan de betaling wordt uitgevoerd.  
19. Klik op **Nieuw** om een eenmalige betaling te maken. Een eenmalige betaling kan op elk moment vóór het boeken aan een betalingsjournaal worden toegevoegd. Dit wordt gedaan door op de knop **Nieuw** te klikken en de betalingsgegevens handmatig toe te voegen, in plaats van het **Betalingsvoorstel** te gebruiken.  
20. Selecteer de leverancier waaraan de betaling wordt uitgevoerd.
21. Als een factuur bestaat om te betalen, selecteert u **Transacties vereffenen** om de factuur voor betaling te selecteren. Als dit een vooruitbetaling betreft, is deze stap optioneel. U kunt de betaling maken zonder een factuur te selecteren. 
22. Markeer alle facturen die worden betaald. Als u **Transacties vereffenen** gebruikt om de facturen voor betaling te selecteren, wordt het betalingsbedrag automatisch berekend op basis van de facturen u voor betaling markeert en het bedrag dat u invoert bij **Bedrag om te vereffenen**.
23. Klik op **OK**.
24. Als u een betaling wilt verwijderen, markeert u de rij.
25. Klik op **Verwijderen**. Bij het verwijderen van een betaling wordt alleen de betaling verwijderd. Alle facturen die zijn gemarkeerd voor betaling zijn nog beschikbaar voor betaling via een andere betaling.
26. Klik op **Ja**.
27. Kies **Betaling genereren** om cheques af te drukken of het elektronische betalingsbestand te maken.
28. Selecteer de betalingsmethode die u wilt genereren. Het betalingsjournaal kan betalingen bevatten voor zowel cheques als elektronische betalingen, maar u kunt slechts één betalingstype tegelijk genereren.
29. Selecteer de bankrekening waarvan de betalingen moeten worden gegenereerd.
30. Klik op **OK**. Er worden alleen betalingen gegenereerd voor betalingen die overeenstemmen met de **Betalingsmethode** en **Bankrekening** die u hebt geselecteerd.
31. Als u **Cheques** genereert, kiest u **Document** om de juiste afdrukbestemming te waarborgen voor de cheques.
32. Klik op **OK**.
33. Klik op **OK** om de betalingen te genereren.
34. Klik op **Boeken** als alle betalingen zijn goedgekeurd en gegenereerd. 

