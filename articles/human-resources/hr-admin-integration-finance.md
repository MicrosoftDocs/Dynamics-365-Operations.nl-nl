---
title: Integratie met Finance configureren
description: In dit artikel wordt de integratie tussen Dynamics 365 Human Resources en Dynamics 365 Finance beschreven.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8be7cbf92c11036d334516116f0895c426380954
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875853"
---
# <a name="configure-integration-with-finance"></a>Integratie met Finance configureren


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Voor de integratie van Dynamics 365 Human Resources met Dynamics 365 Finance kunt u de sjabloon Human Resources naar Finance in [Data Integrator](/powerapps/administrator/data-integrator) gebruiken. Met de sjabloon Human Resources naar Finance worden gegevensstromen voor taken, functies en werknemers ingeschakeld. Met de sjabloon kunnen gegevens stromen van Human Resources naar Finance, niet andersom.

![Integratiestroom van Human Resources naar Finance.](./media/hr-admin-integration-finance-flow.png)

De Human Resources naar Finance-oplossing biedt de volgende typen gegevenssynchronisatie:

- Taken in Human Resources onderhouden en deze synchroniseren van Human Resources naar Finance
- Posities en positietoewijzingen in Human Resources onderhouden en deze synchroniseren van Human Resources naar Finance
- Aanstellingen in Human Resources onderhouden en deze synchroniseren van Human Resources naar Finance
- Medewerkers en adressen van medewerkers in Human Resources onderhouden en deze synchroniseren van Human Resources naar Finance

## <a name="system-requirements-for-human-resources"></a>Systeemvereisten voor Human Resources

Voor de integratie-oplossing zijn de volgende versies van Human Resources en Finance vereist: 

- Dynamics 365 Human Resources in Dataverse
- Dynamics 365 Finance versie 7.2 en hoger

## <a name="template-and-tasks"></a>Sjabloon en taken

De sjabloon Human Resources naar Finance openen.

