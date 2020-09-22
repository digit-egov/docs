# Adding new Master

### Overview <a id="Overview"></a>

For creating a new master in MDMS, create the JSON file with the master data and configure the newly created master in the master config file.

### Pre-requisites <a id="Pre-requisites"></a>

Before proceeding with the configuration, make sure the following pre-requisites are met -

* User with permissions to edit the git repository where MDMS data is configured.

### Deployment Details <a id="Deployment-Details"></a>

1. After adding the new master, the MDMS service needs to be restarted to read the newly added data.

### Configuration Details <a id="Configuration-Details"></a>

1.  1. Creating Master JSON:  The new JSON file needs to contain 3 keys as shown in the below code snippet. The new master can be created for Statewide or ULB wise. Tenant id and config in the master config file determines this.`1 2 3 4 5` `{ "tenantId": "< TENANT ID >", "moduleName": "< MODULE NAME >", "< MASTER NAME >": [] }`
   2. Configuring the master config file:  
  
      The Master config file is structured as below. Each key in the Master config is a module and each key in the module is a master.  
  
      `1 2 3 4 5 6 7 8 9 10 11 12 13` `{ "<module1>":{ "<master1>":{}, "<master2>":{}, ... }, "<module2>":{ <master3>:{}, <master4>:{}, ... }, ... }`

  
      Each master contain following data and keys are self-explanatory  
  
      `1 2 3 4 5` `"master":{ "masterName": "<>", "isStateLevel": true, "uniqueKeys": [] }`



### Reference Docs <a id="Reference-Docs"></a>

#### Doc Links <a id="Doc-Links"></a>

| **Title**  | **Link** |
| :--- | :--- |
|  Sample Master file | [https://github.com/egovernments/playground-mdms-data/blob/master/data/pg/PropertyTax/ConstructionType.json](https://github.com/egovernments/playground-mdms-data/blob/master/data/pg/PropertyTax/ConstructionType.json) |
|  Sample Master configuration | [https://github.com/egovernments/playground-mdms-data/blob/081a232c26be11a9d803d4490e01d49a7e35985c/master-config.json\#L561](https://github.com/egovernments/playground-mdms-data/blob/081a232c26be11a9d803d4490e01d49a7e35985c/master-config.json#L561) |

|  |
| :--- |

