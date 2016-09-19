---
title: "CMFCDisableMenuAnimation Class"
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
ms.assetid: c6eb07da-c382-43d6-8028-007f2320e50e
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCDisableMenuAnimation Class
Disables pop-up menu animation.  
  
## Syntax  
  
```  
class CMFCDisableMenuAnimation  
```  
  
## Members  
  
### Public Constructors  
  
|||  
|-|-|  
|Name|Description|  
|`CMFCDisableMenuAnimation::CMFCDisableMenuAnimation`|Constructs a `CMFCDisableMenuAnimation` object.|  
|`CMFCDisableMenuAnimation::~CMFCDisableMenuAnimation`|Destructor.|  
  
### Public Methods  
  
|||  
|-|-|  
|Name|Description|  
|[CMFCDisableMenuAnimation::Restore](#cmfcdisablemenuanimation__restore)|Restores the previous animation that the framework used to display a pop-up menu.|  
  
### Data Members  
  
|||  
|-|-|  
|Name|Description|  
|`CMFCDisableMenuAnimation::m_animType`|Stores the previous pop-up menu animation type.|  
  
### Remarks  
 Use this helper class to temporarily disable pop-up menu animation (for example, when you process mouse or keyboard commands).  
  
 A `CMFCDisableMenuAnimation` object disables pop-up menu animation during its lifetime. The constructor stores the current pop-up menu animation type in the `m_animType` field and sets the current animation type to `CMFCPopupMenu::NO_ANIMATION`. The destructor restores the previous animation type.  
  
 You can create a `CMFCDisableMenuAnimation` object on the stack to disable pop-up menu animation throughout a single function. If you want to disable popup menu animation between functions, create a `CMFCDisableMenuAnimation` object on the heap and then delete it when you want to restore pop-up menu animation.  
  
## Example  
 The following example shows how to use the stack to temporarily disable menu animation.  
  
 [!CODE [NVC_MFC_Misc#1](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_Misc#1)]  
  
## Inheritance Hierarchy  
 [CMFCDisableMenuAnimation](../vs140/CMFCDisableMenuAnimation-Class.md)  
  
## Requirements  
 **Header:** afxpopupmenu.h  
  
##  <a name="cmfcdisablemenuanimation__restore"></a>  CMFCDisableMenuAnimation::Restore  
 Restores the previous animation that the framework used to display a pop-up menu.  
  
```  
void Restore ();  
```  
  
### Remarks  
 This method is called by the `CMFCDisableMenuAnimation` destructor to restore the previous animation that the framework used to display a pop-up menu.  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [Classes](../vs140/MFC-Classes.md)   
 [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md)