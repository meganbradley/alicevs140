---
title: "COleObjectFactory::COleObjectFactory"
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
ms.assetid: 25b0ad9f-16ac-4189-8288-58a8af635e8a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleObjectFactory::COleObjectFactory
Constructs a `COleObjectFactory` object, initializes it as an unregistered object factory, and adds it to the list of factories.  
  
## Syntax  
  
```  
  
      COleObjectFactory(  
   REFCLSID clsid,  
   CRuntimeClass* pRuntimeClass,  
   BOOL bMultiInstance,  
   LPCTSTR lpszProgID   
);  
COleObjectFactory(  
   REFCLSID clsid,  
   CRuntimeClass* pRuntimeClass,  
   BOOL bMultiInstance,  
   int nFlags,  
   LPCTSTR lpszProgID   
);  
```  
  
#### Parameters  
 `clsid`  
 Reference to the OLE class ID this object factory represents.  
  
 `pRuntimeClass`  
 Pointer to the run-time class of the C++ objects this factory can create.  
  
 `bMultiInstance`  
 Indicates whether a single instance of the application can support multiple instantiations. If **TRUE**, multiple instances of the application are launched for each request to create an object.  
  
 `nFlags`  
 Contains one or more of the following flags:  
  
-   **afxRegDefault** Sets the threading model to ThreadingModel=Apartment.  
  
-   **afxRegInsertable** Allows the control to appear in the **Insert Object** dialog box for OLE objects.  
  
-   `afxRegApartmentThreading` Sets the threading model in the registry to ThreadingModel=Apartment.  
  
-   **afxRegFreeThreading** Sets the threading model in the registry to ThreadingModel=Free.  
  
     You can combine the two flags `afxRegApartmentThreading` and `afxRegFreeThreading` to set ThreadingModel=Both. See [InprocServer32](http://msdn.microsoft.com/library/windows/desktop/ms682390) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for more information on threading model registration.  
  
 `lpszProgID`  
 Pointer to a string containing a verbal program identifier, such as "Microsoft Excel."  
  
## Remarks  
 To use the object, however, you must register it.  
  
 For more information, see [CLSID Key](http://msdn.microsoft.com/library/windows/desktop/ms691424) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleObjectFactory Class](../vs140/COleObjectFactory-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRuntimeClass Structure](../vs140/CRuntimeClass-Structure.md)