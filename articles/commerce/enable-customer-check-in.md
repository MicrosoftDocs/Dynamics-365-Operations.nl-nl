---
title: Incheckmeldingen van klanten in Point of Sale (POS) inschakelen
description: In dit onderwerp wordt beschreven hoe u incheckmeldingen voor klanten in het Microsoft Dynamics 365 Commerce POS kunt inschakelen.
author: bicyclingfool
ms.date: 04/23/2021
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
ms.openlocfilehash: b42dc7766f8a69a7409c28d21b49cc96eca18dd4
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271420"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a>Incheckmeldingen van klanten in Point of Sale (POS) inschakelen

[!include [banner](includes/banner.md)]

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

Voeg de koppeling of knop toe aan de sjabloon die is gekoppeld aan het meldingstype **Inpakken voltooid** en de leveringsmodus die u gebruikt voor het laten afhalen van bestellingen bij een afhaalpunt. Maak in de sjabloon een HTML-koppeling of knop die verwijst naar de URL van de pagina voor het bevestigen van het inchecken die u hebt gemaakt. Hier volgt een voorbeeld.

```
<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%channelreferenceid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>
```
Meer informatie over het configureren van e-mailsjablonen vindt u in [Transactionele e-mails aanpassen per leveringsmethode](customize-email-delivery-mode.md). 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a>In POS wordt een incheckbevestigingstaak gemaakt

Nadat een klant de winkel heeft laten weten dat hij of zij er is om de bestelling af te halen, ontvangt hij of zij een bevestigingsmelding voor het inchecken en wordt een taak gemaakt in de takenlijst in POS voor de winkel waar de klant de order afhaalt. De taak bevat alle klant- en ordergegevens die nodig zijn om de order af te handelen. In de taak bevat het veld Instructies alle gegevens die via het formulier voor aanvullende informatie van de klant zijn verzameld. 

## <a name="additional-resources"></a>Aanvullende bronnen

[De module Inchecken voor ophalen](check-in-pickup-module.md)
