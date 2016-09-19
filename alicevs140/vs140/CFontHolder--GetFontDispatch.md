---
title: "CFontHolder::GetFontDispatch"
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
ms.assetid: b3b00e50-59e3-4709-afc9-9ccb359148e0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFontHolder::GetFontDispatch
Call this function to retrieve a pointer to the font's dispatch interface.  
  
## Syntax  
  
```  
  
LPFONTDISP GetFontDispatch( );  
```  
  
## Return Value  
 A pointer to the `CFontHolder` object's **IFontDisp** interface. Note that the function that calls `GetFontDispatch` must call `IUnknown::Release` on this interface pointer when done with it.  
  
## Remarks  
 Call `InitializeFont` before calling `GetFontDispatch`.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [CFontHolder Class](../vs140/CFontHolder-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFontHolder::InitializeFont](../vs140/CFontHolder--InitializeFont.md)