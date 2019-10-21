---
title: Externe catalogus instellen voor PunchOut eProcurement
description: In dit onderwerp wordt het gebruik beschreven van een externe of punchout-catalogus voor het verzamelen van offertegegevens van een leverancier en het toevoegen ervan aan een bestelopdracht.
author: mkirknel
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e9b6c3cb5b6bbc83604bee11a2472b2ad1136269
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249378"
---
# <a name="set-up-an-external-catalog-for-punchout-eprocurement"></a>Externe catalogus instellen voor PunchOut eProcurement

[!include [banner](../includes/banner.md)]

Met de externe catalogus zorgt u ervoor dat de product- en prijsinformatie die u vervolgens in Dynamics 365 for Finance and Operations juli 2017 verwerkt, nauwkeurig en up-to-date is. De bestelopdracht kan vervolgens worden goedgekeurd en geconverteerd naar een inkooporder en een order kan bij de leverancier worden geplaatst.

Wanneer de externe catalogus is ingesteld en een werknemer een bestelopdracht voorbereidt, is er een optie om door te leiden naar een externe site, de externe catalogus, en de winkelwagen te retourneren die is gemaakt op de externe site. Deze mededeling is gebaseerd op het protocol cXML en moet worden ingesteld tussen de systemen van de kopende organisatie en de verkopende organisatie.

Om de communicatie in te stellen, moet uw leverancier gegevens leveren die u moet gebruiken in de configuratie van de externe catalogus, zoals identiteit, het domein van het kopende bedrijf, bijvoorbeeld 'DUNS' en 'DUNS-nummer', aanmeldgegevens en de URL naar de leverancierscatalogus.

## <a name="setting-up-an-external-catalog"></a>Een externe catalogus instellen

De externe catalogus moet ervoor zorgen dat een werknemer die een opdracht tot inkoop invoert, wordt omgeleid naar een externe site om producten te selecteren. De producten die de werknemer selecteert uit de externe catalogus worden geretourneerd met actuele prijsinformatie. Van daaruit kunnen ze worden toegevoegd aan de opdracht tot inkoop. Het is niet de bedoeling om werknemers in staat te stellen een order te plaatsen op de externe site. Wanneer u de externe catalogus instelt, moet u zorgen dat het doel van de locatie die toegankelijk is voor de externe catalogus is om offerte-informatie te verzamelen en niet om een echte bestelling te plaatsen.

### <a name="to-set-up-an-external-vendor-catalog-complete-the-following-tasks"></a>Voer de volgende taken uit om een externe leverancierscatalogus in te stellen:

