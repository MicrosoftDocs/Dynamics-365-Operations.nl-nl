---
title: Uitgebreide aanmeldingsfunctionaliteit instellen voor Cloud POS en MPOS
description: Dit onderwerp gaat over uw opties voor het instellen van de uitgebreide aanmelding voor Cloud POS en Retail moderne POS (MPOS).
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: 499fd5947a96f4a44f09883d5dd0d6124758e47a
ms.contentlocale: nl-nl
ms.lasthandoff: 04/26/2017


---

# <a name="set-up-extended-logon-functionality-for-cloud-pos-and-mpos"></a>Uitgebreide aanmeldingsfunctionaliteit instellen voor Cloud POS en MPOS

[!include[banner](includes/banner.md)]


Dit onderwerp gaat over uw opties voor het instellen van de uitgebreide aanmelding voor Cloud POS en Retail moderne POS (MPOS).

<a name="setting-up-extended-logon"></a>Uitgebreide aanmelding instellen
=========================

U kunt de instellingen voor streepjescodemaskers vinden via **Detailhandel en commerce** &gt; **Kanaalinstellingen** &gt; **POS-instellingen** &gt; **POS-profielen** &gt; **Functionaliteitsprofielen**. Het sneltabblad **Functies** bevat de volgende opties voor uitgebreide aanmelding.

### <a name="staff-bar-code-logon"></a>Personeel aanmelden met streepjescode

Wanneer de optie **Personeel aanmelden met streepjescode** is ingeschakeld, kunnen werknemers die uitgebreide aanmelding hebben toegewezen aan hun POS-referenties zich aanmelden met een streepjescode.

### <a name="staff-bar-code-logon-requires-password"></a>Voor het aanmelden van personeel met een streepjescode is een wachtwoord vereist

Wanneer de optie **Voor het aanmelden van personeel met een streepjescode is een wachtwoord vereist** is ingeschakeld, selecteert Personeel aanmelden met streepjescode alleen de werknemer die is toegewezen aan de uitgebreide aanmelding die wordt voorgesteld. Werknemers moeten nog steeds hun wachtwoord invoeren wanneer deze optie is ingeschakeld.

### <a name="staff-card-logon"></a>Personeel aanmelden met kaart

Wanneer de optie **Personeel aanmelden met kaart** is ingeschakeld, kunnen werknemers die uitgebreide aanmelding hebben toegewezen aan hun POS-referenties zich aanmelden met een magneetstrip.

### <a name="staff-card-logon-requires-password"></a>Voor het aanmelden van personeel met een kaart is een wachtwoord vereist

Wanneer de optie **Voor het aanmelden van personeel met een kaart is een wachtwoord vereist** is ingeschakeld, selecteert Personeel aanmelden met kaart alleen de werknemer die is toegewezen aan de uitgebreide aanmelding die wordt voorgesteld. Werknemers moeten nog steeds hun wachtwoord invoeren wanneer deze optie is ingeschakeld.

<a name="assigning-an-extended-logon"></a>Een uitgebreide aanmelding toewijzen
===========================

Standaard kunnen alleen managers uitgebreide aanmelding aan werknemers toewijzen. Als u uitgebreide aanmelding wilt toewijzen, gaat u naar **Uitgebreid aanmelden** in POS. Zoek vervolgens naar een werknemer door zijn of haar operator-id in het zoekveld in te voeren. Selecteer de werknemer en klik vervolgens op **Toewijzen**. Op de volgende pagina haalt u de uitgebreide aanmelding door of scant u deze om de werknemer toe te wijzen. Als het doorhalen of scannen met succes is gelezen, wordt de knop **OK** beschikbaar. Klik op **OK** om de uitgebreide aanmelding voor die werknemer op te slaan.

<a name="deleting-an-extended-logon"></a>Een uitgebreide aanmelding verwijderen
==========================

U kunt de uitgebreide aanmelding die aan een werknemer is toegewezen verwijderen door te zoeken naar de werknemer met de bewerking **Uitgebreide aanmelding**. Selecteer de werknemer en klik vervolgens op **Verwijderen**. Alle uitgebreide aanmeldreferenties die zijn gekoppeld aan die werknemer, worden verwijderd.

<a name="extending-extended-logon"></a>Uitgebreide aanmelding uitbreiden
========================

De aanmeldservice kan worden uitgebreid om extra aanmeldenapparaten, zoals uitgebreide palmscanners te ondersteunen. Zie de documentatie van POS-uitbreidbaarheid voor meer informatie.

<a name="using-extended-logon"></a>Uitgebreide aanmelding gebruiken
====================

Wanneer de uitgebreide aanmelding is geconfigureerd, en een werknemer een streepjescode of een magneetstrip is toegewezen, moet de werknemer enkel zijn of haar kaart doorhalen wanneer de POS-aanmeldpagina wordt weergegeven. Als een wachtwoord ook vereist is voordat aanmelding kan plaatsvinden, wordt de werknemer gevraagd zijn of haar wachtwoord in te voeren.




