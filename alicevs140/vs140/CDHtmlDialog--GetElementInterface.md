---
title: "CDHtmlDialog::GetElementInterface"
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
ms.assetid: 0459f728-1585-46c4-9e90-b32fc9c05004
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDHtmlDialog::GetElementInterface
Retrieves the requested interface pointer from the HTML element identified by `szElementId`.  
  
## Syntax  
  
```  
  
      template <class Q>  
HRESULT GetElementInterface(  
   LPCTSTR szElementId,  
   Q** ppvObj   
);  
HRESULT GetElementInterface(  
   LPCTSTR szElementId,  
   REFIID riid,  
   void** ppvObj   
);  
```  
  
#### Parameters  
 `szElementId`  
 The ID of an HTML element.  
  
 `ppvObj`  
 Address of a pointer that will be filled with the requested interface pointer if the element is found and the query succeeds.  
  
 `riid`  
 The interface ID (IID) of the requested interface.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Example  
 [!CODE [NVC_MFCHtmlHttp#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCHtmlHttp#4)]  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [CDHtmlDialog Class](../vs140/CDHtmlDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDHtmlDialog::GetElement](../vs140/CDHtmlDialog--GetElement.md)   
 [CDHtmlDialog::GetControlDispatch](../vs140/CDHtmlDialog--GetControlDispatch.md)