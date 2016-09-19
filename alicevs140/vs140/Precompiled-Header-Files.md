---
title: "Precompiled Header Files"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8228d87a-5609-41f3-9697-b16094c000e5
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Precompiled Header Files
These files are used to build a precompiled header file *Projname*.pch and a precompiled types file Stdafx.obj.  
  
 These files are located in the *Projname* directory. In Solution Explorer, Stdafx.h is in the Header Files folder, and Stdafx.cpp is located in the Source Files folder.  
  
|File name|Description|  
|---------------|-----------------|  
|Stdafx.h|An include file for standard system include files and for project-specific include files that are used frequently but are changed infrequently.<br /><br /> You should not define or undefine any of the _AFX_NO_XXX macros in stdafx.h; see the Knowledge Base article "PRB: Problems Occur When Defining _AFX_NO_XXX". You can find Knowledge Base articles in the MSDN Library or at [http:// support.microsoft.com/](http://%20support.microsoft.com/).|  
|Stdafx.cpp|Contains the preprocessor directive `#include "stdafx.h"` and adds include files for precompiled types. Precompiled files of any type, including header files, support faster compilation times by restricting compilation only to those files that require it. Once your project is built the first time, you will notice much faster build times on subsequent builds because of the presence of the precompiled header files.|  
  
## See Also  
 [File Types Created for Visual C++ Projects](../vs140/File-Types-Created-for-Visual-C---Projects.md)   
 [How to: Specify Project Properties with Property Pages](../vs140/How-to--Specify-Project-Properties-with-Property-Pages.md)