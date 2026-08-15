# **Adamas**
**Infraestructura para la soberanía alimentaria, la economía real, la
coordinación autónoma y las redes descentralizadas.**

#### **Fundemos la web4:**
## Documento de aspectos técnicos
<br>
.
<br>
<br>
<br>


## Resumen ejecutivo

### El problema

2.690 millones de personas — el 32,7% de la humanidad — no pueden costear una dieta saludable.
645 millones enfrentaron hambre en 2025.

El costo de comer bien subió un 46% en ocho años: de 2,94 dólares por persona al día en 2017
a 4,28 en 2025. — FAO et al. (2026). La cifra sigue subiendo.

Un dato que dimensiona la distorsión: el umbral internacional de pobreza extrema está fijado
en 3 dólares diarios, y comer saludablemente cuesta 4,28. Quien está justo por encima de la
línea de pobreza no puede alimentarse bien.

#### La paradoja

El mundo cultiva 5.935 kilocalorías diarias por persona en alimentos directamente comestibles.
Llegan 2.531 a la boca de las personas.

| Etapa | Valor |
|-------|-------|
| Cosecha y suelo | −338 kcal |
| Post-cosecha | −332 kcal |
| Comercio internacional | −73 kcal |
| Biocombustibles | −808 kcal |
| Siembra | −126 kcal |
| Alimentado a animales | −1.738 kcal |
| Devuelto como carne, lácteos y pescado | +594 kcal |
| Procesamiento, distribución y desperdicio | −586 kcal |
| Comido efectivamente | 2.531 kcal |
| Requerimiento medio | 2.353 kcal |
| Excedente real | 178 kcal — 8% |

<small>Fuente: Berners-Lee et al. (2018).</small>

El sistema alimentario mundial produce lo justo. Y produce lo justo porque desvía casi la mitad
de lo comestible a usos que destruyen valor nutricional.

La ganadería con grano es el desvío mayor: consume el equivalente de 5.550 kilocalorías por
persona al día y devuelve 594. Una tasa de conversión del 12%.

En proteína, el efecto es peor: alimentar cultivos comestibles a animales reduce la proteína
disponible en 51 gramos por persona al día — el 116% de lo que toda la humanidad necesita.

El costo no es solo humano: la ganadería ocupa el 77% de la tierra agrícola, aporta solo el 18%
de las calorías y genera el 14,5% de las emisiones globales. Alimentar sin destruir el planeta
requiere coordinar mejor lo que ya existe, no producir más. Adamas es esa infraestructura
de coordinación.

#### La tesis

El problema no es de producción sino de destino, distribución y precio.

Y hay una cifra que lo demuestra: de cada dólar gastado en alimentos, 11,8 centavos llegan
a quien los produjo. Tras descontar sus gastos, le quedan entre 2 y 3 centavos. — USDA
Economic Research Service, (2024).

Los 88,2 centavos restantes son procesamiento, envasado, transporte de larga distancia,
intermediación mayorista y margen comercial de cada eslabón — buena parte de lo cual un
circuito local no necesita.

#### La solución

Adamas es una plataforma de coordinación que permite a las comunidades autogestionar su
economía y gobernanza.

Paga directamente a quien produce, elimina intermediarios, y fija precios por acuerdo
comunitario en lugar de mercado especulativo.

El margen que lo hace posible, calculado: alimentar a 500 personas cuesta 781.000 dólares
anuales a precio de mercado y 125.000 pagando directamente a quienes producen. Un factor de
seis a uno — espacio suficiente para pagar al productor varias veces lo que hoy recibe y
seguir gastando menos.

Su infraestructura combina: gobernanza asamblearia con doble umbral, identidad descentralizada
con unicidad verificable y anónima, moneda social respaldada por producción real, y una red en
malla autónoma que opera sin depender de internet comercial.

<br>
.
<br>
<br>
<br>

### 1. Descripción del proyecto

#### 1.1 Visión y misión

Visión: un mundo donde el acceso a alimentos y recursos básicos no dependa del precio de
mercado sino del acuerdo comunitario y la producción real.

Misión: construir la infraestructura de coordinación que permita a las comunidades
autogestionar su economía y gobernanza, sin intermediarios ni dependencia de infraestructura
externa.


#### 1.2 Arquitectura general
```
┌─────────────────────────────────────────────────────────┐
│  APLICACIÓN — interfaces, foros, red social, traductor  │
├─────────────────────────────────────────────────────────┤
│  GOBERNANZA — asambleas, deliberación por sorteo,       │
│               agenda por canales, identidad             │
├─────────────────────────────────────────────────────────┤
│  ECONOMÍA — moneda social, tesoro, cooperativas,        │
│             detección de concentración                  │
├─────────────────────────────────────────────────────────┤
│  REGISTRO — encadenado con firma de umbral (global)     │
│             + registros distribuidos con CRDTs (local)  │
├─────────────────────────────────────────────────────────┤
│  ALMACENAMIENTO — codificación de borrado, custodia     │
│                   distribuida, verificación periódica   │
├─────────────────────────────────────────────────────────┤
│  RED — LoRa (telegramas), HaLow (contenido),            │
│        BATMAN-adv (enrutamiento en malla)               │
├─────────────────────────────────────────────────────────┤
│  HARDWARE — nodos, antenas, paneles, baterías           │
└─────────────────────────────────────────────────────────┘
```
Capa de gobernanza. Asambleas comunitarias del orden de 150 personas. Doble umbral
asimétrico. Paneles deliberativos por sorteo estratificado. Agenda determinada por cuatro
canales con sorteo puro en cada uno.

Capa económica. Moneda social como registro con respaldo en producción real. Tesoro común
con bienes, infraestructura y cooperativas. Techo de acumulación y piso mínimo por hora.

Capa de registro. Registro encadenado con firma de umbral para lo que exige consenso global
— identidad raíz, tesoro, resultados globales, anclajes de integridad — y registros
distribuidos con convergencia de estado para todo lo demás.

Capa de red. LoRa para telegramas, votos y alertas. Wi-Fi HaLow para transporte de
contenido. BATMAN-adv para enrutamiento auto-reparable. Supernodos comunitarios como
jerarquía blanda — aceleradores, no requisitos.

<br>
.
<br>
<br>
<br>

### 2. PROBLEMA Y SOLUCIÓN

#### 2.1 El flujo alimentario mundial

*Todas las cifras corresponden a Berners-Lee et al. (2018), con datos de 2013 de los balances
alimentarios de la FAO.*

La cuenta de los cultivos: todos los cultivos traducidos a kcal por consumo personal diario:


