---
UID: NF:netrequestqueue.NET_REQUEST_QUEUE_CONFIG_ADD_METHOD_HANDLER
title: NET_REQUEST_QUEUE_CONFIG_ADD_METHOD_HANDLER function (netrequestqueue.h)
description: Adds a caller-provided handler for a specific OID method request to a NET_REQUEST_QUEUE_CONFIG structure.
tech.root: netvista
ms.assetid: 6dba1c38-fcf3-49f3-a1ad-925ab6f545b5
ms.date: 02/09/2018
ms.topic: function
f1_keywords:
 - "netrequestqueue/NET_REQUEST_QUEUE_CONFIG_ADD_METHOD_HANDLER"
ms.keywords: NET_REQUEST_QUEUE_CONFIG_ADD_METHOD_HANDLER
req.header: netrequestqueue.h
req.include-header:
req.target-type: Universal
req.target-min-winverclnt:
req.target-min-winversvr:
req.kmdf-ver: 1.21
req.umdf-ver:
req.lib:
req.dll:
req.irql: PASSIVE_LEVEL
req.ddi-compliance:
req.unicode-ansi:
req.idl:
req.max-support:
req.namespace:
req.assembly:
req.type-library: 
req.alt-api:
req.alt-loc:
topic_type: 
- apiref
api_type: 
- HeaderDef
api_location:
- netrequestqueue.h
api_name: 
- NET_REQUEST_QUEUE_CONFIG_ADD_METHOD_HANDLER
targetos: Windows
product:
- Windows
---

# NET_REQUEST_QUEUE_CONFIG_ADD_METHOD_HANDLER function


## -description

> [!WARNING]
> Some information in this topic relates to prereleased product, which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.
>
> NetAdapterCx is preview only in Windows 10, version 1903.

Adds a caller-provided handler for a specific OID method request to a [NET_REQUEST_QUEUE_CONFIG](ns-netrequestqueue-_net_request_queue_config.md) structure.

## -parameters

### -param NetRequestQueueConfig
A pointer to a driver-allocated [NET_REQUEST_QUEUE_CONFIG](ns-netrequestqueue-_net_request_queue_config.md) structure to which the custom handler is being added.

### -param Oid
The object identifier of the requested operation. The value is an OID\_*XXX* code.

### -param EvtRequestMethod
A pointer to the client driver's implementation of a *[EVT_NET_REQUEST_METHOD](nc-netrequestqueue-evt_net_request_method.md)* event callback function.

### -param MinimumInputLength
A UINT specifying the minimum input length for the request.

### -param MinimumOutputLength
A UINT specifying the minimum output length for the request.

## -remarks
When the client driver has finished adding custom handlers, it registers them with NetAdapterCx by calling [NetRequestQueueCreate](nf-netrequestqueue-netrequestqueuecreate.md).

If the memory allocation for this method fails, the subsequent call to **NetRequestQueueCreate** returns a failure code.

This function has the same effect as the following call sequence:

   1. [NET_REQUEST_QUEUE_METHOD_HANDLER_INIT](nf-netrequestqueue-net_request_queue_method_handler_init.md)
   2. [NET_REQUEST_QUEUE_CONFIG_ADD_INITIALIZED_METHOD_HANDLER](nf-netrequestqueue-net_request_queue_config_add_initialized_method_handler.md)



## -see-also
