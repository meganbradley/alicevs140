---
title: "Linker Tools Error LNK2039"
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
ms.assetid: eaa296bd-4901-41f6-8410-6d03ee827144
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Linker Tools Error LNK2039
importing ref class '<type\>' that is defined in another.obj; it should be either imported or defined, but not both  
  
 The ref class '<`type`>' is imported in the specified .obj file but is also defined in another .obj file. This condition can cause runtime failure or other unexpected behavior.  
  
### To correct this error  
  
1.  Check whether '`type`' must be defined in the other .obj file and check whether it must be imported from the .winmd file.  
  
2.  Remove either the definition or the import.  
  
## See Also  
 [Linker Tools Errors and Warnings](../vs140/Linker-Tools-Errors-and-Warnings.md)   
 [LNK1332](../vs140/Linker-Tools-Error-LNK1332.md)