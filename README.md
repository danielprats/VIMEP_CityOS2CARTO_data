# VIMEP CityOS2CARTO Data Repository

**Repositori públic de dades GeoParquet per CARTO**

---

## 📦 Contingut

Aquest repositori conté fitxers GeoParquet exportats del sistema VIMEP (espai públic Barcelona) per ser consumits per CARTO via URL pública.

### Estructura

```
/
├── README.md                           # Aquest fitxer
├── iris/                               # Incidències IRIS
│   └── vimep_iris_AAMM.parquet
├── ind/                                # Indicadors agregats
│   └── vimep_ind_AAMM.parquet
└── test/                               # Fitxers de test
    └── test_barcelona_pois.parquet
```

---

## 🔗 URLs per CARTO

### Format URL Raw GitHub

```
https://raw.githubusercontent.com/danielprats/VIMEP_CityOS2CARTO_data/main/<path>/<fitxer>.parquet
```

### Exemples

```
# IRIS Gener 2026
https://raw.githubusercontent.com/danielprats/VIMEP_CityOS2CARTO_data/main/iris/vimep_iris_2601.parquet

# Indicadors Gener 2026
https://raw.githubusercontent.com/danielprats/VIMEP_CityOS2CARTO_data/main/ind/vimep_ind_2601.parquet

# Test
https://raw.githubusercontent.com/danielprats/VIMEP_CityOS2CARTO_data/main/test/test_barcelona_pois.parquet
```

---

## 📊 Dades Disponibles

| Dataset | Descripció | Actualització | Mida aprox. |
|---------|------------|---------------|-------------|
| **IRIS** | Incidències ciutadanes | Mensual | ~500KB |
| **IND** | Indicadors agregats territoris | Mensual | ~2MB |

---

## 🔄 Actualització

Les dades s'actualitzen automàticament via pipeline ETL:

```
PostgreSQL (VIMEP) → Export GeoParquet → Git Push → GitHub → CARTO
```

---

## ⚠️ Avís Legal

Aquestes dades són propietat de l'**Ajuntament de Barcelona**.

**Ús permès:**
- Visualització i anàlisi amb CARTO
- Descàrrega per anàlisi intern

**NO permès:**
- Redistribució sense autorització
- Ús comercial sense llicència

---

## 📝 Metadata

| Camp | Valor |
|------|-------|
| **Organització** | Ajuntament de Barcelona |
| **Projecte** | VIMEP - Espai Públic |
| **Format** | GeoParquet (GZIP) |
| **SRID** | EPSG:25831 (ETRS89 UTM 31N) |
| **Encoding** | UTF-8 |

---

## 🔗 Repositori Principal

El codi font ETL complet està al repositori privat:
- 🔐 **vimep-etl** (privat)

---

**Última actualització:** 2026-01-22  
**Versió:** 1.0.0
