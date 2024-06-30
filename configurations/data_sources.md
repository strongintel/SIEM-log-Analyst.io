# Data Sources Configuration

## Overview
This section covers the setup of local data sources for ingestion into our SIEM solution using Splunk.

### Local Logs Configuration

1. **Choosing Data Source**:
   - **Description**: Select the type of data you want to send to Splunk. Options include cloud computing, networking, operating systems, or security.
   - **Screenshot**:
     ![Choosing Data Source](../screenshots/data_ingestion/Selecting_Data_Source.png)

2. **Uploading Log Files**:
   - **Description**: Upload log files directly from your computer, such as `cisco_ironport_web.log`, `MOCK_DATA.csv`, `access.log`, and `secure.log`.
   - **Screenshot**:
     ![Uploading Log Files](../screenshots/data_ingestion/Selecting_Source_File.png)

3. **Setting Source Type**:
   - **Description**: Configure the source type and parsing rules for each log file. This example shows setting the source type for the Cisco IronPort log file.
   - **Screenshot**:
     ![Setting Source Type](../screenshots/data_ingestion/Setting_Source_Type.png)

4. **Detailed Process**:
   - **Select Source File**: Drag and drop your file (e.g., `cisco_ironport_web.log`) for upload.
     ![Select Source File](../screenshots/data_ingestion/Select_Source_File.png)

   - **Configure Source Type**: Adjust source type settings, using pre-defined templates like `cisco:asa` or custom settings.
     ![Configure Source Type](../screenshots/data_ingestion/Configure_Source_Type.png)

### Splunk Universal Forwarder Configuration

1. **Download and Install**:
   - **Description**: Download and install the Splunk Universal Forwarder on your host PC.
   - **Screenshot**:
     ![Download and Install](../screenshots/data_ingestion/Download_and_install_forwarder.png)
   - Install command:
     ```bash
     sudo installer -pkg <path-to-installer> -target /
     ```

2. **Configure the Forwarder**:
   - **Enable boot start and start the forwarder**:
     ```bash
     cd /Applications/SplunkForwarder/bin
     sudo ./splunk enable boot-start
     sudo ./splunk start
     ```
   - **Add the Splunk server as a receiver**:
     - Step 1:
       ![Add Splunk Server Step 1](../screenshots/data_ingestion/add_splunk_server_step1.png)
     - Step 2:
       ![Add Splunk Server Step 2](../screenshots/data_ingestion/add_splunk_server_step2.png)
     - Step 3:
       ![Add Splunk Server Step 3](../screenshots/data_ingestion/add_splunk_server_step3.png)
     ```bash
     sudo ./splunk add forward-server <your forwarder-ip>:9997
     ```

3. **Configure Inputs**:
   - **Edit the `inputs.conf` file to specify logs to forward**:
     ```bash
     cd /Applications/SplunkForwarder/etc/system/local
     sudo nano inputs.conf
     ```
   - Example entries:
     ```ini
     [monitor:///var/log/system.log]
     disabled = false

     [monitor:///var/log/secure.log]
     disabled = false
     ```

4. **Verify Forwarder Status**:
   - **Check the forwarder status**:
     ![Verify Forward Status](../screenshots/data_ingestion/Verify_forward_status.png)
     ```bash
     sudo ./splunk list forward-server
     ```

5. **Verify Data Ingestion**:
   - **Confirm logs from the host PC are visible in the Splunk dashboard**:
     ![Verify Data Ingestion](../screenshots/data_ingestion/Verify_data_ingestion1.5.png)

### Verification
- Confirm that all local logs and forwarded data are successfully ingested and visible in the Splunk dashboard. Check for correct data parsing and timestamps.

### Next Steps
- Continue to monitor the ingestion of logs and adjust configurations as necessary.
- Further refine data parsing and field extraction.

## Conclusion
This configuration ensures that local logs and data from the Splunk Universal Forwarder are effectively ingested for monitoring and analysis. Further steps will enhance data ingestion automation and improve security monitoring.