| Concepto | Valor |
|----------|-------|
| Cultivos directamente comestibles producidos | 5.935 kcal/persona/día |
| Pasto y rastrojo, no digeribles por humanos | 3.812 kcal/persona/día |
| Producción total | 9.747 kcal/persona/día |
| Requerimiento energético medio* | 2.353 kcal/persona/día |
| Alimento efectivamente comido | 2.531 kcal/persona/día |
| Excedente real | 8% |

\* *Promedio global ponderado derivado por los autores aplicando la metodología de la consulta
conjunta de expertos sobre requerimientos energéticos humanos de 2001. No es una cifra
publicada: el documento original proporciona tablas por edad, sexo, peso y actividad física.*

La cuenta de la ganadería:

| Concepto | Valor |
|----------|-------|
| Cultivos comestibles entregados a animales | 1.738 kcal |
| Pasto y rastrojo entregado a animales | 3.812 kcal |
| Total consumido por animales | 5.550 kcal |
| Devuelto como carne, lácteos y pescado | 594 kcal |
| Tasa de conversión | 12% |
        
Y el dato sobre proteína, que es el más contundente del estudio:

| Concepto | Valor |
|----------|-------|
| Proteína comida | 81 g/persona/día |
| Requerimiento medio | 44 g/persona/día |
| Exceso de consumo | 84% |
| Reducción de proteína disponible por alimentar cultivos a animales | 51 g/persona/día — el 116% del requerimiento global |

Los escenarios del propio estudio: dejar de alimentar cultivos comestibles a animales
alcanzaría para alimentar adecuadamente a 9.700 millones de personas en 2050 sin reducir
desperdicio ni consumo excesivo. Seguir la trayectoria proyectada requeriría un 119% más de
producción. Es un dato del que no nos podemos hacer cargo totalmente, pero del que deseamos
su difusión total en el contexto de la discusión presente.

Y la conclusión que los autores enuncian: reducir el desperdicio y aumentar rendimientos son,
en ausencia de aumentos de producción, cuantitativamente menos importantes que reducir los
cultivos comestibles entregados a animales.


#### 2.2 El hambre actual

*Fuente: FAO et al., (2026).*

| Concepto | Valor |
|----------|-------|
| Personas que no pueden costear una dieta saludable | 2.690 millones — 32,7% |
| Personas que enfrentaron hambre | 645 millones — 7,8% |
| Costo de una dieta saludable, 2025 | 4,28 dólares PPA/persona/día |
| El mismo costo en 2021 | 3,44 |
| El mismo costo en 2017 | 2,94 |
| Aumento en ocho años | 46% |
| Población africana sin capacidad de costearla | 66,6% |
| Umbral internacional de pobreza extrema | 3 dólares PPA/día |

El contraste que el propio informe destaca: la línea de pobreza extrema está en 3 dólares y
comer sano cuesta 4,28. La línea de pobreza no mide capacidad de alimentarse bien — mide
capacidad de sobrevivir mal.

#### 2.3 El trabajo del sistema alimentario

*Fuente: FAO, (2025).*

| Concepto | Valor | Cálculo |
|----------|-------|---------|
| Personas empleadas en sistemas agroalimentarios, 2022 | 1.300 millones | |
| Proporción del empleo mundial | Dos de cada cinco personas empleadas | |
| Horas semanales promedio, 81 países, 2023 | 40 | |
| Horas anuales del sistema alimenticio | 2,70 billones | 1.300 M × 40 × 52 |
| Horas por persona al año | 330 | 2,70 billones ÷ 8.200 M (total de la humanidad) |
| Equivalente diario | 0,90 horas | 330 ÷ 365 |

Actualmente el coste de alimentar a toda la humanidad de manera saludable (los estudios de
arriba traducen en calorías la gama completa de la totalidad de los cultivos) se traduce en
que cada persona del mundo trabajase una hora por día. La alimentación diaria de cada persona
correspondería a una hora de trabajo diario. La cifra incluye personas fuera de la capacidad
laboral como niños y ancianos, pero la cifra se considera un indicador de referencia fuerte y
con base y se empleará para futuros cálculos — es un cálculo propio derivado de dos datos
verificados, y no una estadística publicada. Su salvedad principal: el cálculo supone jornada
uniforme, y la fuente advierte que las horas fluctúan con siembra y cosecha. Las horas
efectivas que correspondería por día por persona son probablemente menores, lo que refuerza
el argumento.

Por qué importa: establece que el piso mínimo propuesto — una hora de trabajo vale al menos
una jornada de alimentación — es materialmente alcanzable. No es generosidad: es la
proporción que el sistema ya tiene.

#### 2.4 El factor de eficiencia

*Fuente: USDA Economic Research Service (2024).*

| Concepto | Valor |
|----------|-------|
| Participación del productor en el gasto total en alimentos | 11,8 centavos por dólar |
| Participación en compras de supermercado | 18,5 centavos |
| La misma cifra en 1994 | 24 centavos |
| Lo que queda al productor de cultivos tras gastos | 2,5 centavos |
| Costo de comercialización | 88,2 centavos |

La participación de quien produce se redujo a la mitad en tres décadas.

El cálculo aplicado a una comunidad de 500 personas:

| Concepto | Fórmula | Resultado |
|----------|---------|-----------|
| Costo a precio de mercado | 4,28 × 500 × 365 | 781.000 dólares/año |
| Personas trabajando a tiempo completo | 330 h × 500 ÷ 2.080 h | ≈ 80 |
| Ingreso anual por trabajador | 4,28 × 365 | 1.560 dólares |
| Costo de pagar a quienes producen | 1.560 × 80 | 125.000 dólares/año |
| Factor | 781.000 ÷ 125.000 | ≈ 6 a 1 |

Tres razones lo explican, y ninguna es una eficiencia del proyecto sino una ineficiencia del
sistema actual: no se paga margen comercial de cada eslabón; no se paga el tercio que se
desperdicia y está incorporado al precio; no se paga transporte de larga distancia.

Aun pagando el doble o el triple del piso de subsistencia, el costo seguiría siendo la mitad
o menos que comprar la misma comida.

El supuesto de 80 personas está verificado contra datos de productividad campesina: la
relación de 6,25 personas alimentadas por trabajador cae dentro del rango documentado de 6 a
8 para agricultura de pequeña escala.


#### 2.5 La solución

No se propone producir más excedente, sino que lo producido llegue a las personas.

Pago directo a quien produce, eliminando la intermediación que captura el 88% del precio
final.

Precios fijados por acuerdo comunitario, no por mercado especulativo.

Alimentación entregada como derecho y no vendida — lo que elimina de raíz que alguien deba
trabajar en condiciones degradantes para comer.

Y moneda social como registro con respaldo en producción real, no como activo especulativo.

