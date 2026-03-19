# Laboratorio 9 Parte 2

## Property Statistics Endpoint

Se realizó la implementación del endpoint de estadísticas `GET /api/properties/stats` en el backend de la API RealEstate Hub. El endpoint utiliza las funciones de agregación de Prisma (`groupBy` y `aggregate`) para retornar información analítica sobre las propiedades: conteo por tipo, precio promedio por tipo, rango de precios (mínimo y máximo) y conteo total. En caso de que la base de datos esté vacía, el endpoint retorna ceros en lugar de errores.

---

## Video Explicación:
https://youtu.be/PXAekIWf9OY

---

## Instrucciones para Probar

> **Probado en:** Brave Browser

### Backend

```bash
cd backend

# Instalar dependencias
npm install --legacy-peer-deps
```

### Endpoint de estadísticas

```
http://localhost:3002/api/properties/stats
```

---

## Definition of Done (DoD)

| Criterio | Descripción | Estado |
|----------|-------------|--------|
| Endpoint exists | `GET /api/properties/stats` retorna datos | ✅ |
| Count by type | `{ house: 10, apartment: 15, ... }` | ✅ |
| Average price | Precio promedio por tipo de propiedad | ✅ |
| Price range | `{ min: 50000, max: 2000000 }` | ✅ |
| Total count | Número total de propiedades | ✅ |
| Prisma aggregation | Usa `groupBy` y `aggregate` | ✅ |
| Empty database | Retorna ceros, no errores | ✅ |
