---
title: Problemen met productinformatie oplossen
description: In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met productinformatie.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4c505ccfd1998acd40dbae715c7fa572e315af2e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007511"
---
# <a name="troubleshoot-product-information"></a>Problemen met productinformatie oplossen

In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met productinformatie.

## <a name="i-cant-delete-a-released-product"></a>Ik kan een vrijgegeven product niet verwijderen.

### <a name="issue-description"></a>Probleembeschrijving

U kunt een vrijgegeven product en alle varianten alleen verwijderen als er geen transacties met betrekking tot het vrijgegeven product zijn.

### <a name="issue-resolution"></a>Probleemoplossing

Voer de volgende stappen uit om een vrijgegeven product of productmodel te verwijderen.

1. Sluit alle openstaande transacties voor de artikelen.
1. Verminder de voorraad tot 0 (nul).
1. Voor een voorraadafsluiting uit.
1. Verwijder alle productvarianten voor het productmodel dat u wilt verwijderen.

## <a name="can-i-change-the-item-number-of-a-released-product"></a>Kan ik het artikelnummer van een vrijgegeven product wijzigen?

In de meeste gevallen kunt u artikelnummers voor vrijgegeven producten niet bewerken, omdat hierdoor gegevens beschadigd raken. U kunt het artikelnummer alleen bewerken als u gegevensbeschadiging moet herstellen die is veroorzaakt door een eerdere naamswijziging van de primaire sleutel van dat vrijgegeven product, zoals vermeld in de lijst met [verwijderde of verouderde functies voor Finance and Operations 10.0.0 met Platform update 24](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24).

Als u artikelnummers voor vrijgegeven producten wilt kunnen bewerken, [stem dan op dit idee in de ideeënportal](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).

## <a name="the-default-flushing-principle-from-the-product-isnt-being-entered-on-the-bill-of-materials-line"></a>De standaardbackflushing van het product wordt niet ingevoerd op de stuklijstregel.

### <a name="issue-description"></a>Probleembeschrijving

Wanneer u een artikel aan een stuklijstregel toevoegt, wordt in het systeem niet de backflushing gebruikt die standaard voor het artikel is ingesteld. Met andere woorden, de backflushing van het artikel wordt niet weergegeven op de pagina met de **stuklijstregel**.

### <a name="issue-resolution"></a>Probleemoplossing

Als u een backflushing op een stuklijstregel opgeeft, wordt deze op die stuklijstregel toegepast. Als de backflushing echter leeg is of als deze niet op een stuklijstregel is ingesteld, is de backflushing die voor het artikel is ingesteld nog steeds van toepassing op die stuklijstregel, ook al wordt deze niet op de stuklijstregel weergegeven.

De standaardlogica voor andere functies in Microsoft Dynamics 365 Supply Chain Management werkt normaal gesproken niet op deze manier. Het huidige gedrag kan echter niet worden gewijzigd. Anders ontstaan mogelijk fouten in bepaalde bestaande aanpassingen die hiervan afhankelijk zijn.

## <a name="the-system-lets-me-save-duplicate-bar-codes-for-different-items-or-for-the-same-item-that-has-different-dimensions"></a>Het systeem laat me dubbele streepjescodes opslaan voor verschillende artikelen of voor hetzelfde artikel met verschillende dimensies.

Het systeem dwingt momenteel geen unieke streepjescodes af en de toevoeging van deze beperking zou een wijziging zijn die fouten veroorzaakt. Microsoft kan zelfs aantonen dat in bepaalde bestaande installaties van klanten door deze wijziging fouten zouden worden veroorzaakt. We zullen echter wel een bredere ontwerpwijziging overwegen om deze functie in de toekomst mogelijk te maken.

## <a name="i-receive-the-following-error-message-when-i-edit-item-record-templates-the-warehouse-location-cannot-be-created-because-the-item-is-not-stocked-to-stock-items-the-stocked-product-option-on-the-associated-item-model-group-must-be-selected"></a>Het volgende foutbericht wordt weergegeven wanneer ik artikelrecordsjablonen bewerk: "De magazijnlocatie kan niet worden gemaakt omdat het artikel niet is opgeslagen in voorraad. Om artikelen in de voorraad op te slaan, moet de optie Product in voorraad in de gekoppelde artikelmodelgroep worden geselecteerd."

