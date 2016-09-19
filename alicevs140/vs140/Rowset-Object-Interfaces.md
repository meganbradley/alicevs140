---
title: "Rowset Object Interfaces"
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
ms.assetid: 0d7a5d48-2fe4-434f-a84b-157c1fdc3494
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Rowset Object Interfaces
The following table shows the mandatory and optional interfaces defined by OLE DB for a rowset object.  
  
|Interface|Required?|Implemented by OLE DB templates?|  
|---------------|---------------|--------------------------------------|  
|[IAccessor](https://msdn.microsoft.com/en-us/library/ms719672.aspx)|Mandatory|Yes|  
|[IColumnsInfo](https://msdn.microsoft.com/en-us/library/ms724541.aspx)|Mandatory|Yes|  
|[IConvertType](https://msdn.microsoft.com/en-us/library/ms715926.aspx)|Mandatory|Yes|  
|[IRowset](https://msdn.microsoft.com/en-us/library/ms720986.aspx)|Mandatory|Yes|  
|[IRowsetInfo](https://msdn.microsoft.com/en-us/library/ms724541.aspx)|Mandatory|Yes|  
|[IChapteredRowset](https://msdn.microsoft.com/en-us/library/ms718180.aspx)|Optional|No|  
|[IColumnsInfo2](https://msdn.microsoft.com/en-us/library/ms712953.aspx)|Optional|No|  
|[IColumnsRowset](https://msdn.microsoft.com/en-us/library/ms722657.aspx)|Optional|No|  
|[IConnectionPointContainer](http://msdn.microsoft.com/library/windows/desktop/ms683857)|Optional|Yes (through ATL)|  
|[IDBAsynchStatus](https://msdn.microsoft.com/en-us/library/ms709832.aspx)|Optional|No|  
|[IGetRow](https://msdn.microsoft.com/en-us/library/ms718047.aspx)|Optional|No|  
|[IRowsetChange](https://msdn.microsoft.com/en-us/library/ms715790.aspx)|Optional|Yes|  
|[IRowsetChapterMember](https://msdn.microsoft.com/en-us/library/ms725430.aspx)|Optional|No|  
|[IRowsetCurrentIndex](https://msdn.microsoft.com/en-us/library/ms709700.aspx)|Optional|No|  
|[IRowsetFind](https://msdn.microsoft.com/en-us/library/ms724221.aspx)|Optional|No|  
|[IRowsetIdentity](https://msdn.microsoft.com/en-us/library/ms715913.aspx)|Optional (but required for level 0 providers)|Yes|  
|[IRowsetIndex](https://msdn.microsoft.com/en-us/library/ms719604.aspx)|Optional|No|  
|[IRowsetLocate](https://msdn.microsoft.com/en-us/library/ms721190.aspx)|Optional|Yes|  
|[IRowsetRefresh](https://msdn.microsoft.com/en-us/library/ms714892.aspx)|Optional|No|  
|[IRowsetScroll](https://msdn.microsoft.com/en-us/library/ms712984.aspx)|Optional|No|  
|[IRowsetUpdate](https://msdn.microsoft.com/en-us/library/ms714401.aspx)|Optional|Yes|  
|[IRowsetView](https://msdn.microsoft.com/en-us/library/ms709755.aspx)|Optional|No|  
|[ISupportErrorInfo](https://msdn.microsoft.com/en-us/library/ms715816.aspx)|Optional|Yes|  
|[IRowsetBookmark](https://msdn.microsoft.com/en-us/library/ms714246.aspx)|Optional|No|  
  
 The wizard-generated rowset object implements `IAccessor`, `IRowset`, and `IRowsetInfo` through inheritance. The `IAccessorImpl` binds both output columns. The `IRowset` interface handles fetches rows and data. The `IRowsetInfo` interface handles the rowset properties.  
  
## See Also  
 [OLE DB Provider Template Architecture](../vs140/OLE-DB-Provider-Template-Architecture.md)