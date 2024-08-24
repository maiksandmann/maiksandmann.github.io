---
layout: post
title:  "AWR Module overview of ATROPOSS!"
date:   2024-06-10 08:20:24 +0200
categories: awr
---



<br>
Figure 1: open the pop down list to read an abstract what kind of files can be uploaded at once to the parser
<br>
<img src="/module/AWR/awr/picture1_howitisworking.png" height="500px" width="500px" alt="Overview architecture">

<br>
<br>
Figure 2: The second pop down list shows what kind of scripts can be downloaded to enrich the discovery / sizing of the oracle databases. Furthermore can scripts <b>busiest_awr.sql</b> and <b>busiest_statspack.sql</b> be downloaded to identified the peak workload time periods, if these are not known.
The script <b>dbSizeCsv.sql</b> can be used for Oracle2Postgresql sizing and the <b>dbspace.sql</b> script for Oracle2Oracle IaaS or PaaS sizing.
<br>
<img src="/module/AWR/awr/picture1_howitisworking2-2.png" height="500px" width="500px" alt="Overview architecture">

<br>
<br>
Figure 3: The settings in the module give users the possibility to extend or reduce the parsing inside in AWR'S / statspacks, depending on the requirements. The radio check box <b>"top 20 SQL"</b> will give a minimal insight of used application modules if available, whereas the radio check box <b>"Complete SQL list"</b> will parse over the complete AWR's / statpacks to list all kind of packages and sql functions. 
<br>
<img src="/module/AWR/awr/picture1_howitisworking3-3.png" height="300px" width="500px" alt="Overview architecture">

<br>
<br>
Figure 4: The settings below <b>Cluster of DB workloads</b> is doing a lightweight consolidation of the database based on the chosen <b>"DB sku Template"</b> based on the snap time interval, the calculated consumed CPU and memory behavior during that time period. By uploading multipe reports of different time periods the workload profile over a longer time interval can be calculated as well. The <b>"DB sku Template"</b> represents a small number of available azure sku's and are limited in this version on D-, E- and M-series. The used D- and E-series are available on IaaS and Postgresql sizing engagements. The setting for the number for DB cluster represent the number of server on which the parsed Oracle databases should be consolidated. The numbering is starting with 0 and is adding +1 if the consolidated databases inside the time series are reaching the limit of the chosen sku resources (Threshold 80%). 
<br>
<img src="/module/AWR/awr/picture1_howitisworking4-4.png" height="300px" width="500px" alt="Overview architecture">

<br>
<br>
Figure 4a: The <b>Number of DB clusters</b> is an integer you can choose. The number of consoidated server will be calculated based on the required ressources of the chosen sku and not on the chosen number in the UI of the module. If the chosen number was 10 but the databses can be consolidated on 5, the number 5 will be considered! The consolication column in the output format of the parsed databases will be started with <b>cluster 0</b> (column <b>"cluster consolidation ID"</b>).
<br>
<img src="/module/AWR/awr/picture1_howitisworking41-41.png" height="300px" width="500px" alt="Overview architecture">

<br>
<br>
Figure 6: The output format can be chosen between <b> csv, excel or json</b> and depends on the tool of choice for the analysis. Currently we are in developing of a central reporting repository which should be available till end of this CY 2024. In addition we are storing the results in the session browser as well which makes it easy to re-use the output of existing modules as input for others. We will keep you posted, when the reporting module is available. 
<br>
<img src="/module/AWR/awr/picture1_howitisworking5-5.png" height="300px" width="500px" alt="Overview architecture">

<br>
<br>
Figure 7: After the <b>Upload</b> Buttion is presses all the different data of the sql scripts, the two RVTool csv's and multiple AWR'S and Statspack reports can be uploaed at once. Each parses database will be shown as one record in the output formats. 
<br>
<img src="/module/AWR/awr/picture1_howitisworking6-6.png" height="500px" width="500px" alt="Overview architecture">

<br>
<br>
Figure 8 Because the deployment is running in the browser of the users, the performance depends on his underlying hardware. Therfore the overall architecture is scaling with the number of users and doesn't depend on any backend. The progress bar takes a while till all information are uploaded in the WASM container of the browser and shows in percentage the overall number of parsed information. 
<br><img src="/module/AWR/awr/picture1_howitisworking7-7.png" height="400px" width="500px" alt="Overview architecture">

<br>
<br>
Figure 9: Next to the detailed output formats we have developed a lightweight web report as shown in the following snapshot. The reports has some limited interaction and will be integrated later into the overall reporting for all modules. The <b>"table summary"</b> highlights some limited information and over the available line <b>"Azure VM Comparison"</b> VM's can be chosen and compared based on prices and performance. Next to Azure VM there is a comparison to AWS and GCP available as well. The VM Comparison is as a standalone solution by our founders and partner available as well - see [cloudprice.net].
<br><img src="/module/AWR/awr/picture1_howitisworking8-8.png" height="500px" width="500px" alt="Overview architecture">

<br>
<br>
Figure 10: To allow the ATROPOSS the download of the output formats, the users need to give their permission!. The file are available in the download directory of the windows machine. 
<br>
<img src="/module/AWR/awr/picture1_howitisworking10-10.png" height="150px" width="300px" alt="Overview architecture">


[cloudprice.net]: https://cloudprice.net/