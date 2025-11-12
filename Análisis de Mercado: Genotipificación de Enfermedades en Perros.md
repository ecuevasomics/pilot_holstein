# Análisis de Mercado: Genotipificación de Enfermedades en Perros

## México y Latinoamérica

Este repositorio contiene un análisis completo del mercado de genotipificación de enfermedades en perros en México y Latinoamérica, utilizando marcos de análisis empresarial establecidos.

---

## 📁 Archivos Incluidos

### Documentos de Análisis

1. **analisis_mercado_genotipificacion_canina.qmd** - Documento Quarto completo con análisis, código R y visualizaciones
2. **analisis_mercado_genotipificacion_canina.Rmd** - Versión RMarkdown del análisis
3. **referencias.bib** - Bibliografía en formato BibTeX con todas las fuentes citadas

### Datos

4. **datos_crecimiento_mercado.csv** - Proyecciones de crecimiento del mercado 2024-2030
5. **metricas_clave_mercado.csv** - Métricas clave del mercado con fuentes y URLs
6. **segmentacion_animal.csv** - Segmentación del mercado por tipo de animal
7. **fuerzas_porter.csv** - Análisis detallado de las 5 Fuerzas de Porter

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
  "fmsb"          # Gráficos radar
))
```

### Para Quarto (.qmd)

Quarto viene integrado con RStudio 2022.07 o superior. Si usas una versión anterior:

1. Descarga Quarto desde: https://quarto.org/docs/get-started/
2. Instala Quarto en tu sistema
3. Reinicia RStudio

---

## 📊 Cómo Usar los Archivos

### Opción 1: Documento Quarto (.qmd) - RECOMENDADO

1. Abre `analisis_mercado_genotipificacion_canina.qmd` en RStudio
2. Asegúrate de que todos los archivos CSV y `referencias.bib` estén en el mismo directorio
3. Haz clic en el botón **"Render"** en RStudio
4. Selecciona el formato de salida:
   - **HTML**: Para visualización interactiva en navegador
   - **PDF**: Para documento imprimible (requiere LaTeX)

```r
# O renderiza desde la consola
quarto::quarto_render("analisis_mercado_genotipificacion_canina.qmd", output_format = "html")
```

### Opción 2: RMarkdown (.Rmd)

1. Abre `analisis_mercado_genotipificacion_canina.Rmd` en RStudio
2. Asegúrate de que todos los archivos CSV y `referencias.bib` estén en el mismo directorio
3. Haz clic en el botón **"Knit"** en RStudio
4. Selecciona el formato de salida (HTML o PDF)

```r
# O desde la consola
rmarkdown::render("analisis_mercado_genotipificacion_canina.Rmd", output_format = "html_document")
```

### Opción 3: Usar Solo los Datos

Si solo necesitas los datos para tu propio análisis:

```r
# Cargar datos de crecimiento
datos_crecimiento <- read.csv("datos_crecimiento_mercado.csv")

# Cargar métricas clave
metricas <- read.csv("metricas_clave_mercado.csv")

# Cargar segmentación
segmentacion <- read.csv("segmentacion_animal.csv")

# Cargar análisis de Porter
porter <- read.csv("fuerzas_porter.csv")

