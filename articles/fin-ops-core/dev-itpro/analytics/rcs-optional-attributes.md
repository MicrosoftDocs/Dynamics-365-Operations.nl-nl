---
title: Bestanden in XML-indeling importeren met optionele kenmerken
description: Dit artikel bevat informatie over het ontwerpen van ER‑indelingen waarmee XML-kenmerken worden opgegeven voor het parseren van inkomende elektronische documenten in XML-indeling.
author: NickSelin
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: f5b25b51a4f59bf9c308bcaeb140e2737597798e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873217"
---
# <a name="import-files-in-xml-format-with-optional-attributes"></a>Bestanden in XML-indeling importeren met optionele kenmerken

[!include [banner](../includes/banner.md)]

U kunt ER-indelingen (elektronische rapportage) ontwerpen om inkomende elektronische documenten te parseren in XML-indeling. U kunt bepaalde kenmerken van XML-elementen als optioneel specificeren in de ontworpen ER‑indeling. Hiermee kunt u binnenkomende bestanden met en zonder dergelijke XML-kenmerken op de juiste manier verwerken. Vervolgens kunt u de inhoud van deze bestanden gebruiken om toepassingsgegevens bij te werken.

Als u meer wilt weten over deze functie, voltooit u de stappen in het artikel [RCS‑bestanden in XML-indeling importeren met optionele kenmerken](tasks/import-files-xml-format-optional-attributes.md), die deel uitmaken van het bedrijfsproces 7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677). U kunt deze taakbegeleiding en het bijbehorend voorbeeld downloaden uit het [Microsoft Downloadcentrum](https://go.microsoft.com/fwlink/?linkid=874684).


| Omschrijving inhoud       | Bestand                                                         |
|---------------------------|--------------------------------------------------------------|
| Voorbeeldbestand in XML‑indeling | IncomingdocumentToLearnHowToHandleOptionalAttributes.xml.     |
| Taakbegeleiding                | RCS Bestanden in XML-indeling met optionele kenmerken importeren.axtr |


In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een ER‑indelingsconfiguratie kan ontwerpen om bestanden in XML‑indeling met optionele kenmerken te importeren. Als u deze stappen wilt uitvoeren, moet u eerst de stappen voltooien in de procedure [Configuratieproviders maken en deze als actief markeren](tasks/er-configuration-provider-mark-it-active-2016-11.md). Voordat u begint, moet u het bestand IncomingdocumentToLearnHowToHandleOptionalAttributes.xml downloaden uit het Microsoft Downloadcenter en lokaal opslaan (https://go.microsoft.com/fwlink/?linkid=874684).

1. Ga naar **Organisatiebeheer** > **Werkruimten** > **Elektronische rapportage**.
2. Controleer of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. beschikbaar is en gemarkeerd als **Actief**. Als u deze configuratieprovider niet ziet, voltooit u de stappen in het artikel [Configuratieproviders maken en deze als actief markeren](tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Klik op **Rapportconfiguraties**.

## <a name="create-a-new-data-model-configuration"></a>Een nieuwe gegevensmodelconfiguratie maken
1. Klik op **Configuratie maken** om het dialoogvenster voor beëindigen te openen.
2. Typ in het veld **Naam** 'Model voor importeren van XML-bestand'.
3. Klik op **Configuratie maken**.
4. Klik op **Ontwerper**.
5. Klik op **Nieuw** om het uitklapdialoogvenster te openen.
6. Typ het veld **Naam** 'Basis'.
7. Klik op **Toevoegen**.
8. Klik op **Nieuw** om het uitklapdialoogvenster te openen.
9. Typ het veld **Naam** 'Lijst'.
10.    Selecteer in het veld **Itemtype** **Recordlijst**.
11.    Klik op **Toevoegen**.
12.    Klik op **Nieuw** om het uitklapdialoogvenster te openen.
13.    Typ in het veld **Naam** 'Code'.
14.    Selecteer in het veld **Itemtype** **Tekenreeks**.
15.    Klik op **Toevoegen**.
16.    Klik op **Opslaan**.
17.    Sluit de pagina.
18.    Klik op **Status wijzigen**.
19.    Klik op **Voltooien**.
20.    Klik op **OK**.

## <a name="create-a-format-for-data-import"></a>Een indeling maken voor het importeren van gegevens
1. Klik op **Configuratie maken** om het dialoogvenster voor beëindigen te openen.
2. Voer in het veld **Nieuw** in 'Indeling gebaseerd op gegevensmodel Model voor importeren van xml‑bestand'.
3. Typ in het veld **Naam** 'Indeling voor importeren van XML-bestand'. 
4. Selecteer **Ja** in het veld **Ondersteunt gegevensimport**.
5. Klik op **Configuratie maken**.

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a>Een indeling ontwerpen om het binnenkomende bestand in XML-indeling te parseren
1. Klik op **Ontwerper**.
2. Klik op **Basis toevoegen** om het dialoogvenster voor beëindiging te openen.
3. Selecteer **XML\Element** in de structuur.
4. Typ het veld **Naam** 'basis'.
5. Klik op **OK**.
6. Klik op **Toevoegen** om het dialoogvenster voor beëindigen te openen.
7. Selecteer **XML\Element** in de structuur.
8. Typ in het veld **Naam** 'document'.
9. Selecteer in het veld **Multiplicity** **Eén veel**.
10.    Klik op **OK**.
11.    Selecteer in de structuur **basis\document**.
12.    Klik op **Toevoegen** om het dialoogvenster voor beëindigen te openen.
13.    Selecteer **XML\Attribute** in de structuur.
14.    Typ in het veld **Naam** 'id'.
15.    Klik op **OK**.
16.    Klik op **Opslaan**.

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a>Een indelingstoewijzing ontwerpen om geparseerde informatie op te slaan in het gegevensmodel
1.    Klik op **Indeling aan model toewijzen**.
2.    Klik op **Nieuw**.
3.    Typ of selecteer een waarde in het veld **Definitie**.
4.    Typ in het veld **Naam** 'Toewijzing'.
5.    Klik op **Opslaan**.
6.    Klik op **Ontwerper**.
7.    Vouw in de structuur **indeling** uit.
8.    Vouw in de structuur **format\root: XML Element(root)** uit.
9.    Selecteer in de structuur **format\root: XML Element(root)\document: XML Element 1..* (document)**.
10.    Klik op **Binden**.
11.    Vouw in de structuur **format\root: XML Element(root)\document: XML Element 1..* uit (document)**.
12.    Selecteer in de structuur **format\root: XML Element(root)\document: XML Element 1..* (document)\id**.
13.    Vouw in de structuur **Lijst = format.root.document** uit.
14.    Selecteer in de structuur **Lijst = format.root.document\Code** uit.
15.    Klik op **Binden**.
16.    Klik op **Opslaan**.
17.    Sluit de pagina.

## <a name="run-format-mapping"></a>Indelingstoewijzing uitvoeren
1. Klik op **Uitvoeren**.
2. Klik op **Bladeren** en Selecteer het bestand **IncomingdocumentToLearnHowToHandleOptionalAttributes.xml**.
3. Klik op **OK**.

> [!NOTE]
> Het geselecteerde bestand is niet geïmporteerd omdat het indelingsontwerp ervan uitgaat dat er een id‑kenmerk bestaat voor het element document, maar het geïmporteerde bestand bevat geen kenmerk.

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a>Indelingsstructuur wijzigen om het XML-kenmerk als optioneel te verwerken
1. Sluit de pagina.
2. Vouw in de structuur **basis\document** uit.
3. Selecteer in de structuur **basis\document\id**.
4. Selecteer **Ja** in veld **Lege tekenreeks voor ontbrekend kenmerk**.
5. Klik op **Opslaan**.

## <a name="run-format-mapping-to-test-changes"></a>Indelingstoewijzing uitvoeren voor het testen van de wijzigingen
1. Klik op **Indeling aan model toewijzen**.
2. Klik op **Uitvoeren**.
3. Klik op **Bladeren** en Selecteer het bestand **IncomingdocumentToLearnHowToHandleOptionalAttributes.xml**.
4. Klik op **OK**.
5. Bekijk het gegenereerde bestand. Zie dat hetzelfde bestand is geïmporteerd omdat het indelingsontwerp nu het id‑kenmerk voor het element document beschouwt als optioneel.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]