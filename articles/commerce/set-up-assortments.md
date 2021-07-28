---
title: Assortimenten instellen
description: In dit artikel wordt beschreven wat een assortiment is en hoe u assortimenten instelt in Dynamics 365 Commerce.
author: jblucher
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.custom: 15811
ms.assetid: d2580048-e798-4b33-85f9-d1bad7d262fc
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 447c5f580e5d925efbfeaabc3890e2d67f9688f5
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6344342"
---
# <a name="set-up-assortments"></a>Assortimenten instellen

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven wat een assortiment is en hoe u assortimenten instelt in Dynamics 365 Commerce.

Een assortiment is een verzameling van verwante producten die u aan toewijst aan een kanaal voor handel, zoals een fysieke winkel of een online winkel. U kunt assortimenten gebruiken om de producten te identificeren die beschikbaar zijn in elke winkel. Een assortiment kan productcategorieën bevatten. Alle producten die aan een speciale categorie zijn toegewezen behoren daarom tot het assortiment. Een assortiment kan ook specifieke producten en bepaalde varianten van producten bevatten. Door een assortiment in te stellen, kunt u duizenden producten tegelijkertijd toewijzen aan uw kanalen, in de combinatie die uw winkels vereisen. U kunt zo veel productassortimenten als nodig instellen. Elk product kan in één of meer assortimenten opgenomen worden en elk assortiment kan aan één of meer kanalen toegewezen worden. U definieert bijvoorbeeld één assortiment met een basisset van producten. Alle winkels ontvangen dit assortiment. Vervolgens definieert u een ander assortiment dat alleen grote sportuitrustingen bevat. Alleen uw grotere winkels ontvangen dit assortiment. Het volgende diagram laat zien hoe producten kunnen worden toegewezen aan assortimenten en hoe deze assortimenten kunnen worden toegewezen aan kanalen.

![Relaties productassortiment.](./media/assortments_relationship.gif)

## <a name="prerequisites"></a>Vereisten

Voordat u een assortiment kunt instellen en aan een handelkanaal kunt toewijzen, moet u de volgende taken uitvoeren.

| Opdracht                              | Beschrijving |
|-----------------------------------|-------------|
| Een kanaal instellen.          | Kanalen vertegenwoordigen een fysieke winkel, een online winkel of een online marktplaats. U moet ten minste één kanaal instellen en de opties voor de winkel configureren. Assortimenten zijn toegewezen aan winkels om producten te identificeren die een bepaalde winkel heeft. |
| Een organisatiehiërarchie maken. | Nadat u de handelkanalen hebt ingesteld voor uw organisatie, moet u een organisatiehiërarchie configureren die de organisatorische structuur van uw kanalen vertegenwoordigt. De hiërarchie van een organisatie kan worden gebruikt voor assortimenten, aanvulling en rapportering. Door uw kanalen toe te voegen aan een organisatiehiërarchie, kunt u assortimenten toewijzen aan groepen winkels. In plaats van het assortiment afzonderlijk toe te wijzen aan elke winkel, kunt u het assortiment toewijzen aan het organisatieknooppunt op hoog niveau. Vervolgens, wanneer een nieuw kanaal wordt toegevoegd aan het organisatieknooppunt op hoog niveau, neemt dat kanaal automatisch alle assortimenten over die zijn toegewezen aan het bovenliggende organisatieknooppunt. U kunt alleen assortimenten toewijzen aan kanalen die zijn opgenomen in een organisatiehiërarchie die is toegewezen aan het doel **Commerce-assortiment**. |
| Producten definiëren.                  | Voordat u producten aan een assortiment kunt toevoegen, moet u deze toevoegen in Commerce. U kunt producten handmatig toevoegen of u kunt ze importeren van een leverancier. Nadat u de producten toevoegt, moet u deze vrijgeven aan een rechtspersoon. Alleen producten die zijn vrijgegeven aan een rechtspersoon kunnen aan uw kanalen beschikbaar worden gesteld. Producten die nog niet aan een rechtspersoon zijn vrijgegeven, kunnen worden toegevoegd aan een assortiment en dat assortiment kan goedgekeurd worden. Tot de producten echter vrijgegeven worden aan een rechtspersoon, kunnen deze niet beschikbaar worden gesteld voor kanalen. |
| Een categoriehiërarchie instellen.      | Wanneer u handelsproducten maakt, kunt u deze groeperen en categoriseren door middel van de functie categoriehiërarchie. U kunt één kernhiërarchie maken om alle producten die u via uw kanalen verdeelt, te groeperen en te categoriseren. U kunt ook afzonderlijke, aanvullende categoriehiërarchieën maken om uw producten te groeperen of te categoriseren voor speciale doeleinden, zoals acties of assortimenten. Door categoriehiërarchieën te gebruiken, kunt u alle producten in een bepaalde categorie toewijzen aan een assortiment. Producten die worden toegevoegd aan de categorie die is opgenomen in het assortiment, worden automatisch opgenomen in het assortiment. Vervolgens worden deze producten beschikbaar voor de handelskanalen waar het assortiment aan is toegewezen nadat de handelassortimentplanner wordt uitgevoerd. |

## <a name="setting-up-an-assortment"></a>Een assortiment instellen

Na het voltooien van de vereisten kunt u een assortiment maken en dit aan uw kanalen toewijzen. Voor het instellen van een assortiment moet u de volgende taken voltooien.

1. Een nieuwe assortiment maken of kopiëren van een bestaand assortiment.
2. Selecteer de kanalen of de groepen kanalen op hoog niveau waarop het assortiment van toepassing is.
3. Productcategorieën, individuele producten of productvarianten toevoegen aan het assortiment. U kunt alle producten in een specifieke categorie plaatsen of u kunt geselecteerde producten uitsluiten van een categorie die is opgenomen in het assortiment.
4. Assortiment publiceren. Wanneer u een assortiment publiceert, wordt de assortimentsplanner automatisch uitgevoerd. Dit proces genereert de lijst van producten. Na het uitvoeren van dit proces, worden deze producten beschikbaar voor de kanalen waar het productassortiment aan is toegewezen. Als wijzigingen zijn aangebracht aan een gepubliceerd assortiment of aan de kanalen waar het assortiment aan is toegewezen, moet het assortiment worden bijgewerkt. Om het assortiment bij te werken wanneer wijzigingen worden aangebracht, kunt u de assortimentsplanner uitvoeren als batchtaak.


[!INCLUDE[footer-include](../includes/footer-banner.md)]