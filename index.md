---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
---


<html lang="en">
<head>   
 
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title></title>
    
</head>

<body>
<br>  

<nav>
    <ul>
        {% for item in site.data.menu %}
            <li>
                <a class="{% if page.url == item.link %}active{% endif %}" href="{{ item.link }}">{{item.title}}</a>
            </li>
        {% endfor %}
    </ul>

</nav>


<style>
    nav ul {
        display: flex;
        list-style: none;
    }
    nav ul li {
        margin-right: 10px;
    }
    nav ul li a {
        text-decoration: none;
        color: darkgrey
    }
    nav ul li a:hover {
        color: black;
    }
    .active {
        text-decoration: underline;
    }
</style>

<br>
<br>

<hr style="height:2px;border-width:0;color:gray;background-color:gray">


<h2 style="text-align: center;"> <a href="https://github.com/maiksandmann/maiksandmann.github.io/issues/new">Support us and create Issues & Feature enhancements here or to get in contact with us!</a></h2>

<hr style="height:2px;border-width:0;color:gray;background-color:gray">

<br>
<br>


<a href="https://www.atroposs.com"><img src="/picture/atroposs_logo.png" alt="ATROPOSS logo" widht=150 height=150></a>

<h2> Overview of ATROPOSS </h2>

<div style="text-align: justify">

ATROPOS is one of the greek godness which is cutting with a scissor the life thread of Humans. We like to give users a free of charge tool set to analyze their deployed solution stacks in direction to their data strategies which can be Opensource (OSS - Open Source Solutions) or others. That's the reason why we added a second S for <b>O</b>pen<b>S</b>ource<b>S</b>olutions to the name ATROPOSS. We wish all of you a happy reading.
<br>
By the way you can find us online under <a href="https://www.atroposs.com">ATROPOSS.com</a> as well. Please use for the english version the translation capabilities of your browser.

<br>
<br>


<p>
ATROPOSS is an open-source solution that is developed in a partner 2 partner motion with different partners to offer customers a secure, scalable and none intrusive scoping / discovery solution for their solution stacks. That includes application, databases, ETL processes and infrastructure related patterns.
</p> 

Because of the heterogeneity of the used solution stacks the first release focused on dedicated patterns like java applications, oracle / SQL Server databases, VMWare ESX environments. Because the application is modular written in Angular interested partners can join at anytime the eco systems and provide additional modules to enrich the capabilities on ATROPOSS in the future. A recipe for a new ATROPOSS template is available <a href="https://github.com/atroposs-migration/atroposs-sample-module">here</a>.

<br>
<br>

ATROPOSS is based on webassembly with JavaScript, <b>Python</b> or <b>RUST</b> but can also integrates modules written in <b>JavaScript</b>. The application with the modules will be executed in the secure sandbox of the user's browser! So, <b> no backend is required or involved and data are not leaving the laptop and browser of the user</b>. The scalability of the overall application (a static web page in summary) is realized over the number of frotend browsers. With WASM we based on an open Webstandard, which should be executible by all known browsers. 
<br>
<b>The created outputs of the ATROPOSS modules (csv, json or excel) can be downloaded on your file system. Please be aware that all kind of data should handle carefully and not store public. </b>
<br>
In case of any issues with your browser, please open a GitHub issue and let us know. 

<br>
<br>

The outputs of the modules are stored in different available formats on the filesystem of the user (if you are using windows OS it will by the download directory under your user directory). An additional value of ATROPOSS in the scoping / discovery phase is the avoidance to deploy third party agents inside the client networks because it based on the number of different logs your as an Oracle database administrator for example is using all the time. The solution is using all kind of existing log files like rvtools, output of sql scripts and Oracle's Automatic Workload Repository reports so called AWR's (please check if the required Oracle licenses Diagnostic/Tuning pack are licensed) or Statspack level 7 (if Enterprise Edtion without Diagnostic / Tuning pack licenses are deployed or Standard Edition are used), and correlate the found technical information for sizing and a first complexity check into business kpi's.

<br>
<br>

An final end2end reporting to correlate all outputs into one consolidated enterprise reporting is in work and will soon be available. Information about "What is missing" would be super helpful for us to focus on the features who are requested by real users. 

<br>
<br>

The following snapshot will give an overview about the current solution.

<br>

<div>

<img src="/picture/high_level_architecture.png" height="400px" width="700px" alt="Overview architecture">

<br>
<br>

In the next versions we will extend the features of ATROPOSS and provide for the project managers a central enterprise reporting and additional future modules of addtional solution patterns to scope and discover better deployed solution stacks. Feature requests or error reporting is welcome and can be realized over <b>the existing link on the top of the page</b>!

<br>
<br>

To support better the community, we decided to develop ATROPOSS in an opensource way, so that other partners & persons can join and contribute. The solution is built by using cutting-edge technologies with WebAssembly(WASM), Javascript and Python. As ATROPOSS runs in a modern browser there is no software or additional libraries required to deploy in the network. Because ATROPOSS is running on the local browser of the client, the data will only be stored in the session storage of the browser and removed once the user closes the browser/tab. The cached data in the session storage of the browser can be used as input data for other modules to avoid double efforts inside the other modules.

<br>
<br>

If you are interested in contributing to ATROPOSS, please discuss first changes / ideas you like to make via opening a GitHub issue,
email, or any other method with the ATROPOSS community before making a change. Read more about becoming a contributor in our GitHub Repo <a href="https://github.com/maiksandmann/maiksandmann.github.io#contributing">here</a>.

</div>


</body>

</html>
