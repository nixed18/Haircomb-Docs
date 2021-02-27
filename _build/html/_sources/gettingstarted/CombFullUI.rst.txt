Building CombFullUI.exe
**************************

In order to use Haircomb, you'll need to build the wallet program.

First you'll need to download these tools:
 - `GoLang`_
 - `Git Bash`_
 
Next, open Git Bash, and a black command window will appear. Use the following commands:
 - cd Documents
 - git clone https://github.com/natasha-otomoski/combfullui.git
 - cd combfullui
 - go get github.com/gorilla/mux
 - go get github.com/sipa/bech32/ref/go/src/bech32
 - go build

There should now be a folder named "combfullui" in your Documents folder, and it should contain a file named "combfullui.exe."

If you get the message "bash: go: command not found" while building, follow these steps:
 - Open Control Panel
 - Open System and Security
 - Open System
 - Open Advanced System Settings
 - Open the Advanced tab
 - Open Environmental Variables
 - Select System Variables Path
 - Click Edit
 - Add a new row "C:\Go\Bin" (This should be the folder where "go.exe" was installed)
 
 Close and open Git Bash again, but this time omit the "git clone" step.


 
 
 .. _GoLang: https://golang.org
 .. _Git Bash: https://git-scm.com/downloads