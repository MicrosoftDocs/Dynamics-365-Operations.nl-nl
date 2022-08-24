---
title: Metagegevens van de toepassing openen door gebruik van verbonden toepassingen
description: In de stappen in dit artikel wordt uitgelegd hoe een gebruiker van de Regulatory Configuration Service een nieuwe Elektronisch Rapportage modeltoewijzing kan ontwerpen met behulp van de metagegevens.
author: kfend
ms.date: 06/29/2019
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
ms.openlocfilehash: 1a935b96e247978fc2b2f9449d403c92bff35f17
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267867"
---
# <a name="access-application-metadata-by-using-connected-applications"></a>Metagegevens van de toepassing openen door gebruik van verbonden toepassingen

[!include [banner](../../includes/banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker van Regulatory Configuration Service (RCS) in de rol van systeembeheerder of ER-ontwikkelaar een nieuwe ER-modeltoewijzing kan maken met gebruik van de metagegevens van de apps voor financiën en bedrijfsactiviteiten. Toepassingsmetagegevens worden online benaderd via de met de toepassing RCS verbonden toepassing. Voorbeeld ER modeltoewijzing wordt geconfigureerd voor het openen van transacties van buitenlandse handel. Als u deze stappen wilt uitvoeren, moet u in RCS eerst de stappen voltooien in het artikel [Configuratieproviders maken en deze als actief markeren](er-configuration-provider-mark-it-active-2016-11.md). Als u de stappen in het artikel [Toepassingsmetagegevens openen met gebruik van de ER‑configuratie](access-application-metadata-er-configuration.md) niet hebt voltooid, downloadt u de [pagina Voorbeelden van elektronische rapportage](https://download.microsoft.com/download/0/4/e/04e13839-e423-442b-a6c2-dd35b1045c2d/Dynamics%20365%20for%20Finance%20and%20Operations%208.1%20Electronic%20reporting%20task%20guides.zip) en slaat u de volgende ER‑configuratie op: Metagegevens buitenlandse handel.xml, Metagegevens buitenlandse handel.xml, Toewijzing buitenlandse handel.xml en voltooit u dan de stappen van de procedure.

## <a name="prerequisites"></a>Vereisten
1. Ga naar **Alle werkgebieden** > **Elektronische rapportage**. 
2. Controleer of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. beschikbaar is en gemarkeerd als **Actief**. Als u deze configuratieprovider niet ziet, voltooi dan de stappen in de procedure [Configuratieproviders maken en deze als actief markeren](er-configuration-provider-mark-it-active-2016-11.md). 

## <a name="get-required-er-configurations"></a>De vereiste ER-configuraties verkrijgen
1. Klik op **Rapportconfiguraties**. 
2. Als u de stappen in de procedure [Gebruik de toepassingsmetagegevens met gebruik van de ER‑configuratie](access-application-metadata-er-configuration.md) al hebt voltooid, beschikt u al over alle benodigde ER‑configuraties (metagegevens buitenlandse handel, model- en toewijzingsconfiguraties) in het huidige RCS‑exemplaar. U kunt alle overige stappen in deze subtaak overslaan. 
3. Klik op **Uitwisselen**. 
4. Klik op **Laden uit XML-bestand**. 
5. Klik op **Bladeren** en selecteer het bestand **Buitenlandse handel metagegevens.xml**. 
6. Klik op **OK**. 
7. Klik op **Uitwisselen**. 
8. Klik op **Laden uit XML-bestand**. 
9. Klik op **Bladeren** en selecteer het bestand **Buitenlandse handel model.xml**. 
10. Klik op **OK**. 
11. Klik op **Uitwisselen**. 
12. Klik op **Laden uit XML-bestand**. 
13. Klik op **Bladeren** en selecteer het bestand **Buitenlandse handel toewijzing.xml**. 
14. Klik op **OK**. 

## <a name="register-a-connected-application"></a>Een verbonden toepassing registreren
1. Sluit de pagina. 
2. Sluit de pagina. 
3. Ga naar **Alle werkgebieden** > **Elektronische rapportage**. 
4. Klik op **Verbonden toepassingen**. 
5. Controleer of de geconfigureerde toepassing op Azure gebaseerd is en toegankelijk is voor de huidige RCS-gebruiker. Het is ook noodzakelijk dat de huidige RCS-gebruiker toegang heeft tot de geselecteerde toepassing en dat deze is geregistreerd als gebruiker van deze toepassing met een rol die hem of haar de bevoegdheid geeft om de metagegevens van de toepassing te gebruiken. 
6. Klik op **Nieuw**. 
7. Typ 'MijnVerbondenApp' in het veld **Naam**. 
8. Typ 'https://mycompany.operations.dynamics.com' in het veld **Toepassing**. 
9. Typ 'mycompany.onmicrosoft.com' in het veld **Tenant**. 
10. Klik op **Opslaan**. 
11. Wanneer u de verbinding met de geconfigureerde toepassing controleert, klikt u op de pagina **Maak verbinding met externe toepassing** op de link **Klik hier om verbinding te maken met de geselecteerde externe toepassing**. 
12. Klik op **Verbinding controleren**. 
13. Klik op **Sluiten**. 
14. Wanneer de verbindingsvalidatie is geslaagd, worden de versie- en tenantgegevens bijgewerkt voor de geconfigureerde toepassing in het huidige raster. 

## <a name="review-existing-model-mapping-configuration"></a>Een bestaande modeltoewijzingsconfiguratie controleren
1. Sluit de pagina. 
2. Klik op **Rapportconfiguraties**. 
3. Vouw **Buitenlandse handel model** uit in de structuur. 
4. Selecteer in de structuur **Buitenlandse handel model\Buitenlandse handel toewijzing**. 
5. Vouw de sectie **Vereisten** uit. 

    > [!NOTE]
    > Deze toewijzing verwijst momenteel naar de metagegevensconfiguratie. De metagegevens van de toepassing van deze configuratie worden aangeboden wanneer deze modeltoewijzing wordt ontworpen. 

6. Klik op **Ontwerper**. 
7. Klik op **Ontwerper**. 
8. Selecteer in de structuur **Dynamics 365 for Operations'\Tabelrecords**. 
9. Klik op **Basis toevoegen**. 
10. Typ of selecteer een waarde in het veld **Tabel**. 

    > [!NOTE]
    > Deze toewijzing verwijst momenteel naar de metagegevensconfiguratie. De metagegevens van de toepassing van deze configuratie worden aangeboden wanneer deze modeltoewijzing wordt ontworpen. 

11. Klik op **Annuleren**. 
12. Sluit de pagina. 
13. Sluit de pagina. 

## <a name="assign-connected-application-to-model-mapping"></a>Verbonden toepassing toewijzen aan modeltoewijzing 
1. Klik op **Bewerken**. 
2. Selecteer de **MyConnectedApp** toepassing. 

    > [!NOTE]
    > Op dit moment verwijst deze toewijzing naar de metagegevens van de geselecteerde gekoppelde toepassing. Wanneer dezelfde toewijzing tegelijkertijd verwijst naar de configuratie van de metagegevens en de gekoppelde toepassing, dan worden de metagegevens van de verbonden toepassing gebruikt. 

3. Klik op **Ontwerper**. 
4. Klik op **Ontwerper**. 
5. Selecteer in de structuur **Dynamics 365 for Operations'\Tabelrecords**. 
6. Klik op **Basis toevoegen**. 
7. Typ of selecteer een waarde in het veld **Tabel**. 

    > [!NOTE]
    > Er zijn nu meer dan twee toepassingstabellen aangeboden, omdat deze toewijzing alle metagegevens van de verbonden toepassing gebruikt die hieraan is toegewezen. 

8. Klik op **Annuleren**. 
9. Klik op **Valideren**. 

    > [!NOTE]
    > We hebben elementen van het gegevensmodel gebonden met items van gegevensbronnen die worden beschreven met behulp van details van metagegevens van de verbonden toepassing die is toegewezen voor deze toewijzing. 

10. Sluit de pagina. 
11. Sluit de pagina. 

Wanneer u deze modeltoewijzing wilt evalueren door metagegevens van een andere toepassingsapplicatie te gebruiken, registreert u een andere gekoppelde toepassing, wijst u deze toe aan deze modeltoewijzing en valideert u deze tegen nieuwe metagegevens.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

