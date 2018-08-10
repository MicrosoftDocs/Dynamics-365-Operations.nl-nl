--- 
title: Btw-overeenkomst en -overschrijvingen
description: Deze procedure laat zien hoe u btw-groepen kunt toewijzen aan detailhandelkanalen.
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 816e00e4238cb0d90a2aea9b2bc070d31504c2ce
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="sales-tax-assignment-and-overrides"></a>Btw-overeenkomst en -overschrijvingen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u btw-groepen kunt toewijzen aan detailhandelkanalen. Ook wordt het proces doorlopen van het maken van een nieuwe btw-overschrijving en het toewijzen hiervan aan een bestaande groep voor btw-overschrijving. Deze procedure

gebruikt het demobedrijf USRT.

1. Ga naar Detailhandel en commerce > Kanalen > Detailhandelwinkels > Alle detailhandelwinkels.
2. Klik in de lijst op de koppeling Id van detailhandelafzetkanaal voor "Houston".
3. Klik op Bewerken.
    * Het veld Btw-groep bevat de lijst met btw-groepen voor het huidige bedrijf. De huidige toegewezen groep is een algemene btw-groep genaamd "Texas". Er zijn ook btw-groepen voor 'Washington' en 'Washington, King County.' Btw-groepen kunnen van toepassing zijnde belastingen voor meerdere gemeenten bevatten.  
    * In het veld Btw-overschrijving kunnen groepen voor btw-overschrijving aan het kanaal worden toegewezen. Groepen voor btw-overschrijving kunnen worden gebruikt om btw-overschrijvingen te groeperen die werken voor meerdere winkelen. In plaats van btw-overschrijvingen handmatig één voor één toe te wijzen, kan de groep worden gemaakt en rechtstreeks aan de kanalen worden toegewezen om tijd te besparen.  
4. Klik op Opslaan.
5. Sluit de pagina.
6. Ga naar Detailhandel en commerce > Kanaalinstellingen > Btw > Btw-overschrijvingen.
7. Klik op Nieuw.
8. Geef in het veld Btw-overschrijving een naam op voor uw nieuwe overschrijving.
9. Neem in het veld Omschrijving een beschrijving van de overschrijving op.
10. Stel de status in op "Inschakelen".
11. Vouw de sectie Overschrijving uit of samen.
12. Selecteer een optie in het veld Type.
    * Btw-groepen voor artikel kunnen worden gebruikt om de btw te negeren voor specifieke artikelen die bij de groep behoren. Zo worden bijvoorbeeld voedingsartikelen meestal anders belast dan harde goederen en hebben waarschijnlijk een eigen btw-groep.     Btw-groepen zijn groepen belastingen op een bepaald kanaal van toepassing zijn. Als bijvoorbeeld een kanaal zowel aan de detailhandel als business-to-business verkoopt, kunnen verschillende btw-groepen voor artikelen worden gebruikt. Alle relevante belastingen worden dan aan de btw-groep toegewezen.  
    * U kunt nu de "Vanaf"- en "T/m"-btw of "Vanaf btw-groep" en "T/m btw-groep" selecteren om uw eigen btw-overschrijving te maken.    Het veld "Vanaf" geeft de btw of btw-groep aan die moet worden overschreven. Overschrijving van btw-groep van artikel biedt andere opties dan overschrijving van btw-groep.    Btw-overschrijvingen kunnen worden ingesteld voor het overschrijven van btw over hele transacties of over specifieke regels in de transactie.  
13. Klik op Opslaan.
14. Sluit de pagina.
15. Ga naar Detailhandel en commerce > Kanaalinstellingen > Btw > Groepen voor btw-overschrijving.
    * In deze stap gaat u de nieuw gemaakte btw-overschrijving toewijzen aan de groep voor btw-overschrijving die is toegewezen aan het Houston-kanaal.  
16. Klik op Bewerken.
17. Vouw de sectie Instellingen uit of samen.
18. Klik op Toevoegen.
19. Klik in het veld Btw-overschrijving op de vervolgkeuzeknop om de zoekopdracht te openen.
20. Selecteer de eerder gemaakte btw-overschrijving in de lijst.
21. Klik in de lijst op de koppeling in de geselecteerde rij.
22. Klik op Opslaan.


