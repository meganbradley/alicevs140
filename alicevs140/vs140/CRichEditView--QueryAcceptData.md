---
title: "CRichEditView::QueryAcceptData"
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
ms.assetid: bc2f524f-0b46-44fd-8e5c-1828cf8a4979
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditView::QueryAcceptData
Called by the framework to paste an object into the rich edit.  
  
## Syntax  
  
```  
  
      virtual HRESULT QueryAcceptData(  
   LPDATAOBJECT lpdataobj,  
   CLIPFORMAT* lpcfFormat,  
   DWORD dwReco,  
   BOOL bReally,  
   HGLOBAL hMetaFile   
);  
```  
  
#### Parameters  
 *lpdataobj*  
 Pointer to the [IDataObject](http://msdn.microsoft.com/library/windows/desktop/ms688421) to query.  
  
 *lpcfFormat*  
 Pointer to the acceptable data format.  
  
 `dwReco`  
 Not used.  
  
 *bReally*  
 Indicates if the paste operation should continue or not.  
  
 `hMetaFile`  
 A handle to the metafile used for drawing the item's icon.  
  
## Return Value  
 An `HRESULT` value reporting the success of the operation.  
  
## Remarks  
 Override this function to handle different organization of COM items in your derived document class. This is an advanced overridable.  
  
 For more information on `HRESULT` and `IDataObject`, see [Structure of COM Error Codes](http://msdn.microsoft.com/library/windows/desktop/ms690088) and [IDataObject](http://msdn.microsoft.com/library/windows/desktop/ms688421), respectively, in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFCDocView#160](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#160)]  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditView Class](../vs140/CRichEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)