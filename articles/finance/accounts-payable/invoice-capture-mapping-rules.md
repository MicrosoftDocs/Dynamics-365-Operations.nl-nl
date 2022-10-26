---
title: Toewijzingsregels voor de oplossing Invoice Capture
description: Dit artikel biedt informatie over de instelling van toewijzingsregels in de oplossing Invoice Capture.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: cd0d06f7fd3ed946756e975d0706687c2d4acc93
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691175"
---
# <a name="invoice-capture-solution-mapping-rules"></a>Toewijzingsregels voor de oplossing Invoice Capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Toewijzingsregels brengen basismodelgegevens over vanuit Microsoft Dynamics 365 Finance of het ERP-systeem. Nadat toewijzingsregels zijn ingesteld, wordt de informatie afgeleid die nodig is om leveranciersfacturen te maken in Finance. Wanneer toewijzingsregels worden gebruikt, controleert de klantenadministrateur de status in plaats van alle ontbrekende veldwaarden handmatig in te vullen.

Er zijn vier typen toewijzingsregels:

- Rechtspersoon
- Leveranciersaccount
- Item
- Onkostentype

## <a name="manage-mapping-rules-by-using-the-app"></a>Toewijzingsregels beheren met de app

Als u toewijzingsregels wilt beheren met behulp van de app, selecteert u **Instellingen**. Op het tabblad **Instellingen van toewijzingsregel** zijn vier opties beschikbaar:

- Rechtspersoon 
- Leveranciersaccount 
- Artikeltoewijzing 
- Onkostentype

U selecteert bijvoorbeeld de optie **Regels voor de toewijzing van rechtspersonen**. De rechtspersooncode wordt aangeduid met behulp van de bedrijfsnaam, het adres en het belastingregistratienummer. Voor een regel met de naam **LE-USPM** is de code van de rechtspersoon **USPM** als de bedrijfsnaam de tekst Contoso Robotics USA bevat.

Op deze pagina worden alle actieve toewijzingsregels weergegeven. Als u de inactieve toewijzingsregels wilt weergeven, selecteert u **Actieve regels voor de toewijzing van rechtspersonen** en vervolgens **Inactieve regels voor de toewijzing van rechtspersonen**.

De volgende acties zijn beschikbaar voor toewijzingsregels.

### <a name="create-a-mapping-rule"></a>Een toewijzingsregel maken

U kunt op twee manieren een toewijzingsregel maken:

- Selecteer **Nieuw** voor het maken van een nieuwe toewijzingsregel. Voer vervolgens de gegevens voor de toewijzingsregel in. De waarde voor **Regelnaam** moet uniek zijn voor elk type toewijzingsregel.
- Als u een bestaande toewijzingsregel selecteert, wordt de knop **Kopiëren** beschikbaar. Selecteer deze en selecteer vervolgens **OK** in het dialoogvenster dat verschijnt. Er wordt een toewijzingsregel gemaakt door de geselecteerde regel te dupliceren.

### <a name="edit-a-mapping-rule"></a>Een toewijzingsregel bewerken

Als u een toewijzingsregel wilt bewerken, selecteert u een veld en wijzigt u de waarde.

### <a name="activatedeactivate-mapping-rules"></a>Toewijzingsregels activeren/deactiveren

Als u een of meer toewijzingsregels wilt deactiveren, selecteert u deze op de pagina **Actieve toewijzingsregels** en selecteert u **Deactiveren**. De regels worden van de pagina **Actieve toewijzingsregels** naar de pagina **Inactieve toewijzingsregels** verplaatst.

En als u toewijzingsregels wilt activeren, selecteert u deze op de pagina **Inactieve toewijzingsregels** en selecteert u **Activeren**.

### <a name="remove-mapping-rules"></a>Toewijzingsregels verwijderen

Als u toewijzingsregels wilt verwijderen, selecteert u deze en vervolgens **Verwijderen**.

### <a name="check-for-conflicts"></a>Controleren op conflicten

Als twee toewijzingsregels dezelfde waarden voor **Rechtspersoon** en **Leverancierrekening** hebben, maar verschillende waarden voor **Artikelnaam**, wordt een conflict gedetecteerd en wordt de toewijzingsregel niet gemaakt of bijgewerkt.

## <a name="importexport-mapping-rules-from-excel"></a>Toewijzingsregels vanuit Excel importeren/exporteren

Een Excel-invoegvoeging kan worden gebruikt om regels in een batch te beheren. De volgende opties zijn beschikbaar:

- Een Excel-sjabloon downloaden.
- Exporteren naar Excel.
- Importeren uit Excel.

### <a name="download-an-excel-template"></a>Een Excel-sjabloon downloaden

Selecteer **Sjabloon downloaden** om een Excel-sjabloon te downloaden. Selecteer vervolgens de velden die in de sjabloon moeten worden opgenomen.

### <a name="export-to-excel"></a>Exporteren naar Excel

U kunt op twee manieren exporteren:

- Selecteer **Openen in Excel Online** om het bestand in Excel te openen. Vervolgens kunt u het bestand offline bewerken. Wanneer u klaar bent, selecteert u **Opslaan**. Al uw wijzigingen worden opgeslagen op de pagina **Toewijzingsregel**.
- Selecteer **Werkblad downloaden** om een Excel-bestand te downloaden dat toewijzingsregels bevat. Vervolgens kunt u het bestand bewerken. Wanneer u klaar bent, selecteert u **Importeren vanuit Excel** om het bijgewerkte werkblad te uploaden.

### <a name="import-from-excel"></a>Importeren uit Excel

1. Selecteer **Importeren uit Excel** om gegevens te importeren uit een XLSX-bestand. U kunt ook importeren uit CSV- (Comma Separated Values) of XML-bestanden. Voordat u gaat importeren, moet u bepalen of duplicaten zijn toegestaan.
2. Selecteer **Toewijzing controleren** om de toewijzing van kenmerken te controleren en om te bepalen of deze juist is. U kunt de toewijzingsrelatie wijzigen.
3. Wanneer u klaar bent, selecteert u **Importeren voltooien** om te beginnen met importeren.
4. U kunt **Proces bijhouden** selecteren om de voortgang van het importproces bij te houden.

    De importstatus wordt bijgewerkt van **Voltooien** naar **Parseren** en vervolgens naar **Transformeren** en tot slot naar **Voltooid**.

Wanneer het importproces is voltooid, worden statistieken voor successen, gedeeltelijke fouten, fouten en totale verwerking weergegeven.
