---
title: Incheckmeldingen van klanten in Point of Sale (POS) inschakelen
description: In dit onderwerp wordt beschreven hoe u incheckmeldingen voor klanten in het Microsoft Dynamics 365 Commerce POS kunt inschakelen.
author: bicyclingfool
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 320e9d73ca98bf4ed22ac9bdff2fc34ae83223ec
ms.sourcegitcommit: 5f5a8b1790076904f5fda567925089472868cc5a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/03/2021
ms.locfileid: "7891407"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a>Incheckmeldingen van klanten in Point of Sale (POS) inschakelen

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

In dit onderwerp wordt beschreven hoe u incheckmeldingen voor klanten in het Microsoft Dynamics 365 Commerce POS kunt inschakelen.

In hun e-mails voor 'Order gereed voor ophalen' kunnen organisaties een koppeling of knop bieden, waarmee klanten aan de winkel kunnen melden dat ze zich op het terrein bevinden en wachten tot hun pakket naar hen wordt gebracht. Klanten ontvangen vervolgens een incheckbevestiging en de winkel ontvangt een melding als een taak in de POS-toepassing. Deze taak dient als aansporing voor een verkoopmedewerker om de order af te geven bij het voertuig van de klant. Zo hoeft de klant de winkel niet in te komen.

De workflow voor het inchecken van klanten kan ook worden geconfigureerd om extra informatie te verzamelen van klanten, zoals het nummer van de parkeerplaats, het merk, model en de kleur van de voertuig en instructies voor het afleveren. Met deze informatie kan de winkelmedewerker de afhandeling van de order bespoedigen.

## <a name="enable-customer-check-in"></a>Klantincheck inschakelen

Wanneer de functie voor klantincheck is ingeschakeld, genereert Commerce een orderbevestigings-id (ook wel de afzetkanaalverwijzings-id genoemd). Daarnaast worden orderbevestigings-id's gegenereerd voor orders die zijn gemaakt via kanalen POS of callcenter. 

Als u de functie voor klantincheck wilt inschakelen in Commerce Headquarters, gaat u als volgt te werk.

1. Ga naar **Werkgebieden \> Functiebeheer**.
2. Zoek de functie **Consistente indeling van de kanaalverwijzings-id genereren voor alle kanalen**. 
3. Selecteer de functie en selecteer vervolgens **Nu inschakelen** in het het deelvenster Eigenschappen. 

## <a name="create-a-check-in-confirmation-page"></a>Een pagina voor incheckbevestiging maken

In uw webwinkel moet u een nieuwe pagina maken waarop u het inchecken kunt bevestigen. Met extra configuratie kan de pagina ook een formulier bevatten dat extra informatie van klanten verzamelt, om de afhandeling van de order te bespoedigen. Meer informatie over het instellen van de pagina en de module vindt u in [De module Klantincheck](check-in-pickup-module.md).

## <a name="configure-the-transactional-email-template"></a>De transactionele e-mailsjabloon configureren

U moet een koppeling of knop **Ik ben er** toevoegen aan de sjabloon voor de transactie-e-mail die klanten ontvangen wanneer de order klaar is om te worden opgehaald. Klanten gebruiken deze koppeling of knop om de winkel te laten weten dat ze er zijn om hun bestelling af te halen. 

Voeg de koppeling of knop toe aan de sjabloon die is gekoppeld aan het meldingstype **Inpakken voltooid** en de leveringsmodus die u gebruikt voor het laten afhalen van bestellingen bij een afhaalpunt. Maak in de sjabloon een HTML-koppeling of -knop die naar de URL wijst van de incheckbevestigingspagina die u hebt gemaakt, en die de parameternamen en -waarden bevat, zoals in het volgende voorbeeld wordt weergegeven.

`<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%confirmationid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>`

Meer informatie over het configureren van e-mailsjablonen vindt u in [Transactionele e-mails aanpassen per leveringsmethode](customize-email-delivery-mode.md). 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a>In POS wordt een incheckbevestigingstaak gemaakt

