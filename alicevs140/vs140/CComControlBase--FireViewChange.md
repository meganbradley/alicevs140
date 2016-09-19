---
title: "CComControlBase::FireViewChange"
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
ms.assetid: a384d6b0-4df2-4766-9950-c8e13e33446b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::FireViewChange
Call this method to tell the container to redraw the control, or notify the registered advise sinks that the control's view has changed.  
  
## Syntax  
  
```  
  
HRESULT FireViewChange( );  
  
```  
  
## Return Value  
 One of the standard HRESULT values.  
  
## Remarks  
 If the control is active (the control class data member [CComControlBase::m_bInPlaceActive](../vs140/CComControlBase--m_bInPlaceActive.md) is **TRUE**), notifies the container that you want to redraw the entire control. If the control is inactive, notifies the control's registered advise sinks (through the control class data member [CComControlBase::m_spAdviseSink](../vs140/CComControlBase--m_spAdviseSink.md)) that the control's view has changed.  
  
## Example  
 [!CODE [NVC_ATL_COM#21](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#21)]  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)