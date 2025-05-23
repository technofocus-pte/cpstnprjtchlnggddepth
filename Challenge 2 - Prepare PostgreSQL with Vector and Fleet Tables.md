# Challenge 2 - Prepare PostgreSQL with Vector and Fleet Tables

**Objective**  
Create and configure tables for fleet records, AI embeddings, and tips.

Steps :

1.  Allow public access from any Azure service within Azure to
    PostgreSQL server

2.  Add your IP address to PostgreSQL server

3.  Set **vector** and **azure-ai** extensions in **Server parameters**
    of **PostgreSQL server.**

4.  CREATE TABLE Contoso fleet table with blow code in Postgresql Server
    of **flexibleserverdb** daabase.

```
CREATE TABLE contosofleet (
RecordID  serial PRIMARY KEY,
VehicleID INTEGER,
     MeasurementTimestamp TIMESTAMP,
      FleetID   INTEGER,
    TruckID  INTEGER,
    Region INTEGER,
   Mileage INTEGER,
EngineHealth float,
SensorData float,
VehicleSpeedSensor  INTEGER,
Vibration DOUBLE PRECISION,    
EngineLoad float,
EngineCoolantTemp INTEGER,  
IntakeManifoldPressure INTEGER,
EngineRPM INTEGER,   
SpeedOBD INTEGER,
IntakeAirTemp INTEGER,     
MassAirFlowRate float,
ThrottlePosManifold float,
VoltageControlModule float,
AmbientAirTemp INTEGER,      
AccelPedalPosD float,
EngineOilTemp INTEGER,      
SpeedGPS INTEGER,
GPSLongitude float,
 GPSLatitude float,
GPSBearing float,
GPSAltitude INTEGER,      
TurboBoostAndVcmGauge float,
TripDistance float,
LitresPer100kmInst  float,
AccelSsorTotal float,
CO2InGPerKmInst float,
TripTimeJourney INTEGER,
MaintenanceFlag INTEGER
);
```
+++GRANT ALL ON TABLE contosofleet TO citus;+++

5.  Create **Fleet-Clearned_data** table to export cleaned data

```
CREATE TABLE fleet_cleaned_data (
RecordID  serial PRIMARY KEY,
VehicleID INTEGER,
Region INTEGER,
Mileage INTEGER,
EngineHealth float,
SensorData float,
VehicleSpeedSensor  INTEGER,
Vibration DOUBLE PRECISION,    
EngineLoad float,
EngineCoolantTemp INTEGER,  
IntakeManifoldPressure INTEGER,
EngineRPM INTEGER,   
SpeedOBD INTEGER,
IntakeAirTemp INTEGER,     
MassAirFlowRate float,
ThrottlePosManifold float,
VoltageControlModule float,
AmbientAirTemp INTEGER,      
AccelPedalPosD float,
EngineOilTemp INTEGER,      
SpeedGPS INTEGER,
GPSLongitude float,
 GPSLatitude float,
GPSBearing float,
GPSAltitude INTEGER,      
TurboBoostAndVcmGauge float,
TripDistance float,
LitresPer100kmInst  float,
AccelSsorTotal float,
CO2InGPerKmInst float,
TripTimeJourney INTEGER,
MaintenanceFlag INTEGER
);
```

+++GRANT ALL ON TABLE fleet_cleaned_data TO citus;+++

6.  **Create a** maintenance_documents **Table to Store Documents and
    Embeddings**

    ```
    CREATE TABLE maintenance_documents (
        id SERIAL PRIMARY KEY,
        filename TEXT NOT NULL,
        content TEXT NOT NULL,
        embeddings vector(1536)  -- Adjust dimensions based on the embedding model
    );
    ```

7.  grant table access to the user.provide all tables to the user citus

+++GRANT ALL ON TABLE maintenance_documents TO citus;+++

8.  Install **vecotor and azure_ai** extensions

+++CREATE EXTENSION azure_ai;+++

+++CREATE EXTENSION vector;+++

**Success Criteria:**

- Tables are visible in Azure Database for PostgreSQL

- Extensions azure_ai and vector should have been installed

- User should have provisioned permission to all tables in database