1. Open [Power Apps Beheercentrum](https://admin.powerapps.com/). 

2. Selecteer **Projecten** en vervolgens **Nieuw project** in de rechterbovenhoek. Maak een nieuw project voor elke rechtspersoon die u wilt integreren in Finance.

3. Selecteer **Human Resources (Human Resources Dataverse naar Finance)** voor het synchroniseren van records van Human Resources naar Finance.

De volgende onderliggende taken worden door de sjabloon gebruikt voor het synchroniseren van records van Human Resources naar Finance:

- **Taakfuncties naar Compensatietaakfunctie**
- **Afdelingen naar Operationele eenheid**
- **Taaktypen naar Compensatietaaktype**
- **Taken naar Taken**
- **Taken naar Taakdetails**
- **Positietypen naar Positietype**
- **Taakposities naar Basispositie**
- **Taakposities naar Positiedetails**
- **Taakposities naar Positieduren**
- **Taakposities naar Positiehiërarchieën**
- **Medewerkers naar Medewerker**
- **Aanstellingen naar Aanstelling**
- **Aanstellingen naar Aanstellingsdetails**
- **Positiemedewerkertoewijzing naar Positiemedewerkertoewijzingen**
- **Adressen van medewerkers naar Postadres van medewerker V2**

## <a name="template-mappings"></a>Sjabloontoewijzingen

In de volgende tabellen voor het toewijzen van sjablonen bevat de naam van de taak de entiteiten die in elke toepassing worden gebruikt. De bron (Human Resources) staat aan de linkerkant en de bestemming (Finance) aan de rechterkant.

### <a name="job-functions-to-compensation-job-function"></a>Taakfuncties naar Compensatietaakfunctie

| Dataverse-tabel (bron) | Finance-entiteit (bestemming) |
|-------------------------------------|---------------------------------------------|
| cdm_name (cdm_Job   Function Name)  | JOBFUNCTIONID   (JOBFUNCTIONID)            |
| cdm_description   (cdm_description) | DESCRIPTION   (DESCRIPTION)                 |

### <a name="departments-to-operating-unit"></a>Afdelingen naar Operationele eenheid

| Dataverse-tabel (bron)           | Finance-entiteit (bestemming) |
|-----------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                           | NAME (NAME)                                 |
| cdm_departmentnumber   (cdm_departmentnumber) | OPERATINGUNITNUMBER   (OPERATINGUNITNUMBER) |
|                                               | OPERATINGUNITTYPE   (OPERATINGUNITTYPE)     |
| cdm_description   (cdm_description)           | NAMEALIAS   (NAMEALIAS)                     |

### <a name="job-types-to-compensation-job-type"></a>Taaktypen naar Compensatietaaktype

| Dataverse-tabel (bron)   | Finance-entiteit (bestemming) |
|---------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                   | JOBTYPEID   (JOBTYPEID)                     |
| cdm_description   (cdm_description)   | DESCRIPTION   (DESCRIPTION)                 |
| cdm_exemptstatus   (cdm_exemptstatus) | EXEMPTSTATUS   (EXEMPTSTATUS)               |

### <a name="jobs-to-jobs"></a>Taken naar Taken

| Dataverse-tabel (bron)                           | Finance-entiteit (bestemming)           |
|---------------------------------------------------------------|-------------------------------------------------------|
| cdm_name (cdm_name)                                           | JOBID (JOBID)                                         |
| cdm_maximumnumberofpositions   (cdm_maximumnumberofpositions) | MAXIMUMNUMBEROFPOSITIONS   (MAXIMUMNUMBEROFPOSITIONS) |
| cdm_allowedunlimitedpositions   (cdm_allowunlimitedpositions) | ALLOWUNLIMITEDPOSITIONS   (ALLOWUNLIMITEDPOSITIONS)   |
| cdm_description   (cdm_description)                           | DESCRIPTION   (DESCRIPTION)                           |
| cdm_jobdescription   (cdm_jobdescription)                     | JOBDESCRIPTION   (JOBDESCRIPTIONS)                    |

### <a name="jobs-to-job-detail"></a>Taken naar Taakdetails

| Dataverse-tabel (bron)                             | Finance-entiteit (bestemming) |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                                             | JOBID (JOBID)                               |
| cdm_jobtypeid.cdm_name   (Job Type (Job Type Name))             | JOBTYPEID   (JOBTYPEID)                     |
| cdm_jobfunctionid.cdm_name   (Job Function (Job Function Name)) | FUNCTIONID   (FUCNTIONID)                   |
| cdm_validfrom   (Valid From)                                    | VALIDFROM   (VALIDFROM)                     |
| cdm_validto (Valid To)                                        | VALIDTO (VALIDTO)                           |
| cdm_defaultfulltimeequivalent   (Default Full-time Equivalent)   | FULLTIMEEQUIVALENT   (FULLTIMEEQUIVALENT)   |

### <a name="position-types-to-position-type"></a>Positietypen naar Positietype

| Dataverse-tabel (bron)       | Finance-entiteit (bestemming) |
|-------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                       | POSITIONTYPEID   (POSITIONTYPEID)           |
| cdm_description   (cdm_description)       | DESCRIPTION   (DESCRIPTION)                 |
| cdm_classification   (cdm_classification) | CLASSIFICATION   (CLASSIFICATION)           |

### <a name="job-positions-to-base-position"></a>Taakposities naar Basispositie

| Dataverse-tabel (bron)           | Finance-entiteit (bestemming) |
|-----------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (Job Position Number) | POSITIONID (POSITIONID)                      |

### <a name="job-positions-to-position-details"></a>Taakposities naar Positiedetails

| Dataverse-tabel (bron)              | Finance-entiteit (bestemming)       |
|--------------------------------------------------------------------------|---------------------------------------------------|
| cdm_jobpositionnumber  (Job Position Number)                            | POSITIONID (POSITIONID)                             |
| cdm_jobid.cdm_name   (Job (Name))                                        | JOBID (JOBID)                                    |
| cdm_description   (cdm_description)                                        | DESCRIPTION   (DESCRIPTION)                       |
| cdm_departmentid.cdm_departmentnumber   (Department (Department Number)) | DEPARTMENTNUMBER   (DEPARTMENTNUMBER)             |
| cdm_positiontypeid.cdm_name   (Position Type (Name))                     | POSITIONTYPEID   (POSITIONTYPEID)                 |
| cdm_avaialableforassignment   (Available for Assignment)                 | AVAILABLEFORASSIGNMENT   (AVAILABLEFORASSIGNMENT) |
| cdm_validfrom   (Valid From)                                            | VALIDFROM   (VALIDFROM)                           |
| cdm_validto (Valid To)                                                 | VALIDTO (VALIDTO)                               |
| cdm_fulltimeequivalent   (Full-time Equivalent)                           | FULLTIMEEQUIVALENT   (FULLTIMEEQUIVALENT)         |

### <a name="job-positions-to-position-durations"></a>Taakposities naar Positieduren

| Dataverse-tabel (bron)             | Finance-entiteit (bestemming) |
|-------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (Job Position Number)   | POSITIONID (POSITIONID)                      |
| Calculated   Activation (Calculated Activation) | VALIDFROM (VALIDFROM)                        |
| Calculated   Retirement (Calculated Retirement) | VALIDTO (VALIDTO)                         |

### <a name="job-positions-to-position-hierarchies"></a>Taakposities naar Positiehiërarchieën

| Dataverse-tabel (bron)        | Finance-entiteit (bestemming) |
|-----------------------------------------------------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (Job Position Number)                                                 | POSITIONID(POSITIONID)                      |
| cdm_parentjobpositionid.cdmjobpositionnumber   (cdm_parentjobpositionid.cdmjobpositionnumber) | PARENTPOSITIONID (PARENTPOSITIONID)         |
| cdm_validfrom   (Valid From)                                                                  | VALIDFROM   (VALIDFROM)                     |
| cdm_validto (Valid   To)                                                                      | VALIDTO (VALIDTO)                           |
| HIERARCHYTYPENAME   (HIERARCHYTYPENAME)                                                       | HIERARCHYTYPENAME   (HIERARCHYTYPENAME)     |


### <a name="workers-to-worker"></a>Medewerkers naar Medewerker
| Dataverse-tabel (bron)           | Finance-entiteit (bestemming)       |
|-----------------------------------------------|---------------------------------------------------|
| cdm_birthdate   (cdm_birthdate)               | BIRTHDATE   (BIRTHDATE)                           |
| cdm_gender   (cdm_gender)                     | GENDER (GENDER)                                   |
| cdm_primaryaddress   (cdm_primaryaddress)     | PRIMARYCONTACTEMAIL   (PRIMARYCONTACTEMAIL )      |
| cdm_primarytelephone   (cdm_primarytelephone) | PRIMARYCONTACTPHONE   (PRIMARYCONTACTPHONE)       |
| cdm_facebookidentity   (cdm_facebookidentity) | PRIMARYCONTACTFACEBOOK   (PRIMARYCONTACTFACEBOOK) |
| cdm_twitteridentity   (cdm_twitteridentity)   | PRIMARYCONTACTTWITTER   (PRIMARYCONTACTTWITTER)   |
| cdm_linkedinIdentity   (cdm_linkedinIdentity) | PRIMARYCONTACTLINKEDIN   (PRIMARYCONTACTLINKEDIN) |
| cdm_websiteurl   (cdm_websiteurl)             | PRIMARYCONTACTURL   (PRIMARYCONTACTURL)           |
| cdm_firstname   (cdm_firstname)               | FIRSTNAME   (FIRSTNAME)                           |
| cdm_middlename   (cdm_middlename)             | MIDDLENAME   (MIDDLENAME)                         |
| cdm_lastname   (cdm_lastname)                 | LASTNAME (LASTNAME)                               |
| cdm_workernumber   (cdm_workernumber)         | PERSONNELNUMBER   (PERSONNELNUMBER)               |
| cdm_type (cdm_type)                           | WORKERTYPE   (WORKERTYPE)                         |
| cdm_state   (cdm_state)                       | WORKSTATUS   (WORKERSTATUS)                       |

### <a name="employments-to-employment"></a>Aanstellingen naar Aanstelling

| Dataverse-tabel (bron)                             | Finance-entiteit (bestemming) |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_employmentstartdate   (cdm_employmentstartdate)             | EMPLOYMENTSTARTDATE   (EMPLOYMENTSTARTDATE) |
| cdm_employmentenddate   (cdm_employmentenddate)                 | EMPLOYMENTENDDATE   (EMPLOYMENTENDDATE)     |
| cdm_workertype   (cdm_workertype)                               | WORKERTYPE   (WORKERTYPE)                   |
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)         |
| cdm_companyid.cdm_companycode   (cdm_companyid.cdm_companycode) | LEGALENTITYID   (LEGALENTITYID)             |

