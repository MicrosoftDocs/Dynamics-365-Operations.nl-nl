---
title: Problemen met procesproductie oplossen
description: In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met procesproductie.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d999c91aa1cc14f29ebfa6be8e456e45ef0d3fa4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966175"
---
# <a name="troubleshoot-process-manufacturing"></a>Problemen met procesproductie oplossen

In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met procesproductie.

## <a name="when-i-use-the-job-card-device-to-report-a-partial-quantity-on-the-last-job-in-a-production-order-all-the-previous-jobs-on-that-order-that-have-a-status-of-in-progress-are-automatically-ended"></a>Wanneer ik het taakkaartapparaat gebruik om een gedeeltelijke hoeveelheid te rapporteren voor de laatste taak in een productieorder, worden alle eerdere taken op die order met de status In uitvoering automatisch beëindigd.

Dit is zo ontworpen. Op de pagina **Standaardwaarden productieorder**, op het tabblad **Rapporteren als gereed** is een optie met de naam **Eindmarkering van route**. Als dit onderwerp is ingesteld op *Ja*, wordt een routekaartjournaal geboekt wanneer een werknemer taakkaartapparaat of taakkaartterminal gebruikt om de laatste bewerking te melden. In dit journaal worden alle bewerkingen gemarkeerd als voltooid en worden alle productietaken beëindigd. Wanneer de optie **Eindmarkering van route** is ingesteld op *Ja*, houdt het systeem geen rekening met de taakstatus die de werknemer heeft geselecteerd bij het melden van de laatste bewerking. Het systeem houdt er ook geen rekening mee of de werk nemer een volledige of gedeeltelijke hoeveelheid rapporteert.

## <a name="when-i-attempt-a-stock-closing-i-receive-the-following-warning-message-no-execution-of-backflush-costing-calculation-with-a-date-1-matching-period-end-has-been-registered"></a>Wanneer ik een voorraadafsluiting probeer, wordt het volgende waarschuwingsbericht weergegeven: "Geen uitvoering van kostprijsberekening via terugwaarts afboeken geregistreerd met datum %1 overeenkomend met een einde-periode."

Als u in releases vóór release 10.0.13 de kostenstroom voor de lean-productie niet gebruikt, wordt tijdens de voorraadafsluiting het volgende onjuiste waarschuwingsbericht weergegeven:

> U staat op het punt een voorraadafsluiting uit te voeren met datum %1. Geen uitvoering van kostprijsberekening via terugwaarts afboeken geregistreerd met datum %1 overeenkomend met een periode-einde. Vergeet niet een kostprijsberekening via terugwaarts afboeken uit te voeren met datum %1 overeenkomend met een periode-einde. De waardering van voorraden, kosten van verkochte goederen en afwijkingen is mogelijk niet juist in journaal of grootboek totdat dit is uitgevoerd.

Dit probleem is opgelost in release 10.0.13 en hoger. Zie voor meer informatie [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]