La soberanía sobre los recursos: Adamas apoya la producción diversificada de proximidad, con
variedades locales, prácticas regenerativas y canales de entrega cortos. La soberanía
alimentaria no se decreta: se construye desde el control de las comunidades sobre sus
tierras, semillas y aguas. ¿Por qué? 1. Porque la capacidad de cultivo de una tierra es
directamente proporcional a la salud de un ecosistema cuyas plantas cuentan con diversidad de
especies nativas. 2. Porque la calidad nutricional de los cultivos crece de forma igualmente
proporcional a la afirmación anterior. La ética es un valor importante para el objeto de este
estudio, pero se argumentará con las cifras pertinentes.

La infraestructura: combina un registro encadenado con firma de umbral, registros
distribuidos con CRDTs y una red de comunicación autónoma (LoRa + HaLow + BATMAN). Adamas no
es una app sobre una red centralizada: es una infraestructura que construye su propia red y
su propio registro.

La propuesta integrada: el sistema cierra el círculo desde el problema (producción
suficiente, mal distribuida) hasta la solución (pago directo, acuerdo comunitario, red
autónoma, gobernanza asamblearia, circularidad económica y social, y moneda social con
respaldo real). No hay piezas sueltas: cada capa responde a una distorsión del sistema
actual.

<br>
.
<br>
<br>
<br>

### 3. PROPUESTA TÉCNICA

#### 3.1 Gobernanza

Asambleas barriales o zonales del orden de 150 personas, con autonomía plena sobre sus
asuntos — la autodeterminación es relevante en la organización, es una cifra en la que
organización no se complica. El entramado de organizaciones es lo que marcará la diferencia.

Doble umbral asimétrico para decisiones supralocales, con salvaguardas contra la
fragmentación artificial de zonas.

Paneles deliberativos por sorteo estratificado, con invitación aleatoria amplia y selección
entre quienes aceptan. Compensación equivalente al costo de subsistencia del período dedicado
— no como beneficio sino como condición de representatividad.

Agenda por cuatro canales: sorteo puro sobre el 60% de las plazas, cola de antigüedad
determinista sobre el 20%, y 10% para zonas desatendidas y urgencias respectivamente. Con
semilla generada por compromiso previo entre partes independientes, de modo que nadie pueda
elegir el resultado.

Custodios en tres niveles independientes — global, regional, local — con firma de umbral,
selección por sorteo estratificado y rotación parcial escalonada.

**Un posible pilar permanente de la autogobernanza: AdmsDID**

AdmsDID es un sistema de identidad descentralizada que permite a cada persona demostrar que
es una sola persona sin revelar cuál, y sin recurrir a credenciales estatales.

Opera en dos capas: una identidad raíz que nunca aparece en transacciones, y derivaciones por
contexto que impiden actuar dos veces en un mismo ámbito — votar dos veces, cobrar dos veces,
acumular más allá del techo — sin permitir vincular las actuaciones de alguien entre ámbitos
distintos. La verificación de atributos se realiza mediante pruebas de conocimiento cero: el
sistema sabe que cumples las condiciones, no quién eres.

AdmsDID resuelve la tensión central de la participación de soberanía horizontal: demostrar
que eres una sola persona sin revelar cuál.

En un sistema donde cada persona tiene un voto y cada persona participa en la economía, el
problema no es la identidad — es la unicidad.

En gobernanza: participación verificable y anónima, sin dependencia de credenciales
estatales, sin exposición de datos personales, y sin posibilidad de duplicación.

En economía: cada persona es una sola en el registro de saldos, nadie puede eludir el techo
de acumulación con identidades múltiples, y la moneda social refleja trabajo y producción
reales, no identidades ficticias. La privacidad de las transacciones no es un obstáculo para
la equidad; es su condición.

El problema no es la identidad sino la unicidad, y conviene enunciarlo con precisión: para
impedir que una persona se inscriba dos veces hay que comparar su registro contra los
existentes — y esa comparación es exactamente lo que el anonimato parecería impedir. El
anonimato en las votaciones globales importa el doble porque impide o desvirtúa la
comprobación de compra de voto; el tema es que sin un mecanismo que impida el registro
múltiple, tanto el voto comunitario como la distribución de moneda social son vulnerables a
duplicación. Sin credenciales externas, la participación queda fuera del alcance de quienes
no tienen documentos o no quieren exponerlos. Y no nos confiamos de los registros de los
estados; no abordaremos los motivos de la desconfianza: están a vista de todos, mencionaremos
sí que consideramos las credenciales verificables de los estados como una brecha de seguridad
y comprendemos que el uso que les dan los estados carece de toda ética.

Existe una implementación de referencia que resuelve la tensión de la
duplicación/deduplicación: Janus, presentado en el IEEE Symposium on Security and Privacy de
2024 y desarrollado por el centro CISPA junto al grupo SPRING de la École Polytechnique
Fédérale de Lausanne y el Comité Internacional de la Cruz Roja. Su código es abierto y fue
diseñado para deduplicación biométrica que preserva la privacidad en programas de
identificación humanitaria — Edalatnejad et al. (2024). Antes de continuar, se hace aviso que
este texto se opone a la biometría invasiva, en particular la del registro ocular; si surge un
afianzamiento por necesidad a la biometría, debe ser un registro generado por las personas
libres para las personas libres, a voluntad decidida.

Janus permite comparar un registro contra un conjunto sin que ninguna parte pueda leer su
contenido. El cómputo se reparte entre múltiples custodios y devuelve un solo bit: hay
coincidencia o no la hay.

Sobre eso el proyecto agrega una decisión arquitectónica propia: el corpus federado por
regiones.

Janus resuelve la comparación privada; acotar el ámbito de comparación es lo que hace
tratable el problema de escala. Un registro biométrico planetario único no es viable con
ninguna tecnología disponible — la tasa de casos ambiguos crece con el tamaño del conjunto
hasta volverse complejo, aunque la formulación de uso de biometrías poco invasivas y
sumativas (acumulativas) elimina la mayor parte de ellos — proponemos que nos enseñemos 
las manos: registros de venas palmares mediante detector, más huellas digitales, en 
conjunto a la necesaria presencialidad abierta de libre asistencia comunitaria del registro,
y una complementariedad de biometría en casos de falta para evitar sesgos capacitistas. 
Con corpus regionales y consulta cifrada entre regiones, el número vuelve a ser tratable 
por revisión humana.

Una precisión terminológica que conviene fijar: el corpus existe y es comparable — esa es su
función. Lo que no existe es un corpus legible por una sola parte. La distinción no es entre
tener registro y no tenerlo, sino entre uno que un actor individual puede leer y uno que
ninguna parte puede leer sola.

En etapas tempranas la unicidad — aproximación a la unicidad — se sostiene por otra vía:
inscripción en eventos públicos con verificación cruzada entre comunidades vecinas, muestreo
aleatorio de padrones, y el conocimiento que cada asamblea tiene de sus propios miembros. Es
menos preciso y es lo que funciona sin infraestructura, a cargo de la voluntad de las
personas.

