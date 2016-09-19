---
title: "Default ATL Project Configurations"
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
ms.topic: reference
ms.assetid: 7e272722-41af-4330-b965-a6d74ec16880
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Default ATL Project Configurations
This topic compares the default ATL project configurations in Visual C++ .NET with the default project configurations in Visual C++ 6.0.  
  
## Visual C++ .NET Default Configurations  
 In Visual C++ .NET, the ATL Project Wizard creates two project configurations by default.  
  
### Visual C++ .NET Configurations  
  
|Configuration|Character set|Use of ATL|  
|-------------------|-------------------|----------------|  
|Release|MBCS|DLL|  
|Debug|MBCS|DLL|  
  
 **Character set**, **Use of ATL** and can all be changed in the **Project Settings** dialog under the **General** tab. You can also add your own configurations using the Configuration Manager. For details, see [Build Configurations](../vs140/Understanding-Build-Configurations.md).  
  
## Version 6.0 Default Configurations  
 In Visual C++ version 6.0, the ATL COM AppWizard (now called the ATL Project Wizard) created six project configurations by default. The configurations were variations on Release, Debug, Unicode, and use of CRT and ATL settings. All these configurations can be duplicated in Visual C++ .NET using the Configuration Manager, if so desired.  
  
### Version 6.0 Configurations  
  
|Configuration|Character set|Use of ATL|  
|-------------------|-------------------|----------------|  
|Debug|MBCS|Static|  
|Debug Unicode|UNICODE|Static|  
|Release Min Dependency|MBCS|Static|  
|Release Min Dependency Unicode|UNICODE|Static|  
|Release Min Size|MBCS|DLL|  
|Release Min Size Unicode|UNICODE|DLL|  
  
## See Also  
 [Programming with ATL and C Run-Time Code](../vs140/Programming-with-ATL-and-C-Run-Time-Code.md)   
 [Working with Project Properties](../vs140/Working-with-Project-Properties.md)   
 [Configuration Manager Dialog Box](assetId:///fa182dca-282e-4ae5-bf37-e155344ca18b)   
 [Compiling and Building](../vs140/Compiling-and-Building-in-Visual-Studio.md)