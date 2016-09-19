---
title: "COleControl::OnResetState"
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
ms.assetid: 8f5df748-2deb-4419-820b-d7e8e02d73a3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::OnResetState
Called by the framework when the control's properties should be set to their default values.  
  
## Syntax  
  
```  
  
virtual void OnResetState( );  
```  
  
## Remarks  
 The default implementation calls [DoPropExchange](../vs140/COleControl--DoPropExchange.md), passing a `CPropExchange` object that causes properties to be set to their default values.  
  
 The control writer can insert initialization code for the OLE control in this overridable. This function is called when [IPersistStream::Load](http://msdn.microsoft.com/library/windows/desktop/ms680568) or [IPersistStorage::Load](http://msdn.microsoft.com/library/windows/desktop/ms680557) fails, or [IPersistStreamInit::InitNew](http://msdn.microsoft.com/library/windows/desktop/ms690234) or [IPersistStorage::InitNew](http://msdn.microsoft.com/library/windows/desktop/ms687194) is called, without first calling either **IPersistStream::Load** or **IPersistStorage::Load**.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::OnSetClientSite](../vs140/COleControl--OnSetClientSite.md)