# Ver estructura de datos
str(datos_crecimiento)
head(metricas)
```

---

## 📈 Contenido del Análisis

### 1. Resumen Ejecutivo
- Métricas clave del mercado
- Datos de crecimiento proyectado
- Estadísticas de penetración de mascotas

### 2. Visualizaciones de Datos
- **Gráfico de crecimiento del mercado** (2024-2030)
- **Segmentación por tipo de animal** (gráfico de pastel)
- **Penetración de mascotas en hogares**
- **Oportunidad en seguros para mascotas**

### 3. Análisis PESTEL
Evaluación de factores:
- Políticos
- Económicos
- Sociales
- Tecnológicos
- Ecológicos
- Legales

### 4. Análisis SWOT
- Fortalezas
- Debilidades
- Oportunidades
- Amenazas
- Estrategias derivadas (FO, DO, FA, DA)

### 5. Análisis de las 5 Fuerzas de Porter
- Rivalidad entre competidores
- Amenaza de nuevos entrantes
- Poder de proveedores
- Poder de compradores
- Amenaza de sustitutos
- **Incluye gráfico radar interactivo**

### 6. Business Model Canvas
- Segmentos de clientes
- Propuesta de valor
- Canales
- Relaciones con clientes
- Fuentes de ingresos
- Recursos clave
- Actividades clave
- Asociaciones clave
- Estructura de costos
- KPIs del modelo de negocio

### 7. Conclusiones y Recomendaciones
- Conclusiones principales
- Estrategias de entrada al mercado
- Recomendaciones operativas
- Factores críticos de éxito

---

## 📚 Fuentes de Datos

Todas las cifras y datos incluidos en este análisis provienen de fuentes confiables:

### Principales Fuentes de Investigación de Mercado

1. **Grand View Research** (2024)
   - Mexico Pet DNA Testing Market Size & Outlook, 2024-2030
   - Latin America Veterinary DNA Testing Market Size & Outlook, 2030
   - URL: https://www.grandviewresearch.com/horizon/outlook/

2. **IMARC Group** (2024)
   - Mexico Veterinary Healthcare Market Report 2025-2033
   - URL: https://www.imarcgroup.com/

### Fuentes Gubernamentales

3. **INEGI** - Instituto Nacional de Estadística y Geografía (2021)
   - Encuesta Nacional de Bienestar Autorreportado (ENBIARE)
   - URL: https://www.inegi.org.mx/programas/enbiare/2021/

4. **SENASICA** - Servicio Nacional de Sanidad, Inocuidad y Calidad Agroalimentaria (2024)
   - Regulación de productos veterinarios
   - URL: https://www.gob.mx/senasica/

### Fuentes de Industria

5. **Forbes México** (2024) - Mercado de mascotas
6. **Swiss Info** (2025) - Mercado de alimentos para mascotas
7. **Anuario LatAm Seguros** (2024) - Seguros para mascotas
8. **Milenio** (2024) - Nanotecnología en mascotas

### Fuentes Académicas

9. **CICESE** (2018) - Genotipificación del virus del moquillo canino
10. **ResearchGate** (2025) - Diversificación del virus de moquillo canino

**Todas las fuentes están citadas con URLs completas en el archivo `metricas_clave_mercado.csv` y en la bibliografía `referencias.bib`.**

---

## 🎯 Marcos de Análisis Utilizados

Este análisis aplica cuatro marcos empresariales reconocidos:

1. **PESTEL** - Análisis de factores macro-ambientales
2. **SWOT** - Análisis de fortalezas, debilidades, oportunidades y amenazas
3. **5 Fuerzas de Porter** - Análisis de intensidad competitiva
4. **Business Model Canvas** - Modelo de negocio completo

---

## 💡 Casos de Uso

Este análisis es útil para:

- **Emprendedores**: Evaluación de oportunidad de negocio
- **Inversionistas**: Due diligence de mercado
- **Académicos**: Investigación de mercados emergentes
- **Consultores**: Base para estrategias de entrada al mercado
- **Veterinarios**: Comprensión de tendencias del sector
- **Estudiantes**: Ejemplo de análisis empresarial completo

---

## 📝 Personalización

### Modificar Visualizaciones

Puedes personalizar los gráficos editando los bloques de código R:

```r
# Cambiar colores
scale_color_manual(values = c("México" = "#TU_COLOR", "Latinoamérica" = "#TU_COLOR"))

# Cambiar tema
theme_minimal()  # Puedes usar: theme_bw(), theme_classic(), etc.

# Ajustar tamaño de figura
fig.width = 12
fig.height = 8
```

### Agregar Nuevos Datos

Para agregar tus propios datos:

1. Crea un nuevo data frame en R
2. Agrega la fuente en el campo correspondiente
3. Crea visualizaciones usando ggplot2 o plotly

```r
# Ejemplo: Agregar nuevos datos
mis_datos <- data.frame(
  Variable = c("A", "B", "C"),
  Valor = c(10, 20, 30),
  Fuente = "Mi Fuente 2024"
)

# Crear gráfico
ggplot(mis_datos, aes(x = Variable, y = Valor)) +
  geom_bar(stat = "identity") +
  labs(caption = "Fuente: Mi Fuente 2024")
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

1. Instala TinyTeX (distribución LaTeX ligera):

```r
install.packages("tinytex")
tinytex::install_tinytex()
```

2. O usa solo formato HTML:

```r
quarto::quarto_render("archivo.qmd", output_format = "html")
```

### Gráficos no se muestran

Asegúrate de que:
1. Todos los paquetes están instalados
2. Los archivos CSV están en el mismo directorio
3. Los datos se cargan correctamente (verifica con `head(datos)`)

---

## 📧 Contacto y Soporte

Para preguntas sobre:
- **Datos**: Consulta las fuentes originales listadas en `referencias.bib`
- **Código R**: Revisa la documentación de los paquetes utilizados
- **Metodología**: Los marcos PESTEL, SWOT, Porter y BMC son estándares de análisis empresarial

---

## 📄 Licencia

Este análisis se proporciona con fines educativos y de investigación. Los datos provienen de fuentes públicas citadas. Para uso comercial, consulta las licencias de las fuentes originales.

---

## 🔄 Actualización de Datos

Los datos de mercado se basan en proyecciones de 2024. Para actualizar:

1. Consulta las fuentes originales (URLs en `metricas_clave_mercado.csv`)
2. Actualiza los data frames en los archivos .qmd o .Rmd
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

---

**Fecha de creación:** Noviembre 2024  
**Versión:** 1.0  
**Formato:** Quarto/RMarkdown compatible con RStudio

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

---

¡Disfruta del análisis! 📊🐕
