# TAREA 2- Publicación de mapas bajo estándares OGC utilizando base de datos espacial y servidor de mapas

 TAREA_2_3101490

# Objetivos

Entender el proceso de publicación de mapas en internet utilizando una base de datos espacial y un servidor de mapas bajo el marco de los estándares de interoperabilidad de OGC.

# Actividades

# 1. Definición del problema 

# • Describa un problema hipotético que pueda resolverse a través del análisis y visualización de datos espaciales.

La complejidad territorial implica una gama de opciones para interpretar los territorios pero, así mismo, requiere un esfuerzo para dar a entender la necesidad de diseñar modelos de futuro para un desarrollo sostenible. En este aspecto, los ejercicios que se encuentran sobre el diagnóstico territorial son mayores a los existentes sobre prospectiva territorial o modelación territorial. 
Tal como lo afirma Posada (2017) al referirse a la complejidad sobre los problemas territoriales que son tantos y tan variados que, a veces, las herramientas para tratarlos y manejarlos se quedan cortas. Aun así, en la evolución de las técnicas para el diseño territorial los SIG juegan un papel muy importante al permitir crear modelos en medio de la complejidad multiespacial, multitemporal y multiobjetivo. 
En consecuencia, el ordenamiento territorial como proceso de apropiación de la comunidad frente a su  territorio, en lo referente a escenarios deseados a futuro, desencadena la posibilidad de orientar y priorizar asuntos que relacionen las dinámicas locales, regionales y nacionales. Asimismo de los aspectos de carácter social, económico, ambiental y cultural que aseguren una gestión integral del territorio. 
# • Describa de forma general el enfoque propuesto para desarrollar el problema. 

# 2. Fuentes de datos

• Listado detallado de las fuentes de datos seleccionadas. Mínimo 3 conjuntos de datos vectoriales. Incluir información del proveedor de los datos, enlace para descarga, título y descripción del conjunto de datos, descripción de los atributos principales a utilizar. 

# • Páramos delimitados. Escala 1:25.000 

**Información del proveedor:** El Sistema de Información Ambiental de Colombia (SIAC) “Es el conjunto integrado de actores, políticas, procesos, y tecnologías involucrados en la gestión de información ambiental del país, para facilitar la generación de conocimiento, la toma de decisiones, la educación y la participación social para el desarrollo sostenible”.

**Enlace para descarga:** http://www.siac.gov.co/catalogo-de-mapas

**Título y descripción:**  Ubicación y seguimiento a la delimitación de páramos en Colombia. 

**Descripción atributos:** Páramo, Departamento, Área 

**•Ecosistemas generales de Colombia ** 

**Información del proveedor:** El Sistema de Información Ambiental de Colombia (SIAC) “Es el conjunto integrado de actores, políticas, procesos, y tecnologías involucrados en la gestión de información ambiental del país, para facilitar la generación de conocimiento, la toma de decisiones, la educación y la participación social para el desarrollo sostenible”.

**Enlace para descarga:** http://www.siac.gov.co/catalogo-de-mapas

**Título y descripción:**  De acuerdo con el mapa de ecosistemas continentales, costeros y marinos de Colombia, escala 1:100.000 (IDEAM, et al, 2015), Colombia cuenta con 98 tipos de ecosistemas generales, 74 corresponden a ecosistemas naturales y 24 a ecosistemas transformados y más de 8000 ecosistemas específicos.

**Descripción atributos:** 

**• Cobertura de la tierra 2010-2012 *** 

**Información del proveedor:** El Instituto de Hidrología, Meteorología y Estudios Ambientales -IDEAM- como integrante del Sistema Nacional Ambiental -SINA-, es responsable de la generación de información y conocimiento sobre el estado de los recursos naturales renovables del país, y como instituto de investigación de carácter nacional, juega un papel fundamental en el diseño de políticas para la protección y mejoramiento del medio ambiente.

**Enlace para descarga:** http://www.siac.gov.co/catalogo-de-mapas

**Título y descripción:**  La "Cobertura" de la tierra, es la cobertura (bio) física que se observa sobre la superficie de la tierra (Di Gregorio, 2005), en un término amplio no solamente describe la vegetación y los elementos antrópicos existentes sobre la tierra, sino que también describen otras superficies terrestres como afloramientos rocosos y cuerpos de agua. En términos puntuales para la delimitación de las coberturas de la Tierra, el IDEAM (1997) describe la cobertura como la unidad delimitable que surge a partir de un análisis de respuestas espectrales determinadas por sus características fisionómicas y ambientales, diferenciables con respecto a la unidad próxima.

**Descripción atributos:** 

**• Cartografía Base escala 1:25.000** 

**Información del proveedor:** La cartografía representa áreas del terreno que muestran elementos básicos como son curvas de nivel, aguas, red hídrica, y algunos elementos artificiales, humanos o culturales, como son las redes de transporte y los centros poblados, entre otros. La cartografía básica está orientada a la representación general de los elementos geográficos existentes en su ámbito, sin dar mayor intensidad a un fenómeno u otro (IGAC, Grupo IDE & GIG).

**Enlace para descarga:** https://geoportal.igac.gov.co/contenido/datos-abiertos-cartografia-y-geografia

**Título y descripción:**  Información espacial a escala 1:25.000 que se  integrara  en  una  geodatabasedel  Instituto  Geográfico  Agustín Codazzi (Igac, 2005), constituida por los Feature Datasets:  edificación  de  obra  civil,  transporte  terrestre,  transporte aéreo, instalación de construcciones  para  transporte,  cobertura  vegetal,  superficies  de agua, relieve, entidades territoriales y unidades administrativas  y  topónimos.

**Descripción atributos:** 


# 3. Procesamiento de datos 

• Descripción detallada del procesamiento realizado a los datos (algoritmos, herramientas utilizadas, modelos, etc)

En esta etapa se realizan procesos y tratamiento de los datos cartográficos principalmente para el área de estudio, lo primero que se debe realizar es definir el área de estudio y construir con los datos cartográficos la representación de la misma, la cual se conforma por el municipio de Ráquira en el Departamento de Boyacá, por  medio  de  la  herramienta  Select(ArcToolbox  >  Analysis  Tools  >  Extract), se extrajo el municipio central de estudio. 

![Zona de estudio]( pantallazo1.png "zona_de_estudio")

![Zona de estudio]( pantallazo2.png "zona_de_estudio")

Realizando  un  buffer o zona de influencia (ArcToolbox > Analysis Tools > Proximity) con un radio de 20 Kilómetros.

