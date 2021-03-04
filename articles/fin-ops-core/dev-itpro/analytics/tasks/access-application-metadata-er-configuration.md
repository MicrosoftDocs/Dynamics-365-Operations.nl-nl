---
title: De toepassingsmetagegevens gebruiken met de ER‑configuratie
description: In de stappen in dit onderwerp wordt uitgelegd hoe een gebruiker van de Regulatory Configuration Service (RCS) een nieuwe Elektronisch Rapportage modeltoewijzing kan ontwerpen met behulp van de metagegevens in Finance and Operations.
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fa8e9ac4940bbc1252819ebcc3de2e21c9e0933f
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682160"
---
# <a name="access-application-metadata-by-using-er-configuration"></a>De toepassingsmetagegevens gebruiken met de ER‑configuratie

[!include [banner](../../includes/banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker van Regulatory Configuration Service (RCS) in de rol van systeembeheerder of ER-ontwikkelaar een nieuwe ER-modeltoewijzing kan maken met gebruik van de metagegevens van de toepassing. De metagegevens van de toepassing worden benaderd via een ER-metagegevensconfiguratie die een voorbeeldset bevat van metagegevens voor de toegang tot buitenlandse handelstransacties. Als u deze stappen wilt uitvoeren, moet u eerst in RCS de stappen voltooien in het onderwerp [Configuratieproviders maken en deze als actief markeren](er-configuration-provider-mark-it-active-2016-11.md)‑procedure. Voer vervolgens de stappen uit in het onderwerp, [Toepassingsmetagegevens voorbereiden voor gebruik in RCS](prepare-application-metadata-rcs.md).

## <a name="prerequisites"></a>Vereisten
1. Ga naar **Alle werkgebieden** > **Elektronische rapportage**. 
2. Controleer of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. beschikbaar is en gemarkeerd als **Actief**. Als u deze configuratieprovider niet ziet, voltooi dan de stappen in de procedure [Configuratieproviders maken en deze als actief markeren](er-configuration-provider-mark-it-active-2016-11.md). 

## <a name="import-metadata-configuration"></a>Importeren metagegevensconfiguratie 
1. Klik op **Metagegevensconfiguraties**. 
2. De ER metagegevensconfiguratie importeren die metadata bevat uit de toepassing die is geconfigureerd voor het genereren van elektronische documenten voor buitenlandse handel. Deze ER-metagegevensconfiguratie is geëxporteerd als XML-bestand terwijl de stappen in de procedure [Toepassingsmetagegevens voorbereiden voor gebruik in RCS](prepare-application-metadata-rcs.md) zijn voltooid. 
3. Klik op **Uitwisselen**. 
4. Klik op **Laden uit XML-bestand**. 
5. Klik op **Bladeren** en selecteer het bestand 'Buitenlandse handel metagegevens.xml'. 
6. Klik op **OK**. 
7. Sluit de pagina. 

## <a name="create-data-model-configuration"></a>Een gegevensmodelconfiguratie maken
1. Klik op **Rapportconfiguraties**. 
2. Klik op **Configuratie maken** om het dialoogvenster voor beëindigen te openen. 
3. Type 'Model buitenlandse handel' in het veld **Naam**. 
4. Klik op **Configuratie maken**. 
5. Klik op **Ontwerper**. 
6. Klik op **Nieuw** om het uitklapdialoogvenster te openen. 
7. Typ het veld **Naam** 'Basis'. 
8. Klik op **Toevoegen**. 
9. Klik op **Nieuw** om het uitklapdialoogvenster te openen. 
10.    Typ 'Transactie' in het veld **Naam**. 
11.    Selecteer in het veld **Itemtype** **Recordlijst**. 
12.    Klik op **Toevoegen**. 
13.    Klik op **Nieuw** om het uitklapdialoogvenster te openen. 
14.    Typ 'Code basisproduct' in het veld **Naam**. 
15.    Selecteer in het veld **Itemtype** **Tekenreeks**. 
16.    Klik op **Toevoegen**. 
17.    Klik op **Nieuw** om het uitklapdialoogvenster te openen. 
18.    Typ 'Gefactureerd bedrag' in het veld **Naam**. 
19.    Selecteer in het veld **Itemtype** **Werkelijk**. 
20.    Klik op **Toevoegen**. 
21.    Klik op **Nieuw** om het uitklapdialoogvenster te openen. 
22.    Typ 'Datum' in het veld **Naam**. 
23.    Selecteer in het veld **Itemtype** **Datum**. 
24.    Klik op **Toevoegen**. 
25.    Klik op **Basisverwijzing**. 
26.    Klik op **OK**. 
27.    Klik op **Opslaan**. 
28.    Sluit de pagina. 
29.    Klik op **Status wijzigen**. 
30.    Klik op **Voltooien**. 
31.    Klik op **OK**. 

## <a name="create-model-mapping-configuration"></a>Configuratie modeltoewijzing maken 
1. Klik op **Configuratie maken** om het dialoogvenster voor beëindigen te openen. 
2. Voer in het veld **Nieuw** 'Modeltoewijzing gebaseerd op gegevensmodel Buitenlandse handelsmodel' in. 
3. Type 'Buitenlandse handel toewijzing' in het veld **Naam**. 
4. Klik op **Configuratie maken**. 
5. Vouw de sectie **Vereisten** uit. 
6. Klik op **Bewerken**. 
7. Klik op **Nieuw**. 
8. Markeer in de lijst de geselecteerde rij. 
9. Selecteer in het veld **Vereist onderdeeltype** **Configuratie**. 
10.    Selecteer configuratie **Metagegevens buitenlandse handel**. 
11.    Klik op **Opslaan**. 
12.    De verwijzing naar versie 1 van de configuratie van de 'Metagegevens buitenlandse handel' is toegevoegd. De metagegevens van de toepassing van deze configuratie worden aangeboden wanneer deze modeltoewijzing wordt ontworpen. 
13.    Sluit de pagina. 
14.    Klik op **Ontwerper**. 
15.    Klik op **Ontwerper**. 
16.    Selecteer in de structuur **Dynamics 365 for Operations'\Tabelrecords**. 
17.    Klik op **Basis toevoegen**. 
18.    Typ 'intrastat' in het veld **Naam**. 
19.    Selecteer **Intrastat** tabelrecords. 
20.    Klik op **OK**. 

> [!NOTE]
> De enige twee tabellen zijn aangeboden, omdat de enige twee tabellen zijn toegevoegd aan de set metagegevens die momenteel in gebruik zijn. 

21.    Klik op **Binden**. 
22.    Vouw in de structuur **Intrastat** uit. 
23.    Selecteer **Intrastat\BedragMST** in de structuur. 
24.    Vouw in de structuur **Transactie = Intrastat** uit. 
25.    Selecteer in de structuur **Transacties = Intrastat\Gefactureerd bedrag**. 
26.    Klik op **Binden**. 
27.    Selecteer **Intrastat\TransDatum** in de structuur. 
28.    Selecteer **Transactie = Intrastat\Datum** in de structuur. 
29.    Klik op **Binden**. 
30.    Vouw in de structuur **Intrastat\>Relaties** uit. 
31.    Vouw in de structuur **Intrastat\>Relaties\IntrastatBasisproduct** uit. 
32.    Selecteer in de structuur **Intrastat\>Relaties\IntrastatBasisproduct\Code**. 
33.    Selecteer in de structuur **Transacties = Intrastat\Basisproductcode**. 
34.    Klik op **Binden**. 
35.    Klik op **Valideren**. 

> [!NOTE]
> We hebben elementen van het gegevensmodel gebonden met items van gegevensbronnen die worden beschreven met behulp van toepassingsmetagegevens van de ER metagegevensconfiguratie waarnaar wordt verwezen. 
36.    Klik op **Opslaan**. 
37.    Sluit de pagina. 
38.    Sluit de pagina. 
39.    Indien nodig kunt u de bestaande set metagegevens uitbreiden en vervolgens de nieuwe, voltooide versie van de ER-metagegevensconfiguratie exporteren. U kunt deze vervolgens importeren in RCS en de vereisten van de geconfigureerde configuratie van de modeltoewijzing bijwerken naar een nieuwe versie van de geïmporteerde metagegevensconfiguratie. 

> [!NOTE]
> Deze manier om informatie op te halen over de metagegevens van de toepassing is de enige die beschikbaar is voor lokaal geïmplementeerde toepassingen (wanneer een LBD (Local Business Data) of on-premises implementatiemodel wordt gebruikt).
        


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]