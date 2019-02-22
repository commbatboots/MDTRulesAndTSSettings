# MDT Rules With TaskSequence Settings
MDT deployment rules with Tasksequences for capturing and deployments

## Project: 
 - This is part of my <b>MDT automation Project</b>

## What it does:
<br>Here are rule and task sequences I use for a fully automated capture and deployment
- Rules have custom settings used in other parts of my MDT automation project repos
- TaskSequences also pasts of my MDT automation project repos

## Knowledge
- Understand that every MDT environment is different.
- Knowledge on how to edit task sequences and how to change MDT rule based on your envrionment.
- All of my custom scripts are located un %deployroot%\scripts\Custom. Some are futher located in subfolders such as:
         
      %deployroot%\scripts\Custom\OS-Configs\Win10OptimizeAndConfig.ps1
      %deployroot%\scripts\Custom\OS-Customizations\Invoke-RemoveBuiltinApps.ps1
      
- Windows Operating Systems are up to you to import. Capturing images are located in  %deployroot%\Captures
- Drivers are up to you to import. NOTE driver detection is based on %make%\%model% folder structure
