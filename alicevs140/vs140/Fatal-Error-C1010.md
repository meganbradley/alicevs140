---
title: "Fatal Error C1010"
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
ms.topic: error-reference
ms.assetid: dfd035f1-a7a2-40bc-bc92-dc4d7f456767
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Fatal Error C1010
unexpected end of file while looking for precompiled header. Did you forget to add '#include name' to your source?  
  
 An include file specified with [/Yu](../vs140/-Yu--Use-Precompiled-Header-File-.md) is not listed in the source file.  This option is enabled by default in most Visual C++ Project types and "stdafx.h" is the default include file specified by this option.  
  
 In the Visual Studio environment, use one of the following methods to resolve this error:  
  
-   If you do not use precompiled headers in your project, set the **Create/Use Precompiled Header** property of source files to **Not Using Precompiled Headers**. To set this compiler option, follow these steps:  
  
    1.  In the Solution Explorer pane of the project, right-click the project name, and then click **Properties**.  
  
    2.  In the left pane, click the **C/C++** folder.  
  
    3.  Click the **Precompiled Headers** node.  
  
    4.  In the right pane, click **Create/Use Precompiled Header**, and then click **Not Using Precompiled Headers**.  
  
-   Make sure you have not inadvertently deleted, renamed or removed header file (by default, stdafx.h) from the current project. This file also needs to be included before any other code in your source files using **#include "stdafx.h"**. (This header file is specified as **Create/Use PCH Through File** project property)