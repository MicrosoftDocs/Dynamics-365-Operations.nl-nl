---
title: Metagegevens van de toepassing voorbereiden voor gebruik in RCS
description: In dit artikel wordt beschreven hoe u een nieuwe rapportageconfiguratie maakt die toepassingsmetagegevens bevat.
author: kfend
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ''
ms.openlocfilehash: a9ccbb120be43eaf7a8ae8b5bf8eaafb4850b199
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289969"
---
# <a name="prepare-application-metadata-to-be-used-in-rcs"></a>Metagegevens van de toepassing voorbereiden voor gebruik in RCS
[!include [banner](../../includes/banner.md)]

De volgende stappen leggen uit hoe een gebruiker met de rol Systeembeheerder of Ontwikkelaar Elektronische Rapportage een nieuwe configuratie voor een elektronische rapportage (ER) kan maken die de metagegevens van de toepassing bevat voor het ontwerpen van ER‑modelconfiguratie in Regulatory Configuration Service (RCS). Deze configuratie wordt gebruikt voor het ontwerpen van een voorbeeld van een ER‑modeltoewijzingsconfiguratie om transacties van buitenlandse handel te openen. In dit voorbeeld maakt u een configuratie voor het voorbeeldbedrijf Litware, Inc. Deze stappen kunnen in elk bedrijf worden uitgevoerd. Als u deze stappen wilt uitvoeren, moet u eerst de stappen voltooien in het artikel [Configuratieproviders maken en deze als actief markeren](er-configuration-provider-mark-it-active-2016-11.md).

## <a name="prerequisites"></a>Vereisten
1.    Ga naar **Organisatiebeheer** > **Werkruimten** > **Elektronische rapportage**. 
2.    Controleer of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. beschikbaar is en gemarkeerd als **Actief**. Als u deze configuratieprovider niet ziet, voltooi dan de stappen in de procedure [Configuratieproviders maken en deze als actief markeren](er-configuration-provider-mark-it-active-2016-11.md). 
3.    Klik op **Metagegevensconfiguraties**. 
4.    Stel dat RCS zal worden gebruikt om een ER-oplossing te ontwerpen voor Finance and Operations‑toepassing die elektronische documenten zal genereren die informatie bevatten uit het bedrijfsdomein voor buitenlandse handel. Als u de toewijzing wilt opgeven tussen het ER-gegevensmodel en de bronnen van vereiste gegevens, moeten we in RCS toegang hebben tot de metagegevens van de Finance and Operations‑toepassing. Als onderdeel van het ontwerpproces van de ER-oplossing moeten we dus een nieuwe ER-metagegevensconfiguratie configureren die alle vereiste metagegevens bevat voor het genereren van ER‑rapporten voor het geselecteerde bedrijfsdomein. 

## <a name="add-metadata-configuration"></a>Metagegevensconfiguratie toevoegen 
1.    Klik op **Configuratie maken** om het dialoogvenster voor beëindigen te openen. 
2.    Type 'Metadata buitenlandse handel' in het veld **Naam**. 
3.    Klik op **Configuratie maken**. 
4.    Klik op **Ontwerper**. 
5.    Klik op **Toevoegen**. 
  
> [!NOTE]
> U kunt alle metagegevens voor de gehele toepassing of voor geselecteerde modellen of modules selecteren. Houd er in dit geval rekening mee dat de volgende metagegevens automatisch worden toegevoegd: tabellen met records, inventarisaties en uitgebreide gegevenstypen. Als er aanvullende typen metagegevens nodig zijn, moeten deze handmatig worden toegevoegd. 
 
We hebben wat metagegevens die zijn gerelateerd aan transacties voor buitenlandse handel door metagegevensitems handmatig te selecteren. 
  
6.    Klik op **Gegevensbron toevoegen**. 
7.    Klik op **Tabelrecords**. 
8.    Gebruik het snelfilter om in het veld **Naam** te filteren met een waarde van 'Intrastat'. 
9.    Selecteer de **Intrastat** -tabelrecord. 
10.    Klik op **OK**.
  
We hebben metagegevens over de Intrastat-tabelrecords toegevoegd. 
  
11.    Vouw in de structuur **Tabelrecords Intrastat**\>**Relaties** uit. 
12.    Selecteer in de structuur **Tabelrecords Intrastat**\>**Relaties\ IntrastatCommodity (tabelrecords EcoResCategory)**.     
13.    Klik op **Metagegevens toevoegen**. 
  
> [!NOTE]
> Metagegevens over vereiste relaties voor geselecteerde tabelrecords moeten handmatig worden toegevoegd. 
  
16.    Klik op **Gegevensbron toevoegen**. 
17.    Klik **Opsomming**. 
18.    Gebruik het snelfilter om in het veld **Naam** te filteren met een waarde van 'IntrastatDirection'. 
19.    Selecteer het record **Opsomming IntrastatDirection**. 
20.    Klik op **OK**. 
21.    Klik op **Opslaan**.  
22.    Sluit de pagina. 
  
## <a name="complete-the-draft-version-of-metadata-configuration"></a>De conceptversie van metagegevensconfiguratie voltooien
1.    Klik op **Status wijzigen**. 
2.    Klik op **Voltooien**. 
3.    Klik op **OK**. 
4.    Selecteer de voltooide versie **1**. 
  
## <a name="export-the-completed-version-of-metadata-configuration-from-application-as-xml-file"></a>De voltooide versie van de metagegevensconfiguratie van de toepassing exporteren als een XML-bestand
1.    Klik op **Uitwisselen**. 
2.    Klik op **Exporteren als XML-bestand**. 
3.    Klik op **OK**. 
    
De gemaakte ER‑metagegevensconfiguratie is opgeslagen als XML-bestand dat kan worden geïmporteerd naar RCS en gebruikt als de bron van informatie over metagegevens voor het bedrijfsdomein voor buitenlandse handel. Op basis van deze informatie kunnen we de toewijzing opgeven tussen de metagegevens van de toepassing en het ER-gegevensmodel.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
