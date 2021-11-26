---
title: Uitgestelde verwerking van handmatige voorraadmutaties
description: In dit onderwerp wordt beschreven hoe u uitgestelde verwerking van handmatige voorraadmutaties in Microsoft Dynamics 365 Supply Chain Management gebruikt.
author: Mirzaab
ms.date: 04/27/2021
ms.topic: article
ms.search.form: WHSWorkProcessingPolicy, WHSWorkDeferredPutProcessingTask
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: Mirzaab
ms.search.validFrom: 2021-04-27
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: f5c9ba7079895feeb0c171f2021479587aa13cc9
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/09/2021
ms.locfileid: "7777661"
---
# <a name="deferred-processing-of-manual-inventory-movement"></a>Uitgestelde verwerking van handmatige voorraadmutaties

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u uitgestelde verwerking van handmatige voorraadmutaties in Microsoft Dynamics 365 Supply Chain Management gebruikt.

Met uitgestelde verwerking kunnen magazijnmedewerkers doorgaan met ander werk terwijl de wegzetbewerking op de achtergrond wordt verwerkt. Uitgestelde verwerking is ook handig wanneer de server incidentele of niet-geplande verhogingen in verwerkingstijd kan hebben, en de toegenomen verwerkingstijd kan invloed hebben op de productiviteit van de medewerkers. Het werktype *Voorraadmutatie* is nu toegevoegd aan de set werktypen die deze functie ondersteunt.

De achtergrondverwerking wordt gerealiseerd met de functie [Gebeurtenissen van de magazijnapp verwerken](warehouse-app-events.md).

## <a name="turn-on-this-feature-for-your-system"></a>Deze functie inschakelen voor uw systeem

Als u deze functie beschikbaar wilt maken, schakelt u de volgende functies in [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) in: U moet ze in deze volgende volgorde in- of uitschakelen:

1. Werk blokkeren voor de hele organisatie (vanaf Supply Chain Management versie 10.0.21 is deze functie verplicht, waardoor deze standaard wordt ingeschakeld en niet meer kan worden uitgeschakeld.)
1. Gebeurtenissen in magazijnapp verwerken
1. Uitgestelde put-bewerkingen
1. Uitgestelde verwerking van handmatige bewerking voor voorraadmutatie

## <a name="configure-the-work-processing-policies"></a>Het beleid voor werkverwerking configureren

Om uitgestelde verwerking te gebruiken, moet u beleid voor werkverwerking configureren en gebruiken. Voor uitgestelde wegzetverwerking biedt de [functie Uitgestelde verwerking van magazijnwerk](deferred-put.md) ondersteuning voor de volgende werktypen: *Verkooporder*, *Uitgifte van overboekingsorder* en *Aanvulling*. De functie *Uitgestelde verwerking van handmatige voorraadmutaties* voegt hieraan een nieuw werktype toe: *Voorraadmutatie*.

Volg deze stappen om beleid voor werkverwerking in te stellen.

1. Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werkverwerkingsbeleid**.
1. Selecteer een bestaand beleid in de lijst of maak een nieuw beleid aan door **Nieuw** in het actievenster te selecteren. De koptekst van elk beleid heeft de volgende velden:

    - **Naam werkverwerkingsbeleid**: de naam van het werkverwerkingsbeleid.
    - **Beschrijving:** een beschrijving van het werkverwerkingsbeleid.

1. Stel op het sneltababwerk **Verwerkingsregels** de verzameling regels in waarop het beleid van toepassing is. Gebruik de knoppen op de werkbalk om de gewenste rijen toe te voegen en te verwijderen. Stel voor elke regel de volgende velden in:

    - **Werkordertype**: selecteer het werktype waarop het beleid van toepassing is.
    - **Bewerking**: selecteer de bewerking die het beleid gebruikt voor de verwerking. Als u *Voorraadmutatie* hebt geselecteerd in het veld **Werkordertype**, hoeft u dit veld niet in te stellen, omdat zowel verzamel- als wegzetbewerkingen worden verwerkt als één gebeurtenis.
    - **Werkverwerkingsmethode**: Selecteer de methode die wordt gebruikt om de werkregel te verwerken. Als u *Direct* selecteert, lijkt het gedrag op het gedrag waarbij geen werkverwerkingsbeleid wordt gebruikt om de regel te verwerken. Als u *Uitgesteld* selecteert, wordt uitgestelde verwerking toegepast die gebruikmaakt van het batchframework.
    - **Drempel voor uitgestelde verwerking**: Als u dit veld in stelt op *0* (nul), is er geen drempel. In dit geval wordt de verwerkingsmethode *Uitgesteld* gebruikt waar dat kan. Als de specifieke drempelberekening onder de drempelwaarde ligt, wordt de methode *Direct* gebruikt. Anders wordt de methode *Uitgesteld* gebruikt als dat kan. Voor verkoop- en overdrachtsgerelateerd werk wordt de drempel berekend als het aantal gekoppelde bronbelastingsregels dat voor het werk wordt verwerkt. Voor aanvullingswerk wordt de drempel berekend als het aantal werkregels dat door het werk wordt aangevuld. Door een drempelwaarde van bijvoorbeeld *5* in te stellen voor verkoop, zorgt u ervoor dat kleiner werk met minder dan vijf oorspronkelijke bronbelastingsregels geen uitgestelde verwerking gebruikt, maar groter werk gebruikt dit wel. De drempelwaarde heeft alleen effect als het veld **Werkverwerkingsmethode** is ingesteld op *Uitgesteld*.
    - **Batchgroep voor uitgestelde verwerking**: Geef de batchgroep op die voor de verwerking wordt gebruikt. Als u *Voorraadmutatie* hebt geselecteerd in het veld **Werkordertype**, hoeft u dit veld niet in te stellen, omdat de batchgroep is geselecteerd in het dialoogvenster **Gebeurtenissen in magazijnapp verwerken**.

