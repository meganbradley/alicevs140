---
title: "IView Interface"
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
ms.assetid: 9321f299-486e-4551-bee9-d2c4a7b91548
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IView Interface
Implements several methods that [CWinFormsView](../Topic/CWinFormsView%20Class.md) uses to send view notifications to a managed control.  
  
## Syntax  
  
```  
interface class IView  
```  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[IView::OnActivateView](../vs140/IView--OnActivateView.md)|Called by MFC when a view is activated or deactivated.|  
|[IView::OnInitialUpdate](../vs140/IView--OnInitialUpdate.md)|Called by the framework after the view is first attached to the document, but before the view is initially displayed.|  
|[IView::OnUpdate](../vs140/IView--OnUpdate.md)|Called by MFC after the view's document has been modified; this function allows the view to update its display to reflect modifications.|  
  
## Remarks  
 `IView` implements several methods that `CWinFormsView` uses to forward common view notifications to a hosted managed control. These are [OnInitialUpdate](../vs140/IView--OnInitialUpdate.md), [OnUpdate](../vs140/IView--OnUpdate.md) and [OnActivateView](../vs140/IView--OnActivateView.md).  
  
 `IView` is similar to [CView](../vs140/CView-Class.md), but is used only with managed views and controls.  
  
 For more information on using Windows Forms, see [Using Windows Forms in MFC](../vs140/Using-a-Windows-Form-User-Control-in-MFC.md).  
  
## Requirements  
 Header: afxwinforms.h (defined in assembly atlmfc\lib\mfcmifc80.dll)  
  
## See Also  
 [CWinFormsView Class](../Topic/CWinFormsView%20Class.md)   
 [CView Class](../vs140/CView-Class.md)