---
title: Bestandsindelingen voor betalingsmethoden
description: In dit onderwerp worden de twee methoden beschreven voor het verkrijgen van bestandsindelingen die u voor betalingsmethoden kunt gebruiken.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPaymMode, VendPaymMode
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 262514
ms.search.region: Belgium, France, Germany, Norway, Spain, Sweden, Switzerland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: f6f9e94f7bf590a82d022affb8bc4a3bea5ab56c
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="file-formats-for-methods-of-payment"></a>Bestandsindelingen voor betalingsmethoden

[!include[banner](../includes/banner.md)]


In dit onderwerp worden de twee methoden beschreven voor het verkrijgen van bestandsindelingen die u voor betalingsmethoden kunt gebruiken.

Er zijn twee methoden waarmee u bestandsindelingen kunt verkrijgen voor gebruik bij betalingsmethoden, ER-bestandsindelingen (elektronische rapportage) of X ++-bestandsindelingen. Wanneer u een betalingsmethode voor een klant of leverancier instelt, geeft u aan welke bestandsindelingen en standaarden moeten worden gebruikt voor betalingen en hoe betalingen worden verwerkt. U kunt de volgende typen indelingen selecteren:

-   Exporteren
-   Importeren
-   Retour
-   Remise

### <a name="method-1-electronic-reporting-file-formats"></a>Methode 1: bestandsindelingen elektronische rapportage

Voor bestandsindelingen die zijn gebaseerd op ER-configuraties, moet u de configuraties van Lifecycle Services (LCS) importeren. Zie voor meer informatie [Elektronische rapportageconfiguraties downloaden vanuit Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md). Nadat u configuraties voor rapportage hebt geïmporteerd voor deze bestandsindelingen, zijn de geïmporteerde indelingen beschikbaar om te selecteren op de pagina **Betalingsmethoden**. Het proces voor het importeren en selecteren van bestandsindelingen voor Europa is vergelijkbaar met de procedure voor Japan. Zie [JBA-betalingsbestandsindeling inschakelen](tasks/jba-payment-file-format.md) voor meer informatie

### <a name="method-2-x-file-formats"></a>Methode 2: X++-bestandsindelingen

Als u de bestandsindelingen die zijn gebaseerd op X++-code wilt selecteren, moet u de volgende stappen uitvoeren.

1.  Ga naar de pagina **Betalingsmethoden**.
2.  Klik op het sneltabblad **Bestandsindelingen** op **Instellen**.
3.  Selecteer het tabblad dat overeenkomt met het type bestandsindeling.
4.  Selecteer een bestandsindeling in de lijst **Beschikbaar** en verplaats deze naar de lijst **Geselecteerd** met het pijlbesturingselement.
5.  Sluit de pagina **Bestandsindelingen voor betalingsmethoden**.
6.  Selecteer op het sneltabblad **Bestandsindelingen** de bestandsindeling voor de betalingsmethode in het juiste veld met bestandsindelingen. De algemene opties voor elektronische aangifte moeten worden ingesteld op **Nee** voor X ++-bestandsindelingen.





