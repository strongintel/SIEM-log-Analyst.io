# Data Sources Configuration

## Overview
This section covers the setup of local data sources for ingestion into our SIEM solution using Splunk.

### Local Logs Configuration

1. **Selecting Data Source**:
   - **Description**: Choose the data source you want to send to Splunk.
   - **Screenshot**:
     ![Choosing Data Source](../screenshots/data_ingestion/Selecting_Data_Source.png)

2. **Uploading Log Files**:
   - **Description**: Upload files from your computer. For example, select `cisco_ironport_web.log` for uploading.
   - **Screenshot**:
     ![Uploading Log Files](../screenshots/data_ingestion/Selecting_Source_File.png)

3. **Configuring Source Type**:
   - **Description**: Set the appropriate source type for the data. Here, `cisco:asa` is selected for the Cisco IronPort log.
   - **Screenshot**:
     ![Configuring Source Type](../screenshots/data_ingestion/Splunk_Set_Source_Type.png)

4. **Adding Data File**:
   - **Description**: Choose the file (e.g., `cisco_ironport_web.log`) for data upload.
   - **Screenshot**:
     ![Adding Data File](../screenshots/data_ingestion/Splunk_Select_File.png)

### Verification
- Confirm that all local logs are successfully ingested and visible in the Splunk dashboard. Check for correct data parsing and timestamps.

### Next Steps
- Implement automation with log forwarders for continuous ingestion from local files.
- Further refine data parsing and field extraction.

## Conclusion
This configuration helps ensure local logs are effectively ingested for monitoring and analysis. Further steps will improve data ingestion automation and enhance security monitoring.