Nadat een klant de winkel heeft laten weten dat hij of zij aanwezig is om een artikel op te halen, worden op de incheckpagina een bevestigingsbericht en een optionele QR-code weergegeven die de orderbevestigings-id van de klant bevat. Tegelijkertijd wordt er een taak gemaakt in de takenlijst in POS voor de winkel waar de klant de order afhaalt. Die taak bevat alle klant- en ordergegevens die nodig zijn om de order af te handelen. Het veld Instructies van de taak bevat de gegevens die via het formulier voor aanvullende informatie van de klant zijn verzameld.

## <a name="end-to-end-testing"></a>Complete tests

Voor het inchecken van klanten moeten specifieke parameters en waarden worden doorgegeven aan de incheckpagina en vervolgens aan de incheck-API voor klanten. Daarom is de gemakkelijkste methode om de functie te testen in een omgeving waarin een testorder kan worden gemaakt en verpakt. Op die manier kan een e-mail Order gereed voor ophalen worden gegenereerd met een URL die de vereiste parameternamen en -waarden bevat.

Volg deze stappen om de incheckfunctie voor klanten te testen.

1. Maak de incheckpagina voor klanten en voeg vervolgens de incheckmodule voor klanten toe en configureer deze. Zie [Inchecken voor afhaalmodule](check-in-pickup-module.md) voor meer informatie. 
1. Check de pagina in, maar publiceer deze niet.
1. Voeg de volgende koppeling toe aan een e-mailsjabloon die door het meldingstype Verpakken is voltooid wordt aangeroepen voor een leveringsmodus van het type Afhalen. Zie voor meer informatie [E-mailsjablonen maken voor transactiegebeurtenissen](email-templates-transactions.md).

    - **Voor preproductieomgevingen (UAT):** voeg het codefragment uit de sectie [De transactionele e-mailsjabloon configureren](#configure-the-transactional-email-template) eerder in dit onderwerp toe.
    - **Voor productieomgevingen**: voeg de volgende becommentarieerde code toe zodat dit voor bestaande klanten geen gevolgen heeft.

        `<!-- https://[DOMAIN]/[CHECK_IN_PAGE]?channelReferenceId=%confirmationid%&channelId=%pickupchannelid%&packingSlipId=%packingslipid%&preview=inprogress -->`

1. Maak een order waarin de leveringsmodus Afhalen is opgegeven.
1. Wanneer u het e-mailbericht ontvangt dat wordt geactiveerd door het meldingstype Verpakken is voltooid, test u de incheckingsstroom door de incheckpagina te openen met de URL die u eerder hebt toegevoegd. Aangezien de URL de vlag `&preview=inprogress` bevat, wordt u gevraagd te verifiëren voordat u de pagina kunt weergeven.
1. Voer aanvullende gegevens in die vereist zijn om de module te configureren.
1. Controleer of de weergave van de incheckbevestiging juist wordt weergegeven.
1. Open een POS-terminal voor de winkel waar de order wordt opgehaald.
1. Selecteer de tegel **Orders die moeten worden opgehaald** en controleer of de order wordt weergegeven.
1. Controleer of extra informatie die in de incheckmodule is geconfigureerd, wordt weergegeven in het detailvenster.

Nadat u hebt gecontroleerd of de incheckfunctie voor klanten van begin tot einde werkt, volgt u deze stappen.

1. Publiceer de incheckpagina.
1. Als u in een productieomgeving test, verwijdert u de opmerking uit de URL in de e-mailsjabloon Order gereed voor ophalen, zodat de koppeling of knop **Accepteren** wordt weergegeven. Daarna kunt u de sjabloon opnieuw uploaden.

## <a name="additional-resources"></a>Aanvullende bronnen

[De module Inchecken voor ophalen](check-in-pickup-module.md)

[Transactionele e-mails aanpassen per leveringsmethode](customize-email-delivery-mode.md)

[E-mailsjablonen maken voor transactiegebeurtenissen](email-templates-transactions.md)
