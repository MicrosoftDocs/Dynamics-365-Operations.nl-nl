---
title: Fysieke voorraad in het magazijn overboeken
description: Deze procedure begeleidt u door het proces voor het maken en boeken van een voorraadoverboekingjournaal om verplaatsing van een artikel van een locatie in een magazijn naar een andere locatie te registreren.
author: MarkusFogelberg
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 540ba2266ea74c36babce57670f84159c89018f1
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383414"
---
# <a name="transfer-physical-inventory-within-the-warehouse"></a>Fysieke voorraad in het magazijn overboeken

[!include [banner](../../includes/banner.md)]

Deze procedure begeleidt u door het proces voor het maken en boeken van een voorraadoverboekingjournaal om verplaatsing van een artikel van een locatie in een magazijn naar een andere locatie te registreren. U moet een voorraadjournaalnaam hebben ingesteld voor voorraadoverboekingen voordat u hiermee start. U kunt deze procedure doorlopen in het demobedrijf USMF met de voorbeeldwaarden die worden weergegeven, of u kunt uw eigen gegevens gebruiken als u producten en locaties hebt ingesteld. Deze taken worden normaal gesproken uitgevoerd door een magazijnmedewerker.


## <a name="create-an-inventory-transfer-journal"></a>Een voorraadoverboekingsjournaal maken
1. Ga in het **navigatievenster** naar **Voorraadbeheer > Journaalboekingen > Artikelen > Overboeken**.
2. Klik op **Nieuw**.
3. Typ of selecteer een waarde in het veld **Naam**.
4. Klik op **OK**. Er is de optie om 'Van' en 'Naar' dimensies voor elke journaalregel op te geven. Deze zijn essentieel voor dit journaaltype. U kunt artikelen overboeken naar locaties met verschillende regels. In dit voorbeeld boeken we een artikel over in hetzelfde magazijn, van een locatie waar nummerplaten worden gecontroleerd naar een locatie waar nummerplaten niet worden gecontroleerd.   

## <a name="create-journal-lines"></a>Journaalregels maken
1. Klik op het sneltabblad **Journaalregels** op **Nieuw**.
2. Typ of selecteer een waarde in het veld **Artikelnummer**. Als u USMF gebruikt, kunt u 'A0001' selecteren.  
3. Typ of selecteer een waarde in het veld **Van vestiging**. Als u USMF gebruikt, kunt u '2' selecteren.  
4. Typ of selecteer een waarde in het veld **Naar vestiging**. Als u USMF gebruikt, kunt u '2' selecteren.  
5. Typ of selecteer een waarde in het veld **Van magazijn**. Als u USMF gebruikt, kunt u '24' selecteren.  
6. Typ of selecteer een waarde in het veld **Naar magazijn**. Als u USMF gebruikt, kunt u '24' selecteren.  
7. Typ of selecteer een waarde in het veld **Van locatie**. Als u USMF gebruikt, kunt u 'FL-001' selecteren.  
8. Typ of selecteer een waarde in het veld **Naar locatie**. Als u USMF gebruikt, kunt u 'BULK-001' selecteren.  
9. Voer een getal in het veld **Hoeveelheid** in.
10. Klik op het sneltabblad **Regeldetails** op het tabblad **Voorraaddimensies**.
11. Typ of selecteer een waarde in **Van voorraaddimensies** in het veld **Nummerplaat**. Als u USMF gebruikt, kunt u '24' selecteren.  
12. Klik op **Opslaan**.

## <a name="post-the-inventory-transfer-journal"></a>Het voorraadoverboekingsjournaal boeken
1. Klik in het **actievenster** op **Boeken**.
2. Klik op **OK**.

## <a name="view-inventory-transactions"></a>Voorraadtransacties weergeven
1. Klik op **Voorraad**.
2. Klik op **Transacties**. Hier ziet u de transacties die werden gemaakt toen u uw journaal boekte.  

