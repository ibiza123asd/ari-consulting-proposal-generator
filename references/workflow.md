# Flujo operativo de propuestas ARI CONSULTING

## Mapeo de campos

### Obligatorios (10)

| Bloque | Campo | Formato o restricción | Uso |
|---|---|---|---|
| A - Cliente | A1 Razón social | Nombre legal de la empresa | Portada y contenido |
| A - Cliente | A2 Sector de actuación | Sector económico | Portada y contexto |
| A - Cliente | A3 Contacto principal | Nombre + cargo + email | Portada |
| B - Contexto | B1 Situación actual y principal dolor | Sistemas en uso, problema central y desde cuándo | Sección 01 |
| B - Contexto | B2 Dimensión de la operación | Colaboradores, unidades o volumen relevante | Sección 01 |
| C - Solución | C1 Servicios deseados | Mínimo uno; únicamente del catálogo vigente | Secciones 02 y 03 |
| C - Solución | C2 Fecha prevista de inicio | Fecha del inicio del proyecto | Sección 03 |
| D - Datos internos | D1 Número de propuesta | `XXX/AAAA` | Portada y archivo |
| D - Datos internos | D2 Consultor responsable | Nombre + correo `@ariconsulting.com.mx` | Portada y firma |
| E - Inversión | E1 Valor por servicio | Dentro del rango del catálogo | Sección 04 |

### Opcionales

| Campo | Uso o regla |
|---|---|
| O1 RFC | Incluir en portada solo si se proporciona. |
| O2 Teléfono del contacto | Incluir en pie de página solo si se proporciona. |
| O3 Módulos o frentes prioritarios | Detallar en la sección 02 solo si se informa. |
| O4 Impacto del problema | Enriquecer sección 01 solo si se informa. |
| O5 Gerente de cuenta | Incluir en encabezado solo si se proporciona. |
| O6 Plazo por servicio | Si falta, usar el plazo típico del catálogo. |
| O7 Descuento por combinación | Solo para 2 o más servicios; entre 10% y 15%. |
| O8 Fecha de emisión | Usar la fecha actual si falta; vigencia fija de 30 días naturales. |
| O9 Soporte post-implementación | Mencionarlo como opción en próximos pasos. |
| O10 Idioma | Español por defecto; se aceptan inglés y portugués. |

## Reglas de negocio inviolables

1. Incluye únicamente los servicios vigentes del catálogo. Si se solicita algo fuera, informa y ofrece el servicio más cercano sin agregarlo automáticamente.
2. Cada valor debe mantenerse dentro del rango del catálogo. Un valor fuera de rango bloquea la generación: informa el rango válido y solicita corrección.
3. El plazo debe ser coherente con el plazo típico del servicio.
4. El descuento aplica solo con dos o más servicios y debe estar entre 10% y 15%.
5. Las condiciones de pago son fijas: 30% a la firma, 40% al concluir Build y 30% en Go-Live. Muestra importes absolutos calculados sobre el total con descuento.
6. La vigencia siempre es de 30 días naturales desde la emisión.
7. Si el total supera $1,200,000 MXN, alerta que se debe incorporar un estudio de caso de referencia solicitado a Marketing antes del envío.
8. Al cierre, recuerda la revisión de inversión por el gerente de cuenta antes del envío.
9. La metodología siempre incluye seis fases OCIM: Descubrimiento, Diseño, Build, Pruebas, Go-Live e Hiperescalada. Distribuye las semanas de manera coherente con el plazo total.
10. Nunca menciones otras consultorías.

## Flujo A — Validador de briefing

1. Lee el archivo completo.
2. Extrae y mapea la información disponible a los campos obligatorios y opcionales.
3. Presenta exactamente este informe:

```
VALIDACIÓN DEL BRIEFING — [nombre del archivo]

CAMPOS OBLIGATORIOS ENCONTRADOS (X de 10)
A1 Razón social: [valor]
[continuar solo con los campos identificados]

CAMPOS OBLIGATORIOS FALTANTES (X)
[campo] — necesario para [sección de la propuesta]

ALERTAS DE REGLA DE NEGOCIO
[listar alertas; escribir “Ninguna” si no hay]

CAMPOS OPCIONALES IDENTIFICADOS
[listar valores; escribir “Ninguno” si no hay]
```

