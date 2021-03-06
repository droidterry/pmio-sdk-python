# ProcessMaker_PMIO
This ProcessMaker I/O API provides access to a BPMN 2.0 compliant workflow engine api that is designed to be used as a microservice to support enterprise cloud applications.  The current Alpha 1.0 version supports most of the descriptive class of the BPMN 2.0 specification.

This Python package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1.0.0
- Package version: 1.0.0
- Build date: 2017-06-01T16:59:16.115+03:00
- Build package: class io.swagger.codegen.languages.PythonClientCodegen
For more information, please visit [https://www.processmaker.io/](https://www.processmaker.io/)

## Requirements.

Python 2.7 and 3.4+

## Installation & Usage
### pip install

If the python package is hosted on Github, you can install directly from Github

```sh
pip install git+https://github.com/ProcessMaker/pmio-sdk-python.git.git
```
(you may need to run `pip` with root permission: `sudo pip install git+https://github.com/ProcessMaker/pmio-sdk-python.git`)

Then import the package:
```python
import ProcessMaker_PMIO 
```

### Setuptools

Install via [Setuptools](http://pypi.python.org/pypi/setuptools).

```sh
python setup.py install --user
```
(or `sudo python setup.py install` to install the package for all users)

Then import the package:
```python
import ProcessMaker_PMIO
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```python
from __future__ import print_function
import time
import ProcessMaker_PMIO
from ProcessMaker_PMIO.rest import ApiException
from pprint import pprint

# Configure OAuth2 access token for authorization: PasswordGrant
ProcessMaker_PMIO.configuration.access_token = 'YOUR_ACCESS_TOKEN'
# create an instance of the API class
api_instance = ProcessMaker_PMIO.ProcessmakerApi
user_id = 'user_id_example' # str | ID of the user related to the Oauth client
client_create_item = ProcessMaker_PMIO.ClientCreateItem() # ClientCreateItem | JSON API with the Oauth Client object to add

try:
    api_response = api_instance.add_client(user_id, client_create_item)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ProcessmakerApi->add_client: %s\n" % e)

```

## Documentation for API Endpoints

All URIs are relative to *https://CHANGEME.api.processmaker.io/api/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*ProcessmakerApi* | [**add_client**](docs/ProcessmakerApi.md#add_client) | **POST** /users/{user_id}/clients | 
*ProcessmakerApi* | [**add_event**](docs/ProcessmakerApi.md#add_event) | **POST** /processes/{process_id}/events | 
*ProcessmakerApi* | [**add_event_connector**](docs/ProcessmakerApi.md#add_event_connector) | **POST** /processes/{process_id}/events/{event_id}/connectors | 
*ProcessmakerApi* | [**add_flow**](docs/ProcessmakerApi.md#add_flow) | **POST** /processes/{process_id}/flows | 
*ProcessmakerApi* | [**add_gateway**](docs/ProcessmakerApi.md#add_gateway) | **POST** /processes/{process_id}/gateways | 
*ProcessmakerApi* | [**add_group**](docs/ProcessmakerApi.md#add_group) | **POST** /groups | 
*ProcessmakerApi* | [**add_groups_to_task**](docs/ProcessmakerApi.md#add_groups_to_task) | **PUT** /processes/{process_id}/tasks/{task_id}/groups | 
*ProcessmakerApi* | [**add_input_output**](docs/ProcessmakerApi.md#add_input_output) | **POST** /processes/{process_id}/tasks/{task_id}/inputoutput | 
*ProcessmakerApi* | [**add_instance**](docs/ProcessmakerApi.md#add_instance) | **POST** /processes/{process_id}/instances | 
*ProcessmakerApi* | [**add_process**](docs/ProcessmakerApi.md#add_process) | **POST** /processes | 
*ProcessmakerApi* | [**add_task**](docs/ProcessmakerApi.md#add_task) | **POST** /processes/{process_id}/tasks | 
*ProcessmakerApi* | [**add_task_connector**](docs/ProcessmakerApi.md#add_task_connector) | **POST** /processes/{process_id}/tasks/{task_id}/connectors | 
*ProcessmakerApi* | [**add_user**](docs/ProcessmakerApi.md#add_user) | **POST** /users | 
*ProcessmakerApi* | [**add_users_to_group**](docs/ProcessmakerApi.md#add_users_to_group) | **PUT** /groups/{id}/users | 
*ProcessmakerApi* | [**delete_client**](docs/ProcessmakerApi.md#delete_client) | **DELETE** /users/{user_id}/clients/{client_id} | 
*ProcessmakerApi* | [**delete_event**](docs/ProcessmakerApi.md#delete_event) | **DELETE** /processes/{process_id}/events/{event_id} | 
*ProcessmakerApi* | [**delete_event_connector**](docs/ProcessmakerApi.md#delete_event_connector) | **DELETE** /processes/{process_id}/events/{event_id}/connectors/{connector_id} | 
*ProcessmakerApi* | [**delete_flow**](docs/ProcessmakerApi.md#delete_flow) | **DELETE** /processes/{process_id}/flows/{flow_id} | 
*ProcessmakerApi* | [**delete_gateway**](docs/ProcessmakerApi.md#delete_gateway) | **DELETE** /processes/{process_id}/gateways/{gateway_id} | 
*ProcessmakerApi* | [**delete_group**](docs/ProcessmakerApi.md#delete_group) | **DELETE** /groups/{id} | 
*ProcessmakerApi* | [**delete_input_output**](docs/ProcessmakerApi.md#delete_input_output) | **DELETE** /processes/{process_id}/tasks/{task_id}/inputoutput/{inputoutput_uid} | 
*ProcessmakerApi* | [**delete_instance**](docs/ProcessmakerApi.md#delete_instance) | **DELETE** /processes/{process_id}/instances/{instance_id} | 
*ProcessmakerApi* | [**delete_process**](docs/ProcessmakerApi.md#delete_process) | **DELETE** /processes/{id} | 
*ProcessmakerApi* | [**delete_task**](docs/ProcessmakerApi.md#delete_task) | **DELETE** /processes/{process_id}/tasks/{task_id} | 
*ProcessmakerApi* | [**delete_task_connector**](docs/ProcessmakerApi.md#delete_task_connector) | **DELETE** /processes/{process_id}/tasks/{task_id}/connectors/{connector_id} | 
*ProcessmakerApi* | [**delete_user**](docs/ProcessmakerApi.md#delete_user) | **DELETE** /users/{id} | 
*ProcessmakerApi* | [**event_trigger**](docs/ProcessmakerApi.md#event_trigger) | **POST** /processes/{process_id}/events/{event_id}/trigger | 
*ProcessmakerApi* | [**find_client_by_id**](docs/ProcessmakerApi.md#find_client_by_id) | **GET** /users/{user_id}/clients/{client_id} | 
*ProcessmakerApi* | [**find_clients**](docs/ProcessmakerApi.md#find_clients) | **GET** /users/{user_id}/clients | 
*ProcessmakerApi* | [**find_data_model**](docs/ProcessmakerApi.md#find_data_model) | **GET** /processes/{process_id}/instances/{instance_id}/datamodel | 
*ProcessmakerApi* | [**find_event_by_id**](docs/ProcessmakerApi.md#find_event_by_id) | **GET** /processes/{process_id}/events/{event_id} | 
*ProcessmakerApi* | [**find_event_connector_by_id**](docs/ProcessmakerApi.md#find_event_connector_by_id) | **GET** /processes/{process_id}/events/{event_id}/connectors/{connector_id} | 
*ProcessmakerApi* | [**find_event_connectors**](docs/ProcessmakerApi.md#find_event_connectors) | **GET** /processes/{process_id}/events/{event_id}/connectors | 
*ProcessmakerApi* | [**find_events**](docs/ProcessmakerApi.md#find_events) | **GET** /processes/{process_id}/events | 
*ProcessmakerApi* | [**find_flow_by_id**](docs/ProcessmakerApi.md#find_flow_by_id) | **GET** /processes/{process_id}/flows/{flow_id} | 
*ProcessmakerApi* | [**find_flows**](docs/ProcessmakerApi.md#find_flows) | **GET** /processes/{process_id}/flows | 
*ProcessmakerApi* | [**find_gateway_by_id**](docs/ProcessmakerApi.md#find_gateway_by_id) | **GET** /processes/{process_id}/gateways/{gateway_id} | 
*ProcessmakerApi* | [**find_gateways**](docs/ProcessmakerApi.md#find_gateways) | **GET** /processes/{process_id}/gateways | 
*ProcessmakerApi* | [**find_group_by_id**](docs/ProcessmakerApi.md#find_group_by_id) | **GET** /groups/{id} | 
*ProcessmakerApi* | [**find_groups**](docs/ProcessmakerApi.md#find_groups) | **GET** /groups | 
*ProcessmakerApi* | [**find_input_output_by_id**](docs/ProcessmakerApi.md#find_input_output_by_id) | **GET** /processes/{process_id}/tasks/{task_id}/inputoutput/{inputoutput_uid} | 
*ProcessmakerApi* | [**find_input_outputs**](docs/ProcessmakerApi.md#find_input_outputs) | **GET** /processes/{process_id}/tasks/{task_id}/inputoutput | 
*ProcessmakerApi* | [**find_instance_by_id**](docs/ProcessmakerApi.md#find_instance_by_id) | **GET** /processes/{process_id}/instances/{instance_id} | 
*ProcessmakerApi* | [**find_instances**](docs/ProcessmakerApi.md#find_instances) | **GET** /processes/{process_id}/instances | 
*ProcessmakerApi* | [**find_process_by_id**](docs/ProcessmakerApi.md#find_process_by_id) | **GET** /processes/{id} | 
*ProcessmakerApi* | [**find_processes**](docs/ProcessmakerApi.md#find_processes) | **GET** /processes | 
*ProcessmakerApi* | [**find_task_by_id**](docs/ProcessmakerApi.md#find_task_by_id) | **GET** /processes/{process_id}/tasks/{task_id} | 
*ProcessmakerApi* | [**find_task_connector_by_id**](docs/ProcessmakerApi.md#find_task_connector_by_id) | **GET** /processes/{process_id}/tasks/{task_id}/connectors/{connector_id} | 
*ProcessmakerApi* | [**find_task_connectors**](docs/ProcessmakerApi.md#find_task_connectors) | **GET** /processes/{process_id}/tasks/{task_id}/connectors | 
*ProcessmakerApi* | [**find_task_instance_by_id**](docs/ProcessmakerApi.md#find_task_instance_by_id) | **GET** /task_instances/{task_instance_id} | 
*ProcessmakerApi* | [**find_task_instances**](docs/ProcessmakerApi.md#find_task_instances) | **GET** /task_instances | 
*ProcessmakerApi* | [**find_tasks**](docs/ProcessmakerApi.md#find_tasks) | **GET** /processes/{process_id}/tasks | 
*ProcessmakerApi* | [**find_user_by_id**](docs/ProcessmakerApi.md#find_user_by_id) | **GET** /users/{id} | 
*ProcessmakerApi* | [**find_users**](docs/ProcessmakerApi.md#find_users) | **GET** /users | 
*ProcessmakerApi* | [**import_bpmn_file**](docs/ProcessmakerApi.md#import_bpmn_file) | **POST** /processes/import | 
*ProcessmakerApi* | [**myself_user**](docs/ProcessmakerApi.md#myself_user) | **GET** /users/myself | 
*ProcessmakerApi* | [**remove_groups_from_task**](docs/ProcessmakerApi.md#remove_groups_from_task) | **DELETE** /processes/{process_id}/tasks/{task_id}/groups | 
*ProcessmakerApi* | [**remove_users_from_group**](docs/ProcessmakerApi.md#remove_users_from_group) | **DELETE** /groups/{id}/users | 
*ProcessmakerApi* | [**sync_groups_to_task**](docs/ProcessmakerApi.md#sync_groups_to_task) | **POST** /processes/{process_id}/tasks/{task_id}/groups | 
*ProcessmakerApi* | [**sync_users_to_group**](docs/ProcessmakerApi.md#sync_users_to_group) | **POST** /groups/{id}/users | 
*ProcessmakerApi* | [**update_client**](docs/ProcessmakerApi.md#update_client) | **PUT** /users/{user_id}/clients/{client_id} | 
*ProcessmakerApi* | [**update_event**](docs/ProcessmakerApi.md#update_event) | **PUT** /processes/{process_id}/events/{event_id} | 
*ProcessmakerApi* | [**update_event_connector**](docs/ProcessmakerApi.md#update_event_connector) | **PUT** /processes/{process_id}/events/{event_id}/connectors/{connector_id} | 
*ProcessmakerApi* | [**update_flow**](docs/ProcessmakerApi.md#update_flow) | **PUT** /processes/{process_id}/flows/{flow_id} | 
*ProcessmakerApi* | [**update_gateway**](docs/ProcessmakerApi.md#update_gateway) | **PUT** /processes/{process_id}/gateways/{gateway_id} | 
*ProcessmakerApi* | [**update_group**](docs/ProcessmakerApi.md#update_group) | **PUT** /groups/{id} | 
*ProcessmakerApi* | [**update_input_output**](docs/ProcessmakerApi.md#update_input_output) | **PUT** /processes/{process_id}/tasks/{task_id}/inputoutput/{inputoutput_uid} | 
*ProcessmakerApi* | [**update_instance**](docs/ProcessmakerApi.md#update_instance) | **PUT** /processes/{process_id}/instances/{instance_id} | 
*ProcessmakerApi* | [**update_process**](docs/ProcessmakerApi.md#update_process) | **PUT** /processes/{id} | 
*ProcessmakerApi* | [**update_task**](docs/ProcessmakerApi.md#update_task) | **PUT** /processes/{process_id}/tasks/{task_id} | 
*ProcessmakerApi* | [**update_task_connector**](docs/ProcessmakerApi.md#update_task_connector) | **PUT** /processes/{process_id}/tasks/{task_id}/connectors/{connector_id} | 
*ProcessmakerApi* | [**update_task_instance**](docs/ProcessmakerApi.md#update_task_instance) | **PATCH** /task_instances/{task_instance_id} | 
*ProcessmakerApi* | [**update_user**](docs/ProcessmakerApi.md#update_user) | **PUT** /users/{id} | 


## Documentation For Models

 - [BpmnFile](docs/BpmnFile.md)
 - [BpmnFileAttributes](docs/BpmnFileAttributes.md)
 - [BpmnImportItem](docs/BpmnImportItem.md)
 - [Client](docs/Client.md)
 - [ClientAttributes](docs/ClientAttributes.md)
 - [ClientCollection](docs/ClientCollection.md)
 - [ClientCreateItem](docs/ClientCreateItem.md)
 - [ClientItem](docs/ClientItem.md)
 - [ClientUpdateItem](docs/ClientUpdateItem.md)
 - [DataModel](docs/DataModel.md)
 - [DataModelAttributes](docs/DataModelAttributes.md)
 - [DataModelItem](docs/DataModelItem.md)
 - [DataModelItem1](docs/DataModelItem1.md)
 - [DataModelItemAttributes](docs/DataModelItemAttributes.md)
 - [Error](docs/Error.md)
 - [ErrorArray](docs/ErrorArray.md)
 - [Event](docs/Event.md)
 - [EventAttributes](docs/EventAttributes.md)
 - [EventCollection](docs/EventCollection.md)
 - [EventConnector](docs/EventConnector.md)
 - [EventConnector1](docs/EventConnector1.md)
 - [EventConnectorAttributes](docs/EventConnectorAttributes.md)
 - [EventConnectorCreateItem](docs/EventConnectorCreateItem.md)
 - [EventConnectorUpdateItem](docs/EventConnectorUpdateItem.md)
 - [EventConnectorsCollection](docs/EventConnectorsCollection.md)
 - [EventCreateItem](docs/EventCreateItem.md)
 - [EventItem](docs/EventItem.md)
 - [EventUpdateItem](docs/EventUpdateItem.md)
 - [Flow](docs/Flow.md)
 - [FlowAttributes](docs/FlowAttributes.md)
 - [FlowCollection](docs/FlowCollection.md)
 - [FlowCreateItem](docs/FlowCreateItem.md)
 - [FlowItem](docs/FlowItem.md)
 - [FlowUpdateItem](docs/FlowUpdateItem.md)
 - [Gateway](docs/Gateway.md)
 - [GatewayAttributes](docs/GatewayAttributes.md)
 - [GatewayCollection](docs/GatewayCollection.md)
 - [GatewayCreateItem](docs/GatewayCreateItem.md)
 - [GatewayItem](docs/GatewayItem.md)
 - [GatewayUpdateItem](docs/GatewayUpdateItem.md)
 - [Group](docs/Group.md)
 - [GroupAddUsersItem](docs/GroupAddUsersItem.md)
 - [GroupAttributes](docs/GroupAttributes.md)
 - [GroupCollection](docs/GroupCollection.md)
 - [GroupCreateItem](docs/GroupCreateItem.md)
 - [GroupIds](docs/GroupIds.md)
 - [GroupItem](docs/GroupItem.md)
 - [GroupRemoveUsersItem](docs/GroupRemoveUsersItem.md)
 - [GroupSyncUsersItem](docs/GroupSyncUsersItem.md)
 - [GroupUpdateItem](docs/GroupUpdateItem.md)
 - [InlineResponse200](docs/InlineResponse200.md)
 - [InputOutput](docs/InputOutput.md)
 - [InputOutputAttributes](docs/InputOutputAttributes.md)
 - [InputOutputCollection](docs/InputOutputCollection.md)
 - [InputOutputCreateItem](docs/InputOutputCreateItem.md)
 - [InputOutputItem](docs/InputOutputItem.md)
 - [InputOutputUpdateItem](docs/InputOutputUpdateItem.md)
 - [Instance](docs/Instance.md)
 - [InstanceAttributes](docs/InstanceAttributes.md)
 - [InstanceCollection](docs/InstanceCollection.md)
 - [InstanceCreateItem](docs/InstanceCreateItem.md)
 - [InstanceItem](docs/InstanceItem.md)
 - [InstanceUpdateItem](docs/InstanceUpdateItem.md)
 - [Meta](docs/Meta.md)
 - [MetaLog](docs/MetaLog.md)
 - [Pagination](docs/Pagination.md)
 - [PaginationLinks](docs/PaginationLinks.md)
 - [Process](docs/Process.md)
 - [ProcessAttributes](docs/ProcessAttributes.md)
 - [ProcessCollection](docs/ProcessCollection.md)
 - [ProcessCollection1](docs/ProcessCollection1.md)
 - [ProcessCreateItem](docs/ProcessCreateItem.md)
 - [ProcessItem](docs/ProcessItem.md)
 - [ProcessUpdateItem](docs/ProcessUpdateItem.md)
 - [ResultSuccess](docs/ResultSuccess.md)
 - [ResultSuccessMeta](docs/ResultSuccessMeta.md)
 - [Task](docs/Task.md)
 - [TaskAddGroupsItem](docs/TaskAddGroupsItem.md)
 - [TaskAttributes](docs/TaskAttributes.md)
 - [TaskCollection](docs/TaskCollection.md)
 - [TaskConnector](docs/TaskConnector.md)
 - [TaskConnector1](docs/TaskConnector1.md)
 - [TaskConnectorAttributes](docs/TaskConnectorAttributes.md)
 - [TaskConnectorCreateItem](docs/TaskConnectorCreateItem.md)
 - [TaskConnectorUpdateItem](docs/TaskConnectorUpdateItem.md)
 - [TaskConnectorsCollection](docs/TaskConnectorsCollection.md)
 - [TaskCreateItem](docs/TaskCreateItem.md)
 - [TaskInstance](docs/TaskInstance.md)
 - [TaskInstanceAttributes](docs/TaskInstanceAttributes.md)
 - [TaskInstanceCollection](docs/TaskInstanceCollection.md)
 - [TaskInstanceUpdateItem](docs/TaskInstanceUpdateItem.md)
 - [TaskItem](docs/TaskItem.md)
 - [TaskRemoveGroupsItem](docs/TaskRemoveGroupsItem.md)
 - [TaskSyncGroupsItem](docs/TaskSyncGroupsItem.md)
 - [TaskUpdateItem](docs/TaskUpdateItem.md)
 - [TriggerEventCreateItem](docs/TriggerEventCreateItem.md)
 - [User](docs/User.md)
 - [UserAttributes](docs/UserAttributes.md)
 - [UserCollection](docs/UserCollection.md)
 - [UserCreateItem](docs/UserCreateItem.md)
 - [UserIds](docs/UserIds.md)
 - [UserItem](docs/UserItem.md)
 - [UserUpdateItem](docs/UserUpdateItem.md)


## Documentation For Authorization


## PasswordGrant

- **Type**: OAuth
- **Flow**: password
- **Authorization URL**: /oauth/access_token
- **Scopes**: N/A


## Author

support@processmaker.io

