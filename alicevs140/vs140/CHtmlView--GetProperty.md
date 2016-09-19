---
title: "CHtmlView::GetProperty"
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
ms.assetid: 426270a3-116b-40aa-8652-6f85680460e1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::GetProperty
Call this member function to get the value of the property currently associated with the control.  
  
## Syntax  
  
```  
  
      BOOL GetProperty(  
   LPCTSTR lpszProperty,  
   CString& strValue   
);  
COleVariant GetProperty(  
   LPCTSTR lpszProperty   
);  
```  
  
#### Parameters  
 `lpszProperty`  
 A pointer to a string containing the property to retrieve.  
  
 `strValue`  
 A reference to a [CString](../vs140/CStringT-Class.md) object that receives the current value of the property.  
  
## Return Value  
 In the first version, nonzero if completed successfully; otherwise zero. In the second version, a [COleVariant](../vs140/COleVariant-Class.md) object.  
  
## Remarks  
 Applies to Internet Explorer and WebBrowser.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHtmlView::PutProperty](../vs140/CHtmlView--PutProperty.md)   
 [IWebBrowser2::GetProperty](https://msdn.microsoft.com/en-us/library/aa752120.aspx)