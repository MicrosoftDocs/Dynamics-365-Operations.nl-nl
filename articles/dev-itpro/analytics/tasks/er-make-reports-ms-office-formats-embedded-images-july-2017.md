---
title: Configuraties ontwerpen voor het genereren van rapporten in Office-indeling die ingesloten afbeeldingen bevatten
description: De stappen in dit onderwerp geven informatie over hoe u elektronische rapportage (ER)-configuraties ontwerpt die elektronische documenten in Microsoft Office-indelingen (Excel en Word) genereren die ingesloten afbeeldingen bevatten.
author: NickSelin
manager: AnnBe
ms.date: 01/23/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1fb02e561f6792c57b924ba64a5ca3d3974289ee
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544398"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a>Configuraties ontwerpen voor het genereren van rapporten in Office-indeling die ingesloten afbeeldingen bevatten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Als u de stappen in deze procedure wilt voltooien, moet u eerst de procedure 'ER Een configuratieprovider maken en deze als actief markeren' voltooien. Deze procedure laat zien hoe u elektronische rapportage (ER)-configuraties ontwerpt voor het genereren van een elektronisch Microsoft Excel- of Word-document met ingesloten afbeeldingen. In deze procedure maakt u de vereiste ER-configuraties voor het voorbeeldbedrijf Litware, Inc. Deze stappen kunnen worden uitgevoerd met behulp van de dataset USMF. Deze procedure is gemaakt voor gebruikers met de toegewezen rol van systeembeheerder of elektronische aangifteontwikkelaar. Voordat u begint, downloadt u de bestanden vermeld in het Help-onderwerp [Afbeeldingen en vormen insluiten in bedrijfsdocumenten die zijn gegenereerd via het hulpmiddel voor elektronische aangifte](../electronic-reporting-embed-images-shapes.md) en slaat u ze op. De bestanden zijn: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png en Cheque template Word.docx.

## <a name="verify-prerequisites"></a>Vereisten controleren  
 1. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.  
 2. Controleer of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. beschikbaar is en gemarkeerd als Actief. Als u deze configuratieprovider niet ziet, voert u eerst de stappen uit in de procedure 'Een configuratieprovider maken en deze als actief markeren'.   
 3. Klik op Rapportconfiguraties.  
 
## <a name="add-a-new-er-model-configuration"></a>Een nieuwe ER-modelconfiguratie toevoegen  
 1. In plaats van een nieuw model te maken kunt u het ER-modelconfiguratiebestand (Model voor cheques.xml) laden dat u eerder hebt opgeslagen. Dit bestand bevat het voorbeeldgegevensmodel voor betaalcheques en de toewijzing van het gegevensmodel aan de gegevensonderdelen van de toepassing Dynamics 365 for Operations.   
 2. Klik op het sneltabblad Versies op Uitwisselen.   
 3. Klik op Laden uit XML-bestand.  
 4. Klik op Bladeren en selecteer vervolgens Model voor cheques.xml.   
 5. Klik op OK.  
 6. Het geladen model wordt gebruikt als een gegevensbron met informatie voor het genereren van documenten met afbeeldingen in Excel en Word.  

## <a name="add-a-new-er-format-configuration"></a>Een nieuwe ER-indelingsconfiguratie toevoegen  
 1. In plaats van een nieuwe indeling te maken kunt u het ER-indelingsconfiguratiebestand (Afdrukindeling van cheques.xml) laden dat u eerder hebt opgeslagen. Dit bestand bevat de voorbeeldindeling voor het afdrukken van cheques met behulp van het voorgedrukte formulier en de toewijzing van deze indeling voor het gegevensmodel 'Model voor cheques'.   
 2. Klik op Uitwisselen.  
 3. Klik op Laden uit XML-bestand.  
 4. Klik op Bladeren en selecteer het bestand Afdrukindeling van cheques.xml.   
 5. Klik op OK.  
 6. Vouw in de structuur 'Model voor cheques' uit.  
 7. Selecteer in de structuur ' Model voor cheques\Afdrukindeling van cheques'.  
 8. De geladen indeling wordt gebruikt voor het genereren van documenten met afbeeldingen in Excel en Word.   

## <a name="configure-er-user-parameters"></a>ER-gebruikersparameters configureren  
 1. Klik in het actievenster op Configuraties.  
 2. Klik op Gebruikersparameters.  
 3. Selecteer Ja in het veld Uitvoeringsinstellingen.  
  Schakel de markering 'Concept uitvoeren' in om de conceptversie van de geselecteerde indeling te starten in plaats van de voltooide.  
 4. Klik op OK.  

## <a name="configure-cash--bank-management-parameters"></a>Parameters voor cash- en bankbeheer configureren  
 1. Ga naar Contanten en bankbeheer > Bankrekeningen > Bankrekeningen.  
 2. Gebruik het snelfilter om op het veld Bankrekening te filteren met de waarde 'USMF OPER'.  
 3. Klik in het actievenster op Instellen.  
 4. Klik op Controleren.  
 5. Vouw de sectie Instellingen uit.  
 6. Klik op Bewerken.  
 7. Selecteer Ja in het veld Bedrijfslogo.  
 8. Klik op Bedrijfslogo.  
 9. Klik op Wijzigen.  
 10. Klik op Bladeren en selecteer het bestand dat u eerder hebt gedownload, Bedrijfslogo.png.   
 11. Klik op Opslaan.  
 12. Sluit de pagina.  
 13. Vouw de sectie Handtekening uit.  
 14. Selecteer Ja in het veld Eerste handtekening afdrukken.  
 15. Klik op Wijzigen.  
 16. Klik op Bladeren en selecteer het bestand dat u eerder hebt gedownload, Afbeelding handtekening.png.   
 17. Vouw de sectie Aantal exemplaren uit.  
 18. Selecteer een optie in het veld Watermerk.  
 19. Selecteer Ja in het veld Algemene elektronische exportindeling.  
 20. Selecteer Configuratie 'afdrukindeling van cheques'.  
 21. Nu wordt de geselecteerde ER-indeling gebruikt voor het afdrukken van cheques.  
 22. Klik op Koppelen.  
 23. Klik op Nieuw.  
 24. Klik op Bestand.  
 25. Klik op Bladeren en selecteer het bestand dat u eerder hebt gedownload, Afbeelding handtekening 2.png.   
 26. Sluit de pagina.  
 27. Sluit de pagina.  
 28. Sluit de pagina.  
 29. Ga naar Contanten en bankbeheer > Instellingen > Parameters voor kas- en bankbeheer.  
 30. Selecteer Ja in het veld Voorafmelding maken toestaan voor inactieve bankrekeningen:.  
 31. Klik op Opslaan.  
 32. Sluit de pagina.  
