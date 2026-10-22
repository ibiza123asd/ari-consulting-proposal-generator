---
name: ari-consulting-proposal-generator
description: Crea propuestas comerciales de ARI CONSULTING en Word a partir de un briefing o formulario guiado, aplicando el catálogo, la plantilla y el brand book de la carpeta DOCS. Úsalo para propuestas comerciales ARI; no para cotizaciones de otras marcas.
metadata:
  short-description: Crear propuestas comerciales ARI en Word
---

# Generador de propuestas ARI CONSULTING

Genera propuestas comerciales profesionales para ARI CONSULTING, consultoría Oracle con sede en Ciudad de México. El resultado de un flujo completado es un documento `.docx` nuevo, validado y alineado a la plantilla oficial.

## Fuente de verdad y preparación

1. Localiza la carpeta `DOCS` del proyecto activo. Si el directorio actual ya es `DOCS`, úsalo; de lo contrario, busca una subcarpeta llamada `DOCS`. Si no existe, solicita su ruta al usuario antes de continuar.
2. Conserva en `DOCS` el catálogo vigente, la plantilla oficial, el brand book y los ejemplos de referencia. No los muevas, renombres ni edites. Crea el documento final fuera de esos archivos, en la carpeta de salida indicada por el usuario o en el directorio del proyecto.
3. Antes de presentar servicios, plazos, rangos de inversión o redactar contenido, lee el catálogo ARI vigente, la plantilla oficial y el brand book. Acepta los nombres actuales o equivalentes en español, por ejemplo:
   - `Catalogo-Servicios-*-ARI-CONSULTING*.pdf`
   - `Propuesta-Comercial-ARI-CONSULTING*.docx`
   - `brand-book*.json`
4. Si falta uno de esos tres archivos, informa cuál falta y no generes la propuesta. El catálogo prevalece sobre cualquier solicitud o ejemplo.
5. Usa los ejemplos de propuestas solo para tono y profundidad; nunca para inventar datos, servicios, precios, clientes o casos de éxito.
6. Para consultar `Lista_Consultores.xlsx`, identifica los responsables por especialidad de los servicios elegidos. Muestra nombre y correo corporativo antes de solicitar confirmación. No pidas al usuario que aporte esos datos.

## Inicio de una propuesta

Para una propuesta nueva pregunta exactamente:

> ¿Cómo prefieres comenzar?
> A) Enviar un briefing listo (acepto .txt, .docx o .md)
> B) Completar el formulario guiado conmigo

Si el usuario adjunta un briefing con datos de una oportunidad, omite esta pregunta y ejecuta el flujo de briefing. Un archivo de instrucciones, catálogo, plantilla, brand book o ejemplo no cuenta como briefing.

- Para un briefing, lee [Flujo A](references/workflow.md#flujo-a--validador-de-briefing).
- Para un formulario, sigue [Flujo B](references/workflow.md#flujo-b--formulario-guiado).
- Lee por completo `references/workflow.md` antes de comenzar uno de los dos flujos.

## Límites esenciales

- Incluye solamente servicios del catálogo vigente. Si se solicita algo fuera de catálogo, indícalo y sugiere la alternativa más cercana; no la agregues sin aceptación del usuario.
- No inventes servicios, rangos, plazos, datos de cliente, RFC, teléfonos, gerentes de cuenta, responsables, módulos, descuentos ni casos de éxito.
- No generes el `.docx` si falta un campo obligatorio, el valor de un servicio sale de su rango, el descuento no cumple las reglas o existe otra alerta bloqueante.
- Antes de crear el archivo, presenta el resumen ejecutivo y recibe una confirmación explícita con la pregunta: “¿Puedo generar el documento?”.
- Crea siempre una copia nueva a partir de la plantilla oficial. Modifica los campos y bloques editables en la copia; no reconstruyas la maquetación desde cero ni sobrescribas la plantilla.
- Para crear o editar el `.docx`, usa la habilidad de documentos disponible. Renderiza e inspecciona visualmente cada página antes de entregar. Si no se puede renderizar, informa la limitación antes de entregar y completa las verificaciones estructurales que sí estén disponibles.
- Al cierre, recuerda que la sección de inversión debe ser revisada por el gerente de cuenta antes del envío al cliente.
