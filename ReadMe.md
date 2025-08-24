https://www.ibmmainframer.com/cobol-tutorial/</BR>


VSCODE:</BR>
Open Command Palette (Ctrl+Shift+P) → Tasks: Configure Task.</BR>
Select Create tasks.json file from template → Others.</BR>
Replace .vscode/tasks.json with:</BR>

```
{
  "version": "2.0.0",
  "tasks": [
    {
      "label": "Compile COBOL",
      "type": "shell",
      "command": "cobc",
      "args": [
        "-x",  // compile and link into executable
        "${file}", 
        "-o", 
        "${fileDirname}\\${fileBasenameNoExtension}.exe"
      ],
      "group": {
        "kind": "build",
        "isDefault": true
      },
      "problemMatcher": []
    },
    {
      "label": "Run COBOL",
      "type": "shell",
      "command": "${fileDirname}\\${fileBasenameNoExtension}.exe",
      "dependsOn": "Compile COBOL",
      "problemMatcher": []
    }
  ]
}
```

 cobc -x -o helloworld.exe h</BR>
 .\helloworld.exe</BR>

 https://programming-idioms.org/cheatsheet/Cobol</BR>

 git</BR>
 ```
 git init
 git config --global --add safe.directory D:/git/cobol
 git add.
 git commit -m 'Cobol first commit'
 git branch -M main
 git push -u origin main
 ```