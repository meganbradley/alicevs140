---
title: "CMFCToolBarButton::CreateFromOleData"
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
ms.assetid: 7286b630-6c64-49ab-a91e-d5349ddb9af5
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::CreateFromOleData
Creates a `CMFCToolBarButton` object from the provided `COleDataObject` object.  
  
## Syntax  
  
```  
static CMFCToolBarButton* __stdcall CreateFromOleData(  
   COleDataObject* pDataObject  
);  
```  
  
#### Parameters  
 [in] `pDataObject`  
 The source OLE data object.  
  
## Return Value  
 The created `CMFCToolBarButton` object.  
  
## Remarks  
 This method is used by the framework to perform data transfer in various formats. For example, the `CMFCOutlookBarPane::OnDragOver` method uses this method to perform drag-and-drop operations.  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [COleDataObject Class](../vs140/COleDataObject-Class.md)