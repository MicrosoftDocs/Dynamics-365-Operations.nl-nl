---
title: Korting voor verzending
description: In dit artikel worden de kortingsmogelijkheden voor verzending in Microsoft Dynamics 365 Commerce beschreven en de instellingen die nodig zijn om deze te gebruiken.
author: ShalabhjainMSFT
ms.date: 08/23/2020
ms.topic: overview
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2019-01-31
ms.openlocfilehash: f19566ce64becea4a53a8479cb5a08579567cda1
ms.sourcegitcommit: 1dbff0b5fa1f4722a1720fac35cce94606fa4320
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/24/2022
ms.locfileid: "9346384"
---
# <a name="shipping-discount"></a>Korting voor verzending

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

In dit artikel worden de kortingsmogelijkheden voor verzending in Microsoft Dynamics 365 Commerce beschreven en de instellingen die nodig zijn om deze te gebruiken.

Gratis verzending of verzending korting is een factor die van invloed is op de online aankoopbeslissingen van klanten. Om hun opbrengst per transactie te verhogen, gebruiken veel detailhandelaren een gratis verzendvoordeel om klanten te motiveren hun winkelwageninhoud te vergroten.

Commerce ondersteunt een mogelijkheid voor verzendkortingen waarmee detailhandelaren een kortingspercentage kunnen configureren op de kosten van een specifieke verzendmethode wanneer het totale verkoopbedrag voor gekwalificeerde artikelen in de transactie voldoet aan specifieke criteria. Een voorbeeld van een scenario waarbij de mogelijkheid voor verzendkorting wordt gebruikt, is 'Besteed $ 50 of meer voor gratis levering binnen 24 uur'.

## <a name="prerequisites"></a>Vereisten

De mogelijkheid voor verzendkortingen wordt ondersteund door de [geavanceerde omnichannel-functies voor automatische toeslagen](/dynamics365/unified-operations/retail/omni-auto-charges) van Commerce. Als u de mogelijkheid voor verzendkortingen wilt gebruiken, moet u de configuratie **Geavanceerde automatische toeslagen gebruiken** inschakelen op het tabblad **Klantorders** van de pagina **Commerce-parameters** in Commerce Headquarters. Detailhandelaren kunnen de functie voor geavanceerde automatische toeslagen gebruiken om verschillende typen toeslagen in te stellen, zoals verwerking, installatie en afstoting.

De verzendkorting wordt alleen toegepast op de verzendkosten. Daarom moet een detailhandelaar opgeven welke toeslagen verzendkosten zijn. Als u verzendkosten wilt opgeven, gaat u in Commerce Headquarters naar **Afzetkanaalinstellingen \> Toeslagen \> Toeslagcode** en stelt u de optie **Verzendkosten** in op **Ja** voor de gewenste toeslagen.

![Het opgeven van een toeslag als verzendkosten.](./media/Specify_shipping_charge.png)

## <a name="configuration"></a>Configuratie

De mogelijkheid voor verzendkorting is gebaseerd op niveaus en ondersteunt alleen het berekeningstype **Kortingspercentage**. Als u een verzendkorting wilt instellen, gaat u in Commerce Headquarters naar **Prijzen en kortingen \> Drempelkorting verzending**. Geef vervolgens de leveringsmodus op waarop de korting van toepassing is, definieer een of meer bedragdrempels en stel het kortingspercentage voor elke drempel in. U kunt ook een lijst met categorieën of producten configureren als gekwalificeerde artikelen. Op die manier wordt alleen het verkoopbedrag voor die artikelen in een transactie meegeteld wanneer de prijsengine evalueert of het transactietotaal aan de drempel voldoet.

> [!NOTE]
> In tegenstelling tot andere kortingstypen worden voor de verzendkorting geen kortingsregels gemaakt. In plaats daarvan worden de verzendkosten direct bewerkt en wordt de naam van de korting aan de omschrijving van de toeslag toevoegen.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