![Zona de influencia]( pantallazo3.png "Buffer")

De modo que los municipios intersectados (ArcToolbox > Analysis Tools > Overlay) dentro de dicho polígono tuvieron que ser indagados frente al desarrollo actual de las potencialidades para establecer los integrantes del modelo y la necesidad de desarrollar las potencialidades comunes desde Ráquira como estrategia integradora supramunicipal con los lineamientos de una metodología prospectiva territorial de carácter no prescriptivo y un enfoque participativo, sujeta a entornos inestables,  complejos  y  dinámicos.

![Zona de influencia]( pantallazo4.png "municipios colidantes")

![Zona de influencia]( pantallazo5.png "municipios colidantes")

Fueron superpuestas capas relevantes como páramos, cobertura de tierras, superficies de agua y vías. Para el primer lapso de tiempo  se hizo un análisis espacial con la herramienta Clip (ArcToolbox > Analysis Tools > Extract) de Ráquira con capas como vías, páramos, cobertura vegetal, cobertura de tierra para identificar las fortalezas y las falencias de las potencialidades referidas a la producción minera (carbón) y al sector agrícola de forma espacial. Esta tarea se repite para cada uno de los municipios obtenidos de la tarea anterior.

![Zona de influencia]( pantallazo6.png "clip")

 
• Cargar los datos en el servidor postgresql/ postgis asignado para la clase. 

Por medio de Qgis se van a cargar cada una de las capas a la base de datos Postgis, para esto se debe crear una nueva conexión tal como se ilustra a continuación: 

![Qgis]( pantallazo7.png "conexion base de datos")

En la pestaña Bases de datos se hace clic en Administrador de Bases de Datos 

![Qgis]( pantallazo8.png "conexion base de datos")

Se despliega la siguiente ventana, en donde se dará clic en Importar Capa/Archivo

![Qgis]( pantallazo9.png "conexion base de datos")

![Qgis]( pantallazo.png "conexion base de datos")

• Listar las capas cargadas en el servidor postgresql/postgis (Nota:No olvide el prefijo asignado para la clase.)

Se selecciona la capa que se desea cargar y se nombra con el prefijo asignado para la clase xc_ 

![Qgis]( pantallazo11.png "conexion base de datos")

Realizar la publicación de las capas en Geoserver 

Vamos a la opción capas seguidamente agregar nuevo recurso 

![Qgis]( pantallazo12.png "conexion base de datos")

Se selecciona el almacen de datos de donde se va a sacar la información 

![Qgis]( pantallazo14.png "conexion base de datos")

Se edita la capa que va a ser publicada

![Qgis]( pantallazo15.png "conexion base de datos")

**Capas Cargadas:**

![Qgis]( pantallazo13.png "conexion base de datos")
![Qgis]( pantallazo16.png "conexion base de datos")

# 4. Capa Simbología SLD 

**• Publicar una de las capas utilizando simbología basada en SLD**

Con esta simbología se van a publicar las siguientes capas: 

• Capa de polígonos municipios 
• Capa de polígonos Coberturas de la tierra
•  Capa de polígonos páramos 

**• Si utiliza QGIS para generar el SLD, favor mencionar brevemente el proceso realizado**

Para generar la simbología SLD, se da clic derecho propiedades> simbología la cual es utilizada para el atributo nombre de municipio 

![Qgis]( pantallazo18.png "conexion base de datos")

Se hace clic en estilo>guardar estilo>Archivos SLD tal como se ilustra a continuación: 

![Qgis]( pantallazo17.png "conexion base de datos")

Seguidamente se asigna esta simbología a la capa asignada en geoserver, vamos a estilos y seleccionamos nuevo estilo 

![Qgis]( pantallazo19.png "conexion base de datos")

Se asigna el nombre 

![Qgis]( pantallazo20.png "conexion base de datos")

Se valida que no exista ningún error para cargar la simbología. 

![Qgis]( pantallazo21.png "conexion base de datos")

 **• Texto SLD**

**• Municipios**


 <?xml version="1.0" encoding="UTF-8"?>
