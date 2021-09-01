---
title: Aanschaf van vaste activa voorstellen
description: In dit onderwerp wordt beschreven hoe u een vast activum bijboekt met het verwervingsvoorstel in het vaste-activajournaal.
author: saraschi2
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 99202763ae32d02f94f1590783727d4f2cf7a7bbe45963d0e175bfc449b134d9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742924"
---
# <a name="propose-fixed-asset-acquisitions"></a>Aanschaf van vaste activa voorstellen

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een vast activum bijboekt met het verwervingsvoorstel in het vaste-activajournaal. Het gebruikt de rol Accountant en demogegevens voor de USMF-rechtspersoon. Als u een vast activum via een voorsteljournaal voor vaste activa wilt verkrijgen, moet u eerst de record voor de vaste activa maken en vervolgens de aanschafprijs definiëren in het activaboek.

## <a name="create-an-asset-acquisition-proposal"></a>Een voorstel voor het verwerven van activa maken

Voer de volgende stappen uit om een voorstel voor het verwerven van activa te maken. 

1. Ga in het navigatievenster naar **Modules > Vaste activa > Journaalboekingen > Vaste-activajournaal**.
2. Selecteer **Nieuw**.
3. Typ of selecteer een waarde in het veld **Naam**.
4. Selecteer **Regels** in het actievenster.
5. Selecteer **Voorstellen**.
6. Selecteer **Verwervingsvoorstel**.
7. Selecteer **Filter**. Selecteer **Opnieuw instellen** om eerdere waarden te wissen.
8. Selecteer de rij **Vaste-activanummer**.
9. Typ of selecteer een waarde in het veld **Criteria**. Stel de resterende criteria in voor de vaste activa die u met dit voorstel wilt bijboeken.  
10. Selecteer tweemaal **OK** om het deelvenster af te sluiten.
- Controleer of de transactieregels worden gemaakt.  
- Alleen vaste activa waarvoor de verwervingsdatum en -prijs zijn ingesteld in het boek worden in het verwervingsvoorstel opgenomen.  
11. Selecteer op de pagina het tabblad **Boeken**.
12. Selecteer **Boeken**.

## <a name="include-default-financial-dimensions-in-an-acquisition-proposal"></a>Financiële standaarddimensies opnemen in een overnamevoorstel

De verwervingstransactie kan worden gemaakt met Excel-invoegtoepassingen door naar **Vaste activa > Journaalposten > Vaste-activajournaal** te gaan. Maak een nieuw journaal en ga naar de sectie **Regels** op de pagina en selecteer het Excel-pictogram en vervolgens een journaalregel voor vaste activa. Er wordt een Excel-sjabloon voor journaalregels gemaakt en geopend. U kunt gegevens toevoegen voor de journaalregels die u aan de sjabloon toevoegt en deze gegevens vervolgens weer in het systeem publiceren. 

Als er standaarddimensies zijn ingesteld voor het geselecteerde activaboek en de bijbehorende vaste activa die zijn ingevoerd in de Excel-sjabloon, worden de financiële standaarddimensies aangeroepen vanuit de hoofdgegevens van het activaboek wanneer het journaal vanuit Excel naar het systeem wordt gepubliceerd. Als u automatisch financiële dimensies in een activaboek wilt opnemen tijdens het publiceren van het vaste-activajournaal vanuit de Excel-invoegtoepassing, moeten de standaarddimensies van tevoren zijn ingesteld.  


[!INCLUDE [footer-include](../../../includes/footer-banner.md)]
