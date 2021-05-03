---
description: Configuration changes and service build details
---

# MDMS Configuration & Service Build Updates

### MDMS changes <a id="MDMS-changes"></a>

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Feature</b>
      </th>
      <th style="text-align:left"><b>Service Name</b>
      </th>
      <th style="text-align:left"><b>Changes</b>
      </th>
      <th style="text-align:left"><b>Description</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">WS - Bill Amendment</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"><a href="https://github.com/egovernments/egov-mdms-data/pull/1596">#1596</a>
      </td>
      <td style="text-align:left">Added role action mapping, tax heads, idformat and demand revision basis
        changes for Bill Amendment</td>
    </tr>
    <tr>
      <td style="text-align:left">HRMS - Employee Report</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"><a href="https://github.com/egovernments/egov-mdms-data/pull/1598">#1598</a>
      </td>
      <td style="text-align:left">Created new role to view HRMS Employee report and mapped role action</td>
    </tr>
    <tr>
      <td style="text-align:left">FSM</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <p><a href="https://github.com/egovernments/egov-mdms-data/pull/1602">#1602</a>,
          <a
          href="https://github.com/egovernments/egov-mdms-data/pull/1607">#1607</a>,</p>
        <p><a href="https://github.com/egovernments/egov-mdms-data/pull/1608">#1608</a>,
          <a
          href="https://github.com/egovernments/egov-mdms-data/pull/1610">#1610</a>,</p>
        <p><a href="https://github.com/egovernments/egov-mdms-data/pull/1611">#1611</a>,
          <a
          href="https://github.com/egovernments/egov-mdms-data/pull/1612">#1612</a>,</p>
        <p><a href="https://github.com/egovernments/egov-mdms-data/pull/1613">#1613</a>,
          <a
          href="https://github.com/egovernments/egov-mdms-data/pull/1614">#1614</a>,</p>
        <p><a href="https://github.com/egovernments/egov-mdms-data/pull/1615">#1615</a>,
          <a
          href="https://github.com/egovernments/egov-mdms-data/pull/1624">#1624</a>,</p>
        <p><a href="https://github.com/egovernments/egov-mdms-data/pull/1626">#1626</a>,
          <a
          href="https://github.com/egovernments/egov-mdms-data/pull/1631">#1631</a>,</p>
        <p><a href="https://github.com/egovernments/egov-mdms-data/pull/1632">#1632</a>,
          <a
          href="https://github.com/egovernments/egov-mdms-data/pull/1637">#1637</a>,</p>
        <p><a href="https://github.com/egovernments/egov-mdms-data/pull/1638">#1638</a>,
          <a
          href="https://github.com/egovernments/egov-mdms-data/pull/1640">#1640</a>,</p>
        <p><a href="https://github.com/egovernments/egov-mdms-data/pull/1643">#1643</a>,
          <a
          href="https://github.com/egovernments/egov-mdms-data/pull/1645">#1645</a>, <a href="https://github.com/egovernments/egov-mdms-data/pull/1646">#1646</a>
        </p>
      </td>
      <td style="text-align:left">
        <p>Added FSM related role actions, Billing service, FSM and Vehicle files.</p>
        <p>Enabled cities for FSM.</p>
        <p>Updated Min max value for property Type</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Common</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <p><a href="https://github.com/egovernments/egov-mdms-data/pull/1616">#1616</a>,
          <a
          href="https://github.com/egovernments/egov-mdms-data/pull/1617">#1617</a>,</p>
        <p><a href="https://github.com/egovernments/egov-mdms-data/pull/1618">#1618</a>,
          <a
          href="https://github.com/egovernments/egov-mdms-data/pull/1635">#1635</a>
        </p>
      </td>
      <td style="text-align:left">Changed email id to be generic for city A and removed access from Employee
        role and mapped with specific employee</td>
    </tr>
    <tr>
      <td style="text-align:left">BPA</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"><a href="https://github.com/egovernments/egov-mdms-data/pull/1474">#1474</a>
      </td>
      <td style="text-align:left">Added missing role actions in BPA for different stakeholder types</td>
    </tr>
  </tbody>
</table>

