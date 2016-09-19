---
title: "Setting Up a Static Link to the Registrar Code (C++ Only)"
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
ms.assetid: 835f5885-87a6-48fa-91e6-60988ee65538
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Setting Up a Static Link to the Registrar Code (C++ Only)
C++ clients can create a static link to the Registrar's code. Static linking of the Registrar's parser adds approximately 5K to a release build.  
  
 The simplest way to set up static linking assumes you have specified [DECLARE_REGISTRY_RESOURCEID](../vs140/DECLARE_REGISTRY_RESOURCEID.md) in your object's declaration. (This is the default specification used by the ATL.)  
  
### To create a static link using DECLARE_REGISTRY_RESOURCEID  
  
1.  Specify [/D](../Topic/-D%20\(Preprocessor%20Definitions\).md)`_ATL_STATIC_REGISTRY` instead of /D**_ATL_DLL**.  
  
2.  Recompile.  
  
## See Also  
 [Registry Component (Registrar)](../vs140/ATL-Registry-Component--Registrar-.md)