---
title: Crediteringen en aanmaningen configureren
description: In dit artikel wordt beschreven hoe u de incassofunctie configureert.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustCollectionsActivitiesListPage
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14031
ms.assetid: dcc6da2f-9af5-4f1d-abaa-b72967b66979
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: 1a9bf1067d0f6e0e139ef13d939d2f0e9bf2126b
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-credit-and-collections"></a>Crediteringen en aanmaningen configureren

In dit artikel wordt beschreven hoe u de incassofunctie configureert.

<a name="set-up-aging-period-definitions"></a>Ouderdomsperiodedefinities instellen
-------------------------------

Stel een ouderdomsperiodedefinitie in. Een ouderdomsperiodedefinitie definieert de kolommen die worden weergegeven op de lijstpagina's **Vervallen saldi**, **Incasseringsactiviteiten** en **Incassoaanvragen**. Het definieert ook de perioden die worden weergegeven op de pagina **Aanmaningen**. Wanneer er een klantenverzameling wordt ingesteld, wordt de ouderdomsperiodedefinitie voor de verzameling gebruikt. Als geen verzamelingen zijn geconfigureerd, wordt de standaard ouderdomsperiodedefinitie gebruikt die opgegeven is op de pagina **Parameters van module Klanten**. Als geen standaardouderdomsperiodedefinitie is opgegeven, wordt de eerste ouderdomsperiodedefinitie op de pagina **Ouderdomsperiodedefinities** gebruikt.

## <a name="create-an-aging-snapshot"></a>Een ouderdomsmomentopname maken
Registraties voor ouderdomsmomentopname voor alle klanten of voor de klanten in een klantenverzameling maken. Informatie van de ouderdomsmomentopname wordt weergegeven op de lijstpagina **Vervallen saldi** en op de pagina **Aanmaningen**. U moet een ouderdomsmomentopname maken voordat u de lijstpagina kunt gebruiken. De lijstpagina geeft uitsluitend informatie weer voor klanten voor wie een ouderdomsmomentopname is gemaakt.

## <a name="optional-set-up-customer-pools"></a>Optioneel: Klantverzamelingen instellen
U kunt klantverzamelingen instellen die klantengroepen vertegenwoordigen. U kunt klantverzamelingen gebruiken als filters voor de klantgegevens die op de lijstpagina's **Aanmaningen** worden weergegeven, op de pagina **Aanmaningen**, of wanneer u ouderdomsmomentopnamen maakt.

## <a name="optional-create-a-collections-team"></a>Optioneel: Een team van incassomedewerkers maken
Als er meerdere mensen binnen uw organisatie incassowerk uitvoeren, kunt u een team van incassomedewerkers instellen. U kunt het team selecteren op de pagina **Parameters van module Klanten**. Als u geen team van incassomedewerkers maakt, wordt er automatisch een gemaakt wanneer u incassomedewerkers instelt op de pagina **Incassomedewerker**.

## <a name="set-up-a-collections-case-category"></a>Een aanvraagcategorie voor collecties instellen
Als u uw incassowerkzaamheden organiseert door middel van aanvragen, stelt u een aanvraagcategorie in met het categorietype **Aanmaningen**. Deze instelling is alleen vereist wanneer u de aanvraagfunctionaliteit op de pagina **Aanmaningen** gebruikt.

## <a name="set-up-journal-names-settlement-writeoff-and-nsf"></a>Instellen van journaalnamen (vereffening, afschrijvingen en NSF)
Stel de journaalnamen in die worden gebruikt wanneer transacties op de pagina **Aanmaningen** worden verwerkt. Deze verwerking omvat het vereffenen van een transactie, het afschrijven van een transactie, of het verwerken van een betaling met ontoereikend saldo (NSF).

| Beschrijving | Journaaltype     |
|-------------|------------------|
| Vereffening  | Betaling van klant |
| Afschrijven   | Dagelijks            |
| Onvoldoende fondsen         | Betaling van klant |

## <a name="set-up-a-reason-code-for-writeoff-transactions"></a>Een redencode voor transacties van de afschrijving instellen
De standaardredencode die wordt gebruikt wanneer transacties worden afgeschreven op de pagina **Aanmaningen**. U kunt de code tijdens het afschrijvingsproces wijzigen.

## <a name="set-up-a-folder-for-email-attachments-and-create-email-templates"></a>Een map instellen voor e-mailbijlagen en e-mailsjablonen maken
Als u e-mailberichten van de pagina **Aanmaningen** verzendt met Microsoft Excel-bestanden als bijlage, kunt u optioneel e-mailsjablonen voor deze berichten maken.

