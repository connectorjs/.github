<p align="center">
<a href="https://connectorjs.com" _target="blank">
  <img src="../images/connectjs-logo.png"  width="400" alt="connectorjs.com" >
</a>
  
</p>
<a href="https://connectorjs.com" _target="blank">
  <h1 align="center">CONNECTORJS.com</h1>
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
graph LR
cc(api.connectorjs.com/connector/:func/:param1/:param2);style cc fill:#1122dd,color:#eee;
conn(Connector Client);style conn fill:#1122dd,color:#eee;
mdb[(MongoDb)];style mdb fill:#548235,color:#eee;
mssql[(SQL Server)];style mssql fill:#548235,color:#eee;
mysql[(MySQL)];style mysql fill:#548235,color:#eee;
xls[Excel Files];style xls fill:#d4d235,color:#222;
fs[File System];style fs fill:#333333,color:#ddd;
cmd[shell/bash/cmd];style cmd fill:#333333,color:#ddd;
ra{{Rest API}};style ra fill:#4472c4,color:#eee;
socket{{Socket Server}};style socket fill:#4472c4,color:#eee;
internet(Internet);style internet fill:#dd72c4,color:#111;

mdb --- conn
mssql --- conn
mysql --- conn
xls --- conn
fs --- conn
cmd --- conn

conn --- internet
internet --> socket
socket --> ra
ra -->cc

subgraph UI [Local Server or Computer]
mdb
mssql
mysql
xls
fs
cmd
conn
end

subgraph dd [ConnectorJS Server]
socket
cc
ra
end

```
