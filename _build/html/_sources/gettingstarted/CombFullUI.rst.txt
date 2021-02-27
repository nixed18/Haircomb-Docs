Building CombFullUI.exe
**************************

In order to use Haircomb, you'll need to build the wallet program.

First you'll need to download these tools:
 - `GoLang`_
 - `Git Bash`_
 
Next, open Git Bash, and a black command window will appear. Use the following commands:

1. cd Documents
2. git clone https://github.com/natasha-otomoski/combfullui.git
3. cd combfullui
4. go get github.com/gorilla/mux
5. go get github.com/sipa/bech32/ref/go/src/bech32
6. go build

There should now be a folder named "combfullui" in your Documents folder, and it should contain a file named "combfullui.exe."

If you get the message "bash: go: command not found" while building, follow these steps:

1. Open Control Panel
2. Open System and Security
3. Open System
4. Open Advanced System Settings
5. Open the Advanced tab
6. Open Environmental Variables
7. Select System Variables Path
8. Click Edit

Add a new row "C:\\Go\\Bin" (This should be the folder where "go.exe" was installed)
 
Close and open Git Bash again, but this time omit the "git clone" step.


 
 
 .. _GoLang: https://golang.org
 .. _Git Bash: https://git-scm.com/downloads