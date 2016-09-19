---
title: "COleDataObject::Release"
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
ms.assetid: 1ee76d0b-75b3-4d32-9646-6650779275ef
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDataObject::Release
Call this function to release ownership of the [IDataObject](http://msdn.microsoft.com/library/windows/desktop/ms688421) object that was previously associated with the `COleDataObject` object.  
  
## Syntax  
  
```  
  
void Release( );  
```  
  
## Remarks  
 The `IDataObject` was associated with the `COleDataObject` by calling **Attach** or `AttachClipboard` explicitly or by the framework. If the `bAutoRelease` parameter of **Attach** is **FALSE**, the `IDataObject` object will not be released. In this case, the caller is responsible for releasing the `IDataObject` by calling [IUnknown::Release](http://msdn.microsoft.com/library/windows/desktop/ms682317).  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDataObject Class](../vs140/COleDataObject-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDataObject::Attach](../vs140/COleDataObject--Attach.md)   
 [COleDataObject::COleDataObject](../vs140/COleDataObject--COleDataObject.md)   
 [COleDataObject::Detach](../vs140/COleDataObject--Detach.md)