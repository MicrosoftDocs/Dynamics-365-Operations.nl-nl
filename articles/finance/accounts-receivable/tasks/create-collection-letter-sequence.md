---
title: Een aanmaningsreeks maken
description: Gebruik deze procedure om een aanmaningsreeks te maken.
author: JodiChristiansen
ms.date: 12/07/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CollectionLetterCourse
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af5d0a001fbe705834e116516933be67f2de8826
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734153"
---
# <a name="create-a-collection-letter-sequence"></a>Een aanmaningsreeks maken

[!include [banner](../../includes/banner.md)]

Gebruik deze procedure om een aanmaningsreeks te maken. Bij deze taak wordt het demobedrijf USMF gebruikt.

1. Ga naar **Crediteren en aanmaningen > Instellingen > Aanmaningsreeks instellen**.
2. Klik op **Nieuw**.
3. Voer in het veld **Aanmaningsreeks** een volgorde-id in die de volgorde aangeeft. Deze wordt gebruikt bij het instellen van een boekingsprofiel.
4. Typ een waarde in het veld **Beschrijving**. De betalingsvoorwaarden zijn optioneel. Als u hier een waarde invoert, gebruikt de factuur voor de aanmaningskosten deze betalingsvoorwaarden in plaats van de betalingsvoorwaarden die zijn opgeslagen met de klant.  
5. Selecteer in het veld **Aanmaningscode** de code voor de eerste aanmaning die u wilt verzenden. De eerste aanmaning wordt gemaakt aan de hand van de vervaldatum op de factuur, die waarde die u invoert voor de respijtperiode in het veld Dagen op deze regel en andere gegevens die u in deze regel invoert.  
6. Typ een waarde in het veld **Beschrijving**. 
7. De standaardvaluta voor de bijzondere kosten is de valuta van de rechtspersoon. Deze valutacode kan verschillen van de factuurvaluta.   
8. Klik op **Toevoegen** om de volgende aanmaning toe te voegen die in de reeks wordt verzonden. In veel gevallen is de eerste aanmaning enkel een waarschuwing. U kunt indien nodig bijzondere kosten toevoegen.  
9. Selecteer in het veld **Aanmaningscode** de volgende aanmaning die wordt verzonden in de reeks.
10. Selecteer in het veld **Hoofdrekening** de opbrengstrekening die voor bijzondere kosten wordt gebruikt.
11. Voer de kosten in die worden doorberekend bij het maken van deze aanmaning.
12. Klik in het veld **Btw-groep voor artikel** op de vervolgkeuzeknop om de zoekopdracht te openen. Selecteer een btw-groep voor artikel als btw op de kosten moet worden berekend.  
13. Klik in de lijst op de koppeling in de geselecteerde rij.
14. Voer in het veld **Minimum achterstallig saldo** het minimale achterstallige saldo in dat vereist is voordat een aanmaning wordt verzonden.
15. Voer in het veld **Dagen** het aantal respijtdagen in dat u toestaat. Dit is het aantal dagen na de vervaldatum waarop een aanmaning kan worden gegenereerd. Welke vervaldatum voor de berekening wordt gebruikt, is afhankelijk van de positie van de aanmaning in de aanmaningsreeks:
    - De respijtperiode voor aanmaning 1 is gerelateerd aan de vervaldatum op de factuur.
    - De respijtperiode voor aanmaningen 2 en hoger is gerelateerd aan de datum waarop de vorige aanmaning is geboekt of afgedrukt, afhankelijk van de selectie in het veld Aanmaningscode bijwerken op de pagina Parameters van module Klanten.  
16. Klik op **Toevoegen** om de laatste aanmaning in de reeks toe te voegen. U kunt tot vijf aanmaningscodes toevoegen voor een aanmaningsreeks.  
17. Selecteer in het veld **Aanmaningscode** de volgende aanmaning die wordt verzonden in de reeks.
18. Typ een waarde in het veld **Beschrijving**.
19. Geef in het veld **Hoofdrekening** de gewenste waarden op.
20. Voer in het veld **Bijzondere kosten in valuta** een getal in.
21. Klik in het veld **Btw-groep voor artikel** op de vervolgkeuzeknop om de zoekopdracht te openen.
22. Klik in de lijst op de koppeling in de geselecteerde rij.
23. Voer in het veld **Minimum achterstallig saldo** een getal in.
24. Voer in het veld **Dagen** een getal in.
25. Schakel het selectievakje **Blokkeren** in om ervoor te zorgen dat de klant geen leveringen en facturen meer ontvangt. Als u de rekening wilt deblokkeren, selecteert u **Nee** in het veld **Geblokkeerde facturering en levering** van de pagina **Klanten**.  
26. Vouw het sneltabblad **Notitie** uit.
27. Voer de tekst in die op de aanmaning moet worden weergegeven voor de geselecteerde aanmaningscode. Deze tekst kunt u in meerdere talen vertalen via het menu **Vertalingen** boven het notitievakje.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
