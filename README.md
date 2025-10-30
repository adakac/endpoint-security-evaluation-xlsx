# Endpoint Security Evaluation with MITRE ATT&CK
<a href="https://github.com/adakac/endpoint-security-evaluation-xlsx/releases/latest"><img src="https://img.shields.io/github/v/release/adakac/endpoint-security-evaluation-xlsx?label=Release&color=brightgreen&cacheSeconds=3600" alt="Release"/></a>
<a href="./LICENSE.txt">[![CC BY 4.0][cc-by-shield]][cc-by]</a>
<br>
This project aims to provide an Excel file based Endpoint Security solution for a meta-risk asessment after MITRE ATT&CK, that is accessible to all company sizes and reflects both theoretical IT security factors and the company's point of view.

## Introduction
Some standards already allow for some kind of evaluation of endpoint security, but most of them are hardly feasible for small and medium-sized companies. This led to the development of the following system -  the aim was to design an easy-to-use, easy-to-maintain system that combines the requirements of the respective company with a practical evaluation system. The Endpoint Security Evaluation System (ESE) should make it easier to derive precise measures for your company and at the same time obtain rough metrics on the state of security.

## Versions
Starting with ESE v2.0 not only Windows devices are affected by the evaluation. The evaluation is split into "Clients" (OS agnostic), "Infrastructure" (including ESXi, servers and networking) and "Services" (cloud services). All previous versions (<ESEv1.4) are made for Windows Clients only. With ESE v2.2 we switched to a ODS master file - for optimal use, please read the following notes:

Using our ODS release, ensure you disable Comment Authorship under "Options/LibreOffice Calc/View", otherwise some comments may get cut off.

Using our XLSX release, notice that MS Office does incorrectly round up all of the pie charts results. This does not influence the data itself, it is just those pie charts. ODS does reflect the data correctly.

## Methods
The evaluation model is based on the MITRE ATT\&CK framework, as this provides an internationally recognized basis and is also updated cyclically according to a defined scheme.
The initial version of the evaluation model was based on MITRE ATT&CK version 10. In the course of the initial publication, the defined update processes were applied up to version 12.
On the MITRE ATT&CK Framework website, it is difficult to differentiate which version is currently being displayed. To avoid confusion in this process, we would like to point out that the MITRE ATT&CK version of the currently displayed technique is shown on the a banner on the top as well as on the bottom of the website.

MITRE ATT&CK is divided into three matrices - one each for companies (enterprise), mobile devices and industrial plants. In this evaluation model, the enterprise matrix was taken as the basis. This is structured into so-called techniques, which can have multiple sub-techniques but are enclosed by categories called tactics. For example, the technique “Domain Account” can be found under the "Account Discovery", which in turn can be found in the "Discovery" tactic.

Each technique contains a general explanation, known practical applications, recommended mitigation steps and monitoring options. In some techniques, no in-depth mitigations or monitoring options are offered, as these cannot realistically be mitigated in the time available; for example, in the vector “Gather Victim Identity Information: Employee Names".

### Evaluation
Both the analysis and the evaluation are carried out in the form of an Excel file. As the broad availability and usability for large, small and medium-sized enterprises is one of the aims of this evaluation model, attention was paid to ease of use where possible. The use of Microsoft Excel represents a compromise, which makes this project available for most company sizes. More specialized software would perhaps be more intuitive, but would limit compatibility. 

### Rating System
The aim of the evaluation system is to combine a good evaluation basis with individual risk factors. A 6-point scale is used for this purpose. The higher this value, the higher the criticality of the respective technique for the company in question. Half of the points are statically determined by the impact on the CIA system (confidentiality, integrity, authenticity). The remaining three points are determined by the company's IT security department itself. These are intended to reflect a subjective expert opinion as well as the company's risk appetite. Each technique is considered on a standalone basis: For example, the encrypted extraction of data from a system is assessed separately from the actual infiltration of the Trojan. Even if your company does not use a specific service required for a technique, the subjective analysis should be done in a way that takes your possible future implementation of such a service into account.

