---
title: "IPropertyProxyEESide::GetManagedViewerCreationData"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c4eb4d60-8816-4d52-bc8d-dffd4f066499
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IPropertyProxyEESide::GetManagedViewerCreationData
Retrieves information about the viewer for this property type in order to instantiate that viewer.  
  
## Syntax  
  
```cpp#  
HRESULT GetManagedViewerCreationData(  
   BSTR*                  assemName,  
   IEEDataStorage**       assemBytes,  
   IEEDataStorage**       assemPdb,  
   BSTR*                  className,  
   ASSEMBLYLOCRESOLUTION* alr,  
   BOOL*                  replacementOk  
);  
```  
  
```c#  
int GetManagedViewerCreationData(  
   out string                     assemName,  
   out IEEDataStorage             assemBytes,  
   out IEEDataStorage             assemPdb,  
   out string                     className,  
   out enum_ASSEMBLYLOCRESOLUTION alr,  
   out int                        replacementOk  
);  
```  
  
#### Parameters  
 `assemName`  
 [out] Returns the name of the assembly holding this object.  
  
 `assemBytes`  
 [out] Returns an [IEEDataStorage](../vs140/IEEDataStorage.md) object containing the assembly bytes of this object (this is a null value if no bytes are available).  
  
 `assemPdb`  
 [out] Returns an `IEEDataStorage` object containing the symbol store information for this object (this is a null value if no symbol store is available).  
  
 `className`  
 [out] Returns the class name containing this object.  
  
 `alr`  
 [out] Returns a value from the [ASSEMBLYLOCRESOLUTION](../vs140/ASSEMBLYLOCRESOLUTION.md) enumeration indicating the location of the assembly.  
  
 `replacementOk`  
 [out] Returns nonzero (`TRUE`) if this object's value can be changed; zero (`FALSE`) if the object is read-only.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 This method is used by type visualizers to instantiate a managed viewer.  
  
## See Also  
 [IPropertyProxyEESide](../vs140/IPropertyProxyEESide.md)   
 [ASSEMBLYLOCRESOLUTION](../vs140/ASSEMBLYLOCRESOLUTION.md)   
 [IEEDataStorage](../vs140/IEEDataStorage.md)