## <a name="set-up-accounts-receivable-parameters-for-collections"></a>Parameters van de module Klanten instellen voor aanmaningen
Stel de parameters voor klanten in, die worden getoond op het tabbland **Aanmaningen**.

## <a name="optional-set-up-collections-agents"></a>Optioneel: Incassomedewerkers instellen
Als er meerdere mensen binnen uw organisatie incassowerk uitvoeren, kunt u incassomedewerkers instellen. Een incassomedewerker is een werknemer die is geconfigureerd als een gebruiker op de pagina **Gebruikersrelaties**. U kunt klantverzamelingen (klantquery's) toewijzen aan incassomedewerkers om ze te helpen hun werk te organiseren. De incassomedewerkers worden toegevoegd aan het team dat is geselecteerd op de pagina **Parameters van module Klanten**. Als op die pagina geen team is geselecteerd, wordt automatisch een nieuw team met de naam **Aanmaningen** gemaakt en worden de incassomedewerkers aan dat team toegevoegd.

## <a name="set-up-a-writeoff-account"></a>Een rekening afschrijvingen instellen
Stel de afschrijvingsrekening in die wordt gebruikt voor de afschrijvingsvermelding in het grootboek, wanneer een transactie wordt afgeschreven. Deze rekening wordt opgeslagen in het boekingsprofiel van de klant.

## <a name="set-up-nsf-information-for-bank-accounts"></a>NSF-informatie voor bankrekeningen instellen
Werk de bankrekeningen bij, zodat deze het juiste journaal hebben wanneer NSF-betalingen worden geïdentificeerd op de pagina **Aanmaningen**. Selecteer een betalingsjournaal op het tabblad **Valutabeheer** in het veld **Journaal met betalingen met ontoereikend saldo**.

## <a name="set-up-outlook-settings-for-users-of-the-collections-page"></a>Outlook-instellingen instellen voor gebruikers van de pagina Incasso's
Voordat werknemers activiteiten kunnen maken of e-mailberichten kunnen verzenden door middel van de pagina **Incasso's**, moet u verifiëren of de configuratiesleutel **Synchronisatie Microsoft Outlook** is geselecteerd en dat de Outlook-synchronisatie is ingesteld voor deze werknemers.

## <a name="set-up-email-and-address-settings-for-collections-customer-contacts"></a>E-mail- en adresinstellingen instellen voor de contactpersoon voor incasso's voor de klant
Stel e-mailadressen voor klantcontactpersonen in als u e-mailberichten naar deze contactpersonen wilt verzenden vanaf de pagina **Incasso's**. De contactpersoon voor incasso's wordt als de standaard contactpersoon gebruikt op de pagina **Aanmaningen**. U kunt een adres voor het overzicht voor de klant instellen als overzichten een ander adres dan het primaire adres moeten gebruiken. 

Selecteer op het sneltabblad **Crediteringen en aanmaningen** in het veld **Contactpersoon voor incasseringen** de persoon binnen de klantorganisatie die samenwerkt met uw incassomedewerker. Deze contactpersoon wordt als standaard contactpersoon gebruikt op de pagina **Aanmaningen** en is degene naar wie e-mailberichten worden verzonden. 

> [!NOTE] 
> Als een contactpersoon voor incasso's voor een klant is opgegeven, wordt de primaire contactpersoon voor de klant gebruikt. Als er geen primaire contactpersoon is opgegeven, worden e-mailberichten verzonden naar het eerste adres op de pagina **Contactpersonen**.

## <a name="set-up-email-settings-for-salespeople"></a>E-mailinstellingen instellen voor verkopers
Stel e-mailadressen voor verkopers in als u e-mailberichten naar verkopers wilt verzenden vanaf de pagina **Aanmaningen**. Stel een e-mailadres in voor iedere verkoopvertegenwoordiger in iedere provisieverkoopgroep. De verkoopvertegenwoordiger waarvan het selectievakje **Contactpersoon** is geselecteerd, is de standaardverkoper waarnaar e-mailberichten worden verzonden. 

Als er geen verkoopvertegenwoordiger is opgegeven, wordt de primaire verkoper voor de organisatie van de klant gebruikt. Als geen primaire verkoper is opgegeven, worden e-mailberichten verzonden naar het eerste adres op de pagina.