<StyledLayerDescriptor xmlns="http://www.opengis.net/sld" xsi:schemaLocation="http://www.opengis.net/sld http://schemas.opengis.net/sld/1.1.0/StyledLayerDescriptor.xsd" xmlns:se="http://www.opengis.net/se" xmlns:ogc="http://www.opengis.net/ogc" version="1.1.0" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
  <NamedLayer>
    <se:Name>xc_Municipios_Select1</se:Name>
    <UserStyle>
      <se:Name>xc_Municipios_Select1</se:Name>
      <se:FeatureTypeStyle>
        <se:Rule>
          <se:Name>CHÍQUIZA</se:Name>
          <se:Description>
            <se:Title>CHÍQUIZA</se:Title>
          </se:Description>
          <ogc:Filter xmlns:ogc="http://www.opengis.net/ogc">
            <ogc:PropertyIsEqualTo>
              <ogc:PropertyName>nom_munici</ogc:PropertyName>
              <ogc:Literal>CHÍQUIZA</ogc:Literal>
            </ogc:PropertyIsEqualTo>
          </ogc:Filter>
          <se:PolygonSymbolizer>
            <se:Fill>
              <se:SvgParameter name="fill">#d7191c</se:SvgParameter>
            </se:Fill>
            <se:Stroke>
              <se:SvgParameter name="stroke">#232323</se:SvgParameter>
              <se:SvgParameter name="stroke-width">1</se:SvgParameter>
              <se:SvgParameter name="stroke-linejoin">bevel</se:SvgParameter>
            </se:Stroke>
          </se:PolygonSymbolizer>
        </se:Rule>
        <se:Rule>
          <se:Name>CUCAITA</se:Name>
          <se:Description>
            <se:Title>CUCAITA</se:Title>
          </se:Description>
          <ogc:Filter xmlns:ogc="http://www.opengis.net/ogc">
            <ogc:PropertyIsEqualTo>
              <ogc:PropertyName>nom_munici</ogc:PropertyName>
              <ogc:Literal>CUCAITA</ogc:Literal>
            </ogc:PropertyIsEqualTo>
          </ogc:Filter>
          <se:PolygonSymbolizer>
            <se:Fill>
              <se:SvgParameter name="fill">#ff2b9a</se:SvgParameter>
            </se:Fill>
            <se:Stroke>
              <se:SvgParameter name="stroke">#232323</se:SvgParameter>
              <se:SvgParameter name="stroke-width">1</se:SvgParameter>
              <se:SvgParameter name="stroke-linejoin">bevel</se:SvgParameter>
            </se:Stroke>
          </se:PolygonSymbolizer>
        </se:Rule>
        <se:Rule>
          <se:Name>GUACHETÁ</se:Name>
          <se:Description>
            <se:Title>GUACHETÁ</se:Title>
          </se:Description>
          <ogc:Filter xmlns:ogc="http://www.opengis.net/ogc">
            <ogc:PropertyIsEqualTo>
              <ogc:PropertyName>nom_munici</ogc:PropertyName>
              <ogc:Literal>GUACHETÁ</ogc:Literal>
            </ogc:PropertyIsEqualTo>
          </ogc:Filter>
          <se:PolygonSymbolizer>
            <se:Fill>
              <se:SvgParameter name="fill">#f69053</se:SvgParameter>
            </se:Fill>
            <se:Stroke>
              <se:SvgParameter name="stroke">#232323</se:SvgParameter>
              <se:SvgParameter name="stroke-width">1</se:SvgParameter>
              <se:SvgParameter name="stroke-linejoin">bevel</se:SvgParameter>
            </se:Stroke>
          </se:PolygonSymbolizer>
        </se:Rule>
        <se:Rule>
          <se:Name>LENGUAZAQUE</se:Name>
          <se:Description>
            <se:Title>LENGUAZAQUE</se:Title>
          </se:Description>
          <ogc:Filter xmlns:ogc="http://www.opengis.net/ogc">
            <ogc:PropertyIsEqualTo>
              <ogc:PropertyName>nom_munici</ogc:PropertyName>
              <ogc:Literal>LENGUAZAQUE</ogc:Literal>
            </ogc:PropertyIsEqualTo>
          </ogc:Filter>
          <se:PolygonSymbolizer>
            <se:Fill>
              <se:SvgParameter name="fill">#4be237</se:SvgParameter>
            </se:Fill>
            <se:Stroke>
              <se:SvgParameter name="stroke">#232323</se:SvgParameter>
              <se:SvgParameter name="stroke-width">1</se:SvgParameter>
              <se:SvgParameter name="stroke-linejoin">bevel</se:SvgParameter>
            </se:Stroke>
          </se:PolygonSymbolizer>
        </se:Rule>
        <se:Rule>
          <se:Name>RÁQUIRA</se:Name>
          <se:Description>
            <se:Title>RÁQUIRA</se:Title>
          </se:Description>
          <ogc:Filter xmlns:ogc="http://www.opengis.net/ogc">
            <ogc:PropertyIsEqualTo>
              <ogc:PropertyName>nom_munici</ogc:PropertyName>
              <ogc:Literal>RÁQUIRA</ogc:Literal>
            </ogc:PropertyIsEqualTo>
          </ogc:Filter>
          <se:PolygonSymbolizer>
            <se:Fill>
              <se:SvgParameter name="fill">#ffdf9a</se:SvgParameter>
            </se:Fill>
            <se:Stroke>
              <se:SvgParameter name="stroke">#232323</se:SvgParameter>
              <se:SvgParameter name="stroke-width">1</se:SvgParameter>
              <se:SvgParameter name="stroke-linejoin">bevel</se:SvgParameter>
            </se:Stroke>
          </se:PolygonSymbolizer>
        </se:Rule>
        <se:Rule>
          <se:Name>SÁCHICA</se:Name>
          <se:Description>
            <se:Title>SÁCHICA</se:Title>
          </se:Description>
          <ogc:Filter xmlns:ogc="http://www.opengis.net/ogc">
            <ogc:PropertyIsEqualTo>
              <ogc:PropertyName>nom_munici</ogc:PropertyName>
              <ogc:Literal>SÁCHICA</ogc:Literal>
            </ogc:PropertyIsEqualTo>
          </ogc:Filter>
          <se:PolygonSymbolizer>
            <se:Fill>
              <se:SvgParameter name="fill">#ffffbf</se:SvgParameter>
            </se:Fill>
            <se:Stroke>
              <se:SvgParameter name="stroke">#232323</se:SvgParameter>
              <se:SvgParameter name="stroke-width">1</se:SvgParameter>
              <se:SvgParameter name="stroke-linejoin">bevel</se:SvgParameter>
            </se:Stroke>
          </se:PolygonSymbolizer>
        </se:Rule>
        <se:Rule>
          <se:Name>SAMACÁ</se:Name>
          <se:Description>
            <se:Title>SAMACÁ</se:Title>
          </se:Description>
          <ogc:Filter xmlns:ogc="http://www.opengis.net/ogc">
            <ogc:PropertyIsEqualTo>
              <ogc:PropertyName>nom_munici</ogc:PropertyName>
              <ogc:Literal>SAMACÁ</ogc:Literal>
            </ogc:PropertyIsEqualTo>
          </ogc:Filter>
          <se:PolygonSymbolizer>
            <se:Fill>
              <se:SvgParameter name="fill">#e7dd1c</se:SvgParameter>
            </se:Fill>
            <se:Stroke>
              <se:SvgParameter name="stroke">#232323</se:SvgParameter>
              <se:SvgParameter name="stroke-width">1</se:SvgParameter>
              <se:SvgParameter name="stroke-linejoin">bevel</se:SvgParameter>
            </se:Stroke>
          </se:PolygonSymbolizer>
        </se:Rule>
        <se:Rule>
          <se:Name>SORA</se:Name>
          <se:Description>
            <se:Title>SORA</se:Title>
          </se:Description>
          <ogc:Filter xmlns:ogc="http://www.opengis.net/ogc">
            <ogc:PropertyIsEqualTo>
              <ogc:PropertyName>nom_munici</ogc:PropertyName>
              <ogc:Literal>SORA</ogc:Literal>
            </ogc:PropertyIsEqualTo>
          </ogc:Filter>
          <se:PolygonSymbolizer>
            <se:Fill>
              <se:SvgParameter name="fill">#bce4aa</se:SvgParameter>
            </se:Fill>
            <se:Stroke>
              <se:SvgParameter name="stroke">#232323</se:SvgParameter>
              <se:SvgParameter name="stroke-width">1</se:SvgParameter>
              <se:SvgParameter name="stroke-linejoin">bevel</se:SvgParameter>
            </se:Stroke>
          </se:PolygonSymbolizer>
        </se:Rule>
        <se:Rule>
          <se:Name>SUTAMARCHÁN</se:Name>
          <se:Description>
            <se:Title>SUTAMARCHÁN</se:Title>
          </se:Description>
          <ogc:Filter xmlns:ogc="http://www.opengis.net/ogc">
            <ogc:PropertyIsEqualTo>
              <ogc:PropertyName>nom_munici</ogc:PropertyName>
              <ogc:Literal>SUTAMARCHÁN</ogc:Literal>
            </ogc:PropertyIsEqualTo>
          </ogc:Filter>
          <se:PolygonSymbolizer>
            <se:Fill>
              <se:SvgParameter name="fill">#91cba9</se:SvgParameter>
            </se:Fill>
            <se:Stroke>
              <se:SvgParameter name="stroke">#232323</se:SvgParameter>
              <se:SvgParameter name="stroke-width">1</se:SvgParameter>
              <se:SvgParameter name="stroke-linejoin">bevel</se:SvgParameter>
            </se:Stroke>
          </se:PolygonSymbolizer>
        </se:Rule>
        <se:Rule>
          <se:Name>VENTAQUEMADA</se:Name>
          <se:Description>
            <se:Title>VENTAQUEMADA</se:Title>
          </se:Description>
          <ogc:Filter xmlns:ogc="http://www.opengis.net/ogc">
            <ogc:PropertyIsEqualTo>
              <ogc:PropertyName>nom_munici</ogc:PropertyName>
              <ogc:Literal>VENTAQUEMADA</ogc:Literal>
            </ogc:PropertyIsEqualTo>
          </ogc:Filter>
          <se:PolygonSymbolizer>
            <se:Fill>
              <se:SvgParameter name="fill">#e7dd1c</se:SvgParameter>
            </se:Fill>
            <se:Stroke>
              <se:SvgParameter name="stroke">#232323</se:SvgParameter>
              <se:SvgParameter name="stroke-width">1</se:SvgParameter>
              <se:SvgParameter name="stroke-linejoin">bevel</se:SvgParameter>
            </se:Stroke>
          </se:PolygonSymbolizer>
        </se:Rule>
        <se:Rule>
          <se:Name></se:Name>
          <se:Description>
            <se:Title>nom_munici is ''</se:Title>
          </se:Description>
          <ogc:Filter xmlns:ogc="http://www.opengis.net/ogc">
            <ogc:Or>
              <ogc:PropertyIsEqualTo>
                <ogc:PropertyName>nom_munici</ogc:PropertyName>
                <ogc:Literal></ogc:Literal>
              </ogc:PropertyIsEqualTo>
              <ogc:PropertyIsNull>
                <ogc:PropertyName>nom_munici</ogc:PropertyName>
              </ogc:PropertyIsNull>
            </ogc:Or>
          </ogc:Filter>
          <se:PolygonSymbolizer>
            <se:Fill>
              <se:SvgParameter name="fill">#2b83ba</se:SvgParameter>
            </se:Fill>
            <se:Stroke>
              <se:SvgParameter name="stroke">#232323</se:SvgParameter>
              <se:SvgParameter name="stroke-width">1</se:SvgParameter>
              <se:SvgParameter name="stroke-linejoin">bevel</se:SvgParameter>
            </se:Stroke>
          </se:PolygonSymbolizer>
        </se:Rule>
        <se:Rule>
          <se:TextSymbolizer>
            <se:Label>
              <ogc:PropertyName>nom_munici</ogc:PropertyName>
            </se:Label>
            <se:Font>
              <se:SvgParameter name="font-family">MS Shell Dlg 2</se:SvgParameter>
              <se:SvgParameter name="font-size">13</se:SvgParameter>
            </se:Font>
            <se:LabelPlacement>
              <se:PointPlacement>
                <se:AnchorPoint>
                  <se:AnchorPointX>0</se:AnchorPointX>
                  <se:AnchorPointY>0.5</se:AnchorPointY>
                </se:AnchorPoint>
              </se:PointPlacement>
            </se:LabelPlacement>
            <se:Fill>
              <se:SvgParameter name="fill">#000000</se:SvgParameter>
            </se:Fill>
            <se:VendorOption name="maxDisplacement">1</se:VendorOption>
          </se:TextSymbolizer>
        </se:Rule>
      </se:FeatureTypeStyle>
    </UserStyle>
  </NamedLayer>
