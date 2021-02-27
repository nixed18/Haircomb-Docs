General Use Guidelines
****************************

Haircomb relies on a commits.db file to store information from the Bitcoin blockchain. Unfortunately, the commits file is easy to corrupt. Here are some guidelines to follow to keep your Haircomb running smoothly.
 
 
**Startup**

1. Launch "combfullui.exe"
2. Launch the Modified BTC
 
 
**Shutdown**

1. Shut down the Modified BTC. Wait for the Modified BTC to completely close.
2. Open up the Haircomb client and click the Safe Shutdown button. Safe Shutdown will not shut down Haircomb unless your wallet has been saved properly.
 
If you follow these steps when using Haircomb, your "commits.db" file should be fine. However, you can be extra careful and make a backup of your "commits.db" file, just in case. 
 
 
**Backup** 

0. If your Haircomb is open, shut it down by following the Shutdown instructions.
1. Shut down Haircomb by following the Shutdown instructions. 
2. Copy and paste your "commits.db" file
3. Rename the copy if desired.
 
 
**Restore**

0. If your Haircomb is open, shut it down by following the Shutdown instructions.
1. Delete your "commits.db" file
2. Make a copy of your commits backup, and move it to the same folder as your "combfullui.exe"
3. Rename your Commits copy to "commits.db"
4. Launch Haircomb by following the Startup instructions, and let the Modified BTC rebuild any missing commitments.