Y una decisión que conviene declarar: el sistema no depende de la unicidad verificada para
operar. Las zonas que no puedan desplegar la infraestructura del corpus federado son
previsiblemente las más vulnerables — hacerla requisito de participación las excluiría.

Salvedad declarada: la evaluación documentada de Janus corresponde a programas del orden de
decenas o cientos de miles de personas. Las estadísticas muestran que es viable sin embargo.

#### 3.2 Economía

Moneda social: registro, no activo especulable. No cotiza en ningún mercado, no es adquirible
fuera del sistema, y su valor no flota según expectativas.

Su respaldo es capacidad productiva existente — tierra, infraestructura, cooperativas
(+cooperativas de destinación social del tesoro). No una promesa de conversión.

Y de ahí una propiedad que ningún respaldo monetario tiene: no puede ser corrida. Nadie puede
exigir que se convierta toda a otra cosa, porque no es un derecho de cobro sino el medio de
intercambio de una economía que produce.

El tesoro común opera como puente hacia el exterior. Compra afuera con sus reservas, vende
afuera lo que produce, y acredita adentro. No hay contrato verificador ni mecanismo de
conversión entre registros — hay una entidad que transacciona en ambos mundos.

Techo de acumulación de aire o fijado, con aviso escalonado, no erosión: quien excede el
umbral recibe avisos con plazo inversamente proporcional al monto, y el excedente inmóvil
retorna al fondo para reinversión trazable. Queda a cargo del detector — bajo el ajuste fino
asistido necesario para las primeras etapas — el decidir el momento en el que la economía
debe enviar avisos de umbral.

Detección de concentración por aritmética con parámetros fijos. Sin aprendizaje automático,
sin redes neuronales.

#### 3.2.1 Del Tesoro: bienes, billetera y las dos etapas de Adamas

El Tesoro no es un fondo abstracto: es patrimonio físico y digital.

Por un lado, bienes físicos — tierra, infraestructura, cooperativas sociales, maquinaria,
existencias — que constituyen la base productiva del sistema. Son la garantía real de que la
moneda social no es una promesa, sino el reflejo de una economía que produce.

Por otro lado, una billetera de inversión — activos digitales, fiat y reservas líquidas — que
permite al Tesoro operar en el mundo exterior: comprar tecnología, insumos, y todo aquello
que el circuito no produce, sin necesidad de puentes ni exposición de la moneda social a la
volatilidad externa.

Esa dualidad es la que hace posible el modelo de dos etapas.

Etapa 1: crecimiento y construcción

El Tesoro concentra la toma de decisiones, la gestión de reservas y la coordinación de
cooperativas. Es la etapa de inversión inicial, de ajuste fino de parámetros — tasa de
conversión, techos de acumulación, piso mínimo por hora — y de despliegue de infraestructura.
Sin esta etapa centralizada no hay economía que sostener: una moneda que no compra nada no
vale nada, y un circuito sin oferta interna no circula.

El ajuste fino es aquí una tarea continua: la tasa de conversión se revisa periódicamente,
los techos se calibran según la producción real, y los parámetros económicos se adaptan a la
experiencia de las primeras comunidades. No es improvisación: es aprendizaje antes de
escalar.

Los ajustes del fondo deben desligarse del tesoro y automatizarse mediante aritmética y el
detector, de manera paulatina y creciente.

Etapa 2: autonomía y traspaso

Cuando el sistema alcanza un nivel elevado de participantes, cuando la economía interna es
autónoma y estable, y/o cuando AdmsDID garantiza que cada persona es una sola sin revelar su
identidad, el Tesoro transfiere su función principal a la comunidad.

El traspaso no es una renuncia: es la condición de madurez del sistema, y en su traspaso se
considerarán varios factores como las votaciones de las comunidades, el número de
participantes necesarios para una economía sana, la implementación voluntaria de AdmsDID.

La gobernanza de los parámetros económicos pasa a la asamblea. La gestión del Tesoro se
distribuye entre custodios. La moneda social deja de ser administrada y pasa a ser gobernada.
El Tesoro se convierte entonces en un patrimonio común sin dueño — tierra, infraestructura y
cooperativas de destinación social — que la comunidad administra colectivamente.

El ajuste fino, en esta etapa, ya no es necesario: la economía se regula por el acuerdo entre
pares, no por la calibración de un administrador central.

AdmsDID es un protocolo que haría posible y fácil este tránsito. Sin identidad única y
verificable, el voto comunitario sería vulnerable a duplicaciones. Sin pruebas de conocimiento
cero, la soberanía de los participantes sería nominal. Con AdmsDID, la comunidad puede
decidir globalmente; sin AdmsDID, la organización está forzada a ser regional, aunque se han
tomado medidas paliativas en este ámbito también.

#### 3.2.2 Detector

El detector es un sistema de monitoreo aritmético, no un sistema de vigilancia.

No observa personas ni contenido. Observa flujos de moneda social en el registro. No sabe
quién es quién. Solo sabe cuánto se mueve, entre qué cuentas y con qué patrón.

Su función es detectar concentración anómala y ataques de liberación masiva multicuenta, sin
necesidad de vigilancia humana ni aprendizaje automático.

Distingue entre una compra masiva legítima — patrón estacional, cuentas con historial de
aportes, fondos que circulan dentro del circuito — y un ataque — cuentas recién creadas sin
historial, fondos que se concentran en pocos receptores o salen del circuito hacia conversión
externa.

El detector solo señala anomalías. No decide nada. La decisión es siempre de la comunidad.

#### 3.3 Redes

LoRa: capa telegramática. Votos, huellas criptográficas, alertas. De 2 a 5 kilómetros en
entorno urbano, decenas en línea de vista. Un voto firmado cabe en menos de un kilobyte.

Wi-Fi HaLow: transporte de contenido. 800 metros con línea de vista según mediciones de
campo. La discrepancia con las cifras publicadas por fabricantes está registrada como
pendiente de verificación en terreno.

BATMAN-adv: enrutamiento en malla, capa 2, auto-reparable, en producción durante más de una
década.

Supernodos comunitarios como jerarquía blanda — aceleran la red sin ser requisito para su
funcionamiento.

Convergencia de estado sin conflicto para operación en red particionada: los nodos convergen
al reconectarse sin necesidad de consenso.

#### 3.4 Programación

Núcleo en Rust: identidad, criptografía poscuántica, verificación, convergencia de estado,
protocolo.

El criterio de separación: al núcleo va lo que maneja secretos y lo que debe correr en todas
las plataformas. Un error de memoria en la interfaz cierra la aplicación; en la capa
criptográfica filtra una clave.

