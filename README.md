# Transformación de Facturas Electrónicas con XSLT

Este proyecto consiste en la transformación de archivos XML de FacturaE (formato de factura electrónica española) a formato XHTML utilizando XSLT, permitiendo visualizar los datos más relevantes de una factura para clientes.

## Contenido

- [Descripción](#descripción)
- [Estructura del Proyecto](#estructura-del-proyecto)
- [Transformaciones XSLT](#transformaciones-xslt)
- [Ejemplos de Resultados](#ejemplos-de-resultados)
- [Cómo Utilizar](#cómo-utilizar)
- [Recursos](#recursos)

## Descripción

Este proyecto tiene como objetivo convertir archivos XML de FacturaE a formato XHTML utilizando XSLT. Se han creado dos transformaciones diferentes (estilos) para mostrar los datos más relevantes de una factura de forma amigable para el cliente.

## Estructura del Proyecto

- **xml/**: Contiene los archivos XML de ejemplo de FacturaE
- **xslt/**: Contiene las transformaciones XSLT
- **html/**: Contiene los archivos HTML resultantes de aplicar las transformaciones


## Transformaciones XSLT

### Transformación 1: Estilo Clásico

La primera transformación presenta un diseño clásico de factura con los siguientes elementos:

- Cabecera con información básica de la factura
- Sección de datos del emisor y receptor
- Tabla de productos/servicios detallada
- Resumen de importes y totales
- Pie de factura con información legal

**Características principales:**
- Diseño limpio y claro
- Uso de colores corporativos azules
- Separación clara de secciones
- Tipografía Arial para mejor legibilidad

[Ver código XSLT](xslt/facturae_transform1.xsl)

### Transformación 2: Estilo Moderno

La segunda transformación presenta un diseño más moderno y visual:

- Cabecera con fondo de color y mayor contraste
- Disposición de emisor y receptor en cajas laterales
- Tabla de productos con efectos visuales en hover
- Resumen de importes alineado a la derecha
- Sección destacada de información de pago

**Características principales:**
- Diseño moderno con bordes redondeados
- Uso de colores de acento y bordes laterales
- Tipografía Segoe UI para un aspecto más actual
- Efectos visuales sutiles en tablas y secciones

![Captura de la transformación 2](img/captura2.png)

[Ver código XSLT](xslt/facturae_transform2.xsl)

## Cómo Utilizar

Para aplicar las transformaciones a un archivo XML de FacturaE, puedes usar cualquiera de estos métodos:

### Usando un editor XSLT como Liquid Studio

1. Abre el archivo XML en Liquid Studio
2. Selecciona la transformación XSLT deseada
3. Ejecuta la transformación
4. Guarda el resultado como HTML

### Usando la línea de comandos (con Saxon)

```bash
java -jar saxon9he.jar -s:factura.xml -xsl:facturae_transform1.xsl -o:factura_estilo1.html
```

### Usando VSCode con la extensión DeltaXML

1. Instala la extensión DeltaXML en VSCode
2. Abre el archivo XML y el archivo XSLT
3. Haz clic derecho en el archivo XSLT y selecciona "Transform XML"
4. Selecciona el archivo XML como entrada
5. Guarda el resultado como HTML

## Recursos

- [Documentación de FacturaE](https://www.facturae.gob.es/formato/Paginas/formato-facturae.aspx)
- [Tutorial de XSLT](https://www.w3schools.com/xml/xsl_intro.asp)
- [Documentación de XSLT en MDN](https://developer.mozilla.org/en-US/docs/Web/XSLT)
