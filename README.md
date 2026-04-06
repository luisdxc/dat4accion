# dat4ccion

**Análisis de las barreras al trabajo remunerado de las mujeres en México: brecha salarial, cuidados no remunerados y su valor económico invisible**

Proyecto desarrollado para el datatón [DAT4CCIÓN](https://lac.unwomen.org/es/dat4ccion) organizado por ONU Mujeres América Latina y el Caribe, 2026.

---

## Sobre el proyecto

En México, las mujeres destinan en promedio el doble de horas que los hombres al trabajo doméstico y de cuidados no remunerado — un trabajo que sostiene a las familias y a la economía, pero que no aparece en el PIB ni en ninguna nómina. Esta propuesta parte de ahí: de visibilizar ese trabajo, estimar su valor económico real y mostrar, con datos, cómo su distribución desigual se traduce en consecuencias concretas para las mujeres en su acceso al mercado laboral, su salario, y su tiempo y bienestar.

Lo que distingue este proyecto no es solo reunir datos sobre cuidados y brecha salarial en un mismo lugar, sino **construir un argumento con ellos**. Integramos fuentes que raramente se cruzan — ENOE, ENUT y la Cuenta Satélite de los Hogares — para mostrar el mecanismo: cómo el tiempo dedicado al trabajo no remunerado se traduce en restricciones laborales, salariales y de bienestar. El entregable es un dashboard interactivo navegable por distintas audiencias, no solo por expertas en datos.

El impacto esperado es que funcione como herramienta de incidencia: traducir datos complejos en argumentos comprensibles que respalden políticas de cuidados, corresponsabilidad e igualdad salarial, tanto en México como en otros países de la región donde la metodología pueda replicarse.

---

## Fuentes de datos

Todas las fuentes son públicas, abiertas y de acceso gratuito.

| Base | Edición | Uso en el proyecto | Descarga |
|---|---|---|---|
| ENOE — Encuesta Nacional de Ocupación y Empleo | T4 2024 | Brecha salarial por hora, sector, escolaridad, edad y entidad federativa. Motivos de inactividad laboral femenina. | [INEGI](https://www.inegi.org.mx/programas/enoe/15ymas/#microdatos) |
| ENUT — Encuesta Nacional sobre Uso del Tiempo | 2019 / 2024 | Horas semanales de trabajo no remunerado por actividad y sexo. Insumo central para el análisis de cuidados. | [INEGI](https://www.inegi.org.mx/programas/enut/2019/#microdatos) |
| ENIGH — Encuesta Nacional de Ingresos y Gastos de los Hogares | 2022 / 2024 | Ingreso corriente por hogar, composición familiar, presencia de menores y adultos mayores, análisis por decil y entidad. | [INEGI](https://www.inegi.org.mx/programas/enigh/nc/2024/#microdatos) |
| CSPHOG — Cuenta Satélite del Trabajo No Remunerado de los Hogares | 2022 | Valor económico del trabajo de cuidados como proporción del PIB. Se usa como cifra de referencia, no como microdatos. | [INEGI](https://www.inegi.org.mx/programas/csphog/#tabulados) |
| ILOSTAT — OIT | Actualización continua | Indicadores comparados de brecha salarial y participación laboral para países de ALC. | [ILO](https://ilostat.ilo.org/data/) |
| CEPALSTAT — CEPAL | Actualización continua | Estadísticas de uso del tiempo y trabajo no remunerado para países seleccionados de ALC. | [CEPAL](https://statistics.cepal.org/portal/cepalstat/) |

> **Nota sobre niveles de desagregación:** ENOE y ENIGH tienen representatividad a nivel nacional, 32 entidades federativas y 4 tamaños de localidad. La ENUT tiene representatividad nacional y estatal. Ninguna de las tres desagrega a nivel municipal, por lo que los análisis geográficos están acotados al nivel estatal.

---

## Estructura del repositorio

```
dat4ccion/
├── data/           # Bases de datos en formato CSV 
│                   # No se incluyen los microdatos crudos por su tamaño.
│                   # Se incluyen las bases procesadas y listas para análisis,
│                   # así como los archivos de variables construidas (ej. salario
│                   # por hora expandido, horas de TNR por perfil sociodemográfico).
│
├── doc/            # Documentación del proyecto
│                   # - Diccionarios de variables de cada encuesta
│                   # - Nota metodológica: decisiones de construcción de variables,
│                   #   tratamiento de no respuesta, uso de factores de expansión
│                   #   y supuestos del cruce ecológico ENOE-ENUT
│                   # - Descripción de los módulos del dashboard
│
├── img/            # Imágenes y exportaciones del dashboard
│                   # - Visualizaciones exportadas en PNG/SVG por módulo
│                   # - Capturas del dashboard final
│
├── syntax/         # Scripts de análisis en Python y/o R
│                   
│
└── README.md
```

---

## Equipo


---

## Licencia

Los datos utilizados son de acceso público y pertenecen a sus respectivas fuentes (INEGI, OIT, CEPAL). El código de análisis y visualización se distribuye bajo licencia [MIT](LICENSE).
