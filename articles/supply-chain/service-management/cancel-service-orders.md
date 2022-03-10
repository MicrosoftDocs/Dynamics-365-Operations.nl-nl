---
title: Serviceorders annuleren
description: U kunt een serviceorder of serviceorderregel vanuit de serviceorder zelf annuleren of u kunt meerdere serviceorders annuleren door een periodieke taak uit te voeren.
author: kamaybac
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cca6c34bb43702e2c33935a73dc24f1a630065c0
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571516"
---
# <a name="cancel-service-orders"></a>Serviceorders annuleren   

[!include [banner](../includes/banner.md)]


U kunt een serviceorder of serviceorderregel vanuit de serviceorder zelf annuleren of u kunt meerdere serviceorders annuleren door een periodieke taak uit te voeren.


> [!NOTE]
> <P>Serviceorders kunnen niet worden geannuleerd als in de fase waarin de serviceorder zich bevindt annuleren niet is toegestaan, als de serviceorder artikelbehoeften heeft of als de serviceorder al is geboekt.</P>


## <a name="cancel-a-service-order-in-the-service-orders-form"></a>Een serviceorder annuleren in het formulier Serviceorders

1.  Klik op **Servicebeheer** \> **Algemeen** \> **Serviceorders** \> **Serviceorders**. Selecteer de serviceorder en klik in het actievenster op **Order annuleren**.

## <a name="cancel-a-service-order-line"></a>Een serviceorderregel annuleren

1.  Klik op **Servicebeheer** \> **Algemeen** \> **Serviceorders** \> **Serviceorders**. Dubbelklik op de serviceorder die de regel bevat die u wilt annuleren.

2.  Selecteer de serviceorderregel die u wilt annuleren en klik vervolgens op **Orderregel annuleren** om de status van de regel te wijzigen in **Geannuleerd**.


> [!TIP]
> <P>Als u de annulering van een serviceorderregel ongedaan wilt maken en de status opnieuw wilt wijzigen in <STRONG>Gemaakt</STRONG>, klikt u op <STRONG>Annuleren intrekken</STRONG>.</P>


## <a name="cancel-multiple-service-orders"></a>Meerdere serviceorders annuleren

1.  Klik op **Servicebeheer** \> **Periodiek** \> **Serviceorders** \> **Serviceorders annuleren**.

2.  Klik op de knop **Selecteren**.

3.  Selecteer in het formulier **Query** de kolom **Criteria** de serviceorders die u wilt annuleren.

4.  Klik op **OK** om het formulier **Query** te sluiten.

5.  Schakel het selectievakje **Infologboek weergeven** in om een infologboek te genereren waarin de geannuleerde serviceorders worden weergegeven.

6.  Schakel het selectievakje **Annuleren intrekken** in als u de status **Geannuleerd** van een serviceorder wilt terugdraaien.

7.  Klik tot slot op **OK**.

De geselecteerde serviceorders worden geannuleerd of de voortgangsstatus **Geannuleerd** wordt gewijzigd in **Onderhanden**.


> [!NOTE]
> <P>Als u het selectievakje <STRONG>Annuleren intrekken</STRONG> inschakelt, worden serviceorders met de voortgangsstatus <STRONG>Geannuleerd</STRONG> teruggedraaid en worden serviceorders met de voortgangsstatus <STRONG>Onderhanden</STRONG> niet geannuleerd.</P>


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]