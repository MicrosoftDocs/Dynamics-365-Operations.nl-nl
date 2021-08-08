---
title: Producten met serienummers retourneren in POS
description: In dit onderwerp worden de mogelijkheden beschreven voor het valideren van geserialiseerde artikelen als onderdeel van het retourproces in de toepassing Microsoft Dynamics 365 Commerce POS (Point of Sale).
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e53c8ceb91a007775fa74f0c9598a65745f01cec
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638092"
---
# <a name="return-serial-numbercontrolled-products-in-pos"></a>Producten met serienummers retourneren in POS

[!include [banner](includes/banner.md)]

In dit onderwerp worden de mogelijkheden beschreven voor het valideren van geserialiseerde artikelen als onderdeel van het retourproces in de toepassing Microsoft Dynamics 365 Commerce POS (Point of Sale).

> [!NOTE]
> In versie 10.0.20 en hoger van Commerce is een nieuwe functie met de naam **Uniforme retourverwerkingservaring in POS** beschikbaar. Schakel deze functie in als u de validatie van serienummers wilt gebruiken tijdens de verwerking van retourorders in POS. Zie [Retouren maken in POS](POS-returns.md) voor informatie over andere mogelijkheden die deze functie biedt wanneer deze is ingeschakeld.
>
> Nadat de functie is ingeschakeld, kan deze niet meer worden uitgeschakeld.

## <a name="options-for-validating-serialized-returns"></a>Opties voor het valideren van geserialiseerde retouren

Wanneer de functie **Uniforme retourverwerkingservaring in POS** is ingeschakeld, kunnen organisaties een validatie uitvoeren op retouren van artikelen met serienummers via POS. Deze mogelijkheid kan gebruikers waarschuwen als het serienummer dat wordt geretourneerd, afwijkt van het oorspronkelijke serienummer dat is verkocht. In de release van Commerce versie 10.0.20 en hoger is het bericht dat gebruikers ontvangen slechts een waarschuwingsbericht. Gebruikers kunnen een retour blijven verwerken voor een serienummer dat afwijkt van het serienummer dat oorspronkelijk is verkocht.

Als u validatie van serienummers voor een organisatie wilt configureren nadat de functie **Uniforme retourverwerkingservaring in POS** is ingeschakeld, gaat u naar **Retail en Commerce \> Instelling van hoofdkantoor \> Parameters \> Commerce-parameters** in Commerce Headquarters. Stel op het tabblad **Voorraad** op het sneltabblad **Winkelvoorraadbewerkingen** de optie **Validatie van serienummers in POS-retouren inschakelen** in op **Ja**.

## <a name="process-returns-for-serialized-items-in-pos"></a>Retouren verwerken voor geserialiseerde artikelen in POS

Als de optie **Validatie van serienummers in POS inschakelen** is ingesteld op **Ja** wanneer een artikel met serienummer wordt geretourneerd via het POS, kan de gebruiker het serienummer voor de retourregel invoeren in het detaildeelvenster op de pagina **Retourneerbare producten**. Als het ingevoerde serienummer niet gelijk is aan het oorspronkelijke serienummer dat is verkocht voor de verkooptransactie, wordt een waarschuwingsbericht weergegeven. De toepassing voorkomt echter niet dat de gebruiker de retour kan blijven boeken.

> [!NOTE]
> Op dit moment ondersteunt POS validatie van serienummers alleen voor retourregels waar de oorspronkelijke bestelde hoeveelheid niet meer dan één is. Als de oorspronkelijke verkooporderregel is gemaakt in een niet-POS-kanaal en als de bestelde hoeveelheid voor het geserialiseerde artikel op een bepaalde verkoopregel meer dan één is, kan het artikel niet op de juiste manier worden geretourneerd via het POS.

## <a name="additional-resources"></a>Aanvullende bronnen

[Retouren maken in POS](POS-returns.md)
