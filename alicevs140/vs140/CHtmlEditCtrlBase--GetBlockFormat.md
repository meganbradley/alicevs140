---
title: "CHtmlEditCtrlBase::GetBlockFormat"
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
ms.assetid: 5a19c839-d8e5-439d-8770-052107388875
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::GetBlockFormat
Retrieves the current block format tag.  
  
## Syntax  
  
```  
  
      HRESULT GetBlockFormat(  
   CString& strFormat   
) const;  
```  
  
#### Parameters  
 *strFormat*  
 The current block format tag.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This method sends the [IDM_BLOCKFMT command ID](https://msdn.microsoft.com/en-us/library/aa769883.aspx) to the WebBrowser control.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [CHtmlEditCtrlBase::GetBlockFormatNames](../vs140/CHtmlEditCtrlBase--GetBlockFormatNames.md)