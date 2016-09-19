---
title: "CFormView::CFormView"
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
ms.assetid: 90f54454-cd2b-401e-931e-3353e61a5c11
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFormView::CFormView
Constructs a `CFormView` object.  
  
## Syntax  
  
```  
  
      CFormView(  
   LPCTSTR lpszTemplateName   
);  
CFormView(  
   UINT nIDTemplate   
);  
```  
  
#### Parameters  
 `lpszTemplateName`  
 Contains a null-terminated string that is the name of a dialog-template resource.  
  
 `nIDTemplate`  
 Contains the ID number of a dialog-template resource.  
  
## Remarks  
 When you create an object of a type derived from `CFormView`, invoke one of the constructors to create the view object and identify the dialog resource on which the view is based. You can identify the resource either by name (pass a string as the argument to the constructor) or by its ID (pass an unsigned integer as the argument).  
  
 The form-view window and child controls are not created until `CWnd::Create` is called. `CWnd::Create` is called by the framework as part of the document and view creation process, which is driven by the document template.  
  
> [!NOTE]
>  Your derived class *must* supply its own constructor. In the constructor, invoke the constructor, `CFormView::CFormView`, with the resource name or ID as an argument as shown in the preceding class overview.  
  
## Example  
 [!CODE [NVC_MFCDocView#90](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#90)]  
  
 [!CODE [NVC_MFCDocView#91](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#91)]  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CFormView Class](../vs140/CFormView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::Create](../vs140/CWnd--Create.md)