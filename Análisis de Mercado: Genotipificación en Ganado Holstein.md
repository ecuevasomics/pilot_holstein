# Análisis de Mercado: Genotipificación en Ganado Holstein

## México y Latinoamérica

Este repositorio contiene un análisis completo del mercado de genotipificación en ganado Holstein en México y Latinoamérica, utilizando marcos de análisis empresarial establecidos.

---

## 📁 Archivos Incluidos

### Documentos de Análisis

1. **analisis_holstein_genotipificacion.qmd** - Documento Quarto completo (formato recomendado)
2. **analisis_holstein_genotipificacion.Rmd** - Versión RMarkdown alternativa
3. **referencias_holstein.bib** - Bibliografía en formato BibTeX con 16 fuentes principales

### Archivos de Datos CSV

4. **datos_holstein_mercado.csv** - Proyecciones de mercado 2024-2033 (global y bovino)
5. **datos_produccion_lechera.csv** - Producción lechera por país latinoamericano
6. **datos_porter_holstein.csv** - Análisis de las 5 Fuerzas de Porter
7. **datos_segmentos_clientes.csv** - Segmentación de clientes y potencial de ingresos
8. **datos_fuentes_ingresos.csv** - Fuentes de ingresos y proyecciones

### Documentos de Análisis Conceptual

9. **analisis_holstein_pestel.md** - Análisis PESTEL detallado
10. **analisis_holstein_swot.md** - Análisis SWOT completo
11. **analisis_holstein_porter.md** - Análisis de 5 Fuerzas de Porter
12. **analisis_holstein_bmc.md** - Business Model Canvas

---

## 🔧 Requisitos para RStudio

### Paquetes de R Necesarios

```r
# Instalar paquetes necesarios
install.packages(c(
  "tidyverse",    # Manipulación y visualización de datos
  "plotly",       # Gráficos interactivos
  "knitr",        # Generación de reportes
  "kableExtra",   # Tablas formateadas
  "ggplot2",      # Visualizaciones
  "scales",       # Formateo de escalas
  "fmsb",         # Gráficos radar
  "readr"         # Lectura de CSV
))
```

### Para Quarto (.qmd) - RECOMENDADO

Quarto viene integrado con RStudio 2022.07 o superior. Si usas versión anterior:

1. Descarga Quarto desde: https://quarto.org/docs/get-started/
2. Instala Quarto en tu sistema
3. Reinicia RStudio

---

## 📊 Cómo Usar los Archivos

### Opción 1: Documento Quarto (.qmd) - RECOMENDADO ⭐

1. Abre `analisis_holstein_genotipificacion.qmd` en RStudio
2. Asegúrate de que todos los archivos CSV y `referencias_holstein.bib` estén en el mismo directorio
3. Haz clic en el botón **"Render"** en RStudio
4. Selecciona el formato de salida:
   - **HTML**: Para visualización interactiva en navegador (recomendado)
   - **PDF**: Para documento imprimible (requiere LaTeX/TinyTeX)

```r
# O renderiza desde la consola
quarto::quarto_render("analisis_holstein_genotipificacion.qmd", output_format = "html")
```

### Opción 2: RMarkdown (.Rmd)

1. Abre `analisis_holstein_genotipificacion.Rmd` en RStudio
2. Asegúrate de que todos los archivos CSV y `referencias_holstein.bib` estén en el mismo directorio
3. Haz clic en el botón **"Knit"** en RStudio
4. Selecciona el formato de salida (HTML o PDF)

```r
# O desde la consola
rmarkdown::render("analisis_holstein_genotipificacion.Rmd", output_format = "html_document")
```

### Opción 3: Usar Solo los Datos

Si solo necesitas los datos para tu propio análisis:

```r
# Cargar datos de mercado
datos_mercado <- read.csv("datos_holstein_mercado.csv")

# Cargar producción lechera
produccion <- read.csv("datos_produccion_lechera.csv")

# Cargar análisis de Porter
porter <- read.csv("datos_porter_holstein.csv")

# Cargar segmentos de clientes
segmentos <- read.csv("datos_segmentos_clientes.csv")

# Cargar fuentes de ingresos
ingresos <- read.csv("datos_fuentes_ingresos.csv")

# Ver estructura de datos
str(datos_mercado)
head(produccion)
```

---

## 📈 Contenido del Análisis

### 1. Resumen Ejecutivo
- Hallazgos clave del mercado
- Datos de crecimiento proyectado
- Métricas principales

### 2. Datos del Mercado Global
- **Gráfico de crecimiento**: Mercado global vs. segmento bovino (2024-2033)
- **Producción lechera**: Comparación por país latinoamericano
- Análisis de tendencias

