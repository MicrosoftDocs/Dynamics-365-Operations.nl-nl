---
title: Bestandsindelingen voor betalingsmethoden
description: Dit onderwerp beschrijft de twee methoden voor het verkrijgen van de bestandsindelingen die u voor betalingsmethoden gebruiken kunt.
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustPaymMode, VendPaymMode
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 262514
ms.assetid: 72ea2018-5a49-419c-93d0-755e5ff2722f
ms.search.region: Belgium, France, Germany, Norway, Spain, Sweden, Switzerland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 54af22f1f2ec779bf947ae584a3ae09c20e6a364
ms.lasthandoff: 03/31/2017


---

# <a name="file-formats-for-methods-of-payment"></a>Bestandsindelingen voor betalingsmethoden

Dit onderwerp beschrijft de twee methoden voor het verkrijgen van de bestandsindelingen die u voor betalingsmethoden gebruiken kunt.

Er zijn twee methoden waarmee u kunt u bestandsindelingen voor gebruik met betalingsmethoden, elektronische rapportage (ER)-bestandsindelingen of X ++-bestandsindelingen. Wanneer u een betalingsmethode voor een klant of leverancier instelt, moet u aangeven welke bestandsindelingen en normen moeten worden gebruikt voor betalingen en de manier waarop de betalingen worden verwerkt. U kunt de volgende typen indelingen selecteren:

-   Exporteren
-   Importeren
-   Retour
-   Remise

### <a name="method-1-electronic-reporting-file-formats"></a>Methode 1: Indelingen voor elektronische aangifte

Voor de bestandsindelingen die zijn gebaseerd op Emergency Recovery-configuraties, moet u de configuraties van Lifecycle Services (LCS) importeren. Zie voor meer informatie [elektronische downloaden rapportage configuraties vanuit Lifecycle Services](/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs). Nadat u configuraties voor rapportage geïmporteerd voor de bestandsindelingen, de geïmporteerde indelingen zijn beschikbaar om te selecteren in de **betalingsmethoden** pagina. Het proces voor het importeren en het selecteren van bestandsindelingen voor europa is vergelijkbaar met de procedure voor Japan. <!---For more details, see [Enable the JBA payment file format](https://ax.help.dynamics.com/en/wiki/enable-the-jba-payment-file-format/).-->

### <a name="method-2-x-file-formats"></a>Methode 2: X ++ bestandsindelingen

Als u de bestandsindelingen die zijn gebaseerd op de X ++-code, moet u de volgende stappen uitvoeren.

1.  Ga naar de **betalingsmethoden** pagina.
2.  Op de **bestandsindelingen** sneltabblad, klikt u op **Setup**.
3.  Selecteer het tabblad dat overeenkomt met de bestandsindeling.
4.  Selecteer een bestandsindeling van de **beschikbaar** lijst en verplaats deze naar de **geselecteerd** lijst met het besturingselement pijl.
5.  Sluit de **bestandsindelingen voor betalingsmethoden** pagina.
6.  Op de **bestandsindelingen** sneltabblad, selecteer de bestandsindeling voor de betalingsmethode van het juiste bestand indelingsveld moet worden gebruikt. De algemene opties voor elektronische aangifte moeten worden ingesteld op **Nee** voor X ++-bestandsindelingen.



