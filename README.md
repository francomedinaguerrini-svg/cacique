# Mutual del Cacique — Sistema de Gestión

Sistema de gestión de socios, cuotas y deuda para la Cooperativa de Vivienda Mutual del Cacique.

## Uso

Abrir `mutual_cacique.html` directamente en el navegador (Chrome recomendado). No requiere servidor ni instalación.

## Funcionalidades

- **Informe del tesorero** — resumen ejecutivo con 4 indicadores clickeables
- **Estado por socio** — historial completo de pagos, deuda actualizada por IPIM y plan de pagos
- **Cargar pagos** — registro mensual con cuota normal + cuota plan + Nº comprobante AFIP
- **Listado deudores** — filtrable y ordenable
- **Socios** — padrón completo con edición individual
- **Resumen** — dashboard con métricas del mes

## Flujo mensual

1. Cuando se publica el IPIM → click en **Actualizar IPIM** en el sidebar → ingresar valor y cuota
2. Ir a **Cargar pagos** → seleccionar el mes → registrar pagos → Guardar (genera backup automático)
3. Ver **Informe tesorero** para el estado actualizado

## Datos

- IPIM histórico cargado: Enero 2016 → Junio 2026
- 52 socios con saldos al 30/06/2026
- 6 socios con plan de pago activo (12 cuotas desde Jun 2026)
- Datos guardados en localStorage del navegador

## Backup

Al guardar pagos se descarga automáticamente un archivo `.json` de respaldo.
Para restaurar: **Configuración → Importar backup**.

## Git

```bash
git add mutual_cacique.html README.md
git commit -m "feat: agregar pagos mes YYYY-MM"
git push
```

## Estructura del proyecto

```
mutual_cacique/
├── mutual_cacique.html   # App completa (único archivo)
└── README.md             # Este archivo
```
