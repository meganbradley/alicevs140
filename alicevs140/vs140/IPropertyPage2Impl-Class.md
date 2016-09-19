---
title: "IPropertyPage2Impl Class"
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
ms.assetid: e89fbe90-203a-47f0-a5de-23616697e1ce
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IPropertyPage2Impl Class
This class implements **IUnknown** and inherits the default implementation of [IPropertyPageImpl](../vs140/IPropertyPageImpl-Class.md).  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```  
  
template< class  T>  
   class IPropertyPage2Impl : public IPropertyPageImpl<  T>  
  
```  
  
#### Parameters  
 `T`  
 Your class, derived from `IPropertyPage2Impl`.  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[IPropertyPage2Impl::EditProperty](../vs140/IPropertyPage2Impl--EditProperty.md)|Specifies which property control will receive the focus when the property page is activated. The ATL implementation returns **E_NOTIMPL**.|  
  
## Remarks  
 The [IPropertyPage2](http://msdn.microsoft.com/library/windows/desktop/ms683996) interface extends [IPropertyPage](http://msdn.microsoft.com/library/windows/desktop/ms691246) by adding the `EditProperty` method. This method allows a client to select a specific property in a property page object.  
  
 Class `IPropertyPage2Impl` simply returns **E_NOTIMPL** for **IPropertyPage2::EditProperty**. However, it inherits the default implementation of [IPropertyPageImpl](../vs140/IPropertyPageImpl-Class.md) and implements **IUnknown** by sending information to the dump device in debug builds.  
  
 When you create a property page, your class is typically derived from `IPropertyPageImpl`. To provide the extra support of **IPropertyPage2**, modify your class definition and override the `EditProperty` method.  
  
 **Related Articles** [ATL Tutorial](../vs140/Active-Template-Library--ATL--Tutorial.md), [Creating an ATL Project](../vs140/Creating-an-ATL-Project.md)  
  
## Inheritance Hierarchy  
 `IPropertyPage`  
  
 [IPropertyPageImpl](../vs140/IPropertyPageImpl-Class.md)  
  
 `IPropertyPage2Impl`  
  
## Requirements  
 **Header:** atlctl.h  
  
##  <a name="ipropertypage2impl__editproperty"></a>  IPropertyPage2Impl::EditProperty  
 Specifies which property control will receive the focus when the property page is activated.  
  
```  
  
HRESULT EditProperty(  
      DISPID  dispID  
   );  
  
```  
  
### Return Value  
 Returns **E_NOTIMPL**.  
  
### Remarks  
 See [IPropertyPage2::EditProperty](http://msdn.microsoft.com/library/windows/desktop/ms690353) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## See Also  
 [IPerPropertyBrowsingImpl Class](../vs140/IPerPropertyBrowsingImpl-Class.md)   
 [ISpecifyPropertyPagesImpl Class](../vs140/ISpecifyPropertyPagesImpl-Class.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)