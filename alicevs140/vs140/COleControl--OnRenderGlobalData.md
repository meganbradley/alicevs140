---
title: "COleControl::OnRenderGlobalData"
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
ms.assetid: aaf8f4c4-584c-48db-8360-a0119125c9f3
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::OnRenderGlobalData
Called by the framework to retrieve data in the specified format when the specified storage medium is global memory.  
  
## Syntax  
  
```  
  
      virtual BOOL OnRenderGlobalData(  
   LPFORMATETC lpFormatEtc,  
   HGLOBAL* phGlobal   
);  
```  
  
#### Parameters  
 `lpFormatEtc`  
 Points to the [FORMATETC](http://msdn.microsoft.com/library/windows/desktop/ms682177) structure specifying the format in which information is requested.  
  
 `phGlobal`  
 Points to a handle to global memory in which the data is to be returned. If no memory has been allocated, this parameter can be **NULL**.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 The specified format is one previously placed in the control object using the [DelayRenderData](../vs140/COleDataSource--DelayRenderData.md) member function for delayed rendering. The default implementation of this function simply returns **FALSE**.  
  
 If `phGlobal` is **NULL**, then a new `HGLOBAL` should be allocated and returned in `phGlobal`. Otherwise, the `HGLOBAL` specified by `phGlobal` should be filled with the data. The amount of data placed in the `HGLOBAL` must not exceed the current size of the memory block. Also, the block cannot be reallocated to a larger size.  
  
 Override this function to provide your data in the requested format and medium. Depending on your data, you may want to override one of the other versions of this function instead. If you want to handle multiple storage mediums, override `OnRenderData`. If your data is in a file, or is of variable size, override `OnRenderFileData`.  
  
 For more information, see the **FORMATETC** structure in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::OnRenderFileData](../vs140/COleControl--OnRenderFileData.md)   
 [COleControl::OnRenderData](../vs140/COleControl--OnRenderData.md)