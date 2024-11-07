# NetMedic
NetMedic es un script avanzado en .exe para diagnosticar y solucionar problemas de red en Windows. Incluye opciones como limpiar caché DNS, restablecer TCP/IP, renovar IP, desactivar firewall y reiniciar adaptadores. Fácil de usar y ejecutable como administrador para soluciones rápidas y efectivas.

**NetMedic**

---
# NetMedic
### Herramienta avanzada de diagnóstico y solución de problemas de red

![NetMedic](https://dummyimage.com/600x200/000/fff&text=NetMedic+by+Espinozan)

**NetMedic** es una utilidad de línea de comandos en formato `.exe` desarrollada para diagnosticar, solucionar y optimizar problemas comunes de conexión a red en sistemas Windows. Esta herramienta avanzada permite desde limpiar el caché DNS hasta resetear el adaptador de red y desactivar el firewall, brindando una solución integral y accesible para cualquier usuario o administrador de sistemas.

---

## Características

- Restablecimiento completo de la configuración de TCP/IP y Winsock.
- Limpieza de caché DNS para resolver problemas de conexión y dominios.
- Diagnóstico básico y completo de conexión a través de `ping` y `tracert`.
- Opciones de restablecimiento y desactivación temporal de firewall.
- Muestra la configuración de red actual (IP y Gateway) para revisión rápida.
- Menú interactivo que permite ejecutar funciones individuales o todas a la vez.
- **Compatibilidad**: Windows 8.1, Windows 10, Windows 11.

## Tabla de Contenidos
- [Instalación](#instalación)
- [Uso](#uso)
- [Opciones](#opciones)
- [Requisitos](#requisitos)
- [Funcionamiento Detallado](#funcionamiento-detallado)
- [Advertencias](#advertencias)

---

## Instalación

1. Descarga el archivo **NetMedic.exe** o clona este repositorio:

   ```bash
   git clone https://github.com/espinozan/NetMedic.git
   ```

2. Navega al directorio del proyecto:

   ```bash
   cd NetMedic
   ```

3. Asegúrate de ejecutar el script como administrador para que todas las funciones tengan los permisos necesarios.

---

## Uso

1. **Ejecutar como administrador**: Para usar **NetMedic** correctamente, haz clic derecho sobre el archivo `NetMedic.exe` y selecciona "Ejecutar como administrador". Esto es necesario para ejecutar comandos avanzados que requieren permisos elevados.

2. **Menú principal**: Una vez abierto, el menú te permitirá seleccionar las diferentes opciones de diagnóstico y reparación.

3. **Seleccionar opción**: Introduce el número correspondiente a la opción deseada y presiona `Enter`.

---

## Opciones

**NetMedic** ofrece un menú de opciones para permitir una solución personalizada y flexible. Aquí están las funcionalidades detalladas:

| Opción | Función                                                  | Descripción                                                                                   |
|--------|----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| 1      | Restablecer TCP/IP                                       | Reinicia la configuración de TCP/IP, útil para resolver problemas con la conexión a internet. |
| 2      | Limpiar caché de DNS                                     | Elimina el caché DNS, útil para resolver problemas de acceso a sitios web.                    |
| 3      | Renovar dirección IP                                     | Libera y renueva la dirección IP.                                                             |
| 4      | Restablecer catálogo de Winsock                          | Restablece Winsock para resolver problemas de conectividad y software.                        |
| 5      | Restablecer configuración de Proxy                       | Desactiva cualquier configuración de Proxy.                                                   |
| 6      | Diagnóstico de red                                       | Ejecuta un `ping` y un `tracert` para diagnosticar problemas de conexión.                     |
| 7      | Reiniciar adaptador de red                               | Deshabilita y vuelve a habilitar el adaptador de red principal.                               |
| 8      | Mostrar configuración de red                             | Muestra la configuración actual de IP y Gateway.                                             |
| 9      | Desactivar/Activar Firewall de Windows                   | Activa o desactiva temporalmente el firewall.                                                 |
| 10     | Ejecutar todas las opciones                              | Ejecuta todas las soluciones de red automáticamente.                                          |
| 11     | Salir                                                    | Cierra el script.                                                                             |

## Requisitos

- **Sistema Operativo**: Windows 8.1, Windows 10 o Windows 11
- **Permisos de Administrador**: Se requiere para ejecutar ciertos comandos de red y sistema.

---

## Funcionamiento Detallado

A continuación, una explicación técnica de cada función para ayudar a los usuarios avanzados a entender las acciones de NetMedic:

1. **Restablecimiento de TCP/IP**: Usa el comando `netsh int ip reset` para reiniciar la pila TCP/IP y resolver problemas de red subyacentes.
2. **Limpieza de Caché DNS**: `ipconfig /flushdns` limpia el caché DNS, lo que ayuda a refrescar las direcciones IP asociadas con nombres de dominio.
3. **Renovación de Dirección IP**: `ipconfig /release` y `ipconfig /renew` permiten liberar y obtener una nueva dirección IP.
4. **Restablecimiento de Winsock**: `netsh winsock reset` reinicia el catálogo de Winsock para resolver problemas de conectividad derivados de software mal configurado.
5. **Restablecimiento de Configuración de Proxy**: `netsh winhttp reset proxy` desactiva cualquier configuración de proxy activa.
6. **Diagnóstico de Red**: Comandos `ping` y `tracert` para probar conectividad y latencia.
7. **Reinicio del Adaptador de Red**: Desactiva y reactiva el adaptador principal mediante `netsh`, útil para solucionar problemas de conexión.
8. **Mostrar Configuración de Red**: Usa `ipconfig` para ver la dirección IP y puerta de enlace configurada.
9. **Desactivación/Activación de Firewall**: `netsh advfirewall` permite activar y desactivar el firewall para pruebas temporales de red.

---

## Advertencias

- **Modo Administrador**: **NetMedic** debe ejecutarse como administrador, ya que los comandos de red necesitan permisos elevados.
- **Firewall**: Desactivar el firewall puede dejar el sistema vulnerable a amenazas. Asegúrate de solo desactivarlo temporalmente y para fines de diagnóstico.
- **Cambios de Red**: Este script modifica configuraciones de red temporalmente. Es posible que necesites reiniciar el sistema en caso de cambios persistentes.

---

## Ejemplo de Uso

Una vez descargado y en el directorio, puedes ejecutar **NetMedic** directamente desde el símbolo del sistema:

```bash
NetMedic.exe
```

Tras ejecutar el script como administrador, verás el menú principal. Simplemente ingresa el número de la opción que deseas utilizar y sigue las instrucciones en pantalla.

---

## Contribuciones

¡Las contribuciones son bienvenidas! Si tienes ideas para mejorar NetMedic, realiza un fork de este repositorio y crea un pull request. Las mejoras en funcionalidad y eficiencia siempre son apreciadas.

## Licencia

Este proyecto está licenciado bajo la [Apache 2.0 License](LICENSE).

---

¡Gracias por usar **NetMedic**!
