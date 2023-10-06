# Actividad 0.2 - UDP and TCP: Comparison of Transport Protocols
## Diferencias entre udp y tcp
La principal diferencia entre el TCP (protocolo de control de transmisiones) y el UDP (protocolo de datagramas de usuario) es que el TCP es un protocolo basado en conexiones y el UDP es sin conexiones. Aunque el TCP es más fiable, transfiere los datos más despacio. El UDP es menos fiable pero funciona más rápido.

## ¿Qué aplicaciones usan tcp?
http, smtp, pop, imap, ssh.

## ¿Qué aplicaciones usan udp?
TFTP, DNS, RPC, NFS.

## ¿Qué capa almacena el puerto?
La capa de transporte.

## ¿Qué capa almacena la dirección IP?
La capa de Internet.

## ¿Qué es three-way handshake?
Cuando un host envía un mensaje a otro host, este puede ser particionado en un número de segmentos y reensamblado en el host destino por TCP. IP solo se encarga de rutearlos.
