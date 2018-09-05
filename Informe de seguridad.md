---


---

<h1 id="informe-de-seguridad-producto-de-la-evaluación-de-seguridad">INFORME DE SEGURIDAD PRODUCTO DE LA EVALUACIÓN DE SEGURIDAD</h1>
<h4 id="autor-del-informe-jose-manuel-gómez-benítez">Autor del informe: Jose Manuel Gómez Benítez</h4>
<h2 id="fases-de-la-evaluación-de-seguridad">FASES DE LA EVALUACIÓN DE SEGURIDAD</h2>
<p>Esta evaluación busca ir accediendo de manera progresivamente al ordenador de prueba, obteniendo en el proceso la información sobre el sistema de seguridad informática que lo protege.</p>
<p>Para ello se utilizará, una plataforma conformada por una Raspberry Pi Zero W, con el sistema operativo Raspbian Lite, sobre el que se ha instalado el software libre <em>P4wnP1</em>.</p>
<p>Dicho proceso está conformado por un total de 3 fases:</p>
<ol>
<li>
<p><strong>Desbloqueo del ordenador de prueba</strong>. En esta fase, se intentará desbloquear el ordenador de prueba sin conocimiento previo sobre el usuario o la contraseña, esta última se averiguará en caso de que la prueba tenga existo.</p>
</li>
<li>
<p><strong>Acceso a las credenciales de navegación</strong>. En este paso, se accederá al navegador predeterminado de Windows 10, Microsoft Edge, y se sustraerá todas las credenciales almacenadas en él.</p>
</li>
<li>
<p><strong>Prueba de ejecución de un programa y traspaso del informe de seguridad</strong>. Es este último paso se procederá a ejecutar una serie de comandos en Windows, para abrir el programa Notepad, y escribir en él, el presente informe.</p>
</li>
</ol>
<h3 id="desbloqueo-del-ordenador-de-prueba">DESBLOQUEO DEL ORDENADOR DE PRUEBA</h3>
<h4 id="proceso-realizado-mediante-el-módulo-windows-10-lockpicker">Proceso realizado mediante el módulo <em>Windows 10 LockPicker</em></h4>
<p>En este paso, el dispositivo utilizado para la realización de la prueba se conectará a cualquiera de los múltiples puertos USB del ordenador de prueba; en caso de que se trate de un ordenador de sobremesa se priorizará buscar un puerto libre, al que conectar el dispositivo, en la parte trasera del ordenador, pues en dicha posición se puede ocultar con mayor facilidad el dispositivo.<br>
Una vez conectado el dispositivo, ese iniciará el proceso de desbloqueo del ordenador, dicho proceso llevará más o menos tiempo dependiendo de la fortaleza de la contraseña utilizada para bloquear el ordenador.</p>
<p>Este punto tiene por tanto una doble finalidad:</p>
<ul>
<li>Acceder al ordenador para continuar con el resto de las fases.</li>
<li>Comprobar si el usuario del ordenador utiliza contraseñas insuficientemente complejas.</li>
</ul>
<h3 id="captura-de-credenciales-del-navegador">CAPTURA DE CREDENCIALES DEL NAVEGADOR</h3>
<h4 id="proceso-realizado-mediante-el-módulo-hakin9">Proceso realizado mediante el módulo <em>Hakin9</em></h4>
<p>Esta fase busca comprobar si el usuario del ordenador de prueba accede de manera segura y teniendo en cuenta la importancia de guardar adecuadamente las diversas contraseñas y usuarios con los que acceder a los diversos sitios web.</p>
<p>Para la realización de esta prueba, se ha de modificar en primer lugar la configuración software del dispositivo, desde el ordenador de control, tras esto se reconecta la plataforma de nuevo.</p>
<p>Una vez se ha conectado el dispositivo al ordenador de prueba, se ejecuta el programa encargado de esta fase de la prueba, el cual toma los datos del navegador y los almacena en la tarjeta de memoria del dispositivo.</p>
<p>***Dichos datos serán eliminados tras la prueba, en base a la ley de protección de datos, UE 2016/679. ***</p>
<h3 id="prueba-de-ejecución-de-un-programa-y-transpaso-del-informe-de-seguridad">PRUEBA DE EJECUCIÓN DE UN PROGRAMA Y TRANSPASO DEL INFORME DE SEGURIDAD</h3>
<h4 id="proceso-realizado-mediante-el-módulo-hid_keyboard">Proceso realizado mediante el módulo <em>hid_keyboard</em></h4>
<p>Esta última prueba, busca comprobar si el usuario del ordenador de prueba dispone de alguna contramedida que evite la ejecución de comandos que permitan controlar el ordenador de manera temporal de igual manera que el administrador del ordenador.</p>
<p>Para ello, se ejecutará un pequeño programa de prueba el cual abrirá un solo programa, Notepad, transcribirá de manera completa el presente informe y lo guardará en el escritorio del ordenador.</p>
<h2 id="medidas-que-han-de-ser-tomandas-los-resultados-de-la-prueba-de-penetración">MEDIDAS QUE HAN DE SER TOMANDAS LOS RESULTADOS DE LA PRUEBA DE PENETRACIÓN</h2>
<p>En este apartado se expondrán las diversas medidas de seguridad tanto físicas como informáticas, que se han de tomar para mejorar la seguridad del sistema informático objetivo de la prueba de penetración.</p>
<h3 id="medidas-físicas">MEDIDAS FÍSICAS</h3>
<ol>
<li>Bloqueo de todos los conectores USB, del ordenador; la forma más eficiente de realizar esta operación es introducir el ordenador al completo en un armario, de un material robusto, que disponga de:
<ul>
<li>Rejillas de ventilación, que permita un óptimo flujo de aire, para evitar posibles problemas de ventilación</li>
<li>Salida de cableado de alimentación y periféricos, dicha salida no debe permitir el acceso físico a ningún conector del ordenador.</li>
<li>Botón de encendido externo.</li>
</ul>
</li>
<li>Evitar la utilización de periféricos o cualquier dispositivo USB, no identificado, para realizar el proceso de identificación se recomienda disponer de un ordenador de bajo coste, por ejemplo, un miniordenador de 100€, con Windows 10 al que no se le ha agregado programa alguno, al que conectar los distintos dispositivos USB, por primera vez.</li>
</ol>
<h3 id="medidas-software">MEDIDAS SOFTWARE</h3>
<ol>
<li>
<p>Modificación de la contraseña utilizada, se recomienda utilizar una contraseña superior a 12 dígitos y la renovación de esta de manera periódica cada 1 o 3 meses. A la hora de crear dicha contraseña se ha de tener en cuenta una serie de cuestiones:</p>
<ol>
<li>No utilizar, nombres propios y/o fechas</li>
<li>Crearla a partir de una frase o combinación de palabras, teniendo en cuenta que no deben ser ni frase conocidas ni palabras que hagan referencia a un elemento cultural conocido.</li>
<li>Sustitución de letras por números de manera aleatoria</li>
<li>Eliminación de vocales para modificar aún más la palabra inicial.</li>
<li>Mezclar el orden de las sílabas una vez realizados los pasos anteriores.</li>
</ol>
</li>
<li>
<p>Instalar un navegador distinto al predeterminado por el sistema operativo, algunos de los recomendados son Opera o Chrome.</p>
</li>
<li>
<p>Deshabilitar el guardado de cualquier tipo de contraseña en el navegador, es preferible memorizarlas, o en caso de que esto sea imposible guardarlas en una libreta que lleve el usuario consigo mismo; tampoco es recomendable el guardado de usuarios.</p>
</li>
<li>
<p>Acceder al correo o sitios webs con información crítica desde el <em>modo incognito</em> del navegador, debido a que una vez finalizada la sesión se borran, del ordenador, todos los datos. En el caso de Opera o Chrome, se puede activar mediante el atajo de teclado CTRL + SHIFT DER + N.</p>
</li>
<li>
<p>Instalación de un software destinado a la detección y bloqueo de posibles ataques de <em>USB Rubber Ducky</em>, en este caso se recomienda Beamgun, el cual está disponible aquí: <a href="https://github.com/JLospinoso/beamgun">https://github.com/JLospinoso/beamgun</a>.</p>
</li>
</ol>
<p>Con la combinación de todas estas medidas se podrá mejorar la seguridad del sistema informativo, para evitar la mayoría de posibles ataques conocidos por vía USB; sin embargo, en base a esto se recomienda la realización de una prueba de penetración profesional para evaluar adecuadamente el sistema informático.</p>
<p>Para más información visite:<br>
<a href="https://github.com/Jmg20/TUSB/blob/master/INFORME%20DE%20SEGURIDAD%20PRODUCTO%20DE%20LA%20PRUEBA%20DE%20PENETRACI%C3%93N.txt">https://github.com/Jmg20/TUSB/blob/master/INFORME DE SEGURIDAD PRODUCTO DE LA PRUEBA DE PENETRACIÓN.txt</a></p>
<p>NOTA: El presente informe ha sido creado con el lenguaje de texto <em>Markdown</em>, si desea verlo más claramente puede copiar este texto en cualquier editor online de <em>Markdown</em>, como <a href="https://stackedit.io">https://stackedit.io</a></p>

