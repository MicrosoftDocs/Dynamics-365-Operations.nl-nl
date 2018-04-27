---
title: Leverancierssamenwerking met klanten
description: In dit onderwerp wordt beschreven hoe u leverancierssamenwerking kunt gebruiken om met inkooporders te werken en consignatievoorraad te bewaken in Microsoft Dynamics 365 for Finance and Operations.
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ConsignmentProductReceiptLines, ConsignmentVendorPortalOnHand, PurchVendorPortalConfirmedOrders, PurchVendorPortalOriginalOrder, PurchVendorPortalResponsesHistoryList, PurchVendorPortalResponsesPart
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 221234
ms.assetid: 6e69fb8b-6d3a-46ef-88cf-6d01212aa7c3
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 4252112272e2f86c2c18dc399a713bf652e4228e
ms.contentlocale: nl-nl
ms.lasthandoff: 03/26/2018

---

# <a name="vendor-collaboration-with-customers"></a>Leverancierssamenwerking met klanten

[!INCLUDE [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u leverancierssamenwerking kunt gebruiken om met klanten te werken in Microsoft Dynamics 365 for Finance and Operations. Leveranciers kunnen een reeks bedrijfsprocessen voltooien vanuit de volgende werkgebieden:

- **Inkooporderbevestiging**: controleer inkooporders en reageer hierop.
- **Biedingen van leverancier**: bekijk offerteaanvragen en reageer hierop door te bieden.
- **Leveranciersgegevens**: bekijk modelgegevens van leveranciers en werk deze bij.
- **Facturering**: werk met facturen. In dit onderwerp komt het werkgebied **Facturering** niet aan bod. Zie [Werkgebied voor samenwerkingsfacturering van leveranciers](../../financials/accounts-payable/vendor-portal-invoicing-workspace.md) voor meer informatie over dit werkgebied.

Leveranciers kunnen ook informatie over de consignatievoorraad controleren.

## <a name="working-with-pos-in-the-purchase-order-confirmation-workspace"></a>Werken met inkooporders in het werkgebied Inkooporderbevestiging

In het werkgebied **Inkooporderbevestiging** kunt u reageren op de inkooporders die ter beoordeling naar u zijn verzonden. Daarnaast kunt u informatie weergeven over inkooporders die wachten op actie van de klant en inkooporders die zijn bevestigd, maar nog openstaan.

Er zijn drie lijsten in de werkruimte **Inkooporderbevestiging**:

- **Inkooporders ter beoordeling**: deze lijst bevat inkooporders die aan u zijn verzonden en op een reactie van u wachten. Als u reageert, verdwijnt de inkooporder uit de lijst. Als de klant u een nieuwe versie van de inkooporder stuurt voordat u de vorige hebt beantwoord, wordt alleen de laatste versie weergegeven.
- **In afwachting van actie van klant**: in deze lijst worden alle inkooporders weergegeven waarop u hebt gereageerd, maar die nog niet door de klant zijn bevestigd. Als u een inkooporder accepteert, kunt u deze order in deze lijst blijven controleren totdat de status in **Bevestigd** wordt gewijzigd. Als u een inkooporder afwijst of met wijzigingen accepteert, kunt u de inkooporder hier controleren tot de klant een nieuwe versie stuurt.
- **Bevestigde inkooporders openen**: deze lijst bevat alle inkooporders voor uw rekening die de status **Bevestigd** hebben. Wanneer IO-producten of -services volledig zijn ontvangen, verdwijnt de inkooporder uit de lijst.

U kunt de volgende pagina's gebruiken om met inkooporders te werken:

- **Inkooporders ter beoordeling**: deze pagina bevat dezelfde informatie als de lijst **Inkooporders ter beoordeling** in het werkgebied. Zie de beschrijvingen eerder in dit onderwerp.
- **Historie van leveranciersbevestigingen van inkooporders**: deze pagina bevat alle inkooporders en alle versies van inkooporders die zijn verzonden naar de leverancier. Hier vindt u ook alle geretourneerde antwoorden van de leverancier.
- **Bevestigde inkooporders openen**: deze pagina bevat dezelfde informatie als de lijst **Bevestigde inkooporders openen** in het werkgebied. Zie de beschrijvingen eerder in dit onderwerp.
- **Alle bevestigde inkooporders**: deze pagina bevat alle bevestigde inkooporders. De inkooporderpagina's op deze pagina omvatten inkooporders waarop producten of services zijn ontvangen. U kunt deze lijst gebruiken om te controleren voor welke inkooporders u facturen kunt verzenden.

### <a name="responding-to-pos"></a>Reageren op inkooporders

De inkooporders die de klant ter beoordeling aan u stuurt, zijn alleen in het werkgebied **Inkooporderbevestiging** en op de pagina **Inkooporders ter beoordeling** zichtbaar. Als u een inkooporder opent, kunt u deze accepteren, afwijzen of accepteren met wijzigingen. De koptekst of afzonderlijke regels van de inkooporder kunnen bijlagen bevatten. Daarnaast is het mogelijk voor u om informatie aan uw reactie toe te voegen, aan de koptekst of aan afzonderlijke regels. U kunt bijvoorbeeld een vervangingsitem voor een van de regels voorstellen.

U kunt de inkooporder als PDF-bestand bekijken en afdrukken met de optie **Voorbeeld/afdrukken**. U kunt ook de actie **Dimensies weergeven** gebruiken om de volgende dimensiekolommen te verbergen of weer te geven: **Locatie**, **Magazijn**, **Kleur**, **Grootte**, **Stijl** en **Configuratie**. 

Als u de optie **Accepteren met wijzigingen** gebruikt, kunt u afzonderlijke regels accepteren of afwijzen. U kunt ook de volgende wijzigingen aanbrengen aan regels:

- Wijzig datums of hoeveelheden. Als u de bevestigde leveringsdatum op alle regels wilt bijwerken, gebruikt u de optie **Leveringsdatums bijwerken** voor de IO-koptekst.
- Splits regels op voor verschillende leveringsdatums of -hoeveelheden.
- Vervang een item. Voer een itembeschrijving en het itemnummer in het veld **Extern** in het gedeelte **Regeldetails** in.

U kunt prijsgegevens of toeslagen niet wijzigen, maar u kunt met notities wel suggesties voor dergelijke wijzigingen geven.

Als u van uw klant een nieuwe versie van een inkooporder ontvangt, bevat deze een versieachtervoegsel om aan te geven dat het om een gewijzigde versie van een inkooporder gaat die eerder is verzonden. Op de pagina **Historie van leveranciersbevestigingen van inkooporders** kunt u de historie van elke order volgen.

## <a name="monitoring-consignment-inventory"></a>Consignatievoorraad bewaken

Als u consignatievoorraad gebruikt, kunt u de interface voor leverancierssamenwerking gebruiken om informatie op de volgende pagina's te bekijken:

- **Inkooporders die consignatievoorraad verbruiken**: inkooporders voor consignatievoorraad worden gegenereerd wanneer de klant de voorraad in eigendom krijgt. Deze consignatie-inkooporders worden alleen op deze pagina weergegeven. Ze worden niet opgenomen op de pagina **Alle bevestigde inkooporders**.
- **Producten ontvangen uit consignatievoorraad**: deze pagina bevat een overzicht van alle transacties waarvan het eigendom van producten is overgedragen aan het bedrijf dat de voorraad verbruikt. U kunt deze informatie gebruiken om de klant te factureren.
- **Voorhanden consignatievoorraad**: op deze pagina wordt de voorhanden consignatievoorraad weergegeven die het eigendom is van uw bedrijf en voorhanden is in het magazijn van de klant.

## <a name="working-with-rfqs-in-the-vendor-bidding-workspace"></a>Werken met offerteaanvragen in het werkgebied Biedingen van leverancier

In de werkruimte **Biedingen van leverancier** kunt u de offerteaanvragen weergeven waarop uw bedrijf is gevraagd te reageren. U kunt ook reageren op de offerteaanvragen. 

De werkruimte bevat ook alle offerteaanvragen die u hebt binnengehaald of verloren. Als het systeem is geconfigureerd voor de publieke sector, worden in het werkgebied de offerteaanvragen weergegeven die openbaar zijn.

### <a name="viewing-rfqs"></a>Offerteaanvragen weergeven

Open het werkgebied **Biedingen van leverancier** om toegang te krijgen tot de volgende informatie:

- Selecteer **Uitnodigingen voor nieuw bod** om de offerteaanvragen te bekijken waarvoor u bent uitgenodigd om te reageren. Hier kunt u een offerteaanvraag weergeven en het biedingsproces starten. U ziet ook gewijzigde offerteaanvragen waarvoor een nieuw bod moet worden ingediend.
- Selecteer **Geretourneerde biedingen** om de offerteaanvragen te zien die de klant aan u heeft geretourneerd, zodat u meer informatie kunt opgeven of het bod kunt bijwerken.
- Selecteer **Biedingen in uitvoering** om de offerteaanvragen te zien waaraan u of een contactpersoon die uw bedrijf vertegenwoordigt heeft gewerkt, maar die nog niet zijn ingediend.
- Selecteer **Toegekende biedingen** om te zien wanneer de klant ten minste één regelartikel in uw bod heeft toegekend.
- Selecteer **Verloren biedingen** om biedingen te zien waarin alle regels zijn afgewezen.
- Selecteer de koppeling **Offerteaanvragen** voor een overzicht van alle uitnodigingen voor offerteaanvragen van een leverancier en alle biedingen die zijn ingediend. Op de pagina **Offerteaanvragen** worden alle offerteaanvragen weergegeven waarbij een leverancier betrokken is geweest. U kunt zoeken op status.
- Selecteer de koppeling **Geweigerde biedingen** voor een overzicht van alle offerteaanvragen waarop de contactpersoon van een leverancier heeft geweigerd te bieden.

### <a name="working-with-rfqs-that-are-publicly-available"></a>Werken met offerteaanvragen die openbaar beschikbaar zijn

Mensen die in de publieke sector werken, kunnen openstaande en verlopen offerteaanvragen bekijken die beschikbaar zijn gemaakt voor het publiek.

- Selecteer de koppeling **Gepubliceerde offerteaanvragen openen** voor een overzicht van openstaande offerteaanvragen die openbaar beschikbaar zijn. Een openstaande offerteaanvraag is een offerteaanvraag die nog niet is verlopen. U kunt de vervaldatum en -tijd vinden in de koptekst van de offerteaanvraag.

    Als u bent uitgenodigd om te bieden, kunt u dezelfde offerteaanvraag vinden op de pagina **Uitnodigingen voor nieuw bod**. Soms wilt u mogelijk bieden op een openstaande offerteaanvraag terwijl u niet bent uitgenodigd om te bieden. In dat geval kunt u mogelijk uzelf uitnodigen, mits de klant de mogelijkheid voor zelfuitnodiging voor de offerteaanvraagcase biedt.

- Selecteer de koppeling **Gesloten gepubliceerde offerteaanvragen** voor een overzicht van gesloten offerteaanvragen die beschikbaar zijn voor het publiek. Een gesloten offerteaanvraag is een offerteaanvraag die is verlopen. U kunt de vervaldatum en -tijd vinden in de koptekst van de offerteaanvraag.

    In een gesloten offerteaanvraag worden alle biedingen van leveranciers tot het regelniveau weergegeven. Wanneer biedingen worden toegekend of geweigerd, wordt deze informatie weergegeven in de gesloten offerteaanvraag. Eventuele bijlagen die zijn opgenomen in de bieding zijn ook beschikbaar.

**Opmerking:** deze functionaliteit is alleen beschikbaar als de cofiguratie Publieke sector is ingeschakeld.

### <a name="bidding"></a>Bieden

- Klik op **Bieding** om te beginnen met bieden op een offerteaanvraag.

    Wanneer de biedingsvelden in de kopteksten en regels van een offerteaanvraag kunnen worden bewerkt, kunt u uw bod rechtstreeks in het regelraster invoeren. Bedenk ook welke aanvullende biedingsgegevens moeten worden opgenomen in de regeldetails.

    Wanneer u begint te werken aan een bod, wordt dit weergegeven in het gedeelte **Biedingen in uitvoering**.

    U kunt een bod opslaan op elk gewenst moment vóór de vervaldatum. U kunt dan later terugkeren en het bod indienen. Nadat u een bod hebt ingediend, kunt u dit nog intrekken en bijwerken tot de vervaldatum.

- Selecteer **Opnieuw instellen vanuit offerteaanvraag** om de gegevens van de oorspronkelijke offerteaanvraag te herstellen. U kunt de koptekst of de regel opnieuw instellen.
- Selecteer **Alternatief toevoegen** of **Alternatief verwijderen** in het regelraster om te werken met alternatieven.

    Voor sommige offerteaanvragen worden alternatieve biedingen toegestaan. U kunt alleen alternatieve biedingen voor regels van het type **Categorie** typen omdat specifieke artikelen niet kunnen worden toegevoegd als alternatieven. 

- Selecteer **Bijlage bij offerteaanvraag** of **Bijlagen bij offerteaanvraagregels** om bijlagen te openen die de klant heeft toegevoegd aan een offerteaanvraag. Selecteer **Bijlagen bij biedingen** of **Bijlagen bij biedingsregels** om bijlagen samen met het bod te uploaden.

    Mogelijk moet u vragenlijsten invullen voordat u een bod mag indienen.

- Selecteer **Weigeren** als u geen bod wilt doen. Nadat u **Weigeren** hebt geselecteerd, kunt u deze actie niet intrekken om alsnog een bod te doen.

Als een offerteaanvraag wordt aangepast, moet u een nieuw bod invoeren. U vindt informatie over de aanpassing op het tabblad **Aanpassingen** van de pagina van de offerteaanvraag. Aangepaste offerteaanvragen worden weergegeven op de pagina **Uitnodigingen voor nieuw bod**.

## <a name="accessing-vendor-master-data-in-the-vendor-information-workspace"></a>Toegang tot modelgegevens van leveranciers in het werkgebied Leveranciergegevens

Als leverancier hebt u toegang tot een deel van de gegevens die de klant bijhoudt in de hoofdrecord van een leverancier. U kunt deze gegevens dus up-to-date houden. Als u de gegevens wilt bijwerken, moet u de rol Leveranciersbeheerder (extern) hebben.

De toegankelijke gegevens zijn de naam van de leverancier, adressen, contactgegevens, contactpersonen en hun contactgegevens, identificatienummers, btw-registratienummers, inkoopcategorieën waarvoor de leverancier is goedgekeurd en informatie over certificeringen.

## <a name="see-also"></a>Zie ook

[Gebruikers van leverancierssamenwerking beheren](manage-vendor-collaboration-users.md)

