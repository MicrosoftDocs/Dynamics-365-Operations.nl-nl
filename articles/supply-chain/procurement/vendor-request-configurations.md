---
title: Configuraties leverancieraanvraag
description: In dit onderwerp worden de velden beschreven die moeten worden ingevuld in een nieuwe leverancieraanvraag.
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: AX 7.3
ms.translationtype: HT
ms.sourcegitcommit: 0ca19ab9ed7a52328c5dd5252c418bb9343bdc2b
ms.openlocfilehash: e45f8698e69a2a870c7c00f91622216deb4cb38a
ms.contentlocale: nl-nl
ms.lasthandoff: 12/14/2017

---

# <a name="vendor-request-configurations"></a>Configuraties leverancieraanvraag
[!include[banner](../includes/banner.md)]

Om een leverancieraanvraag te voltooien, moet de contactpersoon van de leverancier de wizard voor registratie van een potentiële leverancier uitvoeren.

In het formulier **Configuraties leverancieraanvraag** kunt u profielen maken waarmee verplichte en zichtbare velden in de wizard voor registratie van een potentiële leverancier worden opgegeven.

In de wizard voor leveranciersregistratie wordt eerst gevraagd in welk land of welke regio de gebruiker van de potentiële leverancier actief is. Deze gegevens bepalen de toepasselijke configuratie. Als er geen specifieke configuratie voor een land/regio wordt gedefinieerd, wordt een standaardconfiguratie gebruikt.

### <a name="set-up-a-vendor-request-configuration"></a>Een configuratie voor leverancieraanvragen instellen

Standaard is er een leveranciersconfiguratie beschikbaar in het formulier Configuraties leverancieraanvraag.

Het is niet mogelijk om landen/regio's voor de standaardconfiguratie te selecteren, dus het gedeelte **Landen/regio's** kan niet worden gewijzigd.

1.  Klik op **Inkoopbeheer** > **Instelling** > **Leveranciers** en **Configuraties leverancieraanvraag**.
2.  Klik op het tabblad **Velden** om de status van de weergegeven velden in te stellen.
-   Verborgen (niet zichtbaar)
-   Weergegeven (zichtbaar, maar niet verplicht)
-   Vereist (zichtbaar en verplicht)
3.  Klik op het tabblad **Inhoud** om op te geven of er tekst moeten worden weergegeven in de wizard en of de gebruiker van de potentiële leverancier iets moet accepteren voordat deze naar de volgende stap in de wizard gaat. De bevestiging wordt gevraagd voor alle voorwaarden die de gebruiker moet accepteren om door te gaan.

U kunt ook een bevestigingsbericht opgeven dat wordt weergegeven zodra de wizard is voltooid en u kunt een of meer vragenlijsten toevoegen.

### <a name="create-a-vendor-configuration-for-a-specific-countryregion"></a>Een leveranciersconfiguratie maken voor een bepaald land of een bepaalde regio
1.  Klik op **Inkoopbeheer** > **Instelling** > **Leveranciers** en **Configuraties leverancieraanvraag**.
2.  Klik op **Nieuw** om een nieuwe configuratie te maken en geef een naam op voor de configuratie.
3.  Klik op **Opslaan**.
4.  Open het tabblad **Land/regio's** om het land of de regio te selecteren waarvoor de configuratie moet worden gebruikt.
5.  Voltooi de configuratie door de richtlijnen voor de standaardconfiguratie te volgen.


