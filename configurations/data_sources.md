# Data Sources Configuration

## Overview
This section covers the setup of local data sources for ingestion into our SIEM solution.

### Local Logs Configuration

1. **Selecting Data Source**:
   - **Description**: Navigate to the data sources section in your SIEM tool.
   - **Screenshot**:
     ![Selecting Data Source](../screenshots/data_ingestion/Selecting_Data_Source.png)

2. **Selecting Source File**:
   - **Description**: Choose the log files for ingestion (e.g., `cisco_ironport_web.log`, `MOCK_DATA.csv`, `access.log`, `secure.log`).
   - **Screenshot**:
     ![Selecting Source File](../screenshots/data_ingestion/Selecting_Source_File.png)

3. **Setting Source Type**:
   - **Description**: Configure the source type and parsing rules for each log file.
   - **Screenshot**:
     ![Setting Source Type](../screenshots/data_ingestion/Setting_Source_Type.png)

### Verification
- Confirm that all local logs are successfully ingested and visible in the SIEM dashboard.

### Next Steps
- Implement automation with log forwarders for continuous ingestion from local files.
- Further refine data parsing and field extraction.

## Conclusion
This configuration helps ensure local logs are effectively ingested for monitoring and analysis. Further steps will improve data ingestion automation.
