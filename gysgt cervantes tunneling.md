# Tunnels
##### But a different lesson

| x | Host | Host | Host  |
| ------ |------ | ------ | ------  |
| Port(s) | 1111, 3333 | 22, 2222 | 23, 22  |
| x | IH --> | --> T1 | --> T2  |

IH ssh user@t1 -L 1111:T2:23 -NT

IH telnet 127.0.0.1

T2 ssh user@T1 -R 2222:127.0.0.1:22 -NT

IH ssh user@T1 -L 3333:127.0.0.1:



| Host | Host | Host  |
| ------ |------ | ------ |
| IH --> | --> T1 | --> T2  |
