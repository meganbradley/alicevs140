---
title: "CDaoRecordView::CDaoRecordView"
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
ms.assetid: 75c063dc-a4e3-45ff-9189-4716da83f424
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordView::CDaoRecordView
When you create an object of a type derived from `CDaoRecordView`, call either form of the constructor to initialize the view object and identify the dialog resource on which the view is based.  
  
## Syntax  
  
```  
  
      explicit CDaoRecordView(   
   LPCTSTR lpszTemplateName    
);  
explicit CDaoRecordView(   
   UINT nIDTemplate    
);  
```  
  
#### Parameters  
 `lpszTemplateName`  
 Contains a null-terminated string that is the name of a dialog template resource.  
  
 `nIDTemplate`  
 Contains the ID number of a dialog template resource.  
  
## Remarks  
 You can either identify the resource by name (pass a string as the argument to the constructor) or by its ID (pass an unsigned integer as the argument). Using a resource ID is recommended.  
  
> [!NOTE]
>  Your derived class must supply its own constructor. In the constructor of your derived class, call the constructor `CDaoRecordView::CDaoRecordView` with the resource name or ID as an argument.  
  
 **CDaoRecordView::OnInitialUpdate** calls `CWnd::UpdateData`, which calls `CWnd::DoDataExchange`. This initial call to `DoDataExchange` connects `CDaoRecordView` controls (indirectly) to `CDaoRecordset` field data members created by ClassWizard. These data members cannot be used until after you call the base class **CFormView::OnInitialUpdate** member function.  
  
> [!NOTE]
>  If you use ClassWizard, the wizard defines an `enum` value `CDaoRecordView::IDD` in the class declaration and uses it in the member initialization list for the constructor.  
  
 [!CODE [NVC_MFCDatabase#35](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDatabase#35)]  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordView Class](../vs140/CDaoRecordView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::UpdateData](../vs140/CWnd--UpdateData.md)   
 [CWnd::DoDataExchange](../vs140/CWnd--DoDataExchange.md)