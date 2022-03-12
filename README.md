# swagger_client

SwaggerClient - the Ruby gem for the Swagger Petstore

This is a sample server Petstore server.  You can find out more about Swagger at [http://swagger.io](http://swagger.io) or on [irc.freenode.net, #swagger](http://swagger.io/irc/).  For this sample, you can use the api key `special-key` to test the authorization filters.

This SDK is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1.0.6
- Package version: 1.0.0
- Build date: 2022-03-12T19:27:27.808Z
- Build package: class io.swagger.codegen.languages.RubyClientCodegen

## Installation

### Build a gem

To build the Ruby code into a gem:

```shell
gem build swagger_client.gemspec
```

Then either install the gem locally:

```shell
gem install ./swagger_client-1.0.0.gem
```
(for development, run `gem install --dev ./swagger_client-1.0.0.gem` to install the development dependencies)

or publish the gem to a gem hosting service, e.g. [RubyGems](https://rubygems.org/).

Finally add this to the Gemfile:

    gem 'swagger_client', '~> 1.0.0'

### Install from Git

If the Ruby gem is hosted at a git repository: https://github.com/GIT_USER_ID/GIT_REPO_ID, then add the following in the Gemfile:

    gem 'swagger_client', :git => 'https://github.com/GIT_USER_ID/GIT_REPO_ID.git'

### Include the Ruby code directly

Include the Ruby code directly using `-I` as follows:

```shell
ruby -Ilib script.rb
```

## Getting Started

Please follow the [installation](#installation) procedure and then run the following code:
```ruby
# Load the gem
require 'swagger_client'

# Setup authorization
SwaggerClient.configure do |config|
  # Configure OAuth2 access token for authorization: petstore_auth
  config.access_token = 'YOUR ACCESS TOKEN'
end

api_instance = SwaggerClient::PetApi.new

body = SwaggerClient::Pet.new # Pet | Pet object that needs to be added to the store


begin
  #Add a new pet to the store
  api_instance.add_pet(body)
rescue SwaggerClient::ApiError => e
  puts "Exception when calling PetApi->add_pet: #{e}"
end

```

## Documentation for API Endpoints

All URIs are relative to *https://petstore.swagger.io/v2*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*SwaggerClient::PetApi* | [**add_pet**](docs/PetApi.md#add_pet) | **POST** /pet | Add a new pet to the store
*SwaggerClient::PetApi* | [**delete_pet**](docs/PetApi.md#delete_pet) | **DELETE** /pet/{petId} | Deletes a pet
*SwaggerClient::PetApi* | [**find_pets_by_status**](docs/PetApi.md#find_pets_by_status) | **GET** /pet/findByStatus | Finds Pets by status
*SwaggerClient::PetApi* | [**find_pets_by_tags**](docs/PetApi.md#find_pets_by_tags) | **GET** /pet/findByTags | Finds Pets by tags
*SwaggerClient::PetApi* | [**get_pet_by_id**](docs/PetApi.md#get_pet_by_id) | **GET** /pet/{petId} | Find pet by ID
*SwaggerClient::PetApi* | [**update_pet**](docs/PetApi.md#update_pet) | **PUT** /pet | Update an existing pet
*SwaggerClient::PetApi* | [**update_pet_with_form**](docs/PetApi.md#update_pet_with_form) | **POST** /pet/{petId} | Updates a pet in the store with form data
*SwaggerClient::PetApi* | [**upload_file**](docs/PetApi.md#upload_file) | **POST** /pet/{petId}/uploadImage | uploads an image
*SwaggerClient::StoreApi* | [**delete_order**](docs/StoreApi.md#delete_order) | **DELETE** /store/order/{orderId} | Delete purchase order by ID
*SwaggerClient::StoreApi* | [**get_inventory**](docs/StoreApi.md#get_inventory) | **GET** /store/inventory | Returns pet inventories by status
*SwaggerClient::StoreApi* | [**get_order_by_id**](docs/StoreApi.md#get_order_by_id) | **GET** /store/order/{orderId} | Find purchase order by ID
*SwaggerClient::StoreApi* | [**place_order**](docs/StoreApi.md#place_order) | **POST** /store/order | Place an order for a pet
*SwaggerClient::UserApi* | [**create_user**](docs/UserApi.md#create_user) | **POST** /user | Create user
*SwaggerClient::UserApi* | [**create_users_with_array_input**](docs/UserApi.md#create_users_with_array_input) | **POST** /user/createWithArray | Creates list of users with given input array
*SwaggerClient::UserApi* | [**create_users_with_list_input**](docs/UserApi.md#create_users_with_list_input) | **POST** /user/createWithList | Creates list of users with given input array
*SwaggerClient::UserApi* | [**delete_user**](docs/UserApi.md#delete_user) | **DELETE** /user/{username} | Delete user
*SwaggerClient::UserApi* | [**get_user_by_name**](docs/UserApi.md#get_user_by_name) | **GET** /user/{username} | Get user by user name
*SwaggerClient::UserApi* | [**login_user**](docs/UserApi.md#login_user) | **GET** /user/login | Logs user into the system
*SwaggerClient::UserApi* | [**logout_user**](docs/UserApi.md#logout_user) | **GET** /user/logout | Logs out current logged in user session
*SwaggerClient::UserApi* | [**update_user**](docs/UserApi.md#update_user) | **PUT** /user/{username} | Updated user


## Documentation for Models

 - [SwaggerClient::ApiResponse](docs/ApiResponse.md)
 - [SwaggerClient::Category](docs/Category.md)
 - [SwaggerClient::Order](docs/Order.md)
 - [SwaggerClient::Pet](docs/Pet.md)
 - [SwaggerClient::Tag](docs/Tag.md)
 - [SwaggerClient::User](docs/User.md)


## Documentation for Authorization


### petstore_auth

- **Type**: OAuth
- **Flow**: implicit
- **Authorization URL**: https://petstore.swagger.io/oauth/authorize
- **Scopes**: 
  - read:pets: read your pets
  - write:pets: modify pets in your account

### api_key

- **Type**: API key
- **API key parameter name**: api_key
- **Location**: HTTP header

