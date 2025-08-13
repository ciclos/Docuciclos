# Configurar un servidor OVPN en RuoterOS de Mikrotik

<details>

<summary> Conocimientos previos</summary>

* ![DDNS](DDNS.md)

</details>

## Crear los certificados

![crear CA](1-crearCA.png)

![alt text](2-crearCA.png)

Firmamos usando un [DDNS](DDNS.md) como FreeDNS

![alt text](3-firmarCA.png)


Creamos el servidor

![alt text](4-crearServer.png)

![alt text](5-crearServer.png)

Firmamos el certificado del servidor con el CA.

![alt text](7-firmarServer.png)

Una vez firmado el servidor, aparece el checkbox para poder marcar el servidor como confiable.

![alt text](7-firmarServer.png)

Creamos el certificado del cliente, con las siguientes especificaciones y después los firmamos con el CA, igual que el servidor.

![alt text](8-crearCliente.png)

## Exportamos los certificados

Exportamos el certificado del cliente y del CA. 

![alt text](10-exportarCliente-1.png)

![alt text](10-exportarCliente-2.png)

> [!NOTE]
> Al exportar el del cliente le pondemos una clave, que se usará después al realizar la conexión desde el cliente, para poder usar este certificado.

El CA lo exportamos sin llave de paso.

![alt text](9-exportarCA.png)