Dependencies: 
Install anaconda (for conda and jupyter notebook) https://www.anaconda.com/download
Install YeaZ in a conda environment titled yeaz https://github.com/rahi-lab/YeaZ-GUI/blob/master/readme.md
Enable conda in powershell https://gist.github.com/martinsotir/2bd2e16332dff71e0fa5be3ed3468a6c
Install Fiji https://imagej.net/software/fiji/downloads
Install Stardist plugin for Fiji https://imagej.net/plugins/stardist
--------------------------------------
--------------------------------------
0. Folder formating

make sure .nd2s of interest are in folders
.nd2 from experiment(s) should be in a folder 
.nd2 for autoflourescent normalization controls (ACY1516 cells) should be in a seperate folder

.nd2 files should only have RFP, GFP, and DIC channels. z-stack not supported at this time
---------------------------------------
1. FIJI/Stardist (do this step first, the powershell step needs a DIC layer only image which FIJI will split off as a .tif)

open fiji

go to Plugins>New>Macro

paste from FIJI_Macro.txt

in the fiji macro editor, click run. Enter the folder path (where .nd2 files are) in prompt
for each additional folder, click run in fiji macro editor and enter folder paths
---------------------------------------
2. PowerShell/YeaZ

open a new notepad, paste from PowerShell_Script.txt

replace [FOLDER PATH HERE] with folder path (where .nd2 files are)

open powershell

paste edited script and hit enter
for each additional folder, edit a script with appropriate folder path and hit enter
---------------------------------------
3. Jupyter

Open Anaconda

Start Jupyter

Open Image Analysis Nuclear with Autofluorescent v7.ipynb
click the first cell, hit ctrl+enter 

follow prompt 

