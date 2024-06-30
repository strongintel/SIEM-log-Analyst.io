# Data Sources Configuration

## Overview
This section covers the setup of local data sources for ingestion into our SIEM solution using Splunk.

### Local Logs Configuration

1. **Choosing Data Source**:
   - **Description**: Select the type of data you want to send to Splunk. Here, you can choose from options like cloud computing, networking, operating systems, or security.
   - **Screenshot**:
     ![Choosing Data Source](../screenshots/data_ingestion/Selecting_Data_Source.png)

2. **Uploading Log Files**:
   - **Description**: Upload log files directly from your computer, such as `cisco_ironport_web.log`, `MOCK_DATA.csv`, `access.log`, and `secure.log`.
   - **Screenshot**:
     ![Uploading Log Files](../screenshots/data_ingestion/Select_Source_File.png)

3. **Setting Source Type**:
   - **Description**: Configure the source type and parsing rules for each log file. This example shows setting the source type for the Cisco IronPort log file.
   - **Screenshot**:
     ![Setting Source Type](../screenshots/data_ingestion/Setting_Source_Type.png)

4. **Detailed Process**:
   - **Select Source File**: Drag and drop your file (e.g., `cisco_ironport_web.log`) for upload.
     ![Select Source File](../screenshots/data_ingestion/Select_Source_File.png)

   - **Configure Source Type**: Adjust source type settings, using pre-defined templates like `cisco:asa` or custom settings.
     ![Configure Source Type](../screenshots/data_ingestion/Configure_Source_Type.png)

### Verification
- Confirm that all local logs are successfully ingested and visible in the Splunk dashboard. Check for correct data parsing and timestamps.

### Next Steps
- Implement automation with log forwarders for continuous ingestion from local files.
- Further refine data parsing and field extraction.

## Conclusion
This configuration helps ensure local logs are effectively ingested for monitoring and analysis. Further steps will improve data ingestion automation and enhance security monitoring.
