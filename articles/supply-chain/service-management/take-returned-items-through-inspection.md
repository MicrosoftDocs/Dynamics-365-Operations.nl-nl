---
title: Retourartikelen aan een inspectie onderwerpen
description: Onderwerp retourartikelen aan een inspectie.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bdc42f9c5ece8e2c2570cadf623f52648b7b174e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425604"
---
# <a name="take-returned-items-through-inspection"></a>Retourartikelen aan een inspectie onderwerpen 

[!include [banner](../includes/banner.md)]


1.  Klik op **Voorraadbeheer** \> **Periodiek** \> **Kwaliteitsbeheer** \> **Quarantaineorders**.

2.  Zoek de orderregel op van het geretourneerde artikel dat u controleert.

    > [!NOTE]
    > <P>Een quarantaineorder kan alleen aan een enkel artikelnummer worden gekoppeld. Als er in een enkele zending tien artikelen met verschillende artikelnummers worden geretourneerd en in quarantaine worden geplaatst, worden er tien verschillende quarantaineorders gemaakt.</P>

3.  Nadat u het artikel hebt gecontroleerd, geeft u met behulp van het veld **Beschikkingscode** aan wat er met het artikel moet gebeuren en hoe de gerelateerde financiële transacties ervoor worden afgehandeld. Voorbeelden daarvan zijn onder andere het weer toevoegen van het artikel aan de voorraad en het restitueren van de klant, het vernietigen van het artikel en het sturen van eenzelfde artikel naar de klant of het terugsturen van het artikel naar de klant zonder de klant te crediteren.
    
    > [!NOTE]
    > <P>Als er geen beschikkingscode kan worden toegewezen aan meerdere geretourneerde artikelen in een batch met één artikelnummer, moet u de quarantainecode splitsen (<STRONG>Functies</STRONG> &gt; <STRONG>Splitsen</STRONG>) om aan elke subbatch een andere dispositiecode te kunnen toewijzen.</P>


4.  Wanneer u klaar bent met de inspectie, klikt u op **Gereedmelden** om de geretourneerde artikelen vrij te geven en een journaalpost te maken. De persoon of de afdeling die de artikelen ontvangt, verwerkt het journaal voor de artikelen die weer aan de voorraad moeten worden toegevoegd.
    
    – of –
    
    Beëindig de quarantaineorder en plaats de artikelen rechtstreeks terug in de voorraad via een van de functies voor **Voorraad**.

5.  Sluit het formulier om de wijzigingen op te slaan.

## <a name="see-also"></a>Zie ook

[Opgeven op welke wijze retourartikelen moeten worden afgestoten](specify-how-to-dispose-of-returned-items.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]