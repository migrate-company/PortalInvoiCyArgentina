# Integración vía API REST

InvoiCy ofrece a sus clientes la posibilidad de integrarse mediante una API REST, lo que permite realizar la emisión de Facturas Electrónicas (FE) de forma segura y eficiente, así como la consulta de documentos, monedas, unidades de medida y países.

Para facilitar el proceso, el servicio cuenta con dos entornos diferenciados: uno de Pruebas, destinado exclusivamente a la validación y simulación de procesos antes de la puesta en marcha, y otro de Producción, donde las operaciones son definitivas y los documentos generados poseen validez fiscal y legal.

En la documentación disponible se encuentran detallados los servicios y las direcciones URL correspondientes a cada entorno.

## :material-send: API Emisión
- **Finalidad:** Enviar Facturas Electrónicas (FE) para procesamiento por InvoiCy.
- **Endpoints:**
- Pruebas URL: https://apparpruebas.migrate.info/Api/Factura/Emitir
- Producción URL: https://appar.migrate.info/Api/Factura/Emitir

## :material-file-search: API Documentos
- **Finalidad:** Consultar Facturas Electrónicas emitidas.
- **Endpoints:**
- Pruebas URL: https://apparpruebas.migrate.info/Api/Factura/Documento
- Producción URL: https://appar.migrate.info/Api/Factura/Documento

## :material-counter: API Último Comprobante Autorizado
- **Finalidad:** Consultar el último comprobante autorizado.
- **Endpoints:**
- Pruebas URL: https://apparpruebas.migrate.info/Api/Factura/UltimoComprobanteAutorizado
- Producción URL: https://appar.migrate.info/Api/Factura/UltimoComprobanteAutorizado

## :material-currency-usd: API Monedas
- **Finalidad:** Consultar el listado de monedas disponibles.
- **Endpoints:**
- Pruebas URL: https://apparpruebas.migrate.info/Api/Data/Monedas
- Producción URL: https://appar.migrate.info/Api/Data/Monedas

## :material-scale-balance: API Unidades de Medida
- **Finalidad:** Consultar las unidades de medida disponibles.
- **Endpoints:** 
- Pruebas URL: https://apparpruebas.migrate.info/Api/Data/UnidadesMedida
- Producción URL: https://appar.migrate.info/Api/Data/UnidadesMedida

## :material-flag: API Países
- **Finalidad:** Consultar el listado de países.
- **Endpoints:**
- Pruebas URL: https://apparpruebas.migrate.info/Api/Data/Paises
- Producción URL: https://appar.migrate.info/Api/Data/Paises

## :material-currency-exchange: API Cotización Moneda
**Finalidad:** Consultar la cotización de una moneda.
**Endpoints:**
- Pruebas URL: https://apparpruebas.migrate.info/Api/Data/CotizacionMoneda
- Producción URL: https://appar.migrate.info/Api/Data/CotizacionMoneda

Antes de poder consumir los servicios de la API REST de InvoiCy, es necesario autenticarse. La autenticación garantiza que solo los usuarios autorizados puedan utilizar los servicios disponibles.

Para más detalles sobre cómo realizar la autenticación y obtener los tokens de acceso necesarios, consulte la documentación completa de [Autenticación API Rest](https://migrate-company.github.io/PortalInvoiCyArgentina/Integraci%C3%B3n/Autenticaci%C3%B3n%20API%20Rest.html){target="_blank"}.