---
title: Leenartikelen maken
description: Leenartikelen zijn records waarmee u fysieke artikelen, zoals telefoons of computers die uw bedrijf aan werknemers uitleent, bijhoudt.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmLoanType, DefaultDashboard, HcmLoanItem, HcmWorkerLookUp
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 75b2f17eb41ead7422276f72429eb6ede2ef4759
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177272"
---
# <a name="create-loan-items"></a>Leenartikelen maken

[!include [task guide banner](../../includes/task-guide-banner.md)]

Leenartikelen zijn records waarmee u fysieke artikelen, zoals telefoons of computers die uw bedrijf aan werknemers uitleent, bijhoudt. Elke fysiek artikel moet een bijbehorend leenartikel hebben. Bij elk leenartikelrecord moet worden beschreven wat er precies wordt uitgeleend, wie ervoor verantwoordelijk is en het aantal dagen dat een artikel kan worden geleend. U kunt meerdere uitleenartikelen zoals sleutels, toegangskaarten of uniformen tegelijk maken. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.


## <a name="create-loan-types"></a>Leningtypen maken
1. Ga naar Human resources > Werknemers > Leenartikelen > Leningtypen.
2. Klik op Nieuw.
3. Typ een waarde in het veld Leningtype.
4. Typ een waarde in het veld Omschrijving.
5. Voer het aantal dagen in dat artikelen die zijn toegewezen aan dit leningtype over tijd mogen zijn. 
6. Klik op Opslaan.
7. Sluit de pagina.
8. Vernieuw de pagina.

## <a name="create-loan-items"></a>Leenartikelen maken
1. Ga naar Human resources > Werknemers > Leenartikelen > Leenartikelen.
2. Klik op Leenartikelen maken.
3. Voer in het veld Hoeveelheid een getal in.
4. Typ een waarde in het veld Omschrijving.
5. Klik in het veld Leningtype op de vervolgkeuzeknop om de zoekopdracht te openen.
6. Zoek en selecteer het gewenste record in de lijst.
7. Klik in de lijst op de koppeling in de geselecteerde rij.
8. Het aantal dagen invoeren dat het artikel kan worden uitgeleend.
    * De standaardwaarde van het veld Geplande teruggave op de pagina Geleende uitrusting wordt berekend als de huidige datum plus dit getal.  
9. Klik in het veld Verantwoordelijke persoon op de vervolgkeuzeknop om de zoekopdracht te openen.
10. Klik op Selecteren.
11. Typ een waarde in het veld Beginwaarde.
12. Typ een getal in het veld Interval.
13. Typ een waarde in het veld Notatie.
    * Als het beginnummer voor een leenartikel bijvoorbeeld 10 is, voert u twee hekjes in het veld Notatie in.  
14. Klik op OK.
15. Vernieuw de pagina.

