---
title: "CMouseManager::AddView"
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
ms.assetid: 81a5f35e-a1c5-4186-9343-1caadfeccd02
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMouseManager::AddView
Registers a [CView](../vs140/CView-Class.md) object with the [CMouseManager Class](../vs140/CMouseManager-Class.md) to support custom mouse behavior.  
  
## Syntax  
  
```  
BOOL AddView(  
   int iViewId,  
   UINT uiViewNameResId,  
   UINT uiIconId = 0  
);  
BOOL AddView(  
   int iId,  
   LPCTSTR lpszViewName,  
   UINT uiIconId = 0  
);  
```  
  
#### Parameters  
 [in] `iViewId`  
 A view ID.  
  
 [in] `uiViewNameResId`  
 A resource string ID that references the view name.  
  
 [in] `uiIconId`  
 A view icon ID.  
  
 [in] `iId`  
 A view ID.  
  
 [in] `lpszViewName`  
 A view name.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 In order to support custom mouse behavior, a view must be registered with the `CMouseManager` object. Any object derived from the `CView` class can be registered with the mouse manager. The string and icon associated with a view are displayed in the **Mouse** tab of the **Customize** dialog box.  
  
 It is the responsibility of the programmer to create and maintain view IDs such as `iViewId` and `iId`.  
  
 For more information about how to provide custom mouse behavior, see [Keyboard and Mouse Customization](../vs140/Keyboard-and-Mouse-Customization.md).  
  
## Example  
 The following example demonstrates how to retrieve a pointer to a `CMouseManager` object by using the `CWinAppEx::GetMouseManager` method and the `AddView` method in the `CMouseManager` class. This code snippet is part of the [State Collection sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_StateCollection#4](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_StateCollection#4)]  
  
## Requirements  
 **Header:** afxmousemanager.h  
  
## See Also  
 [CMouseManager Class](../vs140/CMouseManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [Keyboard and Mouse Customization](../vs140/Keyboard-and-Mouse-Customization.md)