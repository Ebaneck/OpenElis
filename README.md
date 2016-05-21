Lab System
========

[![Build Status](https://travis-ci.org/Ebaneck/OpenElis.svg?branch=master)](https://travis-ci.org/Ebaneck/OpenElis)


*To build OpenElis run*
* `ant dist`  Creates OpenELIS War
* `ant setupDB test dist`  Creates clinlims database in postgres, runs tests, and then creates OpenELIS War
* `./scripts/vagrant-deploy.sh` Create OpenELIS War and deploys it to your vagrant's tomcat
* `./scripts/vagrant-database.sh` Runs Liquibase migration script in your vagrant 

Technical issues with the codebase
======================================

- Transaction and Hibernate session management
- Pagination handled via HttpSession
- Code duplication in various places (need examples here)
	- ResultValidationPaging, ResultsPaging and AnalyzerResultsPaging. Same copy-pasted code with very minor difference.

Functional changes made by us
=============================
- The order should contain the panel along with the tests. Hence making panel more than convenience tool for selecting multiple tests.
- REST endpoint for Patient, LabResults

- Added functionality to validate test results by a particular accession number. Also you can see items to be validated across all test sections.