### <a name="issue-description"></a>Probleembeschrijving

Dit probleem treedt op als u de volgende stappen uitvoert om een sjabloon te maken voor een artikel dat niet in voorraad is opgeslagen.

1. Open een vrijgegeven product dat niet is opgeslagen in voorraad.
1. Selecteer in het actievenster op het tabblad **Opties** de optie **Recordinfo**.
1. Selecteer **Bedrijfsrekeningsjabloon** in het dialoogvenster **Recordinfo**.

In dat geval wordt het volgende foutbericht weergegeven:

> De magazijnlocatie kan niet worden gemaakt omdat het artikel niet is opgeslagen in voorraad. Om artikelen in de voorraad op te slaan, moet de optie Product in voorraad in de gekoppelde artikelmodelgroep worden geselecteerd.

### <a name="issue-resolution"></a>Probleemoplossing

Voor het proces van het maken van productsjablonen is extra productspecifieke logica nodig. U kunt daarom de knop **Bedrijfsrekeningsjabloon** niet voor dit doel gebruiken. Volg in plaats daarvan deze stappen.

1. Open een vrijgegeven product.
1. Selecteer in het actievenster op het tabblad **Product** in de groep **Nieuw** de optie **Sjabloon \> Gedeelde sjabloon maken**.

## <a name="default-help-text-that-is-added-in-product-attributes-isnt-entered-in-a-released-product"></a>Help-tekst die standaard in productkenmerken wordt toegevoegd, wordt niet in een vrijgegeven product ingevoerd.

Een omschrijving en Help-tekst die in de productkenmerken worden toegevoegd, worden niet standaard in de vrijgegeven producten weergegeven of ingevoerd. Dit is zo ontworpen.

## <a name="the-default-quantity-that-is-entered-differs-when-its-registered-from-a-bom-and-when-its-registered-from-a-bom-version"></a>De standaardhoeveelheid die wordt ingevoerd, verschilt wanneer deze wordt geregistreerd vanuit een stuklijst en wanneer deze wordt geregistreerd vanuit een stuklijstversie.

### <a name="issue-description"></a>Probleembeschrijving

Wanneer u een artikel aan een stuklijst toevoegt, wordt de hoeveelheid standaard op 1 ingesteld in plaats van de hoeveelheid die is gedefinieerd in het veld **Min.orderhoeveelheid** op de pagina **Standaard orderinstellingen** voor een geselecteerd product. Wanneer u echter een artikel uit een stuklijstversie toevoegt en het artikel en de variant zijn geselecteerd, wordt bij de hoeveelheid die standaard wordt ingevoerd rekening gehouden met de minimumhoeveelheid die is ingesteld in de standaard orderinstellingen voor de specifieke dimensies.

### <a name="issue-resolution"></a>Probleemoplossing

Dit gedrag is verwacht. Het feit dat de logica echter verschilt van de stuklijst en de stuklijstversie is een bekend probleem. Dit gedrag wordt echter niet gewijzigd, omdat een wijziging gevolgen kan hebben voor veel verschillende klantscenario's.

## <a name="in-the-released-product-details-i-cant-change-the-attached-images-that-were-uploaded-from-the-product-document-attachments-data-entity"></a>Ik kan in de details van vrijgegeven producten de bijgevoegde afbeeldingen die zijn geüpload vanuit de gegevensentiteit Documentbijlagen van producten.

### <a name="issue-description"></a>Probleembeschrijving

Dit probleem kan optreden wanneer u een afbeelding aan een artikel koppelt met behulp van de gegevensentiteit *Documentbijlagen van producten*. In dit geval wordt de artikelafbeelding weergegeven voor het artikel. Als u echter **Afbeelding wijzigen** selecteert, wordt er niets weergegeven in de lijst met geüploade afbeeldingen. Bovendien worden er geen bijlagen weergegeven voor het artikel.

### <a name="issue-resolution"></a>Probleemoplossing

