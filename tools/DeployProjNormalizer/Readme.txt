This tool is to answer this problem: 
https://quality.embarcadero.com/browse/RSP-27612

Usage: 
DeployProjNormalizer.exe "<DprojFilename>" <createBackup>(ie: true/false)

This tool will create from the dproj a new deployproj file
from scratch and will normalize it (ie: order the node so that you
can compare different revision with diff compare tools). 

when you choose to create a backup the tool will normalize 
the existing deployproj and rename it to deployproj.bak so that 
you can make a diff compare against the new generated dployproj

To verify that this tool still work with a new delphi compiler: 
1/ Create a new multi plateform blank project
2/ Deploy each plateform/release and each time run this tool
   against the dproj with createBackup:true and make a diff 
   compare with the new generate deployproj vs deployproj.bak
3/ Run DprojNormalizer against the Dproj and them run again 
   this tool on the dproj with createBackup:true and make 
   a diff compare with the new generate deployproj vs 
   deployproj.bak   
4/ if you do not detect any difference => it's ok else you need
   to update the source code