### 3. Análisis PESTEL
Evaluación de factores:
- **Políticos**: Marco regulatorio, apoyo gubernamental
- **Económicos**: Tamaño de mercado, volatilidad, oportunidades
- **Sociales**: Humanización, sostenibilidad, educación
- **Tecnológicos**: Disponibilidad de tecnología, laboratorios locales
- **Ecológicos**: Regulaciones ambientales, eficiencia
- **Legales**: Regulaciones, estándares internacionales

### 4. Análisis SWOT
- **Fortalezas**: Mercado en crecimiento, producción significativa, mejora comprobada
- **Debilidades**: Adopción baja, costos elevados, brecha digital
- **Oportunidades**: Demanda de productividad, sostenibilidad, educación
- **Amenazas**: Competencia internacional, volatilidad económica, resistencia

### 5. Análisis de las 5 Fuerzas de Porter
- **Rivalidad entre Competidores**: ALTA (7.5/10)
- **Amenaza de Nuevos Entrantes**: MEDIA-ALTA (6.5/10)
- **Poder de Proveedores**: MEDIA-BAJO (4/10)
- **Poder de Compradores**: MEDIA-ALTO (6.5/10)
- **Amenaza de Sustitutos**: MEDIA (5/10)
- **Gráfico radar interactivo** para visualización

### 6. Business Model Canvas
- **Segmentos de Clientes**: 5 segmentos principales
- **Propuesta de Valor**: Mejora genética, sostenibilidad, precisión
- **Canales**: Directos e indirectos
- **Relaciones**: Educación, soporte, comunidad
- **Fuentes de Ingresos**: 6 fuentes diversificadas
- **Recursos Clave**: Tecnología, personal, datos
- **Actividades Clave**: Procesamiento, análisis, educación
- **Asociaciones**: Instituciones, veterinarios, proveedores
- **Estructura de Costos**: Fijos y variables

### 7. Indicadores Clave de Desempeño (KPIs)
- Financieros: Ingresos, márgenes, ROI
- Volumen: Pruebas, clientes, suscriptores
- Mercado: Cuota, crecimiento, penetración
- Cliente: Retención, CAC, lifetime value, NPS
- Operación: Tiempo, calidad, disponibilidad, satisfacción

### 8. Conclusiones y Recomendaciones
- Conclusiones principales
- Estrategias de entrada al mercado
- Recomendaciones operativas
- Factores críticos de éxito

---

## 📚 Fuentes de Datos

Todas las cifras y datos incluidos en este análisis provienen de fuentes confiables:

### Principales Fuentes de Investigación de Mercado

1. **Grand View Research** (2024)
   - Animal Genetics Market Size & Share | Industry Report, 2033
   - URL: https://www.grandviewresearch.com/industry-analysis/animal-genetics-market

2. **Mordor Intelligence** (2025)
   - Bovine Animal Genetics Market Size & Share Analysis
   - URL: https://www.mordorintelligence.com/industry-reports/bovine-animal-genetics-market

### Fuentes Gubernamentales

3. **INIFAP** - Instituto Nacional de Investigaciones Forestales, Agrícolas y Pecuarias (2022, 2024)
   - Evaluaciones genéticas de ganado Holstein para producción de leche
   - URL: https://www.gob.mx/inifap/

4. **IBGE** - Instituto Brasileño de Geografía y Estadística (2024)
   - Producción de leche: 35.7 mil millones de litros
   - URL: https://agenciadenoticias.ibge.gov.br/

5. **OCLA** - Observatorio de la Cadena Láctea Argentina (2024)
   - Producción láctea en diversas regiones: América Latina
   - URL: https://www.ocla.org.ar/

6. **Fedegán** - Federación Colombiana de Ganaderos (2024)
   - Estadísticas de producción lechera
   - URL: https://www.fedegan.org.co/

### Fuentes Académicas y Científicas

7. **IFCN** - International Farm Comparison Network (2024)
   - IFCN Dairy Report 2024: Improved global milk production
   - URL: https://ifcndairy.org/

8. **Frontiers in Genetics** (2015)
   - García-Ruiz et al.: Genetic differentiation of Mexican Holstein cattle
   - URL: https://www.frontiersin.org/journals/genetics/

9. **Animal Frontiers** (2012)
   - Montaldo: Opportunities and challenges from genomic selection
   - URL: https://academic.oup.com/af/

### Fuentes de Empresas y Servicios

10. **Asociación Holstein de México** (2024)
    - Evaluaciones Genéticas
    - URL: http://holstein.com.mx/

11. **Neogen** (2024)
    - Igenity Cattle Genomics
    - URL: https://www.neogen.com/

12. **ABS Global** (2024)
    - De Novo Genetics
    - URL: https://www.absglobal.com/

---

## 💡 Casos de Uso

Este análisis es útil para:

- **Emprendedores**: Evaluación de oportunidad de negocio en genotipificación
- **Inversionistas**: Due diligence de mercado para decisiones de inversión
- **Académicos**: Investigación de mercados emergentes en Latinoamérica
- **Consultores**: Base para estrategias de entrada al mercado
- **Veterinarios**: Comprensión de tendencias del sector pecuario
- **Ganaderos**: Información sobre mejora genética y tecnologías disponibles
- **Estudiantes**: Ejemplo completo de análisis empresarial multi-framework

---

## 📝 Personalización

### Modificar Visualizaciones

Puedes personalizar los gráficos editando los bloques de código R:

```r
# Cambiar colores
scale_color_manual(values = c("Brasil" = "#TU_COLOR", "México" = "#TU_COLOR"))

# Cambiar tema
theme_minimal()  # Otras opciones: theme_bw(), theme_classic(), theme_dark()

# Ajustar tamaño de figura
fig.width = 14
fig.height = 8
```

### Agregar Nuevos Datos

Para agregar tus propios datos:

```r
# Crear nuevo data frame
mis_datos <- data.frame(
  País = c("Costa Rica", "Panamá"),
  Producción = c(0.5, 0.3),
  Fuente = "Datos 2024"
)

# Combinar con datos existentes
datos_completos <- rbind(produccion, mis_datos)

# Crear visualización
ggplot(datos_completos, aes(x = País, y = Producción)) +
  geom_bar(stat = "identity") +
  labs(caption = "Fuente: Datos 2024")
```

---

## 🐛 Solución de Problemas

### Error: "Package not found"

```r
# Instala el paquete faltante
install.packages("nombre_del_paquete")
```

### Error al renderizar PDF

Si tienes problemas al generar PDF:

```r
# Opción 1: Instala TinyTeX
install.packages("tinytex")
tinytex::install_tinytex()

# Opción 2: Usa solo HTML
quarto::quarto_render("archivo.qmd", output_format = "html")
```

### Gráficos no se muestran

Asegúrate de que:
1. Todos los paquetes están instalados
2. Los archivos CSV están en el mismo directorio
3. Los datos se cargan correctamente (verifica con `head(datos)`)
4. Las rutas de archivos son correctas

---

## 📧 Contacto y Soporte

Para preguntas sobre:
- **Datos**: Consulta las fuentes originales listadas en `referencias_holstein.bib`
- **Código R**: Revisa la documentación de los paquetes utilizados
- **Metodología**: Los marcos PESTEL, SWOT, Porter y BMC son estándares de análisis empresarial

---

## 📄 Licencia

Este análisis se proporciona con fines educativos y de investigación. Los datos provienen de fuentes públicas citadas. Para uso comercial, consulta las licencias de las fuentes originales.

---

## 🔄 Actualización de Datos

Los datos de mercado se basan en información de 2024-2025. Para actualizar:

1. Consulta las fuentes originales (URLs en referencias)
2. Actualiza los archivos CSV con nuevos datos
3. Vuelve a renderizar el documento

---

## ✅ Checklist de Uso

- [ ] Instalar paquetes de R necesarios
- [ ] Descargar todos los archivos en el mismo directorio
- [ ] Abrir archivo .qmd o .Rmd en RStudio
- [ ] Verificar que los datos CSV se cargan correctamente
- [ ] Renderizar/Knit el documento
- [ ] Revisar el output HTML o PDF generado
- [ ] Personalizar según necesidades (opcional)
- [ ] Exportar a formato deseado (PDF, Word, etc.)

---

## 🎓 Recursos Adicionales

### Aprender más sobre los marcos de análisis:

- **PESTEL**: https://www.mindtools.com/pages/article/newTMC_09.htm
- **SWOT**: https://www.mindtools.com/pages/article/newTMC_05.htm
- **5 Fuerzas de Porter**: https://www.isc.hbs.edu/strategy/business-strategy/Pages/the-five-forces.aspx
- **Business Model Canvas**: https://www.strategyzer.com/canvas/business-model-canvas

### Tutoriales de R y Quarto:

- **Quarto**: https://quarto.org/docs/guide/
- **RMarkdown**: https://rmarkdown.rstudio.com/lesson-1.html
- **ggplot2**: https://ggplot2.tidyverse.org/
- **plotly**: https://plotly.com/r/

### Información sobre Genética Bovina:

- **INIFAP**: https://www.gob.mx/inifap/
- **Asociación Holstein de México**: http://holstein.com.mx/
- **IFCN Dairy**: https://ifcndairy.org/

---

**Versión:** 1.0  
**Fecha de creación:** Noviembre 2024  
**Formato:** Quarto/RMarkdown compatible con RStudio  
**Última actualización:** Noviembre 2024

¡Disfruta del análisis! 📊🐄
