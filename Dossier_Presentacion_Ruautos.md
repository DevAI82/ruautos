# Dossier Ejecutivo: Plan de Transformación Digital & Automatización con IA para RUAUTOS (Albacete)

---

## 1. Resumen Ejecutivo & Contexto de RUAUTOS

**RUAUTOS** es un concesionario de referencia en Albacete especializado en vehículos de ocasión, seminuevos y km 0, avalado por más de 7 años de trayectoria comercial, garantía oficial de 1 año y un riguroso estándar de inspección de **82 puntos de control mecánico y electrónico**.

- **Web oficial auditada:** `https://ruautos.es/`
- **Teléfono de contacto:** `+34 613 05 05 67`
- **Ubicación:** Albacete (Castilla-La Mancha)

### Diagnóstico de los Cuellos de Botella Detectados:
1. **Web Actual en PrestaShop + Elementor:** La web actual utiliza un motor de comercio electrónico tradicional con carrito de compras para vehículos. Su arquitectura sobrecargada genera tiempos de carga superiores a 4 segundos en dispositivos móviles y una tasa de rebote elevada.
2. **Llamadas y Consultas Perdidas en Horas Punta:** Cuando los asesores están en la campa atendiendo a un cliente o realizando una entrega, no pueden descolgar el teléfono ni contestar de inmediato por WhatsApp. En el mercado de ocasión, si un cliente no recibe respuesta en menos de 15 minutos, contacta con otro compraventa.
3. **SEO Local y Erratas en Metadatos:** El título web contiene errores gramaticales (*"Vehículos de Segunda Mano a precio asequibles"*), ausencia de marcado Schema.org `AutoDealer` con geolocalización en Albacete y falta de sincronización directa de stock con Google Merchant/Vehicles.
4. **Dependencia de Procesos Manuales para Tasaciones y Seguimiento:** Ausencia de un CRM automotriz sincronizado que organice el pipeline de leads y recuerde automáticamente a los compradores la revisión gratuita y la ITV anual.

---

## 2. La Solución en Dos Fases

```
┌─────────────────────────────────────────────────────────────┐
│ FASE 1: CAPTACIÓN INMEDIATA & ATENCIÓN 24/7 (Semanas 1-2)    │
│  • Web Showroom ultrarrápida (< 0.8s) + SEO Local Albacete   │
│  • Asistente Telefónico Conversacional (ElevenLabs)         │
│  • Chatbot Multicanal WhatsApp & Instagram DM (Zernio)      │
│  • Campañas de Meta Ads de Alta Conversión (Albacete)        │
└──────────────────────────────┬──────────────────────────────┘
                               │ (Validación de métricas y leads)
                               ▼
┌─────────────────────────────────────────────────────────────┐
│ FASE 2: CRM AUTOMOTRIZ A MEDIDA (Meses 2-3)                 │
│  • Tablero Kanban de Ventas (Nuevo Lead -> Cita -> Entrega) │
│  • Ficha Digital Certificada de Inspección de 82 Puntos     │
│  • Tasador Instantáneo con márgenes y costes de taller      │
│  • Disparos Post-Venta Automáticos (ITV y Aceite a los 11m) │
│  • Base de datos privada en Supabase con Row Level Security │
└─────────────────────────────────────────────────────────────┘
```

---

## 3. Los 4 Pilares de la Propuesta

### Pilar 1: Mejora de Visibilidad Web, Frontend, Seguridad & SEO
- **Frontend Design de Alta Fidelidad:** Desarrollo bajo las directrices de `CLAUDE FRONTEND.md` (Mobile-First, paleta cromática automotriz personalizada `brand-900: #061b3a` y `accent-cyan: #00d1ff`, sombras en capas, micro-interacciones ágiles).
- **Auditoría de Seguridad Exhaustiva:** Conforme a `Auditoria-de-Seguridad.md`:
  - Variables de entorno aisladas en `.env` (credenciales de Supabase, ElevenLabs y Zernio blindadas).
  - Protección de rutas y endpoints API contra inyecciones y accesos no autorizados.
  - Implementación de cabeceras seguras (CSP, HSTS, X-Content-Type-Options).
- **SEO Local Albacete:** Optimización técnica completa: marcado `AutoDealer` JSON-LD, sitemap XML autogenerado, corrección de títulos y metas para búsquedas clave como *"coches segunda mano Albacete"*, *"concesionario ocasión Albacete"* y *"tasación coches Albacete"*.

