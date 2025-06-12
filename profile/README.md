<div align="center">

# SPI-Birds Code Library

<a href="https://spibirds.org">
  <img src="https://assets.dryicons.com/uploads/icon/preview/6913/small_2x_65dd15db-6b26-4c6e-b3e5-eea8ad3c6a42.png" alt="Homepage" width="30" height="30" style="margin: 10 5px;">
</a>
<a href="mailto:spibirds@nioo.knaw.nl">
  <img src="https://assets.dryicons.com/uploads/icon/svg/8069/f5795797-ab7a-4600-86b2-89cb508324e9.svg" alt="Email" width="30" height="30" style="margin: 10 5px;">
</a>
<a href="https://bsky.app/profile/spibirds.bsky.social">
	<svg width="30" height="30" viewBox="0 0 600 530" version="1.1" xmlns="http://www.w3.org/2000/svg" alt="Bluesky">
      <path d="m135.72 44.03c66.496 49.921 138.02 151.14 164.28 205.46 26.262-54.316 97.782-155.54 164.28-205.46 47.98-36.021 125.72-63.892 125.72 24.795 0 17.712-10.155 148.79-16.111 170.07-20.703 73.984-96.144 92.854-163.25 81.433 117.3 19.964 147.14 86.092 82.697 152.22-122.39 125.59-175.91-31.511-189.63-71.766-2.514-7.3797-3.6904-10.832-3.7077-7.8964-0.0174-2.9357-1.1937 0.51669-3.7077 7.8964-13.714 40.255-67.233 197.36-189.63 71.766-64.444-66.128-34.605-132.26 82.697-152.22-67.108 11.421-142.55-7.4491-163.25-81.433-5.9562-21.282-16.111-152.36-16.111-170.07 0-88.687 77.742-60.816 125.72-24.795z" fill="currentColor" />
    </svg>
</a>

SPI-Birds is a resource hub for data and code related to studies of populations of individual birds. Follow the links above to visit our website, contact us via e-mail, or to follow us on social media. 

Welcome to the SPI-Birds Code Library, a community-driven open-source LGPL-licensed code library *in development*, which aims to host scripts for data processing and analysis of SPI-Birds standardised data.
This README provides an overview of citable code workflows and information on how to contribute to the code library as both a code developer and code reviewer:

[Terms of Use](#terms-of-use)  
[Guide of available codes](#guide-of-available-codes)  
[Information for code developers](#information-for-code-developers)  
[Information for code reviewers](#information-for-code-reviewers)

</div>

<!-- to discuss 

different licenses for different code types, differentiating between "functions"/applications (LGPL) and whole scripts (not LGPL but MIT, for example)?

However, arguably, there's not enough unique intellectual property value to justify individual DOIs for code snippets that are easily-ish written by ppl

Licensing solution proposal:
The SPI-Birds Library has one DOI, and one license.
There's a stable version of the library (updated every 6months or once a year or whatever; with a how-to-cite, a DOI and the "SPI-birds seal of approval"), and there's a beta version of the library on GitHub with work-in-progress/under-review/"dirty" code

-->


# SPI-Birds Code Library: Introduction

The SPI-Birds Network and Database was established to facilitate access to data and collaborations between researchers working on populations on individually-marked birds. We are extending the functionality of SPI-Birds by building a library of peer-reviewed FAIR code for processing and analysing SPI-Birds standard data. 

All code in this repository is published under the GNU Lesser General Public License [LGPL](https://www.gnu.org/licenses/lgpl-3.0.en.html).

We value transparency in research and encourage community participation: Please contribute to collaborative code improvement and participate in code review! 



# Terms of Use: Code Licensing<a id='terms-of-use'></a>

The SPI-Birds Code Library is distributed under the GNU Lesser General Public License Version 3.0 (LGPL-3.0); the full text of the license can be found here: https://www.gnu.org/licenses/lgpl-3.0-standalone.html

Users can use and rework the licensed code, but if they distribute modifications to the source code, they must release these updates in source code form.

Users of code licensed under the GNU LGPL 3 must
- include a copy of the full license text and the original copyright notice
- make available the source code when you distribute a derivative work based on the licensed library
- license any derivative works of the library under the same or later version of the LGPL

In simpler terms, if someone modifies or distributes a work licensed under the LGPL-3.0, they must also provide the complete source code of their modifications to anyone who receives the modified work. This ensures that the spirit of openness and collaboration, central to open-source software, is maintained.

**Compatibility Information**

GNU LGPL (Lesser General Public License) is a weak copyleft license and allows linking with non-(L)GPL software, and therefore is more permissive than the GPL. LGPL can be used in a wider range of projects, including proprietary (closed-source) software. When incorporating code licensed under other licenses into an LGPL project, or when using LGPL-licensed code from this library in your project, you need to check compatibility.

Compatible Licenses: Permissive (Weak Copyleft) licenses that are fully compatible with LGPL include the MIT License, Zlib License, both the 2-clause and 3-clause BSD licenses, and the ISC License. The Apache License 2.0 is generally compatible, but be aware of the patent clauses, if applicable.

Incompatible Licenses: Strong copyleft licenses are not compatible with LGPL; for example, incorporating as GNU General Public License (GPL) or Affero General Public License (AGPL) would require the entire project to be licensed under the GPL/AGPL.

Example usecases: You can freely incorporate MIT-licensed code into your LGPL library, but you must include the MIT license text and attribution. Use dynamic linking when combining LGPL libraries with proprietary (closed-source) or other non-(L)GPL software to avoid licensing conflicts. If you modify the LGPL-licensed library itself or its open-source code, those modifications must be licensed under the same license as the original, i.e. LGPL.

# Guide of available codes

Pipelines to process the raw, primary data into the structure described in the [SPI-Birds standard data protocol](https://github.com/SPI-Birds/documentation/tree/master/standard_protocol) can be found in the [pipelines repository](https://github.com/SPI-Birds/pipelines). 

**Warranty statement**
The code published here has undergone peer-review to increase reusability, but may contain errors; SPI-Birds does not provide a guarantee of accuracy. 

---

# Submit code for peer review
Inside the Code Library, go to the [Code Review](tbc) folder, open a pull request, and request a reviewer. Alternatively, send code via email and the SPI-Birds editorial team will handle the process.

Metadata may be provided as a seperate file, or in the code script header.

### Information for code developers

The most useful code is correct, well-documented, and openly shared. Code review can help you learn new methods to improve the reliability, efficiency, style, and reusability of your code. Below, we summarise standards and resources that you might find useful for code development.

All code in this library is supposed to work seamlessly on any SPI-Birds standard-formatted data (see [SPI-Birds standard data protocol](https://github.com/SPI-Birds/documentation/tree/master/standard_protocol)). Please consider this during code development and testing. If you plan to develop a data-standardisation pipeline, which converts primary raw data into SPI-Birds' standard data format, please follow the detailed workflow recommendations in the [pipelines repository](https://github.com/SPI-Birds/pipelines).

By submitting code to the code library, you agree that it will be published under the  license.



##### Guide for Reproducible Code
The British Ecological Society produced a [Guide to Reproducible Code](https://www.britishecologicalsociety.org/wp-content/uploads/2017/12/guide-to-reproducible-code.pdf) in Ecology and Evolution, with useful information on organising projects (file system structure) to programming reproducible code (e.g., using relative paths for loading data).

##### Code Syntax in R
We expect that most code in this library will be written in R, and are therefore currently. The SPI-Birds team mostly works using the `tidyverse` packages; please try and use these packages to improve consistency and compatibility across code files.

##### Style Guide
Stylistic differences may seem opinionated and low-priority concerns, but can affect the overall efficiency and quality of collaborative projects: code review may not be as effective when reviewers are confronted with unfamiliar syntax or functions, and time-consuming or frustrating discussions about coding styles can avoided by agreeing to a standard.

Please refer to the [tidyverse style guide](https://style.tidyverse.org/) for naming conventions of files and object names. Useful R packages for automated style checks and formatting: `lintr` checks if you conform to the style guide, and `styler` (includes an RStudio add-in) can help restyle code sections, or entire files and projects.

##### Test code
Throughout development, please conduct basic tests to ensure that the code works as expected, also when using different inputs (e.g. population A, versus population B, versus multiple populations). When writing custom functions, tests should include if the function can deal with missing arguments. Consider using the R package [`testthat`](https://cran.r-project.org/web/packages/testthat/testthat.pdf) for writing tests, or the R package [`fuzzr`](https://cran.r-project.org/web/packages/fuzzr/vignettes/fuzzr.html) to check how your function responds to a range of unexpected inputs. 

You may use our example SPI-Birds standard data file to test your code.

##### Metadata Documentation
In addition to thorough commenting throughout the code, please make sure you provide the following metadata with your code:
- author details
- general description of the code's functionality
- description of all input arguments 

You may use our example metadata file.

---

# Funding



# Contribute to code review

The general workflow to review code that you have been assigned to
To contribute to this public repository, you have to fork it, clone your fork locally (i.e. work with a local version of the files), create a new branch for your changes, commit and push your changes, and finally open a pull request.

Make a pull request to [this repo] to submit your code file. If you are not comfortable using GitHub, contact [email] to send the files via email.
using templates: https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/configuring-issue-templates-for-your-repository

Actual review, and adding comments: Reviewers can add information to pull requests in the form of comments to instruct contributors on how to get approval for the changes they have worked on. Comments can be added to any specific line of code, or reviewers can leave general comments to the whole project (i.e., the entire pull request). More on commenting on a pull request: https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/commenting-on-a-pull-request

Alternatively, submit comments as a [new GitHub Issue](https://github.com/SPI-Birds/code/issues/new/choose), or email 

add labels -- TO DO: define labels
push your revised code to the remote's branch (`git push`) and a label the code according to areas where improvement is needed.


Limit review time
Reviewing code can be challenging, often requiring a surprising degree of concentration to be handled effectively. Setting time limits for reviews helps keep reviewers from missing important details. Whether they should simply take a break and return to finish their review or pass on remaining code to another reviewer is up to you.






### Information for code reviewers

Code review includes testing code for quality assurance; making sure the code is reproducible, interpretable and that it renders locally on your machine.
    
One key aspect of the code review should also be to test the pipelines on both Mac OSX and Windows.

Important quality check: does the code run on another SPI-Birds standard data set?

##### Reusability
  - Does the code contain a general description of what the code does?
  - Does it provide excessive documentation throughout, i.e. clear documentation that detail the rationale behind, e.g., data wrangling decisions and analytical approaches?
  - Does the code contain detailed metadata (e.g., a README file or a dedicated section at the beginning of the script), describing relevant details about data collection, processing, analysis and presentation
  - Are the files organised and named clearly and consistently, avoiding long names, spaces, and special characters?
  - Are all dependencies (associated scripts or software required to run the script) listed and do they load
  - Does the code specify which versions of packages/libraries were used?
- Are there references to other data, where applicable. Primary data should be included, either via repository upload or in the Appendix (provide DOIs). Secondary data users should cite the original data resources and respect all the conditions of data (re)use set by the data creators or managers. 
  - Is the whole workflow code/script-based? Is it self-contained (e.g., the code does not involve steps outside the script or pipeline, such as manual manipulation in other software like Excel)?
  - is the code readable, i.e. indentation? use of headers and sections? consistent formatting? informative naming of objects?




Join the SPI-Birds network: Sign up to ...

[GitHub Discussions](https://github.com/scikit-bio/scikit-bio/discussions): This is your go-to place for asking questions, Alternatively, you can report issues and bugs via [GitHub Issues](https://github.com/spibirds/..issues). 

We enthusiastically welcome community contributions -- from adding new code workflows for peer review or improving code and its documentation ([guidelines for code review](https://..)) !


## Review

*Please check off boxes as applicable, and elaborate in the comments below. Your review is not limited to these topics, as described in the reviewer guide*


- **Briefly describe any working relationship you have (had) with the package authors.**
- [ ] As the reviewer I confirm that there are no [conflicts of interest](https://devguide.ropensci.org/policies.html#coi) for me to review this work (if you are unsure whether you are in conflict, please speak to your editor _before_ starting your review).

#### Documentation

The package includes all the following forms of documentation:

- [ ] **A statement of need:** clearly stating problems the software is designed to solve and its target audience in README
- [ ] **Installation instructions:** for the development version of package and any non-standard dependencies in README
- [ ] **Vignette(s):** demonstrating major functionality that runs successfully locally
- [ ] **Function Documentation:** for all exported functions
- [ ] **Examples:** (that run successfully locally) for all exported functions
- [ ] **Community guidelines:** including contribution guidelines in the README or CONTRIBUTING, and DESCRIPTION with `URL`, `BugReports` and `Maintainer` (which may be autogenerated via `Authors@R`).

#### Functionality

- [ ] **Installation:** Installation succeeds as documented.
- [ ] **Functionality:** Any functional claims of the software have been confirmed.
- [ ] **Performance:** Any performance claims of the software have been confirmed.
- [ ] **Automated tests:** Unit tests cover essential functions of the package and a reasonable range of inputs and conditions. All tests pass on the local machine.
- [ ] **Packaging guidelines**: The package conforms to the rOpenSci packaging guidelines.

Estimated hours spent reviewing:

- [ ] Should the author(s) deem it appropriate, I agree to be acknowledged as a package reviewer ("rev" role) in the package DESCRIPTION file.

---

### Review Comments