</StyledLayerDescriptor>

![Qgis]( pantallazo22.png "conexion base de datos")

**• Coberturas de la tierra**

?xml version="1.0" encoding="UTF-8"?>
<StyledLayerDescriptor xmlns="http://www.opengis.net/sld" xsi:schemaLocation="http://www.opengis.net/sld http://schemas.opengis.net/sld/1.1.0/StyledLayerDescriptor.xsd" xmlns:se="http://www.opengis.net/se" xmlns:ogc="http://www.opengis.net/ogc" version="1.1.0" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
  <NamedLayer>
    <se:Name>xc_Cobertura_tierra_2010_2012_C</se:Name>
    <UserStyle>
      <se:Name>xc_Cobertura_tierra_2010_2012_C</se:Name>
      <se:FeatureTypeStyle>
        <se:Rule>
          <se:Name>1.1.1. Tejido urbano continuo</se:Name>
          <se:Description>
            <se:Title>1.1.1. Tejido urbano continuo</se:Title>
          </se:Description>
          <ogc:Filter xmlns:ogc="http://www.opengis.net/ogc">
            <ogc:PropertyIsEqualTo>
              <ogc:PropertyName>leyenda3n</ogc:PropertyName>
              <ogc:Literal>1.1.1. Tejido urbano continuo</ogc:Literal>
            </ogc:PropertyIsEqualTo>
          </ogc:Filter>
          <se:PolygonSymbolizer>
            <se:Fill>
              <se:SvgParameter name="fill">#440154</se:SvgParameter>
            </se:Fill>
            <se:Stroke>
              <se:SvgParameter name="stroke">#232323</se:SvgParameter>
              <se:SvgParameter name="stroke-width">1</se:SvgParameter>
              <se:SvgParameter name="stroke-linejoin">bevel</se:SvgParameter>
            </se:Stroke>
          </se:PolygonSymbolizer>
        </se:Rule>
        <se:Rule>
          <se:Name>1.1.2. Tejido urbano discontinuo</se:Name>
          <se:Description>
            <se:Title>1.1.2. Tejido urbano discontinuo</se:Title>
          </se:Description>
          <ogc:Filter xmlns:ogc="http://www.opengis.net/ogc">
            <ogc:PropertyIsEqualTo>
              <ogc:PropertyName>leyenda3n</ogc:PropertyName>
              <ogc:Literal>1.1.2. Tejido urbano discontinuo</ogc:Literal>
            </ogc:PropertyIsEqualTo>
          </ogc:Filter>
          <se:PolygonSymbolizer>
            <se:Fill>
              <se:SvgParameter name="fill">#471265</se:SvgParameter>
            </se:Fill>
            <se:Stroke>
              <se:SvgParameter name="stroke">#232323</se:SvgParameter>
              <se:SvgParameter name="stroke-width">1</se:SvgParameter>
              <se:SvgParameter name="stroke-linejoin">bevel</se:SvgParameter>
            </se:Stroke>
          </se:PolygonSymbolizer>
        </se:Rule>
        <se:Rule>
          <se:Name>1.3.1. Zonas de extraccion minera</se:Name>
          <se:Description>
            <se:Title>1.3.1. Zonas de extraccion minera</se:Title>
          </se:Description>
          <ogc:Filter xmlns:ogc="http://www.opengis.net/ogc">
            <ogc:PropertyIsEqualTo>
              <ogc:PropertyName>leyenda3n</ogc:PropertyName>
              <ogc:Literal>1.3.1. Zonas de extraccion minera</ogc:Literal>
            </ogc:PropertyIsEqualTo>
          </ogc:Filter>
          <se:PolygonSymbolizer>
            <se:Fill>
              <se:SvgParameter name="fill">#482173</se:SvgParameter>
            </se:Fill>
            <se:Stroke>
              <se:SvgParameter name="stroke">#232323</se:SvgParameter>
              <se:SvgParameter name="stroke-width">1</se:SvgParameter>
              <se:SvgParameter name="stroke-linejoin">bevel</se:SvgParameter>
            </se:Stroke>
          </se:PolygonSymbolizer>
        </se:Rule>
        <se:Rule>
          <se:Name>2.3.1. Pastos limpios</se:Name>
          <se:Description>
            <se:Title>2.3.1. Pastos limpios</se:Title>
          </se:Description>
          <ogc:Filter xmlns:ogc="http://www.opengis.net/ogc">
            <ogc:PropertyIsEqualTo>
              <ogc:PropertyName>leyenda3n</ogc:PropertyName>
              <ogc:Literal>2.3.1. Pastos limpios</ogc:Literal>
            </ogc:PropertyIsEqualTo>
          </ogc:Filter>
          <se:PolygonSymbolizer>
            <se:Fill>
              <se:SvgParameter name="fill">#462f7e</se:SvgParameter>
            </se:Fill>
            <se:Stroke>
              <se:SvgParameter name="stroke">#232323</se:SvgParameter>
              <se:SvgParameter name="stroke-width">1</se:SvgParameter>
              <se:SvgParameter name="stroke-linejoin">bevel</se:SvgParameter>
            </se:Stroke>
          </se:PolygonSymbolizer>
        </se:Rule>
        <se:Rule>
          <se:Name>2.3.3. Pastos enmalezados</se:Name>
          <se:Description>
            <se:Title>2.3.3. Pastos enmalezados</se:Title>
          </se:Description>
          <ogc:Filter xmlns:ogc="http://www.opengis.net/ogc">
            <ogc:PropertyIsEqualTo>
              <ogc:PropertyName>leyenda3n</ogc:PropertyName>
              <ogc:Literal>2.3.3. Pastos enmalezados</ogc:Literal>
            </ogc:PropertyIsEqualTo>
          </ogc:Filter>
          <se:PolygonSymbolizer>
            <se:Fill>
              <se:SvgParameter name="fill">#423e85</se:SvgParameter>
            </se:Fill>
            <se:Stroke>
              <se:SvgParameter name="stroke">#232323</se:SvgParameter>
              <se:SvgParameter name="stroke-width">1</se:SvgParameter>
              <se:SvgParameter name="stroke-linejoin">bevel</se:SvgParameter>
            </se:Stroke>
          </se:PolygonSymbolizer>
        </se:Rule>
        <se:Rule>
          <se:Name>2.4.1. Mosaico de cultivos</se:Name>
          <se:Description>
            <se:Title>2.4.1. Mosaico de cultivos</se:Title>
          </se:Description>
          <ogc:Filter xmlns:ogc="http://www.opengis.net/ogc">
            <ogc:PropertyIsEqualTo>
              <ogc:PropertyName>leyenda3n</ogc:PropertyName>
              <ogc:Literal>2.4.1. Mosaico de cultivos</ogc:Literal>
            </ogc:PropertyIsEqualTo>
          </ogc:Filter>
          <se:PolygonSymbolizer>
            <se:Fill>
              <se:SvgParameter name="fill">#3e4b8a</se:SvgParameter>
            </se:Fill>
            <se:Stroke>
              <se:SvgParameter name="stroke">#232323</se:SvgParameter>
              <se:SvgParameter name="stroke-width">1</se:SvgParameter>
              <se:SvgParameter name="stroke-linejoin">bevel</se:SvgParameter>
            </se:Stroke>
          </se:PolygonSymbolizer>
        </se:Rule>
        <se:Rule>
          <se:Name>2.4.2. Mosaico de pastos y cultivos</se:Name>
          <se:Description>
            <se:Title>2.4.2. Mosaico de pastos y cultivos</se:Title>
          </se:Description>
          <ogc:Filter xmlns:ogc="http://www.opengis.net/ogc">
            <ogc:PropertyIsEqualTo>
              <ogc:PropertyName>leyenda3n</ogc:PropertyName>
              <ogc:Literal>2.4.2. Mosaico de pastos y cultivos</ogc:Literal>
            </ogc:PropertyIsEqualTo>
          </ogc:Filter>
          <se:PolygonSymbolizer>
            <se:Fill>
              <se:SvgParameter name="fill">#38588c</se:SvgParameter>
            </se:Fill>
            <se:Stroke>
              <se:SvgParameter name="stroke">#232323</se:SvgParameter>
              <se:SvgParameter name="stroke-width">1</se:SvgParameter>
              <se:SvgParameter name="stroke-linejoin">bevel</se:SvgParameter>
            </se:Stroke>
          </se:PolygonSymbolizer>
        </se:Rule>
        <se:Rule>
          <se:Name>2.4.3. Mosaico de cultivos, pastos y espacios naturales</se:Name>
          <se:Description>
            <se:Title>2.4.3. Mosaico de cultivos, pastos y espacios naturales</se:Title>
          </se:Description>
          <ogc:Filter xmlns:ogc="http://www.opengis.net/ogc">
            <ogc:PropertyIsEqualTo>
              <ogc:PropertyName>leyenda3n</ogc:PropertyName>
              <ogc:Literal>2.4.3. Mosaico de cultivos, pastos y espacios naturales</ogc:Literal>
            </ogc:PropertyIsEqualTo>
          </ogc:Filter>
          <se:PolygonSymbolizer>
            <se:Fill>
              <se:SvgParameter name="fill">#32648d</se:SvgParameter>
            </se:Fill>
            <se:Stroke>
              <se:SvgParameter name="stroke">#232323</se:SvgParameter>
              <se:SvgParameter name="stroke-width">1</se:SvgParameter>
              <se:SvgParameter name="stroke-linejoin">bevel</se:SvgParameter>
            </se:Stroke>
          </se:PolygonSymbolizer>
        </se:Rule>
        <se:Rule>
          <se:Name>2.4.4. Mosaico de pastos con espacios naturales</se:Name>
          <se:Description>
            <se:Title>2.4.4. Mosaico de pastos con espacios naturales</se:Title>
          </se:Description>
          <ogc:Filter xmlns:ogc="http://www.opengis.net/ogc">
            <ogc:PropertyIsEqualTo>
              <ogc:PropertyName>leyenda3n</ogc:PropertyName>
              <ogc:Literal>2.4.4. Mosaico de pastos con espacios naturales</ogc:Literal>
            </ogc:PropertyIsEqualTo>
          </ogc:Filter>
          <se:PolygonSymbolizer>
            <se:Fill>
              <se:SvgParameter name="fill">#2d6f8e</se:SvgParameter>
            </se:Fill>
            <se:Stroke>
              <se:SvgParameter name="stroke">#232323</se:SvgParameter>
              <se:SvgParameter name="stroke-width">1</se:SvgParameter>
              <se:SvgParameter name="stroke-linejoin">bevel</se:SvgParameter>
            </se:Stroke>
          </se:PolygonSymbolizer>
        </se:Rule>
        <se:Rule>
          <se:Name>2.4.5. Mosaico de cultivos con espacios naturales</se:Name>
          <se:Description>
            <se:Title>2.4.5. Mosaico de cultivos con espacios naturales</se:Title>
          </se:Description>
          <ogc:Filter xmlns:ogc="http://www.opengis.net/ogc">
            <ogc:PropertyIsEqualTo>
              <ogc:PropertyName>leyenda3n</ogc:PropertyName>
              <ogc:Literal>2.4.5. Mosaico de cultivos con espacios naturales</ogc:Literal>
            </ogc:PropertyIsEqualTo>
          </ogc:Filter>
          <se:PolygonSymbolizer>
            <se:Fill>
              <se:SvgParameter name="fill">#297a8e</se:SvgParameter>
            </se:Fill>
            <se:Stroke>
              <se:SvgParameter name="stroke">#232323</se:SvgParameter>
              <se:SvgParameter name="stroke-width">1</se:SvgParameter>
              <se:SvgParameter name="stroke-linejoin">bevel</se:SvgParameter>
            </se:Stroke>
          </se:PolygonSymbolizer>
        </se:Rule>
        <se:Rule>
          <se:Name>3.1.1. Bosque denso</se:Name>
          <se:Description>
            <se:Title>3.1.1. Bosque denso</se:Title>
          </se:Description>
          <ogc:Filter xmlns:ogc="http://www.opengis.net/ogc">
            <ogc:PropertyIsEqualTo>
              <ogc:PropertyName>leyenda3n</ogc:PropertyName>
              <ogc:Literal>3.1.1. Bosque denso</ogc:Literal>
            </ogc:PropertyIsEqualTo>
          </ogc:Filter>
          <se:PolygonSymbolizer>
            <se:Fill>
              <se:SvgParameter name="fill">#24858e</se:SvgParameter>
            </se:Fill>
            <se:Stroke>
              <se:SvgParameter name="stroke">#232323</se:SvgParameter>
              <se:SvgParameter name="stroke-width">1</se:SvgParameter>
              <se:SvgParameter name="stroke-linejoin">bevel</se:SvgParameter>
            </se:Stroke>
          </se:PolygonSymbolizer>
        </se:Rule>
        <se:Rule>
          <se:Name>3.1.2. Bosque abierto</se:Name>
          <se:Description>
            <se:Title>3.1.2. Bosque abierto</se:Title>
          </se:Description>
          <ogc:Filter xmlns:ogc="http://www.opengis.net/ogc">
            <ogc:PropertyIsEqualTo>
              <ogc:PropertyName>leyenda3n</ogc:PropertyName>
              <ogc:Literal>3.1.2. Bosque abierto</ogc:Literal>
            </ogc:PropertyIsEqualTo>
          </ogc:Filter>
          <se:PolygonSymbolizer>
            <se:Fill>
              <se:SvgParameter name="fill">#20908d</se:SvgParameter>
            </se:Fill>
            <se:Stroke>
              <se:SvgParameter name="stroke">#232323</se:SvgParameter>
              <se:SvgParameter name="stroke-width">1</se:SvgParameter>
              <se:SvgParameter name="stroke-linejoin">bevel</se:SvgParameter>
            </se:Stroke>
          </se:PolygonSymbolizer>
        </se:Rule>
        <se:Rule>
          <se:Name>3.1.3. Bosque fragmentado</se:Name>
          <se:Description>
            <se:Title>3.1.3. Bosque fragmentado</se:Title>
          </se:Description>
          <ogc:Filter xmlns:ogc="http://www.opengis.net/ogc">
            <ogc:PropertyIsEqualTo>
              <ogc:PropertyName>leyenda3n</ogc:PropertyName>
              <ogc:Literal>3.1.3. Bosque fragmentado</ogc:Literal>
            </ogc:PropertyIsEqualTo>
          </ogc:Filter>
          <se:PolygonSymbolizer>
            <se:Fill>
              <se:SvgParameter name="fill">#1e9b89</se:SvgParameter>
            </se:Fill>
            <se:Stroke>
              <se:SvgParameter name="stroke">#232323</se:SvgParameter>
              <se:SvgParameter name="stroke-width">1</se:SvgParameter>
              <se:SvgParameter name="stroke-linejoin">bevel</se:SvgParameter>
            </se:Stroke>
          </se:PolygonSymbolizer>
        </se:Rule>
        <se:Rule>
          <se:Name>3.1.4. Bosque de galeria y ripario</se:Name>
          <se:Description>
            <se:Title>3.1.4. Bosque de galeria y ripario</se:Title>
          </se:Description>
          <ogc:Filter xmlns:ogc="http://www.opengis.net/ogc">
            <ogc:PropertyIsEqualTo>
              <ogc:PropertyName>leyenda3n</ogc:PropertyName>
              <ogc:Literal>3.1.4. Bosque de galeria y ripario</ogc:Literal>
            </ogc:PropertyIsEqualTo>
          </ogc:Filter>
          <se:PolygonSymbolizer>
            <se:Fill>
              <se:SvgParameter name="fill">#21a685</se:SvgParameter>
            </se:Fill>
            <se:Stroke>
              <se:SvgParameter name="stroke">#232323</se:SvgParameter>
              <se:SvgParameter name="stroke-width">1</se:SvgParameter>
              <se:SvgParameter name="stroke-linejoin">bevel</se:SvgParameter>
            </se:Stroke>
          </se:PolygonSymbolizer>
        </se:Rule>
        <se:Rule>
          <se:Name>3.1.5. Plantacion forestal</se:Name>
          <se:Description>
            <se:Title>3.1.5. Plantacion forestal</se:Title>
          </se:Description>
          <ogc:Filter xmlns:ogc="http://www.opengis.net/ogc">
            <ogc:PropertyIsEqualTo>
              <ogc:PropertyName>leyenda3n</ogc:PropertyName>
              <ogc:Literal>3.1.5. Plantacion forestal</ogc:Literal>
            </ogc:PropertyIsEqualTo>
          </ogc:Filter>
          <se:PolygonSymbolizer>
            <se:Fill>
              <se:SvgParameter name="fill">#2ab07e</se:SvgParameter>
            </se:Fill>
            <se:Stroke>
              <se:SvgParameter name="stroke">#232323</se:SvgParameter>
              <se:SvgParameter name="stroke-width">1</se:SvgParameter>
              <se:SvgParameter name="stroke-linejoin">bevel</se:SvgParameter>
            </se:Stroke>
          </se:PolygonSymbolizer>
        </se:Rule>
        <se:Rule>
          <se:Name>3.2.1. Herbazal</se:Name>
          <se:Description>
            <se:Title>3.2.1. Herbazal</se:Title>
          </se:Description>
          <ogc:Filter xmlns:ogc="http://www.opengis.net/ogc">
            <ogc:PropertyIsEqualTo>
              <ogc:PropertyName>leyenda3n</ogc:PropertyName>
              <ogc:Literal>3.2.1. Herbazal</ogc:Literal>
            </ogc:PropertyIsEqualTo>
          </ogc:Filter>
          <se:PolygonSymbolizer>
            <se:Fill>
              <se:SvgParameter name="fill">#3bbb75</se:SvgParameter>
            </se:Fill>
            <se:Stroke>
              <se:SvgParameter name="stroke">#232323</se:SvgParameter>
              <se:SvgParameter name="stroke-width">1</se:SvgParameter>
              <se:SvgParameter name="stroke-linejoin">bevel</se:SvgParameter>
            </se:Stroke>
          </se:PolygonSymbolizer>
        </se:Rule>
        <se:Rule>
          <se:Name>3.2.2. Arbustal</se:Name>
          <se:Description>
            <se:Title>3.2.2. Arbustal</se:Title>
          </se:Description>
          <ogc:Filter xmlns:ogc="http://www.opengis.net/ogc">
            <ogc:PropertyIsEqualTo>
              <ogc:PropertyName>leyenda3n</ogc:PropertyName>
              <ogc:Literal>3.2.2. Arbustal</ogc:Literal>
            </ogc:PropertyIsEqualTo>
          </ogc:Filter>
          <se:PolygonSymbolizer>
            <se:Fill>
              <se:SvgParameter name="fill">#51c569</se:SvgParameter>
            </se:Fill>
            <se:Stroke>
              <se:SvgParameter name="stroke">#232323</se:SvgParameter>
              <se:SvgParameter name="stroke-width">1</se:SvgParameter>
              <se:SvgParameter name="stroke-linejoin">bevel</se:SvgParameter>
            </se:Stroke>
          </se:PolygonSymbolizer>
        </se:Rule>
        <se:Rule>
          <se:Name>3.2.3. Vegetacion secundaria o en transicion</se:Name>
          <se:Description>
            <se:Title>3.2.3. Vegetacion secundaria o en transicion</se:Title>
          </se:Description>
          <ogc:Filter xmlns:ogc="http://www.opengis.net/ogc">
            <ogc:PropertyIsEqualTo>
              <ogc:PropertyName>leyenda3n</ogc:PropertyName>
              <ogc:Literal>3.2.3. Vegetacion secundaria o en transicion</ogc:Literal>
            </ogc:PropertyIsEqualTo>
          </ogc:Filter>
          <se:PolygonSymbolizer>
            <se:Fill>
              <se:SvgParameter name="fill">#69cd5b</se:SvgParameter>
            </se:Fill>
            <se:Stroke>
              <se:SvgParameter name="stroke">#232323</se:SvgParameter>
              <se:SvgParameter name="stroke-width">1</se:SvgParameter>
              <se:SvgParameter name="stroke-linejoin">bevel</se:SvgParameter>
            </se:Stroke>
          </se:PolygonSymbolizer>
        </se:Rule>
        <se:Rule>
          <se:Name>3.3.3. Tierras desnudas y degradadas</se:Name>
          <se:Description>
            <se:Title>3.3.3. Tierras desnudas y degradadas</se:Title>
          </se:Description>
          <ogc:Filter xmlns:ogc="http://www.opengis.net/ogc">
            <ogc:PropertyIsEqualTo>
              <ogc:PropertyName>leyenda3n</ogc:PropertyName>
              <ogc:Literal>3.3.3. Tierras desnudas y degradadas</ogc:Literal>
            </ogc:PropertyIsEqualTo>
          </ogc:Filter>
          <se:PolygonSymbolizer>
            <se:Fill>
              <se:SvgParameter name="fill">#85d54a</se:SvgParameter>
            </se:Fill>
            <se:Stroke>
              <se:SvgParameter name="stroke">#232323</se:SvgParameter>
              <se:SvgParameter name="stroke-width">1</se:SvgParameter>
              <se:SvgParameter name="stroke-linejoin">bevel</se:SvgParameter>
            </se:Stroke>
          </se:PolygonSymbolizer>
        </se:Rule>
        <se:Rule>
          <se:Name>4.1.1. Zonas Pantanosas</se:Name>
          <se:Description>
            <se:Title>4.1.1. Zonas Pantanosas</se:Title>
          </se:Description>
          <ogc:Filter xmlns:ogc="http://www.opengis.net/ogc">
            <ogc:PropertyIsEqualTo>
              <ogc:PropertyName>leyenda3n</ogc:PropertyName>
              <ogc:Literal>4.1.1. Zonas Pantanosas</ogc:Literal>
            </ogc:PropertyIsEqualTo>
          </ogc:Filter>
          <se:PolygonSymbolizer>
            <se:Fill>
              <se:SvgParameter name="fill">#a3da36</se:SvgParameter>
            </se:Fill>
            <se:Stroke>
              <se:SvgParameter name="stroke">#232323</se:SvgParameter>
              <se:SvgParameter name="stroke-width">1</se:SvgParameter>
              <se:SvgParameter name="stroke-linejoin">bevel</se:SvgParameter>
            </se:Stroke>
          </se:PolygonSymbolizer>
        </se:Rule>
        <se:Rule>
          <se:Name>4.1.3. Vegetacion acuatica sobre cuerpos de agua</se:Name>
          <se:Description>
            <se:Title>4.1.3. Vegetacion acuatica sobre cuerpos de agua</se:Title>
          </se:Description>
          <ogc:Filter xmlns:ogc="http://www.opengis.net/ogc">
            <ogc:PropertyIsEqualTo>
              <ogc:PropertyName>leyenda3n</ogc:PropertyName>
              <ogc:Literal>4.1.3. Vegetacion acuatica sobre cuerpos de agua</ogc:Literal>
            </ogc:PropertyIsEqualTo>
          </ogc:Filter>
          <se:PolygonSymbolizer>
            <se:Fill>
              <se:SvgParameter name="fill">#c2e023</se:SvgParameter>
            </se:Fill>
            <se:Stroke>
              <se:SvgParameter name="stroke">#232323</se:SvgParameter>
              <se:SvgParameter name="stroke-width">1</se:SvgParameter>
              <se:SvgParameter name="stroke-linejoin">bevel</se:SvgParameter>
            </se:Stroke>
          </se:PolygonSymbolizer>
        </se:Rule>
        <se:Rule>
          <se:Name>5.1.2. Lagunas, lagos y cienagas naturales</se:Name>
          <se:Description>
            <se:Title>5.1.2. Lagunas, lagos y cienagas naturales</se:Title>
          </se:Description>
          <ogc:Filter xmlns:ogc="http://www.opengis.net/ogc">
            <ogc:PropertyIsEqualTo>
              <ogc:PropertyName>leyenda3n</ogc:PropertyName>
              <ogc:Literal>5.1.2. Lagunas, lagos y cienagas naturales</ogc:Literal>
            </ogc:PropertyIsEqualTo>
          </ogc:Filter>
          <se:PolygonSymbolizer>
            <se:Fill>
              <se:SvgParameter name="fill">#e1e419</se:SvgParameter>
            </se:Fill>
            <se:Stroke>
              <se:SvgParameter name="stroke">#232323</se:SvgParameter>
              <se:SvgParameter name="stroke-width">1</se:SvgParameter>
              <se:SvgParameter name="stroke-linejoin">bevel</se:SvgParameter>
            </se:Stroke>
          </se:PolygonSymbolizer>
        </se:Rule>
        <se:Rule>
          <se:Name></se:Name>
          <se:Description>
            <se:Title>leyenda3n is ''</se:Title>
          </se:Description>
          <ogc:Filter xmlns:ogc="http://www.opengis.net/ogc">
            <ogc:Or>
              <ogc:PropertyIsEqualTo>
                <ogc:PropertyName>leyenda3n</ogc:PropertyName>
                <ogc:Literal></ogc:Literal>
              </ogc:PropertyIsEqualTo>
              <ogc:PropertyIsNull>
                <ogc:PropertyName>leyenda3n</ogc:PropertyName>
              </ogc:PropertyIsNull>
            </ogc:Or>
          </ogc:Filter>
          <se:PolygonSymbolizer>
            <se:Fill>
              <se:SvgParameter name="fill">#fde725</se:SvgParameter>
            </se:Fill>
            <se:Stroke>
              <se:SvgParameter name="stroke">#232323</se:SvgParameter>
              <se:SvgParameter name="stroke-width">1</se:SvgParameter>
              <se:SvgParameter name="stroke-linejoin">bevel</se:SvgParameter>
            </se:Stroke>
          </se:PolygonSymbolizer>
        </se:Rule>
      </se:FeatureTypeStyle>
    </UserStyle>
  </NamedLayer>