Periféricos en lo que ya funciona probado: enrutamiento en C, firmware de radio en C++,
interfaces en el lenguaje nativo de cada plataforma.

Registro encadenado, no marco de cadena externo. Se evaluaron marcos con arquitectura de
cadena principal y se descartan: exigen alquilar espacio con costo permanente en moneda
ajena, operan con validadores que no son propios, y su gobernanza es por participación
económica — lo que contradice el principio de una persona un voto.

Construcción reproducible obligatoria desde el inicio. El mismo código debe producir el mismo
binario, verificable por cualquiera.

#### 3.5 Seguridad

Sin puentes entre cadenas. Es la decisión de seguridad más importante del diseño: los puentes
concentraron el 69% de lo robado del sector en 2022, y el mayor incidente de 2026 — 292
millones de dólares — ocurrió por un esquema de verificación con quórum de uno sobre uno
(Chainalysis, 2022; Blockonomi, 2026; Gate News, 2026).

Firmas de umbral con generación distribuida de claves para decisiones críticas. Ninguna parte
individual puede autorizar nada.

Recuperación de identidad por tres vías concurrentes: fragmentación de clave entre guardianes
elegidos, frase de respaldo, y reenrolamiento asambleario.

Refresco frecuente de fragmentos, rotación infrecuente de personas. El refresco invalida
fragmentos comprometidos sin exponer al sistema al momento de mayor vulnerabilidad, que es la
renovación completa del conjunto.

Actualización de nodos firmada por umbral, distribuida por la propia malla, con verificación
antes de aplicar, capacidad de revertir y despliegue escalonado. Sin actualización silenciosa
— es la lección directa del historial de extensiones maliciosas, donde el vector principal no
fue la instalación sino la actualización automática.

Y el dato que ordena las prioridades de seguridad: el 88% de las pérdidas del sector en 2025
provino de compromiso de claves privadas, no de errores de código (Chainalysis, 2025). Un caso
perdió 285 millones tras seis meses de ingeniería social (Blockonomi, 2025; COINTURK News,
2025; Lekati, 2026). No hubo exploit: hubo paciencia (Lekati, 2026).

<br>
.
<br>
<br>
<br>


### 4. Hoja de ruta

Fase 1 — seis meses. Prototipo funcional de gobernanza asamblearia y registro de moneda
social. Nodos LoRa operativos en una comunidad piloto. Verificación en terreno del alcance
real de HaLow.

Fase 2 — doce meses. Despliegue en un par campo-ciudad. Primeras cooperativas operando antes
de liberar la moneda social — una moneda que no compra nada no vale nada. Circuito
alimentario en funcionamiento.

Fase 3 — veinticuatro meses. Escalado a red regional. Registro encadenado operativo con
custodios en tres niveles. Integración con AirNodes donde exista cobertura.

Fase 4 — treinta y seis meses. Red multinacional. La escala mínima viable es de varios países
con complementariedad productiva — ningún país tiene superficie calórica suficiente para su
propia población.

Y una precisión sobre el orden que conviene declarar: el primer despliegue no debe ser una
comunidad rural aislada. Una comunidad sola no tiene con quién intercambiar y su moneda queda
inmovilizada. Debe ser un par campo-ciudad desde el inicio.

<br>
.
<br>
<br>
<br>

### 5. Presupuestos e hitos

#### 5.1 Costo anual de la plataforma en etapa inicial operativa

*Todos los componentes son supuestos de diseño y no datos de operación. Las compensaciones
están calculadas al mínimo de subsistencia.*

| Concepto | Cálculo | Dólares/año |
|----------|---------|-------------|
| Custodia de 20 supernodos | 20 × 40 × 12 | 9.600 |
| Custodia de 50 nodos históricos | 50 × 15 × 12 | 9.000 |
| Deliberación, 10 paneles anuales | 10 × 20 × 18 días × 4,28 | 15.410 |
| Desarrollo, 5 personas | 5 × 800 × 12 | 48.000 |
| Infraestructura no personal | Conectividad, energía, reposición | 12.000 |
| **Total** | | **94.010** |

El desarrollo es la mitad del costo y no escala con participantes — cuesta lo mismo con 600
usuarios que con 60.000.

#### 5.2 Autosuficiencia

| Paso | Cálculo | Resultado |
|------|---------|-----------|
| Volumen que genera un participante | 1.560 × 5 vueltas de circulación | 7.800 |
| Comisión al fondo, 1%* | 7.800 × 0,01 | 78 |
| Participantes necesarios | 94.010 ÷ 78 | ≈ 1.205 |

*Meramente un cálculo referencial, se pretenden comisiones menores.*

Con unas 600 personas activas, la plataforma se paga sola. En el escenario pesimista —
comisión baja y circulación lenta — hacen falta unas 2.000.

El supuesto más frágil son las cinco vueltas de circulación, que dependen de que exista
oferta interna. En etapa inicial habrá poco.

#### 5.3 Capital del circuito alimentario

| Modelo | Capital | Por persona alimentada, una vez |
|--------|---------|--------------------------------|
| Arrendamiento de tierra | 15–25 millones | 230–380 dólares |
| Adquisición de tierra | 150–250 millones | 2.300–3.800 dólares |

Solo la adquisición en el tesoro construye patrimonio común global. El arrendamiento paga
renta a quien tiene la tierra.

Referencia: una operación de 10.000 hectáreas alimenta a entre 50.000 y 80.000 personas si su
producción se destina a consumo humano directo, con 30 a 50 trabajadores.

#### 5.4 Monto mínimo solicitado y su desglose

Se solicita 150.000 dólares para doce meses, correspondientes a la Fase 1 completa y el
arranque de la Fase 2.

#### Diseño para 200 personas, 20 nodos comunitarios

Un nodo cada diez personas. Los nodos multiuso no son radios simples: combinan comunicación,
almacenamiento local, punto de acceso inalámbrico y energía autónoma.

#### Nodos comunitarios multiuso - 20 unidades

| Componente | Costo $ |
|-----------|---------|
| Computadora de placa única, 4 GB | 70 |
| Almacenamiento, tarjeta industrial o unidad sólida 256 GB | 30 |
| Módulo LoRa con placa base | 59 |
| Antena exterior 5 dBi con cable | 35 |
| Panel solar 20 W, batería 20 Ah, controlador | 100 |
| Caja estanca IP67 | 25 |
| Montaje, cableado, misceláneos | 20 |
| **Subtotal por nodo** | **339** |
| **20 nodos** | **6.780** |
 
#### Supernodos comunitarios - 3 unidades

| Componente | Costo $ |
|-----------|---------|
| Computadora de mayor capacidad | 500 |
| Almacenamiento 2 TB | 120 |
| Radio HaLow con antena direccional | 200 |
| Pasarela LoRa | 59 |
| Panel solar 100 W, batería 100 Ah, controlador | 400 |
| Gabinete, protección eléctrica | 140 |
| **Subtotal por supernodo** | **1.419** |
| **3 supernodos** | **4.257** |

