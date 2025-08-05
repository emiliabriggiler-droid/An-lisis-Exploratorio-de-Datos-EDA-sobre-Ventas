# Analisis-Exploratorio-de-Datos-EDA-sobre-Ventas
Analizar la dinámica de ventas a lo largo del tiempo con foco en la combinación producto-semana, entendiendo patrones, estacionalidades y posibles inconsistencias en los datos.

Este proyecto se basa en un conjunto de datos transaccionales que registra ventas de productos alimenticios en el canal mayorista, realizadas a distintos puntos de venta (PDV) que operan como clientes del sistema. El propósito es aplicar técnicas de ciencia de datos para identificar patrones comerciales, optimizar decisiones estratégicas y generar valor a partir del análisis del comportamiento de compra.

### 📚 Índice

1. [🔍 Exploración inicial del conjunto de datos](#-1-exploración-inicial-del-conjunto-de-datos)    
    - [🔧 1.1 Revisión de datos faltantes](#11-revisión-de-datos-faltantes)  
    - [📊 1.2 Exploración de variables relevantes](#-12-exploración-de-variables-relevantes)  
        - [🧑‍💼 Clientes](#clientes)  
        - [📦 Productos](#productos)  
        - [🧾 Facturas](#facturas)  
        - [📅 Fechas](#fechas)  

2. [📈 Análisis y visualización de variables clave](#2-análisis-y-visualización-de-variables-clave)  
    - [🏆 2.1 Productos y clientes destacados](#21-productos-y-clientes-destacados)  
    - [💲 2.2 Evolución temporal de ventas y precios](#22-evolución-temporal-de-ventas-y-precios)  
    - [📆 2.3 Tendencias y estacionalidad](#23-tendencias-y-estacionalidad)  

3. [🕒 Análisis de granularidad temporal](#3-análisis-de-granularidad-temporal)  

4. [💡 Observaciones para la limpieza y curación de datos](#4-hallazgos-y-observaciones-relevantes)


Identificación del comprobante

**factu_codi, factu_nume, factu_letra**: código, número y letra de la factura.

**sucur**: sucursal que emitió la factura.

**fecha**: fecha de la venta.

**cliente**: identificador del cliente.

**usua, host_name_alta**: quién cargó la venta y desde qué servidor.

**fecha_alta, fecha_regis**: registro de cuándo se creó/cargó el documento.

Datos del cliente
**nombre, cuit:** nombre y CUIT del cliente.

**condi_venta:** condición de venta (por ejemplo, contado, crédito).

**tipo_negocio:** tipo de cliente o segmento de negocio.

Importes generales
**total**: total facturado por la venta (probablemente a nivel de comprobante).

**iva1:** importe de IVA en la venta.

**impor_gravado**: base imponible (monto antes de impuestos).

**iva_percep**: percepciones de IVA (otras cargas).

**precio_total**: Este parece ser el total de esta línea. Muy importante.

Detalle de producto y línea
**linea_nume**: número de línea dentro de la factura.

**produc**: código del producto.

**descrip**: descripción del producto.

**canti, uni_medi**: cantidad y unidad de medida.

**precio_uni**: precio unitario bruto (sin descuentos).

**boni_porcen, boni_impor**: porcentaje y monto del descuento.

**precio_uni_neto**: precio unitario neto de descuentos.

**precio_total**: cantidad * precio unitario neto.

Conversión y ventas
**conver, canti_venta**: variables relacionadas a ventas con conversión de unidades (por ejemplo, cajas a unidades).

**depo**: depósito u origen del stock.

**pedi_codi, pedi_nume, pedi_sucur**: datos del pedido relacionado.
