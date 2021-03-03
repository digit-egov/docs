# Deductions

### Introduction

A deduction master is defined to create a reference between ledger codes and to the standard and statutory deductions that are deducted in various creditor bills. By defining this deduction master, accounts department can process the remittance of all the deductions done for a time period at once and keep track of the same.

An example of a deduction is what is deducted from salary bill as income taxes.

### Data Table

| Sr. No\* | Deduction Name\* | Deduction Code\* | Subledger Category | Account Code\* | \*Remitted To | IFSC Code | Account No | Description |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | CPF Deduction | CPF | Employee | 3502003 - CPF Deduction | Central Provident Fund Board | UBIN0XXXX69 | 2XXXX1234XX4 | CPF Deduction |
| 2 | TDS Deduction | TDS | Contractor | 3502001 - TDS Deduction | Central Government | ICICI00XXXX7 | 6XXX97156XX5 | TDS Deduction |
| 3 | TDS from Employees | TDS Employees | Employee | 3502008 - TDS Employee | Central Government | HDFC00XXX51 | 9XXXX759691XX7 | TDS from Employees |

{% hint style="info" %}
Data given in the table is a sample data.
{% endhint %}

### Procedure

#### Data Definition

| Sr No | Column Name | Data Type | Data Size | Is Mandatory? | Definition/ Description |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Deduction Name | Text | 250 | Yes | The name for the deduction head, wherein users use this deduction head name while posting the transactions into the system and also user can generate an individual report using the deduction name. |
| 2 | Deduction Code | Alphanumeric | 20 | Yes | A unique code that identifies the deduction name, this will help the user to easily identify the deduction type while doing a transaction. |
| 3 | Subledger Category | Text | 250 | No | The Subledger type is the value which will tell the party type associated with the deduction. This will be aligned with the standard set of sub-ledger types in DIGIT like - Contractor, Supplier and Employee. Example: When payment to be made for a contractor, TDS deduction is done and “Contractor” would be mapped to the sub-ledger type. Click [SubLedger Category](sub-ledger-category.md) for the master details |
| 4 | Account Code | Alphanumeric | 50 | Yes | A particular GL code would be mapped for the deduction code, these accounts codes would be used in the transaction when a deduction needs to be made. If the sub-ledger type is present then the GL code has to be a control code of that sub-ledger. If sub-ledger type is blank, then the GL code mapped will be a non-control code |
| 5 | Remitted To | Text | 250 | Yes | The “Remitted To” represent the relevant government department to which all the statutory remittances like Provident fund, TDS, CPF and ESI etc are deducted and remitted as per the Act. So while making the payment the “Pay To” will be set to this value |
| 6 | IFSC Code | Alphanumeric | 11 | No | The Bank IFSC code pertaining to the bank branch to which the payment will be made for this particular deduction |
| 7 | Account No | Alphanumeric | 25 | No | The Bank account number represents the account number to which all the deduction which are made would be remitted |
| 8 | Description | Text | 250 | No | A short description shows the deduction details for which the remittance made to the relevant government department |

#### Steps to fill data

1. Download the data template attached to this page.
2. Have it open and go through all the headers and understand the meaning of them by referring 'Data Definition' section.
3. Make sure all the headers, its data type, field size and its definition/ description is understood properly. In case of any doubt, please reach out to the person who has shared this document with you to discuss the same and clear out the doubts.
4. Identify all different types of deduction.
5. Start filling the data starting from serial no. and complete a record at once. repeat this exercise until the entire data is filled into a template.
6. Verify the data once again by going through the checklist and taking care of each and every point mentioned in the checklist.

### Checklist

The checklist is a set of activities to be performed once the data is filled into a template to ensure data type, size, and format of data is as per the expectation. These activities have been divided into 2 groups as given below.

#### Common Checklist

This checklist covers all the activities which are common across the entities.

| Sr. No | Checklist Parameter | Example |
| :--- | :--- | :--- |
| 1 | Make sure that each and every point in this reference list has been taken care of. | [Checklist](../common-config/checklist.md) |

#### Entity Specific Checklist

This checklist covers the activities which are specific to the entity.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Sr. No.</th>
      <th style="text-align:left">Activity</th>
      <th style="text-align:left">Example</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">1</td>
      <td style="text-align:left">Deduction Code should be unique and no special character is allowed.</td>
      <td
      style="text-align:left">
        <p>CPF : [Allowed]</p>
        <p>#CPF! : [Not allowed]</p>
        </td>
    </tr>
    <tr>
      <td style="text-align:left">2</td>
      <td style="text-align:left">The format of the Account Code to be 7 to 9 digits numeric and unique
        no repetitive code should be entered. Only detailed account code should
        be listed here and this should be an active code in the COA master.</td>
      <td
      style="text-align:left">
        <p>Click on Chart of Accounts for master details.</p>
        <p><a href="chart-of-accounts.md">Chart of Accounts</a>
        </p>
        </td>
    </tr>
  </tbody>
</table>

### Attachments

{% file src="../../../../.gitbook/assets/configuration-data-template-deduction.xlsx" caption="Configuration Data Template" %}

{% file src="../../../../.gitbook/assets/sample-confugration-data-deduction.xlsx" caption="Sample Data" %}


