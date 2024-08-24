---
layout: post
title:  "Impacts of Exadata Smart Scan & Hybrid Columnar Compression on Oracle database workloads"
date:   2024-06-20 08:30:40 +0200
categories: awr
---

Oracle databases can be deployed on different environments. Especially the deployment of databases on Oracle Engineered Systems - especially Exadata's should be considered in this Blog. On Exadata you have multiple feature which might have a significant impact on the workload behavior of the database. Here we like to pick two of the feature so called <b>Smart Scan</b> and <b>Hybrid Columnar Compression</b>.
<br>
Both of the feature are not available inside the common AWR report. To get a general impact we are calculating the data volume across the interconnect, which is of course more than the smart scan volume, but will give us how much impact the smart scan has on the workload characterisitics of the database.
<br>
<br>
Following snapshot and description gives an overview how to interpret the values. If you have an idea how to get more detailed information about smart scans, please let us know. 
<br>
<br>
<img src="/module/AWR/awr/smart_scan_impact_awr.png" height="150px" width="400px" alt="Overview architecture">
<br>
<br>

Description:
<ul>
<li>Exadata Smart Scan feature usage (Storage Index and Read IO Transfer Offloading):</li>
<ul>
    <li>- exa_smart_scan_pct = percent of physical reads benefits from exadata smart scan features</li>
    <li>- exa_storage_index_pct = percent of smart scan able physical reads avoided by exadata storage index feature</li>
    <li>- exa_read_offload_pct = percent of physical reads avoided by exadata offload feature</li>
<li>High ratios indicate massive exadata read io reduction feature usage!</li>
</ul>





