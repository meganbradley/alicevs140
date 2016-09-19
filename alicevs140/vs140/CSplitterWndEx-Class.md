---
title: "CSplitterWndEx Class"
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
ms.assetid: 33e5eef3-05e1-4a07-a968-bf9207ce8598
caps.latest.revision: 21
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSplitterWndEx Class
Represents a customized splitter window.  
  
## Syntax  
  
```  
class CSplitterWndEx : public CSplitterWnd  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|`CSplitterWndEx::CSplitterWndEx`|Default constructor.|  
|`CSplitterWndEx::~CSplitterWndEx`|Destructor.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CSplitterWndEx::OnDrawSplitter](#csplitterwndex__ondrawsplitter)|Called by the framework to draw a splitter window. (Overrides [CSplitterWnd::OnDrawSplitter](../vs140/CSplitterWnd-Class.md#csplitterwnd__ondrawsplitter).)|  
  
## Remarks  
 Override the `OnDrawSplitter` method to customize the appearance of the graphical components of a splitter window.  
  
 The `CSplitterWndEx` class is used together with the [OnDrawSplitterBorder](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__ondrawsplitterborder), [OnDrawSplitterBox](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__ondrawsplitterbox), and [OnFillSplitterBackground](../vs140/CMFCVisualManager-Class.md#cmfcvisualmanager__onfillsplitterbackground) methods, which are implemented by a visual manager. To cause a visual manager to draw a splitter window in your application, replace declarations of the `CSplitterWnd` class with the `CSplitterWndEx` class. For frame window applications, the splitter window class is declared in the CMainFrame class that is located in mainfrm.h. For an example, see the `OutlookDemo` sample in the Samples directory.  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CCmdTarget](../vs140/CCmdTarget-Class.md)  
  
 [CWnd](../vs140/CWnd-Class.md)  
  
 [CSplitterWnd](../vs140/CSplitterWnd-Class.md)  
  
 [CSplitterWndEx](../vs140/CSplitterWndEx-Class.md)  
  
## Requirements  
 **Header:** afxsplitterwndex.h  
  
##  <a name="csplitterwndex__ondrawsplitter"></a>  CSplitterWndEx::OnDrawSplitter  
 Called by the framework to draw a splitter window.  
  
```  
virtual void OnDrawSplitter(  
   CDC* pDC,  
   ESplitType nType,  
   const CRect& rect   
);  
```  
  
### Parameters  
 [in] `pDC`  
 Pointer to the device context. If this parameter is `NULL`, the framework redraws the active window.  
  
 [in] `nType`  
 One of the `CSplitterWnd::ESplitType` enumeration values that specifies the splitter window element to draw. Valid values are `splitBox`, `splitBar`, `splitIntersection`, and `splitBorder`.  
  
 [in] `rect`  
 A bounding rectangle that specifies the dimensions and location to draw the specified splitter window element.  
  
### Remarks  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [Classes](../vs140/MFC-Classes.md)   
 [CSplitterWnd Class](../vs140/CSplitterWnd-Class.md)   
 [CMFCVisualManager](../vs140/CMFCVisualManager-Class.md)