#### Nodo histórico de archivo - 1 unidad

| Componente | Costo $ |
|-----------|---------|
| Equipo con mayor capacidad de cómputo | 800 |
| Almacenamiento redundante, 2 × 4 TB | 300 |
| Energía autónoma ampliada | 450 |
| Protección y respaldo | 120 |
| **Subtotal** | **1.470** |

#### Complementos

| Concepto | Precio |
|----------|--------|
| Repetidores HaLow solares, 2 unidades | 500 |
| Nodos portátiles para quienes no tienen teléfono, 20 unidades | 1.000 |
| Herramientas de instalación y medición | 300 |
| Repuestos, 15% del hardware | 270 |
| **Total** | **1.530** |

#### Total hardware

| Concepto | Monto |
|----------|-------|
| Hardware | 14.037 |
| Envío e importación, ~25% | 3.509 |
| **Total** | **17.546** |

*Queda dentro de los 20.000 con margen de unos 2.400 dólares.

#### Infraestructura y operación 

| Concepto | Monto |
|----------|-------|
| Conectividad de enlace, 12 meses | 600 |
| Servicios de desarrollo y dominios | 1.200 |
| Reposición por fallas de campo | 2.500 |
| Transporte e instalación en terreno | 3.000 |
| Capacitación de operadores locales | 2.000 |
| Herramientas de mantenimiento | 1.500 |
| Energía de respaldo | 500 |
| Contingencia de campo | 1.000 |
| Imprevistos | 1.700 |
| **Total** | **14.000** |

#### Anexo: cifras de escalabilidad

| Indicador | Valor |
|-----------|-------|
| Costo de red por persona, primera zona | 95 dólares |
| Costo marginal por persona adicional en la misma zona | ~34 dólares |
| Costo por nodo comunitario multiuso | 339 dólares |

*La diferencia entre ambas cifras es lo que importa para escalar.*

*Los 95 dólares incluyen supernodos y archivo, que son costo fijo de la zona. Duplicar la
población de esa zona no duplica el costo: solo agrega nodos comunitarios, a 339 dólares cada
diez personas.*

*Con 2.000 personas en la misma zona, el costo por persona caería a unos 45 dólares.*

| Concepto | Monto | Detalle |
|----------|-------|---------|
| Dirección de proyecto | 24.000 | 2.000 mensuales, dedicación completa |
| Desarrollo del núcleo | 192.000 | Dos personas, 8.000 mensuales cada una |
| Hardware para piloto | 20.000 | Nodos LoRa, HaLow, supernodos, energía |
| Infraestructura y operación | 14.000 | Conectividad, servicios, reposición |
| Reserva | 20.000 | Imprevistos generales |
| Redondeo | –20.000 | |
| **Total** | **250.000** | |

La estrategia es prueba antes de escalar. El desarrollo completo del sistema requeriría mucho
más, pero se espera conseguir algún grado de circularidad, o realizar más postulaciones con
prueba de dispositivo.

Este monto cubre lo que permite demostrar que el mecanismo funciona: un prototipo operativo
de gobernanza asamblearia y registro de moneda social, con nodos desplegados en una comunidad
piloto y verificación en terreno de los supuestos de red. El plazo calculado es durante un
año.

Sobre la eliminación de costos de cadena externa. El descarte de marcos con arquitectura de
cadena principal elimina los costos recurrentes de alquiler de espacio y validadores, y
aumenta el trabajo de desarrollo porque el registro encadenado debe construirse. Los dos
efectos se compensan aproximadamente en este horizonte.

| Categoría | Monto | Detalle |
|-----------|-------|---------|
| Desarrollo de software | 540.000 | 3 años, creciendo de 2 a 5 desarrolladores |
| Dirección y coordinación del proyecto | 108.000 | 3 años |
| Hardware de red, tres regiones | 180.000 | ~60.000 por región: supernodos, nodos de acceso, nodos de archivo, antenas, solar |
| Adquisición de tierra productiva | 1.200.000 | Entra al tesoro de forma permanente y nunca se revende |
| Equipamiento agrícola y logística | 400.000 | Maquinaria, transporte, almacenamiento, cadena de frío |
| Capital de trabajo, circuito alimentario | 450.000 | Primer ciclo productivo, que por definición no puede autofinanciarse |
| Financiamiento semilla para cooperativas | 200.000 | Cooperativas no alimentarias — reparación, herramientas, textiles, construcción |
| Auditorías de seguridad | 60.000 | Criptografía, firmas de umbral, compilaciones reproducibles |
| Estructura legal y jurisdiccional | 40.000 | Creación de entidad en tres jurisdicciones |
| Contingencia | 22.000 | |
| **Total** | **3.200.000** | |


#### 5.5 Hitos medibles

| Fase | Mes | Hito verificable |
|------|-----|------------------|
| 1 | 3 | Registro de identidad operativo en entorno de prueba |
| 1 | 6 | Prototipo funcional: asamblea, votación y registro de saldos |
| 2 | 9 | Nodos LoRa desplegados y operativos en comunidad piloto |
| 2 | 12 | Medición en terreno del alcance real de HaLow |
| 2 | 12 | Primeras cooperativas operando antes de liberar moneda social |

Cada hito es verificable por terceros, no por declaración propia.

<br>
.
<br>
<br>
<br>

### Anexos

#### Anexo A --- Arquitectura del sistema

### 

#### A.1 Capas
```
┌───────────────────────────────────────────────────────────┐
│  APLICACIÓN                                               │
│  Interfaces · Foros · Red social · Traductor              │
├───────────────────────────────────────────────────────────┤
│  GOBERNANZA                                               │
│  AdmsDID · Asambleas · Deliberación por sorteo            │
│  Agenda por canales · Doble umbral asimétrico             │
├───────────────────────────────────────────────────────────┤
│  ECONOMÍA                                                 │
│  Moneda social · Tesoro común · Cooperativas              │
│  Detección de concentración · Piso mínimo por hora        │
├───────────────────────────────────────────────────────────┤
│  REGISTRO                                                 │
│  Encadenado con firma de umbral (consenso global)         │
│  Registros distribuidos con CRDTs (estado local)          │
├───────────────────────────────────────────────────────────┤
│  ALMACENAMIENTO                                           │
│  Codificación de borrado · Custodia distribuida           │
│  Verificación criptográfica periódica                     │
├───────────────────────────────────────────────────────────┤
│  RED                                                      │
│  LoRa (telegramas) · HaLow (contenido)                    │
│  BATMAN-adv (enrutamiento en malla)                       │
├───────────────────────────────────────────────────────────┤
│  HARDWARE                                                 │
│  Nodos · Antenas · Paneles solares · Baterías             │
└───────────────────────────────────────────────────────────┘

```

