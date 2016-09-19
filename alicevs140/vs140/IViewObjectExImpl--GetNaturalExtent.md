---
title: "IViewObjectExImpl::GetNaturalExtent"
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
ms.assetid: deef7553-378e-4edf-a4bf-de71f000756d
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IViewObjectExImpl::GetNaturalExtent
Provides sizing hints from the container for the object to use as the user resizes it.  
  
## Syntax  
  
```  
  
      STDMETHOD(GetNaturalExtent)(  
   DWORD dwAspect,  
   LONG /* lindex */,  
   DVTARGETDEVICE* /* ptd */,  
   HDC /* hicTargetDevice */,  
   DVEXTENTINFO* pExtentInfo,  
   LPSIZEL psizel   
);  
```  
  
## Remarks  
 If `dwAspect` is `DVASPECT_CONTENT` and *pExtentInfo->dwExtentMode* is **DVEXTENT_CONTENT**, sets *`psizel` to the control class's data member [CComControlBase::m_sizeNatural](../vs140/CComControlBase--m_sizeNatural.md). Otherwise, returns an error `HRESULT`.  
  
 See [IViewObjectEx::GetNaturalExtent](http://msdn.microsoft.com/library/windows/desktop/ms683718) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IViewObjectExImpl Class](../vs140/IViewObjectExImpl-Class.md)