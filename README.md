# Comandos para configuracion del router

Comandos de forma descargables en comando.txt

## Modo Exec

### Entrar a modo Exec privelegiado: 

```
Router>enable
```

### Salir de modo Exec privelegiado: 

```
Router#disable
```

## Modo Config

### Entrar a modo de Configuracion de terminal: 

```
Router#configure terminal
```
o
```
Router#conf t
```

### Salir de modo de Configuracion de terminal: 

```
Router(config)#exit
```

## Configurar dispositivo

### Configurar nombre del dispositivo:

```
Router(config)#hostname ...
```

### Configurar contraseña de enable:

```
Router(config)#enable secret ...
```

### Configurar contraseña de entrada:

#### Para puerto de consola

```
Router(config)#line console 0
Router(config-line)#password ...
Router(config-line)#login
```

#### Para acesso remoto

```
Router(config)#line vty 0 15
Router(config-line)#password ...
Router(config-line)#login
```

### Configurar cifrado de contraseñas:

```
Router(config)#service password-encryption
```

### Configurar banner de entrada al dispositivo:

```
Router(config)#banner motd # ... #
```

### Mostrar configuración actual:

```
Router#show running-config
```

### Hacer configuración actual a configuracion de inicio:

```
Router#copy running-config startup-config
```

### Restaurar configuración de inicio:

```
Router#reload
```

### Eliminar configuración de inicio:

```
Router#erase startup-config
```

## Configuración de interfaces:

### Entrar a la interfaz:

```
Router(config)#interface {int} {num}
```
o

```
Router(config)#int {int} {num}
```

* int:
    - Fa: FastEthernet
    - Gi: GigabitEthernet
    - Se: Serial
    - Lo: Loopback
* num:
    - n/0: Se usa para FastEthernet/GigabitEthernet
        - n: Numero de puerto
    - 0/x/n : Se usa para Serial
        - x: Numero del slot donde se encuentra colocado
        - n: Numero de puerto
    - x/n : Se usa para Serial
        - x: Numero del slot donde se encuentra colocado
        - n: Numero de puerto

### Asignación de ip a interfaz:

```
Router(config)#ip address {ip} {mascara-de-subred}
```

### Activación de puerto:

```
Router(config)#no shutdown
```

## Verificación de conexion:

### Ping a otra maquina:

```
Router(config)#ping {ip}
```

### Trazar ruta a otra maquina:

```
Router(config)#traceroute {ip}
```

### Mostrar interfaces breve:

```
Router(config)#show ip route brief
```
