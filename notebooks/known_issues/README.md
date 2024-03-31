# Known Issues


### Asset Management
https://github.com/ooi-integration/asset-management

* The cycle for loading changes to asset information into the system is slow.
* Pull Request -> Release Tag -> Redmine Ticket -> Load onto Test -> Verification on Test -> Load onto Production -> Verification on Production.
* Automated Pull Request can be used to Load changes onto Production with DevOps tools similar to GitOps.
* To update asset information, if an operator with the right permissions uses the OOI (ooinet.oceanobservatories.org) user interface, these changes are neither recorded nor version controlled through this GitHub repository.

### Preload
https://github.com/oceanobservatories/preload-database

* This sheet is poorly formatted and contains parameters that are no longer produced by the system. Cleaning it up could stop proposed updates affecting the formatting of the sheet. 
* The process of integrating proposed changes into the system is not nclear. 
* Preload information should be available for query via an organized m2m endpoint.

### OOI Raw Data Parsers
https://github.com/oceanobservatories/mi-instrument  

* Cannot run data ingestion on Cabled Port Agent Log files, only raw data is stored in UW archive.

### OOI Data Product Algorithms
https://github.com/oceanobservatories/ion-functions/  

* It needs cleaning up to invite contributions from the user community.
* Could develop an M2M endpoint that allows users to specify a custom algorithm for processing on-demand data requests.


### QC Algorithm Values
https://github.com/ooi-integration/qc-lookup

* Global Range Test: Missing some values.
* Local Range Test: Does not work.
* Spike Test: Does not work reliably.
* Trend Test: Does not work.
* Gradient Test: Does not work.


### Annotations
* Parameter level annotations are referenced by PD number instead of name, making it hard for users to know which parameters are affected unless they parse a preload of GitHub (there is no preload m2m endpoint) or a data evaluator that includes the name of the affected parameter in the annotation.
* Annotation timestamps are returned as milliseconds since 1970, while data timestamps are returned as seconds since 1900.

