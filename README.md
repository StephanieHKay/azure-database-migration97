# Azure Database Migration Project

## Introduction
In this project, I implemented a cloud-based database system on Microsoft Azure, transitioning an on-premise database to the Azure SQL Database. K

- **Established a production environment:** Set up a SQL server database on an Azure VM.
- **Database Migration:** Migrated the database to Azure SQL Database, ensuring data backup and automated scheduling.
- **Backup:**Used SQL Server Management Studio to set a connection to Azure, schedule weekly backups, and store them in the cloud. 
- **Disaster recovery**: Simulated a disaster recovery scenario with data loss and data restoration from backups.
- **Geo-replication and Failover configuration:** Set up geo-replication and failover configuration and testing to ensure data availability.
- **Security Integration:** Used Microsoft Entra ID integration for defining access roles, adding an extra layer of control and protection to the database environment.

### Final Architecture:
A visual representation of the setup, migration, disaster recovery, geo-replication, failover, and security configurations.

<div align="center">
  <img src="architecture.PNG" alt="Architecture">
</div>

### Technologies Used:
- **Microsoft Azure**: Central platform for hosting and managing cloud-based database services.
- **Azure SQL Database**: Cloud-based relational database service for data storage and management.
- **Azure Data Studio**: A versatile tool for managing SQL Server, including Azure SQL Database and SQL Data Warehouse.
- **SQL Server Management Studio (SSMS)**: Integrated environment for SQL infrastructure management.
- **Microsoft Entra ID**: Identity and access management service for secure authentication.
- **Azure Blob Storage**:  Online storage service for data backup and recovery.
- **Windows Virtual Machine**: Used for creating production and development environments.

## Table of contents 
1. [Setting up the Production Environment](#Setting-up-the-Production-Environment)
2. [Database Migration to Azure SQL Database](#Database-Migration-to-Azure-SQL-Database)
2. [Dev Environment Setup and Data Loss Simulation] 
TODO(#dev-environment-setup-and-data-loss-simulation)
   - [Set Up a Dev Environment] 
   TODO(#set-up-a-dev-environment)
   - [Automated Backup of the Dev DB] 
   TODO(#automated-backup-of-the-dev-db)
   - [Data Loss Simulation in the Azure Prod Environment & Disaster Recovery] 
   TODO(#data-loss-simulation-in-the-azure-prod-environment--disaster-recovery)
3. [Geo-replication and Failover](#geo-replication-and-failover) TODO
4. [Microsoft Entra ID for Azure SQL DB](#microsoft-entra-id-for-azure-sql-db) TODO

## Setting up the Production Environment 

- Azure VM and Firewall Setup:
  - Created an Azure Virtual Machine (Windows 11).
  - Configured appropriate firewall rules for remote connections via the RDP protocol.
  - Established a remote connection using the RDP protocol and Microsoft Remote Desktop.
  
- Installed SQL Server and SSMS on the VM.

- Connected to SQL Server via SSMS.

- Used SSMS to restore a database from a .bak backup file, ensuring the production environment mirrors the on-premise server's functionality.



## Database Migration to Azure SQL Database

- Azure Server and Database Creation:
  - Created an Azure SQL Server.
  - Provisioned an SQL Database.




- Database Migration to Azure:
  - Downloaded Data Studio and the following extensions: **Azure SQL Migration** and **SQL Server schema compare** 
  - Utilized Data Studio to migrate the on-premises database to Azure (completed in roughly 7 minutes).
  - A full backup was generated using SSMS (tasks -> backup) and uploaded into a container that had been previously created within a storage account.