---
title: Restbedrag vereffenen
description: U kunt het resterende bedrag van de vereffeningsactiviteit vereffenen door het toe te passen op een grootboekrekening.
author: mikefalkner
ms.date: 10/16/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 8c865b4b0481b7753588ef17bc0250bab2b6c191
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834910"
---
# <a name="settle-remainder"></a>Restbedrag vereffenen

[!include [banner](../includes/banner.md)]

U kunt het resterende bedrag van de vereffeningsactiviteit vereffenen door het toe te passen op een grootboekrekening of een andere klant. U kunt de rest vereffenen wanneer u bedragen vereffent die zijn ingevoerd in een journaal of wanneer u alleen openstaande transacties vereffent.

## <a name="setting-up-defaults"></a>Standaardinstellingen opgeven 
U moet de functie Restbedrag vereffenen inschakelen en de standaardinstellingen instellen voordat u Restbedrag vereffenen gebruikt

1)  Klik op **Klanten   > Parameters > Vereffeningen** of **Leveranciers > Parameters > Vereffeningen**
2)  Selecteer het tabblad **Vereffening** en klik op **Restbedrag vereffenen inschakelen**
3)  Selecteer bij **Standaardredencode** een standaardredencode. De redencodes moeten al zijn ingesteld in **Klanten > Instellingen > Redencodes voor afschrijvingen van klant** of **Leveranciers > Instellingen > Redencodes voor afschrijvingen van klant**. Bij **Standaardrekening voor restbedrag vereffenen** wordt standaard de rekening ingesteld die is toegewezen aan de redencode voor afschrijving.
3)  Werk de waarde voor **Standaardrekening voor restbedrag vereffenen** zo nodig bij.
4)  Selecteer bij **Standaardjournaalnaam** een betalingsjournaal dat wordt gebruikt als u een betalingsjournaal wilt maken wanneer u alleen openstaande transacties vereffent. Als u de functie Restbedrag vereffenen inschakelt, moet u een standaardjournaalnaam toevoegen.

## <a name="settle-remainder-from-a-journal"></a>Restbedrag uit een journaal vereffenen
Als u de functie **Restbedrag vereffenen** niet inschakelt, kunt u nog steeds een transactie invoeren in een journaal en vervolgens transacties hiervoor vereffenen, net als in het verleden. Wanneer u op de knop **OK** klikt, wordt het openstaande saldo op de factuur verminderd met het contante bedrag. Als de factuur niet volledig wordt vereffend met het contante bedrag, blijft de factuur openstaan met een resterend bedrag dat op een later tijdstip moet worden vereffend.

Wanneer de functie **Restbedrag vereffenen** is ingeschakeld, kunt u het restbedrag vereffenen naar een grootboekrekening. U kunt ook de rest overboeken naar een andere klantrekening (voor klanttransacties) of een andere leverancier (voor leverancierstransacties) in plaats van de facturen open te laten. 

Ga als volgt te werk om de rest te vereffenen via de pagina **Vereffening**:

1)  Markeer op de pagina **Vereffening** de facturen of transacties die u wilt vereffenen.
2)  Klik op de knop **Restbedrag vereffenen**.
3)  Er wordt een dialoogvenster weergegeven met het bedrag dat wordt vereffend met een grootboekrekening, de datum die wordt gebruikt voor het vereffenen van het restbedrag, de standaardredencode uit de parameters en de standaardrekening uit de parameters. 
4)  Selecteer een nieuwe vereffeningsreden als u de standaardreden wilt wijzigen. De vereffeningsrekening wordt gewijzigd in de rekening die is gekoppeld aan de redencode.
5)  Bewerk de vereffeningsrekening als u deze wilt wijzigen.
6)  Als u bij het vereffenen van klanttransacties het restbedrag wilt verplaatsen naar een andere klant, selecteert u een klant bij **Restbedrag vereffenen met klantrekening**. Als u bij het vereffenen van leverancierstransacties het restbedrag wilt verplaatsen naar een andere leverancier, selecteert u een leverancier bij **Restbedrag vereffenen met leveranciersrekening**.
6)  Klik op **Restbedrag vereffenen**.
7)  De pagina **Journaal** wordt weergegeven. Er wordt een extra regel aan het journaal toegevoegd met het resterende vereffeningsbedrag als het bedrag en met de rekening voor het restbedrag als tegenrekening. Als u een klant of leverancier hebt toegevoegd zodat u het vereffeningsbedrag naar een andere klant of leverancier kunt verplaatsen, wordt een extra regel toegevoegd aan het journaal om het vereffeningsbedrag naar die klant of leverancier te verplaatsen.

Wanneer u het journaal boekt, wordt de openstaande transactie volledig vereffend. 

## <a name="settle-remainder-when-you-are-only-settling-open-transactions"></a>Restant vereffenen wanneer u alleen openstaande transacties vereffent
U kunt het restant ook vereffenen wanneer u openstaande transacties zonder een journaal vereffent.

Ga als volgt te werk om het restant te vereffenen:

1)  Markeer op de pagina **Vereffening** de facturen of transacties die u wilt vereffenen
2)  Klik op **Restbedrag vereffenen**
3)  Er wordt een dialoogvenster weergegeven met het bedrag dat wordt vereffend met een grootboekrekening, de datum die wordt gebruikt voor het vereffenen van het restbedrag, de standaardredencode uit de parameters en de standaardrekening uit de parameters. 
4)  Selecteer een nieuwe vereffeningsreden als u de standaardreden wilt wijzigen. De vereffeningsrekening wordt gewijzigd in de rekening die is gekoppeld aan de redencode.
5)  Bewerk de **vereffeningsrekening** als u deze wilt wijzigen.
6)  Als u bij het vereffenen van klanttransacties het restbedrag wilt verplaatsen naar een andere klant, selecteert u een klant bij **Restbedrag vereffenen met klantrekening**. Als u bij het vereffenen van leverancierstransacties het restbedrag wilt verplaatsen naar een andere leverancier, selecteert u een leverancier bij **Restbedrag vereffenen met leveranciersrekening**
7)  U kunt er ook voor kiezen een betalingsjournaal met het restbedrag van de vereffening te maken of dit alleen zonder een journaal boeken. Selecteer **Ja** voor **Bewerken in journaal** om een betalingsjournaal te maken. U kunt het door u gemaakte betalingsjournaal bewerken.
8)  Klik op **Restbedrag vereffenen**. Als u ervoor hebt gekozen een journaal te maken, wordt de knop gewijzigd in **Journaal maken**. Klik in dat geval op **Journaal maken**.
9)  Als u een betalingsjournaal hebt gemaakt, wordt de journaalpagina geopend als u op **Restbedrag vereffenen** klikt. Er wordt een regel aan het journaal toegevoegd met het resterende vereffeningsbedrag als het bedrag en met de rekening voor het restbedrag als tegenrekening. Als u een klant of leverancier hebt toegevoegd zodat u het vereffeningsbedrag naar een andere klant of leverancier kunt verplaatsen, wordt een extra regel toegevoegd aan het journaal om het vereffeningsbedrag naar die klant of leverancier te verplaatsen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]