1. Een hiërarchie van aanschaffingscategorieën instellen. Zie voor meer informatie [Beleid instellen voor categoriehiërarchieën voor aanschaffing](tasks/set-up-policies-procurement-category-hierarchies.md).
2. Registreer de leverancier in Supply Chain Management. Voordat u configuraties kunt instellen om toegang te krijgen tot de externe leverancierscatalogus, moet u de leverancier en de contactpersoon van de leverancier eerst instellen in Microsoft Dynamics 365. De leverancier van de externe catalogus moet ook aan de geselecteerde aanschaffingscategorie worden toegevoegd. Zie voor meer informatie over het registreren van leveranciers het onderwerp [Gebruikers van leverancierssamenwerking beheren](manage-vendor-collaboration-users.md). Zie voor uitleg over het toewijzen van leveranciers aan een inkoopcategorie het onderwerp [Leveranciers goedkeuren voor specifieke aanschaffingscategorieën](tasks/approve-vendors-specific-procurement-categories.md).
3. Let erop dat de maateenheden en de valuta waarmee de leverancier werkt, zijn ingesteld. Zie voor informatie over het maken van een maateenheid [Maateenheden beheren](../pim/tasks/manage-unit-measure.md).
4. Configureer de externe leverancierscatalogus op basis van de vereisten voor de externe catalogussite van uw leverancier. Zie [De externe leverancierscatalogus configureren](#configure-the-external-vendor-catalog) voor meer informatie over deze taak.
5. Test de configuraties van de externe catalogus van de leverancier om te verifiëren dat de instellingen geldig zijn en dat u toegang kunt krijgen tot de externe leverancierscatalogus. Gebruik de actie **Instellingen valideren** om het bericht voor instellen van de aanvraag te valideren, dat u hebt gedefinieerd. Dit bericht moet ervoor zorgen dat de externe catalogussite van de leverancier wordt geopend in een browservenster. Zolang de validatie duurt, kunt u geen artikelen en services bij de leverancier bestellen. Om artikelen en diensten te bestellen, moet u de catalogus van de leverancier benaderen via een opdracht tot inkoop.
6. Activeer de externe catalogus door middel van de knop **Catalogus activeren** op de pagina **Externe catalogi**. De externe catalogus moet worden geactiveerd voordat werknemers deze kunnen gebruiken. U kunt de externe catalogus op elk gewenst moment uitschakelen.


## <a name="configure-the-external-vendor-catalog"></a>De externe leverancierscatalogus configureren

Deze sectie biedt meer details over taak 4 uit de vorige sectie.

1. Voer een naam en omschrijving in voor de externe leverancierscatalogus. De naam die u invoert, wordt weergegeven op de winkelwagen die de externe catalogus vertegenwoordigt die wordt weergegeven aan werknemers die een opdracht tot inkoop maken. Een werknemer kan op de winkelwagen klikken om de catalogus te openen op de externe catalogussite van de leverancier.
2. Voeg een afbeelding toe met behulp van de actie  **Externe catalogusafbeelding**. De afbeelding wordt weergegeven op de winkelwagen die de externe catalogus vertegenwoordigt die wordt weergegeven aan werknemers die een opdracht tot inkoop maken. Houd er rekening mee dat de breedte en hoogte van de afbeelding gelijk moeten zijn. Anders wordt de afbeelding niet correct weergegeven.
3. Geef aan of de externe cataloguswebsite van de leverancier moet worden weergegeven in hetzelfde browservenster als waarin de werknemer de inkoopopdracht heeft gemaakt, of dat deze in een nieuw venster wordt geopend.
4. Selecteer de leverancier voor de catalogus. In de lijst **Rechtspersonen** is er een rij voor elke rechtspersoon waarvoor de leverancier is ingesteld. Als u wilt toestaan dat gebruikers producten rechtstreeks uit de catalogus van de leverancier bestellen in sommige rechtspersonen maar niet in andere, kunt u dit instellen met de knoppen **Toegang voorkomen** of **Toegang toestaan** voor elke rechtspersoon waarvoor u de catalogus al dan niet toegankelijk wilt maken.
5. Voer in het veld **Standaardvervalperiode (dagen)** het aantal dagen in dat een offerte uit de externe catalogus geldig is en kan worden gebruikt om in te kopen bij de externe leverancier. Wanneer een offerte wordt gemaakt en opgehaald van de externe catalogussite van de leverancier, dan is de offerte geldig met ingang van de huidige systeemdatum en blijft geldig gedurende het aantal dagen dat u in dit veld invoert.
6. Klik op de knop **Toevoegen** om de aanschaffingscategorieën aan de externe catalogus toe te wijzen. Selecteer vervolgens een categorie in de lijst Categorienaam. De lijst met categorieën is een superset van aanschaffingscategorieën waaraan de leverancier is toegewezen in alle rechtspersonen die zijn ingesteld voor de leverancier.

    > [!NOTE]
    > Aanschaffingsbeleidsregels worden gebruikt om toegang tot categorieën toe te staan of te verbieden voor de kopende rechtspersoon of de ontvangende operationele eenheid. Punchout naar een externe catalogus vereist dat toegang wordt toegestaan tot tenminste één van de aanschaffingscategorieën die is toegewezen aan de catalogus.

7. Stel het cXML bericht voor instellen van de aanvraag in, dat wordt verzonden naar de leverancier. De automatisch gegenereerde berichtindeling is de minimale sjabloon die is vereist om een sessie starten. Vul waarden in voor de codes.

U kunt op elk gewenst moment de door het systeem gegenereerde berichtsjabloon laden door te klikken op **Berichtindeling herstellen**. 
Houd er rekening mee dat als u de berichtindeling herstelt, het huidige bericht wordt vervangen door de automatisch gegenereerde berichtindeling met lege codes.

### <a name="cxml-setup-message"></a>cXML-instellingsbericht
Hieronder volgt een beschrijving van de codes die zijn opgenomen in de sjabloon:

| Veld | Omschrijving | 
|---------|---------|
|< Header >< From >< Credential domain=”” >|Het domein van het bedrijf van de koper.|
|< Header >< From >< Credential>< Identity >< /Identity > | De identiteit van het bedrijf van de koper.|
|< Header >< To >< Credential domain=”” > | Het domein van het bedrijf van de leverancier.|
|< Header >< To >< Credential>< Identity >< /Identity> | De identiteit van het bedrijf van de leverancier.|
|< Header >< Sender >< Credential domain=”” > | Het domein van het bedrijf van de koper.|
|< Header >< Sender >< Credential >< Identity >< /Identity> | De identiteit van het bedrijf van de koper.|
|< Header >< Sender >< Credential >< SharedSecret >< /SharedSecret >|Het gedeelde geheim voor het bedrijf van de koper.|
|< Request deploymentMode=”” >|De test- of productie-implementatie.|
|< Request >< PunchOutSetupRequest >< SupplierSetup >< URL >< /URL>|De URL van het punch-outeindpunt van de leverancier.|

### <a name="extrinsic-elements"></a>Extrinsieke elementen

Een extrinsiek element is extra informatie, zoals een gebruikersnaam die is gebaseerd op een gebruiker die een punch-out uitvoert. Het extrinsieke element wordt ingesteld wanneer de punch-out plaatsvindt en kan worden verzonden in het aanvraaginstellingsbericht.
Uw leverancier kan een vereiste hanteren voor het ontvangen van een extrinsiek element in de instellingsaanvraag. In dat geval moet u het extrinsieke element toevoegen aan de lijst met extrinsieke elementen in de sectie **Berichtindeling** van de pagina **Externe catalogus**. Geef een naam op voor het extrinsieke element dat de leverancier kan herkennen, en wijs deze toe aan een waarde. De opties voor waarden zijn: User name, User email of Random value.
Zie voor meer informatie over het cXML-protocol de [cXML.org-website](http://cxml.org/).

## <a name="post-back-message"></a>Terugpostbericht
Het terugpostbericht is het bericht dat wordt ontvangen van de leverancier wanneer de gebruiker bij de externe site uitcheckt en terugkeert naar Supply Chain Management. Terugpostberichten kunnen worden niet geconfigureerd. De berichten zijn gebaseerd op de definitie van het cXML-protocol. Hier is de informatie die deel kan uitmaken van het terugpostbericht dat is ontvangen voor een inkoopregel.

| Bericht ontvangen van leverancier | Gekopieerd naar inkoopregel|
|------------------------------|----------------------------------------------------------|
|< ItemIn quantity=”” > |Hoeveelheid|
|< ItemIn>< ItemID >< SupplierPartID >< /SupplierPartID >|Extern artikel-id|
|< ItemDetail>< UnitPrice >< Money currency=”” >| Valuta|
|< ItemDetail >< UnitPrice >< Money >< /Money >| Eenheidsprijs|
|< ItemDetail >< Description ShortName=”” >|Productnaam|
|< ItemDetail >< Description >< /Description >|Opgenomen in artikelbeschrijving; productnaam als ShortName niet is opgegeven.|
|< ItemDetail >< UnitOfMeasure >< /UnitOfMeasure >|Eenheid|
|< ItemDetail >< Classification >< /Classification >|Opgenomen in artikelbeschrijving|
|< ItemDetail >< Classification domain=”” >|Opgenomen in artikelbeschrijving|

## <a name="delete-an-external-catalog"></a>Een externe catalogus verwijderen
Een externe catalogus verwijderen met de actie Verwijderen op de pagina.

Als een product in de catalogus van de externe leverancier is aangevraagd, kan de externe leverancierscatalogus niet gewist worden. In plaats daarvan wordt de status van de externe leverancierscatalogus ingesteld op inactief. Als u de alleen toegang tot de externe leverancierscatalogussite wilt verwijderen zonder de catalogussite te verwijderen, wijzigt u de status van de externe catalogus naar Inactief.

