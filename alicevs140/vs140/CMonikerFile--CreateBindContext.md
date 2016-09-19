---
title: "CMonikerFile::CreateBindContext"
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
ms.assetid: ef4511f8-3bc7-4254-8dd0-08db410c6785
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMonikerFile::CreateBindContext
Call this function to create a default initialized bind context.  
  
## Syntax  
  
```  
  
      IBindCtx* CreateBindContext(   
   CFileException* pError    
);  
```  
  
#### Parameters  
 `pError`  
 A pointer to a file exception. In the event of an error, it will be set to the cause.  
  
## Return Value  
 A pointer to the bind context [IBindCtx](http://msdn.microsoft.com/library/windows/desktop/ms693755) to bind with if successful; otherwise **NULL**. If the instance was opened with an `IBindHost` interface, the bind context is retrieved from the `IBindHost`. If there is no `IBindHost` interface or the interface fails to return a bind context, a bind context is created. For a description of the [IBindHost](http://msdn.microsoft.com/library/ie/ms775076) interface, see the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Remarks  
 A bind context is an object that stores information about a particular moniker binding operation. You can override this function to provide a custom bind context.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [CMonikerFile Class](../vs140/CMonikerFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)