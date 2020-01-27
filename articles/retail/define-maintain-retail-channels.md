---
title: Detailhandelskanalen definiëren en onderhouden
description: Dit onderwerp biedt een overzicht van het proces voor het opzetten van fysieke winkels, waarnaar in Dynamics 365 Retail als detailhandelwinkels wordt verwezen. Het bevat informatie over de taken die u vóór en na het opzetten van een detailhandelwinkel moet uitvoeren.
author: mugunthanm
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 45d0386d215da15103a417502debb245c91f6309
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934603"
---
# <a name="define-and-maintain-retail-channels"></a>Detailhandelskanalen definiëren en onderhouden

[!include [banner](includes/banner.md)]

Dit onderwerp biedt een overzicht van het proces voor het opzetten van fysieke winkels, waarnaar in Dynamics 365 Retail als detailhandelwinkels wordt verwezen. Het bevat informatie over de taken die u vóór en na het opzetten van een detailhandelwinkel moet uitvoeren.

Retail ondersteunt meerdere retailkanalen, zoals onlinewinkels, callcenters en fysieke winkels. Een fysieke winkel wordt een detailhandelswinkel genoemd. Iedere detailhandelwinkel kan zijn eigen betalingsmethoden, prijsgroepen, verkooppuntkassa's (POS), inkomsten- en uitgavenrekeningen en personeel hebben. U moet al deze elementen voor een detailhandel instellen voordat u deze maakt. Nadat u de detailhandelswinkel hebt gemaakt, wijst u de producten toe die u wilt verkopen. U moet ook werknemers, kassa's en klanten aan de winkel toewijzen. Tot slot voegt u de nieuwe winkel toe aan een organisatiehiërarchie.

## <a name="setting-up-retail-stores"></a>Detailhandelwinkels instellen

Voordat u een detailhandel kunt instellen in Retail, moet u enkele vereiste taken uitvoeren. U kunt de detailhandel vervolgens maken en gegevens toevoegen.

### <a name="prerequisites"></a>Vereisten

Voordat u een detailhandel kunt instellen, moet u enkele vereiste taken uitvoeren:

1. Configureer uw organisatiestructuur en stel de organisatiehiërarchieën in voor detailhandelsassortimenten, aanvulling en rapportage.
2. Een magazijn voor de detailhandel instellen.
3. Nummerreeksen voor detailhandelwinkels, winkeloverzichten en overzichtboekstukken instellen.
4. Parameters voor detailhandel configureren
5. De betalingsmethoden instellen die door de winkel worden geaccepteerd.
6. Om creditcardtransacties op de POS-kassa's van de detailhandelswinkel te kunnen verwerken, kunt u ook betalingsservices instellen.
7. Btw-groepen instellen.
8. Detailhandelproducten instellen. Als onderdeel van deze taak kunt u ook detailhandelsproducthiërarchieën instellen, productvarianten en productassortimenten.
9. Productprijsgroepen instellen.
10. Prijzen voor detailhandelproducten instellen. Als onderdeel van deze taak kunt u ook prijscorrecties, kortingen en kortingsperioden instellen.
11. Personeelsleden instellen.

    > [!NOTE]
    > U moet ook de juiste machtigingen aan werknemers toewijzen, zodat ze zich kunnen aanmelden en taken kunnen uitvoeren met het Retail POS-systeem.

12. Configureer de Retail POS-profielen die u aan de winkel wilt toewijzen. Deze taak omvat veel andere taken, zoals het opzetten van kassa´s, het instellen van offlineprofielen en ontvangstbewijsindelingen en -profielen.

Controleer alle taken die in de vereiste taken zijn opgenomen en voer alleen alle taken uit die op u van toepassing zijn.

### <a name="set-up-a-retail-store"></a>Een detailhandelwinkel instellen

Nadat u de vereiste taken hebt uitgevoerd, voert u deze taken uit voor het instellen van de details voor de detailhandelswinkel:

1. Maak een detailhandelwinkel.
2. Wijs een btw-groep aan de winkel toe.
3. Wijs de geaccepteerde betalingsmethoden aan de winkel toe.
4. Details toevoegen aan de productbeschrijvingen voor producten die u in uw detailhandels aanbiedt. U kunt bijvoorbeeld opgemaakte tekst en afbeeldingen toevoegen. Deze gegevens worden weergegeven in verschillende contexten, zoals in de POS-kassa of op afgedrukte labels.
5. Voeg de winkel toe aan een organisatiehiërarchie die is bestemd voor **Detailhandelsassortiment**, **Detailhandelsaanvulling** of **Detailhandelsrapportage**.

### <a name="after-you-set-up-a-retail-store"></a>Na het instellen van een detailhandelwinkel

Nadat u de gegevens voor de detailhandelswinkel hebt ingevoerd, voert u deze taken uit om de gegevens van de nieuwe detailhandelswinkel naar Retail POS te verzenden.

1. Configureer de POS-kassa's voor de winkel.
2. Wijs productassortimenten aan de winkel toe.
3. Verwerk assortimenten om de lijst met producten te genereren die in het assortiment zijn opgenomen en om de producten in de detailhandelwinkel beschikbaar te maken.
4. Verzend gegevens zoals numerreeksen, hardwareprofielen en POS-schermindelingen naar de Retail POS-kassa´s.
5. Publiceer de detailhandelswinkel om winkelgegevens te verzenden naar Retail POS.
6. Voer de taken uit om de winkelgegevens naar Retail POS te verzenden.

## <a name="organization-hierarchies"></a>Organisatiehiërarchieën

Retail gebruikt organisatiehiërarchieën om detailhandelkanalen structuur te geven. Met organisatiehiërarchieën worden de relaties aangegeven tussen de organisaties waaruit het bedrijf bestaat. Bij het instellen van winkels, kunt u ze toevoegen aan een organisatiehiërarchie. De winkels delen vervolgens gegevens die wordt gebruikt voor assortimenten, aanvulling en rapportering.

> [!NOTE]
> Als u de functionaliteit voor detailhandelverkoop wilt gebruiken, moet de configuratiesleutel voor **Meerdere verzendadressen** zijn ingeschakeld. Deze configuratiesleutel kunt u vinden in de **handelsconfiguratiesleutels** onder **Systeembeheer**\> **Instellingen** \> **Licentieconfiguratie**. Dit is vereist vanwege de detailhandelfunctionaliteit die verschillende validaties uitvoert op basis van het afleveradres dat is geconfigureerd op het niveau van de verkooporderregel.
