## Dashboard

* [x] Title  
* [x] Overview Paragraph 
* [ ] Experimental Design (required for analysis-focused workspaces) 
* [ ] Data 
     - [ ] Sample Data
     - [ ] Workspace Data
* [ ] Tools
* [ ] Tool Name Versions 
* [ ] Notebooks 
* [ ] Software versions
* [ ] Time and cost
* [x] Contact Information
* [x] Licensing

[Example Dashboard](Example_Dashboard.md)

[Template Document](Terra_FW_template.pdf)

## WDL

* [ ] WDL is in a repository

     ### SCIENTIST IS PROVIDING THE REPO 

     - [ ] Scientist has a method in the Firecloud Methods Repo
     - [ ] Scientist has uploaded wdl and json to Github 
          - [ ] & made a workflow in Dockstore
     - [ ] Scientist has created a ReadMe for the repo

          [Template for README.md from Colaboratory in Google Drive](Readme_Template_Beri.md)
          
          [Example README.md file for Scientist Repo](Example_Readme_Github_Repo.md)

     ### COMMS TEAM IS PROVIDING THE REPO 
     
     - [ ] Comms Team member has uploaded the wdl and json to  [terra-workflows github](https://github.com/terra-workflows/)
          - [ ] & made a workflow in Dockstore.
     - [ ] Comms Team Member has created a ReadMe for the repo
     
* [ ] Repos containing WDL contain the [Broad Licensing File](LICENSE) or equivalent if covered under a different license.
      

## Notebook

* [ ] All required dependencies are loaded
* [ ] Links to required startup scripts are provided
* [ ] The [instructions for using environmental variables](https://broadinstitute.zendesk.com/hc/en-us/articles/360026639112-New-Environmental-Variables-for-Jupyter-Notebooks) in the notebook are linked to inside the notebook.

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
* [ ] The provided WDL/Inputs/Resources/Docker Images must be able to complete successfully with valid resultsFor example, variant callers should be calling variants in known locations for the input data.
* [ ] The summary of the pipeline and/or work provides enough detail for someone not knowledgeable about the method to be able to run it successfully.
* [ ] Relevant publications are linked in the dashboard.

## Finishing Steps

* [ ] Have the Science Advisor look over the workspace and have them focus on making sure what’s written in the workspace summary is scientifically accurate and the generated outputs are correct. 
* [ ] Have a person from Eds review workspace so that the workspace summary communicates its contents effectively
* [ ] Notify Eric Karofsky (erickarofsk@broadinstitute.org) (optional)
* [ ] Create a final version of the workspace by cloning the draft workspace created earlier in to the appropriate billing project ID (same as namespace). 
     - [ ] Scientists Billing Project if hosted and maintained by their lab.
     - [ ] gatk-help if the workspace is hosted and maintained by Comms and related to GATK
     - [ ] OBJECT-NAME-TBD if the workspace is hosted and maintained by Comms and not GATK
* [ ] Get the final approval from Beri {for the moment, and possibly Tiffany, Robert, or Geraldine if there are higher level issues needing to be addressed}
* [ ] Make the workspace public (Beri, Tiffany, Sushma and Adelaide currently have permissions.  One of these people need to be an owner on the workspace in order to make it public.

* [ ] Once it’s public, you can use the [Firecloud SOP on the dsde-docs wiki] (https://github.com/broadinstitute/dsde-docs/wiki/FireCloud-SOP) to make it featured.