## <a name="assign-the-work-creation-policy"></a>Het beleid voor het maken van werk toewijzen

Meer informatie over het toewijzen van een beleid voor het maken werk vindt u in [Uitgestelde verwerking van magazijnwerk](deferred-put.md).

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>Een batchtaak instellen om gebeurtenissen van de app voor magazijnbeheer te verwerken

Als u het proces *Uitgestelde verwerking van handmatige voorraadmutaties* wilt gebruiken, stelt u een geplande batchtaak in.

1. Ga naar **Magazijnbeheer \> Periodieke taken \> Gebeurtenissen in app voor magazijnbeheer verwerken**.
1. Stel in het dialoogvenster **Gebeurtenissen in magazijnapp verwerken** op het sneltabblad **Op de achtergrond uitvoeren** de optie **Batchverwerking** in op *Ja*.
1. Selecteer **Terugkeerpatroon** en stel een schema in dat voldoet aan de behoeften van uw bedrijf.
1. Selecteer **OK** in elk dialoogvenster.

## <a name="inquire-about-the-warehouse-app-events"></a>Informatie opvragen over gebeurtenissen van de magazijnapp

U kunt de gebeurtenissenwachtrij en gebeurtenisberichten die de magazijnapp genereert, weergeven door te gaan naar **Magazijnbeheer \> Query's en rapporten \> Logboeken voor mobiel apparaat \> Gebeurtenissen in app voor magazijnbeheer**.

De gebeurtenisberichten voor *Voorraadmutatie* hebben de status *In wachtrij* nadat ze zijn gemaakt. Deze status geeft aan dat de batchtaak **Gebeurtenissen in app voor magazijnbeheer verwerken** de gebeurtenisberichten ophaalt en verwerkt. Wanneer de status wordt gewijzigd in *Voltooid*, worden alle gerelateerde gebeurtenissen uit de wachtrij verwijderd.

Alle *Voorraadmutatie*-gebeurtenissen worden bij samengevoegd in één verzameling per gebeurtenistype en magazijn.

Met de batchtaak worden de gebeurtenissen uit de magazijnapp verwerkt op basis van het terugkeerpatroon dat is ingesteld in het dialoogvenster **Gebeurtenissen uit de magazijnapp verwerken**. Zo kunt u, totdat een bericht wordt verwerkt, de magazijn-id vinden door in het veld **Identificatie** te zoeken.

De details van het bericht bevatten de details van de mutatie (bijvoorbeeld de locaties 'van' en 'naar').

Zie [Verwerking van de gebeurtenis van de app voor magazijnbeheer](warehouse-app-events.md) voor meer informatie.

## <a name="configure-the-mobile-device-menu-to-skip-the-deferred-processing-policy"></a>Het menu voor het mobiele apparaat configureren om het beleid voor uitgestelde verwerking over te slaan

Meer informatie over het configureren van het menu op het mobiele apparaat om het beleid voor uitgestelde verwerking over te slaan, vindt u in [Uitgestelde verwerking van magazijnwerk](deferred-put.md).

## <a name="impact-on-closed-work-dates"></a>Impact op datums waarop het werk is gesloten

Meer informatie over het effect op datums voor sluiting van werk vindt u in [Uitgestelde verwerking van magazijnwerk](deferred-put.md).

## <a name="additional-resources"></a>Aanvullende bronnen

- [Uitgestelde verwerking van magazijnwerk](deferred-put.md)
- [Verwerking van gebeurtenissen in magazijnapp](warehouse-app-events.md)
- [Mobiele apparaten instellen voor magazijnwerk](configure-mobile-devices-warehouse.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
