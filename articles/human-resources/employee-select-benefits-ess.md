---
title: Werknemers selecteren plannen via Werknemerselfservice (optioneel)
description: In dit onderwerp wordt beschreven hoe werknemers hun vergoedingen kunnen selecteren of bijwerken.
author: twheeloc
ms.date: 12/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 68aa401487a74b9fcd186ec6cbdb268cdb41168c
ms.sourcegitcommit: e4cc43b06ef3f0f562849e2c960025cb244d6017
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2022
ms.locfileid: "8743481"
---
# <a name="employees-select-plans-by-using-employee-self-service-optional"></a>Werknemers selecteren plannen via Werknemerselfservice (optioneel)


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Wanneer een nieuwe werknemer in dienst wordt genomen, kan deze werknemers **Werknemerselfservice** gebruiken om zijn/haar vergoedingen te selecteren of bijwerken via open inschrijving.

Voor toegang tot zijn/haar vergoedingen voor inschrijving gaat de werknemer naar **Werknemerselfservice** en selecteert hij/zij **Selfservice voor vergoedingen** op de tegel **Vergoedingen**.

Op de pagina **Selfservice voor vergoedingen** worden vergoedingsplannen gegroepeerd op plantype. Om de vergoedingsplannen in een plantype weer te geven, selecteert de werknemer een tegel op de pagina **Werknemersvergoedingen**. De werknemer krijgt alleen de vergoedingen te zien waar hij of zij recht op heeft.

> [!IMPORTANT]
> Voordat een plantype kan worden weergegeven in **Werknemerselfservice**, moet het worden geconfigureerd. Zie [Werknemerselfservice configureren](/dynamics365/human-resources/hr-benefits-setup-employee-self-service) voor meer informatie.

Afhankelijk van het plantype, kunnen een of meer vergoedingen voor inschrijving worden geselecteerd. Een medisch plantype kan bijvoorbeeld worden geconfigureerd om de werknemer te beperken tot één medisch plan. Met een plan van het type Levensverzekering kan de werknemer meerdere levensverzekeringsplannen selecteren.

Nadat de werknemer heeft bepaald met welk plan hij of zij zich wil inschrijven, moet deze mogelijk gezinsleden selecteren. Als de werknemer de dekkingsoptie **Werknemer +1**, **Werknemer + kinderen** of **Familie** heeft geselecteerd, moeten gezinsleden worden geselecteerd. Zie [Opties voor dekking maken](/dynamics365/human-resources/hr-benefits-setup-coverage-options) voor meer informatie over dekkingsopties.

Om een vergoedingsplan te selecteren, moet de werknemer de knop met het beletselteken (**...**) of **Toevoegen aan winkelwagen** selecteren. Wanneer de werknemer alle vergoedingsselecties aan de winkelwagen heeft toegevoegd, selecteert hij of zij **Winkelwagen bekijken**. De werknemer wordt vervolgens naar de pagina **Plannen** genomen, waar hij of zij de geselecteerde en kwijtgescholden vergoedingsplannen kan bekijken.

De werknemer moet de optie **Accepteren** selecteren voordat hij of zij de knop **Uitchecken** kan selecteren. De verklaring rechts van de optie **Accepteren** kan worden aangepast op het tabblad **Vergoedingenbeheer** van de pagina **Gedeelde parameters voor Human Resources**.

Wanneer de werknemer de selecties van zijn of haar vergoedingsplan bevestigt via **Werknemerselfservice**, worden deze selecties geregistreerd en weergegeven op de pagina's **Vergoedingsplannen voor medewerker** en **Bulkupdate van vergoedingsplannen voor medewerkers**.

Nadat de werknemer de plannen heeft geselecteerd, wordt de status van de vergoedingen weergegeven als **Geselecteerd**. Als de werknemer **Uitchecken** selecteert op de pagina **Selfservice voor vergoedingen**, wordt de optie **Uitgecheckt** geselecteerd.

> [!IMPORTANT]
> Om de inschrijving te voltooien, moet de vergoedingenbeheerder **Bevestigen** selecteren voor elke werknemervergoeding die is geselecteerd. De bevestiging kan worden voltooid op de pagina **Vergoedingenplan medewerker** of **Bulkupdate van vergoedingsplannen voor medewerkers**.
>

Werknemers zijn niet verplicht om vergoedingen te selecteren via **Werknemerselfservice**. Vergoedingen kunnen namens een werknemer wordt geselecteerd op de pagina **Vergoedingenplan medewerker** of **Bulkupdate van vergoedingsplannen voor medewerkers**. De werknemer wordt pas voor deze vergoedingen ingeschreven als de vergoedingenbeheerder deze heeft bevestigd.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
