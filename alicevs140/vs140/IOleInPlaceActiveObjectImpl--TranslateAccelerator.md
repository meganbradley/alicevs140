---
title: "IOleInPlaceActiveObjectImpl::TranslateAccelerator"
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
ms.assetid: d33e1059-769f-411f-bd5c-53bc077d14f8
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleInPlaceActiveObjectImpl::TranslateAccelerator
Processes menu accelerator-key messages from the container.  
  
## Syntax  
  
```  
  
      HRESULT TranslateAccelerator(  
   LPMSG lpmsg   
);  
```  
  
## Return Value  
 This method supports the following return values:  
  
 `S_OK` if the message was translated successfully.  
  
 **S_FALSE** if the message was not translated.  
  
## Remarks  
 See [IOleInPlaceActiveObject::TranslateAccelerator](http://msdn.microsoft.com/library/windows/desktop/ms693360) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleInPlaceActiveObjectImpl Class](../vs140/IOleInPlaceActiveObjectImpl-Class.md)