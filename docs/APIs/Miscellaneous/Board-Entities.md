# Board Entities

This API is used to add Customer Name/Address record, Account Base Segment record, Embosser record, and Relationship record and Insurance record based on the input criteria.

Fields that are not provided in the Request object will be initialized to their default values. All numeric fields are initialized to zero and alphanumeric fields initialized to spaces.

## Endpoint

`POST /v1/misc/boardEntities`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json

{
  "accountId": "/",
  "isCustomerIdEnabled": "Y",
  "createAccountRecord": "Y",
  "isSameCustomerIdAccountIdEnabled": "N",
  "isRelationshipEnabled": "N",
  "isPaymentInstrumentIdEnabled": "Y",
  "businessUnit": 600,
  "productId": 1,
  "customerId": "/",
  "relationshipNumber": "",
  "isInsuranceProductEnabled": "N",
  "customerDemographicDetails": {
    "dualFlag": "0",
    "title": "",
    "nameTypeIndicator1": "0",
    "nameTypeIndicator2": "0",
    "nameTypeIndicator3": "0",
    "residenceFlag": "1",
    "homePhone": "11230342",
    "employeePhone": "67894",
    "birthDate": "01/02/2010",
    "externalId": "",
    "gender": "1",
    "emailAddress": "",
    "alternateEmailAddress": "",
    "mobileNumber": "",
    "emailAddressFlag": "0",
    "addressDetails": {
      "addressLine1": "",
      "addressLine2": "",
      "addressLine3": "",
      "addressLine4": "",
      "city": "",
      "state": "",
      "postalCode": "",
      "countryCode": ""
    },
    "nameDetails": {
      "nameLine1": "",
      "nameLine2": "",
      "nameLine3": "",
      "birthName": "",
      "middleName": "",
      "givenName": "Tom"
    }
  },
  "relationshipDetails": {
    "relationshipCreditLimit": "0.00",
    "relationshipBlockCode": " ",
    "mailCode": "0",
    "reserveAmountpctFlag": "0",
    "availableReservePctAmount": "0.00",
    "isStatememtTypeEnabled": "0",
    "accountControlTableOverride": 0,
    "relationshipLevelBillingCycle": 0,
    "billingLevel": "1",
    "isBillingLevelModificationEnabled": "0",
    "defaultCreditLimit": "0.00",
    "isCreditLimitModificationEnabled": "0",
    "corporateCustomerId": "",
    "customerGroupCode": "",
    "costCenterReportingNumber": "",
    "fiscalYearEnd": 0,
    "currentExpiryDate": "00/00/0000",
    "sourceCode": "",
    "contactName": "",
    "contactPhone": "",
    "officerName": "",
    "commercialFlag": "0",
    "authorizationCriteriaTable": "",
    "memoDetails": {
      "billingCurrency": 0,
      "paymentTransactionCode": 0,
      "paymentReversalTransactionCode": 0,
      "balanceIndicator": "0"
    },
    "feeDetails": {
      "annualFeeAssessmentLevel": "0",
      "isAnnualFeeModificationEnabled": "0",
      "lateFeeAssessmentLevel": "0",
      "isLateFeeModificationEnabled": "0",
      "nsfFeeAssessmentLevel": "0",
      "isNsfFeeModificationEnabled": "0"
    },
    "userDetails": {
      "userDate1": "00/00/0000",
      "userDate2": "00/00/0000",
      "userAmount1": "0.00",
      "userAmount2": "0.00",
      "userField5": "",
      "userField6": ""
    }
  },
  "accountDetails": {
    "accountDirectDebitDetails": {
      "accountType": "D",
      "customerName": "Alex Rey",
      "externalAccountId": "00000001000000057",
      "nominatedPaymentAmountOrPercentage": "$10.00",
      "nominatedType": 1,
      "paymentChangeDate": "04/10/2021",
      "paymentExpiryDate": "04/11/2021",
      "paymentRemittanceMethod": 2,
      "paymentStartDate": "04/10/2021",
      "paymentType": 1,
      "requestDays": 4,
      "routingBankID": "123456"
    },
    "corporateId": "",
    "primaryAccountFlag": " ",
    "shortName": "",
    "creditLimit": "10.00",
    "billingLevel": "1",
    "dualBillingFlag": "0",
    "customerSelectedDueDay": 0,
    "billingCycle": 18,
    "residenceId": "",
    "issuanceId": " ",
    "cashPlanId": 0,
    "retailPlanId": 0,
    "cardTechnology": "0",
    "temporaryCreditLimit": "0.00",
    "temporaryCreditLimitExpiryDate": "00/00/0000",
    "owningBranchNumber": 999999998,
    "isMobilePiEnabled": "0",
    "authorizationCriteriaTable": "",
    "isSuppressLetterEnabled": "0",
    "isWaiveAnnualMembershipFeeEnabled": "0",
    "isSupressTokenEnabled": "0",
    "coreBankingIndicator": " ",
    "pctOverrideDetails": {
      "pctOverride": " ",
      "pctOverrideStartDate": "00/00/0000",
      "pctOverrideExpiryDate": "00/00/0000",
      "level": " ",
      "levelStartDate": "00/00/0000",
      "levelExpiryDate": "00/00/0000"
    },
    "ibsDetails": {
      "ddaRoutingId": 0,
      "ddaAccountId": "",
      "savingsRoutingId": 0,
      "savingsAccountId": ""
    },
    "externalContractId": "0000000000012672379",
    "addressId": "HOME",
    "sourceCode": " ",
    "statementDeliveryMode": "E",
    "bnplDetails": {
      "configurationTemplate": "BNPL01TRAN",
      "preferredDayOfWeek": 1,
      "defaultRepaymentReferenceIndicator": 0,
      "alerts": {
        "bookingAlertChannelIndicator": 0,
        "iplanActivationAlertChannelIndicator": 0,
        "paymentDueAlertChannelIndicator": 0,
        "missedPaymentAlertChannelIndicator": 0,
        "switchAlertChannelIndicator": 0,
        "snoozeAlertChannelIndicator": 0
      },
      "directDebitDetails": {
        "externalAccountsBankId": "1234",
        "routingBankId": "01",
        "externalAccountType": "D",
        "externalAccountId": "14725836978945612",
        "paymentStartDate": "01/01/2031",
        "paymentExpiryDate": "01/01/2032",
        "internationalBankingAccountId": "12345",
        "bankIdentifierCode": "12345678912",
        "paymentCardNumberExpiryDate": 1036,
        "paymentCardNumber": "9123900123789012",
        "paymentType": 1,
        "repaymentType ": 0
      }
    }
  },
  "accountInsuranceProductDetails": {
    "dualIndicator": " ",
    "productCode": "",
    "statusCode": " ",
    "effectiveDate": "00/00/0000",
    "enrollId": "",
    "insuredPartyIndicator": "0",
    "premiumRate": 0,
    "ficheNumber": "",
    "source": "",
    "cancelReason": " ",
    "isMailLetterEnabled": "0",
    "isMailLetterFeeEnabled": "0",
    "mailStatement": "0"
  },
  "cardDetails": {
    "paymentInstrumentId": "/",
    "cardAction": "1",
    "numberOfCardsRequested": 0,
    "cardType": 0,
    "requestedCardType": 0,
    "cardMailerType": 0,
    "plasticId": "",
    "name1TypeIndicator": "0",
    "name2TypeIndicator": "0",
    "posServiceCode": 0,
    "cardholderFlag": "1",
    "visaMiniIndicator": "0",
    "programId": 0,
    "mobileDeviceId": "",
    "mobileProvisionStatus": "0",
    "deviceIndicator": "0",
    "mccGroupLimits": 0,
    "chequeAccountId": "",
    "savingAccountId": "",
    "cardNameDetails": {
      "embossedName1": "Trump",
      "embossedName2": "",
      "name1": "",
      "name2": ""
    },
    "cardAddressDetails": {
      "addressLine1": "",
      "addressLine2": "",
      "city": "",
      "stateprovince": "",
      "postalCode": "",
      "addressId": " "
    },
    "physicalVirtualIndicator": "P",
    "isDynamicCVV2Enabled": "0",
    "externalContractId": "0000000000012672379"
  }
}
```

<!--
type: tab
-->

```json
{
  "businessUnit": 600,
  "productId": 1,
  "customerId": "0006000012000000191",
  "relationshipId": "",
  "accountId": "0006000012000000191",
  "cardDetails": {
    "paymentInstrumentId": "0004440010910990851",
    "nameOnCard": "Trump",
    "expiryDate": "18/01/2024",
    "activationStatus": "0",
    "maskedPaymentCardNumber": ""
  }
}
```

<!--
type: tab
-->

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "440401",
    "instance": "/v1/misc/boardEntities",
    "invalid-params": [
        "V5S84154SB: CUSTOMER NUMBER ALREADY EXISTS FOR THIS ORG",
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/misc/boardEntities).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Payload | *string* | 19 | Unique identification number for cardholder billing account. |
| `isCustomerIdEnabled` | Payload | *string* | 01 | This is the code that indicates whether to add a new customer record. |
| `createAccountRecord` | Payload | *string* | 01 | This is the code that indicates whether to add a new account record. |
| `isSameCustomerIdAccountIdEnabled` | Payload | *string* | 01 | This is the code that indicates whether CUSTOMER NUMBER and BASE ACCOUNT NUMBER are to be the same number. |
| `isRelationshipEnabled` | Payload | *string* | 01 | This is the code that indicates whether to add a new Relationship record. |
| `isPaymentInstrumentIdEnabled` | Payload | *string* | 01 | This is the code that indicates whether to add a new Embosser record. |
| `businessUnit` | Payload | *number* | 03 | Identification number of the business unit associated with the  account. |
| `productId` | Payload | *number* | 03 | Identification number of the product associated with the account or relationship. |
| `customerId` | Payload | *string* | 19 | Unique identification number assigned to a customer. |
| `isInsuranceProductEnabled` | Payload | *string* | 01 | This is the code that indicates whether to add an Insurance Product record. |
| `givenName` | Payload | *string* | 40 | First name of the customer. |
| `creditLimit` | Payload | *string* | 17 | Credit limit of this account. |
| `cardAction` | Payload | *string* | 1 | This field is the card issue action code that determines the action CMS performs during the next run. |
| `addressId` | Payload | *string* | 15 | Address identifier to determine the type of address. Ex: Home, Office, etc. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5S84003EA` | Base account number required |
| `V5S84003EG` | Base account number must be numeric |
| `V5S84005EA` | Customer NA account must be blank |
| `V5S84003EA/V5S84003EE` | Base account number required |
| `V5S84150EE` | Customer NA account and base account are equal |
| `V5S84005EB` | Customer NA account required |
| `V5S84005EG` | Customer NA account must be blank |
| `V5S84003EG` | Base account number must be numeric |
| `V5S84150EG` | Customer NA account and base account are equal |
| `V5S84005EH` | Customer NA account must be numeric |
| `V5S84003EH` | Base account number required |
| `V5S84009EA` | Relationship number required |
| `V5S84154EC` | Relationship number cannot equal customer or account number |
| `V5S84154SA` | Customer number not on file for this org |
| `V5S84154SB` | Customer number already exists for this org |
| `V5S84156EA` | Relationship number already exists for this org |
| `V5S84156EC` | Relationship number cannot equal account number for this org |
| `V5S84156ED` | Relationship number cannot equal customer number for this org |
| `V5S84156EE` | Relationship not on file for this org or relationship number |
| `V5S84156EG` | Relationship already exist for this org or relationship number |
| `V5S84156EJ` | Relationship number cannot be same as existing customer number |
| `V5S84156EL` | Relationship cannot be same as existing account for this org |
| `V5S84157EA` | Base account number already exists for this org |
| `V5S84157EC` | Account nbr exist on relationship file for this org |
| `V5S84158EA` | Account nbr cannot duplicate existing embosser for this org |
| `V5S84151EE` | Maximum number of 20 attempts made on base account number |
| `V5S84152EC` | Maximum number of 20 attempts made on customer number |
| `V5S84152EE` | Generated relationship number is less than beginning range |
| `V5S84162SB` | DDA/savings routing information is required |
| `V5S89909SA` | CCID should not be spaces or zeroes |
| `V5S89910SA` | Address id should not be spaces or zeroes |
| `V5S89516SB` | ACCT CCID should contain only alphanumeric |
| `V5S89517SB` | ACCT addrid should contain only alphanumeric chars and '-' |
| `V5S89519SA` | Card CCID should contain only alphanumeric |
| `V5S89518SB` | Card addrid should contain only alphanumeric chars and '-' |
| `V5S84004SK` | CGID/customer number should be numeric |
| `V5NA0419ED` | Email cont ind not active |
| `V5NA0333EE/V5NA0419EE` | SMS ind not active |
| `V5NA0419EF` | Email cont ind not active |
| `V5NA4002EB` | Nbr already exists on relationship file |
| `V5NA0332EA` | Mobile number is required when SMS ind flag is 1 |
| `V5NA0333EA/V5NA0333EB/V5NA0333EC` | Mobile number not found |
| `V5NA0333ED` | Mobile number required |
| `V5NA0419EA/V5NA0419EB/V5NA0419EC` | Email address not found |
| `V5NA4001SI` | Org does not allow cust nbr generation |
| `V5NA4001SJ` | Max nbr of 20 attempts made on cust nbr |
| `V5NA4001SK` | Customer number generation error |
| `V5NA4001SL` | Generated cust nbr is greater than ending cust nbr |
| `V5NA4002SA` | AMNA - account not found |
| `V5NA4002SB` | AMNA - account is in add pending |
| `V5NA0519EB` | End date must be greater than start date |
| `V5NA9901EX` | Field not maintaiNAble when name type ind > 0 |
| `V5NA0202EA` | Either of first/middle/last name is required for maker |
| `V5NA0327EA` | Home phone is required when call ind flag is 1 |
| `V5NA0330EA` | Fax phone is required when fax ind flag is 1 |
| `V5NA0333EH` | Mobile number is required when call ind flag is 1 |
| `V5NA0414EA` | Employer phone required when work phone flag is 1 |
| `V5NA0419EG` | Email id is required when mail ind flag is 1 |
| `V5NA4081EA` | First name is required |
| `V5A34058SB` | Customer number not found |
| `V5BS0102SA` | 004Customer number cannot be zeros |
| `V5BS0102SB` | 095Generic customer not allowed |
| `V5BS0102SC` | 005No active customer on file |
| `V5BS0103SA` | Crlim not maint if AMRM-clm-sub-not-allowed |
| `V5BS0103SC` | 006Cannot be greater than logo credit limit |
| `V5BS0103SD` | Credit limit exceeds secured amount use armd |
| `V5BS0103SY` | Cannot be greater than parent node avail credit limit |
| `V5BS0103SZ` | Cannot be greater than company node avail credit limit |
| `V5BS0110EC` | Cannot use chgoff rsn defined in logo lvl for chgoff sta'2' |
| `V5BS0111SB` | 095Generic customer not allowed |
| `V5BS0111SC` | 015No active customer rec on file |
| `V5BS0125SB/V5BS0127SB` | 022Must be alphabetic |
| `V5BS0148SA` | 032Requested statement not found |
| `V5BS0148SB` | 033Cannot print recap statement |
| `V5BS0152EA` | 065Field entry is required for rtn mail user |
| `V5BS0156SA` | 056Acct billing lvl cannot be 0,when rel bill lvl is 1 |
| `V5BS0156SB` | 060Billing level must be 0 or 1 |
| `V5BS0156SC` | 057Prim ACCT billing lvl cannot be 1,when rel bill lvl is 0 or 2 |
| `V5BS0156SD` | 058Billing level for primary account cannot be changed to a 1 |
| `V5BS0156SE` | Billing level cannt b changed to 1 when ACCT payment due is > 0 |
| `V5BS0156SF` | Rel nbr cannot be all # when payment due is > 0 or bill lvl = 0 |  
| `V5BS0160SA` | 054Cannot chargeoff account with 0 bal or credit bal |
| `V5BS0162SB` | Primary ACCT already setup for relationship number |
| `V5BS0163EA` | Relationships not activated on org ctrl record |
| `V5BS0163ED` | No relationship record exists |
| `V5BS0163EE` | Relationship record in add-pending status |
| `V5BS0163EJ` | Cannot add a purchase card account to a corporate relationship  |  
| `V5BS0163EK` | Cannot add a corporate account to a purchasecard relationship |
| `V5BS0163SB` | 046No relationship rec exists |
| `V5BS0163SD` | 055When bill level is 0,relationship number cannot be # |
| `V5BS0163SE` | 062Cannot add a non purchase account to a purchase relationship |  
| `V5BS0163SF` | 063Cannot add a non corporate account to a corporate relationship |
| `V5BS0164SC` | 043Card scheme must be 0 for non-relationship accounts |
| `V5BS0164SF` | 042Card scheme must be 1, 2 or 3 |
| `V5BS0164SG` | 076 No relationship being added, card scheme cannot be 1 |
| `V5BS0164SH` | 077Org card scheme 2/3 not active, card scheme cannot be 2 or 3 |  
| `V5BS0164SI` | 064Card scheme cannot b 0 unless  relatnship # is spaces or all # |
| `V5BS0164SJ` | 081No relationship exists, card scheme cannot be 1' |
| `V5BS0164SL` | 079Card scheme cannot be 2 if amex is active |
| `V5BS0164SM` | Card scheme cannot be 2 if uci is active |
| `V5BS0164SO` | Card scheme cannot be edited since AMBS-rel-nbr = # |
| `V5BS0164SP` | Crd# scm change not allowed due to pending card action |
| `V5BS0165SA` | 083Value must be 0 on an add |
| `V5BS0165SF` | 103Value must be 0 for a new account |
| `V5BS0170SB` | 093Either due or cycle must be entered |
| `V5BS0171SB` | 102Exp date must be greater than zeroes when st dt > zeros |
| `V5BS0172SA` | 095Generic customer not allowed |
| `V5BS0172SB` | 105No active customer on file |
| `V5BS0172SC` | 106Cust nbr not in add complete status |
| `V5BS0181SA` | 099Date must be > current processing date |
| `V5BS0207ED` | Rel type must be greater than zero if type = 1 |
| `V5BS0213EB` | Cannot change wc 2 to > 2 if it already is 1 or 2 |
| `V5BS0235EB` | Date must be greater than last processing date |
| `V5BS0301SA` | Residence id not on usury table |
| `V5BS0301SB` | Zero $$$ in usury table for sor |
| `V5BS0301SC` | Residence id can not be spaces |
| `V5BS0301SD` | No PCT rec found at this level |
| `V5BS0301SE` | No active rates in processing control table |
| `V5BS0301SF` | No file processing control table |
| `V5BS0302EC` | C -0 $$$$ in usury tbl for soi |
| `V5BS0302SA` | Issuance id must equal perm issuance id on logo |
| `V5BS0302SB` | Issuance id not on usury table |
| `V5BS0302SC` | Zero $$$$ in usury table for soi |
| `V5BS0302SD` | No PCT rec found at this level |
| `V5BS0302SE` | No active rates in processing control table |
| `V5BS0302SF` | No file processing control table |
| `V5BS0303SA/V5BS0303SB` | No PCT rec found at this level |
| `V5BS0303SC` | No active rates in processing control table |
| `V5BS0303SD` | No file processing control table |
| `V5BS0304SA` | Pricing ctrl start/expiration dates conflict |
| `V5BS0304SB` | Enter pricing ctrl when using dates |
| `V5BS0304SC` | Start date less than the org next processing date |
| `V5BS0304SD` | Expire date less than the org next processing date |
| `V5BS0306SA` | No PCT rec found at this level |
| `V5BS0306SC` | Start date less than the org next processing date |
| `V5BS0307SA` | PCT level start/expiration dates conflict |
| `V5BS0307SB` | Enter PCT lvl override when using dates |
| `V5BS0320SA` | 035Pending payment |
| `V5BS0320SC/V5BS0320SD` | Chg from x to z or x to m/n if pmt cyc=1 and logo skip pmt allow |
| `V5BS0320SF` | 038Criteria not met for next skip pay |
| `V5BS0324SA` | Must be space,a-f,i,m,n,p,s,x,y,z,*,or-' |
| `V5BS0324SB` | Must be space,a-f,m,n,p,s,x,y,z,*,or-' |
| `V5BS0342SG` | Start date less than the org next processing date |
| `V5BS0343SC` | Expire date less than the org next processing date |
| `V5BS0403SA` | 018Effective dt must be = or > than next proc dt |
| `V5BS0404SA` | 020No cash cr plan found for this cash plan nbr |
| `V5BS0404SB` | Cash plan cannot be zero during add |
| `V5BS0405SA` | 021No rtl cr plan found for this retail plan nbr |
| `V5BS0405SC` | Retail plan cannot be zero during add |
| `V5BS0502ED` | Required field for add action |
| `V5BS0504EA/V5BS0505EA/V5BS0506EA` | Required field for add function |  
| `V5BS0507EA` | Local use ind must be 0 or 1 |
| `V5BS0516EA/V5BS0516EF` | Smart cards not allowed for logo |
| `V5BS0516EB/V5BS0517EE` | ARMS02 smart card must be 1 |
| `V5BS0516EG/V5BS0517EG` | Default logo program is not on file |
| `V5BS0520EA` | Mobile pi not active at logo level |
| `V5BS0522EA` | ACCT switch date must be equal or greater than next proc date |
| `V5BS0601EC/V5BS0601SC` | Cannot be greater than logo credit limit |
| `V5BS0601SA` | Must be greater than cms file date |  
| `V5BS0602EA` | 065Must be greater than cms file date |
| `V5BS0602EB` | 017Must be equal or greater than cms file date |
| `V5BS0605SA` | Prefer start date must be less than prefer end date |
| `V5BS0611EA` | 029Rec not found on amcp file for this plan |
| `V5BS0611EB` | 025Plan type must be R in file amcp |
| `V5BS0613EA` | 035 1St byte should = zero and  last 9 bytes must be > zeros |
| `V5BS0614EA` | 039Must be equal or greater than next processing date or zeros |
| `V5BS0615EA` | 040Must be zero when logo DD payment flag is S or D |
| `V5BS0615EB` | 041Must be 1 through 31 when logo DD payment flag is P or R |
| `V5BS0615EC` | 024Request day should be between 00 and 31 |
| `V5BS0616EA` | 017Must be equal or greater than cms file date |
| `V5BS0616EB` | 037DD start date must be less than DD expire date |
| `V5BS0617EA` | 039Must be equal or greater than next processing date or zeros |
| `V5BS0618EA` | 023DC start date must be less than DC expire date |
| `V5BS0622EA` | DD account nbr required field |
| `V5BS0624EB` | 011Logo does not allow dd/dc processing |
| `V5BS0624EC` | 012DD/DC processing not allowed for this account |
| `V5BS0624EF` | DD expre dt mst b 0 or > next process dt to reinstate dirct debit |
| `V5BS0624EG` | Pmt rev cntr mst b < x,  pmt rev lmt on logo to reinstate dir dbt |
| `V5BS0624EH` | Ach r/t nbr required |
| `V5BS0624EJ` | Required field |
| `V5BS0624EK` | 035 1St byte should = zero and  last 9 bytes must be > zeros |
| `V5BS0624EL` | Armb011 logo does not allow dd/dc processing |
| `V5BS0626EA` | DD nom ind mst b 1,2,3,9 and DD amt/PCT>= 0 for DD pmt to 2 or 7 |
| `V5BS0627EA` | 016Must be equal to zero when DD nom ind is 0 or 3 |
| `V5BS0627EB` | 018Must be greater than zero when DD nom ind is 1 or 2 or 9 |
| `V5BS0627EC` | 015Must be < 100% and not 0 when DD nom indicator is 2 or 9 |
| `V5BS0628EB` | 031Logo when set to y, allowed values are 0, 1, or 2 |
| `V5BS0630EB` | 042Mst b 0 or 1 when direct credit has expired or been cancelled |
| `V5BS0630EC` | DC request day mst b 0 when DC request indicator is 0, 2, or 3 |
| `V5BS0630ED` | DC req day mst 0 or 1 through 31 when DC request indicator is 1 |  
| `V5BS0630EE` | DC request day must be > 0 when DC request indicator is 4  |
| `V5BS0631EA` | 017Must be equal or greater than cms file date |
| `V5BS0631EB` | 048Change dt mst b >= start dt and < expire dt, unless a dt is 0 |
| `V5BS0631EC` | 048Change dt mst b >= start dt and < expire dt, unless a dt is 0
| `V5BS0640EB` | 035 1St byte should = zero and  last 9 bytes must be > zeros |
| `V5BS0642SD` | Request day not allowed when daily frequency is 1, 2 or 3 |
| `V5BS0642SE` | DD payment must be 2 when daily frequency is 1, 2 or 3 |
| `V5BS0642SF` | Pymt change date must be zero when daily frequency is 1, 2 or 3 |  
| `V5BS0642SG` | DD payment must be zero when changing daily frequency to zero |
| `V5BS0713SA` | 001Required field for add function |
| `V5BS0714SA` | 001Required field for add function
| `V5BS0715SA` | 001Required field for add function
| `V5BS0914SA` | 1St byte should be space or 0 and last 9 bytes must be numeric |
| `V5BS0914SB` | Ibs DDA/savings routing information is not numeric |
| `V5BS0916SA` | 1St byte should be space or 0 and last 9 bytes must be numeric
| `V5BS0916SB` | Ibs DDA/savings routing information is required |
| `V5BS0916SC` | Ibs DDA/savings routing information is required
| `V5BS0916SD` | Ibs DDA/savings routing information is required
| `V5BS0925SB` | Account balance cannot be greater than 0 |
| `V5BS301EA`  | 1) Residence id not on usury table - error code A |
| `V5BS301EB`  | 2) Zero $$$$ in usury table for sor - error code B |
| `V5BS302EA`  | B - issuance id not on usury table |
| `V5BS303EA`  | No PCT rec found at this level |
| `V5BS304EA`  | Pricing ctrl start/expiration dates conflic |
| `V5BS306EA`  | No PCT rec found at this level |
| `V5BS329EA`  | Value should not be 0,1,2 |
| `V5BS4001SB` | AMBS - org is in add pending |
| `V5BS4002EE` | Max nbr of 20 attempts made on base nbr |
| `V5BS4002EF` | Logo does not allow ACCT nbr generation |
| `V5BS4002EG` | Generated ACCT nbr is greater than base ending nbr |
| `V5BS4002EH` | Logo does not allow billing ACCT generation |
| `V5BS4002EI` | Max nbr of 20 attempts made on billing ACCT |
| `V5BS4002EJ` | Generated ACCT nbr is greater than ending billing nbr |
| `V5BS4002SF` | Account number already exists on embosser file |
| `V5BS4002SL` | Account nbr already exists on relationship master |
| `V5BS4084SA` | Minimum values is 0 for number of days delinq |
| `V5BS4288SA` | 028Cycle cannot be zeros  |
| `V5BS4288SB` | 029Cannot add an ACCT with cycle greater than 31 |
| `V5BS4419SA` | Group id not present in the group id file     :amgp |
| `V5BS9976SA` | Generic customer not allowed for non-generic account |
| `V5AK4003SA` | Card number already exists |
| `V5AK4005SA` | Account number required if card number not provided |
| `V5AK4011EA` | Embossing card field must be numeric |
| `V5AK4012EA` | Embossing req field must be numeric |
| `V5AK4024EA` | Pin suppression field must be 0 or 1 |
| `V5AK4025EA` | Block code must equal A - Z or space |
| `V5AK4043EA` | Next card expire date must be numeric and future date |
| `V5AK4044EA` | Next card expire date must be numeric and future date |
| `V5AK4051EA` | Value must be either 1 thru 4 or A thru G |
| `V5AK4056SA` | Org/account number combination not found |
| `V5AK4061EA` | Number cards required must equal zero or 1 |
| `V5AK4063EA` | Embossed name type must not equal 3 |
| `V5AK4064EA` | Embossed name 1 must be greater than space |
| `V5AK4066EA` | Pin delay days must equal zero for smart card |
| `V5AK4075EA` | Cardholder flag must equal 0 or 1 for card scheme 2 or 3 |
| `V5AK4076EA` | Mini field must equal zero for non - visa account |
| `V5AK4077EA` | Maximum freq input not allowed when no auth limit overrd |
| `V5AK4087EA` | Next card expire date must be numeric and future date |
| `V5AK4091EA` | Auth criteria tbl nbr does not match the logo qtrly affl |
| `V5AK4092EA` | Program id must not be greater than zero for mag strip |
| `V5AK4097SA` | Card nbr and account nbr must be equal for card scheme |
| `V5SP4006EA` | Card action should be numeric |
| `V5SP4011SA` | Embosser record not found on file |
| `V5ED0204EC` | Card cannot be reissued |
| `V5ED0204ED` | Card action must be less than 7 |
| `V5ED0204EE` | Additional card not allowed for smart card |
| `V5ED0204EF` | Cannot reissue embosser with status of s |
| `V5ED0204EH` | This field must be 0 for a foreign account |
| `V5ED0204EJ` | Action of 1 allowed only if nbr outst and dte last plastic are 0 |
| `V5ED0204EN` | Nbr of outstanding cards can not be maintaible for card action |
| `V5ED0204EO` | Add is not allowed on nbr of outstanding cards flag |
| `V5ED0205EA` | This field must be 0 for a foreign account |
| `V5ED0211EA` | Add line 1 cannot = spaces if city, state, pstl cde not = spaces |
| `V5ED0221EB` | Cardholder flag must be zero for card scheme 0 |
| `V5ED0222EA` | Embosser name 1 reqd and cannot equal spaces |
| `V5ED0222EB` | Value is required and cannot equal spaces |
| `V5ED0223EA` | Value is required and cannot equal spaces
| `V5ED0230EA` | Mini card processing inactive for logo |
| `V5ED0232EB/V5ED0233EE/V5ED233EE` | Personalized cards not allowed |
| `V5ED0232ED/V5ED232ED/V5ED0233ED/V5ED233ED` | Non personalized cards not allowed |
| `V5ED0234EB/V5ED234EA` | Form factors processing inactive for logo |
| `V5ED0234EC/V5ED234EC` | Mini card processing inactive for logo, DVC ind cannot be 2 or 3 |
| `V5ED0234EF` | DVC must equal 3 |
| `V5ED0234EG` | DVC must equal A or D |
| `V5ED0234EH` | DVC must equal C or F |
| `V5ED0234EI` | DVC must equal D |
| `V5ED0234EJ` | DVC must equal F |
| `V5ED0234EK` | DVC must equal G |
| `V5ED0237EB` | Cannot have more than one primary card |
| `V5ED0240EA/V5ED240EA` | Mobile pi s are not allowed at logo level |
| `V5ED0240EB/V5ED240EB` | Mobile pi s are not allowed at account level |
| `V5ED0404EB` | Value required for an add |
| `V5ED0407SB` | Org not present in amcr file |
| `V5ED0407SF` | Relationship not present |
| `V5ED0802EA` | Date must be greater than current processing date |
| `V5ED203EC`  | Nbr requested can not be greater than nbr outstandng |
| `V5ED204EE`  | Additional card not allowed for smart card |
| `V5ED204EF`  | Cannot reissue embosser with status of S |
| `V5ED211EA`  | Address line 1 cannot=spaces if city,state,or postal cd not=space |
| `V5ED221EB`  | Cardholder flag must equal to zeroes for card scheme 0 |
| `V5ED222EA`  | Value required for an add |
| `V5ED222EB`  | Value is required and cannot equal spaces |
| `V5ED4001SD` | Account not present |
| `V5ED4002ED` | Card number must be provided  |
| `V5ED4004SC` | Business unit does not match with input card number |
| `V5ED4017SA` | Account logo not found |
| `V5ED1901EA` | Group id is not present in group table file |
| `V5ED9934EAV5ED9934EB` | Add not allowed, seq nbr would exceed 99 for smart cd |
| `V5DB4002SA` | AMDB - account not found |
| `V5DB4002SB` | AMDB - account is in add pending |
| `V5DB4001SD` | Customer number can not be spaces |
| `V5DB4001AS` | Cust nbr not found |
| `V5DB4001SC` | AMBX rec not found |
| `V5DB4001SE` | AMBS rec not found |
| `V5DB4001SF` | Account not found amax |
| `V5DB4001SH` | AMED record not found |
| `V5DB4001SJ` | ZAMDX rec not found |
| `V5RM0102EA` | Customer number is required |
| `V5RM0102EB` | Customer number not on file |
| `V5RM0102EC` | Customer number - add pending |
| `V5RM0102ED` | Customer number - not active |
| `V5RM0106EA` | This amount cannot be <  sum of all subordiNAte accounts cr limit |
| `V5RM0106EB` | Credit limit difference cannot be >  company node available |
| `V5RM0106EC` | AMRM - credit limit cannot be zeroes. |
| `V5RM0109EA` | Whole monetary unit - does not conform to CU |
| `V5RM0109EB` | SubordiNAte credit limit cannot be > relationship credit limit |
| `V5RM0112EA` | Bill lvl cannot be 1 when subord accts bill lvl not 1 |
| `V5RM0112EB` | Bill lvl cannot be 0 when subord accts bill lvl not 0 |
| `V5RM0112EC` | Bill lvl cannot be 0 if org cnsld pmts not active |
| `V5RM0112EK` | Bill lvl cannot be set frm 1-0 or 0-1 when subord accts present |  
| `V5RM0113EA` | Billing level modify of 0 not allowed whn billing level is 0 or 1 |
| `V5RM0135EA` | ACCT ctl tbl ovrride is not in amrt file |
| `V5RM0135EB` | ACCT ctl tbl ovrride in amrt - add pending |
| `V5RM0135ED` | Account control table must be zero when billing level is 1 |
| `V5RM0135EE` | ACCT ctl tbl ovrride is not in amrt file  |
| `V5RM0135EF` | ACCT ctl tbl ovrride in amrt - add pending  |
| `V5RM0139EA` | Tran code must point to lm 99 |
| `V5RM0139EB` | Memo pmt trans & rev trans cannot be 0 when bill level is 0 or 2 |
| `V5RM0139EC` | Memo pmt trans & memo pmt rev trans cannot be the same |
| `V5RM0140EA` | Tran code must point to lm 99 |
| `V5RM0142EH` | If rpt freq  or vgis fg is 0 cntry cd & reg nbr are not maintain |
| `V5RM0142EJ/V5RM0205EA` | Customer not on file |
| `V5RM0153ED` | Cash limit cannot be greater than the credit limit |
| `V5RM0205EB/V5RM0142EK` | Customer name/address - add pending |
| `V5RM0205EC/V5RM0142EL` | Customer name/address - not active |
| `V5RM0205ED` | Corp customer number is required |
| `V5RM0228EI` | Freq must be 0 when all extnl rpt value = 0  |
| `V5RM0407SB` | Org not present in amcr file |
| `V5RM4001SG` | Relationships not activated on control record |
| `V5RM4001SI` | Org does not allow rel nbr generation |
| `V5RM4001SJ` | Max nbr of 20 attempts made on rel nbr |
| `V5RM4001SK` | Relation number generation error |
| `V5RM4001SL` | Generated rel nbr is greater than ending rel nbr |
| `V5RM4002SC` | Relationship not on file |
| `V5RM4002SD` | Pending add use add function |
| `V5RM4002SH` | Dup number on name & addr file |
| `V5RM4002SI` | Dup number on account file |
| `V5RM0106EC` | AMRM - credit limit cannot be zeroes |
| `V5S80821SV` | Invalid Statement Delivery Mode |
| `V5AK1512EC` | Invalid DCVV2 method for products supporting both physical and virtual cards |
| `V5AK1512EB` | Invalid DCVV2 method for virtual card |
| `V5AK1512EA` | Invalid DCVV2 method for physical card |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
