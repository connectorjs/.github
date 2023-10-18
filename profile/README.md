<a href="https://connectorjs.com" _target="blank">
  <img src="/images/connectjs-logo.png"  width="400" alt="connectorjs.com" >

  <h1>CONNECTORJS.com</h1>
</a>

[![](https://img.shields.io/badge/%F0%9F%8C%90%20Powered_by-miajupiter.com-blueviolet?style=flat&labelColor=%23323232)](https://miajupiter.com) [![](https://img.shields.io/github/followers/miajupiter?label=MiaJupiter&logo=github)](https://github.com/miajupiter)


## About

ConnectorJS developed by [MiaJupiter](https://miajupiter.com)


## Our mottos

- Simplicity is a form of high intelligence.
- Think & work for all mankind.


## Ideas we support

- Knowledge belongs to all beings, even to humanity.
- Open source softwares

## Structure

```mermaid
flowchart TD
    ccJS(fas:fa-city<br>connectir.io)
    ccService(((fa:fa-gear<br>Client Connector<br>Service)))
    ccWebSocket[fas:fa-plug WebSocket Manager]
    ccRestApi[fas:fa-arrows-to-dot RestAPI]
    cc1[Client-1<br>fab:fa-windows Windows<br>Server or Desktop]
    cc2[Client-2<br>fab:fa-linux Linux/Ubuntu<br> Server or Desktop]
    cc3[Client-3<br>fab:fa-apple MacOS]
    cc4[Client-..n<br>fas:fa-desktop Other Clients &<br>Operating Systems]
    ccDbMsSQL[(fas:fa-database SQL Server)]
    ccDbMySQL[(fas:fa-database MySQL)]
    ccDbPgSQL[(fas:fa-database PostgreSQL)]
    ccFileExcel[(fas:fa-file-excel Excel)]
    ccFileExcel2[(fas:fa-file-excel Excel)]
    ccShell[(fas:fa-terminal<br>Shell Scripts<br>File System)]
    ccApp1{{fas:fa-gears ClientConnector fas:fa-plug<br>Service App}}
    ccApp2{{fas:fa-gears ClientConnector fas:fa-plug<br>Service App}}
    ccApp3{{fas:fa-gears ClientConnector fas:fa-plug<br>Service App}}
    ccApp4{{fas:fa-gears ClientConnector fas:fa-plug<br>Service App}}


    ccWebSocket <---> ccService
    ccRestApi <---> |https<br>get/post/put/delete| ccService
    cc1 -->ccApp1 --->|tls/wss connection| ccWebSocket
    cc2 -->ccApp2 --->|tls/wss connection| ccWebSocket
    cc3 -->ccApp3 --->|tls/wss connection| ccWebSocket
    cc4 -->ccApp4 --->|tls/wss connection| ccWebSocket
    ccService ---> ccJS

    ccDbMsSQL ---> cc1
    ccFileExcel ---> cc1

    ccDbPgSQL ---> cc2

    ccDbMySQL ---> cc3
    ccFileExcel2 ---> cc3
    ccShell ---> cc4

%% subgraph ui [CONNECTORJS SERVER]
%%     ccService
%%     ccWebSocket
%%     ccRestApi
%% end

classDef classCC fill:cornflowerblue,stroke:white,color:white,stroke-width:1px;
class cc1,cc2,cc3,cc4 classCC;

classDef classCCJS fill:green,stroke:white,color:white,stroke-width:3px;
class ccJS classCCJS;

classDef ccConnectorApp fill:slateblue,stroke:white,color:yellowgreen,stroke-width:1px;
class ccApp1,ccApp2,ccApp3,ccApp4 ccConnectorApp;

```
