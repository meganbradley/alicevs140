---
title: "CRecordView::CRecordView"
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
ms.assetid: 405e9858-98e7-4bb8-a261-04085c20d442
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordView::CRecordView
When you create an object of a type derived from `CRecordView`, call either form of the constructor to initialize the view object and identify the dialog resource on which the view is based.  
  
## Syntax  
  
```  
  
      explicit CRecordView(   
   LPCTSTR lpszTemplateName    
);  
explicit CRecordView(  
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
>  Your derived class *must* supply its own constructor. In the constructor of your derived class, call the constructor `CRecordView::CRecordView` with the resource name or ID as an argument, as shown in the example below.  
  
 **CRecordView::OnInitialUpdate** calls `UpdateData`, which calls `DoDataExchange`. This initial call to `DoDataExchange` connects `CRecordView` controls (indirectly) to `CRecordset` field data members created by ClassWizard. These data members cannot be used until after you call the base class **CFormView::OnInitialUpdate** member function.  
  
> [!NOTE]
>  If you use ClassWizard, the wizard defines an `enum` value `CRecordView::IDD`, specifies it in the class declaration, and uses it in the member initialization list for the constructor.  
  
## Example  
 [!CODE [NVC_MFCDatabase#32](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDatabase#32)]  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordView Class](../vs140/CRecordView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::DoFieldExchange](../vs140/CRecordset--DoFieldExchange.md)   
 [CView::OnInitialUpdate](../vs140/CView--OnInitialUpdate.md)   
 [CWnd::UpdateData](../vs140/CWnd--UpdateData.md)