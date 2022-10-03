---
title: Leverancierscertificering onderhouden
description: In dit artikel worden de stappen beschreven waarmee leveranciers hun certificaten kunnen onderhouden met behulp van het werkgebied Leverancierssamenwerking.
author: TaylorVH
ms.date: 04/27/2021
ms.topic: article
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: TaylorVH
ms.search.validFrom: 2021-02-09
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c66952d19cddd9d4a9a102ba59e8d6d97b75ed4d
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/22/2022
ms.locfileid: "9583200"
---
# <a name="maintain-vendor-certification"></a>Leverancierscertificering onderhouden

[!include [banner](../includes/banner.md)]

In dit artikel worden de stappen beschreven waarmee uw leveranciers hun certificaten kunnen onderhouden met behulp van het werkgebied **Leverancierssamenwerking**. Certificaten kunnen bijvoorbeeld worden toegekend voor initiatieven op gebied van vrouwelijke ondernemers of milieuvriendelijke producten. Leveranciers moeten certificeringsgegevens invoeren in het werkgebied **Leveranciergegevens**. Hier selecteren leveranciers **Meer details** en vervolgens **Certificaten**.

## <a name="turn-on-the-vendor-certification-feature"></a>De functie voor leverancierscertificering inschakelen

Voordat u deze functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen gebruikmaken van de pagina [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en deze zo nodig in te schakelen. Schakel in het werkgebied **Functiebeheer** de functie als volgt in:

- **Module** - *Leveranciers*
- **Functienaam** - *Certificeringsbeheer voor leverancierssamenwerking inschakelen*

## <a name="add-a-new-certification"></a>Een nieuwe certificering toevoegen

Als u een nieuw certificaat wilt toevoegen, klikt u op de knop **Toevoegen** die zich boven het raster **Certificaat** in het werkgebied **Leveranciergegevens** bevindt. Voer de volgende gegevens in:

- Certificaatnummer
- Certificaattype
- Certificaatorganisatie
- Certificaatdatum
- Aansprakelijkheidsbedrag, indien van toepassing
- Ingangsdatum
- Verloopdatum
- Opmerkingen, optioneel

Als er documenten zijn die betrekking hebben op het specifieke certificaat, kunt u deze koppelen door de knop **Document** te selecteren.

Aan certificaten die door uw leveranciers op deze pagina worden ingevoerd, wordt de bron 'Leverancier' toegewezen. U kunt certificaatgegevens namens uw leverancier invoeren onder bankrekeningen van de leverancier. De informatie wordt hier weergegeven en de bron wordt getoond als **Klant**.

Leveranciers kunnen hun certificaten zo nodig bewerken of verwijderen.

## <a name="vendor-collaboration-generated-certification-records"></a>Door leverancierssamenwerking gegenereerde certificeringsrecords

Nadat certificeringsgegevens zijn toegevoegd door een leverancier, is de informatie zichtbaar op de pagina **Door leverancierssamenwerking gegenereerde certificeringen**. U opent de pagina door naar **Leveranciers > Query's > Leveranciersrapporten > Door leverancierssamenwerking gegenereerde certificeringen** te gaan. Standaard zijn alle nieuwe of gewijzigde certificeringsrecords zichtbaar. Een medewerker Leveranciers kan de wijzigingen bekijken en de informatie valideren via het bevestigingsproces voor validatie. Wanneer de informatie is bevestigd, kan de certificeringsrecord op de pagina worden geselecteerd en als beoordeeld worden gemarkeerd. Als u de record markeert als beoordeeld, wordt deze uit de standaardlijst verwijderd.

Alle certificeringswijzigingen worden weergegeven op de pagina **Door leverancierssamenwerking gegenereerde certificeringen**. Als een wijziging niet op de pagina wordt weergegeven, kunt u deze weergeven door de filters voor de leveranciersrekening en het ingangsdatumbereik aan te passen of te kiezen of u informatie wilt opnemen voor certificeringswijzigingen die zijn beoordeeld.

