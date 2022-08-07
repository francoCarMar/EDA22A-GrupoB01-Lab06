<div align="center">
<table>
    <theader>
        <tr>
            <td><img src="https://github.com/rescobedoq/pw2/blob/main/epis.png?raw=true" alt="EPIS" style="width:50%; height:auto"/></td>
            <th>
                <span style="font-weight:bold;">UNIVERSIDAD NACIONAL DE SAN AGUSTIN</span><br />
                <span style="font-weight:bold;">FACULTAD DE INGENIERÍA DE PRODUCCIÓN Y SERVICIOS</span><br />
                <span style="font-weight:bold;">ESCUELA PROFESIONAL DE INGENIERÍA DE SISTEMAS</span>
            </th>
            <td><img src="https://github.com/rescobedoq/pw2/blob/main/abet.png?raw=true" alt="ABET" style="width:50%; height:auto"/></td>
        </tr>
    </theader>
    <tbody>
        <tr><td colspan="3"><span style="font-weight:bold;">Formato</span>: Guía de Práctica de Laboratorio / Talleres / Centros de Simulación</td></tr>
        <tr><td><span style="font-weight:bold;">Aprobación</span>:  2022/03/01</td><td><span style="font-weight:bold;">Código</span>: GUIA-PRLD-001</td><td><span style="font-weight:bold;">Página</span>: 1</td></tr>
    </tbody>
</table>
</div>

<div>
<span style="font-weight:bold;">INFORME DE LABORATORIO</span><br />

<table>
<theader>
<tr><th colspan="6">INFORMACIÓN BÁSICA</th></tr>
</theader>
<tbody>
<tr><td>ASIGNATURA:</td><td colspan="5">Estructura de Datos y Algoritmos</td></tr>
<tr><td>TÍTULO DE LA PRÁCTICA:</td><td colspan="5">Árbol B</td></tr>
<tr>
<td>NÚMERO DE PRÁCTICA:</td><td>06</td><td>AÑO LECTIVO:</td><td>2022 A</td><td>NRO. SEMESTRE:</td><td>III</td>
</tr>
<tr>
<td>FECHA DE PRESENTACIÓN:</td><td>07/08/2022</td><td>HORA DE PRESENTACIÓN:</td><td colspan="3"></td>
</tr>
<tr><td colspan="3">INTEGRANTE(s):
<ul>
<li>Cárdenas Martínez Franco Luchiano - fcardenasm@unsa.edu.pe</li>
<li>Carrillo Daza Barbara Rubi - bcarrillo@unsa.edu.pe</li>
<li>Diaz Portilla Carlo Rodrigo - cdiazpor@unsa.edu.pe</li>
<li>Hancco Condori Bryan Orlando - bhanccoco@unsa.edu.pe</li>
<li>Mamani Cañari Gabriel Anthony - gmamanican@unsa.edu.pe</li>
</ul>
</td>
<td>NOTA:</td><td colspan="2"></td>
</<tr>
<tr><td colspan="6">DOCENTE(s):
<ul>
<li>Richart Smith Escobedo Quispe - rescobedoq@unsa.edu.pe</li>
</ul>
</td>
</<tr>
</tbody>
</table>

<!-- Reportes -->
## SOLUCIÓN Y RESULTADOS
  
---

I. SOLUCIÓN DE EJERCICIOS/PROBLEMAS <br>
* La organización del repositorio es la siguiente
    ```sh
    .
    ├── BTree.java
    ├── Test.java
    └── README.md
    ```
  * **Nota :** Para los ver los ejercicios propuestos deberá compilar y ejecutar "Test.java".
* **Ejercicio 1:** Título
	
  Descripción
  ```java
  //Código resaltante
  ```    
* **Ejercicio 2:** Títuo
     
    Descripción
    ```java
    //Código resaltante
    ```


* **Ejercicio 3:** 

    El método toString() del árbol, retorna lo siguiente. ¿Por qué están entre paréntesis ciertas claves?

    Mostrar paso a paso el arbol-B al eliminar "www.espn.com":

    * 1. Para realizar <code>delete("www.espn.com")</code> al igual que cuando insertamos se tiene que buscar el nodo con la clave que queremos eliminar.
  
    <img src="img/delete1.jpeg" style="width:90%; height:auto"/>

    * 2. Se empieza buscando el nodo a eliminar desde el nodo raíz (<code>root</code>), entonces se evalua el nodo con la clave <code>www.cs.princeton.edu</code> donde se evaluará por donde continuar la búsqueda.

    <img src="img/delete2.jpeg" style="width:90%; height:auto"/>

    * 3. Internamente se realiza el <code>"www.espn.com".compareTo("www.cs.princeton.edu")</code> el cual nos dará por resultado un número positivo, indicando que se debe continuar por la derecha.
    
    <img src="img/delete3.jpeg" style="width:90%; height:auto"/>

    * 4. Luego tenemos un nodo que tiene 3 <code>Entry</code>, entonces se debe comparar la clave a buscar con las 3 claves que tenemos en este node. Debido a que <code>"www.espn.com".compareTo("www.google.com")</code> nos resulta en un número negativo, no hay necesidad de seguir comparando con las otras dos claves.
    
    <img src="img/delete4.jpeg" style="width:90%; height:auto"/>

    * 5. Internamente se realiza un <code>"www.espn.com".compareTo("www.google.com")</code>, resultado negativo que nos indicaría que debemos seguir por la izquierda.
    
    <img src="img/delete5.jpeg" style="width:90%; height:auto"/>

    * 6. A este punto la altura a la que se encuentra es igual a 0, entonces se realizan <code>compareTo()</code> para encontrar la posición de la clave a eliminar
    
    <img src="img/delete6.jpeg" style="width:90%; height:auto"/>

    * 7. Una vez se ha encontrado la posición de la clave se debe analizar si el nodo que queremos eliminar es un nodo interior o es una hoja, en este caso la clave <code>"www.espn.com"</code> es una hoja, por lo que podemos eliminarlo. Luego de eliminar se debe analizar si se realiza una redistribución o una unión dependiendo si el nodo se encuentra en un estado de underflow o se encuentra en overflow.
    
    <img src="img/delete7.jpeg" style="width:90%; height:auto"/>

    * 8. En este caso no se tiene que realizar ningún movimiento (redistribución o unión), entonces simplemente se elimina.
    
    <img src="img/delete8.jpeg" style="width:90%; height:auto"/>
    

II. CONCLUSIONES
	
- 
- 
- 
- 

---
    
## RETROALIMENTACIÓN GENERAL
 <pre>
 
 </pre>
---
    
### REFERENCIAS Y BIBLIOGRAFÍA
<ul>
    <li>https://www.w3schools.com/java/</li>
    <li>https://www.eclipse.org/downloads/packages/release/2022-03/r/eclipse-ide-enterprise-java-and-web-developers</li>
    <li>https://docs.oracle.com/javase/tutorial/java/generics/types.html</li>
</ul>