4. Pregunta únicamente por los obligatorios faltantes, agrupados por bloque y un bloque por vez. No repitas datos ya extraídos.
5. Cuando estén completos y no existan alertas bloqueantes, presenta el resumen ejecutivo y pregunta: “¿Puedo generar el documento?”.
6. Tras la confirmación, genera el `.docx`.

## Flujo B — Formulario guiado

Conduce una etapa por vez. Al final de cada una, muestra exactamente: `Etapa X de 5 completada ✓`.

1. **Etapa 1 de 5 — Cliente (A1-A3):** solicita razón social, sector y contacto principal (nombre, cargo y email).
2. **Etapa 2 de 5 — Contexto (B1-B2):** solicita situación actual y dolor (sistemas, problema y desde cuándo) y dimensión de la operación. Incentiva detalles útiles para la sección 01.
3. **Etapa 3 de 5 — Solución (C1-C2):** presenta todos los servicios vigentes con nombre, plazo típico y rango de inversión tomados del catálogo. Solicita selección y después fecha de inicio.
4. **Etapa 4 de 5 — Datos internos (D1-D2):** solicita el número de propuesta. Luego revisa `Lista_Consultores.xlsx` en `DOCS`; muestra únicamente cada consultor aplicable como `Nombre — correo@ariconsulting.com.mx`. Si hay uno, solicita confirmar su asignación. Si hay varios, solicita confirmar si se incluirá a todos. No pidas nombres ni correos al usuario.
5. **Etapa 5 de 5 — Inversión y opcionales (E1 y opcionales):** propone un valor por servicio dentro de su rango según complejidad y solicita confirmación o ajuste. Para dos o más servicios, pregunta por descuento. Ofrece los opcionales pertinentes, incluido soporte post-implementación e idioma.

Al completar la etapa 5, presenta el resumen ejecutivo y pide confirmación antes de generar.

## Resumen ejecutivo previo a generación

Incluye cliente y contacto; servicios y plazo total; inicio; valores por servicio, subtotal, descuento y total; parcialidades 30%, 40% y 30%; emisión y vigencia; alertas no bloqueantes, incluido el estudio de caso cuando aplique; e indicación de revisión de inversión por el gerente de cuenta.

No generes el documento sin confirmación explícita.

## Generación del documento Word

1. Trabaja desde una copia de la plantilla oficial de `DOCS`; conserva su estructura, páginas, estilos, tablas, encabezados, pies, espaciado y maquetación. No rediseñes el documento ni sustituyas la plantilla por un archivo creado desde cero.
2. Rellena o adapta solamente los espacios editables de la plantilla. Elimina las filas opcionales sin datos cuando la plantilla lo permita, en lugar de dejar marcadores.
3. Aplica el brand book:
   - fondo `#FFFFFF`; títulos y contraste `#0D0D0D`; bloques alternos `#F9F9F9`; metadatos `#555555`;
   - Arial; titulares en negrita, alineados a la izquierda;
   - pills rectangulares negros en mayúsculas para portada;
   - encabezados `XX / 05` en gris muted;
   - tablas sin bordes visibles, fondos alternos y etiquetas en mayúsculas;
   - tabla de inversión con encabezado y total en bloque negro;
   - CTA final limpio con flecha `→`;
   - firma con consultor, cargo, ARI CONSULTING, Ciudad de México y datos disponibles.
4. Mantén la estructura: Portada; 01 Comprensión del Contexto; 02 Solución Propuesta; 03 Metodología y Cronograma; 04 Inversión; 05 Próximos Pasos.
5. Redacta contexto específico en la sección 01; justifica los servicios y alcance en la 02; distribuye OCIM en la 03; muestra inversión, descuento y pagos en la 04; e incluye aprobación, alineación, firma, kickoff y soporte opcional en la 05.
6. Usa el nombre `Propuesta-[NUM]-[AÑO]-[Nombre-Cliente]-ARI-CONSULTING.docx`. Sanitiza el nombre del cliente y cambia la separación de número/año a guiones, por ejemplo: `Propuesta-872-2026-Banco-Americano-Del-Sur-ARI-CONSULTING.docx`.
7. Renderiza e inspecciona todas las páginas antes de entregar. Verifica ausencia de placeholders, datos correctos, tablas, fechas, vigencia, importes, descuento y pagos. Entrega únicamente el `.docx` salvo solicitud contraria.
