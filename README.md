# 🏨 Alojamiento turístico en España · Análisis de datos

> Proyecto en equipo del curso de Data Analytics de IT Academy (Barcelona Activa), enero – febrero 2026: [Yoneidy Galindez](https://github.com/YoneidyGalindez), [Luis Chicott](https://github.com/luischicott), [Mariela Giménez](https://github.com/GimenezMariela), [Jianji Chen](https://github.com/JianjiC) y [Esra Kesken](https://github.com/esrakesken).
>
> Repositorio original (rama `Equip_22`): [ITACADEMYprojectes/ProjecteData](https://github.com/ITACADEMYprojectes/ProjecteData/tree/Equip_22/Equip_22)

Análisis de una plataforma de alojamiento turístico con anuncios en ocho provincias españolas, combinado con datos de turismo del INE, para proponer acciones de negocio.

## Preguntas del proyecto

El trabajo se repartió por áreas de análisis:

- **Operaciones e inventario:** ¿cuál es la disponibilidad media de los alojamientos a 30, 60, 90 y 365 días en cada ciudad? ¿Qué características del alojamiento se relacionan con la ocupación?
- **Marketing:** ¿qué destinos y nacionalidades atraen más viajeros? ¿En qué idiomas se publican los anuncios?
- **Experiencia del cliente:** ¿cómo se relacionan el precio, el tipo de habitación y la valoración de los huéspedes?
- **Perfil del viajero:** ¿de dónde vienen los turistas, cuánto tiempo se quedan y en qué meses viajan?

## Datos

| Fuente | Contenido |
|---|---|
| Base de datos MySQL del curso (`Tourist_Accommodation`) | Anuncios de la plataforma: ubicación, precio, disponibilidad, ocupación, valoraciones |
| INE | Pernoctaciones, viajeros por origen y destino, meses de visita |

En `Data/` hay una versión cruda (`Raw`) y otra limpia (`Clean`) de cada tabla. La fecha del nombre indica el sprint.

## Algunos resultados

- **9.650 alojamientos** de 7.269 anfitriones en 8 provincias. Barcelona (2.719) y Madrid (2.134) concentran la mayor oferta.
- Los viajeros pasaron de **81 millones en 2021 a 152 millones en 2022** (+88 %).
- **Idiomas de los anuncios:** 57 % inglés, 38 % español y 5 % otros.
- **Julio 2020:** las provincias de costa (Valencia, Málaga, Baleares) y Sevilla no tenían alojamientos activos; la oferta se concentraba en Madrid y Barcelona.
- **Ocupación:** en una regresión por ciudad, más dormitorios se asocia con más ocupación y más camas con menos. El R² es bajo: el tamaño del alojamiento explica solo una pequeña parte de la ocupación.
- **Estancias:** Baleares tiene las estancias más largas y Madrid las más cortas; Málaga y Girona son los destinos con más crecimiento de pernoctaciones.

**Propuestas de negocio:** captar alojamientos antes del verano en Valencia, Málaga y Baleares; campañas para viajeros de Alemania, Francia y Reino Unido; escapadas cortas en Madrid frente a paquetes de 7 noches o más en Baleares; y abrir mercado en Alicante, Ibiza, Tenerife y Las Palmas.

## Estructura

```
Data/       datos crudos y limpios (MySQL e INE)
Scripts/    notebooks por sprint: extracción, limpieza, EDA, KPIs y análisis por área
Results/    dashboards de Power BI (.pbix) y presentaciones (.pptx)
```

La presentación final es [`Results/Presentación17022026.pptx`](Results/Presentación17022026.pptx).

## Herramientas

Python · Pandas · Jupyter · SQLAlchemy · MySQL · Power BI · PowerPoint · Git y GitHub

## Nota

Fue el primer proyecto del equipo con Git y GitHub, y se trabajó por sprints semanales. Los datos de conexión a la base de datos del curso se han sustituido por marcadores (`TU_HOST`, `TU_USUARIO`).
