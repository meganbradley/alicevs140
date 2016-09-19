---
title: "IDataObjectImpl::EnumFormatEtc"
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
ms.assetid: 410bfc9d-6e07-4ef6-8fea-3165924b40e6
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDataObjectImpl::EnumFormatEtc
Creates an enumerator to iterate through the **FORMATETC** structures supported by the data object.  
  
## Syntax  
  
```  
  
      HRESULT EnumFormatEtc(  
   DWORD dwDirection,  
   IEnumFORMATETC** ppenumFormatEtc   
);  
```  
  
## Remarks  
 See [IDataObject::EnumFormatEtc](http://msdn.microsoft.com/library/windows/desktop/ms683979) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 Returns **E_NOTIMPL**.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IDataObjectImpl Class](../vs140/IDataObjectImpl-Class.md)   
 [IEnumFORMATETC](http://msdn.microsoft.com/library/windows/desktop/ms682337)