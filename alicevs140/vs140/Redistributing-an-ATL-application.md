---
title: "Redistributing an ATL application"
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
ms.assetid: 9a696b22-2345-43ec-826b-be7cb8cfd676
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Redistributing an ATL application
Starting in Visual Studio 2012, Active Template Library (ATL) is a header-only library. ATL projects do not have a Dynamic Link to ATL option. No redistributable ATL library is required.  
  
 If you redistribute an ATL executable application, you must register the .exe file (and any controls inside it) by issuing the following command:  
  
```  
filename /regserver  
```  
  
 where `filename` is the name of the executable file.  
  
 In Visual Studio 2010, an ATL project can be built for a MinDependency or a MinSize configuration. A MinDependency configuration is what you get when you set the **Use of ATL** property to **Static Link to ATL** on the **General** property page and set the **Runtime Library** property to **Multi-threaded (/MT)** on the **Code Generation** property page (C/C++ folder).  
  
 A MinSize configuration is what you get when you set the **Use of ATL** property to **Dynamic Link to ATL** on the **General** property page, or set the **Runtime Library** property to **Multi-threaded DLL (/MD)** on the **Code Generation** property page (C/C++ folder).  
  
 MinSize makes the output file as small as possible but requires that ATL100.dll and Msvcr100.dll (if you selected the **Multi-threaded DLL (/MD)** option) are on the target computer. ATL100.dll should be registered on the target computer to ensure that all ATL functionality is present. ATL100.dll contains ANSI and Unicode exports.  
  
 If you build your ATL or OLE DB Templates project for a MinDependency target, you do not need to install and register ATL100.dll on the target computer, although you might get a larger program image.  
  
 If you redistribute an ATL executable application, you must register the .exe file (and any controls inside it) by issuing the following command:  
  
```  
filename /regserver  
```  
  
 where `filename` is the name of the executable file.  
  
 For OLE DB Templates applications, ensure that the target computer has the latest versions of Microsoft Data Access Components (MDAC) files. For more information, see [Redistributing Database Support Files](../vs140/Redistributing-Database-Support-Files.md).  
  
## See Also  
 [Redistributing Visual C++ Files](../vs140/Redistributing-Visual-C---Files.md)