COVID-19

El crecimiento de contagio de la enfermedad COVID-19 causada por el virus SARS-CoV-2, se comporta de una manera que puede ser modelada muy bien con funciones exponenciales. Por ello, se habla de que el crecimiento de contagios es exponencial. Y dado que, como vimos, estamos hablando de funciones que crecen de una manera pavorosa en poco tiempo.

Un detalle que la convirtió en pandemia, es su bajo índice de letalidad. El Ébola, por ejemplo, con un índice de letalidad que llegó al 90% en ciertos brotes, no se convirtió en pandemia porque si bien era muy contagioso, los afectados no daban tiempo a expandir la enfermedad porque morían pronto.

Se hablaba mucho de que con la cuarentena se buscaba aplanar la curva de contagios con el fin de que el sistema de salud no colapse, y de esa manera, todos los infectados puedan ser atendidos en las mejores condiciones posibles. Pero ¿a qué se refieren concretamente con aplanar una curva y de qué curva hablan?

Tomando datos del Ministerio de Salud de la Nación (que incluyen los casos registrados en las Islas Malvinas, como era de esperarse), realicé una serie de interpolaciones de dichos datos, y luego de haber hallado las funciones exponenciales que mejor ajustaban esa muestra, extrapolé a futuro la función que ajustaba el comienzo de la muestra, a fin de ver cuán eficiente estaba resultando la cuarentena.

Los datos a los que me refiero consisten en la cantidad de infectados detectados acumulados para cada día desde el primer contagio detectado el 03 de marzo (al que llamaré día t = 1 de la muestra en los gráficos), hasta el día 31 de mayo (día t = 90). Hago hincapié en detectados, porque la muestra no refleja la cantidad de infectados reales que existen en la población, sino solamente en aquellos casos testeados que dieron positivo. Graficando dichas cantidades en función de los días, se obtienen los puntos negros del gráfico de la Fig.1, que representé en escala logarítmica para hacer más visibles los detalles.




Fuente de los datos: https://www.argentina.gob.ar/salud/epidemiologia/vigilancia-epidemiologica/reportes-sobre-covid-19-en-argentina








Lo primero que salta a la vista es que hay un quiebre en la muestra que se da entre los días 26 (t = 24) y 27 (t = 25) de marzo, haciendo evidente un aplanamiento de la curva de contagios producto, fundamentalmente, del aislamiento poblacional (cuarentena). La afirmación de que, efectivamente, el aplanamiento se da en esas fechas, será fundada al final de este artículo con argumentos matemáticos.

Interpolando los datos desde t = 1 hasta t = 25 se obtiene la función exponencial E1(t), que si se la deja seguir (extrapolación) como si el quiebre (cuarentena) no existiera, la línea punteada llegaría a 5331 casos contagiados acumulados al 23 de abril (t = 35), fecha en la que se flexibilizó la cuarentena. Sin embargo, interpolando desde dicho quiebre con la función exponencial E2(t), vemos que al 23 de abril llegamos a sólo 1622 casos (basta con reemplazar con una calculadora t=35 en mi fórmula de E2(t), para llegar a ese resultado), muy en acuerdo con el dato dado por el Ministerio de Salud de la Nación para esa fecha, que fue de 1628 casos acumulados.

La conclusión más importante es que gracias a la cuarentena se logró detener el crecimiento un 70% en apenas 10 días, y sostenerse esa tendencia hasta a la baja hasta comenzado el pico. Cabe destacar que en virtud de lo expuesto sobre el enorme crecimiento de estas funciones en muy poco tiempo, un cambio importante en las condiciones de aislamiento, puede disparar la curva a límites indeseados.

Siempre teniendo la precaución de que este análisis no profundiza en cuestiones médicas, o del sistema de salud o sobre ciertas conductas poblacionales que pudieran introducir variables particulares, utilizando la expresión dada por la función exponencial E3(t), uno podría estimar la cantidad aproximada de infectados que acumulará Argentina en una fecha futura dada, reemplazando en la variable t de la misma, la cantidad de días transcurridos desde el 03 de marzo (día t = 1) hasta la fecha elegida. Como aclaré antes, las extrapolaciones no deben ir muy lejos de la muestra porque las fórmulas dejan de tener validez. En este caso en particular, ello se debe a que, como la situación es muy dinámica, naturalmente las condiciones en las que construí las interpolaciones variarán en el tiempo por múltiples razones, y esas variaciones irán acumulando más y más errores cuanto más nos alejemos de esas condiciones iniciales, hasta que llegará un momento en el que las diferencias entre la realidad y lo que predicen mis ecuaciones serán inaceptables desde el punto de vista científico. Usualmente, uno no se excede yendo más allá en días, que los que posee la mitad de la muestra. Con una muestra de uns 65 días, no es recomendable usar, por ejemplo, la ecuación E3(t) más allá de unos 30 días después del 6 de mayo, esto es, no más allá de fines de mayo para ser conservadores.

