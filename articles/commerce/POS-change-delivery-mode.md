---
title: Leveringsmethode wijzigen in POS
description: In dit onderwerp wordt beschreven hoe u de bewerking Leveringsmethode wijzigen in POS configureert en gebruikt.
author: hhainesms
ms.date: 03/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: fd69d82536047c06e94ba4a7e860ef54680619a4
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193126"
---
# <a name="change-mode-of-delivery-in-pos"></a>Leveringsmethode wijzigen in POS

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u de functionaliteit Leveringsmethode wijzigen kunt instellen en gebruiken in uw POS-omgeving. 

In Dynamics 365 Commerce 10.0.10 en hoger is de bewerking **Leveringsmethode wijzigen** (647) beschikbaar om aan uw POS-schermindelingen toe te voegen.

De functie Leveringsmethode wijzigen biedt u de optie om de leveringsmethode te wijzigen voor een of meer voor verkoop geconfigureerde verkoopregels in de POS-transactie. In eerdere versies van Commerce moest u de volledige configuratiestromen **Alles verzenden** of **Selectie verzenden** doorlopen als u de leveringsmethode wilde wijzigen voor een bestaande regel die voor verzending was geconfigureerd. Dit proces was tijdrovend en kon leiden tot onbedoelde wijzigingen in de leveringsoorsprong of leveringsdatums voor de regel. De nieuwe functionaliteit biedt een alternatieve methode voor het efficiënt bijwerken van de leveringsmethode op deze verkoopregels.

Zie [Schermindelingen voor het verkooppunt](pos-screen-layouts.md) voor meer informatie over het toevoegen van een bewerking aan een knop in uw POS-knoppenraster.

Wanneer deze functie is geconfigureerd in POS en u **Leveringsmethode wijzigen** selecteert, wordt er een lijstpagina weergegeven waarop u de regels kunt kiezen van de transactie waarvoor u de leveringsmethode wilt wijzigen. U kunt enkele of alle regels kiezen of afsluiten zonder wijzigingen aan te brengen. De verkoopregels die eerder waren geconfigureerd voor verzending, zijn de enige regels in de lijst die u kunt wijzigen. Als u een regel wilt wijzigen die is toegewezen voor ophalen of uitvoeren voor verzending, moet u de bewerking **Alles verzenden** of **Selectie verzenden** gebruiken. Als u daarentegen een regel wilt wijzigen die is aangewezen voor ophalen of uitvoering, moet u de bewerking **Alles ophalen**, **Selectie ophalen**, **Alles uitvoeren** of **Selectie uitvoeren** gebruiken.

Nadat u de regels hebt geselecteerd die u wilt wijzigen, klikt u op **Leveringsmethode wijzigen** om te worden gevraagd de opties voor de leveringsmethode te selecteren. Als u meerdere regels hebt geselecteerd om te wijzigen, worden in POS alleen leveringsmethoden weergegeven die zijn geconfigureerd als toegestaan voor alle geselecteerde producten. Leveringsmethoden kunnen worden geconfigureerd voor de ondersteuning van specifieke producten en leveringsadressen. Als er een leveringsmethode is die acceptabel is voor één combinatie van product en adres, maar die niet acceptabel is voor een andere geselecteerde combinatie van product en adres, is de leveringsmethode niet beschikbaar. U moet mogelijk regels één voor één selecteren en de leveringsmethode voor elke regel afzonderlijk wijzigen als u een leveringsmethode wilt selecteren voor een product dat niet door een ander product wordt ondersteund.  

Nadat u de nieuwe leveringsmethode hebt geselecteerd, wordt de transactiepagina weergegeven. Als u de nieuwe selecties voor de leveringsmethode wilt controleren, selecteert u het tabblad **Levering** in de transactielijst.

## <a name="additional-resources"></a>Aanvullende bronnen

[Callcenterorders maken](tasks/create-call-center-orders.md)

[Transactionele e-mails aanpassen per leveringsmethode](customize-email-delivery-mode.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]