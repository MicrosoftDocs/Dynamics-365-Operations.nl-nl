---
title: Veelgestelde vragen over verkooporders
description: Deze pagina behandelt vaak gestelde vragen die naar boven komen bij het werken met verkooporders in Dynamics 365 Supply Chain Management.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d75022dcc476052040b16c9033cf5ff2a697ae6c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476003"
---
# <a name="sales-order-faqs"></a>Veelgestelde vragen over verkooporders

Deze pagina behandelt vaak gestelde vragen die naar boven komen bij het werken met verkooporders in Dynamics 365 Supply Chain Management.

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a>Kan ik een inkooporder aan een verkooporder koppelen om aan de vraag te voldoen?

U kunt een inkooporder maken op basis van een verkooporder. Meer informatie vindt u in [Een inkooporder maken op basis van een verkooporder](/dynamics365/supply-chain/sales-marketing/tasks/create-purchase-order-sales-order).

## <a name="can-i-cancel-or-delete-a-sales-order-or-return-order"></a>Kan ik een retourorder of een verkooporder annuleren of verwijderen?

U kunt alleen verkooporders en retourorders annuleren die de status *Gemaakt* hebben. Zie voor meer informatie [Een retourorder annuleren](/dynamics365/supply-chain/service-management/cancel-return-order).

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a>Kan ik een gefactureerde verkooporder terugzetten als die is verwijderd?

Als een gefactureerde verkooporder per ongeluk verwijderd is kan u deze herstellen of de details weergeven.

Ga naar **Klantrekening \>Transacties \> Origineel document \> Details weergeven**. Zoek de factuur waarnaar u op zoek bent en selecteer deze om de details weer te geven. Deze gegevens omvatten de verkooporderverwijzing. Op die pagina hebt u ook toegang tot de verkoopordergegevens.

## <a name="how-do-i-delete-orphaned-sales-order-records"></a>Hoe kan ik zwevende verkooporderrecords verwijderen?

Als u zwevende verkooporderrecords wilt opschonen, voert u de periodieke taak *Verkooporders verwijderen* uit door naar een van de volgende locaties te gaan:

- Verkoop en marketing \> Periodieke taken \> Opschonen \> Verkooporders verwijderen
- Detailhandel en commerce \> IT detailhandel en commerce \> Opschonen \> Verkooporders verwijderen

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a>Is er een manier om commissies te berekenen op facturen die al zijn geboekt?

Supply Chain Management biedt momenteel geen ondersteuning voor de berekening van commissies voor geboekte facturen.
