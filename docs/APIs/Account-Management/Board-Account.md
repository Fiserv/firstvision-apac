# Board Account

This API is used to board a new account. API internally generate a new account Id that identify the record being added. 

Fields that are not provided in the request object will be initialized to their default values. All numeric fields are initialized to zero and alphanumeric fields initialized to spaces.

## Endpoint

`POST /v1/accounts/boardAccount`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
    "isInsuranceProductEnabled": "N",
    "businessUnit": 700,
    "productId": 1,
    "customerId": "12345679",
    "corporateId": "0",
    "shortName": "Charlie",
    "primaryAccountFlag": " ",
    "creditLimit": "15000.0",
    "billingLevel": "1",
    "dualBillingFlag": "0",
    "customerSelectedDueDay": 0,
    "billingCycle": 18,
    "cashPlanId": 0,
    "retailPlanId": 0,
    "cardTechnology": "0",
    "temporaryCreditLimit": "0",
    "temporaryCreditLimitExpiryDate": "00/00/0000",
    "owningBranchNumber": 999999998,
    "isMobilePiEnabled": "0",
    "authorizationCriteriaTable": " ",
    "isSuppressLetterEnabled": "0",
    "isWaiveAnnualMembershipFeeEnabled": "0",
    "isSupressTokenEnabled": "0",
    "coreBankingIndicator": " ",
    "pctOverrideDetails": {
        "pctOverride": " ",
        "pctOverrideStartDate": "00/00/0000",
        "pctOverrideExpireDate": "00/00/0000",
        "levelStartDate": "00/00/0000",
        "levelExpireDate": "00/00/0000",
        "level": " "
    },
    "ibsDetails": {
        "ddaRoutingId": "0",
        "ddaAccountId": " ",
        "savingsRoutingId": "12345",
        "savingsAccountId": "12345"
    },
    "residenceId": "600",
    "issuanceId": " ",
    "externalContractId": "000012672379",
    "addressId": "HOME",
    "sourceCode": " ",
    "statementDeliveryMode": "E"
}
``` 

<!--
type: tab
-->

```json
{
    "businessUnit": 700,
    "productId": 1,
    "accountId": "0007000011614703900"
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
    "instance": "/v1/accounts/boardAccount",
    "invalid-params": [
      "V5S84001EA: ORGANIZATION NOT ON FILE"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/accounts/boardAccount).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `isInsuranceProductEnabled` | Payload | *string* | 01 | This is the code that indicates whether to add an Insurance Product record. |
| `businessUnit` | Payload | *number* | 3 | Unique identification number associated with the organization. Valid values from 1-998. |
| `customerId` | Payload | *string* | 19 | Unique identification number assigned to a customer. |
| `creditLimit` | Payload | *string* | 17 | This is the credit limit of the account. |
| `isSuppressLetterEnabled`| Payload | *number* | 01 | Code that indicates whether to suppress all letters for the account. |
| `isSupressTokenEnabled` | Payload | *number* | 01 | Code that indicates whether the account is eligible for tokenization. |
| `coreBankingIndicator` | Payload | *string* | 01 | Code that indicates type of account. |
| `isAnnualMembershipFeeEnabled` | Payload | *number* | 01 | Flag that indicates whether to waive the annual membership fee for the account. |
| `ProductId` | Payload | *number* | 3 | Unique identification number of the product associated with the organization. Valid values are 1-998. |
| `addressId` | Payload | *string* | 15 | Address identifier to determine the type of address. Ex: Home, Office, etc. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5S84005EA` | Customer NA account must be blank |                                
| `V5S84003EA/V5S84003EE` | Base account number required | 
| `V5S84003EG` | Base account number must be numeric |  
| `V5S84003EH` | Base account number required |                                     
| `V5S84009EA` | Relationship number required |                                     
| `V5S84154EC` | Relationship number cannot equal customer or account number |      
| `V5S84154SA` | Customer number not on file for this org |                         
| `V5S84154SB` | Customer number already exists for this org |  
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
| `V5DB4002SA` | AMDB - account not found |                                         
| `V5DB4002SB` | AMDB - account is in add pending |                                 
| `V5DB4001SD` | Customer number can not be spaces |                                
| `V5DB4001AS` | Cust nbr not found |                                               
| `V5DB4001SC` | AMBX rec not found |                                               
| `V5DB4001SE` | AMBS rec not found |                                               
| `V5DB4001SF` | Account not found amax |                                           
| `V5DB4001SH` | AMED record not found |                                            
| `V5DB4001SJ` | ZAMDX rec not found | 

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*