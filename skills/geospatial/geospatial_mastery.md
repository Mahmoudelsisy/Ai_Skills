# Geospatial Engineering & GIS Mastery | احتراف الهندسة الجيومكانية ونظم المعلومات الجغرافية

## Arabic Description | وصف بالعربية
قواعد هندسية متقدمة لتطوير الأنظمة الجيومكانية (Geospatial) ونظم المعلومات الجغرافية (GIS). تركز القواعد على قواعد البيانات المكانية (PostGIS)، أنظمة الإحداثيات، ومعالجة البيانات الجغرافية الضخمة.

---

## Strict Rules | قواعد صارمة

### 1. Spatial Databases & PostGIS
- **Spatial Indexing**: ALWAYS use spatial indexes (GIST) for geometry and geography columns to ensure query performance.
- **Geography vs Geometry**: Use `Geography` for global measurements (taking the Earth's curve into account) and `Geometry` for flat, local plane calculations.

### 2. Coordinate Systems & Projections
- **Standardization**: Store all data in WGS84 (EPSG:4326) unless there is a strong requirement for a specific local projection.
- **Transformation Management**: Explicitly handle coordinate transformations (reprojections) to avoid spatial drift and errors.

### 3. High-Scale Geospatial Processing
- **H3 & S2 Indexing**: Use hierarchical hexagonal (H3) or quadkey (S2) indexing for massive spatial aggregations and efficient neighbors searching.
- **Vector Tiles**: Implement MVT (Mapbox Vector Tiles) for efficient web-based map rendering of large datasets.

### 4. Precision & Accuracy
- **Topology Verification**: Ensure spatial data is topologically correct (no self-intersections, no gaps where they shouldn't exist).
- **Precision Limits**: Be mindful of precision limitations in spatial calculations; avoid unnecessary high-precision math for low-resolution data.

### 5. GIS Integration & Standards
- **OGC Compliance**: Adhere to Open Geospatial Consortium (OGC) standards (WMS, WFS, WCS) for interoperability.
- **Data Formats**: Use efficient formats like GeoJSON, GeoPackage, or Cloud Optimized GeoTIFF (COG).