De entiteit *EcoResProductDocumentAttachmentEntity* (*Documentbijlagen van producten*) importeert documentbijlagen voor *producten* maar niet voor *vrijgegeven producten*. (Vrijgegeven producten worden ook wel *artikelen* genoemd.) Als u de bijlagen voor een artikel op de pagina **Vrijgegeven productdetails** wilt weergeven, moet u de entiteit *EcoResReleasedProductDocumentAttachmentEntity* (*Documentbijlagen van vrijgegeven producten*) gebruiken.

## <a name="the-microsoft-flow-connector-shows-the-following-error-message-update-not-allowed-for-field-productnumber"></a>De Microsoft Flow-connector toont het volgende foutbericht: "Update niet toegestaan voor veld 'ProductNumber '."

### <a name="issue-description"></a>Probleembeschrijving

Dit probleem doet zich voor als u het veld **Productnummer** wilt bijwerken met behulp van de entiteit *Vrijgegeven producten* V2 en Microsoft Flow.

### <a name="issue-resolution"></a>Probleemoplossing

Dit gedrag is verwacht. De mogelijkheid om het productnummer voor een vrijgegeven product te bewerken, is verwijderd in Dynamics 365 Finance and Operations 10.0.0 met Platformupdate 24 om gegevensbeschadiging te helpen voorkomen. In uitzonderlijke gevallen, als u gegevens moet herstellen die zijn beschadigd door een eerdere naamswijziging van de primaire sleutel van een vrijgegeven product, kunt u Microsoft Support vragen om deze beperking tijdelijk te verwijderen.

## <a name="i-cant-create-a-released-product-variant-in-another-legal-entity"></a>Ik kan geen vrijgegeven productvariant in een andere rechtspersoon maken.

### <a name="issue-description"></a>Probleembeschrijving

Als u een productmodel zonder varianten probeert vrij te geven en vervolgens de varianten in elke rechtspersoon (bedrijf) hebt gemaakt wanneer dit nodig is, kunt u de varianten niet vrijgeven met behulp van variantsuggesties. U kunt de varianten ook niet handmatig maken.

### <a name="issue-resolution"></a>Probleemoplossing

Dit is zo ontworpen. De relaties van een productmodel en de mogelijke dimensies van dat model worden op een gedeeld niveau bewaard. Daarom kunt u de beschikbare dimensies voor een gedeeld productmodel niet maken in de specifieke rechtspersoon waar deze dimensies worden vrijgegeven en vervolgens het proces repliceren in elke rechtspersoon waar de dimensies zijn vereist. In plaats daarvan moet u het vrijgaveproces aanpassen aan het ontworpen proces.

Dit is het proces voor het vrijgeven van producten.

1. Maak het gedeelde productmodel en de dimensies die kunnen worden vrijgegeven aan de rechtspersonen.
1. Geeft de producten vrij aan de rechtspersonen door gebruik te maken van variantsuggesties of door handmatig de combinaties toe te voegen die moeten worden vrijgegeven.

U kunt het vrijgegeven product ook rechtstreeks maken.

## <a name="when-i-release-a-variant-in-another-company-i-receive-the-following-error-message-product-variant-with-specified-dimensions-has-already-been-created"></a>Wanneer ik een variant in een ander bedrijf vrijgeef, krijg ik het volgende fout bericht: "Er is al een productvariant met de opgegeven dimensies gemaakt."

### <a name="issue-description"></a>Probleembeschrijving

Als er al een productvariant is vrijgegeven in een bedrijf A en u probeert deze vrij te geven in bedrijf B met behulp de knop **Nieuw** op de pagina **Vrijgegeven productvarianten**, wordt het volgende foutbericht weergegeven:

> Er is al een productvariant met de opgegeven dimensies gemaakt.

### <a name="issue-resolution"></a>Probleemoplossing

Met de knop **Nieuw** op de pagina **Vrijgegeven productvarianten** maakt u de variant en geeft u deze vrij in de bedrijfscontext. Als de variant al is gemaakt, kunt u de knop **Nieuw** niet gebruiken om de variant vrij te geven in een ander bedrijf.

Om het probleem op te lossen, opent u de pagina **Productmodel** en selecteert u **Vrijgeven product** om de bestaande variant in het gewenste bedrijf vrij te geven.
