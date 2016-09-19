---
title: "IViewObjectExImpl::GetColorSet"
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
ms.assetid: dab20987-37f3-40b5-b01f-bb21b14b3fca
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IViewObjectExImpl::GetColorSet
Returns the logical palette used by the control for drawing. The ATL implementation returns **E_NOTIMPL**.  
  
## Syntax  
  
```  
  
      STDMETHOD(GetColorSet)(  
   DWORD /* dwAspect */,  
   LONG /* lindex */,  
   void* /* pvAspect */,  
   DVTARGETDEVICE* /* ptd */,  
   HDC /* hicTargetDevice */,  
   LOGPALETTE** /* ppColorSet */  
);  
```  
  
## Remarks  
 See [IViewObject::GetColorSet](http://msdn.microsoft.com/library/windows/desktop/ms686553) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IViewObjectExImpl Class](../vs140/IViewObjectExImpl-Class.md)