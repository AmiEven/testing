Security Insights
=================

API spec for Microsoft.SecurityInsights (Azure Security Insights)
resource provider

More information: [https://helloreverb.com](https://helloreverb.com)

Contact Info: [hello@helloreverb.com](hello@helloreverb.com)

Version: 2020-01-01

BasePath:

All rights reserved

http://apache.org/licenses/LICENSE-2.0.html

Access
------

1.  OAuth
    AuthorizationUrl:https://login.microsoftonline.com/common/oauth2/authorizeTokenUrl:

Methods
-------

[ Jump to [Models](#__Models) ]

### Table of Contents

#### [Actions](#Actions)

-   [`get /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.OperationalInsights/workspaces/{workspaceName}/providers/Microsoft.SecurityInsights/alertRules/{ruleId}/actions`](#actionsListByAlertRule)
-   [`put /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.OperationalInsights/workspaces/{workspaceName}/providers/Microsoft.SecurityInsights/alertRules/{ruleId}/actions/{actionId}`](#alertRulesCreateOrUpdateAction)
-   [`delete /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.OperationalInsights/workspaces/{workspaceName}/providers/Microsoft.SecurityInsights/alertRules/{ruleId}/actions/{actionId}`](#alertRulesDeleteAction)
-   [`get /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.OperationalInsights/workspaces/{workspaceName}/providers/Microsoft.SecurityInsights/alertRules/{ruleId}/actions/{actionId}`](#alertRulesGetAction)

#### [AlertRules](#AlertRules)

-   [`put /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.OperationalInsights/workspaces/{workspaceName}/providers/Microsoft.SecurityInsights/alertRules/{ruleId}`](#alertRulesCreateOrUpdate)
-   [`delete /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.OperationalInsights/workspaces/{workspaceName}/providers/Microsoft.SecurityInsights/alertRules/{ruleId}`](#alertRulesDelete)
-   [`get /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.OperationalInsights/workspaces/{workspaceName}/providers/Microsoft.SecurityInsights/alertRules/{ruleId}`](#alertRulesGet)
-   [`get /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.OperationalInsights/workspaces/{workspaceName}/providers/Microsoft.SecurityInsights/alertRules`](#alertRulesList)

#### [DataConnectors](#DataConnectors)

-   [`put /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.OperationalInsights/workspaces/{workspaceName}/providers/Microsoft.SecurityInsights/dataConnectors/{dataConnectorId}`](#dataConnectorsCreateOrUpdate)
-   [`delete /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.OperationalInsights/workspaces/{workspaceName}/providers/Microsoft.SecurityInsights/dataConnectors/{dataConnectorId}`](#dataConnectorsDelete)
-   [`get /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.OperationalInsights/workspaces/{workspaceName}/providers/Microsoft.SecurityInsights/dataConnectors/{dataConnectorId}`](#dataConnectorsGet)
-   [`get /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.OperationalInsights/workspaces/{workspaceName}/providers/Microsoft.SecurityInsights/dataConnectors`](#dataConnectorsList)

#### [Default](#Default)

-   [`get /providers/Microsoft.SecurityInsights/operations`](#operationsList)

Actions
=======

[Up](#__Methods)

``` {.get}
get /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.OperationalInsights/workspaces/{workspaceName}/providers/Microsoft.SecurityInsights/alertRules/{ruleId}/actions
```

(actionsListByAlertRule)

Gets all actions of alert rule.

### Path parameters {.field-label}

subscriptionId (required)

Path Parameter — Azure subscription ID

resourceGroupName (required)

Path Parameter — The name of the resource group within the user's
subscription. The name is case insensitive.

workspaceName (required)

Path Parameter — The name of the workspace.

ruleId (required)

Path Parameter — Alert rule ID

### Consumes {.field-label}

This API call consumes the following media types via the Content-Type
request header:

-   `application/json`

### Query parameters {.field-label}

api-version (required)

Query Parameter — API version for the operation

### Return type {.field-label}

[ActionsList](#ActionsList)

### Example data {.field-label}

Content-Type: application/json

``` {.example}
{
  "value" : [ "", "" ],
  "nextLink" : "nextLink"
}
```

### Produces {.field-label}

This API call produces the following media types according to the Accept
request header; the media type will be conveyed by the Content-Type
response header.

-   `application/json`

### Responses {.field-label}

#### 200 {.field-label}

OK [ActionsList](#ActionsList)

#### default {.field-label}

Error response describing why the operation failed.
[CloudError](#CloudError)

* * * * *

[Up](#__Methods)

``` {.put}
put /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.OperationalInsights/workspaces/{workspaceName}/providers/Microsoft.SecurityInsights/alertRules/{ruleId}/actions/{actionId}
```

(alertRulesCreateOrUpdateAction)

Creates or updates the action of alert rule.

### Path parameters {.field-label}

subscriptionId (required)

Path Parameter — Azure subscription ID

resourceGroupName (required)

Path Parameter — The name of the resource group within the user's
subscription. The name is case insensitive.

workspaceName (required)

Path Parameter — The name of the workspace.

ruleId (required)

Path Parameter — Alert rule ID

actionId (required)

Path Parameter — Action ID

### Consumes {.field-label}

This API call consumes the following media types via the Content-Type
request header:

-   `application/json`

### Request body {.field-label}

action [ActionRequest](#ActionRequest) (required)

Body Parameter — The action

### Query parameters {.field-label}

api-version (required)

Query Parameter — API version for the operation

### Return type {.field-label}

[ActionResponse](#ActionResponse)

### Example data {.field-label}

Content-Type: application/json

``` {.example}
""
```

### Produces {.field-label}

This API call produces the following media types according to the Accept
request header; the media type will be conveyed by the Content-Type
response header.

-   `application/json`

### Responses {.field-label}

#### 200 {.field-label}

OK [ActionResponse](#ActionResponse)

#### 201 {.field-label}

Created [ActionResponse](#ActionResponse)

#### default {.field-label}

Error response describing why the operation failed.
[CloudError](#CloudError)

* * * * *

[Up](#__Methods)

``` {.delete}
delete /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.OperationalInsights/workspaces/{workspaceName}/providers/Microsoft.SecurityInsights/alertRules/{ruleId}/actions/{actionId}
```

(alertRulesDeleteAction)

Delete the action of alert rule.

### Path parameters {.field-label}

subscriptionId (required)

Path Parameter — Azure subscription ID

resourceGroupName (required)

Path Parameter — The name of the resource group within the user's
subscription. The name is case insensitive.

workspaceName (required)

Path Parameter — The name of the workspace.

ruleId (required)

Path Parameter — Alert rule ID

actionId (required)

Path Parameter — Action ID

### Consumes {.field-label}

This API call consumes the following media types via the Content-Type
request header:

-   `application/json`

### Query parameters {.field-label}

api-version (required)

Query Parameter — API version for the operation

### Produces {.field-label}

This API call produces the following media types according to the Accept
request header; the media type will be conveyed by the Content-Type
response header.

-   `application/json`

### Responses {.field-label}

#### 200 {.field-label}

OK [](#)

#### 204 {.field-label}

No Content [](#)

#### default {.field-label}

Error response describing why the operation failed.
[CloudError](#CloudError)

* * * * *

[Up](#__Methods)

``` {.get}
get /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.OperationalInsights/workspaces/{workspaceName}/providers/Microsoft.SecurityInsights/alertRules/{ruleId}/actions/{actionId}
```

(alertRulesGetAction)

Gets the action of alert rule.

### Path parameters {.field-label}

subscriptionId (required)

Path Parameter — Azure subscription ID

resourceGroupName (required)

Path Parameter — The name of the resource group within the user's
subscription. The name is case insensitive.

workspaceName (required)

Path Parameter — The name of the workspace.

ruleId (required)

Path Parameter — Alert rule ID

actionId (required)

Path Parameter — Action ID

### Consumes {.field-label}

This API call consumes the following media types via the Content-Type
request header:

-   `application/json`

### Query parameters {.field-label}

api-version (required)

Query Parameter — API version for the operation

### Return type {.field-label}

[ActionResponse](#ActionResponse)

### Example data {.field-label}

Content-Type: application/json

``` {.example}
""
```

### Produces {.field-label}

This API call produces the following media types according to the Accept
request header; the media type will be conveyed by the Content-Type
response header.

-   `application/json`

### Responses {.field-label}

#### 200 {.field-label}

OK [ActionResponse](#ActionResponse)

#### default {.field-label}

Error response describing why the operation failed.
[CloudError](#CloudError)

* * * * *

AlertRules
==========

[Up](#__Methods)

``` {.put}
put /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.OperationalInsights/workspaces/{workspaceName}/providers/Microsoft.SecurityInsights/alertRules/{ruleId}
```

(alertRulesCreateOrUpdate)

Creates or updates the alert rule.

### Path parameters {.field-label}

subscriptionId (required)

Path Parameter — Azure subscription ID

resourceGroupName (required)

Path Parameter — The name of the resource group within the user's
subscription. The name is case insensitive.

workspaceName (required)

Path Parameter — The name of the workspace.

ruleId (required)

Path Parameter — Alert rule ID

### Consumes {.field-label}

This API call consumes the following media types via the Content-Type
request header:

-   `application/json`

### Request body {.field-label}

alertRule [AlertRule](#AlertRule) (required)

Body Parameter — The alert rule

### Query parameters {.field-label}

api-version (required)

Query Parameter — API version for the operation

### Return type {.field-label}

[AlertRule](#AlertRule)

### Example data {.field-label}

Content-Type: application/json

``` {.example}
""
```

### Produces {.field-label}

This API call produces the following media types according to the Accept
request header; the media type will be conveyed by the Content-Type
response header.

-   `application/json`

### Responses {.field-label}

#### 200 {.field-label}

OK [AlertRule](#AlertRule)

#### 201 {.field-label}

Created [AlertRule](#AlertRule)

#### default {.field-label}

Error response describing why the operation failed.
[CloudError](#CloudError)

* * * * *

[Up](#__Methods)

``` {.delete}
delete /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.OperationalInsights/workspaces/{workspaceName}/providers/Microsoft.SecurityInsights/alertRules/{ruleId}
```

(alertRulesDelete)

Delete the alert rule.

### Path parameters {.field-label}

subscriptionId (required)

Path Parameter — Azure subscription ID

resourceGroupName (required)

Path Parameter — The name of the resource group within the user's
subscription. The name is case insensitive.

workspaceName (required)

Path Parameter — The name of the workspace.

ruleId (required)

Path Parameter — Alert rule ID

### Consumes {.field-label}

This API call consumes the following media types via the Content-Type
request header:

-   `application/json`

### Query parameters {.field-label}

api-version (required)

Query Parameter — API version for the operation

### Produces {.field-label}

This API call produces the following media types according to the Accept
request header; the media type will be conveyed by the Content-Type
response header.

-   `application/json`

### Responses {.field-label}

#### 200 {.field-label}

OK [](#)

#### 204 {.field-label}

No Content [](#)

#### default {.field-label}

Error response describing why the operation failed.
[CloudError](#CloudError)

* * * * *

[Up](#__Methods)

``` {.get}
get /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.OperationalInsights/workspaces/{workspaceName}/providers/Microsoft.SecurityInsights/alertRules/{ruleId}
```

(alertRulesGet)

Gets the alert rule.

### Path parameters {.field-label}

subscriptionId (required)

Path Parameter — Azure subscription ID

resourceGroupName (required)

Path Parameter — The name of the resource group within the user's
subscription. The name is case insensitive.

workspaceName (required)

Path Parameter — The name of the workspace.

ruleId (required)

Path Parameter — Alert rule ID

### Consumes {.field-label}

This API call consumes the following media types via the Content-Type
request header:

-   `application/json`

### Query parameters {.field-label}

api-version (required)

Query Parameter — API version for the operation

### Return type {.field-label}

[AlertRule](#AlertRule)

### Example data {.field-label}

Content-Type: application/json

``` {.example}
""
```

### Produces {.field-label}

This API call produces the following media types according to the Accept
request header; the media type will be conveyed by the Content-Type
response header.

-   `application/json`

### Responses {.field-label}

#### 200 {.field-label}

OK [AlertRule](#AlertRule)

#### default {.field-label}

Error response describing why the operation failed.
[CloudError](#CloudError)

* * * * *

[Up](#__Methods)

``` {.get}
get /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.OperationalInsights/workspaces/{workspaceName}/providers/Microsoft.SecurityInsights/alertRules
```

(alertRulesList)

Gets all alert rules.

### Path parameters {.field-label}

subscriptionId (required)

Path Parameter — Azure subscription ID

resourceGroupName (required)

Path Parameter — The name of the resource group within the user's
subscription. The name is case insensitive.

workspaceName (required)

Path Parameter — The name of the workspace.

### Consumes {.field-label}

This API call consumes the following media types via the Content-Type
request header:

-   `application/json`

### Query parameters {.field-label}

api-version (required)

Query Parameter — API version for the operation

### Return type {.field-label}

[AlertRulesList](#AlertRulesList)

### Example data {.field-label}

Content-Type: application/json

``` {.example}
{
  "value" : [ "", "" ],
  "nextLink" : "nextLink"
}
```

### Produces {.field-label}

This API call produces the following media types according to the Accept
request header; the media type will be conveyed by the Content-Type
response header.

-   `application/json`

### Responses {.field-label}

#### 200 {.field-label}

OK [AlertRulesList](#AlertRulesList)

#### default {.field-label}

Error response describing why the operation failed.
[CloudError](#CloudError)

* * * * *

DataConnectors
==============

[Up](#__Methods)

``` {.put}
put /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.OperationalInsights/workspaces/{workspaceName}/providers/Microsoft.SecurityInsights/dataConnectors/{dataConnectorId}
```

(dataConnectorsCreateOrUpdate)

Creates or updates the data connector.

### Path parameters {.field-label}

subscriptionId (required)

Path Parameter — Azure subscription ID

resourceGroupName (required)

Path Parameter — The name of the resource group within the user's
subscription. The name is case insensitive.

workspaceName (required)

Path Parameter — The name of the workspace.

dataConnectorId (required)

Path Parameter — Connector ID

### Consumes {.field-label}

This API call consumes the following media types via the Content-Type
request header:

-   `application/json`

### Request body {.field-label}

dataConnector [DataConnector](#DataConnector) (required)

Body Parameter — The data connector

### Query parameters {.field-label}

api-version (required)

Query Parameter — API version for the operation

### Return type {.field-label}

[DataConnector](#DataConnector)

### Example data {.field-label}

Content-Type: application/json

``` {.example}
""
```

### Produces {.field-label}

This API call produces the following media types according to the Accept
request header; the media type will be conveyed by the Content-Type
response header.

-   `application/json`

### Responses {.field-label}

#### 200 {.field-label}

OK [DataConnector](#DataConnector)

#### 201 {.field-label}

Created [DataConnector](#DataConnector)

#### default {.field-label}

Error response describing why the operation failed.
[CloudError](#CloudError)

* * * * *

[Up](#__Methods)

``` {.delete}
delete /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.OperationalInsights/workspaces/{workspaceName}/providers/Microsoft.SecurityInsights/dataConnectors/{dataConnectorId}
```

(dataConnectorsDelete)

Delete the data connector.

### Path parameters {.field-label}

subscriptionId (required)

Path Parameter — Azure subscription ID

resourceGroupName (required)

Path Parameter — The name of the resource group within the user's
subscription. The name is case insensitive.

workspaceName (required)

Path Parameter — The name of the workspace.

dataConnectorId (required)

Path Parameter — Connector ID

### Consumes {.field-label}

This API call consumes the following media types via the Content-Type
request header:

-   `application/json`

### Query parameters {.field-label}

api-version (required)

Query Parameter — API version for the operation

### Produces {.field-label}

This API call produces the following media types according to the Accept
request header; the media type will be conveyed by the Content-Type
response header.

-   `application/json`

### Responses {.field-label}

#### 200 {.field-label}

OK [](#)

#### 204 {.field-label}

No Content [](#)

#### default {.field-label}

Error response describing why the operation failed.
[CloudError](#CloudError)

* * * * *

[Up](#__Methods)

``` {.get}
get /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.OperationalInsights/workspaces/{workspaceName}/providers/Microsoft.SecurityInsights/dataConnectors/{dataConnectorId}
```

(dataConnectorsGet)

Gets a data connector.

### Path parameters {.field-label}

subscriptionId (required)

Path Parameter — Azure subscription ID

resourceGroupName (required)

Path Parameter — The name of the resource group within the user's
subscription. The name is case insensitive.

workspaceName (required)

Path Parameter — The name of the workspace.

dataConnectorId (required)

Path Parameter — Connector ID

### Consumes {.field-label}

This API call consumes the following media types via the Content-Type
request header:

-   `application/json`

### Query parameters {.field-label}

api-version (required)

Query Parameter — API version for the operation

### Return type {.field-label}

[DataConnector](#DataConnector)

### Example data {.field-label}

Content-Type: application/json

``` {.example}
""
```

### Produces {.field-label}

This API call produces the following media types according to the Accept
request header; the media type will be conveyed by the Content-Type
response header.

-   `application/json`

### Responses {.field-label}

#### 200 {.field-label}

OK [DataConnector](#DataConnector)

#### default {.field-label}

Error response describing why the operation failed.
[CloudError](#CloudError)

* * * * *

[Up](#__Methods)

``` {.get}
get /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.OperationalInsights/workspaces/{workspaceName}/providers/Microsoft.SecurityInsights/dataConnectors
```

(dataConnectorsList)

Gets all data connectors.

### Path parameters {.field-label}

subscriptionId (required)

Path Parameter — Azure subscription ID

resourceGroupName (required)

Path Parameter — The name of the resource group within the user's
subscription. The name is case insensitive.

workspaceName (required)

Path Parameter — The name of the workspace.

### Consumes {.field-label}

This API call consumes the following media types via the Content-Type
request header:

-   `application/json`

### Query parameters {.field-label}

api-version (required)

Query Parameter — API version for the operation

### Return type {.field-label}

[DataConnectorList](#DataConnectorList)

### Example data {.field-label}

Content-Type: application/json

``` {.example}
{
  "value" : [ "", "" ],
  "nextLink" : "nextLink"
}
```

### Produces {.field-label}

This API call produces the following media types according to the Accept
request header; the media type will be conveyed by the Content-Type
response header.

-   `application/json`

### Responses {.field-label}

#### 200 {.field-label}

OK [DataConnectorList](#DataConnectorList)

#### default {.field-label}

Error response describing why the operation failed.
[CloudError](#CloudError)

* * * * *

Default
=======

[Up](#__Methods)

``` {.get}
get /providers/Microsoft.SecurityInsights/operations
```

(operationsList)

Lists all operations available Azure Security Insights Resource
Provider.

### Consumes {.field-label}

This API call consumes the following media types via the Content-Type
request header:

-   `application/json`

### Query parameters {.field-label}

api-version (required)

Query Parameter — API version for the operation

### Return type {.field-label}

[OperationsList](#OperationsList)

### Example data {.field-label}

Content-Type: application/json

``` {.example}
{
  "value" : [ {
    "display" : {
      "provider" : "provider",
      "resource" : "resource",
      "description" : "description",
      "operation" : "operation"
    },
    "name" : "name"
  }, {
    "display" : {
      "provider" : "provider",
      "resource" : "resource",
      "description" : "description",
      "operation" : "operation"
    },
    "name" : "name"
  } ],
  "nextLink" : "nextLink"
}
```

### Produces {.field-label}

This API call produces the following media types according to the Accept
request header; the media type will be conveyed by the Content-Type
response header.

-   `application/json`

### Responses {.field-label}

#### 200 {.field-label}

OK. Successfully retrieved operations list.
[OperationsList](#OperationsList)

#### default {.field-label}

Error response describing why the operation failed.
[CloudError](#CloudError)

* * * * *

Models
------

[ Jump to [Methods](#__Methods) ]

### Table of Contents

1.  [`AADDataConnector` -](#AADDataConnector)
2.  [`AADDataConnectorProperties` -](#AADDataConnectorProperties)
3.  [`AATPDataConnector` -](#AATPDataConnector)
4.  [`AATPDataConnectorProperties` -](#AATPDataConnectorProperties)
5.  [`ASCDataConnector` -](#ASCDataConnector)
6.  [`ASCDataConnectorProperties` -](#ASCDataConnectorProperties)
7.  [`ActionPropertiesBase` -](#ActionPropertiesBase)
8.  [`ActionRequest` -](#ActionRequest)
9.  [`ActionRequestProperties` -](#ActionRequestProperties)
10. [`ActionResponse` -](#ActionResponse)
11. [`ActionResponseProperties` -](#ActionResponseProperties)
12. [`ActionsList` -](#ActionsList)
13. [`AlertRule` -](#AlertRule)
14. [`AlertRuleKind` -](#AlertRuleKind)
15. [`AlertRuleTemplate` -](#AlertRuleTemplate)
16. [`AlertRuleTemplateDataSource` -](#AlertRuleTemplateDataSource)
17. [`AlertRuleTemplatePropertiesBase`
    -](#AlertRuleTemplatePropertiesBase)
18. [`AlertRuleTriggerOperator` -](#AlertRuleTriggerOperator)
19. [`AlertRulesList` -](#AlertRulesList)
20. [`AlertSeverity` -](#AlertSeverity)
21. [`AlertsDataTypeOfDataConnector` -](#AlertsDataTypeOfDataConnector)
22. [`AttackTactic` -](#AttackTactic)
23. [`AwsCloudTrailDataConnector` -](#AwsCloudTrailDataConnector)
24. [`AwsCloudTrailDataConnectorDataTypes`
    -](#AwsCloudTrailDataConnectorDataTypes)
25. [`AwsCloudTrailDataConnectorProperties`
    -](#AwsCloudTrailDataConnectorProperties)
26. [`CloudError` -](#CloudError)
27. [`CloudErrorBody` -](#CloudErrorBody)
28. [`DataConnector` -](#DataConnector)
29. [`DataConnectorDataTypeCommon` -](#DataConnectorDataTypeCommon)
30. [`DataConnectorKind` -](#DataConnectorKind)
31. [`DataConnectorList` -](#DataConnectorList)
32. [`DataConnectorTenantId` -](#DataConnectorTenantId)
33. [`DataConnectorWithAlertsProperties`
    -](#DataConnectorWithAlertsProperties)
34. [`FusionAlertRule` -](#FusionAlertRule)
35. [`FusionAlertRuleProperties` -](#FusionAlertRuleProperties)
36. [`FusionAlertRuleTemplate` -](#FusionAlertRuleTemplate)
37. [`IncidentInfo` -](#IncidentInfo)
38. [`Label` -](#Label)
39. [`MCASDataConnector` -](#MCASDataConnector)
40. [`MCASDataConnectorDataTypes` -](#MCASDataConnectorDataTypes)
41. [`MCASDataConnectorProperties` -](#MCASDataConnectorProperties)
42. [`MDATPDataConnector` -](#MDATPDataConnector)
43. [`MDATPDataConnectorProperties` -](#MDATPDataConnectorProperties)
44. [`MicrosoftSecurityIncidentCreationAlertRule`
    -](#MicrosoftSecurityIncidentCreationAlertRule)
45. [`MicrosoftSecurityIncidentCreationAlertRuleCommonProperties`
    -](#MicrosoftSecurityIncidentCreationAlertRuleCommonProperties)
46. [`MicrosoftSecurityIncidentCreationAlertRuleProperties`
    -](#MicrosoftSecurityIncidentCreationAlertRuleProperties)
47. [`MicrosoftSecurityIncidentCreationAlertRuleTemplate`
    -](#MicrosoftSecurityIncidentCreationAlertRuleTemplate)
48. [`OfficeConsent` -](#OfficeConsent)
49. [`OfficeConsentList` -](#OfficeConsentList)
50. [`OfficeConsentProperties` -](#OfficeConsentProperties)
51. [`OfficeDataConnector` -](#OfficeDataConnector)
52. [`OfficeDataConnectorDataTypes` -](#OfficeDataConnectorDataTypes)
53. [`OfficeDataConnectorProperties` -](#OfficeDataConnectorProperties)
54. [`Operation` -](#Operation)
55. [`Operation_display` -](#Operation_display)
56. [`OperationsList` -](#OperationsList)
57. [`Resource` -](#Resource)
58. [`ResourceWithEtag` -](#ResourceWithEtag)
59. [`ScheduledAlertRule` -](#ScheduledAlertRule)
60. [`ScheduledAlertRuleCommonProperties`
    -](#ScheduledAlertRuleCommonProperties)
61. [`ScheduledAlertRuleProperties` -](#ScheduledAlertRuleProperties)
62. [`ScheduledAlertRuleTemplate` -](#ScheduledAlertRuleTemplate)
63. [`Settings` -](#Settings)
64. [`SettingsKind` -](#SettingsKind)
65. [`TIDataConnector` -](#TIDataConnector)
66. [`TIDataConnectorDataTypes` -](#TIDataConnectorDataTypes)
67. [`TIDataConnectorProperties` -](#TIDataConnectorProperties)
68. [`ThreatIntelligence` -](#ThreatIntelligence)
69. [`ToggleSettings` -](#ToggleSettings)
70. [`ToggleSettingsProperties` -](#ToggleSettingsProperties)
71. [`UebaSettings` -](#UebaSettings)
72. [`UebaSettingsProperties` -](#UebaSettingsProperties)
73. [`UserInfo` -](#UserInfo)

### `AADDataConnector` - [Up](#__Models)

Represents AAD (Azure Active Directory) data connector.

id (optional)

[String](#string) Azure resource Id

name (optional)

[String](#string) Azure resource name

type (optional)

[String](#string) Azure resource type

etag (optional)

[String](#string) Etag of the azure resource

kind (optional)

[String](#string) The kind of the data connector

Enum:

AzureActiveDirectory

AzureSecurityCenter

MicrosoftCloudAppSecurity

ThreatIntelligence

Office365

AmazonWebServicesCloudTrail

AzureAdvancedThreatProtection

MicrosoftDefenderAdvancedThreatProtection

properties (optional)

[AADDataConnectorProperties](#AADDataConnectorProperties) AAD (Azure
Active Directory) data connector properties.

### `AADDataConnectorProperties` - [Up](#__Models)

AAD (Azure Active Directory) data connector properties.

tenantId (optional)

[String](#string) The tenant id to connect to, and get the data from.

dataTypes (optional)

[AlertsDataTypeOfDataConnector](#AlertsDataTypeOfDataConnector) The
available data types for the connector.

### `AATPDataConnector` - [Up](#__Models)

Represents AATP (Azure Advanced Threat Protection) data connector.

id (optional)

[String](#string) Azure resource Id

name (optional)

[String](#string) Azure resource name

type (optional)

[String](#string) Azure resource type

etag (optional)

[String](#string) Etag of the azure resource

kind (optional)

[String](#string) The kind of the data connector

Enum:

AzureActiveDirectory

AzureSecurityCenter

MicrosoftCloudAppSecurity

ThreatIntelligence

Office365

AmazonWebServicesCloudTrail

AzureAdvancedThreatProtection

MicrosoftDefenderAdvancedThreatProtection

properties (optional)

[AATPDataConnectorProperties](#AATPDataConnectorProperties) AATP (Azure
Advanced Threat Protection) data connector properties.

### `AATPDataConnectorProperties` - [Up](#__Models)

AATP (Azure Advanced Threat Protection) data connector properties.

tenantId (optional)

[String](#string) The tenant id to connect to, and get the data from.

dataTypes (optional)

[AlertsDataTypeOfDataConnector](#AlertsDataTypeOfDataConnector) The
available data types for the connector.

### `ASCDataConnector` - [Up](#__Models)

Represents ASC (Azure Security Center) data connector.

id (optional)

[String](#string) Azure resource Id

name (optional)

[String](#string) Azure resource name

type (optional)

[String](#string) Azure resource type

etag (optional)

[String](#string) Etag of the azure resource

kind (optional)

[String](#string) The kind of the data connector

Enum:

AzureActiveDirectory

AzureSecurityCenter

MicrosoftCloudAppSecurity

ThreatIntelligence

Office365

AmazonWebServicesCloudTrail

AzureAdvancedThreatProtection

MicrosoftDefenderAdvancedThreatProtection

properties (optional)

[ASCDataConnectorProperties](#ASCDataConnectorProperties) ASC (Azure
Security Center) data connector properties.

### `ASCDataConnectorProperties` - [Up](#__Models)

ASC (Azure Security Center) data connector properties.

dataTypes (optional)

[AlertsDataTypeOfDataConnector](#AlertsDataTypeOfDataConnector) The
available data types for the connector.

subscriptionId (optional)

[String](#string) The subscription id to connect to, and get the data
from.

### `ActionPropertiesBase` - [Up](#__Models)

Action property bag base.

logicAppResourceId

[String](#string) Logic App Resource Id,
providers/Microsoft.Logic/workflows/{WorkflowID}.

### `ActionRequest` - [Up](#__Models)

Action for alert rule.

id (optional)

[String](#string) Azure resource Id

name (optional)

[String](#string) Azure resource name

type (optional)

[String](#string) Azure resource type

etag (optional)

[String](#string) Etag of the azure resource

properties (optional)

[ActionRequestProperties](#ActionRequestProperties) Action properties
for put request

### `ActionRequestProperties` - [Up](#__Models)

Action property bag.

logicAppResourceId

[String](#string) Logic App Resource Id,
providers/Microsoft.Logic/workflows/{WorkflowID}.

triggerUri (optional)

[String](#string) Logic App Callback URL for this specific workflow.

### `ActionResponse` - [Up](#__Models)

Action for alert rule.

id (optional)

[String](#string) Azure resource Id

name (optional)

[String](#string) Azure resource name

type (optional)

[String](#string) Azure resource type

etag (optional)

[String](#string) Etag of the action.

properties (optional)

[ActionResponseProperties](#ActionResponseProperties) Action properties
for get request

### `ActionResponseProperties` - [Up](#__Models)

Action property bag.

logicAppResourceId

[String](#string) Logic App Resource Id,
providers/Microsoft.Logic/workflows/{WorkflowID}.

workflowId (optional)

[String](#string) The name of the logic app's workflow.

### `ActionsList` - [Up](#__Models)

List all the actions.

nextLink (optional)

[String](#string) URL to fetch the next set of actions.

value

[array[ActionResponse]](#ActionResponse) Array of actions.

### `AlertRule` - [Up](#__Models)

Alert rule.

id (optional)

[String](#string) Azure resource Id

name (optional)

[String](#string) Azure resource name

type (optional)

[String](#string) Azure resource type

etag (optional)

[String](#string) Etag of the azure resource

kind

[String](#string) The kind of the alert rule

Enum:

Scheduled

MicrosoftSecurityIncidentCreation

Fusion

### `AlertRuleKind` - [Up](#__Models)

Describes an Azure resource with kind.

kind

[String](#string) The kind of the alert rule

Enum:

Scheduled

MicrosoftSecurityIncidentCreation

Fusion

### `AlertRuleTemplate` - [Up](#__Models)

Alert rule template.

id (optional)

[String](#string) Azure resource Id

name (optional)

[String](#string) Azure resource name

type (optional)

[String](#string) Azure resource type

kind

[String](#string) The kind of the alert rule

Enum:

Scheduled

MicrosoftSecurityIncidentCreation

Fusion

### `AlertRuleTemplateDataSource` - [Up](#__Models)

alert rule template data sources

connectorId (optional)

[String](#string) The connector id that provides the following data
types

dataTypes (optional)

[array[String]](#string) The data types used by the alert rule template

### `AlertRuleTemplatePropertiesBase` - [Up](#__Models)

Base alert rule template property bag.

alertRulesCreatedByTemplateCount (optional)

[Integer](#integer) the number of alert rules that were created by this
template

createdDateUTC (optional)

[Date](#DateTime) The time that this alert rule template has been added.
format: date-time

description (optional)

[String](#string) The description of the alert rule template.

displayName (optional)

[String](#string) The display name for alert rule template.

requiredDataConnectors (optional)

[array[AlertRuleTemplateDataSource]](#AlertRuleTemplateDataSource) The
required data connectors for this template

status (optional)

[String](#string) The alert rule template status.

Enum:

Installed

Available

NotAvailable

### `AlertRuleTriggerOperator` - [Up](#__Models)

The operation against the threshold that triggers alert rule.

### `AlertRulesList` - [Up](#__Models)

List all the alert rules.

nextLink (optional)

[String](#string) URL to fetch the next set of alert rules.

value

[array[AlertRule]](#AlertRule) Array of alert rules.

### `AlertSeverity` - [Up](#__Models)

The severity of the alert

### `AlertsDataTypeOfDataConnector` - [Up](#__Models)

Alerts data type for data connectors.

alerts (optional)

[Object](#object) Alerts data type connection.

### `AttackTactic` - [Up](#__Models)

The severity for alerts created by this alert rule.

### `AwsCloudTrailDataConnector` - [Up](#__Models)

Represents Amazon Web Services CloudTrail data connector.

id (optional)

[String](#string) Azure resource Id

name (optional)

[String](#string) Azure resource name

type (optional)

[String](#string) Azure resource type

etag (optional)

[String](#string) Etag of the azure resource

kind (optional)

[String](#string) The kind of the data connector

Enum:

AzureActiveDirectory

AzureSecurityCenter

MicrosoftCloudAppSecurity

ThreatIntelligence

Office365

AmazonWebServicesCloudTrail

AzureAdvancedThreatProtection

MicrosoftDefenderAdvancedThreatProtection

properties (optional)

[AwsCloudTrailDataConnectorProperties](#AwsCloudTrailDataConnectorProperties)
Amazon Web Services CloudTrail data connector properties.

### `AwsCloudTrailDataConnectorDataTypes` - [Up](#__Models)

The available data types for Amazon Web Services CloudTrail data
connector.

logs (optional)

[Object](#object) Logs data type.

### `AwsCloudTrailDataConnectorProperties` - [Up](#__Models)

Amazon Web Services CloudTrail data connector properties.

awsRoleArn (optional)

[String](#string) The Aws Role Arn (with CloudTrailReadOnly policy) that
is used to access the Aws account.

dataTypes (optional)

[AwsCloudTrailDataConnectorDataTypes](#AwsCloudTrailDataConnectorDataTypes)
The available data types for the connector.

### `CloudError` - [Up](#__Models)

Error response structure.

error (optional)

[CloudErrorBody](#CloudErrorBody) Error data

### `CloudErrorBody` - [Up](#__Models)

Error details.

code (optional)

[String](#string) An identifier for the error. Codes are invariant and
are intended to be consumed programmatically.

message (optional)

[String](#string) A message describing the error, intended to be
suitable for display in a user interface.

### `DataConnector` - [Up](#__Models)

Data connector.

id (optional)

[String](#string) Azure resource Id

name (optional)

[String](#string) Azure resource name

type (optional)

[String](#string) Azure resource type

etag (optional)

[String](#string) Etag of the azure resource

kind (optional)

[String](#string) The kind of the data connector

Enum:

AzureActiveDirectory

AzureSecurityCenter

MicrosoftCloudAppSecurity

ThreatIntelligence

Office365

AmazonWebServicesCloudTrail

AzureAdvancedThreatProtection

MicrosoftDefenderAdvancedThreatProtection

### `DataConnectorDataTypeCommon` - [Up](#__Models)

Common field for data type in data connectors.

state (optional)

[String](#string) Describe whether this data type connection is enabled
or not.

Enum:

Enabled

Disabled

### `DataConnectorKind` - [Up](#__Models)

Describes an Azure resource with kind.

kind (optional)

[String](#string) The kind of the data connector

Enum:

AzureActiveDirectory

AzureSecurityCenter

MicrosoftCloudAppSecurity

ThreatIntelligence

Office365

AmazonWebServicesCloudTrail

AzureAdvancedThreatProtection

MicrosoftDefenderAdvancedThreatProtection

### `DataConnectorList` - [Up](#__Models)

List all the data connectors.

nextLink (optional)

[String](#string) URL to fetch the next set of data connectors.

value

[array[DataConnector]](#DataConnector) Array of data connectors.

### `DataConnectorTenantId` - [Up](#__Models)

Properties data connector on tenant level.

tenantId (optional)

[String](#string) The tenant id to connect to, and get the data from.

### `DataConnectorWithAlertsProperties` - [Up](#__Models)

Data connector properties.

dataTypes (optional)

[AlertsDataTypeOfDataConnector](#AlertsDataTypeOfDataConnector) The
available data types for the connector.

### `FusionAlertRule` - [Up](#__Models)

Represents Fusion alert rule.

id (optional)

[String](#string) Azure resource Id

name (optional)

[String](#string) Azure resource name

type (optional)

[String](#string) Azure resource type

etag (optional)

[String](#string) Etag of the azure resource

kind

[String](#string) The kind of the alert rule

Enum:

Scheduled

MicrosoftSecurityIncidentCreation

Fusion

properties (optional)

[FusionAlertRuleProperties](#FusionAlertRuleProperties) Fusion alert
rule properties

### `FusionAlertRuleProperties` - [Up](#__Models)

Fusion alert rule base property bag.

alertRuleTemplateName

[String](#string) The Name of the alert rule template used to create
this rule.

description (optional)

[String](#string) The description of the alert rule.

displayName (optional)

[String](#string) The display name for alerts created by this alert
rule.

enabled

[Boolean](#boolean) Determines whether this alert rule is enabled or
disabled.

lastModifiedUtc (optional)

[Date](#DateTime) The last time that this alert has been modified.
format: date-time

severity (optional)

[AlertSeverity](#AlertSeverity) The severity for alerts created by this
alert rule.

tactics (optional)

[array[AttackTactic]](#AttackTactic) The tactics of the alert rule

### `FusionAlertRuleTemplate` - [Up](#__Models)

Represents Fusion alert rule template.

id (optional)

[String](#string) Azure resource Id

name (optional)

[String](#string) Azure resource name

type (optional)

[String](#string) Azure resource type

kind

[String](#string) The kind of the alert rule

Enum:

Scheduled

MicrosoftSecurityIncidentCreation

Fusion

properties (optional)

[Object](#object) Fusion alert rule template properties

### `IncidentInfo` - [Up](#__Models)

Describes related incident information for the bookmark

incidentId

[String](#string) Incident Id

severity

[String](#string) The severity of the incident

Enum:

Critical

High

Medium

Low

Informational

title

[String](#string) The title of the incident

relationName

[String](#string) Relation Name

### `Label` - [Up](#__Models)

Label that will be used to tag and filter on.

### `MCASDataConnector` - [Up](#__Models)

Represents MCAS (Microsoft Cloud App Security) data connector.

id (optional)

[String](#string) Azure resource Id

name (optional)

[String](#string) Azure resource name

type (optional)

[String](#string) Azure resource type

etag (optional)

[String](#string) Etag of the azure resource

kind (optional)

[String](#string) The kind of the data connector

Enum:

AzureActiveDirectory

AzureSecurityCenter

MicrosoftCloudAppSecurity

ThreatIntelligence

Office365

AmazonWebServicesCloudTrail

AzureAdvancedThreatProtection

MicrosoftDefenderAdvancedThreatProtection

properties (optional)

[MCASDataConnectorProperties](#MCASDataConnectorProperties) MCAS
(Microsoft Cloud App Security) data connector properties.

### `MCASDataConnectorDataTypes` - [Up](#__Models)

The available data types for MCAS (Microsoft Cloud App Security) data
connector.

alerts (optional)

[Object](#object) Alerts data type connection.

discoveryLogs (optional)

[Object](#object) Discovery log data type connection.

### `MCASDataConnectorProperties` - [Up](#__Models)

MCAS (Microsoft Cloud App Security) data connector properties.

tenantId (optional)

[String](#string) The tenant id to connect to, and get the data from.

dataTypes (optional)

[MCASDataConnectorDataTypes](#MCASDataConnectorDataTypes) The available
data types for the connector.

### `MDATPDataConnector` - [Up](#__Models)

Represents MDATP (Microsoft Defender Advanced Threat Protection) data
connector.

id (optional)

[String](#string) Azure resource Id

name (optional)

[String](#string) Azure resource name

type (optional)

[String](#string) Azure resource type

etag (optional)

[String](#string) Etag of the azure resource

kind (optional)

[String](#string) The kind of the data connector

Enum:

AzureActiveDirectory

AzureSecurityCenter

MicrosoftCloudAppSecurity

ThreatIntelligence

Office365

AmazonWebServicesCloudTrail

AzureAdvancedThreatProtection

MicrosoftDefenderAdvancedThreatProtection

properties (optional)

[MDATPDataConnectorProperties](#MDATPDataConnectorProperties) MDATP
(Microsoft Defender Advanced Threat Protection) data connector
properties.

### `MDATPDataConnectorProperties` - [Up](#__Models)

MDATP (Microsoft Defender Advanced Threat Protection) data connector
properties.

tenantId (optional)

[String](#string) The tenant id to connect to, and get the data from.

dataTypes (optional)

[AlertsDataTypeOfDataConnector](#AlertsDataTypeOfDataConnector) The
available data types for the connector.

### `MicrosoftSecurityIncidentCreationAlertRule` - [Up](#__Models)

Represents MicrosoftSecurityIncidentCreation rule.

id (optional)

[String](#string) Azure resource Id

name (optional)

[String](#string) Azure resource name

type (optional)

[String](#string) Azure resource type

etag (optional)

[String](#string) Etag of the azure resource

kind

[String](#string) The kind of the alert rule

Enum:

Scheduled

MicrosoftSecurityIncidentCreation

Fusion

properties (optional)

[MicrosoftSecurityIncidentCreationAlertRuleProperties](#MicrosoftSecurityIncidentCreationAlertRuleProperties)
MicrosoftSecurityIncidentCreation rule properties

### `MicrosoftSecurityIncidentCreationAlertRuleCommonProperties` - [Up](#__Models)

MicrosoftSecurityIncidentCreation rule common property bag.

displayNamesFilter (optional)

[array[String]](#string) the alerts' displayNames on which the cases
will be generated

productFilter

[String](#string) The alerts' productName on which the cases will be
generated

Enum:

Microsoft Cloud App Security

Azure Security Center

Azure Advanced Threat Protection

Azure Active Directory Identity Protection

Azure Security Center for IoT

severitiesFilter (optional)

[array[AlertSeverity]](#AlertSeverity) the alerts' severities on which
the cases will be generated

### `MicrosoftSecurityIncidentCreationAlertRuleProperties` - [Up](#__Models)

MicrosoftSecurityIncidentCreation rule property bag.

displayNamesFilter (optional)

[array[String]](#string) the alerts' displayNames on which the cases
will be generated

productFilter

[String](#string) The alerts' productName on which the cases will be
generated

Enum:

Microsoft Cloud App Security

Azure Security Center

Azure Advanced Threat Protection

Azure Active Directory Identity Protection

Azure Security Center for IoT

severitiesFilter (optional)

[array[AlertSeverity]](#AlertSeverity) the alerts' severities on which
the cases will be generated

alertRuleTemplateName (optional)

[String](#string) The Name of the alert rule template used to create
this rule.

description (optional)

[String](#string) The description of the alert rule.

displayName (optional)

[String](#string) The display name for alerts created by this alert
rule.

enabled (optional)

[Boolean](#boolean) Determines whether this alert rule is enabled or
disabled.

lastModifiedUtc (optional)

[Date](#DateTime) The last time that this alert has been modified.
format: date-time

### `MicrosoftSecurityIncidentCreationAlertRuleTemplate` - [Up](#__Models)

Represents MicrosoftSecurityIncidentCreation rule template.

id (optional)

[String](#string) Azure resource Id

name (optional)

[String](#string) Azure resource name

type (optional)

[String](#string) Azure resource type

kind

[String](#string) The kind of the alert rule

Enum:

Scheduled

MicrosoftSecurityIncidentCreation

Fusion

properties (optional)

[Object](#object) MicrosoftSecurityIncidentCreation rule template
properties

### `OfficeConsent` - [Up](#__Models)

Consent for Office365 tenant that already made.

id (optional)

[String](#string) Azure resource Id

name (optional)

[String](#string) Azure resource name

type (optional)

[String](#string) Azure resource type

properties (optional)

[OfficeConsentProperties](#OfficeConsentProperties) Office consent
properties

### `OfficeConsentList` - [Up](#__Models)

List of all the office365 consents.

nextLink (optional)

[String](#string) URL to fetch the next set of office consents.

value

[array[OfficeConsent]](#OfficeConsent) Array of the consents.

### `OfficeConsentProperties` - [Up](#__Models)

Consent property bag.

tenantId (optional)

[String](#string) The tenantId of the Office365 with the consent.

tenantName (optional)

[String](#string) The tenant name of the Office365 with the consent.

### `OfficeDataConnector` - [Up](#__Models)

Represents office data connector.

id (optional)

[String](#string) Azure resource Id

name (optional)

[String](#string) Azure resource name

type (optional)

[String](#string) Azure resource type

etag (optional)

[String](#string) Etag of the azure resource

kind (optional)

[String](#string) The kind of the data connector

Enum:

AzureActiveDirectory

AzureSecurityCenter

MicrosoftCloudAppSecurity

ThreatIntelligence

Office365

AmazonWebServicesCloudTrail

AzureAdvancedThreatProtection

MicrosoftDefenderAdvancedThreatProtection

properties (optional)

[OfficeDataConnectorProperties](#OfficeDataConnectorProperties) Office
data connector properties.

### `OfficeDataConnectorDataTypes` - [Up](#__Models)

The available data types for office data connector.

exchange (optional)

[Object](#object) Exchange data type connection.

sharePoint (optional)

[Object](#object) SharePoint data type connection.

### `OfficeDataConnectorProperties` - [Up](#__Models)

Office data connector properties.

tenantId (optional)

[String](#string) The tenant id to connect to, and get the data from.

dataTypes (optional)

[OfficeDataConnectorDataTypes](#OfficeDataConnectorDataTypes) The
available data types for the connector.

### `Operation` - [Up](#__Models)

Operation provided by provider

display (optional)

[Operation\_display](#Operation_display)

name (optional)

[String](#string) Name of the operation

### `Operation_display` - [Up](#__Models)

Properties of the operation

description (optional)

[String](#string) Description of the operation

operation (optional)

[String](#string) Operation name

provider (optional)

[String](#string) Provider name

resource (optional)

[String](#string) Resource name

### `OperationsList` - [Up](#__Models)

Lists the operations available in the SecurityInsights RP.

nextLink (optional)

[String](#string) URL to fetch the next set of operations.

value

[array[Operation]](#Operation) Array of operations

### `Resource` - [Up](#__Models)

An azure resource object

id (optional)

[String](#string) Azure resource Id

name (optional)

[String](#string) Azure resource name

type (optional)

[String](#string) Azure resource type

### `ResourceWithEtag` - [Up](#__Models)

An azure resource object with an Etag property

id (optional)

[String](#string) Azure resource Id

name (optional)

[String](#string) Azure resource name

type (optional)

[String](#string) Azure resource type

etag (optional)

[String](#string) Etag of the azure resource

### `ScheduledAlertRule` - [Up](#__Models)

Represents scheduled alert rule.

id (optional)

[String](#string) Azure resource Id

name (optional)

[String](#string) Azure resource name

type (optional)

[String](#string) Azure resource type

etag (optional)

[String](#string) Etag of the azure resource

kind

[String](#string) The kind of the alert rule

Enum:

Scheduled

MicrosoftSecurityIncidentCreation

Fusion

properties (optional)

[ScheduledAlertRuleProperties](#ScheduledAlertRuleProperties) Scheduled
alert rule properties

### `ScheduledAlertRuleCommonProperties` - [Up](#__Models)

Schedule alert rule template property bag.

query (optional)

[String](#string) The query that creates alerts for this rule.

queryFrequency (optional)

[String](#string) The frequency (in ISO 8601 duration format) for this
alert rule to run. format: duration

queryPeriod (optional)

[String](#string) The period (in ISO 8601 duration format) that this
alert rule looks at. format: duration

severity (optional)

[AlertSeverity](#AlertSeverity) The severity for alerts created by this
alert rule.

triggerOperator (optional)

[AlertRuleTriggerOperator](#AlertRuleTriggerOperator) The operation
against the threshold that triggers alert rule.

triggerThreshold (optional)

[Integer](#integer) The threshold triggers this alert rule.

### `ScheduledAlertRuleProperties` - [Up](#__Models)

Scheduled alert rule base property bag.

query (optional)

[String](#string) The query that creates alerts for this rule.

queryFrequency (optional)

[String](#string) The frequency (in ISO 8601 duration format) for this
alert rule to run. format: duration

queryPeriod (optional)

[String](#string) The period (in ISO 8601 duration format) that this
alert rule looks at. format: duration

severity (optional)

[AlertSeverity](#AlertSeverity) The severity for alerts created by this
alert rule.

triggerOperator (optional)

[AlertRuleTriggerOperator](#AlertRuleTriggerOperator) The operation
against the threshold that triggers alert rule.

triggerThreshold (optional)

[Integer](#integer) The threshold triggers this alert rule.

alertRuleTemplateName (optional)

[String](#string) The Name of the alert rule template used to create
this rule.

description (optional)

[String](#string) The description of the alert rule.

displayName (optional)

[String](#string) The display name for alerts created by this alert
rule.

enabled (optional)

[Boolean](#boolean) Determines whether this alert rule is enabled or
disabled.

lastModifiedUtc (optional)

[Date](#DateTime) The last time that this alert rule has been modified.
format: date-time

suppressionDuration (optional)

[String](#string) The suppression (in ISO 8601 duration format) to wait
since last time this alert rule been triggered. format: duration

suppressionEnabled (optional)

[Boolean](#boolean) Determines whether the suppression for this alert
rule is enabled or disabled.

tactics (optional)

[array[AttackTactic]](#AttackTactic) The tactics of the alert rule

### `ScheduledAlertRuleTemplate` - [Up](#__Models)

Represents scheduled alert rule template.

id (optional)

[String](#string) Azure resource Id

name (optional)

[String](#string) Azure resource name

type (optional)

[String](#string) Azure resource type

kind

[String](#string) The kind of the alert rule

Enum:

Scheduled

MicrosoftSecurityIncidentCreation

Fusion

properties (optional)

[Object](#object) Scheduled alert rule template properties

### `Settings` - [Up](#__Models)

The Setting.

id (optional)

[String](#string) Azure resource Id

name (optional)

[String](#string) Azure resource name

type (optional)

[String](#string) Azure resource type

etag (optional)

[String](#string) Etag of the azure resource

kind (optional)

[String](#string) The kind of the setting

Enum:

UebaSettings

ToggleSettings

### `SettingsKind` - [Up](#__Models)

Describes an Azure resource with kind.

kind (optional)

[String](#string) The kind of the setting

Enum:

UebaSettings

ToggleSettings

### `TIDataConnector` - [Up](#__Models)

Represents threat intelligence data connector.

id (optional)

[String](#string) Azure resource Id

name (optional)

[String](#string) Azure resource name

type (optional)

[String](#string) Azure resource type

etag (optional)

[String](#string) Etag of the azure resource

kind (optional)

[String](#string) The kind of the data connector

Enum:

AzureActiveDirectory

AzureSecurityCenter

MicrosoftCloudAppSecurity

ThreatIntelligence

Office365

AmazonWebServicesCloudTrail

AzureAdvancedThreatProtection

MicrosoftDefenderAdvancedThreatProtection

properties (optional)

[TIDataConnectorProperties](#TIDataConnectorProperties) TI (Threat
Intelligence) data connector properties.

### `TIDataConnectorDataTypes` - [Up](#__Models)

The available data types for TI (Threat Intelligence) data connector.

indicators (optional)

[Object](#object) Data type for indicators connection.

### `TIDataConnectorProperties` - [Up](#__Models)

TI (Threat Intelligence) data connector properties.

tenantId (optional)

[String](#string) The tenant id to connect to, and get the data from.

dataTypes (optional)

[TIDataConnectorDataTypes](#TIDataConnectorDataTypes) The available data
types for the connector.

### `ThreatIntelligence` - [Up](#__Models)

ThreatIntelligence property bag.

confidence (optional)

[Double](#double) Confidence (must be between 0 and 1) format: double

providerName (optional)

[String](#string) Name of the provider from whom this Threat
Intelligence information was received

reportLink (optional)

[String](#string) Report link

threatDescription (optional)

[String](#string) Threat description (free text)

threatName (optional)

[String](#string) Threat name (e.g. "Jedobot malware")

threatType (optional)

[String](#string) Threat type (e.g. "Botnet")

### `ToggleSettings` - [Up](#__Models)

Settings with single toggle.

id (optional)

[String](#string) Azure resource Id

name (optional)

[String](#string) Azure resource name

type (optional)

[String](#string) Azure resource type

etag (optional)

[String](#string) Etag of the azure resource

kind (optional)

[String](#string) The kind of the setting

Enum:

UebaSettings

ToggleSettings

properties (optional)

[ToggleSettingsProperties](#ToggleSettingsProperties) toggle properties

### `ToggleSettingsProperties` - [Up](#__Models)

toggle property bag.

isEnabled (optional)

[Boolean](#boolean) Determines whether the setting is enable or
disabled.

### `UebaSettings` - [Up](#__Models)

Represents settings for User and Entity Behavior Analytics enablement.

id (optional)

[String](#string) Azure resource Id

name (optional)

[String](#string) Azure resource name

type (optional)

[String](#string) Azure resource type

etag (optional)

[String](#string) Etag of the azure resource

kind (optional)

[String](#string) The kind of the setting

Enum:

UebaSettings

ToggleSettings

properties (optional)

[UebaSettingsProperties](#UebaSettingsProperties) User and Entity
Behavior Analytics settings properties

### `UebaSettingsProperties` - [Up](#__Models)

User and Entity Behavior Analytics settings property bag.

atpLicenseStatus (optional)

[String](#string) Determines whether the tenant has ATP (Advanced Threat
Protection) license.

Enum:

Enabled

Disabled

isEnabled (optional)

[Boolean](#boolean) Determines whether User and Entity Behavior
Analytics is enabled for this workspace.

statusInMcas (optional)

[String](#string) Determines whether User and Entity Behavior Analytics
is enabled from MCAS (Microsoft Cloud App Security).

Enum:

Enabled

Disabled

### `UserInfo` - [Up](#__Models)

User information that made some action

email (optional)

[String](#string) The email of the user.

name (optional)

[String](#string) The name of the user.

objectId

[UUID](#UUID) The object id of the user. format: uuid
