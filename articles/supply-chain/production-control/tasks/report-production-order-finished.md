---
title: Een productieorder gereedmelden
description: Deze procedure toont aan hoe u een productieorder gereedmeldt.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmReportFinished, ProdJournalTransProd, ProdSetupReportFinished
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5d9dcdbcb89df6430fb286c253ebecfc6d885af8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011142"
---
# <a name="report-a-production-order-as-finished"></a>Een productieorder gereedmelden

[!include [banner](../../includes/banner.md)]

Deze procedure toont aan hoe u een productieorder gereedmeldt. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. Dit is de zesde procedure van zeven die de productieorderlevenscyclus beschrijven.


## <a name="report-a-production-order-as-finished"></a>Een productieorder gereedmelden
1. Ga naar Productiebeheer > Productieorders > Alle productieorders.
    * Selecteer een productieorder met de status Gestart.  
2. Klik in het actievenster op Productieorder.
3. Klik op Gereedmelden.
    * Op deze pagina kunt u de hoeveelheid bevestigen van het eindproduct die moet worden gereedgemeld.  
4. Klik op het tabblad Algemeen.
5. Stel Goede hoeveelheid in op '18'.
6. Stel Slechte hoeveelheid in op '2'.
7. Selecteer 'Materiaal' in het veld Foutoorzaak.
8. Schakel selectievakje Taak beëindigen in of uit.
9. Schakel het selectievakje Fout accepteren in of uit.
10. Klik op OK.

## <a name="verify-the-report-as-finished-journal"></a>Het gereedmeldingsjournaal verifiëren
1. Klik in het actievenster op Weergeven.
2. Klik op Gereedgemeld.
3. Markeer in de lijst de geselecteerde rij.
4. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Het gereedmeldingsjournaal is geboekt. Als u aan het journaal correcties wilt aanbrengen, kunt u handmatig een nieuw journaal maken waarin u wijzigingen kunt aanbrengen.  

