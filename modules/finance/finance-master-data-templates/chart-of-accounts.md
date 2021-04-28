# Chart Of Accounts

## Introduction <a id="introduction"></a>

A chart of Accounts \(COA\) is a listing of the Ledger codes that a State or ULB’s has identified and made available for recording transactions in its general ledger. COA is a standard data that need to be set up as per the National Municipal Accounting Manual or Respective State-wise manual. Click [here](http://www.cmao.nic.in/Resources/National%20Accounting%20Manual.pdf) for the NMAM manual. The COA definition can consist of 3 or 4 levels of hierarchy. Ex: Major-&gt;Minor-&gt;Detailed \(3 levels\) or Major-&gt;Minor-&gt;Sub Minor-&gt;Detailed \(4 Levels\). It is up to the state to define the levels required depending on the reporting needs. Detailed code is the node or the level at which the transaction is done.

## Data Table <a id="data-table"></a>

| Sr. No\* | Major Code\* | Major head Description\* | Minor Code\* | Minor Head Description\* | SubMinor Code | SubMinor Head Description | Detailed Heads \(Ledgers\)\* | Ledger Code\* | Type | Account Detail Type | Function Required | Budget Required |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | 110 | Tax Revenue | 110-01 | Property Tax | 110-01-01 | Property Tax - General Tax | Property Tax - General Tax - Residential | 110-01-01-01 | Income | ​ | Yes/No | Yes/No |
| 2 | 210 | Establishment Expenses | 210-10 | Salaries and Wages | ​ | ​ | Basic Pay | 210-10-01 | Expenses | ​ | Yes/No | Yes/No |
| 3 | 350 | Other Liabilities | 350-11 | Employee Liabilities | ​ | ​ | Salaries Unpaid | 350-11-01 | Liabilities | Drawing Officer | Yes/No | Yes/No |
| 4 | 410 | Fixed Assets | 410-20 | Buildings | ​ | ​ | Office Building | 410-20-02 | Assets | ​ | Yes/No | Yes/No |

The data given in the table is sample data.

## Procedure <a id="procedure"></a>

### Data Definition <a id="data-definition"></a>

| Sr No | Column Name | Data Type | Data Size | Is Mandatory? | Definition/ Description |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Major Code | Alphanumeric | 50 | Yes | The Major Code can be any number of digits, \(though NMAM suggest the first 3 digits\) of the GL Code to be the Major code, this will help in collating the reports at the Nation level |
| 2 | Major head Description | Text | 250 | Yes | The short name given to the Major code to easily identify the Account Name for individual code |
| 3 | Minor Code | Alphanumeric | 50 | Yes | The Minor Code can be any number of digits, the digits are configurable. The Minor code will help in collating the reports at the State level. Also, the State has the flexibility to define the minor codes |
| 4 | Minor Head Description | Text | 250 | Yes | The short name given to the Minor code to easily identify the Account Name for individual code |
| 5 | SubMinor Code | Alphanumeric | 50 | No | The SubMinor Code can be optional, State/ULB can set up a sub minor level code based on their requirement, this would help in facilitating the additional level of reporting and also detail transaction-level information \(The SubMinor code is not listed in NMAM manual\) |
| 6 | SubMinor Head Description | Text | 250 | No | The short name given to the SubMinor code to easily identify the Account Name for individual code |
| 7 | Detailed Heads \(Ledgers\) | Text | 250 | Yes | The short name for the Ledger Code, wherein users use this account head name while posting the transactions into the system |
| 8 | Ledger Code | Alphanumeric | 50 | Yes | A General Ledger Code \(GL Code\) is a string of 7 to 9 digit numeric characters assigned to each financial entry in a State/ULB ledger. A GL Code can be assigned to different debit or credit entries to make accounting transactions |
| 9 | Type | Text | 250 | No | The Type indicates the Income, Expenses, Liabilities and Assets which are mapped to each individual GL code. User can easily identify the GL code by this mapping |
| 10 | Account Detail Type | Text | 250 | No | The account details type is the subsidiary ledger, The Suppliers, Contractors and Employees are standard subsidiary ledger. This will help the user to identify the subsidiary ledger details while processing any bill transaction in the system |
| 11 | Function Required | Text | 250 | No | A GL Code can be linked for the validation of the Function, the user while posting a transaction can select a particular function to which transaction will be linked and this will facilitate easy Function wise reporting |
| 12 | Budget Required | Text | 250 | No | A GL Code can be linked for the validation of a Budget. User can have a validation check while posting a transaction into the system, this will facilitate tracking the amount usage |

### Steps to fill data <a id="steps-to-fill-data"></a>

1. Download the data template attached to this page.
2. Have it open and go through all the headers and understand the meaning of them by referring 'Data Definition' section.
3. Make sure all the headers, its data type, field size and its definition/ description is understood properly. In case of any doubt, please reach out to the person who has shared this document with you to discuss the same and clear out the doubts.
4. Start filling the data starting from serial no. and complete a record at once. repeat this exercise until the entire data is filled into a template.
5. Verify the data once again by going through the checklist and taking care of each and every point mentioned in the checklist.

## Checklist <a id="checklist"></a>

The checklist is a set of activities to be performed once the data is filled into a template to ensure data type, size, and format of data is as per the expectation. These activities have been divided into 2 groups as given below.

### Common Checklist <a id="common-checklist"></a>

This checklist covers all the activities which are common across the entities.

| Sr. No | Checklist Parameter | Example |
| :--- | :--- | :--- |
| 1 | Make sure that each and every point in this reference list has been taken care of | ​[Checklist](https://docs.digit.org/configure-digit/configuring-master-data-templates/module-setup/common-config/checklist)​ |

### Entity Specific Checklist <a id="entity-specific-checklist"></a>

This checklist covers the activities which are specific to the entity.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Sr. No.</th>
      <th style="text-align:left">Checklist Parameter</th>
      <th style="text-align:left">Example</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">1</td>
      <td style="text-align:left">The Major, Minor and Sub minor Description Name should not contain any
        special characters</td>
      <td style="text-align:left">
        <p>Tax Revenue : [Allowed]</p>
        <p>#Tax Revenue! : [Not allowed]</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">2</td>
      <td style="text-align:left">The Ledger Codes that are defined by the state team should be alphanumeric
        and Unique</td>
      <td style="text-align:left">110-01-01-01</td>
    </tr>
  </tbody>
</table>

## Attachments <a id="attachments"></a>

[Configuration Data Templateconfiguration-data-template-chart-of-account.xlsx - 31KB](https://firebasestorage.googleapis.com/v0/b/gitbook-28427.appspot.com/o/assets%2F-MERG_iQW5oN4ukgXP8K%2Fsync%2F08b0416a4e3c96ac2346f8f64018ff5f2bca0cf2.xlsx?generation=1602050612773894&alt=media)

[Sample Datasample-confugration-data-chart-of-account.xlsx - 25KB](https://firebasestorage.googleapis.com/v0/b/gitbook-28427.appspot.com/o/assets%2F-MERG_iQW5oN4ukgXP8K%2Fsync%2F65851ed3e05ff2f4520ba79e055c6ed828604c41.xlsx?generation=1602050612896329&alt=media)
