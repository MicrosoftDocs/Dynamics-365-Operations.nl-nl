---
title: RCS‑bestanden in XML-indeling importeren met optionele kenmerken
description: Dit onderwerp biedt informatie over de manier waarop een gebruiker ER‑opmaakconfiguraties kan ontwerpen om bestanden in XML-indeling met optionele kenmerken te importeren.
author: NickSelin
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1d4c8c1d81faa60193d2339fd6541e752c2e2f9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684133"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a>RCS‑bestanden in XML-indeling importeren met optionele kenmerken

[!include [banner](../../includes/banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een ER‑indelingsconfiguratie kan ontwerpen om bestanden in XML‑indeling met optionele kenmerken te importeren. Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" voltooien. Voordat u begint, moet u het bestand IncomingdocumentToLearnHowToHandleOptionalAttributes.xml downloaden uit het [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684) en lokaal opslaan.

1.    Ga naar **Alle werkgebieden** > **Elektronische rapportage**.
2.    Controleer of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. beschikbaar is en gemarkeerd als **Actief**. Als u deze configuratieprovider niet ziet, voltooi dan de stappen in de procedure [Configuratieproviders maken en deze als actief markeren](er-configuration-provider-mark-it-active-2016-11.md).
3.    Klik op **Rapportconfiguraties**.

## <a name="create-a-new-data-model-configuration"></a>Een nieuwe gegevensmodelconfiguratie maken
1.    Klik op **Configuratie maken** om het dialoogvenster voor beëindigen te openen.
2.    Typ in het veld **Naam** 'Model voor importeren van XML-bestand'.
3.    Klik op **Configuratie maken**.
4.    Klik op **Ontwerper**.
5.    Klik op **Nieuw** om het uitklapdialoogvenster te openen.
6.    Typ het veld **Naam** 'Basis'.
7.    Klik op **Toevoegen**.
8.    Klik op **Nieuw** om het uitklapdialoogvenster te openen.
9.    Typ het veld **Naam** 'Lijst'.
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
1.    Klik op **Configuratie maken** om het dialoogvenster voor beëindigen te openen.
2.    Voer in het veld **Nieuw** in 'Indeling gebaseerd op gegevensmodel Model voor importeren van xml‑bestand'.
3.    Typ in het veld **Naam** 'Indeling voor importeren van XML-bestand'.
4.    Selecteer **Ja** in het veld **Ondersteunt gegevensimport**.
5.    Klik op **Configuratie maken**.

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a>Een indeling ontwerpen om het binnenkomende bestand in XML-indeling te parseren
1.    Klik op **Ontwerper**.
2.    Klik op **Basis toevoegen** om het dialoogvenster voor beëindiging te openen.
3.    Selecteer **XML\Element** in de structuur.
4.    Typ het veld **Naam** 'basis'.
5.    Klik op **OK**.
6.    Klik op **Toevoegen** om het dialoogvenster voor beëindigen te openen.
7.    Selecteer **XML\Element** in de structuur.
8.    Typ in het veld **Naam** 'document'.
9.    Selecteer in het veld **Multiplicity** **Eén veel**.
10.    Klik op **OK**.
11.    Selecteer in de structuur **basis\document**.
12.    Klik op **Toevoegen** om het dialoogvenster voor beëindigen te openen.
13.    Selecteer **XML\Attribute** in de structuur.
14.    Typ in het veld **Naam** 'ID'.
15.    Klik op **OK**.
16.    Klik op **Opslaan**.

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a>Een indelingstoewijzing ontwerpen om geparseerde informatie op te slaan in het gegevensmodel
1. Klik op **Indeling aan model toewijzen**.
2. Klik op **Nieuw**.
3. Typ of selecteer een waarde in het veld **Definitie**.
4. Klik in de lijst op de koppeling in de geselecteerde rij.
5. Typ in het veld **Naam** 'Toewijzing'.
6. Klik op **Opslaan**.
7. Klik op **Ontwerper**.
8. Vouw in de structuur **indeling** uit.
9. Vouw in de structuur **format\root: XML Element(root)** uit.
10.    Selecteer in de structuur **format\root: XML Element(root)\document: XML Element 1..* (document)**.
11.    Klik op **Binden**.
12.    Vouw in de structuur **format\root: XML Element(root)\document: XML Element 1..* uit (document)**.
13.    Selecteer in de structuur **format\root: XML Element(root)\document: XML Element 1..* (document)\id**.
14.    Vouw in de structuur **Lijst = format.root.document** uit.
15.    Selecteer in de structuur **Lijst = format.root.document\Code** uit.
16.    Klik op **Binden**.
17.    Klik op **Opslaan**.
18.    Sluit de pagina.
 
## <a name="run-format-mapping"></a>Indelingstoewijzing uitvoeren
1. Klik op **Uitvoeren**.
2. Klik op **Bladeren** en Selecteer **IncomingdocumentToLearnHowToHandleOptionalAttributes.xml**.
3. Klik op **OK**.

> [!NOTE]
> Het geselecteerde bestand is niet geïmporteerd omdat het indelingsontwerp ervan uitgaat dat er een id‑kenmerk bestaat voor het element document, maar het geïmporteerde bestand bevat geen kenmerk.

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a>Indelingsstructuur wijzigen om het XML-kenmerk als optioneel te verwerken
1. Sluit de pagina.
2. Vouw in de structuur **basis\document** uit.
3. Selecteer in de structuur **basis\document\id**.
4. Selecteer **Ja** in veld **Lege tekenreeks voor ontbrekende kenmerk**.
5. Klik op **Opslaan**.
 
## <a name="run-format-mapping-to-test-changes"></a>Indelingstoewijzing uitvoeren voor het testen van de wijzigingen
1. Klik op **Indeling aan model toewijzen**.
2. Klik op **Uitvoeren**.
3. Klik op **Bladeren** en Selecteer het bestand **IncomingdocumentToLearnHowToHandleOptionalAttributes.xml**.
4. Klik op **OK**.
5. Bekijk het gegenereerde bestand. 

> [!NOTE]
> Hetzelfde bestand is geïmporteerd als het opmaakontwerp, beschouw nu het kenmerk 'id' voor het element 'document' als optioneel.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]