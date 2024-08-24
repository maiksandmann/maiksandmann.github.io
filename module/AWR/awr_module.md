---
permalink: /awr-module/
layout: module

---


![image](/picture/atroposs_logo.png){:height="150px" :width="150px"}



<br>

What happened about 15 years ago where UNIX derivates were migrated in direction to Linux, is happening today in terms of the traditional RDBMS's. A good overview about the currenty trends can be check on stackoverflow - [stackoverflow2024] or on DB-Engines [dbengines]. 

<br>

The developed AWR module should give user the possibility to parse mass of AWR's or Statspack level 7 in combination with the CSV output of available sql scritps and RVTool csv outputs to size oracle databases in direction to Oracle IaaS & PaaS environments or PaaS solutions like Postgresql on Azure. 
<br>
Please keep in mind that the generation of AWR reports in Oracle enterprise editions required a appropriate license for the database! Therefore, please be sure if you have a required licenses available.If that is not the case you can use statspack level 7 report! In total there are different levels of statspack reports available and we agreed in the groud to use the leve 7 with the output format <b>.lst</b>. Because the generated reports represent average data, it is important to upload into ATROPOSS reports during peak workloads to considering for the sizing the highest consumred resources of the underlying infrastructures of the databases. In case the peak workloads are unknown of the chosen databases the script <b>busiest_awr.sql</b> for AWR's or <b>busiest_statspack.sql</b> can be used and the displayed snap Id's be used for the report generation. 

<br>

<br>



Oracle databases are deployed on bare metal and virtualized environments like hyper-V or vmware (ESX) in customers or third party environments. The following module works for all bare metal deployed Oracle databases or ESX depoyed ones. In case of ESX deployed environment you can upload in addtion to the AWR & Statspack level 7, sql scripts (csv output) also the following 2 outputs CSV's of the RVTools Excel worksheet directly.
<br>
<ol>
<li>
RVTools_tabvHost.csv 
</li>
<li>
RVTools_tabvInfo.csv 
</li>
</ol>

How to download and install RVTools is described under [rvtool].
<br>
<br>

Please also review our existing <b>posts</b> in terms of news around the modules to keep the information here manageable. So, you can find for example 
<br>

<ul>
{% for post in site.categories.awr %}
    <li><a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>

<br>
<br>
<br>

The following documentation gives an overview about the parsed information from the CSV output format. The column name are a little bit different in the CSV and EXCEL output. If there are any additional information you are looking for, feel free to add them including the calcualtion and open a github issue. Thanks in advance.
<br>

<object data="../pdf/awr_module_documentation.pdf" width="1000" height="1000" type='application/pdf'></object>


   



[rvtool]: /module/AWR/rvtool/RVTools.html
[Just the docs repo]: https://github.com/atroposs-migration/atroposs-sample-module
[stackoverflow2024]: https://survey.stackoverflow.co/2024/technology#most-popular-technologies-database
[dbengines]: https://db-engines.com/en/ranking


