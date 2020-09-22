# Configuring Master Data



### Overview <a id="Overview"></a>

Configuring Master Data for a new module requires creating a new module in the master config file and adding masters data. For better organizing, create all the master data files belongs to the module in the same folder. Organizing in same folder is not mandatory it is based on the moduleName in the Master data file.

### Pre-requisites <a id="Pre-requisites"></a>

Before you proceed with the configuration, make sure the following pre-requisites are met -

* User with permissions to edit the git repository where MDMS data is configured.

### Key Functionalities <a id="Key-Functionalities"></a>

These data can be used to validate the incoming data.

### Deployment Details <a id="Deployment-Details"></a>

1. After adding the new module data, the MDMS service needs to be restarted to read the newly added data.

### Configuration Details <a id="Configuration-Details"></a>

1. Adding new module

The Master config file is structured as below. Each key in the Master config is a module and each key in the module is a master.`1 2 3 4 5 6 7 8 9 10 11 12 13` `{ "<module1>":{ "<master1>":{}, "<master2>":{}, ... }, "<module2>":{ <master3>:{}, <master4>:{}, ... }, ... }`

the new module can be added below the existing modules in the master config file.

2. Creating Masters data

Please check the link to create new master[ Adding New Master](https://digit-discuss.atlassian.net/wiki/spaces/DD/pages/644874241/Adding+New+Master)

### Reference Docs <a id="Reference-Docs"></a>

#### Doc Links <a id="Doc-Links"></a>

| **Title**  | **Link** |
| :--- | :--- |
|   Sample Master config file | [![](https://github.githubassets.com/favicon.ico)https://github.com/egovernments/playground-mdms-data/blob/master/master-config.json - Connect to preview](https://github.com/egovernments/playground-mdms-data/blob/master/master-config.json) |
|  Sample Module folder |  [![](https://github.githubassets.com/favicon.ico)https://github.com/egovernments/playground-mdms-data/tree/master/data/pg/TradeLicense - Connect to preview](https://github.com/egovernments/playground-mdms-data/tree/master/data/pg/TradeLicense) |
