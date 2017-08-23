--- 
title: Configuraties genereren met een update van toepassingsgegevens voor elektronische aangifte (ER)
description: 'Als u de stappen in deze procedure wilt voltooien, moet u eerst de procedure ''ER Documenten genereren met update van toepassingsgegevens (deel 1: Configuraties importeren)'' voltooien.'
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: f10faaaffeb7df5be0b37a9b8dbfa5db5c24d2a2
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="generate-documents-with-application-data-update-for-electronic-reporting-er"></a>Configuraties genereren met een update van toepassingsgegevens voor elektronische aangifte (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Als u de stappen in deze procedure wilt voltooien, moet u eerst de procedure 'ER Documenten genereren met update van toepassingsgegevens (deel 1: configuraties importeren)' voltooien.



De stappen in deze procedure leggen uit hoe u ER-configuraties ontwerpt om een elektronisch document te genereren. In deze procedure voert u de geïmporteerde ER-indelingsconfiguraties uit die zijn gemaakt voor het voorbeeldbedrijf, Litware, Inc. om elektronische documenten te genereren.



Deze procedure is gemaakt voor gebruikers met de toegewezen rol van systeembeheerder of elektronische aangifteontwikkelaar. Deze stappen kunnen worden voltooid met de DEMF-gegevensset. 



Voordat u begint, moet u de context van het land/de regio wijzigen voor het DEMF-bedrijf, van DEU (Duitsland) naar BEL (België). Klik op Organisatiebeheer > Organisaties > Rechtspersonen om de land/regio-code bij te werken in het primaire adres van de rechtspersoon DEMF. Start uw toepassing opnieuw.


## <a name="run-imported-er-format"></a>Geïmporteerde ER-indeling uitvoeren
1. Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.
2. Vouw in de structuur 'Intrastat (model)' uit.
3. Selecteer in de structuur 'Intrastat (model)\Intrastat (indeling)'.
4. Klik op Uitvoeren.
    * Voer de conceptversie van de ER-indelingsconfiguratie uit om het Intrastat-rapport te genereren.  
5. Typ in het veld Invoeren 'intrastat.xml'.
    * Geef de naam van het bestand op.  
6. Klik op OK.
    * Bekijk het gegenereerde XML-bestand.  
7. Sluit de pagina.
8. Ga naar Belasting > Aangiften > Buitenlandse handel > Intrastat.
    * Open dit formulier om de Intrastat-transacties weer te geven die zijn opgenomen in het gegenereerde elektronische document.  
9. Klik op Intrastat-archief.
    * Omdat de uitgevoerde ER-indeling geen instellingen voor het bijwerken van toepassingsgegevens bevat, zijn de details van het voltooide Intrastat-rapport niet gearchiveerd.  
10. Sluit de pagina.
11. Sluit de pagina.


