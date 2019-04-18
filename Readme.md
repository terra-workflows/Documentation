This document consolidates the expectations from the several files that are currently in the google drive.

![Current documents in the drive](Terra_Documents.png)


## Dashboard

* [ ] Title  
* [ ] Overview Paragraph 
* [ ] Experimental Design (required for analysis-focused workspaces) 
* [ ] Data
      * [ ] Sample Data
      * [ ] Workspace Data
* [ ] Tools
* [ ] Tool Name Versions 
* [ ] Notebooks 
* [ ] Software versions
* [ ] Time and cost
* [ ] Contact Information
* [ ] Licensing

[Example Dashboard](Example_Dashboard.png)
[Template Document](Terra_FW_Template.pdf)

## WDL

* [ ] WDL is in a repository

     ### SCIENTIST IS PROVIDING THE REPO 

     - [ ] Scientist has a method in the Firecloud Methods Repo
     - [ ] Scientist has uploaded wdl and json to Github 
          - [ ] & made a workflow in Dockstore
     - [ ] Scientist has created a ReadMe for the repo

          [Example README.md file for Scientist Repo](Template_Readme_Github_Repo.md)

     ### COMMS TEAM IS PROVIDING THE REPO 
     
     - [ ] Comms Team member has uploaded the wdl and json to  [terra-workflows github](https://github.com/terra-workflows/)
          - [ ] & made a workflow in Dockstore.
     - [ ] Comms Team Member has created a ReadMe for the repo
      
[Example Github Structure in terra-workflows](https://github.com/terra-workflows/tetralogy-of-fallot)
![Example Folders to be included in github](Example_github_structure.png)
      
[Example Workflow on Dockstore](https://dockstore.org/my-workflows/github.com/terra-workflows/tetralogy-of-fallot/Call-single-sample-GVCF-GATK)
![Example Worklow on Dockstore](Example_Workflow_Tool.png)
      


## Notebook

* [ ] All required dependencies are loaded
* [ ] Links to required startup scripts are provided
* [ ] The [instructions for using environmental variables](https://broadinstitute.zendesk.com/hc/en-us/articles/360026639112-New-Environmental-Variables-for-Jupyter-Notebooks) in the notebook are linked to inside the notebook.
* [ ] unchecked 
* [ ] unchecked 
* [ ] unchecked 

## Dataset 

* [ ] Workspace Attributes Loaded into Workspace
     - [ ] References uploaded to a google bucket that are publicly accessible.
     - [ ] References correspond to input files (e.g. input bams are aligned to hg38, then reference should be hg38.)
     - [ ] Access to all attribute files should be public. 
* [ ] Access to all dockers in the workspace attributes and WDLs should be public. [Broadies Instructions](https://software.broadinstitute.org/firecloud/documentation/article?id=6886)
* [ ] Data Models loaded into Workspace 
* [ ] Input and reference data uploaded to a google bucket.
     - [ ] Reference data sets required by the WDL and notebooks.
     - [ ] Test data sets to show that methods are working.
     - [ ] Directions on how to load full data sets into the data model provided in [Dashboard](Example_Dashboard.md)
     - [ ] If data is not fully accessible to the public, the dashboard contains instructions on how to obtain credentials.
* [ ] Access to all test files and references should be public.
     - [ ] Public bucket owned and maintained by Scientist.
     - [ ] Public bucket owned and maintained by [Comms Team](https://console.cloud.google.com/storage/browser/terra-featured-workspaces/?project=broad-dsde-outreach&organizationId=548622027621)

     Here is a code snipped that allows bucket owners to make their bucket public.  The user needs to have [Google SDK Tools](https://cloud.google.com/sdk/) installed on their local machine before running this code.
     
     ```
     gsutil acl ch -r -u AllUsers:R gs://path/to/bucket
     ```

## Review - In addition to reviewing the checklist above

* [ ] All WDL Analysis run with the Datasets provided.
* [ ] All test datasets, Workspace attributes, reference data and dockers are publicly readable.
* [ ] If full data sets are not public, instructions on how to obtain access are in the dashboard.
* [ ] All Notebooks Run and generate plots with no additional *ad hoc* loading of packages
* [ ] unchecked 
* [ ] unchecked 
* [ ] unchecked 
* [ ] unchecked 

## Finishing Steps

* [ ] unchecked 
* [ ] unchecked 
* [ ] unchecked 
* [ ] unchecked 
* [ ] unchecked 
* [ ] unchecked 


