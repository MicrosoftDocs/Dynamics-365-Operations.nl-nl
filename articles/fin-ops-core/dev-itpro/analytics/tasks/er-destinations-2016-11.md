---
title: ER-bestemmingen configureren
description: Deze procedure laat zien hoe u verschillende bestemmingen voor uitvoercomponenten voor ER (Elektronische rapportage) instelt en gebruikt, zoals een map of een bestand.
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERFormatDestinationTable, SysLookupPicklist, ERFormatDestinationSettings, ERFormatDestinationEmailSettings, ERExpressionDesignerFormula, SRSPrintDestinationTokens
ms.openlocfilehash: 3c8d03e9783013183fbe76cb36014fa9e1e1cbed
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291049"
---
# <a name="er-configure-destinations"></a>ER-bestemmingen configureren

[!include [banner](../../includes/banner.md)]

Deze procedure laat zien hoe u verschillende bestemmingen voor uitvoercomponenten voor ER (Elektronische rapportage) instelt en gebruikt, zoals een map of een bestand. Het demobedrijf dat wordt gebruikt om deze procedure te maken is DEMF. Duitsland is het land\de regio van het primaire adres van de rechtspersoon, maar u kunt elke rechtspersoon voor deze procedure gebruiken. 

De in dit voorbeeld gebruikte indeling is ISO20022 Kredietoverdracht, maar u kunt elke indeling gebruiken die u al hebt geïmporteerd. Deze procedure is een voorbeeld van het instellen van één bestand en één bestemming. Meer informatie over bestemmingsbeheer voor elektronische rapportage is te vinden in de Help van Dynamics 365 Finance.

1. Ga naar Organisatiebeheer > Elektronische rapportage > Bestemming elektronische rapportage.
2. Klik op Nieuw om een nieuwe set bestemmingen voor een indeling te maken.
3. Selecteer in het veld Verwijzing een indeling waarvoor u bestemmingen wilt configureren.
    * Als u geen waarde hebt om te selecteren, betekent dit dat u geen indelingsconfiguraties voor elektronische rapportage hebt geïmporteerd. U moet een indelingsconfiguratie importeren voordat u bestemmingen instelt.  
4. Klik op Nieuw om een nieuwe bestandsbestemming te maken.
    * U kunt één bestandsbestemming voor elke uitvoercomponent met dezelfde indeling maken, zoals een map of een bestand. U kunt bestemmingen in de instellingen afzonderlijk in- en uitschakelen.  
5. Typ in het veld Naam de gebruikersvriendelijke naam van de uitvoercomponent.
    * Het wordt aanbevolen omschrijvende namen te gebruiken, zoals "Betalingsbestand" of "Controlerapport". Deze namen worden aan gebruikers gepresenteerd tijdens de uitvoering van de configuratie samen met de bestemmingsinstellingen.  
6. Selecteer in het veld Bestandsnaam een bestand dat of een map die specifiek geldt voor de indeling.
7. Klik op Instellingen.
8. Selecteer Ja in het veld Ingeschakeld.
    * Met het selectievakje Ingeschakeld op elk tabblad wordt elke bestemming afzonderlijk in- en uitgeschakeld. In dit voorbeeld schakelt u het verzenden van een uitvoerbestand aan een e-mailontvanger in wanneer het bestand wordt gegenereerd.  
9. Klik op Bewerken om de e-mailontvangers in te stellen.
10. Klik op Toevoegen.
11. Klik op E-mail van Afdrukbeheer.
12. Selecteer een optie in het veld E-mailbron.
    * U kunt de verschillende typen selecteer voor e-mailbron, zoals een klant of een leverancierstype. Hiermee wordt het type argument aangegeven dat wordt geretourneerd door de formule voor het e-mailbronaccount. De formule voor het e-mailbronaccount die wordt beschreven in een volgende stap, is de plaats waaraan u een e-mailbron verbindt. Selecteer Leverancier als met uw formule een leveranciersrekening wordt geretourneerd. Gebruik Leverancier als u het configuratievoorbeeld ISO 20022 Kredietoverdracht gebruikt.  
13. Klik op de knop E-mailbron binden.
14. Typ in de formule een documentspecifieke verwijzing naar een eerder geselecteerd partijtype.
    * In plaats van te typen kunt u een gegevensbronknooppunt zoeken waarmee de partijrekening wordt weergegeven. Klik vervolgens op de knop Gegevensbron toevoegen om de formule bij te werken. Bijvoorbeeld als u de configuratie ISO 20022 Kredietoverdracht gebruikt, is het knooppunt waarmee een leveranciersrekening wordt voorgesteld '$PaymentsForCoveringLetter'.Creditor.Identification.SourceID. Voer anders een tekenreekswaarde in, zoals "DE-001", om een formule op te slaan.  
15. Klik op Opslaan.
16. Sluit de pagina.
17. Klik op Bewerken om contactgegevens voor de partij te configureren.
18. Selecteer Ja in het veld Primaire contactpersoon.
    * U kunt verschillende opties gebruiken om op te geven welk type contactpersoon van de partij als e-mailadres voor deze bestemming moet worden gebruikt. We gebruiken in dit voorbeeld de primaire contactpersoon.  
19. Klik op OK.
20. Klik op OK.
21. Typ een waarde in het veld Onderwerp.
22. Klik op OK.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
