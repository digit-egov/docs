# User Services

### Overview <a id="Overview"></a>

User service is responsible for user data management and providing functionality to login and logout into Digit system

### Pre-requisites <a id="Pre-requisites"></a>

Before you proceed with the configuration, make sure the following pre-requisites are met -

* Java 8
* Kafka server is up and running
* Encryption and MDMS services are running
* PSQL server is running and database
* Redis is running

### Key Functionalities <a id="Key-Functionalities"></a>

* Store, update and search user data
* Provide authentication
* Provide login, logout functionality into DIGIT platform
* Store user data PIIs in encrypted form

### Interaction Diagram <a id="Interaction-Diagram"></a>

![](../../../.gitbook/assets/image%20%2875%29.png)

### Deployment Details <a id="Deployment-Details"></a>

1. Setup latest version of egov-enc-service and egov-mdms- service
2. Deploy the latest version of egov-user service
3. Add Role-Action mapping for API’s

### Configuration Details <a id="Configuration-Details"></a>

Following application properties file in user service are configurable.

| **Property** | **Value** | **Remarks** |
| :--- | :--- | :--- |
| egov.user.search.default.size | 10 | default search record number limit |
| citizen.login.password.otp.enabled | true | whether citizen login otp based |
| employee.login.password.otp.enabled | false | whether employee login otp based |
| citizen.login.password.otp.fixed.value | 123456 | fixed otp for citizen |
| citizen.login.password.otp.fixed.enabled | false | allow fixed otp for citizen |
| otp.validation.register.mandatory | true | whether otp compulsory for registration |
| access.token.validity.in.minutes | 10080 | validity time of access token |
| refresh.token.validity.in.minutes | 20160 | validity time of refresh token |
| default.password.expiry.in.days | 90 | expiry date of a password |
| account.unlock.cool.down.period.minutes | 60 | unlock time |
| max.invalid.login.attempts.period.minutes | 30 | window size for counting attempts for lock |
| max.invalid.login.attempts | 5 | max failed login attempts before account is locked |
| egov.state.level.tenant.id | pb |  |

### Integration <a id="Integration"></a>

#### Integration Scope <a id="Integration-Scope"></a>

User data management and functionality to login and logout into Digit system using OTP and password.

#### Integration Benefits <a id="Integration-Benefits"></a>

Providing following functionality to citizen and employee type users

*  Employee:
  * User registration
  * Search user
  * Update user details
  * Forgot password
  * Change password
  * User role mapping\(Single ULB to multiple roles\)
  * Enable employee to login into DIGIT system based on a password.
* Citizen:
  * Create user
  * Update user
  * Search user
  * User registration using OTP
  * OTP based login

#### Steps to Integration <a id="Steps-to-Integration"></a>

* To integrate, host of egov-user should be overwritten in the helm chart.
* Use /citizen/\_create and /users/\_createnovalidate endpoints for creating users into the system
* Use /v1/\_search and /\_search endpoints to search users in the system depending on various search parameters
* Use /profile/\_update for partial update and /users/\_updatenovalidate for update
* Use /password/nologin/\_update for otp based password reset and /password/\_update for logged in user password reset
* Use /user/oauth/token for generating token, /\_logoutfor logout and /\_details for getting user information from his token

### Reference Docs <a id="Reference-Docs"></a>

#### Doc Links <a id="Doc-Links"></a>

| **Title**  | **Link** |
| :--- | :--- |
| User service Product requirement | [User Service](https://digit-discuss.atlassian.net/l/c/9ih2SBox) |
| User Data encryption promotion details | [User data encryption promotion](https://digit-discuss.atlassian.net/l/c/xSSnmk12) |
| Encryption Service | [Encryption Service](https://digit-discuss.atlassian.net/l/c/HJwxmms6) |

#### API List <a id="API-List"></a>

|  | **Link** |
| :--- | :--- |
| /citizen/\_create | [https://www.getpostman.com/collections/15443fcb25c8aacd8897](https://www.getpostman.com/collections/15443fcb25c8aacd8897) |
| /users/\_createnovalidate | [https://www.getpostman.com/collections/15443fcb25c8aacd8897](https://www.getpostman.com/collections/15443fcb25c8aacd8897) |
| /\_search | [https://www.getpostman.com/collections/15443fcb25c8aacd8897](https://www.getpostman.com/collections/15443fcb25c8aacd8897) |
| /v1/\_search | [https://www.getpostman.com/collections/15443fcb25c8aacd8897](https://www.getpostman.com/collections/15443fcb25c8aacd8897) |
| /\_details | [https://www.getpostman.com/collections/15443fcb25c8aacd8897](https://www.getpostman.com/collections/15443fcb25c8aacd8897) |
| /users/\_updatenovalidate | [https://www.getpostman.com/collections/15443fcb25c8aacd8897](https://www.getpostman.com/collections/15443fcb25c8aacd8897) |
| /profile/\_update | [https://www.getpostman.com/collections/15443fcb25c8aacd8897](https://www.getpostman.com/collections/15443fcb25c8aacd8897) |
| /password/\_update | [https://www.getpostman.com/collections/15443fcb25c8aacd8897](https://www.getpostman.com/collections/15443fcb25c8aacd8897) |
| /password/nologin/\_update | [https://www.getpostman.com/collections/15443fcb25c8aacd8897](https://www.getpostman.com/collections/15443fcb25c8aacd8897) |
| /\_logout | [https://www.getpostman.com/collections/15443fcb25c8aacd8897](https://www.getpostman.com/collections/15443fcb25c8aacd8897) |
| /user/oauth/token | [https://www.getpostman.com/collections/15443fcb25c8aacd8897](https://www.getpostman.com/collections/15443fcb25c8aacd8897) |