The three company-specific points should be awarded according to the following scale:

* 1 point - Priority Medium - Low losses on utilization, expected risks, unlikely
* 2 points - Priority High - Losses on utilization, accepted risks, probable
* 3 points - Priority Very High - Large loss on utilization, high risk, high probability

This expert evaluation is recommended to be done in a 12 month interval.

### The Risk Matrix
The situation is graded using a standardized risk matrix. This can be adapted in theory, however, adaptation is not recommended as the prioritization and scaling of the system was already taken into account when it was created - changes would most likely lead to uneven distribution.
<p align="center"><img src="https://i.imgur.com/NQo5HnK.png" alt="Table 1"/> </p>
<p align="center"><img src="https://i.imgur.com/qlkqJ7k.png" alt="Table 2"/> </p>

### Evaluation Results
Once the assessment has been carried out for each technique, an overall picture of the company's IT security situation is created. In the “Overview” tab of the spreadsheet, the current security level and rating can now be read from the diagram. Depending on the business sector and the requirement profile, a result between A and A+ or higher is generally desirable. These categories assume that the most problematic vectors have been mitigated and that there is also good basic protection for less dangerous techniques. 

### Maintaining and Updating ESE
As new major releases of the MITRE ATT&CK Framework are published every year, it is also advisable to maintain the evaluation system on an ongoing basis, in the sense of a PDCA cycle (Plan-Do-Check-Act).

This should be done at least once a year to ensure that the system is up to date and that current threats can be appropriately assessed. However, the evaluation system should also be revised if new threats have been identified or existing ones have changed significantly. In addition, the constantly changing conditions in modern companies also make ongoing reviews of the evaluation system necessary. Through regular maintenance and updating, the company can ensure that it can react optimally to threats and keep its IT security up to date.

The update procedure begins with a review of the MITRE ATT&CK update log. All changes are checked and updated in the evaluation system - for example, completely new techniques may have been added or old ones may have been removed. Newly added techniques require initial evaluation.

Evaluations of criticality were done by several IT security experts, serving as the basis for evaluating the default values for the expert opinion. The decision to integrate default values is intended to help companies to quickly obtain an evaluation with minimal effort. Differentiation/precision on factors such as company size would be helpful here in order to generate even more realistic default values for the respective types of company. Alternatively, consideration could also be given to removing these default values in order to force a precise evaluation by the IT security department at the expense of accessibility.

## Conclusion
ESE allows companies of all sizes to easily integrate a known security evaluation tool into their processes. The practice-oriented approach quickly leads to results, which can easily be summarized for executive summaries. The model not only integrates expert opinions, but also concrete improvement approaches, which can also be looked up centrally thanks to MITRE ATT&CK. Even if the model focuses on a practical orientation, the constant updating of the underlying MITRE ATT&CK database can be perceived as time-consuming for small and medium-sized companies. Nevertheless, even versions of ESE based upon older MITRE ATT&CK Framework versions, offer a very good basis of protection.

## Thanks
Thanks to [lostalien2099](https://github.com/lostalien2099) and Lukas S. for lending their time and expertise for the base evaluation and creation of this project up to v1.1.

## Disclaimer
This project has NO affiliation with, sponsorship, or endorsement by MITRE. This project does NOT represent the views and opinions of MITRE or MITRE personnel.

## Licensing
[![CC BY 4.0][cc-by-shield]][cc-by]

This work is licensed under a
[Creative Commons Attribution 4.0 International License][cc-by].

[![CC BY 4.0][cc-by-image]][cc-by]

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg

You are free to:
* Share — copy and redistribute the material in any medium or format for any purpose, even commercially.
* Adapt — remix, transform, and build upon the material for any purpose, even commercially.
* The licensor cannot revoke these freedoms as long as you follow the license terms.

Under the following terms:
* Attribution — You must give appropriate credit , provide a link to the license, and indicate if changes were made . You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.
* No additional restrictions — You may not apply legal terms or technological measures that legally restrict others from doing anything the license permits.


