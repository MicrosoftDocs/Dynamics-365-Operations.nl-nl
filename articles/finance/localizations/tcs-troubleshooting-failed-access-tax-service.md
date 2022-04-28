---
title: Kan geen toegang krijgen tot de belastingservice
description: In dit onderwerp wordt uitgelegd hoe u een toegangsprobleem oplost in de service voor belastingberekening.
author: hangwan
ms.date: 03/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 02/16/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: f4682b83405071b4ad7647958122ab2b4e082133
ms.sourcegitcommit: 2977e92a76211875421e608555311c363cfbdc25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/16/2022
ms.locfileid: "8612311"
---
# <a name="failed-to-access-tax-service"></a>Kan geen toegang krijgen tot de belastingservice

[!include [banner](../includes/banner.md)]


In dit onderwerp wordt uitgelegd hoe u de fout 'Geen toegang tot de belastingservice' van de Belastingberekeningsservice herstelt.

## <a name="symptoms"></a>Symptomen

In Microsoft Dynamics 365 Finance gaat u naar **Belasting** \> **Instellen** \> **Belastingconfiguratie** \> **Belastingserviceparameters**. Schakel op het tabblad **Algemeen** de optie **Belastingberekening inschakelen** in. Als u vervolgens een waarde probeert te selecteren in het veld **Naam van de functie-instelling**, treedt er een fout op. In het foutbericht staat: 'De toegang tot de belastingservice is mislukt'.

## <a name="cause"></a>Oorzaak

Deze fout treedt op omdat Finance geen toegang heeft tot de belastingberekeningsservice.

## <a name="resolution"></a>Oplossing 

1. Meld u aan bij Microsoft Dynamics LCS (LifeCycle Services).
2. Zoek op de pagina **Omgeving** op het tabblad **Invoegtoepassingen voor omgeving**, het item **Belastingberekening** en bekijk de status. De status moet **Wordt geïnstalleerd** of **Geïnstalleerd** zijn. Als de invoegtoepassing Belastingberekening niet is geïnstalleerd, wordt de fout weergegeven.

## <a name="mitigation"></a>Risicobeperking

1. Selecteer **Een nieuwe invoegtoepassing installeren** in LCS op de pagina **Finance** in de sectie **Power Platform-integratie**.
2. Blader naar de onderkant van de pagina en selecteer de invoegtoepassing **Belastingberekening** om deze te installeren.
3. Keer terug naar uw Finance-omgeving en probeer de belastingberekeningsservice te openen.

> [!NOTE]
> Controleer de [Vereisten van de belastingberekeningsservice](global-get-started-with-tax-calculation-service.md#prerequisites) voordat u de service Belastingberekening installeert.
> 
> Als u de invoegtoepassing niet kunt installeren om de sectie **Power Platform-integratie** niet beschilbaar is, gaat u naar [Overzicht invoegtoepassingen](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Neem contact op met uw systeembeheerder als de fout blijft optreden nadat u de invoegtoepassing hebt geïnstalleerd.
