---
jupytext:
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.11.5
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

# Capitulo 1

## Elasticidad

Para poder entender este propiedad de los materiales, analizaremos el siguiente gráfico.

```{figure} 1.svg
:height: 500px
:name: Gráfico
```

Como se puede apreciar, el objeto en análisis experimentará una deformación y a medida que la fuerza es aplicada, se va acumulando energía potencial de deformación. La misma que puede ser recuperada mediante trabajo externo realizado por el mismo cuerpo, siempre en cuando no se sobrepase el límite elástico.

Es importante comentar que los esfuerzos producidos cerca al punto de aplicación no serán estudiados en este curso, tampoco en los posteriores. Así mismo, es de vital importancia reconocer que la deformacion longitudinal en la sección es la misma para todos los puntos que la conforman. Por lo tanto, se definirá el esfuerzo de la siguiente forma:

```{figure} 2.svg
:height: 500px
:name: Esfuerzo
```

$$\sigma=\frac{P}{A}$$

Esta expresión correspondiente al esfuerzo, significa que la fuerza aplicada se distribuye uniformemente en la seccion, produciéndose asi una deformación uniforme. Si recordamos de la estática, la fuerza P se descompone de manera uniforme sobre la sección.

Ahora bien, cuando la fuerza deja de ser aplicada el cuerpo puede regresar a su estado original, dependiendo de la magnitud y permanencia de la carga, en forma absoluta o parcial, a esta propiedad se la conoce como **Elasticidad** y hay materiales más elásticos que otros. Uno de estos es el acero, por su gran esfuerzo de fluencia (asociado al límite de proporcionalidad).

Estos son algunos valores de módulos de elasticidad para diferentes materiales:

| Material | Módulo de Elasticidad (kgf/cm2) |
|----------|-----------------------------|
| Acero    | 2 x 10^6                  |
| Concreto | 15000 x $\sqrt{f'c}$              |


```{note}
El módulo de elasticidad para el acero para este caso es de grado 60, el más utilizado en el medio.

```

## Ley de Hooke

Robert Hooke desarrolló experimentalmente lo que hoy se conoce como la ley de Hooke y expresa lo siguiente:

$$\delta=\frac{P*L}{A*E}$$

Donde la deformación o elongación es proporcional a la carga y longitud, e inversamente proporcional al área de la sección y módulo de elasticidad. La esencia de este concepto también puede aplicarse a un caso de compresión y no de tensión o tracción. Como se verá más adelante el módulo de elasticidad para el concreto está en función de su resistencia mientras que para el acero dependiendo del grado que sea tendrá un valor diferente. En muchos casos este valor será el mismo para la compresión, salvo para el concreto que es bueno para compresión y no para la tracción.

Considerando que:

$$\frac{\delta}{L}=\epsilon$$
$$\sigma=\frac{P}{A}$$

Tenemos que:

$$\epsilon=\frac{\sigma}{E}$$
$$\sigma=\epsilon*E$$

Esta relación es de suma importancia, ya que sienta las bases del diseño estructura. Sin ella, nada de lo que hoy está construido lo hubiera sido.

```{warning}
La ley de Hooke es válida dentro del rango elástico, más allá ya no. La ley de Hooke como se verá en la curva de deformación justamente viene a ser la pendiente de la función lineal entre el esfuerzo y la deformación.
```

## Ejemplos 1

1. Se pide determinar la elongación de una barra cuyo módulo de elasticidad = 10 x 10^6 psi, longitud = 25 in y el esfuerzo axial = 15 x 10^3 psi.

```{figure} 3.svg
:height: 300px
:name: Ejercicio 1
```

## Diagrama de ensayo a tracción

Para poder comenzar con este apartado, haremos referencia a la curva de esfuerzo ($\sigma$) y deformación ($\epsilon$). En esta gráfica, resaltaremos 4 puntos en específico:

```{figure} 4.svg
:height: 500px
:name: Curva Esfuerzo ' Deformación
```

El punto A es conocido como limite de proporcionalidad, la región debajo de este es de mucha importancia ya que define el rango elástico del material. Como se verá en el siguiente apartado este límite ayudará a establecer un Factor de Seguridad de tal forma que no se incurra en el rango inelástico el cual es muy complicado de analizar.

```{warning}
Para el estudio del impacto de un sismo sobre una edificación no se toma en cuenta el rango no lineal de los materiales propiamente, sino se realiza una simplificación.
```

El otro punto importante es el C, correspondiente al esfuerzo último o de resistencia última. Este valor es de mucha importancia para materiales como el concreto, donde el límite de proporcionalidad es pequeño comparado con el acero.


## Esfuerzo Permisible

Este valor está en función de la resistencia última o de fluencia, dependiendo del material. Veamos la notación:

$$\sigma_w=\frac{\sigma_{YP}}{n}$$
$$\sigma_w=\frac{\sigma_{u}}{n}$$

Para el caso del acero, generalmente se toma un valor de n = 2.

## Ejemplos 2

1. Determinar la elongación y diámetro de la barra

```{figure} 5.svg
:height: 500px
:name: Ejemplo 2
```

2. Determinar la elongación del punto B.

```{figure} 6.svg
:height: 500px
:name: Ejemplo 3
```

```{figure} 7.svg
:height: 500px
:name: Ejemplo 3
```