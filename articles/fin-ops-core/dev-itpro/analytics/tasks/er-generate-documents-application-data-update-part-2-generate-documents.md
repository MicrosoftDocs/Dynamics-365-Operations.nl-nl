---
title: Configuraties ontwerpen voor het genereren van documenten die toepassingsgegevens bevatten
description: Dit artikel laat zien hoe u configuraties voor elektronische rapportage (ER) ontwerpt voor het genereren van elektronische documenten. (Deel 1 - Configuraties importeren).
author: kfend
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8494f54c6f84e63e75469aa9d80d090c050b0f7f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290539"
---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a>Configuraties ontwerpen voor het genereren van documenten die toepassingsgegevens bevatten

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
