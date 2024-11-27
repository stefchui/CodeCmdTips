# CodeCmdTips
Code or Commnad Tips

## Msbuild Topics

### Use Case: How to build an MVC4 solution from the command line

Command 1:
```
msbuild ProjectFile.csproj /p:Configuration=Release ^
                           /p:Platform=AnyCPU ^
                           /t:WebPublish ^
                           /p:WebPublishMethod=FileSystem ^
                           /p:DeleteExistingFiles=True ^
                           /p:publishUrl=c:\output
```

Command 2:
```
msbuild Solution.sln /p:Configuration=Release ^ 
                     /p:DeployOnBuild=True ^
                     /p:DeployDefaultTarget=WebPublish ^
                     /p:WebPublishMethod=FileSystem ^
                     /p:DeleteExistingFiles=True ^
                     /p:publishUrl=c:\output
```

Command 3: using /t:SolutionFolder/Project:Target syntax
```
msbuild Solution.sln /t:SolutionFolder/ProjectFile:WebPublish ^
                     /p:Configuration=Release ^ 
                     /p:WebPublishMethod=FileSystem ^
                     /p:DeleteExistingFiles=True ^
                     /p:publishUrl=c:\output
```
