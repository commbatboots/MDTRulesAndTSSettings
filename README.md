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
      
## How to use it
1. Import Operating Systems
2. Build Capture folder under Task Sequence and disable from view
3. Build Tasksequence (using naming convention by folders in repo)

       eg.
       WIN10809_BC01 --> Build and Capture Tasksequence for Windows 10 1809
       WIN10809_BC02 --> Build and Capture Tasksequence for Windows 10 1809 with Office 
       WIN10_01 --> Tasksequence for Windows 10 Deployment
       WIN10_02 --> Tasksequence for Windows 10 with OFfice Deployment
       
4. Overwrite TS.xml with corresponding repo file
5. Build Make\Model folders for Out-of-Box Drivers
6. Import Drivers to corresponding make/model folder
7. Optional: Build Operating System\Component folders for Packages
8. Optional: Import Windows packages (eg. .Net cab files from ISO source\sxs) to Packages 
9. Optional: Build selection profiles for packages corresponding to Operating System
10. Import Applications
11. Create Custom folder unders %scriptsroot%
12. Create Logs folder under %Deployroot%
13. Create Capture folder under %Deployroot%
14. Edit tasksequence steps (to fix errors and paths):

        For Build and Capture only:
        Preinstall\Apply Packages --> Select Corresponding profiles or Nothing
        Install\Install Operating System --> Select Corresponding Operating System
        State Restore\Install Microsoft Office 2016 Pro Plus --> Change to imported Office Application
        State Restore\Windows Update (Post-Application Installation and Cleanup) --> Disable or remvoe if not using my ZTIWindowsUpdateWithCleanup.wsf script
        Capture Image\Clean Windows --> Disable or remvoe if not using Clean-ReferenceOS.ps1
        Capture Image\Clean Finish\Clean Harddrive --> Disable or remove if not using dispart clean script
        
        For deployment:
        There are ALOT of custom scripts in here. Remove what your don't use or just build a standard tasksequence
        
 15. Edit CustomeSettings.ini
 
         There are alot of custom rules in here: they have been sectionalized. Remove whats not needed
 16. test all tasksequences
       
        
