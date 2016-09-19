---
title: "File Types Created for Visual C++ Projects"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2b0ee2e0-ae81-4185-9bb9-11da3c99a283
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# File Types Created for Visual C++ Projects
This topic describes all the types of files that are associated with Visual C++ projects for classic desktop applications. The actual files included in your project depend on the project type and the options you select when using a wizard.  
  
-   [Project and Solution Files](../vs140/Project-and-Solution-Files.md)  
  
-   [Files Created for CLR Projects](../vs140/Files-Created-for-CLR-Projects.md)  
  
-   [ATL Program or Control Source and Header Files](../vs140/ATL-Program-or-Control-Source-and-Header-Files.md)  
  
-   [MFC Program or Control Source and Header Files](../vs140/MFC-Program-or-Control-Source-and-Header-Files.md)  
  
-   [Precompiled Header Files](../vs140/Precompiled-Header-Files.md)  
  
-   [Resource Files](../vs140/Resource-Files--C---.md)  
  
-   [Help Files (WinHelp)](../vs140/Help-Files--WinHelp-.md)  
  
-   [Hint Files](../vs140/Hint-Files.md)  
  
 When you [create a Visual C++ project](../vs140/Creating-Desktop-Projects-By-Using-Application-Wizards.md), you might be creating a new solution, or you might be adding a project to a solution. Non-trivial applications are commonly developed with multiple projects in a solution.  
  
 Projects usually produce either an EXE or a DLL. Projects can be dependent on each other; during the build process, the Visual C++ environment checks dependencies both within and between projects. Each project has core source code, and depending on the kind of project, it may have many other files containing various aspects of the project. The contents of these files are indicated by the file extension. The Visual Studio development environment uses the file extensions to determine how to handle the file contents during a build.  
  
 The following table shows common files in a Visual C++ project, and identifies them with their file extension.  
  
|File extension|Type|Contents|  
|--------------------|----------|--------------|  
|.asmx|Source|Deployment file.|  
|.asp|Source|Active Server Page file.|  
|.atp|Project|Application template project file.|  
|.bmp, .dib, .gif, .jpg, .jpe, .png|Resource|General image files.|  
|.bsc|Compiling|The browser code file.|  
|.cpp; .c|Source|Main source code files for your application.|  
|.cur|Resource|Cursor bitmap graphic file.|  
|.dbp|Project|Database project file.|  
|.disco|Source|The dynamic discovery document file. Handles XML Web service discovery.|  
|.exe, .dll|Project|Executable or dynamic-link library files.|  
|.h|Source|A header (include) file.|  
|.htm, .html, .xsp, .asp, .htc, .hta, .xml|Resource|Common Web files.|  
|.HxC|Project|Help project file.|  
|.ico|Resource|Icon bitmap graphic file.|  
|.idb|Compiling|The state file, containing dependency information between source files and class definitions, which can be used by the compiler during minimal rebuild and incremental compilation. Use the [/Fd](../vs140/-Fd--Program-Database-File-Name-.md) compiler option to specify the name of the .idb file. See [/Gm (Enable Minimal Rebuild)](../vs140/-Gm--Enable-Minimal-Rebuild-.md) for more information.|  
|.idl|Compiling|An interface definition language file. See [Interface Definition (IDL) File](http://msdn.microsoft.com/library/windows/desktop/aa378712) in the [!INCLUDE[winsdkshort](../vs140/includes/winsdkshort_md.md)] for more information.|  
|.ilk|Linking|Incremental link file. See [/INCREMENTAL](../Topic/-INCREMENTAL%20\(Link%20Incrementally\).md) for more information.|  
|.map|Linking|A text file containing linker information. Use the [/Fm](../Topic/-Fm%20\(Name%20Mapfile\).md) compiler option to name the map file. See [/MAP](../vs140/-MAP--Generate-Mapfile-.md) for more information.|  
|.mfcribbon-ms|Resource|A resource file that contains the XML code that defines the buttons, controls, and attributes in the ribbon. For more information, see [Ribbon Designer (MFC)](../vs140/Ribbon-Designer--MFC-.md).|  
|.obj, .o||Object files, compiled but not linked.|  
|.pch|Debug|Precompiled header file.|  
|.rc, .rc2|Resource|[Resource script files](../vs140/Working-with-Resource-Files.md) to generate resources.|  
|.sbr|Compiling|Source browser intermediate file. The input file for [BSCMAKE](../vs140/BSCMAKE-Options.md).|  
|.sln|Solution|The [solution](assetId:///a45c299d-69f5-4b67-879d-1383417df0a7) file.|  
|.suo|Solution|The solution options file.|  
|.txt|Resource|A text file, usually the "readme" file.|  
|.vap|Project|A Visual Studio Analyzer project file.|  
|.vbg|Solution|A compatible project group file.|  
|.vbp, .vip, .vbproj|Project|The Visual Basic project file.|  
|.vcxproj|Project|The Visual C++ project file. See [Project Files and Makefiles](../vs140/Project-and-Solution-Files.md) for more information.|  
|.vcxproj.filters|Project|When Solution Explorer is used to add a file to a project, the filters file defines where in the Solution Explorer tree view the file is added, based on its file name extension.|  
|.vdproj|Project|The Visual Studio deployment project file.|  
|.vmx|Project|The macro project file.|  
|.vup|Project|The utility project file.|  
  
 For information on other files associated with Visual Studio, see [File Types and File Extensions in Visual Studio .NET](../vs140/Project-and-Solution-File-Types.md).  
  
 Project files are organized into folders in Solution Explorer. Visual C++ creates a folder for source files, header files, and resource files, but you can reorganize these folders or create new ones. You can use folders to organize explicitly logical clusters of files within the hierarchy of a project. For example, you could create folders to contain all your user interface source files, or specifications, documentation, or test suites. All file folder names should be unique.  
  
 When you add an item to a project, you add the item to all configurations for that project, regardless of whether or not the item is buildable. For example, if you have a project named MyProject, adding an item adds it to both the Debug and Release project configurations.  
  
## See Also  
 [Creating and Managing Visual C++ Projects](../vs140/Creating-and-Managing-Visual-C---Projects.md)   
 [Visual C++ Project Types](../vs140/Visual-C---Project-Types.md)   
 [Wizard Support for Other Languages](../vs140/Wizard-Support-for-Other-Languages.md)