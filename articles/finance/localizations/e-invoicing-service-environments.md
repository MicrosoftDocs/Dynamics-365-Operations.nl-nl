---
title: Serviceomgevingen
description: In dit artikel vindt u informatie over serviceomgevingen voor elektronische facturering en uitleg over het instellen ervan.
author: dkalyuzh
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8c743c5b2fbc7dcc3ae04fa4d7ca0e65de6c2507
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901242"
---
# <a name="service-environments"></a>Serviceomgevingen

[!include [banner](../includes/banner.md)]

Serviceomgevingen zijn logische partities die worden aangemaakt om de uitvoering van de globalisatiefuncties en de bijbehorende documenten die worden verwerkt in de Elektronische factureringsservice te ondersteunen. De beveiligingsrechten, digitale certificaten en de toegangsmachtigingen (governance) moeten worden geconfigureerd op het niveau van de serviceomgeving.

U kunt zoveel serviceomgevingen maken als nodig zijn. Alle serviceomgevingen die u maakt, zijn onafhankelijk van elkaar. Het is raadzaam om minimaal twee serviceomgevingen te maken:

- Eén omgeving voor hoofdontwikkelings- en validatiedoeleinden. Deze omgeving is meestal een UAT-omgeving (user acceptance testing).
- Eén omgeving voor productiedoeleinden. Deze omgeving is meestal een productieomgeving.

Met dit type partitionering zorgt u ervoor dat de e-factureringsprocessen worden gevalideerd en aangepast in de sandbox voordat ze naar de productie gaan.

Serviceomgevingen moeten worden gemaakt en beheerd in Regulatory Configuration Service (RCS). Wanneer ze gereed zijn, moeten ze worden gepubliceerd in de Elektronische factureringsservice. Het publicatieproces stuurt de parameters van de serviceomgeving van het RCS-exemplaar naar de Elektronische factureringsservice.

Als u het publicatieproces niet voltooit nadat u een nieuwe serviceomgeving hebt gemaakt of als u een bestaande serviceomgeving hebt aangepast (bijvoorbeeld door gebruikers of geheimen voor Microsoft Azure Key Vault toe te voegen of te verwijderen), zijn de wijzigingen niet geldig. Alleen gepubliceerde omgevingen zijn toegankelijk voor Dynamics 365 Finance of Dynamics 365 Supply Chain Management.

## <a name="service-environment-statuses"></a>Statussen van serviceomgevingen

Serviceomgevingen kunnen worden beheerd via de status. U kunt de status van een omgeving bekijken op de pagina **Serviceomgevingen**. De volgende statussen zijn beschikbaar:

- **Niet gepubliceerd**: de omgeving is gemaakt, maar nog niet gepubliceerd.
- **Gepubliceerd**: de omgeving is gepubliceerd in de Elektronische factureringsservice.
- **Gewijzigd**: de kenmerken van een gepubliceerde omgeving zijn gewijzigd, maar de wijzigingen zijn nog niet gepubliceerd.

## <a name="users"></a>Gebruikers

Elke serviceomgeving moet een lijst maken met de gebruikers die vanuit Finance od Supply Chain Management verbinding kunnen maken met Elektronische facturering.

## <a name="applications"></a>Aanvragen

In sommige scenario's moeten andere toepassingen dan Finance of Supply Chain Management mogelijk verbinding maken met de elektronische factureringsservice om elektronische documenten in te dienen voor verdere verwerking of om informatie op te halen, zoals de indieningsstatus van een document. In deze scenario's moet de toepassing worden gedefinieerd in de lijst met toepassingen. Op deze manier heeft deze service toegang tot de Elektronische factureringsservice. De toepassing moet ook als een toepassing worden geregistreerd in Azure Active Directory (Azure AD) en de object-id moet worden gebruikt om deze te identificeren. 

Omdat Microsoft een hoog beveiligingsniveau vereist voor toepassingen die verbinding kunnen maken met de elektronische factureringsservice, moet u contact opnemen met Microsoft op <DGXRegulatoryservicesengineering@service.microsoft.com> en de volgende gegevens van uw toepassing verstrekken:

- Id Azure AD-tenant
- Omgevings-id van Microsoft Dynamics Lifecycle Services (LCS)
- Toepassings-id (client-id)
- Object-id
- Rechtvaardiging en omschrijving op hoog niveau van de toepassing

Microsoft zal de aanvraag beoordelen en de toepassing registreren in het beveiligingsregister om ervoor te zorgen dat deze kan werken met Elektronische facturering.

