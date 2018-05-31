---
title: Collection Control Codes
description: The Failover Cluster API defines the following external control codes for collections (there are no internal control codes defined for collections).
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: 85DD2E41-B5DA-41E8-ACD8-2BE283CCF67A
ms.prod: windows-server-dev
ms.technology: failover-clustering
ms.tgt_platform: multiple
keywords:
- collection control codes Failover Cluster
- control codes Failover Cluster ,collection
- collections Failover Cluster ,control codes
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
---

# Collection Control Codes

The [Failover Cluster API](the-server-cluster-api.md) defines the following [*external control codes*](e-gly.md#-wolf-external-control-code-gly) for collections (there are no [*internal control codes*](i-gly.md#-wolf-internal-control-code-gly) defined for collections).

Collection control codes use the **CLUS\_OBJECT\_COLLECTION** value of the [**CLUSTER\_CONTROL\_OBJECT**](/windows/previous-versions/ClusAPI/ne-clusapi-cluster_control_object?branch=master) enumeration to indicate that the control code applies to clusters. For more information about control codes, see [Control Code Architecture](control-code-architecture.md).

Collection control codes are enumerated by the [**CLUSCTL\_COLLECTION\_CODES**](/windows/previous-versions/msclus/ne-clusapi-clusctl_groupset_codes?branch=master) enumeration.

## In this section

<dl> <dt>

[CLUSCTL\_COLLECTION\_GET\_COMMON\_PROPERTIES](clusctl-collection-get-common-properties.md)
</dt> <dd>

Retrieves the read/write properties for a collection.

</dd> <dt>

[CLUSCTL\_COLLECTION\_GET\_GROUPS](clusctl-collection-get-groups.md)
</dt> <dd>

Retrieves a list of the groups in the collection.

</dd> <dt>

[CLUSCTL\_COLLECTION\_GET\_PROVIDER\_COLLECTIONS](clusctl-collection-get-provider-collections.md)
</dt> <dd>

Retrieves the collections in the collection that come from a provider.

</dd> <dt>

[CLUSCTL\_COLLECTION\_GET\_PROVIDER\_GROUPS](clusctl-collection-get-provider-groups.md)
</dt> <dd>

Retrieves the groups in the collection that come from a provider.

</dd> <dt>

[CLUSCTL\_COLLECTION\_GET\_RO\_COMMON\_PROPERTIES](clusctl-collection-get-ro-common-properties.md)
</dt> <dd>

Retrieves the read-only private properties for a collection.

</dd> <dt>

[CLUSCTL\_COLLECTION\_SET\_COMMON\_PROPERTIES](clusctl-collection-set-common-properties.md)
</dt> <dd>

Updates the read/write [common properties](common-properties.md) for a collection.

</dd> </dl>

 

 



