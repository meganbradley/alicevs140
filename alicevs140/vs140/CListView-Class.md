---
title: "CListView Class"
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
ms.assetid: 7626bdb2-a1b8-4eab-b631-6743710a8432
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListView Class
Simplifies use of the list control and of [CListCtrl](../vs140/CListCtrl-Class.md), the class that encapsulates list-control functionality, with MFC's document-view architecture.  
  
## Syntax  
  
```  
class CListView : public CCtrlView  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CListView::CListView](#clistview__clistview)|Constructs a `CListView` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CListView::GetListCtrl](#clistview__getlistctrl)|Returns the list control associated with the view.|  
  
### Protected Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CListView::RemoveImageList](#clistview__removeimagelist)|Removes the specified image list from the list view.|  
  
## Remarks  
 For more information on this architecture, see the overview for the [CView](../vs140/CView-Class.md) class and the cross-references cited there.  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CCmdTarget](../vs140/CCmdTarget-Class.md)  
  
 [CWnd](../vs140/CWnd-Class.md)  
  
 [CView](../vs140/CView-Class.md)  
  
 [CCtrlView](../vs140/CCtrlView-Class.md)  
  
 `CListView`  
  
## Requirements  
 **Header:** afxcview.h  
  
##  <a name="clistview__clistview"></a>  CListView::CListView  
 Constructs a `CListView` object.  
  
```  
CListView( );  
  
```  
  
##  <a name="clistview__getlistctrl"></a>  CListView::GetListCtrl  
 Call this member function to get a reference to the list control associated with the view.  
  
```  
CListCtrl& GetListCtrl( ) const;  
  
```  
  
### Return Value  
 A reference to the list control associated with the view.  
  
### Example  
 [!CODE [NVC_MFCListView#7](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCListView#7)]  
  
##  <a name="clistview__removeimagelist"></a>  CListView::RemoveImageList  
 Removes the specified image list from the list view.  
  
```  
void RemoveImageList(    int  nImageList );  
  
```  
  
### Parameters  
 `nImageList`  
 The zero-based index of the image to remove.  
  
## See Also  
 [MFC Sample ROWLIST](../vs140/Visual-C---Samples.md)   
 [Base Class](../vs140/CCtrlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CCtrlView](../vs140/CCtrlView-Class.md)