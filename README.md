# EFCore3Sample
EF Core 3 sample for CRUD

## Schema Requirements:
### SQL Server:
  
```sql
CREATE TABLE [EFCore3Sample].[AppConfig](
[version] INT NOT NULL,    
[ConfigKey] VARCHAR(24) NOT NULL,  
[ConfigValue] VARCHAR(100),  
[Rmrk] VARCHAR(256),  
[IsActive] CHAR(1),  
[CreID] VARCHAR(25),  
[CreTime] DATETIME,  
[ModID] VARCHAR(25),  
[ModTime] DATETIME,  
CONSTRAINT [PK_AppConfig] PRIMARY KEY CLUSTERED([version]ASC,[ConfigKey]ASC));
```
  
### Oracle:
```sql
CREATE TABLE "EFCore3Sample"."AppConfig"(  
"version" NUMBER(10),  
"ConfigKey" VARCHAR2(24),  
"ConfigValue" VARCHAR2(100),  
"Rmrk" VARCHAR2(256),  
"IsActive" CHAR(1),  
"CreID" VARCHAR2(25),  
"CreTime" DATE,  
"ModID" VARCHAR2(25),  
"ModTime" DATE,  
CONSTRAINT PK_AppConfig PRIMARY KEY("version","ConfigKey"));
``` 
  
### PostgreSQL:
```sql
CREATE TABLE "EFCore3Sample"."AppConfig"  
(  
    "version" integer NOT NULL,  
    "ConfigKey" character varying(24) NOT NULL,  
    "ConfigValue" character varying(100) NOT NULL,  
    "Rmrk" character varying(256),  
    "IsActive" character varying(1),  
    "CreID" character varying(25),  
    "CreTime" timestamp without time zone,  
    "ModID" character varying(25),  
    "ModTime" timestamp without time zone,  
    CONSTRAINT appconfig_pkey PRIMARY KEY ("version", "ConfigKey")  
)
```
  
## Package Requirements:
### Core
Microsoft.NETCore.App  
System.Linq.Dynamic.Core 
### Common
Microsoft.EntityFrameworkCore  
Microsoft.EntityFrameworkCore.Tools
### SQL Server
Microsoft.EntityFrameworkCore.SqlServer
### Oracle
Oracle.EntityFrameworkCore
### PostgreSQL
Npgsql.EntityFrameworkCore.PostgreSQL
