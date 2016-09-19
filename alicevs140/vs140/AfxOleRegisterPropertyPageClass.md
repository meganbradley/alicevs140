---
title: "AfxOleRegisterPropertyPageClass"
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
ms.topic: article
ms.assetid: 96a0aeea-4d76-42e7-a5f3-df1bb36cc4e8
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxOleRegisterPropertyPageClass
Registers the property page class with the Windows registration database.  
  
## Syntax  
  
```  
  
      BOOL AFXAPI AfxOleRegisterPropertyPageClass(  
   HINSTANCE hInstance,  
   REFCLSID clsid,  
   UINT idTypeName,  
   int nRegFlags   
);  
```  
  
#### Parameters  
 `hInstance`  
 The instance handle of the module associated with the property page class.  
  
 `clsid`  
 The unique class ID of the property page.  
  
 `idTypeName`  
 The resource ID of the string that contains a user-readable name for the property page.  
  
 `nRegFlags`  
 May contain the flag:  
  
-   `afxRegApartmentThreading` Sets the threading model in the registry to ThreadingModel = Apartment.  
  
> [!NOTE]
>  In MFC versions prior to MFC 4.2, the `int` `nRegFlags` parameter was not available. Note also that the `afxRegInsertable` flag is not a valid option for property pages and will cause an ASSERT in MFC if it is set  
  
## Return Value  
 Nonzero if the control class was registered; otherwise 0.  
  
## Remarks  
 This allows the property page to be used by containers that are OLE-control aware. `AfxOleRegisterPropertyPageClass` updates the registry with the property page name and its location on the system and also sets the threading model that the control supports in the registry. For more information, see [Technical Note 64](../vs140/TN064--Apartment-Model-Threading-in-ActiveX-Controls.md), "Apartment-Model Threading in OLE Controls," and [About Processes and Threads](http://msdn.microsoft.com/library/windows/desktop/ms681917) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [AfxOleRegisterControlClass](../vs140/AfxOleRegisterControlClass.md)   
 [AfxOleRegisterTypeLib](../vs140/AfxOleRegisterTypeLib.md)