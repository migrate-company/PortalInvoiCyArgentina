# Autenticación API Rest

## Generando el JWT

Pensando en la seguridad de los datos de nuestros clientes, al actualizar la versión del sistema, el usuario deberá realizar el proceso de generación de Token para su integración vía Rest API. Antes de iniciar el desarrollo de la autenticación con InvoiCy en la integración a través de la API, la mejor alternativa para entender el proceso de autenticación es generar el token en el patrón JWT - JSON Web Token manualmente.

Para hacer esto, acceda al portal JWT (https://jwt.io/) y configure el panel Decoded ajustando los grupos Payload y Verify Signature.

<figure markdown="span" style="max-width: 600px; margin: 0 auto; text-align: center;">
  ![Image title](../img/Artigos/Autenticacion_API_Rest_decoded_AR.png){ loading=lazy style="max-width: 100%; height: auto;" }
  <figcaption>Decodificación de un JWT</figcaption>
</figure>

## Entendiendo al grupo Payload:

El host varía según el entorno, siendo de pruebas https://apparpruebas.migrate.info/ y de producción https://appar.migrate.info/.
“Iat”: campo numérico que debe contener la fecha / hora actual en zona cero y en formato de marca de tiempo;
“Exp”: campo numérico que debe contener la fecha / hora actual + 120 segundos en zona cero y en formato de marca de tiempo;
“Sub”: es una cadena con el código de establecimiento RUC + de la empresa emisora. Cuando el RUC no tiene un total de 8 dígitos, es necesario llenarlo al inicio con el valor 0 hasta cerrar el valor total. Lo mismo se repite para el código de establecimiento, siendo necesario completar el total de 10 dígitos.
“PartnerKey”: es una cadena con la clave de socio proporcionada por InvoiCy, que se puede encontrar a través de la pantalla Panel de control> Socios.
La generación de fecha / hora en la timestamp se puede realizar a través del portal Epoch Converter, como se muestra en la imagen de ejemplo a continuación:

## Entendiendo al grupo Verify Signature:

<figure markdown="span" style="max-width: 600px; margin: 0 auto; text-align: center;">
  ![Image title](../img/Artigos/Autenticacion_API_Rest_epoch_ar.png){ loading=lazy style="max-width: 100%; height: auto;" }
  <figcaption>Conversión de un timestamp Epoch</figcaption>
</figure>

En el campo donde se permite la edición, informe la clave de acceso de la empresa. La clave de acceso es la clave privada proporcionada por InvoiCy para cada empresa registrada, disponible a través de la pantalla de datos de la sucursal.

Al completar esta información, se generará el JWT en el panel Encoded para ser enviado a Invoicy en la opción Generate Token en la herramienta Postman, usando el proyecto de ejemplo en el botón abajo:

<div class="postman-run-button"
data-postman-action="collection/fork"
data-postman-visibility="public"
data-postman-var-1="11545214-a3b7f5b0-a051-4f2c-ba7a-17979a7a6e9f"
data-postman-collection-url="entityId=11545214-a3b7f5b0-a051-4f2c-ba7a-17979a7a6e9f&entityType=collection&workspaceId=8991473f-9646-4aa0-8a89-3b8ce13d45ba"></div>
<script type="text/javascript">
  (function (p,o,s,t,m,a,n) {
    !p[s] && (p[s] = function () { (p[t] || (p[t] = [])).push(arguments); });
    !o.getElementById(s+t) && o.getElementsByTagName("head")[0].appendChild((
      (n = o.createElement("script")),
      (n.id = s+t), (n.async = 1), (n.src = m), n
    ));
  }(window, document, "_pm", "PostmanRunObject", "https://run.pstmn.io/button.js"));
</script>