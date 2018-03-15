--- 
title: " Een overzicht maken, berekenen en boeken voor een detailhandelwinkel"
description: Deze procedure doorloopt de handmatige stappen voor het maken, berekenen en boeken van een overzicht voor een winkel.
author: jashanno
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 33ebb28196baa9ae944dbd124274b05cb587fea4
ms.contentlocale: nl-nl
ms.lasthandoff: 02/07/2018

---
# <a name="create-calculate-and-post-a-statement-for-a-retail-store"></a> Een overzicht maken, berekenen en boeken voor een detailhandelwinkel

[!include[task guide banner](../includes/task-guide-banner.md)]

Deze procedure doorloopt de handmatige stappen voor het maken, berekenen en boeken van een overzicht voor een winkel. Er zijn ook batchtaken die voor dezelfde taken kunnen worden geconfigureerd. De stappen voor het configureren en uitvoeren van de batchtaken kunnen in andere onderwerpen worden gevonden. Als u deze procedure wilt voltooien, moet u transacties hebben die in POS zijn voltooid en vervolgens in Dynamics AX zijn opgehaald. Deze registratie gebruikt het demobedrijf USRT. In deze procedure kan worden verwezen naar Microsoft Dynamics AX. Houd er rekening mee dat Dynamics AX nu Microsoft Dynamics 365 for Operations wordt genoemd.

1. Ga naar Alle werkgebieden > .. > Financiën van detailhandelwinkel.
2. Klik op Nieuw overzicht.
3. Klik in het veld Winkelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Klik in de lijst op de koppeling in de geselecteerde rij.
5. Klik op OK.
    * De instellingengroep bevat de instellingen die bepalen welke transacties in het overzicht worden opgenomen en hoe ze in overzichtsregels worden gegroepeerd. U kunt de instellingengroep openen en deze instellingen wijzigen of u kunt de standaardwaarden gebruiken.  
    * Het veld Overzichtsmethode bepaalt hoe de overzichtsregels worden gegroepeerd.  
    * Selecteer een personeelslid of een register als u alleen een overzicht wilt berekenen voor dat specifieke personeelslid of register.  
6. Selecteer een optie in het veld Afsluitingsmethode.
7. Klik op Overzicht berekenen.
8. Klik op Ja.
    * Na het berekenen van het overzicht moeten er regels zijn gemaakt met totale bedragen voor elke betalingsmethode en de overzichtsmethode die is gebruikt.  
    * Voer een geteld bedrag op elke regel in als het moet worden ingevoerd of bijgewerkt. Het getelde veld wordt gevuld met bedragen van kascontroles die in POS zijn uitgevoerd.  
9. Klik op Overzicht boeken.
10. Klik op Sluiten.
11. Ga naar Detailhandel en commerce > Kanalen > Financiën van detailhandelwinkel.
12. Klik op het tabblad Geboekte overzichten.


