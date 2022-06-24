---
title: Klantcertificaten en -geheimen
description: In dit artikel wordt uitgelegd hoe u klantcertificaten en -geheimen voor elektronische facturering instelt.
author: dkalyuzh
ms.date: 02/07/2022
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
ms.openlocfilehash: a4d33135bf352a4c4a245e597e0c3c7467317864
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880655"
---
# <a name="customer-certificates-and-secrets"></a>Klantcertificaten en -geheimen

[!include [banner](../includes/banner.md)]

Als u al een Microsoft Azure Key Vault-referentie in Regulatory Configuration Service (RCS) hebt, kunt u verwijzingen maken naar de Key Vault-certificaten en -geheimen. Als u nog geen Key Vault-referentie hebt, leest u in [Service-omgevingen](e-invoicing-service-environments.md) hoe u deze maakt.

## <a name="create-certificates-and-secrets"></a>Certificaten en geheimen maken

Voer deze stappen uit om certificaten en geheimen te maken en in te stellen.

1. Meld u aan bij uw RCS-account.
2. Selecteer in de werkruimte **Globalisatiefunctie** in de sectie **Omgeving** de tegel **Elektronische facturering**.
3. Selecteer op de pagina **Omgevingsinstellingen** in het actievenster de optie **Serviceomgevingen**.
4. Selecteer op de pagina **Serviceomgevingen** in het actievenster de optie **Key Vault-parameters**.
5. Selecteer op de pagina **Key Vault-parameters** een Key Vault-verwijzing en vervolgens **Toevoegen** in de sectie **Certificaten**.
6. Voer in het veld **Naam** de naam in voor het Key Vault-certificaat of -geheim. Zie [Een Azure Key Vault-opslagaccount maken in de Azure Portal](e-invoicing-create-azure-storage-account-azure-portal.md) voor meer informatie.
7. Voer in het veld **Beschrijving** een beschrijving in.
8. Selecteer in het veld **Type** de optie **Certificaat** als u verwijst naar het certificaat dat is opgeslagen in de sleutelkluis. Selecteer **Geheim** als u verwijst naar het geheim dat is opgeslagen in de sleutelkluis.
9. Selecteer **Opslaan**.

> [!NOTE]
> In sommige scenario's moet u openbare certificaten gebruiken met de bestandsextensie .cer. Het importeren en opslaan van certificaten van dit type wordt echter niet ondersteund voor Key Vault-certificaten. In deze scenario's moet u het .cer-bestand opslaan als een Base-64-encoded X.509 (.CER) string. Sla vervolgens in het Key Vault-certificaat de tekenreeks op die tussen de regel **BEGIN CERTIFICAAT** en **EINDCERTIFICAAT** in het bestand wordt weergegeven. In de serviceomgeving moet u nog steeds een verwijzing maken naar de Key Vault-record en het veld **Type** instellen op **Certificaat**.

## <a name="create-a-chain-of-certificates"></a>Een reeks certificaten maken

Als voor uw land-/regiospecifieke facturen een reeks certificaten nodig is om digitale handtekeningen toe te passen of om een beveiligde (Secure Sockets Layer \[SSL\])-verbinding met externe webservices tot stand te brengen, maakt u een reeks certificaten in de volgende volgorde:

1. Basiscertificaten
2. Tussenliggende certificaten
3. Certificaten van eindgebruikers

Basiscertificaatinstanties (CAs) zijn een vertrouwde bron van certificaten. Tussenliggende CA-certificaten zijn bruggen die de eindgebruikercertificaten aan de CA-basiscertificaten koppelen.

Voer deze stappen uit om een reeks certificaten te maken en in te stellen.

1. Selecteer op de pagina **Key Vault-parameters** in het actievenster de optie **Keten van certificaten**.
2. Selecteer **Nieuw** om een keten certificaten te maken.
3. Voer in het veld **Naam** de naam in voor de certificaatketen.
4. Voer in het veld **Beschrijving** een beschrijving in.
5. Selecteer in het gedeelte **Certificaten** de oiptie **Toevoegen** om een certificaat aan de keten toe te voegen.
6. Met de knop **Omhoog** of **Omlaag** kunt u de positie van het certificaat in de keten wijzigen. Houd het CA-basiscertificaat bovenaan de lijst en het eindgebruikscertificaat onderaan.
7. Selecteer **Opslaan**.

U kunt zoveel Key Vault-verwijzingen in RCS maken als u wilt. Houd er rekening mee dat het geheim voor het SAS-token (Storage Shared Access Signature) wordt gebruikt om een bepaalde serviceomgeving te koppelen aan de Key Vault-referentie. U kunt verwijzen naar de Key Vault-certificaten en -geheimen die zijn opgeslagen in een sleutelkluis die ook het geheim voor het SAS-token bevat dat u gebruikt bij het instellen van de serviceomgeving.
