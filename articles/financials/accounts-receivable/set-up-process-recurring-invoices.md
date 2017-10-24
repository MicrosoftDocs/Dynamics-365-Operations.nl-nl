---
title: Terugkerende facturen instellen en verwerken
description: In dit artikel wordt beschreven hoe u terugkerende facturen instelt en verwerkt. U kunt terugkerende facturen gebruiken als u klanten regelmatig voor hetzelfde bedrag moet factureren.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustInvoiceTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14011
ms.assetid: 9cc37003-adf1-413d-b2b2-2badcf512e3b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5f095b74df8b680f6e7e54520f9684298ec51aad
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-and-process-recurring-invoices"></a>Terugkerende facturen instellen en verwerken

[!include[banner](../includes/banner.md)]


In dit artikel wordt beschreven hoe u terugkerende facturen instelt en verwerkt. U kunt terugkerende facturen gebruiken als u klanten regelmatig voor hetzelfde bedrag moet factureren.

<a name="create-a-recurring-free-text-invoice-template"></a>Een sjabloon maken voor een terugkerende vrije-tekstfactuur
---------------------------------------------

Als u klanten voor dezelfde services periodiek wilt factureren, moet u een sjabloon voor vrije-tekstfacturen definiëren die kan worden hergebruikt om de facturen te maken. Deze sjabloon bevat de volgende gegevens:

-   Koptekstgegevens, zoals belastinggroepen, betalingsvoorwaarden en de betalingsmethode
-   Regelgegevens, zoals serviceomschrijving, opbrengstenrekeningen, eenheidsprijs en factuurbedrag
-   Toeslagen voor verpakken en verzenden
-   Boekhoudingsverdelingen samen met gegevens over financiële dimensies, zoals kostencentra en bedrijfseenheden

In feite maakt u een volledige factuur en slaat u deze als een sjabloon op. U kunt de sjablonen instellen met de pagina **Terugkerende facturen**.

## <a name="assign-a-free-text-invoice-template-to-a-customer-and-enter-recurrence-details"></a>Een sjabloon voor een vrije-tekstfactuur toewijzen aan een klant en terugkeergegevens invoeren
Nadat de sjabloon is gemaakt, moet u de sjabloon aan de klanten toewijzen die u wilt factureren. Bovendien moet u opgeven wanneer en hoe vaak de factuur wordt gebruikt. U kunt de sjablonen op het tabblad **Factuur** van de pagina **Klanten** toewijzen. Voeg de sjabloon aan de lijst toe en werk de volgende gegevens bij:

-   De begindatum en desgewenst de einddatum voor de terugkerende facturering.
-   De frequentie van de terugkerende facturering (bijvoorbeeld elke dag of eens per maand)
-   Het maximale factureringsbedrag (als deze gegevens vereist zijn)

Een klant kan meerdere sjablonen hebben die verschillende frequenties hebben.

## <a name="generate-the-recurring-invoices"></a>De terugkerende facturen genereren
De pagina **Terugkerende facturen** bevat een taak waarmee sjablonen voor terugkerende facturen worden verwerkt. U geeft de factuurdatum en de sjabloon op op basis waarvan u de facturen wilt genereren. Facturen worden gegenereerd en worden als één herhalings-ID toegewezen voor elke groep facturen die wordt verwerkt.
Terugkerende vrije-tekstfacturen boeken
---------------------------------

Nadat terugkerende facturen zijn gegenereerd, wordt de factuurherhalings-ID weergegeven in een boekingstaak op de pagina **Terugkerende facturen**. U kunt alle facturen voor een herhalings-ID weergeven door op de koppeling te klikken. Tijdens de controle van de facturen voor de herhalings-ID kunt u afzonderlijke facturen verwijderen. De herhalingsinstellingen van de klant worden voor die sjabloon opnieuw ingesteld, zodat deze later opnieuw kan worden gegenereerd. U kunt één factuur, een groot aantal facturen of alle facturen voor een herhalings-ID boeken. Als workflows worden ingeschakeld, moet u klikken op **Verzenden** voordat u de facturen kunt boeken.
Terugkerende vrije-tekstfacturen afdrukken
----------------------------------

Nadat terugkerende facturen zijn geboekt, kunt u de facturen op de pagina met de lijst vrije-tekstfacturen afdrukken. U kunt de geselecteerde facturen afdrukken of u kunt een bereik facturen selecteren die u wilt afdrukken.




