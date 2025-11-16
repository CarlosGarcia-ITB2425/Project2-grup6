## Consulta de IP y configuración de red

`ipconfig`

Visualiza la configuración y dirección IP del adaptador Ethernet.

![IP(Windows)](/Projecte2-grup6/Imagenes/IP(Windows).png)
Consulta avanzada de red
powershell
ipconfig /all
Muestra todos los detalles avanzados del adaptador de red, como gateway y DNS.

text
![ipa(windows)](ipa-windows.jpg)
Creación de usuario bchecker en Windows
Sin comando (interfaz gráfica).
Añade usuario local y define su contraseña en Configuración de Windows.

text
![CreandoUserBcheckeryusuariocreado(Windows)](CreandoUserBcheckeryusuariocreado-Windows.jpg)
Instalación de Wireshark con Winget
powershell
winget install --id=WiresharkFoundation.Wireshark -e --source winget
Instala Wireshark fácilmente desde la terminal de Windows.

text
![InstallWitheshark(Windows)](InstallWitheshark-Windows.jpg)
Test de conectividad con ping
powershell
ping <IPDestino>
Verifica conexión y latencia hacia otros hosts desde Windows.

text
![Conectividad(Windows)](Conectividad-Windows.jpg)
Test de conectividad con varios hosts
powershell
ping <IPDestino>
Ejecuta pruebas hacia diferentes hosts y observa la respuesta.

text
![Conecividad(Windows)](Conecividad-Windows.jpg)  
