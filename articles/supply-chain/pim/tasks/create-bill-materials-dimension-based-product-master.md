---
title: Een stuklijst maken voor een op dimensies gebaseerd productmodel
description: Voor deze procedure moet u de vorige 4 guides in deze reeks van acht registraties hebben voltooid.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f86625821f8a01a6d4949f9dca538a279f52ce9c
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565580"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a>Een stuklijst maken voor een op dimensies gebaseerd productmodel

[!include [banner](../../includes/banner.md)]

Voor deze procedure moet u de vorige 4 guides in deze reeks van acht registraties hebben voltooid. Met de eerste 4 registraties zijn gegevens ingesteld die nodig zijn om deze procedure te voltooien. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. Deze taak wordt doorgaans afgehandeld door de productontwerper.

## <a name="select-the-product"></a>Het product selecteren

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Markeer in de lijst de geselecteerde rij.
    * Zoek het vrijgegeven productmodel met op dimensies gebaseerde configuratietechnologie die u in de eerste taakbegeleider in deze reeks hebt gemaakt.  
1. Selecteer in het actievenster de optie **Technicus**.
1. Selecteer **Stuklijstversies**.

## <a name="create-new-bom-and-bom-version"></a>Een nieuwe stuklijst en stuklijstversie maken

1. Selecteer **Nieuw**.
1. Selecteer **Stuklijst en stuklijstversie**.
1. Typ een waarde in het veld **Naam**.
    * Een vestiging instellen  
    * In deze procedure wordt geen specifieke vestiging voor de stuklijst ingesteld.  
1. Selecteer **OK**.
1. Selecteer **Nieuw**.
    * In deze procedure worden vier regels aan de stuklijst toegevoegd. Twee regels staan voor kabelopties en twee regels staan voor behuizingsopties.  
1. Markeer in de lijst de geselecteerde rij.
1. Typ of selecteer een waarde in het veld **Artikelnummer**.
    * Selecteer artikelnummer A0001, HDMI 6' kabels.  
1. Typ of selecteer een waarde in het veld **Configuratiegroep**.
    * Selecteer de kabelconfiguratiegroep die is gemaakt in guide 4 in deze reeks.  
1. Selecteer **Nieuw**.
    * Selecteer artikelnummer A0002, HDMI 12' kabels.  
1. Markeer in de lijst de geselecteerde rij.
1. Typ of selecteer een waarde in het veld **Artikelnummer**.
1. Typ of selecteer een waarde in het veld **Configuratiegroep**.
    * Selecteer de kabelconfiguratiegroep opnieuw.  
1. Selecteer **Nieuw**.
1. Markeer in de lijst de geselecteerde rij.
1. Typ of selecteer een waarde in het veld **Artikelnummer**.
    * Selecteer artikelnummer D0002 behuizing  
1. Typ of selecteer een waarde in het veld **Configuratiegroep**.
    * Selecteer de behuizingsconfiguratiegroep voor deze stuklijstregel.  
1. Selecteer **Nieuw**.
1. Markeer in de lijst de geselecteerde rij.
1. Typ of selecteer een waarde in het veld **Artikelnummer**.
    * Selecteer artikelnummer M0007 standaardbehuizing als de laatste stuklijstregel.  
1. Typ of selecteer een waarde in het veld **Configuratiegroep**.
    * Selecteer de behuizingsconfiguratiegroep voor de laatste stuklijstregel.  

## <a name="approve-and-activate"></a>Goedkeuren en activeren

1. Sluit de pagina.
1. Selecteer **Goedkeuren**.
1. Typ of selecteer een waarde in het veld **Goedgekeurd door**.
1. Selecteer *Ja* in het veld **Wilt u ook de stuklijst goedkeuren?**
1. Selecteer **OK**.
1. Selecteer **Activeren**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]