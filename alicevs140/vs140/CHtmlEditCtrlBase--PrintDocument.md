---
title: "CHtmlEditCtrlBase::PrintDocument"
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
ms.assetid: 6f0d5b54-7f0f-496a-8888-b2e817e5c0cf
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::PrintDocument
Prints the current document.  
  
## Syntax  
  
```  
  
      HRESULT PrintDocument( ) const;   
HRESULT PrintDocument(  
   LPCTSTR szPrintTemplate   
) const;  
HRESULT PrintDocument(  
   bool bShowPrintDialog   
) const;  
```  
  
#### Parameters  
 `szPrintTemplate`  
 Path to a print template; if none is specified, the default print template is used.  
  
 *bShowPrintDialog*  
 If true, shows the Print dialog.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This method sends the [IDM_PRINT command ID](https://msdn.microsoft.com/en-us/library/aa769937.aspx) to the WebBrowser control.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [CHtmlEditCtrlBase::PrintPreview](../vs140/CHtmlEditCtrlBase--PrintPreview.md)