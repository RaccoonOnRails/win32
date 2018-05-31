---
Description: The GetTcpStatistics function fills a pointer to an MIB\_TCPSTATS structure with information on the TCP protocol statistics for the local computer.
ms.assetid: cb405d46-cf3e-4f3c-870a-935a0cc8118f
title: Retrieving Information Using GetTcpStatistics
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Retrieving Information Using GetTcpStatistics

The [**GetTcpStatistics**](/windows/win32/Iphlpapi/nf-iphlpapi-gettcpstatistics?branch=master) function fills a pointer to an [**MIB\_TCPSTATS**](rras.mib_tcpstats) structure with information on the TCP protocol statistics for the local computer.

**To use GetTcpStatistics**

1.  Declare some variables that are needed.

    Declare a **DWORD** variable `dwRetVal` that will be using for error checking function calls. Declare a pointer to an [**MIB\_TCPSTATS**](rras.mib_tcpstats) variable called *pTCPStats*, and allocate memory for the structure. Check that memory could be allocated.

    ```C++
    DWORD dwRetVal = 0;
    PMIB_TCPSTATS pTCPStats;

    pTCPStats = (MIB_TCPSTATS *) malloc(sizeof (MIB_TCPSTATS));
    if (pTCPStats == NULL) {
        printf("Error allocating memory\n");
    }
    ```

    

2.  Call the [**GetTcpStatistics**](/windows/win32/Iphlpapi/nf-iphlpapi-gettcpstatistics?branch=master) function with the *pTCPStats* parameter to retrieve TCP statistics for IPv4 on the local computer. Check for errors and return the error value in the **DWORD** variable `dwRetVal`. If an error occurs, the `dwRetVal` variable can be used for more extensive error checking and reporting.
    ```C++
        if ((dwRetVal = GetTcpStatistics(pTCPStats)) != NO_ERROR) {
            printf("GetTcpStatistics failed with error: %ld\n", dwRetVal);
        } 
    ```

    

3.  If the call was successful, access the data returned in the [**MIB\_TCPSTATS**](rras.mib_tcpstats) pointed to by the *pTCPStats* parameter.
    ```C++
    printf("\tNumber of active opens:  %u\n", pTCPStats->dwActiveOpens);
    printf("\tNumber of passive opens: %u\n", pTCPStats->dwPassiveOpens);
    printf("\tNumber of segments received: %u\n", pTCPStats->dwInSegs);
    printf("\tNumber of segments transmitted: %u\n", pTCPStats->dwOutSegs);
    printf("\tNumber of total connections: %u\n", pTCPStats->dwNumConns);
    ```

    

4.  Free the memory allocated for the [**MIB\_TCPSTATS**](rras.mib_tcpstats) structure pointed to by the *pTCPStats* parameter. This should be done once the application no longer needs the data returned by the *pTCPStats* parameter.
    ```C++
    if (pTCPStats)
        free(pTCPStats);
    ```

    

Next Step: [Retrieving Information Using GetIpStatistics](retrieving-information-using-getipstatistics.md)

Previous Step: [Retrieving Information Using GetIpStatistics](retrieving-information-using-getipstatistics.md)

## Complete Source Code

-   [Complete IP Helper Application Source Code](complete-ip-helper-application-source-code.md)

 

 