### Config Changes   <a id="Config-Changes"></a>

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Module</b>
      </th>
      <th style="text-align:left"><b>Action</b>
      </th>
      <th style="text-align:left"><b>PR</b>
      </th>
      <th style="text-align:left"><b>Description</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">PDF Service</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"><a href="https://github.com/egovernments/configs/pull/714">#714</a>
      </td>
      <td style="text-align:left">Added amendment coupon pdf changes for water and sewerage connections</td>
    </tr>
    <tr>
      <td style="text-align:left">egov-persister</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"><a href="https://github.com/egovernments/configs/pull/715">#715</a>
      </td>
      <td style="text-align:left">Updated the changes required for multiple road types in water and sewerage
        connection</td>
    </tr>
    <tr>
      <td style="text-align:left">Report - Employee report</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <p><a href="https://github.com/egovernments/configs/pull/716">#716</a>,</p>
        <p><a href="https://github.com/egovernments/configs/pull/717">#717</a>,</p>
        <p><a href="https://github.com/egovernments/configs/pull/721">#721</a>
        </p>
      </td>
      <td style="text-align:left">Added new file employee report for HRMS Admin and configured the report
        path</td>
    </tr>
    <tr>
      <td style="text-align:left">Report - PGR Reports</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <p><a href="https://github.com/egovernments/configs/pull/722">#722</a>,</p>
        <p><a href="https://github.com/egovernments/configs/pull/725">#725</a>
        </p>
      </td>
      <td style="text-align:left">Updated PGR report config file and GRO, LME report designation id and
        tenantid search fix</td>
    </tr>
    <tr>
      <td style="text-align:left">egov-persister,
        <br />egov-indexer</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <p><a href="https://github.com/egovernments/configs/pull/724">#724</a>,</p>
        <p><a href="https://github.com/egovernments/configs/pull/735">#735</a>
        </p>
      </td>
      <td style="text-align:left">Added persister file for dso, fsm calculator, fsm, vehicle, vendor, fsm
        receipt, indexer file for fsm and vendor</td>
    </tr>
  </tbody>
</table>

### Infra Change <a id="Infra-Change"></a>

