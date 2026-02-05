---
layout: default
title: "Certificado en Windows"
---

## Sprint 4. Certificados Windows

*Para esta practica se utilizara el mismo windows server utilizado en el Sprint.3 VPN en windows*

Entramos dentro de la configuracion de adaptadores y deshabilitamos la IPv6 de el adaptador NAT

<img width="338" height="439" alt="image" src="https://github.com/user-attachments/assets/a164eb8b-dc81-4e70-8eb8-70afe5195729" />

<img width="501" height="272" alt="image" src="https://github.com/user-attachments/assets/51e6bf33-68e5-4661-8f71-43e7c282f7da" />

Agregamos en el Administrador de DNS la redirección a la WEB

<img width="624" height="447" alt="image" src="https://github.com/user-attachments/assets/4f94ed4e-fbf1-4c7f-b5b9-bcaff12343b0" />

Comprobamos que se resuelve con un nslookup

<img width="542" height="218" alt="image" src="https://github.com/user-attachments/assets/dce2247e-4a26-449e-8722-b5d256f15034" />

Agregamos el rol / caracteristica de Certificados para Active Directory

<img width="626" height="430" alt="image" src="https://github.com/user-attachments/assets/42f89a58-0b77-4c87-877a-20d465b6c8b0" />

<img width="619" height="447" alt="image" src="https://github.com/user-attachments/assets/67fc4d92-85e2-4a0f-9f6b-50df270830e7" />

Hacemos la configuracion que nos pide (lo dejamos todo por defecto)

<img width="619" height="448" alt="image" src="https://github.com/user-attachments/assets/7faf28ce-15ea-42e4-995c-f52fe5e7565d" />

Ahora abrimos certtmpl.msc en el Windows + R y duplicamos la plantilla de servidor Web, seguidamente le cambiamos el nombre en la pantalla general

<img width="625" height="480" alt="image" src="https://github.com/user-attachments/assets/6b36604a-201d-42cb-87f5-05c00334c596" />

Entramos en la Entidad de certificación -> Servidor -> Plantillas de Certificado -> Click derecho -> Nuevo -> Plantilla de Certificado que se va a emitir. De esta manera crearemos el certificado.

<img width="625" height="427" alt="image" src="https://github.com/user-attachments/assets/78f43aeb-cea2-400f-a5fd-d018df518355" />

Buscamos nuestro certificado y lo seleccionamos para añadirlo

<img width="612" height="313" alt="image" src="https://github.com/user-attachments/assets/36a7bf26-98b5-4674-9d1a-56c45a00948d" />

Creamos este archivo con este contenido para que funcione el certificado

<img width="625" height="568" alt="image" src="https://github.com/user-attachments/assets/712ee66f-7423-425b-a539-70979f39ead4" />

Creamos la solicitud del certificado

<img width="621" height="160" alt="image" src="https://github.com/user-attachments/assets/8615e2ec-eba6-4483-8c49-d8037a63b128" />

Ahora procesamos el certificado

<img width="622" height="581" alt="image" src="https://github.com/user-attachments/assets/021944b6-8847-4c7b-baf9-a32fb3fc3c6b" />

<img width="420" height="173" alt="image" src="https://github.com/user-attachments/assets/50f31e51-d394-4c17-a5b0-969408d1e3a2" />

Finalmente tramitamos el certificado

<img width="625" height="169" alt="image" src="https://github.com/user-attachments/assets/a1394327-3bb9-4e61-8cf4-4ccf00d1b696" />

Una vez tenemos el certificado tramitado abrimos el IIS

<img width="529" height="408" alt="image" src="https://github.com/user-attachments/assets/27ed8ba4-c398-4dbc-adbd-811098cf4689" />

Vamos a Sitios -> Default Web Site y en el panel de acciones vamos a enlaces para configurar el https con el certificado SSL generado, en mi caso se llama web.hugo.local

<img width="627" height="447" alt="image" src="https://github.com/user-attachments/assets/c98b7353-14e6-4e04-b697-f17453b39cb9" />

Entramos a la web y comprobamos que sale como seguro

<img width="625" height="504" alt="image" src="https://github.com/user-attachments/assets/0cfaefeb-25d1-4804-8ed6-cfa50915ffad" />

