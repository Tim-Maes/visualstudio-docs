---
description: "Determines the existence of a custom attribute for this field and, if it exists, returns the attribute information."
title: IDebugCustomAttributeQuery2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugCustomAttributeQuery2
helpviewer_keywords:
- IDebugCustomAttributeQuery interface
- IDebugCustomAttributeQuery2 interface
ms.assetid: 7cfa23e4-a05a-47a3-af6c-bd40c655014b
author: maiak
ms.author: maiak
manager: jmartens
ms.technology: vs-ide-debug
ms.workload:
- vssdk
---
# IDebugCustomAttributeQuery2

 [!INCLUDE [Visual Studio](~/includes/applies-to-version/vs-windows-only.md)]
Determines the existence of a custom attribute for this field and, if it exists, returns the attribute information.

## Syntax

```
IDebugCustomAttributeQuery2 : IDebugCustomAttributeQuery
```

## Notes for Implementers
 A symbol provider implements this interface on the same object that implements [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) in order to support custom attributes.

## Notes for Callers
 Use [QueryInterface](/cpp/atl/queryinterface) to obtain this interface from the [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) interface.

## Methods in Vtable Order
 The following table shows the methods of the **IDebugCustomAttributeQuery** interface.

|Method|Description|
|------------|-----------------|
|[IsCustomAttributeDefined](../../../extensibility/debugger/reference/idebugcustomattributequery2-iscustomattributedefined.md)|Determines whether a custom attribute exists by name.|
|[GetCustomAttributeByName](../../../extensibility/debugger/reference/idebugcustomattributequery2-getcustomattributebyname.md)|Gets the attribute information for the given custom attribute.|

 In addition to the **IDebugCustomAttributeQuery** methods, `IDebugCustomAttributeQuery2` implements the following method:

|Method|Description|
|------------|-----------------|
|[EnumCustomAttributes](../../../extensibility/debugger/reference/idebugcustomattributequery2-enumcustomattributes.md)|Gets an enumerator for all custom attributes attached to this field.|

## Remarks
 The [IEnumDebugCustomAttributes](../../../extensibility/debugger/reference/ienumdebugcustomattributes.md) method can return an enumerator for all custom attributes defined for this field.

## Requirements
 Header: sh.h

 Namespace: Microsoft.VisualStudio.Debugger.Interop

 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll

## See also
- [Symbol Provider Interfaces](../../../extensibility/debugger/reference/symbol-provider-interfaces.md)
- [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)
- [IEnumDebugCustomAttributes](../../../extensibility/debugger/reference/ienumdebugcustomattributes.md)
