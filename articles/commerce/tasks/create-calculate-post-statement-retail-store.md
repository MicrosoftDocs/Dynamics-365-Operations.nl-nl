---
title: Overzichten maken, berekenen en boeken voor een detailhandelwinkel
description: In dit artikel worden de handmatige stappen beschreven voor het maken, berekenen en boeken van een overzicht voor een winkel.
author: jashanno
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 740857e6a902e21588855eef5e36cac68e560898
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873273"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a>Overzichten maken, berekenen en boeken voor een detailhandelwinkel

[!include [banner](../includes/banner.md)]

In dit artikel worden de handmatige stappen beschreven voor het maken, berekenen en boeken van een overzicht voor een winkel. Er zijn ook batchtaken die voor dezelfde taken kunnen worden geconfigureerd. De stappen voor het configureren en uitvoeren van de batchtaken kunnen in andere artikelen worden gevonden. Als u deze procedure wilt voltooien, moet u transacties hebben die in POS zijn voltooid en vervolgens in Dynamics 365 Commerce zijn opgehaald. Deze registratie gebruikt het demobedrijf USRT.

1. Selecteer **Financiën van winkel** op de startpagina.
2. Selecteer **Nieuw overzicht**.
3. Selecteer in het veld **Winkelnummer** een optie in het vervolgkeuzemenu.
4. Selecteer **OK**.
5. De groep **Instellingen** bevat de instellingen die bepalen welke transacties in het overzicht worden opgenomen en hoe ze in overzichtsregels worden gegroepeerd. U kunt de groep **Instellingen** openen en deze instellingen wijzigen of u kunt de standaardwaarden gebruiken.  
    - Het veld **Overzichtsmethode** bepaalt hoe de overzichtsregels worden gegroepeerd.  
    - Selecteer een personeelslid of een register in het veld **Personeel/kassa** als u alleen een overzicht wilt berekenen voor dat specifieke personeelslid of die specifieke kassa.  
6. Selecteer een optie in het veld **Afsluitingsmethode**.
7. Selecteer **Overzicht berekenen** in het actievenster.
8. Selecteer **Ja**.
    - Na het berekenen van het overzicht moeten er regels zijn gemaakt met totale bedragen voor elke betalingsmethode en de overzichtsmethode die is gebruikt.  
    - Voer een geteld bedrag op elke regel in als het moet worden ingevoerd of bijgewerkt. Het getelde veld wordt gevuld met bedragen van kascontroles die in POS zijn uitgevoerd.  
9. Selecteer **Overzicht boeken** in het actievenster.
10. Selecteer **Sluiten**.
11. Sluit het deelvenster.
12. Selecteer **Financiën van winkel** op de startpagina.
13. Selecteer het tabblad **Geboekte overzichten**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]