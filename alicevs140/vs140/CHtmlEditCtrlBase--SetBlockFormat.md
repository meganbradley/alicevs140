---
title: "CHtmlEditCtrlBase::SetBlockFormat"
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
ms.assetid: ea2b2c0b-5125-44cf-bc7f-e16c60564ad0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::SetBlockFormat
Sets the current block format tag.  
  
## Syntax  
  
```  
  
      HRESULT SetBlockFormat(  
   LPCTSTR szFormat   
) const;  
```  
  
#### Parameters  
 `szFormat`  
 The format tag.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This method sends the [IDM_BLOCKFMT_command ID](https://msdn.microsoft.com/en-us/library/aa769883.aspx) to the WebBrowser control.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [CHtmlEditCtrlBase::GetBlockFormat](../vs140/CHtmlEditCtrlBase--GetBlockFormat.md)