#### A.2 Jerarquía de nodos

```
                    ┌──────────────────┐
                    │  NODO HISTÓRICO  │
                    │  Custodia de     │
                    │  archivo         │
                    └────────┬─────────┘
                             │
              ┌──────────────┴──────────────┐
              │                             │
     ┌────────▼─────────┐         ┌─────────▼────────┐
     │   SUPERNODO      │◄───────►│   SUPERNODO      │
     │   COMUNITARIO    │  HaLow  │   COMUNITARIO    │
     │                  │         │                  │
     │ Almacenamiento   │         │ Almacenamiento   │
     │ Traductor        │         │ Traductor        │
     │ Enrutamiento     │         │ Enrutamiento     │
     └────┬────────┬────┘         └────┬─────────────┘
          │        │                   │
      LoRa│    WiFi│               LoRa│
          │        │                   │
    ┌─────▼──┐  ┌──▼─────┐       ┌─────▼──┐
    │ NODO   │  │ NODO   │       │ NODO   │
    │ ACCESO │  │ ACCESO │       │ ACCESO │
    └────────┘  └────────┘       └────────┘
       │              │
   ┌───▼───┐     ┌────▼───┐
   │Persona│     │Persona │
   └───────┘     └────────┘
```

La jerarquía es blanda: los supernodos aceleran la red, no son requisito para su
funcionamiento. Si un supernodo cae, los nodos deacceso siguen comunicándose entre sí.

#### 

#### A.3 Flujo del circuito económico

```
   CAPITAL EXTERNO
   (aportes, venta de producción, compras de MS)
          │
          ▼
   ┌─────────────┐
   │   TESORO    │  Reservas externas + bienes + cooperativas
   │             │  Firma de umbral · Transparencia total
   └──┬───────┬──┘
      │       │
      │       └──────────► COMPRA AFUERA
      │                    (tecnología, maquinaria, insumos)
      ▼
   PAGA EN MONEDA SOCIAL
   a quienes producen, transportan,
   acopian y custodian nodos
      │
      ▼
   ┌──────────────────────────────────┐
   │  CIRCUITO INTERNO                │
   │                                  │
   │  Personas ──gastan──► Cooperativas
   │     ▲                      │     │
   │     │                      │     │
   │     └───pagan trabajo──────┘     │
   │                                  │
   │  Cada intercambio deja comisión ─┼──► FONDO
   └──────────────────────────────────┘
      │
      ▼
   ALIMENTO ENTREGADO
   (no vendido — es derecho, no mercancía)
```

```
### A.4 Integración inicial con World Mobile


   ┌─────────────────────┐         ┌──────────────────────┐
   │   WORLD MOBILE      │         │      ADAMAS          │
   │                     │         │                      │
   │  ┌───────────┐      │         │   ┌──────────────┐   │
   │  │ AirNodes  │──────┼─────────┼──►│ Usuarios     │   │
   │  │           │ conectividad   │   │ con acceso   │   │
   │  └───────────┘      │         │   └──────────────┘   │
   │                     │         │                      │
   │  ┌───────────┐      │         │   ┌──────────────┐   │
   │  │ EarthNodes│──────┼─────────┼──►│ Caché        │   │
   │  │           │ cómputo auxiliar│  │ Indexación   │   │
   │  └───────────┘      │         │   └──────────────┘   │
   │                     │         │                      │
   │  ┌───────────┐      │         │   ┌──────────────┐   │
   │  │  WMTX     │──────┼─────────┼──►│ Tesoro       │   │
   │  │           │  compra posible│   │ (reservas)   │   │
   │  └───────────┘      │         │   └──────────────┘   │
   │                     │         │                      │
   │  ┌───────────┐      │         │   ┌──────────────┐   │
   │  │ Usuarios  │◄─────┼─────────┼───│ Red en malla │   │
   │  │ sin       │ comunicación   │   │ LoRa + HaLow │   │
   │  │ cobertura │ autónoma       │   └──────────────┘   │
   │  └───────────┘      │         │                      │
   └─────────────────────┘         └──────────────────────┘

* Sin puentes entre registros*

* Sin validación cruzada*

* Sin custodia delegada*
```


* Cada red funciona sin la otra...pero juntas funcionan mucho mejor.*


<br>
<br> 

#### Anexo B --- Tablas de datos 

#### Tablas del cuerpo de texto y anexas

#### B.1 El flujo alimentario mundial

| Concepto | Valor |
|----------|-------|
| Total consumido por animales | 5.550 kcal/persona/día |
| Devuelto a la cadena humana | 594 kcal/persona/día |
| Tasa de conversión | 12% |


Proteína:

| Concepto | Valor |
|----------|-------|
| Proteína comida | 81 g/persona/día |
| Requerimiento medio recomendado | 44 g/persona/día |
| Exceso de consumo | 84% |
| Reducción de proteína disponible por alimentar cultivos a animales | 51 g — 116% del requerimiento global |


#### B.2 Hambre y costo de la alimentación

| Concepto | Valor |
|----------|-------|
| Personas que no pueden costear dieta saludable | 2.690 millones — 32,7% |
| Personas que enfrentaron hambre en 2025 | 645 millones — 7,8% |
| Costo de dieta saludable, 2025 | 4,28 dólares PPA/persona/día |
| El mismo costo en 2021 | 3,44 |
| El mismo costo en 2017 | 2,94 |
| Aumento en ocho años | 46% |
| Umbral internacional de pobreza extrema | 3 dólares PPA/día |
| Población africana sin capacidad de costearla | 66,6% |


#### B.3 Trabajo del sistema alimentario

| Concepto | Valor | Estado |
|----------|-------|--------|
| Personas en sistemas agroalimentarios, 2022 | 1.300 millones | Verificado |
| Proporción del empleo mundial | Dos de cada cinco | Verificado |
| Horas semanales promedio, 81 países | 40 | Verificado |
| Horas anuales del sistema | 2,70 billones | Cálculo |
| Horas por persona al año | 330 | Cálculo |
| Equivalente diario | 0,90 horas | Cálculo |


#### B.4 Participación del productor en el precio

| Concepto | Valor |
|----------|-------|
| Participación en el gasto total en alimentos, 2024 | 11,8 centavos por dólar |
| Participación en compras de supermercado | 18,5 centavos |
| La misma cifra en 1994 | 24 centavos |
| Lo que queda al productor de cultivos tras gastos | 2,5 centavos |
| Costo de comercialización | 88,2 centavos |
  

#### B.5 El factor de eficiencia

