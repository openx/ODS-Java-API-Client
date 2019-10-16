
 Copyright (c) 2011, OpenX Technologies, Inc. All rights reserved.    
                                                                     
 Licensed under the New BSD License (the "License"); you may not use  
 this file except in compliance with the License. Unless required     
 by applicable law or agreed to in writing, software distributed      
 under the License is distributed on an "AS IS" BASIS, WITHOUT        
 WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.     
 See the License for the specific language governing permissions and  
 limitations under the License. See accompanying LICENSE file.        
 
 
 
 
For OpenX Reporting access using the Java API Client you will need:

### 1. Your credentials:
- consumer_key,
- consumer_secret,
- email address and password for your user of your OpenX instance.

To use Java API Client:

### 2. Install Java Development Kit (version 8-12)

### 3. Now, being in your workspace download the library into your working directory:

<code>$ git clone https://github.com/openx/ODS-Java-API-Client.git</code>

### 4. Open the project in your IDE (e.g. Eclipse)

### 5. Edit 'default.properties' file - OX3-Java-API-Client\src\main\resources\default.properties

- edit apiKey, apiSecret, username, password and domain
- myParams variable is used in the post request. Place your request body in that variable. You'll find some requests in here http://openxcorporate-ui3.openxenterprise.com/data/1.0/ods.html
- dateRange variable is used to check for available data for the specified report. You can simply copy/paste myParams without the StartDate and EndDate.
- myPost variable is used in the post request to our '/ox/4.0/' endpoint. Place your request body there, e.g. configuration of an ad unit.

### 6. Run java scripts
- 'ox_pull_fields.java' to receive all available fields (OX3-Java-API-Client\src\main\java\com\openx\oauthdemo\ox_pull_fields.java)
- 'ox_check_date_range.java' to check what is the available date range for selected report (earliest possible StartData, closest possible EndDate) (OX3-Java-API-Client\src\main\java\com\openx\oauthdemo\ox_check_date_range.java)
- 'ox_pull_report.java' to receive your report (OX3-Java-API-Client\src\main\java\com\openx\oauthdemo\ox_pull_report.java) 
- 'ox_post' to create a UI item, e.g. an adunit (OX3-Java-API-Client\src\main\java\com\openx\oauthdemo\ox_post.java)