### <a name="employments-to-employment-detail"></a>Aanstellingen naar Aanstellingsdetails

| Dataverse-tabel (bron)                             | Finance-entiteit (bestemming)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_employmentstartdate   (cdm_employmentstartdate)             | EMPLOYMENTSTARTDATE   (EMPLOYMENTSTARTDATE)   |
| cdm_employmentenddate   (cdm_employmentenddate)                 | EMPLOYMENTENDDATE   (EMPLOYMENTENDDATE)       |
| cdm_validfrom   (Valid From)                                    | VALIDFROM   (VALIDFROM)                       |
| cdm_validto (Valid   To)                                        | VALIDTO (VALIDTO)                             |
| cdm_workerstartdate   (cdm_workerstartdate)                     | WORKERSTARTDATE   (WORKERSTARTDATE)           |
| cdm_lastdateworked   (cdm_lastdateworked)                       | LASTDATEWORKED   (LASTDATEWORKED)             |
| cdm_transitiondate   (cdm_transitiondate)                       | TRANSITIONDATE   (TRANSITIONDATE)             |
| cdm_employerunitofnotice   (cdm_employerunitofnotice)           | EMPLOYERUNITOFNOTICE   (EMPLOYERUNITOFNOTICE) |
| cdm_workerunitofnotice   (cdm_workerunitofnotice)               | WORKERUNITOFNOTICE   (WORKERUNITOFNOTICE)     |
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_companyid.cdm_companycode   (cdm_companyid.cdm_companycode) | LEGALENTITYID   (LEGALENTITYID)               |
| cdm_employernoticeamount   (cdm_employernoticeamount)           | EMPLOYERNOTICEAMOUNT   (EMPLOYERNOTICEAMOUNT) |
| cdm_workernoticeamount   (cdm_workernoticeamount )              | WORKERNOTICEAMOUNT   (WORKERNOTICEAMOUNT)     |