| Concepto | Fórmula | Resultado |
|----------|---------|-----------|
| Costo a precio de mercado, 500 personas | 4,28 × 500 × 365 | 781.000 dólares/año |
| Personas trabajando a tiempo completo | 330 h × 500 ÷ 2.080 h | ≈ 80 |
| Ingreso anual por trabajador | 4,28 × 365 | 1.560 dólares |
| Costo de pagar a quienes producen | 1.560 × 80 | 125.000 dólares/año |
| Factor | 781.000 ÷ 125.000 | ≈ 6 a 1 |

#### B.6 Escala industrial

| Parámetro | Valor |
|-----------|-------|
| Superficie de referencia | 10.000 hectáreas |
| Personas trabajando | 30 a 50 |
| Personas alimentadas, consumo humano directo | 50.000 a 80.000 |
| Personas alimentadas, modelo actual | 15.000 a 25.000 |
| Calorías que llegan a seres humanos | 30 a 40% |

#### B.7 Precedentes de falla en seguridad

| Concepto | Valor |
|----------|-------|
| Proporción de lo robado en puentes entre cadenas, 2022 | 69% |
| Mayor pérdida por puente, 2026 | 292 millones de dólares |
| Proporción de pérdidas por compromiso de claves, no por errores de código | 88% |
| Pérdida por ingeniería social sostenida seis meses | 285 millones |
| Colapso de mecanismo algorítmico de estabilización, 2022 | ≈ 40.000 millones |

<br>
.
<br>
<br>

### --- Glosario

AdmsDID ---     Sistema de identidad descentralizada del proyecto.
                                Permite demostrar que se es una sola persona sin revelar cuál y sin
                                recurrir a credenciales estatales.              

AirNode ---     Punto de acceso a internet de la red World Mobile.

BATMAN-adv ---  Protocolo de enrutamiento en malla que opera en capa
                                2 y se repara automáticamente ante caída de nodos. En producción durante
                                más de una década.

Codificación de borrado --- Técnica que divide un archivo en
                                                        fragmentos con redundancia matemática, de modo que baste recuperar una
                                                        fracción para reconstruirlo íntegro. Más eficiente que replicar copias
                                                        completas.

CRDT --- *Conflict-free Replicated Data Type*. Estructura de datos
                 que permite que múltiples copias converjan al mismo estado sin necesidad
                 de coordinación ni consenso. Es lo que permite operar en red
             particionada.

Custodio --- Persona o entidad que conserva un fragmento de clave
                     criptográfica. Ninguno puede firmar solo.

DID --- *Decentralized Identifier*. Identificador que no depende de
                 una autoridad emisora.

EarthNode --- Nodo de validación y coordinación de la red World
                          Mobile.

Firma de umbral --- Esquema donde la clave se reparte entre
                                        múltiples custodios y se requiere un número mínimo de ellos
                                        para firmar. La clave completa nunca existe en ningún lugar.

Janus --- Protocolo de deduplicación biométrica que preserva la
                  privacidad. Permite comparar un registro contra un conjunto sin que
                  ninguna parte pueda leer su contenido; devuelve un solo bit.

LoRa --- Tecnología de radio de largo alcance y muy baja tasa de
                 transmisión. Adecuada para mensajes cortos a decenas de kilómetros con
                 consumo mínimo.

Moneda Social = MS--- Unidad de intercambio del circuito interno.
                                          No cotiza, no es adquirible fuera del sistema, no se multiplica sola, y
                                          no compra lo esencial.

Nulificador --- Valor derivado de una identidad que impide actuar
                                dos veces en un mismo ámbito sin revelar de quién se trata ni permitir
                                vincular ámbitos distintos.

Piso mínimo por hora --- Valor por debajo del cual ninguna hora de
                                                 trabajo puede acordarse dentro del sistema.

Prueba de conocimiento cero (ZK) - Método criptográfico que
                                                                   permite demostrar que se cumple una condición sin revelar la información
                                                                   que la satisface.

Registro encadenado - Registro ordenado donde cada bloque
                                          referencia al anterior por su huella criptográfica, firmado por un
                                          umbral de custodios. No es una cadena de bloques con consenso
                                          económico: no hay minería, ni token que sostenga la seguridad, ni
                                          contratos programables.

Supernodo comunitario - Nodo con mayor capacidad de almacenamiento
                                                y cómputo que acelera la red de una zona. Es jerarquía blanda: su caída
                                                no impide el funcionamiento.

Techo de aire - Mecanismo de límite a la acumulación. Quien excede
                                el umbral recibe avisos con plazo inversamente proporcional al monto; el
                                excedente inmóvil retorna al fondo para reinversión trazable. El margen
                                de riesgo lo pone el detector según la economía.

Tesoro común -  Patrimonio sin dueño: tierra, infraestructura y
                                cooperativas de destinación social. Opera como puente hacia el exterior
                                comprando y vendiendo, y acredita moneda social adentro.

Wi-Fi HaLow --- Variante de Wi-Fi en banda inferior a 1 GHz, con
                                mayor alcance y menor tasa que el Wi-Fi convencional.

<br>
.
<br>
<br>
<br>

### Referencias

Berners-Lee, M., Kennelly, C., Watson, R., & Hewitt, C. N. (2018). Current global food production is sufficient to meet human nutritional needs in 2050 provided there is radical societal adaptation. *Elementa: Science of the Anthropocene*, *6*(1), Article 52. https://doi.org/10.1525/elementa.310

FAO. (2025). *Employment indicators 2000–2023 — July 2025 update*. FAOSTAT Analytical Briefs, No. 110. Rome. https://doi.org/10.4060/cd5821en

FAO, IFAD, UNICEF, WFP, & WHO. (2026). *The State of Food Security and Nutrition in the World 2026*. Rome. https://doi.org/10.4060/cd8306en

USDA Economic Research Service. (2024). *Food Dollar Series*. Washington. https://www.ers.usda.gov/data-products/food-dollar-series/

FAO, WHO, & UNU. (2004). *Human energy requirements: Report of a Joint FAO/WHO/UNU Expert Consultation*. FAO Food and Nutrition Technical Report Series, No. 1. Rome: FAO. https://www.fao.org/4/Y5686E/y5686e00.htm

EAT-Lancet Commission. (2025). *Food, planet, health: Healthy diets from sustainable food systems. Summary report of the EAT-Lancet Commission*. EAT. https://www.fao.org/family-farming/detail/en/c/1743260/

Edalatnejad, K., Lueks, W., Sukaitis, J., Graf Narbel, V., Marelli, M., & Troncoso, C. (2024). Janus: Safe biometric deduplication for humanitarian aid distribution. In *2024 IEEE Symposium on Security and Privacy (SP)* (pp. 655-672). IEEE. https://eprint.iacr.org/archive/2023/1377/1699444969.pdf

World Inequality Lab. (2026). *World Inequality Report 2026*. Paris. https://wir2026.wid.world
