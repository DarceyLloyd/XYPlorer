# XYPlorer configurations

## Video guide
https://youtu.be/cSMdQnxiye4

<br><hr><br>

## Open PHPStorm to active folder
1. Add user button to nav bar
2. Set name
3. Set icon as path to exe
4. At end of "on left click" line click edit and insert the following code.
<br>NOTE: You may need to change paths to suite your application paths

TIP: Want to run as admin, right click on app icon in start menu and choose MORE, then choose FILE LOCATION. Then on the shortcut right click and choose properties, tick run as administrator and press ok.

```
// SCRIPT: Run application with parameter 1 the active folder path
// WARNING: Add space after 1st line of code (bit of a WTF, but hey I didn't make XYPlorer)
$script_name = "PHPStorm open folder";
 $cpath = "<curpath>";
 $app = "C:\Program Files\JetBrains\PhpStorm 2022.3\bin\phpstorm64.exe";
 run """$app"" ""$cpath""";
```


<br><hr><br>

## Open VSCode to active folder or selected file
1. Add user button to nav bar
2. Set name
3. Set icon as path to exe
4. At end of "on left click" line click edit and insert the following code.
<br>NOTE: You may need to change paths to suite your application paths

TIP: Want to run as admin, right click on app icon in start menu and choose MORE, then choose FILE LOCATION. Then on the shortcut right click and choose properties, tick run as administrator and press ok.

```
// SCRIPT: Run application at active folder path or open selected file
// WARNING: Add space after 1st line of code (bit of a WTF, but hey I didn't make XYPlorer)
// WARNING: VSCode path will be different for you
 $cpath = "<curpath>";
 $selected = "<curname>";
 $app = "C:\Users\Darcey\AppData\Local\Programs\Microsoft VS Code\Code.exe";

 $target = "";
 if ($selected == "") {
    $target = $cpath;
 } else {
    $target = $selected;
 }

 run """$app"" ""$target""";
```


<br><hr><br>

## Open CMD to active folder
1. Add user button to nav bar
2. Set name
3. Set icon as path to exe
4. At end of "on left click" line click edit and insert the following code.
<br>NOTE: You may need to change paths to suite your application paths

TIP: Want to run as admin, right click on app icon in start menu and choose MORE, then choose FILE LOCATION. Then on the shortcut right click and choose properties, tick run as administrator and press ok.

```
// SCRIPT: Run application at active folder path or open selected file
// WARNING: Add space after 1st line of code (bit of a WTF, but hey I didn't make XYPlorer)
$script_name = "Open CMD at folder";
 $cpath = "<curpath>";
 $selected = "<curname>";
 $app = "%windir%\system32\cmd.exe";

 run """$app"" ""$cpath""";
```



<br><hr><br>

## Open CMDer to active folder
1. Add user button to nav bar
2. Set name
3. Set icon as path to exe
4. At end of "on left click" line click edit and insert the following code.
<br>NOTE: You may need to change paths to suite your application paths
5. Make folder at C:\Users\[[YOUR USER NAME]]\AppData\Local\CMDer
6. Download CMDer and extract to C:\Users\[[YOUR USER NAME]]\AppData\Local\CMDer

TIP: Want to run as admin, right click on app icon in start menu and choose MORE, then choose FILE LOCATION. Then on the shortcut right click and choose properties, tick run as administrator and press ok.

```
// SCRIPT: Run application at active folder path or open selected file
// WARNING: Add space after 1st line of code (bit of a WTF, but hey I didn't make XYPlorer)
$script_name = "Open CMDer at folder";
 $cpath = "<curpath>";
 $selected = "<curname>";
 $app = "C:\Users\Darcey\AppData\Local\CMDer\Cmder.exe";

 run """$app"" ""$cpath""";
```




<br><hr><br>

## Open PowerShell to active windows folder
1. Add user button to nav bar
2. Set name
3. Set icon as path to exe (%SystemRoot%\system32\WindowsPowerShell\v1.0\powershell.exe or C:\Program Files\PowerShell\7\pwsh.exe)
4. At end of "on left click" line click edit and insert the following code.
<br>NOTE: You may need to change paths to suite your application paths

TIP: Want to run as admin, right click on app icon in start menu and choose MORE, then choose FILE LOCATION. Then on the shortcut right click and choose properties, tick run as administrator and press ok.

NOTE: How this is getting the active folder I have no idea as the script doesn't pass it, so it might or might not work but at least it will open it

```
// SCRIPT: Run application with parameter 1 the active selection or folder path (selection takes priority)
// WARNING Space 1st after 1st line of code!!! WTF
// C:\Program Files\PowerShell\7\pwsh.exe -NoExit -Command "cd C:\MyScripts"
// %SystemRoot%\system32\WindowsPowerShell\v1.0\powershell.exe -NoExit;
// %windir%\system32\cmd.exe

$script_name = "Open PS7 in active folder";
 $command = "-NoExit";
 run """C:\Program Files\PowerShell\7\pwsh.exe"" ""$command""";
```