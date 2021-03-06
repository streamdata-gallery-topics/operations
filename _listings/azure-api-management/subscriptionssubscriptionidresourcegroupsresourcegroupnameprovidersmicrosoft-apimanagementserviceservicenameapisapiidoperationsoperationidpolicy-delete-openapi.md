---
swagger: "2.0"
x-collection-name: Azure API Management
x-complete: 0
info:
  title: Azure API Management API ApiOperationsPolicy Delete
  description: Deletes the policy configuration at the Api Operation.
  version: 1.0.0
host: management.azure.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ApiManagement/service/{serviceName}/apis/{apiId}/operations
  : get:
      summary: ApiOperations ListByApis
      description: Lists a collection of the operations for the specified API.
      operationId: ApiOperations_ListByApis
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-apimanagementserviceservicenameapisapiidoperations-get
      parameters:
      - in: query
        name: $filter
        description: '| Field       | Supported operators    | Supported functions               ||-------------|------------------------|-----------------------------------||
          name        | ge, le, eq, ne, gt, lt | substringof, startswith, endswith
          || method      | ge, le, eq, ne, gt, lt | substringof, startswith, endswith
          || description | ge, le, eq, ne, gt, lt | substringof, startswith, endswith
          || urlTemplate | ge, le, eq, ne, gt, lt | substringof, startswith, endswith
          |'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - API Operations
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ApiManagement/service/{serviceName}/apis/{apiId}/operations/{operationId}
  : get:
      summary: ApiOperations Get
      description: Gets the details of the API Operation specified by its identifier.
      operationId: ApiOperations_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-apimanagementserviceservicenameapisapiidoperationsoperationid-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - API Operations
    put:
      summary: ApiOperations CreateOrUpdate
      description: Creates a new API operation or updates an existing one.
      operationId: ApiOperations_CreateOrUpdate
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-apimanagementserviceservicenameapisapiidoperationsoperationid-put
      parameters:
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: Create parameters
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - API Operations
    patch:
      summary: ApiOperations Update
      description: Updates the details of the operation specified by its identifier.
      operationId: ApiOperations_Update
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-apimanagementserviceservicenameapisapiidoperationsoperationid-patch
      parameters:
      - in: header
        name: If-Match
        description: ETag of the API Operation Entity
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: API Operation Update parameters
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - API Operations
    delete:
      summary: ApiOperations Delete
      description: Deletes the specified operation.
      operationId: ApiOperations_Delete
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-apimanagementserviceservicenameapisapiidoperationsoperationid-delete
      parameters:
      - in: header
        name: If-Match
        description: ETag of the API Operation Entity
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - API Operations
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ApiManagement/service/{serviceName}/apis/{apiId}/operations/{operationId}/policy
  : get:
      summary: ApiOperationsPolicy Get
      description: Get the policy configuration at the API Operation level.
      operationId: ApiOperationsPolicy_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-apimanagementserviceservicenameapisapiidoperationsoperationidpolicy-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - API Operations
    put:
      summary: ApiOperationsPolicy CreateOrUpdate
      description: Creates or updates policy configuration for the API Operation level.
      operationId: ApiOperationsPolicy_CreateOrUpdate
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-apimanagementserviceservicenameapisapiidoperationsoperationidpolicy-put
      parameters:
      - in: header
        name: If-Match
        description: The entity state (Etag) version of the Api Operation policy to
          update
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: The policy contents to apply
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - API Operations
    delete:
      summary: ApiOperationsPolicy Delete
      description: Deletes the policy configuration at the Api Operation.
      operationId: ApiOperationsPolicy_Delete
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-apimanagementserviceservicenameapisapiidoperationsoperationidpolicy-delete
      parameters:
      - in: header
        name: If-Match
        description: The entity state (Etag) version of the Api operation policy to
          update
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - API Operations
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---