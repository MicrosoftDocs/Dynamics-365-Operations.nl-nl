---
title: Leases beheren via het raamwerk voor het importeren van leases
description: In dit onderwerp wordt uitgelegd hoe u het raamwerk voor het importeren van leases kunt gebruiken om meerdere leases tegelijk aan te passen.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7df2f55f596cab54315c2da2ec0492422514f49c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971298"
---
# <a name="manage-leases-through-the-lease-import-framework"></a>Leases beheren via het raamwerk voor het importeren van leases

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u het raamwerk voor het importeren van leases kunt gebruiken om meerdere leases in één stap aan te passen. Als u deze functie gebruikt, kunt u tijd besparen en kunt u nauwkeurige correcties garanderen door de kans op een menselijke fout te verlagen. Bovendien kan deze mogelijkheid Microsoft Dynamics 365 Finance met externe gegevensentiteiten verbinden om gegevens efficiënt te uploaden.

De volgende gegevensentiteiten kunnen worden gebruikt om activa-leasing met externe systemen te integreren:

- Fasering van lease
- Fasering van betalingscontract
- Fasering van contract voor bijkomende kosten weergeven

U kunt het importproces gebruiken om een lease aan te passen, niet-financiële informatie bij te werken of nieuwe leases toe te voegen. U kunt de leasinggegevens weergeven en bewerken voordat u deze importeert.

Het systeem kan de volgende drie processen uitvoeren via de suite voor het importeren van leases.

| Procestype  | Beschrijving |
|---------------|-------------|
| Record toevoegen    | Gemigreerde leases die dit procestype hebben, maken een lease in het systeem. Het betalingsschema moet handmatig worden bevestigd en de journaalpost voor de eerste toerekening moet na de migratie handmatig worden geboekt. |
| Record bijwerken | Gemigreerde leases die dit veld voor het bijwerken van het procestype hebben, zijn van belang voor een lease die al in het systeem aanwezig is. Alleen de velden die zijn geselecteerd op de pagina **Selectie velden bijwerken** worden bijgewerkt. We raden u aan om niet-financiële velden te selecteren op de pagina **Selectie velden bijwerken**, omdat de lease niet wordt aangepast door dit procestype. |
| Record aanpassen | Gemigreerde leases die dit procestype hebben, passen de lease aan. Deze correctie veroorzaakt een financiële lease-wijziging van de lease. Nadat de lease is verwerkt, maakt het systeem een nieuw betalingsschema door de nieuwe gegevens uit de suite voor het importeren van leases te gebruiken. Het systeem bevestigt het betalingsschema of boekt de correctiejournaalpost niet. |

Nadat de gegevens zijn geüpload via het werkgebied **Gegevensbeheer**, opent u de pagina **Importheader** (**Asset-leasing \> Raamwerk voor het importeren van leases \> Importheader**). Op deze pagina worden alle imports weergegeven van de drie gegevensentiteiten die eerder zijn vermeld.

Als u de leasefaseringsgegevens wilt weergeven voordat de verwerking wordt uitgevoerd, selecteert u **Faseringsgegevens**.

Met de functie vergelijken kunt u een record die u importeert vergelijken met de corresponderende record die al in uw systeem staat. Als u een afzonderlijke leaserecord wilt vergelijken, selecteert u een lease en vervolgens **Vergelijken**. U moet deze stap uitvoeren om een rapport **Verschillen** te genereren voordat u de leaserecords migreert. Met de functionaliteit Vergelijken worden de waarden in de faseringsgegevens vergeleken met de waarden voor leases die zich momenteel in het systeem bevinden.

> [!NOTE]
> De functionaliteit Vergelijken werkt niet voor leases die het procestype **Record toevoegen** hebben, omdat er niets met die lease kan worden vergeleken.
>
> Als u meerdere leases tegelijk wilt vergelijken, gaat u naar **Activa leasen \> Raamwerk voor het importeren van leases \> Periodiek \> Vergelijken** en selecteert u **Vergelijken**.

Voor elke entiteit kunt u de verschillen weergeven tussen wat zich momenteel in het systeem bevindt en wat zich in de faseringstabellen bevindt. Selecteer voor elke entiteit in de faseringstabellen **Verschillen bekijken**. In het dialoogvenster dat verschijnt, worden de huidige waarde en de voorgestelde faseringswaarde weergegeven.

U kunt de faseringswaarde ook bijwerken door deze te wijzigen in de kolom **Nieuwe waarde** en vervolgens **Fasering bijwerken** te selecteren.

U kunt leases valideren om ervoor te zorgen dat de records in het systeem kunnen worden gebracht zonder dat er fouten worden geïntroduceerd. Voordat een leaserecord wordt gemigreerd, voert het systeem diverse validaties uit om ervoor te zorgen dat de record met succes kan worden geïmporteerd. Selecteer **Valideren** om een individuele lease te valideren.

> [!NOTE]
> Als u meerdere leases tegelijk wilt valideren, gaat u naar **Activa leasen \> Raamwerk voor het importeren van leases \> Periodiek \> Valideren** en selecteert u **Vergelijken**.

Als u een afzonderlijke lease wilt verwerken, selecteert u **Leaserecords migreren** op de pagina **Importheader**. Wanneer een lease wordt gemigreerd, voert het systeem de actie uit die is opgegeven in het veld **Procestype**.

> [!NOTE]
> Als u meerdere leases tegelijk wilt valideren, gaat u naar **Activa leasen \> Raamwerk voor het importeren van leases \> Periodiek \> Valideren** en selecteert u **Vergelijken**.

Nadat de leases zijn vergeleken, kunt u een rapport uitvoeren om de verschillen weer te geven voor elke lease die is opgenomen in de import-id. Als u het rapport wilt uitvoeren voor één lease, selecteert u die lease in de faseringsgegevens en vervolgens selecteert u **Vergelijken en rapport weergeven \> Verschillenrapport**.

> [!NOTE]
> Als u meerdere leases tegelijk wilt valideren, gaat u naar **Activa leasen \> Query's en rapporten \> Verschillenrapport** en selecteert u **Vergelijken**.

## <a name="set-up-update-fields"></a>Bijwerkvelden instellen

Als u het lease-importraamwerk gebruikt om leases bij te werken en het procestype **Record bijwerken** is, kunt u specifieke velden selecteren die u wilt bijwerken.

1. Ga naar **Activa leasen \> Raamwerk voor het importeren van leases \> Instellen \> Selectie veld bijwerken**.
2. Selecteer op de pagina die wordt weergegeven de velden die moeten worden bijgewerkt en selecteer vervolgens de groene pijl om deze naar de lijst **Geselecteerde velden** te verplaatsen. Alleen velden in de lijst **Geselecteerde velden** kunnen worden bijgewerkt met de lease-import suite.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]