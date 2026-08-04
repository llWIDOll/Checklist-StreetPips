# Directiva: ui_tabs_checklist_nas100

**Estado:** ACTIVO  
**Versión:** v1.0.0  
**Última actualización:** 2026-08-04  
**Autor:** Agente Antigravity  

---

## Objetivo

Agregar un sistema de tabs (pestañas) al checklist StreetPips que permita alternar entre:
1. **Checklist Original** — El checklist diario existente (Bloque 2, 3 y 5)
2. **Estrategia NAS100 M1** — Nuevo checklist con 10 ítems específicos para operar NAS100 en timeframe M1

### Criterio de Éxito

- El usuario puede alternar entre tabs sin perder el estado de los checks
- Cada tab tiene su propia barra de progreso independiente
- El botón "Reiniciar" limpia solo la tab activa
- El formato visual es idéntico al checklist actual
- La advertencia "Si alguno es NO, no operar" se muestra cuando corresponde

---

## Diseño Visual

### Tabs
- Posicionados debajo del header, antes del progress bar
- Estilo minimalista acorde al diseño existente (bordes sutiles, transiciones suaves)
- Tab activa con indicador visual (border-bottom con color accent)
- Hover suave en tabs inactivas

### Contenido Tab NAS100 M1
- Título: "ESTRATEGIA NAS100 – TF M1"
- Un solo bloque con los 10 ítems del checklist
- Warning row idéntico al existente: "Si alguno es NO, no operar"
- Progress bar independiente mostrando X / 10

---

## Ítems del Checklist NAS100 M1

1. ¿Dónde estoy? POI en H1
2. Rango de 8:12 a 9:12 (máximo y mínimo)
3. ENTRADA SOLO DESPUES DE LAS 9:30 NY
4. Tomar entrada solo si saca el máximo o el mínimo
5. ¿La narrativa es clara con tu dirección?
6. Confirmación en M1: creación del OB y confirmación del 25% FIBONACCI
7. SL técnico en el máximo o mínimo de la estructura M1. Colocar 10 puntos
8. RB gráfico mínimo 1:2
9. TP 1: 75% del Fibo – TP 2: 100% del Fibo o RB 1:2
10. CERRAR EL TRADE COMO ESTÉ A LAS 10:00

---

## Interacciones

- **Click en tab:** Cambia la vista al checklist correspondiente con transición suave
- **Click en check item:** Toggle del estado checked/unchecked (igual al actual)
- **Reiniciar:** Limpia todos los checks de la tab activa y el campo "Activo"
- **Warning:** Se muestra cuando hay al menos 1 item marcado pero no todos

---

## Estados de UI

- **Normal:** Todos los items sin marcar, progress en 0
- **En progreso:** Algunos items marcados, warning visible si hay NO implícitos
- **Completo:** Todos marcados, progress al 100%

---

## Restricciones

- No se usa framework, todo es vanilla HTML/CSS/JS
- CDN para íconos Tabler (ya en uso)
- Sin dependencias adicionales
- Estado en memoria (no persiste entre recargas, igual al actual)

---

## Dependencias y Relaciones

**Depende de:** Ninguna  
**Es prerequisito de:** Ninguna  
**Relacionado con:** Diseño original del checklist StreetPips (mismo archivo index.html)

---

## Protocolo de Errores y Aprendizaje (Memoria Viva)

| Fecha | Problema Detectado | Causa Raíz | Solución Aplicada | Regla Preventiva |
| --- | --- | --- | --- | --- |
| — | — | — | — | — |

---

## Changelog

- v1.0.0 (2026-08-04): Versión inicial — tabs con checklist NAS100 M1 + checklist original
