---
title: "CHtmlEditCtrlBase::GetBookMark"
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
ms.assetid: 651c8052-9f90-449c-aa64-d207e60ef0eb
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::GetBookMark
Retrieves the name of a bookmark anchor.  
  
## Syntax  
  
```  
  
      HRESULT GetBookMark(  
   CString& strAnchor   
) const;  
```  
  
#### Parameters  
 *strAnchor*  
 The name of a bookmark anchor.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 For more information, see [IDM_BOOKMARK Command ID](https://msdn.microsoft.com/en-us/library/aa769873.aspx).  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [CHtmlEditCtrlBase::SetBookMark](../vs140/CHtmlEditCtrlBase--SetBookMark.md)