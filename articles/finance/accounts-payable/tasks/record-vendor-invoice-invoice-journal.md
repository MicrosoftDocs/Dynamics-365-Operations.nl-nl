---
title: Een leveranciersfactuur in het factuurjournaal registreren
description: Deze taakbegeleiding toont hoe leveranciersfacturen moeten worden geregistreerd die niet aan inkooporders zijn gekoppeld.
author: abruer
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 27d0e81ca37c9a59adc3acce3610fd17fd954a8b
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/05/2022
ms.locfileid: "8716636"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a>Een leveranciersfactuur in het factuurjournaal registreren

[!include [banner](../../includes/banner.md)]

Deze taakbegeleiding toont hoe leveranciersfacturen moeten worden geregistreerd die niet aan inkooporders zijn gekoppeld. Voorbeelden van dit type factuur zijn onkosten voor levering of services.  Bij deze registratie wordt het demobedrijf USMF gebruikt.

1. Ga naar **Navigatievenster > Modules > Leveranciers > Werkgebieden > Leveranciersfactuurregistratie**.
2. Klik in het **actievenster** op **Nieuw factuurjournaal**.
3. Klik op **Nieuw**.
4. Voer in het veld **Naam** de journaalnaam in of klik op de vervolgkeuzeknop om de zoekopdracht te openen.
5. Typ een waarde in het veld **Beschrijving**.
6. Klik in het **actievenster** op **Regels**. Voer in het veld **Datum** de boekingsdatum in waarmee Grootboek wordt bijgewerkt.  
7. Geef in het veld **Rekening** de **Leveranciersrekening** op.
8. Voer in het veld **Factuur** het factuurnummer in.
9. Typ een waarde in het veld **Beschrijving**.
10. Voer in het veld **Krediet** een numerieke waarde in.
11. Voer in het veld **Tegenrekening** het rekeningnummer in of klik op de vervolgkeuzeknop om de zoekopdracht te openen
    * De **btw-groep** wordt standaard uit de leveranciersrekening opgehaald.  
    * De **Btw-groep van het artikel** wordt standaard opgehaald uit de hoofdrekening die is opgegeven in het veld **Tegenrekening**.  
    * De **Vervaldatum** wordt berekend aan de hand van de betalingsvoorwaarden.  
    * De **Contantkorting** is afkomstig van de leveranciersrekening.
12. Als u workflow voor Journaalwerkstroom voor leveranciersfacturen hebt ingeschakeld, klikt u op **Werkstroom > Indienen**.
    * Wanneer de inzending is goedgekeurd, wordt de datum vervroegd tot de eerste dag van de volgende open periode, als de transactieboekingsdatum binnen een periode valt met de status In wachtstand of Gesloten voor boekingen in het grootboek.
12. Klik op **Boeken**.
13. Sluit de pagina.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