### <a name="position-worker-assignment-to-position-worker-assignments"></a>Positiemedewerkertoewijzing naar Positiemedewerkertoewijzingen

| Dataverse-tabel (bron)                             | Finance-entiteit (bestemming)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_jobpositionnumber   (Job Position Number)                   | POSITIONID(POSITIONID)                        |
| cdm_validfrom   (Valid From)                                    | VALIDFROM   (VALIDFROM)                       |
| cdm_validto (Valid To)                                        | VALIDTO (VALIDTO)                             |

### <a name="worker-addresses-to-worker-postal-address-v2"></a>Adressen van medewerkers naar Postadres van medewerker V2

| Dataverse-tabel (bron)                             | Finance-entiteit (bestemming)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_addresstype   (cdm_addresstype)                             | ADDRESSLOCATIONROLES   (ADDRESSLOCATIONROLES) |
| cdm_line1   (cdm_line1)                                         | ADDRESSSTREET   (ADDRESSSTREET)               |
| cdm_city (cdm_city)                                             | ADDRESSCITY   (ADDRESSCITY)                   |
| cdm_stateorprovince   (cdm_stateorprovince)                     | ADDRESSSTATE   (ADDRESSSTATE)                 |
| cdm_postalcode   (cdm_postalcode)                               | ADDRESSZIPCODE(ADDRESSZIPCODE)                |
| cdm_countryregion   (cdm_countryregion)                         | ADDRESSCOUNTRYREGION(ADDRESSCOUNTRYREGION)    |
| cdm_addressnumber   (cdm_addressnumber)                         | ADDRESSLOCATIONID(ADDRESSLOCATIONID)          |
| cdm_ispreferred   (cdm_ispreferred)                             | ISPRIMARY   (ISPRIMARY)                       |
| cdm_county   (cdm_county)                                       | ADDRESSCOUNTYID(ADDRESSCOUNTYID)              |
| cdm_addresstype   (cdm_addresstype)                             | ADDRESSDESCRIPTION(ADDRESSDESCRIPTION)        |

## <a name="integration-considerations"></a>Overwegingen bij integratie

Bij de integratie van gegevens van Human Resources in Finance wordt een poging gedaan om records te koppelen op basis van hun id. Als de records overeenkomen, worden de gegevens in Finance overschreven door de waarden in Human Resources. Een probleem kan echter optreden als de records logisch gezien van elkaar verschillen en hun id is gegenereerd in Human Resources of Finance op basis van hun desbetreffende nummerreeks.

Dit probleem kan zich voordoen met **Medewerker**, waarvoor **Personeelsnummer** wordt gebruikt om overeenkomende records te vinden, en **Posities**. Voor taken worden geen nummerreeksen gebruikt. Het resultaat hiervan is dat als dezelfde taak-id aanwezig is in zowel Human Resources als Finance, de Dynamics 365 Finance-informatie wordt overschreven door de Human Resources-informatie. 

Om problemen met dubbele id's te voor komen, kunt u een voorvoegsel toevoegen aan de [nummerreeks](/dynamics365/unified-operations/fin-and-ops/organization-administration/number-sequence-overview?toc=%2fdynamics365%2funified-operations%2ftalent%2ftoc.json) of een beginnummer instellen voor de nummerreeks die buiten het bereik van het andere systeem valt. 

De locatie-id die wordt gebruikt voor het werknemersadres, maakt geen deel uit van een nummerreeks. Wanneer een werknemersadres uit Human Resources wordt geïntegreerd in Finance, kan er een dubbele adresrecord worden gemaakt als het werknemersadres al bestaat in Finance. 

In de volgende afbeelding ziet u een voorbeeld van een sjabloontoewijzing in de Data Integrator. 

![Sjabloontoewijzing.](./media/IntegrationMapping.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
