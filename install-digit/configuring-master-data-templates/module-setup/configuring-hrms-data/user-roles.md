# User Roles

### Introduction

A user role defines permissions for users to perform a group of tasks. In a default application installation, there are some predefined roles with a predefined set of permissions. Each role has a certain number set of tasks it is allowed to perform and these roles are Super Admin, Trade License Approver, Data Entry Admin and Trade License document verifier etc.

### Data Table

| Sr. No. | Code\* | Name\* | Description |
| :--- | :--- | :--- | :--- |
| 1 | TL\_APPROVER | TL Approver | Trade License Approver |
| 2 | GRO | Grievance Routing Officer | Grievance Routing Officer |
| 3 | CSR | Customer Support Representative | An employee who files and follows up complaints on behalf of the citizen |

{% hint style="info" %}
Data given in the table is sample data for reference.
{% endhint %}

### Procedure

#### Data Definition

| Sr. No. | Column Name | Data Type | Data Size | Is Mandatory? | Definition/ Description |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Code | Alphanumeric | 64 | Yes | A unique code that identifies the user role name. |
| 2 | Name | Text | 256 | Yes | The Name indicates the User Role while creating an employee a role can be assigned to an individual employee |
| 3 | Description | Text | 256 | No | A short narration provided to the user role name |

#### Steps to fill data

1. Download the data template attached to this page.
2. Have it open and go through all the headers and understand the meaning of them by referring 'Data Definition' section.
3. Make sure all the headers, its data type, field size and its definition/ description is understood properly. In case of any doubt, please reach out to the person who has shared this document with you to discuss the same and clear out the doubts.
4. Identify all different types of user roles on the basis of ULB’s functions.
5. Start filling the data starting from serial no. and complete a record at once. repeat this exercise until the entire data is filled into a template.
6. Verify the data once again by going through the checklist and taking care of each and every point mentioned in the checklist.

### Checklist

The checklist is a set of activities to be performed once the data is filled into a template to ensure data type, size, and format of data is as per the expectation. These activities have been divided into 2 groups as given below.

#### Common Checklist

This checklist covers all the activities which are common across the entities.

| Sr. No | Checklist Parameter | Example |
| :--- | :--- | :--- |
| 1 | Make sure that each and every point in this reference list has been taken care of | [Checklist](../untitled-1/checklist.md) |

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
      <td style="text-align:left">The Code should be alphanumeric and unique</td>
      <td style="text-align:left">TL_APPROVER, GRO</td>
    </tr>
    <tr>
      <td style="text-align:left">2</td>
      <td style="text-align:left">The Name should not contain any special characters</td>
      <td style="text-align:left">
        <p>TL Approver : [Allowed]</p>
        <p>#TL Approver! : [Not allowed]</p>
      </td>
    </tr>
  </tbody>
</table>

### Attachments

{% file src="../../../../.gitbook/assets/configuration-data-template-user-roles.xlsx" caption="Configuration Data Template " %}

{% file src="../../../../.gitbook/assets/sample-confugration-data-user-roles.xlsx" caption="Sample Data" %}
