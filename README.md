# + ArkOffsetDumper 💻
Offset Dumper - A text file based offset dumper in which can retrieve or print class/structure property & function offsets by name!

***[NOTICE: IN ITS CURRENT STATE OFFSET DUMPER IS NOT STEAM ARK SUPPORTIVE - THIS MAY CHANGE IN THE FUTURE]***

# + Instructions (Class Dump) 📝
**[1] - Ensure Your GObjects & GNames Offsets Are Up To Date In 'Dump/SDK.h'. (This Will Not Be Necessary In The Future)**

**[2] - Visit 'Dump/Logger.h' & Change The std::wstring Definition Of 'OutputPCUser' To Your PC Username, PC Username Can Be Found At 'C:\Users\' In File Explorer!**

**[3] - Visit 'Dump/Dump.cpp' & Look For 'OffsetDumper::DumpRequestedOffsets' Function Code, Within The Function Code After The Initialize Functions Write Out The Function Calls You Want To Make For The Classes You Are Targeting (Comments Provided In 'Dump/Dump.h')**

**[4] - Build DLL/Project & Use Your Choice Of Injector To Inject To ShooterGame.exe, The Outputted Information Will Be In A Text File At The Path Used In 'Dump/Logger.h'**

**[✔] - Enjoy Freshly Gathered Class Offsets**
```c++
OffsetDumper::DumpPartialClass("Class Engine.Actor", std::vector<std::string>{ "TargetingTeam", "CreationTime","RootComponent", "LastRenderTime", "bForceNonBlockingHits" }, std::vector<std::string>{ "int", "double", "USceneComponent*", "double", "bool" });**
```

# + Instructions (Function Dump) 📝
**[1] - Visit 'Dump/Dump.cpp' & Inside 'OffsetDumper::DumpRequestedOffsets' Function Code Write Out The Calls You Want To Make For Target Functions!**

**[2] - Visit 'Dump/Logger.h' & Change The std::wstring Definition Of 'OutputPCUser' To Your PC Username, PC Username Can Be Found At 'C:\Users\' In File Explorer!**

**[3] - Build DLL/Project & Use Your Choice Of Injector To Inject To ShooterGame.exe, The Outputted Information Will Be In A Text File At The Path Used In 'Dump/Logger.h'**

**[✔] - Enjoy Freshly Gathered Function Offsets**
```c++
auto Offset = OffsetDumper::FindFunctionOffset("UObject::ProcessEvent");
```

**[OR]**
```c++
auto FunctionAddress = DetourFindFunction("ShooterGame.exe", "UObject::ProcessEvent");
```

