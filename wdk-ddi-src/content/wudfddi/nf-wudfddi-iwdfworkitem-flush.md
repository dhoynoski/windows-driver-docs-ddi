---
UID: NF:wudfddi.IWDFWorkItem.Flush
title: IWDFWorkItem::Flush (wudfddi.h)
description: The Flush method returns after this interface's work item has been serviced.
old-location: wdf\iwdfworkitem_flush.htm
tech.root: wdf
ms.assetid: AB79C2AE-0696-4EEC-9FC0-8A458CF19B82
ms.date: 02/26/2018
ms.keywords: Flush, Flush method, Flush method,IWDFWorkItem interface, IWDFWorkItem interface,Flush method, IWDFWorkItem.Flush, IWDFWorkItem::Flush, umdf.iwdfworkitem_flush, wdf.iwdfworkitem_flush, wudfddi/IWDFWorkItem::Flush
ms.topic: method
f1_keywords:
 - "wudfddi/IWDFWorkItem.Flush"
req.header: wudfddi.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 1.11
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: Unavailable in UMDF 2.0 and later.
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: WUDFx.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- WUDFx.dll
api_name:
- IWDFWorkItem.Flush
product:
- Windows
targetos: Windows
req.typenames: 
---

# IWDFWorkItem::Flush


## -description


<p class="CCE_Message">[<b>Warning:</b> UMDF 2 is the latest version of UMDF and supersedes UMDF 1.  All new UMDF drivers should be written using UMDF 2.  No new features are being added to UMDF 1 and there is limited support for UMDF 1 on newer versions of Windows 10.  Universal Windows drivers must use UMDF 2.  For more info, see <a href="https://docs.microsoft.com/windows-hardware/drivers/wdf/getting-started-with-umdf-version-2">Getting Started with UMDF</a>.]

The <b>Flush</b> method returns after this interface's work item has been serviced.


## -parameters






## -remarks



If a driver calls the <b>Flush</b> method, the method does not return until a worker thread has removed the specified work item from the work-item queue and called the driver's <a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/wudfworkitem/nc-wudfworkitem-wudf_workitem_function">OnWorkItem</a> callback function, and the <i>OnWorkItem</i> callback function has subsequently returned after processing the work item.

For more information, see <a href="https://docs.microsoft.com/windows-hardware/drivers/wdf/using-workitems">Using Work Items</a>.




## -see-also




<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/wudfddi/nn-wudfddi-iwdfworkitem">IWDFWorkItem</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/wudfworkitem/nc-wudfworkitem-wudf_workitem_function">OnWorkItem</a>
 

 