Para terminar, algo había quedado por justificar: ¿Por qué estamos seguros que la curva se empezó a aplanar, digamos, desde el 27 de marzo? Que se vea a ojo en el gráfico no siempre es confiable y es, en todo caso, muy subjetivo. Pensemos en lo siguiente y demos así una explicación matemática. Un grupo de científicos del Instituto Balseiro, CONICET, CNEA y Universidad del Comahue (https://es-la.facebook.com/cyua.bariloche/) desarrollaron una idea para determinar el punto de inflexión de la curva. Yo le agrego a esa idea dos ajustes lineales que facilitan visualizar los resultados.

Supongamos que en algún hipotético país que no es la Argentina, en los días t = 1, 2, 3, 4, 5, 6 y 7 hubieran habido respectivamente 1, 6, 15, 30, 33, 33, 34 infectados acumulados. Lo que se ve es que, a partir del cuarto día, tendrán casi la misma cantidad de contagiados acumulados (un promedio de poco más de 32 por día). En otras palabras, la cantidad de contagios se frenó, lo cual se ve porque en esos últimos días la cantidad de infectados que suma un día es casi la misma que la que sumaba el día anterior.

Una forma matemática de interpretar ese hecho es teniendo en cuenta algo que todos sabemos y es que si dividimos entre sí dos números muy parecidos, la división nos dará casi 1. O sea que un criterio que puede utilizarse para medir cuándo los contagios empiezan a bajar, es ver desde cuándo la cantidad de contagiados acumulados hasta cierto día, dividida por la cantidad de contagiados acumulados al día anterior nos empieza a dar cerca de 1. De hecho, si los habitantes de ese país fueran muy afortunados y un día tienen la misma cantidad de contagiados acumulados que el día anterior (o sea, no tuvieron ningún infectado nuevo), esa cuenta les dará exactamente 1. Veamos esas divisiones en el caso de ese hipotético país:

6/1 = 6, 15/6 = 2.5, 30/15 = 2, 33/30 = 1.1, 33/33 = 1 y 34/33 = 1.03. Como vemos, la sucesión de cocientes será:

6, 2.5, 2, 1.1, 1, 1.03.

De dicha sucesión podemos inferir que dado que 33/30 = 1.1 es el primer número de la serie donde él y los restantes de la misma se aproximan mucho a 1, es entre los días t = 4 y t = 5 donde la cantidad de infectados nuevos se frena, lo que produce que en ese país la curva se quiebre y comience a aplanarse.

Con esta misma idea, y volviendo a los datos reales de nuestro Ministerio de Salud de la Nación, grafiqué los cocientes entre "días consecutivos vs. los días de la muestra" (Fig.4), y ajusté dos rectas (y1(t) e y2(t)) que interpolan las cruces, donde se ve claramente que a partir del 27 de marzo los cocientes (las cruces) se empiezan a acercar a 1 (ese 1 debe leerse en el eje vertical). De hecho, la sucesión de los cocientes a partir de ese día (t = 25 en la Fig.4), poseen una media (promedio de los valores) de 1.4 para los primeros días antes del quiebre, y de 1.1 -más cercano a 1- para el resto de la muestra.

La gran dispersión (“desparramo”, permítaseme el término) de los datos iniciales (ajustados por y1(t)), se debe a las bruscas variaciones de cantidad de casos detectados acumulados en los primeros días con respecto al siguiente, y claramente, aunque el quiebre existe, esos primeros casos -que podrían excluirse del análisis-, lo exagera y lo deja más en evidencia.



$$
\overline{x} = \frac{\sum x}{n}
$$

$$
\overline{y'} = \frac{\sum y'}{n}
$$

$$
m = \frac{n \left( \sum xy' \right) - \left( \sum x \right) \left( \sum y' \right)}{ \left( \sum x \right)^2 - \left( \sum x^2 \right) }
$$

$$
b' = \overline{y'} -m \overline{x}
$$


