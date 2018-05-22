---
title: Invoking RSVP
description: How to invoke RSVP.
ms.assetid: '2bff34c7-2db9-4845-9db5-906c3ef3fa7f'
keywords: ["Quality of Service QOS , tasks, invoking RSVP"]
---

# Invoking RSVP

There are two ways to invoke RSVP:

-   Using defaults, through the RSVP SP
-   Overriding defaults, by using the [**RSVP\_RESERVE\_INFO**](rsvp-reserve-info.md) object

RSVP signaling is invoked automatically when an application invokes the RSVP SP to provide QOS reservations on its behalf. The RSVP SP provides QOS reservations on behalf of an application when the service type in either the **SendingFlowspec** or **ReceivingFlowspec** members of the [**QOS**](qos.md) structure is set to a service type other than [SERVICETYPE\_BESTEFFORT](best-effort.md) or [SERVICETYPE\_NOTRAFFIC](servicetype-notraffic.md). Note that there are a number of individual APIs that can invoke the RSVP SP. For more information, see [Invoking the RSVP SP](invoking-the-rsvp-sp.md).

Another mechanism that an application developer can use to invoke RSVP, and to gain access to advanced RSVP features available in the [**QOS**](qos.md) structure, is through the [ProviderSpecific](the-providerspecific-buffer.md) buffer in the **QOS** structure.

The ProviderSpecific buffer can be used in conjunction with the [**RSVP\_RESERVE\_INFO**](rsvp-reserve-info.md) object. When specific RSVP-based reservation information is specified in the **RSVP\_RESERVE\_INFO** object, RSVP SP-supplied default information is superseded by the information, enabling application developers to fine-tune the way RSVP handles reservation requests (and responses). For more information on using the **RSVP\_RESERVE\_INFO** object, see [Using the RSVP\_RESERVE\_INFO Object](using-the-rsvp-reserve-info-object.md). For more information about the [**FLOWSPEC**](flowspec.md) structure, including which of its members can be defaulted, see **FLOWSPEC**.

 

 



