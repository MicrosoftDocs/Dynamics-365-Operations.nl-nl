---
title: Assortimenten instellen
description: In dit artikel wordt beschreven wat een assortiment is en hoe u assortimenten instelt in Microsoft Dynamics 365 for Retail.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15811
ms.assetid: d2580048-e798-4b33-85f9-d1bad7d262fc
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 91713a4492ad82520f7dde611c17a5ea168ed80d
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-assortments"></a>Assortimenten instellen

[!include[banner](includes/banner.md)]


In dit artikel wordt beschreven wat een assortiment is en hoe u assortimenten instelt in Microsoft Dynamics 365 for Retail.

Een assortiment is een verzameling van verwante producten die u aan toewijst aan een afzetkanaal voor detailhandel, zoals een fysieke winkel of een online winkel. U kunt assortimenten gebruiken om de producten te identificeren die beschikbaar zijn in elke winkel. Een assortiment kan productcategorieën bevatten. Alle producten die aan een speciale categorie zijn toegewezen behoren daarom tot het assortiment. Een assortiment kan ook specifieke producten en bepaalde varianten van producten bevatten. Door een assortiment in te stellen, kunt u duizenden producten tegelijkertijd toewijzen aan uw verkoopkanalen, in de combinatie die uw winkels vereisen. U kunt zo veel productassortimenten als nodig instellen. Elk product kan in één of meer assortimenten opgenomen worden en elk assortiment kan aan één of meer detailhandelkanalen toegewezen worden. U definieert bijvoorbeeld één assortiment met een basisset van producten. Alle winkels ontvangen dit assortiment. Vervolgens definieert u een ander assortiment dat alleen grote sportuitrustingen bevat. Alleen uw grotere winkels ontvangen dit assortiment. Het volgende diagram laat zien hoe producten kunnen worden toegewezen aan assortimenten en hoe deze assortimenten kunnen worden toegewezen aan verkoopkanalen. ![Relaties productassortiment](./media/assortments_relationship.gif)

## <a name="prerequisites"></a>Vereisten
Voordat u een assortiment kunt instellen en aan een detailhandelkanaal kunt toewijzen, moet u de volgende taken uitvoeren.

| Opdracht                              | Beschrijving                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Een detailhandelkanaal instellen.          | Verkoopkanalen vertegenwoordigen een fysieke winkel, een online winkel of een online marktplaats. U moet ten minste één detailhandelkanaal instellen en de opties voor de winkel configureren. Assortimenten zijn toegewezen aan winkels om producten te identificeren die een bepaalde winkel heeft.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Een organisatiehiërarchie maken. | Nadat u de detailhandelkanalen hebt ingesteld voor uw organisatie, moet u een hiërarchie van de detailhandel configureren die de organisatorische structuur van uw detailhandelkanalen vertegenwoordigt. De hiërarchie van een organisatie kan worden gebruikt voor assortimenten, aanvulling en rapportering. Door uw detailhandelkanalen toe te voegen aan een organisatiehiërarchie, kunt u assortimenten toewijzen aan groepen winkels. In plaats van het assortiment afzonderlijk toe te wijzen aan elke winkel, kunt u het assortiment toewijzen aan het organisatieknooppunt op hoog niveau. Vervolgens, wanneer een nieuw detailhandelkanaal wordt toegevoegd aan het organisatieknooppunt op hoog niveau, neemt die detailhandel automatisch alle assortimenten over die zijn toegewezen aan het bovenliggende organisatieknooppunt. U kunt alleen assortimenten toewijzen aan verkoopkanalen die zijn opgenomen in een organisatiehiërarchie die is toegewezen aan het doel **Detailhandelassortiment**. |
| Producten definiëren.                  | Voordat u producten aan een assortiment kunt toevoegen, moet u deze toevoegen in Microsoft Dynamics 365 for Retail. U kunt producten handmatig toevoegen of u kunt ze importeren van een leverancier. Nadat u de producten toevoegt, moet u deze vrijgeven aan een rechtspersoon. Alleen producten die zijn vrijgegeven aan een rechtspersoon kunnen aan uw detailhandelkanalen beschikbaar worden gesteld. Producten die nog niet aan een rechtspersoon zijn vrijgegeven, kunnen worden toegevoegd aan een assortiment en dat assortiment kan goedgekeurd worden. Tot de producten echter vrijgegeven worden aan een rechtspersoon, kunnen deze niet beschikbaar worden gesteld voor verkoopkanalen.                                                                                                                                                                                                                                                                                     |
| Een categoriehiërarchie instellen.      | Wanneer u detailhandelproducten maakt, kunt u deze groeperen en categoriseren door middel van de functie categoriehiërarchie. U kunt één kernhiërarchie maken om alle producten die u via uw detailhandelkanalen verdeelt, te groeperen en te categoriseren. U kunt ook afzonderlijke, aanvullende categoriehiërarchieën maken om uw producten te groeperen of te categoriseren voor speciale doeleinden, zoals acties of assortimenten. Door categoriehiërarchieën te gebruiken, kunt u alle producten in een bepaalde categorie toewijzen aan een assortiment. Producten die worden toegevoegd aan de categorie die is opgenomen in het assortiment, worden automatisch opgenomen in het assortiment. Vervolgens worden deze producten beschikbaar voor de detailhandelkanalen waar het assortiment aan is toegewezen nadat de detailhandelassortimentplanner wordt uitgevoerd.                                            |

## <a name="setting-up-an-assortment"></a>Een assortiment instellen
Na het voltooien van de vereisten kunt u een assortiment maken en dit aan uw detailhandelkanalen toewijzen. Voor het instellen van een assortiment moet u de volgende taken voltooien.

1.  Een nieuwe assortiment maken of kopiëren van een bestaand assortiment.
2.  Selecteer de detailhandelkanalen of de groepen detailhandelkanalen op hoog niveau waarop het assortiment van toepassing is.
3.  Productcategorieën, individuele producten of productvarianten toevoegen aan het assortiment. U kunt alle producten in een specifieke categorie plaatsen of u kunt geselecteerde producten uitsluiten van een categorie die is opgenomen in het assortiment.
4.  Assortiment publiceren. Wanneer u een assortiment publiceert, wordt de planner van het detailhandelassortiment automatisch uitgevoerd. Dit proces genereert de lijst van producten. Na het uitvoeren van dit proces, worden deze producten beschikbaar voor de detailhandelkanalen waar het productassortiment aan is toegewezen. Als wijzigingen zijn aangebracht aan een gepubliceerd assortiment of aan de detailhandelkanalen waar het assortiment aan is toegewezen, moet het assortiment worden bijgewerkt. Om het assortiment bij te werken wanneer wijzigingen worden aangebracht, kunt u de detailhandelassortimentplanner uitvoeren als batchtaak.