| **Feature** | **Feature** | **Description** |
| :--- | :--- | :--- |
| WS - Bill Amendment | [\#1335](https://github.com/egovernments/eGov-infraOps/pull/1335) | Added Water and Sewerage service bill amendment credit/debit note pdf config path |
| FSM | [\#1344](https://github.com/egovernments/eGov-infraOps/pull/1344) | Added FSM persister and indexer file path |

### Service Build Updates

| Category | Services | GIT TAGS | Docker Artifact ID | **Remarks** |
| :--- | :--- | :--- | :--- | :--- |
| **Frontend** [**v2.3**](https://github.com/egovernments/frontend/tree/v2.3) | Citizen | [citizen-v1.4.0](https://github.com/egovernments/frontend/releases/tag/citizen-v1.4.0) | citizen:v1.4.0-ab35e639e-1010 |   |
|   | Employee | [employee-v1.4.0](https://github.com/egovernments/frontend/releases/tag/employee-v1.4.0) | employee:v1.4.0-ab35e639e-1107 |   |
|   | DSS Dashboard | [dashboard-v1.4.0](https://github.com/egovernments/frontend/releases/tag/dashboard-v1.4.0) | dss-dashboard:v1.4.0-a5b225df3-55 |   |
|   | DIGIT UI | [digit-ui-v1.1.0](https://github.com/egovernments/digit-ui/tree/digit-ui-v1.1.0) | digit-ui:v1.1.0-b2eb2a6-236 |   |
| **Core Services** [**v2.3**](https://github.com/egovernments/core-services/tree/v2.3) | Encryption | [enc-service-v1.1.1](https://github.com/egovernments/core-services/tree/enc-service-v1.1.1) | egov-enc-service:v1.1.1-19a3ba19-5 |   |
|   | Searcher | [searcher-v1.1.2](https://github.com/egovernments/core-services/tree/searcher-v1.1.2) | egov-searcher:v1.1.2-19a3ba19-10 |   |
|   | Payment Gateway | [pg-service-v1.2.1](https://github.com/egovernments/core-services/tree/pg-service-v1.2.1) | egov-pg-service:v1.2.1-19a3ba19-46 |   |
|   | Filestore | [filestore-v1.2.2](https://github.com/egovernments/core-services/tree/filestore-v1.2.2) | egov-filestore:v1.2.2-19a3ba19-12 |   |
|   | Zuul - API Gateway | [zuul-v1.2.1](https://github.com/egovernments/core-services/tree/zuul-v1.2.1) | zuul:v1.2.1-19a3ba19-17 |   |
|   | Mail Notification | [notification-mail-v1.1.1](https://github.com/egovernments/core-services/tree/notification-mail-v1.1.1) | egov-notification-mail:v1.1.1-19a3ba19-5 |   |
|   | SMS Notification | [notification-sms-v1.1.1](https://github.com/egovernments/core-services/tree/notification-sms-v1.1.1) | egov-notification-sms:v1.1.1-19a3ba19-13 |   |
|   | Localization | [localization-v1.1.0](https://github.com/egovernments/core-services/tree/localization-v1.1.0) | egov-localization:v1.1.0-f9375a4 | No changes in the current release. |
|   | Persister | [persister-v1.1.2](https://github.com/egovernments/core-services/tree/persister-v1.1.2) | egov-persister:v1.1.2-2fc5d31a-18 | No changes in the current release. |
|   | ID Gen | [idgen-v1.2.1](https://github.com/egovernments/core-services/tree/idgen-v1.2.1) | egov-idgen:v1.2.1-74723a03-4 |   |
|   | User | [user-v1.2.3](https://github.com/egovernments/core-services/tree/user-v1.2.3) | egov-user:v1.2.3-19a3ba19-42 |   |
|   | User Chatbot | [user-chatbot-v1.2.1](https://github.com/egovernments/core-services/tree/user-chatbot-v1.2.1) | egov-user-chatbot:v1.2.1-4976757 | No changes in the current release. |
|   | MDMS | [mdms-service-v1.3.0](https://github.com/egovernments/core-services/tree/mdms-service-v1.3.0) | egov-mdms-service:v1.3.0-e50b9eb | No changes in the current release. |
|   | URL Shortening | [url-shortening-v1.1.0](https://github.com/egovernments/core-services/tree/url-shortening-v1.1.0) | egov-url-shortening:v1.1.0-19a3ba19-1 |   |
|   | Indexer | [indexer-v1.1.3](https://github.com/egovernments/core-services/tree/indexer-v1.1.3) | egov-indexer:v1.1.3-19a3ba19-25 |   |
|   | Report | [report-v1.3.1](https://github.com/egovernments/core-services/releases/tag/report-v1.3.1) | report:v1.3.1-697b9687-6 |   |
|   | Workflow | [workflow-v2-v1.1.3](https://github.com/egovernments/core-services/tree/workflow-v2-v1.1.3) | egov-workflow-v2:v1.1.3-19a3ba19-53 |   |
|   | PDF Generator | [pdf-service-v1.1.2](https://github.com/egovernments/core-services/releases/tag/pdf-service-v1.1.2) | pdf-service:v1.1.2-f56c8a38-16 |   |
|   | Chatbot | [chatbot-v1.1.3](https://github.com/egovernments/core-services/tree/chatbot-v1.1.3) | chatbot:v1.1.3-19a3ba19-30 |   |
|   | Access Control | [accesscontrol-v1.1.1](https://github.com/egovernments/core-services/tree/accesscontrol-v1.1.1) | egov-accesscontrol:v1.1.1-19a3ba19-4 |   |
|   | Location | [location-v1.1.2](https://github.com/egovernments/core-services/tree/location-v1.1.2) | egov-location:v1.1.2-19a3ba19-18 |   |
|   | OTP | [otp-v1.2.0](https://github.com/egovernments/core-services/tree/otp-v1.2.0) | egov-otp:v1.2.0-27f2fa2e-3 | No changes in the current release. |
|   | User OTP | [user-otp-v1.1.1](https://github.com/egovernments/core-services/releases/tag/user-otp-v1.1.1) | user-otp:v1.1.1-19a3ba19-3 |   |
| **Business Services** [**v2.3**](https://github.com/egovernments/business-services/tree/v2.3) | Apportion | [apportion-service-v1.1.4](https://github.com/egovernments/business-services/releases/tag/apportion-service-v1.1.4) | egov-apportion-service:v1.1.4-ec514d1-12 |   |
|   | Collection | [collection-services-v1.1.3](https://github.com/egovernments/business-services/releases/tag/collection-services-v1.1.3) | collection-services:v1.1.3-ec514d1-94 |    |
|   | Billing | [billing-service-v1.3.1](https://github.com/egovernments/business-services/releases/tag/billing-service-v1.3.1) | billing-service:v1.3.1-ec514d1-114 |   |
|   | HRMS | [hrms-v1.2.1](https://github.com/egovernments/business-services/releases/tag/hrms-v1.2.1) | egov-hrms:v1.2.1-ec514d1-15 |   |
|   | Dashboard Analytics | [dashboard-analytics-v1.1.3](https://github.com/egovernments/business-services/releases/tag/dashboard-analytics-v1.1.3) | dashboard-analytics:v1.1.3-ec514d1-17 |   |
|   | Dashboard Ingest | [dashboard-ingest-v1.1.2](https://github.com/egovernments/business-services/releases/tag/dashboard-ingest-v1.1.2) | dashboard-ingest:v1.1.2-4d1acca-8 |   |
|   | EGF Instrument | [egf-instrument-v1.1.2](https://github.com/egovernments/business-services/releases/tag/egf-instrument-v1.1.2) | egf-instrument:v1.1.2-c3a5a65-4 |   |
|   | EGF Master | [egf-master-v1.1.1](https://github.com/egovernments/business-services/releases/tag/egf-master-v1.1.1) | egf-master:v1.1.1-ec514d1-1 |   |
|   | Finance Collection Voucher Consumer | [finance-collections-voucher-consumer-v1.1.2](https://github.com/egovernments/business-services/releases/tag/finance-collections-voucher-consumer-v1.1.2) | finance-collections-voucher-consumer:v1.1.2-ec514d1-23 |   |
| **Municipal Services** [**v2.3**](https://github.com/egovernments/municipal-services/releases/tag/v2.3) | Trade License | [tl-services-v1.1.3](https://github.com/egovernments/municipal-services/releases/tag/tl-services-v1.1.3) | tl-services:v1.1.3-22e87ed4-77 |   |
|   | Trade License Calculator | [tl-calculator-v1.1.2](https://github.com/egovernments/municipal-services/releases/tag/tl-calculator-v1.1.2) | tl-calculator:v1.1.2-22e87ed4-11 |   |
|   | Fire NOC | [firenoc-services-v1.1.2](https://github.com/egovernments/municipal-services/releases/tag/firenoc-services-v1.1.2) | firenoc-services:v1.1.2-9eddbc22-23 |   |
|   | Fire NOC Calculator | [firenoc-calculator-v1.1.2](https://github.com/egovernments/municipal-services/releases/tag/firenoc-calculator-v1.1.2) | firenoc-calculator:v1.1.2-9eddbc22-13 |   |
|   | Property Services | [property-services-v1.1.4](https://github.com/egovernments/municipal-services/releases/tag/property-services-v1.1.4) | property-services:v1.1.4-22e87ed4-210 |   |
|   | Property Tax Calculator | [pt-calculator-v2-v1.1.3](https://github.com/egovernments/municipal-services/releases/tag/pt-calculator-v2-v1.1.3) | pt-calculator-v2:v1.1.3-22e87ed4-130 |   |
|   | Property Tax | [pt-services-v2-v1.0.0](https://github.com/egovernments/municipal-services/tree/pt-services-v2-v1.0.0) | pt-services-v2:v1.0.0-ecf3410a | No changes in the current release. |
|   | Water Charges | [ws-services-v1.3.0](https://github.com/egovernments/municipal-services/releases/tag/ws-services-v1.3.0) | ws-services:v1.3.0-22e87ed4-100 |   |
|   | Water Charges Calculator | [ws-calculator-v1.3.0](https://github.com/egovernments/municipal-services/releases/tag/ws-calculator-v1.3.0) | ws-calculator:v1.3.0-22e87ed4-63 |   |
|   | Sewerage Charges | [sw-services-v1.3.0](https://github.com/egovernments/municipal-services/releases/tag/sw-services-v1.3.0) | sw-services:v1.3.0-22e87ed4-48 |   |
|   | Sewerage Charges Calculator | [sw-calculator-v1.3.0](https://github.com/egovernments/municipal-services/releases/tag/sw-calculator-v1.3.0) | sw-calculator:v1.3.0-22e87ed4-32 |   |
|   | BPA Calculator | [bpa-calculator-v1.1.0](https://github.com/egovernments/municipal-services/tree/bpa-calculator-v1.1.0) | bpa-calculator:v1.1.0-4ee62c15-5 |   |
|   | BPA Services | [bpa-services-v1.1.2](https://github.com/egovernments/municipal-services/tree/bpa-services-v1.1.2) | bpa-services-db:v1.1.2-22e87ed4-11 |   |
|   | User Event | [user-event-v1.1.2](https://github.com/egovernments/municipal-services/releases/tag/user-event-v1.1.2) | egov-user-event:v1.1.2-22e87ed4-5 |   |
|   | PGR | [rainmaker-pgr-v1.1.3](https://github.com/egovernments/municipal-services/releases/tag/rainmaker-pgr-v1.1.3) | rainmaker-pgr:v1.1.3-22e87ed4-38 |   |
|   | PGR Service | [pgr-services-v1.1.1](https://github.com/egovernments/municipal-services/releases/tag/pgr-services-v1.1.1) | pgr-services:v1.1.1-22e87ed4-94 |   |
|   | Land Services | [land-services-v1.0.1](https://github.com/egovernments/municipal-services/releases/tag/land-services-v1.0.1) | land-services:v1.0.1-22e87ed4-5 |   |
|   | NOC Services | [noc-services-v1.0.1](https://github.com/egovernments/municipal-services/releases/tag/noc-services-v1.0.1) | noc-services:v1.0.1-22e87ed4-5 |   |
|   | FSM | [fsm-v1.0.0](https://github.com/egovernments/municipal-services/releases/tag/fsm-v1.0.0) | fsm:v1.0.0-05847a57-70 | New Service |
|   | FSM Calculator | [fsm-calculator-v1.0.0](https://github.com/egovernments/municipal-services/releases/tag/fsm-calculator-v1.0.0) | fsm-calculator:v1.0.0-39678039-14 | New Service |
|   | Vehicle | [vehicle-v1.0.0](https://github.com/egovernments/municipal-services/releases/tag/vehicle-v1.0.0) | vehicle:v1.0.0-f898438c-14 | New Service |
|   | Vendor | [vendor-v1.0.0](https://github.com/egovernments/municipal-services/releases/tag/vendor-v1.0.0) | vendor:v1.0.0-f898438c-5 | New Service |
| **Utilities Services** [**v2.3**](https://github.com/egovernments/utilities/tree/v2.3) | Custom Consumer | [custom-consumer-v1.1.0](https://github.com/egovernments/utilities/tree/custom-consumer-v1.1.0) | egov-custom-consumer:v1.1.0-7a6db73 | No changes in the current release. |
|   | PDF | [pdf-v1.0.1](https://github.com/egovernments/utilities/tree/pdf-v1.0.1) | egov-pdf:v1.0.1-20a54e0-2 | No changes in the current release. |
| **Others Service** | eDCR | [egov-edcr-v1.1.0](https://github.com/egovernments/eGov-dcr-service/tree/egov-edcr-v1.1.0) | egov-edcr:v1.1.0-60cf5c6-7 |   |
|   | Finance |   |   |   |
| **Configs** [**v2.3**](https://github.com/egovernments/configs/tree/v2.3) |   |   |   |   |
|  **MDMS** [**v2.3**](https://github.com/egovernments/egov-mdms-data/tree/v2.3) |   |   |   |   |
|  **Localization** [**v2.3**](https://github.com/egovernments/releasekit/releases/tag/v2.3) |   |   |   |   |

