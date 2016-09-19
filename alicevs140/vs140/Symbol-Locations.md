---
title: "Symbol Locations"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7c8cd8fe-169e-4161-9cff-5e9015984add
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Symbol Locations
Most symbols have a defined location within the image file. A symbol's location is specified with a value from the [LocationType Enumeration](../vs140/LocationType.md) enumeration. The symbol may support additional properties depending on its location.  
  
 The following table shows the most commonly used location types and their additional properties.  
  
|Location type|Additional properties|  
|-------------------|---------------------------|  
|`LocIsNull`|none|  
|`LocIsStatic`|[IDiaSymbol::get_addressOffset](../vs140/IDiaSymbol--get_addressOffset.md)<br /><br /> [IDiaSymbol::get_addressSection](../vs140/IDiaSymbol--get_addressSection.md)<br /><br /> [IDiaSymbol::get_relativeVirtualAddress](../vs140/IDiaSymbol--get_relativeVirtualAddress.md) (if relative virtual addresses are enabled)<br /><br /> [IDiaSymbol::get_virtualAddress](../vs140/IDiaSymbol--get_virtualAddress.md) (if the image base has been set to nonzero)|  
|`LocIsTLS`|[IDiaSymbol::get_addressSection](../vs140/IDiaSymbol--get_addressSection.md)<br /><br /> [IDiaSymbol::get_addressOffset](../vs140/IDiaSymbol--get_addressOffset.md)|  
|`LocIsRegRel`|[IDiaSymbol::get_registerId](../vs140/IDiaSymbol--get_registerId.md)<br /><br /> [IDiaSymbol::get_offset](../vs140/IDiaSymbol--get_offset.md)|  
|`LocIsThisRel`|[IDiaSymbol::get_offset](../vs140/IDiaSymbol--get_offset.md)|  
|`LocIsEnregistered`|[IDiaSymbol::get_registerId](../vs140/IDiaSymbol--get_registerId.md)|  
|`LocIsBitField`|[IDiaSymbol::get_bitPosition](../vs140/IDiaSymbol--get_bitPosition.md)<br /><br /> [IDiaSymbol::get_length](../vs140/IDiaSymbol--get_length.md)<br /><br /> [IDiaSymbol::get_offset](../vs140/IDiaSymbol--get_offset.md)|  
|`LocIsSlot`|[IDiaSymbol::get_slot](../vs140/IDiaSymbol--get_slot.md)|  
|`LocIsIlRel`|[IDiaSymbol::get_offset](../vs140/IDiaSymbol--get_offset.md)|  
|`LocInMetaData`|[IDiaSymbol::get_token](../vs140/IDiaSymbol--get_token.md)|  
|`LocIsConstant`|[IDiaSymbol::get_value](../vs140/IDiaSymbol--get_value.md)|  
  
## See Also  
 [IDiaSymbol::get_addressOffset](../vs140/IDiaSymbol--get_addressOffset.md)   
 [IDiaSymbol::get_addressSection](../vs140/IDiaSymbol--get_addressSection.md)   
 [IDiaSymbol::get_bitPosition](../vs140/IDiaSymbol--get_bitPosition.md)   
 [IDiaSymbol::get_length](../vs140/IDiaSymbol--get_length.md)   
 [IDiaSymbol::get_locationType](../vs140/IDiaSymbol--get_locationType.md)   
 [IDiaSymbol::get_offset](../vs140/IDiaSymbol--get_offset.md)   
 [IDiaSymbol::get_registerId](../vs140/IDiaSymbol--get_registerId.md)   
 [IDiaSymbol::get_relativeVirtualAddress](../vs140/IDiaSymbol--get_relativeVirtualAddress.md)   
 [IDiaSymbol::get_slot](../vs140/IDiaSymbol--get_slot.md)   
 [IDiaSymbol::get_token](../vs140/IDiaSymbol--get_token.md)   
 [IDiaSymbol::get_value](../vs140/IDiaSymbol--get_value.md)   
 [IDiaSymbol::get_virtualAddress](../vs140/IDiaSymbol--get_virtualAddress.md)   
 [LocationType Enumeration](../vs140/LocationType.md)   
 [Symbols and Symbol Tags](../vs140/Symbols-and-Symbol-Tags.md)