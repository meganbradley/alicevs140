---
title: "CComControlBase::DoVerbProperties"
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
ms.assetid: ab0641ad-c55a-4f62-a3c8-fa0512dc7972
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::DoVerbProperties
Displays the control's property pages.  
  
## Syntax  
  
```  
  
      HRESULT DoVerbProperties(  
   LPCRECT /* prcPosRect */,  
   HWND hwndParent   
);  
```  
  
#### Parameters  
 `prcPosRec`  
 Reserved.  
  
 *hwndParent*  
 Handle of the window containing the control.  
  
## Return Value  
 One of the standard HRESULT values.  
  
## Example  
 [!CODE [NVC_ATL_COM#19](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#19)]  
  
 [!CODE [NVC_ATL_COM#20](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#20)]  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)   
 [IOleObjectImpl::DoVerbPrimary](../vs140/IOleObjectImpl--DoVerbPrimary.md)