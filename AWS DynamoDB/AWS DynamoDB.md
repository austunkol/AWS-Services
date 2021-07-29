# `AWS DynamoDB`

## `Creating DynamoDB Tables`
- Go to `DynamoDB` service on AWS console

## `Create ProductCatalog Table`

- CLick `Create Table`
- Set the table name `ProductCatalog`
- Set primary key `Id` and select the type `Number`
- Leave `Use default settings` as under `Table Settings`
- Click `Create`

## `Create Forum Table`

- Click `Create Table`
- Set table name `Forum`
- Set primary key `Name` the type `String`
- Leave `Use default settings` checked under `Table Settings`
- Click `Create`

## ` Create Thread Table`

- Click `Create Table`
- Set table name `Thread`
- Set primary key `ForumName` the type `String`
- Put checkmark `Add sort key` and set `Subject` and select type `String`
- Leave ` Use default settings` checked under `Table Settings` as default
- Click `Create`

## `Create Reply Table`

- Click `Create Table`
- Set table name `Reply`
- Set primary key `Id` the type `String`
- Checkmark `Add sort key` set sort key `ReplyDateTime` select type of sort key `String`
- Uncheck `Use default settings` under `Table Settings`
- Click `+ Add index` under secondary indexes, pop up;
	- Set primary key `PostedBy` select the type `String`
	- Put checkmark on `Add sort key` set sort key `Message` select the sort key `String`
	- Leave the index name `PostedBy-Message-Index` is automatically created
	- Leave projected attributes `All`
	- Click `Add Index`
- Kepp rest of the all settings as default
- Click `Create`

## `Manipulating DynamoDB Database`

- There are two options to connect `DynamoDB`
	- CLI
	- EC2
- I will show with EC2 connections

- Connect to `EC2`
- Create a directory ` dynamodb`
	- mkdir dynamodb
- Download the `sampledata.zip`
           - wget https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/samples/sampledata.zip
- Unzip `sampledata.zip` file into the `dynamodb` folder
	- unzip sampledata.zip

## `Upload sample data into the DynamoDB tables`

- Populate the `ProductCatalog` table 
	- aws dynamodb batch-write-item --request-items file://ProductCatalog.json
- Populate the `Forum` table
	-  aws dynamodb batch-write-item --request-items file://Forum.json
- Populate the `Thread` table
	- aws dynamodb batch-write-item --request-items file://Thread.json
- Populate the `Reply` table
	- aws dynamodb batch-write-item --request-items file://Reply.json

## `Verify that data with AWS Management Console`

- Open the `DynamoDB` in console
- Select `ProductCatalog` from the list of tables
- Click `Items` to view the data

## `Running Queries on DynamoDB Tables`

- Open `DynamoDB` console

- Select `Reply` from the list of tables
- Click on the `Items` tab
- Click on the data filtering link, located just below the `Create item` button

## `Data Filtering`
- Change the operation from `Scan` to `Query`
- For the Partition key, enter `Amazon DynamoDB#DynamoDB Thread 1` as the value
- Click `Start Search`. (Only the items that match your query criteria are returned from the `Reply` table) 