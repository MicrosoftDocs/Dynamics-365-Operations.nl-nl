---
title: Leverancierscatalogi importeren
description: Dit onderwerp beschrijft het importproces van leverancierscatalogusgegevens.
author: mkirknel
manager: AnnBe
ms.date: 03/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationRequests
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: mkirknel
ms.search.validFrom: 2018-04-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: cf81823de46da9a834f0214896b9e634989cac0e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "362022"
---
# <a name="import-vendor-catalogs"></a>Leverancierscatalogi importeren
[!include[banner](../includes/banner.md)]

## <a name="vendor-catalogs-import"></a>Leverancierscatalogi importeren

In Microsoft Dynamics 365 for Finance and Operations kunnen inkoopprofessionals catalogi maken en onderhouden die werknemers van het bedrijf kunnen gebruiken wanneer ze artikelen en services voor intern gebruik bestellen. Wanneer u een aanschaffingscatalogus maakt, kunt u de artikelen en diensten toevoegen die u beschikbaar wilt maken voor werknemers door de gegevens van de productcatalogus te importeren of door de gegevens van de productcatalogus handmatig aan het productmodel toe te voegen. 

U kunt catalogusgegevens die zijn ingediend door een leverancier uploaden vanuit de Microsoft Dynamics 365-client.

De productgegevens die een leverancier bij u indient in het formulier van een CMR-bestand (Catalog Maintenance Request) moeten de XML-bestandsindeling hebben. Het CMR-bestand moet gegevens bevatten voor de producten die de leveranciers aan uw bedrijf levert.

## <a name="import-vendor-catalog-data"></a>Leverancierscatalogusgegevens importeren

U moet de volgende taken uitvoeren om leverancierscatalogusgegevens te importeren:

1.  Stel een project in in het werkgebied Gegevensbeheer waar u uw toewijzingsregels voor gegevens hebt gedefinieerd. Selecteer **Gegevensbeheer** en selecteer vervolgens **Rollen voor gegevensprojecten instellen**. 

2.  Stel een hiërarchie van aanschaffingscategorieën in en wijs uw leveranciers aan aanschaffingscategorieën toe. Als u basisproductcodes gebruikt, voegt u de basisproductcodes aan de aanschaffingscategorieën toe. Zie [Een hiërarchie van aanschaffingscategorieën instellen](../procurement/tasks/set-up-procurement-category-hierarchy.md) voor informatie over het instellen van een hiërarchie van aanschaffingscategorieën.

3.  Configureer de leveranciers voor het importeren van catalogi. Selecteer een leverancier en selecteer vervolgens **Inkoop** > **Instellen** > **Leverancier configureren voor importeren van catalogus**.

4.  Configureer de workflow voor het importeren van catalogi. Maak een CMR-bestandssjabloon en deel deze met uw leverancier.

5.  Selecteer **Inkoop en sourcing** \> **Algemeen** \> **Catalogi** \> **Leverancierscatalogi** voor het maken van een leverancierscatalogus. De catalog maintenance request (CMR)-bestanden die u van uw leverancier ontvangt, worden in deze catalogus gegroepeerd. 

6.  Upload het CMR-bestand.

7.  De producten controleren, goedkeuren of afwijzen in de leverancierscatalogus. De producten worden automatisch toegewezen aan de aanschaffingscategorieën in Dynamics 365 for Finance and Operations. 
    
Goedgekeurde producten worden toegevoegd aan het productmodel en worden vrijgegeven aan de geselecteerde rechtspersonen. Alleen goedgekeurde producten kunnen aan de aanschaffingscatalogus worden toegevoegd.

## <a name="generate-a-catalog-import-file-template"></a>Een sjabloon voor een catalogusimportbestand

De sjabloon voor het catalogusimportbestand is een XSD-bestand dat u kunt gebruiken voor het maken van een CMR-bestand voor de producten van de leverancier. U kunt het CMR-bestand gebruiken voor het maken van een nieuwe catalogus, het vervangen van een bestaande catalogus of het wijzigen van een bestaande catalogus.

1.  Selecteer **Inkoop en sourcing** \> **Catalogi** \> **Leverancierscatalogi** en dubbelklik op de catalogus die u wilt bewerken.

2.  Download een bestaande sjabloon voor catalogusimport (XSD-bestand). Op de pagina **Catalogus bijwerken** klikt u in het **actievenster**op het tabblad **Catalogi** in de groep **Verwante informatie** op **Catalogussjabloon genereren** en selecteert u **Aanschaffingscategorie**.

    -   Met de optie **Aanschaffingscategorie** kunt u een catalogussjabloon genereren die de aanschaffingscategorieën bevat waarvoor de leverancier producten mag leveren.

3. Selecteer in het dialoogvenster **Opslaan als** de locatie waar u de sjabloon voor het catalogusbestand wilt opslaan, waarna u het bestand opslaat.

Voor meer informatie en voorbeelden verwijzen we naar dit blogbericht: [Leverancierscatalogi in Dynamics AX.](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/)
