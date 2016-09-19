---
title: "FtmBase Class"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 275f3b71-2975-4f92-89e7-d351e96496df
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# FtmBase Class
Represents a free-threaded marshaler object.  
  
## Syntax  
  
```  
  
class FtmBase : public Microsoft::WRL::Implements<  
   Microsoft::WRL::RuntimeClassFlags< WinRtClassicComMix >,   
   Microsoft::WRL::CloakedIid< IMarshal > >;  
```  
  
## Remarks  
 For more information, see the "IMarshal" topic in the "COM Interfaces" subtopic of the "COM Reference" topic in the MSDN Library.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[FtmBase::FtmBase Constructor](../vs140/FtmBase--FtmBase-Constructor.md)|Initializes a new instance of the FtmBase class.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[FtmBase::CreateGlobalInterfaceTable Method](../vs140/FtmBase--CreateGlobalInterfaceTable-Method.md)|Creates a global interface table (GIT).|  
|[FtmBase::DisconnectObject Method](../vs140/FtmBase--DisconnectObject-Method.md)|Forcibly releases all external connections to an object. The object's server calls the object's implementation of this method prior to shutting down.|  
|[FtmBase::GetMarshalSizeMax Method](../vs140/FtmBase--GetMarshalSizeMax-Method.md)|Get the upper bound on the number of bytes needed to marshal the specified interface pointer on the specified object.|  
|[FtmBase::GetUnmarshalClass Method](../vs140/FtmBase--GetUnmarshalClass-Method.md)|Gets the CLSID that COM uses to locate the DLL containing the code for the corresponding proxy. COM loads this DLL to create an uninitialized instance of the proxy.|  
|[FtmBase::MarshalInterface Method](../vs140/FtmBase--MarshalInterface-Method.md)|Writes into a stream the data required to initialize a proxy object in some client process.|  
|[FtmBase::ReleaseMarshalData Method](../vs140/FtmBase--ReleaseMarshalData-Method.md)|Destroys a marshaled data packet.|  
|[FtmBase::UnmarshalInterface Method](../vs140/FtmBase--UnmarshalInterface-Method.md)|Initializes a newly created proxy and returns an interface pointer to that proxy.|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[FtmBase::marshaller_ Data Member](../vs140/FtmBase--marshaller_-Data-Member.md)|Holds a reference to the free threaded marshaler.|  
  
## Inheritance Hierarchy  
 `FtmBase`  
  
## Requirements  
 **Header:** ftm.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [WRL Namespace](../vs140/Microsoft--WRL-Namespace.md)