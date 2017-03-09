# Salesforce DX Common Commands

These are SFDX commands I have found I use most often.

Feel free to suggest additions/changes.


## Setup
Create workspace `sfdx force:workspace:create --workspacename <workspace name>`

Create Scratch Org   `sfdx force:org:create --setdefaultusername -a <alias> -f config/workspace-scratch-def.json`

Open the org         `sfdx force:org:open`

Fetch Metadata       `sfdx force:mdapi:retrieve -s -r ./mdapipackage -u <alias or username> -p <package>`

Convert Metadata     `sfdx force:mdapi:convert --rootdir ./mdapipackage`

Switch default org   `sfdx force:config:set defaultusername=<alias>`


## Develop
Push to scratch	`sfdx force:source:push -u <alias or username>`

Pull from scratch     `sfdx force:source:pull -u <alias or username>`

Run tests `sfdx force:apex:test:run`

## Deploy
Convert to metadata  `sfdx force:source:convert -d mdapioutput_dir/`

Deploy to Org        `sfdx force:mdapi:deploy -d mdapioutput_dir/ -u <alias or username> -l RunSpecifiedTests -r <test1,test2>`

## Cleanup
Delete scratch org   `sfdx force:org:delete -u <alias or username>`

## Settings
Current configuration and settings: sfdx force:config:list