</StyledLayerDescriptor>




# 5. Capa simbología CSS

• Publicar una de las capas utilizando simbología basada en CSS
• Incluir texto del CSS en el markdown del Readme.md
• Describir método utilizado para clasificar los datos.
• Describir el criterio para la selección de los colores a utilizar en la simbología
• Las reglas de la simbología deben incluir control de escala y etiquetado.
• Adjuntar imagen con la leyenda de la capa. 

# 6. Capa Simbología YSLD 

• Publicar una de las capas utilizando simbología basada en YSLD
• Incluir texto del YSLD en el markdown del Readmen.md 
• Describir método utilizado para clasificar los datos. 
• Describir el criterio para la selección de los colores a utilizar en la simbología 
* Las regals de la simbología deben incluir control de escala y etiquetado. 
Adjuntar imagen con la leyenda de la cpa 

# 7. Grupo de capas 

• Crear un layer group (https://docs.geoserver.org/stable/en/user/data/webadmin/layergroups.html ) que contenga las capas creadas en los puntos, y   y las adicionales que considere necesarias para darle contexto a la visualización ( ejm. límites departamentales, límites municipales, límites internacionales, etc)
• Adjuntar  el URL  de la previsualización openlayers del conjunto de capas generada por Geoserver.Ejemplo: http://34.83.176.208:18080/geoserver/wms?service=WMS&version=1.1.0&request=GetMap&layers=tiger-ny&bbox=-74.047185%2C40.679648%2C-73.907005%2C40.882078&width=531&height=768&srs=EPSG%3A4326&format=application/openlayers

# 8. Conclusiones 

• Publicar un video en Loom ( https://www.loom.com/ ) de mínimo 5 minutos y máximo 8 y adjuntar el url del mismo. 
• En el video describa brevemente lo siguiente: 
* Problema planteado 
* Procesamiento y análisis realizado a los datos 
* Proceso de publicación de capas 
* Conclusiones del ejercicio desde el punto de vista temático según problema definido. 
Tutorial de loom https://support.loom.com/hc/en-us/articles/360006847737-Guide-to-Using-Loom-for-Education 