## <a name="number-sequences"></a>Nummerreeksen

Als uw scenario's nummerreeksen vereisen (bijvoorbeeld in bestandsnamen), kunt u nummerreeksen gebruiken die voor een specifieke omgeving zijn gedefinieerd, maar die in alle globalisatiefuncties of voor een specifieke globalisatiefunctie kunnen worden gebruikt. Nadat een nummerreeks is gedefinieerd, kunt u deze gebruiken in variabelen en het verwerken van pijplijnen. Als u het gebruik ervan wilt bijhouden, gaat u op de pagina **Nummerreeksen** naar de waarde **Huidig** voor de parameter **In gebruik**.

### <a name="working-with-number-sequences"></a>Werken met nummerreeksen
Op de pagina **Nummerreeksen**: 

- Selecteer **Nieuw** om een nummerreeks te maken. Voer vervolgens een naam en omschrijving in. 
- Selecteer **Verwijderen** om een nummerreeks te verwijderen als deze niet meer wordt gebruikt.
- U hoeft het selectievakje **Publiceren** in het actievenster niet te selecteren om de wijzigingen in een nummerreeks te publiceren. De bijwerking vindt automatisch plaats.

## <a name="create-a-key-vault-reference"></a>Key Vault-verwijzing maken

1. Meld u aan bij uw RCS-account.
2. Selecteer in de werkruimte **Globalisatiefunctie** in de sectie **Omgeving** de tegel **Elektronische facturering**.
3. Selecteer op de pagina **Omgevingsinstellingen** in het actievenster de optie **Serviceomgevingen**.
4. Selecteer op de pagina **Serviceomgevingen** in het actievenster de optie **Key Vault-parameters**.
5. Selecteer op de pagina **Sleutelkluisparameters** de optie **Nieuw** om een Key Vault-verwijzing te maken.
6. Voer in het veld **Naam** de naam in voor de Key Vault-verwijzing.
7. Voer in het veld **Beschrijving** een beschrijving in.
8. Plak in het veld **Key Vault-URI** de Key Vault-URI uit de sleutelkluis (`https://<your key vault>.vault.azure.net/`). Zie [Een Azure Key Vault maken in de Azure Portal](e-invoicing-create-azure-key-vault-azure-portal.md) voor meer informatie.
9. Selecteer **Opslaan**.
    
## <a name="create-a-secret-for-the-storage-account-secret-token"></a>Een geheim maken voor het geheime token van het opslagaccount

1. Selecteer op de pagina **Key Vault-parameters** de Key Vault-verwijzing die u hebt gemaakt in de vorige procedure en selecteer vervolgens **Toevoegen** in de sectie **Certificaten**.
2. Voer in het veld **Naam** de naam in voor het opslagaccountgeheim. Deze naam moet overeenkomen met de naam van het Key Vault-geheim dat de SAS-token (Storage Shared Access Signature) bevat. Zie [Een Azure Key Vault-opslagaccount maken in de Azure Portal](e-invoicing-create-azure-storage-account-azure-portal.md) voor meer informatie. 
3. Voer in het veld **Beschrijving** een beschrijving in.
4. Selecteer in het veld **Type** de optie **Geheim**.
5. Selecteer **Opslaan**.
    
## <a name="create-a-service-environment"></a>Een serviceomgeving maken

1. Selecteer op de pagina **Service-omgevingen** de optie **Nieuw** om een serviceomgeving te maken.
2. Voer in het veld **Naam** de naam in voor de omgeving voor elektronische facturering.
3. Voer in het veld **Beschrijving** een beschrijving in.
4. Selecteer in het veld **Opslag SAS-tokengeheim** de naam van het opslagaccountgeheim dat moet worden gebruikt om toegang tot het opslagaccount te verifiëren.
5. In de sectie **Gebruikers** selecteert u **Toevoegen** om een gebruiker toe te voegen die elektronische facturen via de omgeving mag indienen en verbinding mag maken met het opslagaccount.
6. Voer in het veld **Gebruikers-id** het alias van de gebruiker in. 
7. Voer in het veld **E-mail** het e-mailadres van de gebruiker in.
8. Selecteer **Opslaan**.
9. Selecteer **Publiceren** in het actievenster om de omgeving naar de elektronische factureringsservice te publiceren. Controleer of de waarde van het veld **Status** wordt gewijzigd in **Gepubliceerd**.
