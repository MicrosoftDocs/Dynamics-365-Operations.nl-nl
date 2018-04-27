--- 
title: Een indeling wijzigen door een Microsoft Excel-sjabloon voor elektronische aangifte opnieuw toe te passen (ER)
description: Als u de stappen in deze procedure wilt voltooien, moet u eerst de procedure ER Een configuratie maken voor het genereren van rapporten in OPENXML-indeling voltooien.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: b49cfe39732a450e4723419c50d8bcc3d64b7ec9
ms.openlocfilehash: 2f35727376812b0de428ce929ebe0d33bc497984
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="modify-a-format-by-reapplying-a-microsoft-excel-template-for-electronic-reporting-er"></a>Een indeling wijzigen door een Microsoft Excel-sjabloon voor elektronische aangifte opnieuw toe te passen (ER)

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Als u de stappen in deze procedure wilt voltooien, moet u eerst de procedure ER Een configuratie maken voor het genereren van rapporten in OPENXML-indeling voltooien.

In deze procedure wordt uitgelegd hoe u een elektronische rapportage (ER)-indelingsconfiguratie wijzigt door het opnieuw toepassen van een Microsoft Excel-sjabloon die is gewijzigd. In deze procedure importeert u een gewijzigde Excel-sjabloon in Emergency Recovery-indelingsconfiguraties die zijn gemaakt voor het voorbeeldbedrijf, Litware, Inc., en genereert u vervolgens elektronische documenten. Deze procedure is bedoeld voor gebruikers met de rol Systeembeheerder of Elektronische aangifteontwikkelaar. Deze stappen kunnen worden voltooid met de GBSI-gegevensset. Voordat u begint, downloadt u het bestand SampleVendPaymWsReport2.xlsx en slaat u het op, dat wordt vermeld in het Help-onderwerp Een indeling voor elektronische aangifte wijzigen door een Microsoft Excel-sjabloon opnieuw toe te passen (modify-electronic-reporting-format-reapply-excel-template/).

1. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.
    * Controleer of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. beschikbaar is en gemarkeerd als Actief. Als u deze configuratieprovider niet ziet, voert u eerst de stappen uit in de procedure Een configuratieprovider maken en deze als actief markeren.  

## <a name="select-the-er-format"></a>Selecteer de ER-indeling
1. Klik op Rapportconfiguraties.
2. Vouw "Betalingsmodel" uit in de structuur.
3. Selecteer Betalingsmodel\Voorbeeldwerkbladrapport in de structuur.
4. Klik op Bijlagen.
    * Het Excel-bestand SampleVendPaymWsReport.xlsx Excel wordt momenteel gebruikt als een sjabloon voor betalingsjournaalverwerking.   
5. Klik op Openen.
    * Klik op Openen om de indeling van de Excel-sjabloon te bekijken.  
    * Bekijk de sjabloon. Deze bevat momenteel de volgende details van elke betalingsregel: rekeningnummer van leverancier, leveranciersnaam, bank, routenummer, rekeningnummer, debet, credit en valuta. Voor dit voorbeeld willen we deze lijst uitbreiden door details toe te voegen over de betalingsdatum.   
6. Sluit de pagina.

## <a name="reapply-a-new-excel-template-to-er-format"></a>Een nieuwe Excel-sjabloon opnieuw toepassen op ER-indeling
1. Klik op Ontwerper.
    * Open de conceptversie van de geselecteerde ER-indeling voor bewerking.  
2. Klik in het actievenster op Importeren.
3. Klik op Bijwerken vanuit Excel.
    * Klik op 'Sjabloon bijwerken' en selecteer vervolgens het bestand SampleVendPaymWsReport2.xlsx.  
    * Klik op Sjabloon bijwerken en blader om het eerder gedownloade bestand SampleVendPaymWsReport2.xlsx te krijgen.  
4. Klik op OK.
    * De sjabloon SampleVendPaymWsReport2.xlsx wordt toegepast. De structuur van de ER-indeling wordt gesynchroniseerd met de inhoud van de sjabloon, waarvan elementen worden toegevoegd aan de ER-indeling. Bestaande elementen in de ER-indeling die niet zijn opgenomen in de sjabloon, worden verwijderd uit de indelingsdefinitie.  
5. Selecteer in de structuur 'Excel'.
    * Het veld Sjabloon bevat nu een verwijzing naar de nieuwe sjabloon.   
6. Klik op Bijlagen.
7. Klik op Openen.
    * Klik op Openen om de indeling van de gewijzigde Excel-sjabloon te bekijken.  
    * Bekijk de sjabloon. Deze bevat nu een regel voor de betalingsdatum.   
8. Sluit de pagina.
9. Vouw in de structuur 'Excel' uit.
10. Vouw in de structuur 'Excel\PaymLines' uit.
11. Selecteer in de structuur 'Excel\Betalingsregels\Betaaldatum'.
    * De ER-indeling bevat nu één artikel meer. Er is een cel, Betaaldatum, toegevoegd aan de Excel-sjabloon.  
12. Klik op het tabblad Toewijzing.
13. Vouw in de structuur "model" uit.
14. Vouw "model\Payments" uit in de structuur.
15. Selecteer "model\Payments\Transaction date(TransactionDate)" in de structuur.
16. Klik op Binden.
    * Geef op wat voor gegevens tijdens de uitvoering aan de nieuwe cel worden toegevoegd.  
17. Klik op Opslaan.
18. Sluit de pagina.

## <a name="enable-the-modified-draft-version-of-the-er-format-for-use-in-payment-journal-processing"></a>De gewijzigde conceptversie van de ER-indeling inschakelen voor gebruik in betalingsjournaalverwerking
1. Klik in het actievenster op Configuraties.
2. Klik op Gebruikersparameters.
3. Selecteer Ja in het veld Uitvoeringsinstellingen.
4. Klik op OK.
5. Klik op Bewerken.
6. Selecteer Ja in het veld Concept uitvoeren.

## <a name="use-the-modified-draft-version-of-the-er-format-for-payment-journal-processing"></a>De gewijzigde conceptversie van de ER-indeling gebruiken voor betalingsjournaalverwerking
    * Controleer het gemaakte werkblad, inclusief nieuwe details van betalingsregels: betalingsdatum.  