### Pilar 2: Recepción Telefónica (ElevenLabs) + WhatsApp & Instagram (Zernio)
- **Asistente de Voz Telefónico (ElevenLabs):**
  - Descolgado instantáneo en el `+34 613 05 05 67`.
  - Voz humana hiperrealista en castellano.
  - Consulta en tiempo real de vehículos disponibles, precios al contado y cuotas de financiación.
  - Agendamiento directo de citas para pruebas de conducción y envío simultáneo de WhatsApp con la confirmación y enlace a Google Maps.
- **Suite Omnicanal Zernio (WhatsApp & Instagram):**
  - Atención 24/7 en la API oficial de WhatsApp Business Cloud.
  - Conexión con Instagram Direct de `@ruautos.albacete`: auto-respuesta inmediata a comentarios en Reels o Stories solicitando precio.
  - Filtros interactivos por presupuesto, tipo de coche y combustible.

### Pilar 3: CRM a Medida al Estilo del Salón de Peluquería
- Adaptación del modelo implementado en Salón 224:
  - **Ficha Técnica Única de 82 Puntos:** Sustituye el historial de colorimetría por un informe pericial digitalizado del estado de motor, frenos, diagnosis electrónica y chapa.
  - **Pipeline Visual Kanban:** Control de cada comprador potencial en tiempo real.
  - **Automatización de Fidelización:** Disparo de WhatsApp a los 11 meses de la venta para invitar al cliente a su revisión de cortesía y cambio de aceite, garantizando recompra o recomendación.

### Pilar 4: Campañas de Meta Ads (Facebook & Instagram)
- **Estrategia Dual de Captación:**
  1. *Campaña de Compra Directa:* "Compramos tu coche en Albacete hoy mismo con tasación en 30 minutos".
  2. *Campaña de Venta de Seminuevos:* Carruseles dinámicos con los vehículos recién llegados y cuotas desde 150€/mes con garantía incluida.
  3. *Tráfico directo a WhatsApp Zernio:* Elimina intermediarios y convierte el clic en una conversación en menos de 10 segundos.

---

## 4. Arquitectura Técnica bajo Framework WAT

- **Capa 1: Workflows (SOPs):** Protocolos estandarizados de cualificación de leads, tasación preliminar, reserva de prueba de conducción y entrega de llaves con certificado de 82 puntos.
- **Capa 2: Agentes de IA:**
  - `ElevenLabs Voice Agent`: Reconocimiento de voz (ASR), contexto comercial de automoción y síntesis vocal en castellano.
  - `Zernio Omnichannel Bot`: Gestión de webhooks de WhatsApp e Instagram Graph API.
- **Capa 3: Tools Deterministas:**
  - `inventory_sync.ts`: Consulta y reserva de vehículos en la base de datos de stock.
  - `lead_router.ts`: Asignación automática de oportunidades a los comerciales de Ruautos.
  - `supabase_crm`: PostgreSQL con políticas RLS para garantizar la privacidad de los datos de clientes según el RGPD.

---

## 5. Análisis Financiero & Retorno de Inversión (ROI)

| Métrica Proyectada | Con Sistema Tradicional | Con Plataforma RUAUTOS IA | Impacto Neto |
| :--- | :---: | :---: | :---: |
| **Tiempo de Respuesta a Nuevos Leads** | 2 a 6 horas (o nunca) | **< 10 segundos (24/7)** | Cero fugas comerciales |
| **Llamadas Perdidas Atendidas** | Pérdida de 15-25 llamadas/mes | **100% de llamadas contestadas** | +15 citas de prueba |
| **Coches Vendidos Adicionales** | 0 | **+3 a 5 vehículos/mes** | +4.200€ a 7.000€ margen |
| **Retorno de Inversión Estimado (ROI)** | — | **> 900% anual** | Amortización inmediata |

---

## 6. Recursos & Entregables Disponibles

1. **Simulador Interactivo en Vivo:** Abrir `mockup_interactivo_ruautos.html` en el navegador para probar el asistente de voz con síntesis real, el bot de WhatsApp, el CRM Kanban y la calculadora de ROI.
2. **Presentación Ejecutiva Web:** Abrir `VER_PRESENTACION_RUAUTOS.html`.
3. **Diagrama Vectorial Editable:** Abrir `arquitectura_ruautos.excalidraw` en [excalidraw.com](https://excalidraw.com).
