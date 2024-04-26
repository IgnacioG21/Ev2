# Ev2
Este es un repositorio de la evaluación 2 de Programación Front End Inacap La Granja
26/04/2024

Primeros 3 dias estudiando el contenido para saber que hacer y como hacerlo, hoy empecé el documento, hice el header con las 4 secciones aunque el home no deberia estar ahí, lo cambiaré por otra sección y lo pondré en el footer para volver al inicio de la página. 

    <header class="titulo">
        <h1> Juegos Populares </h1>
        <nav class="secciones">
            <table style="width: 100%;">
                <tr>
                    <td style="padding: 10px 24px 10px 10px; width: 50%;">
                        <a href=""> Inicio </a>
                    </td>

                    <td style="padding: 10px; width: 50%;">
                        <a href=""> Quienes Somos </a>
                    </td>
                </tr>
                <tr>
                    <td style="padding: 10px; width: 50%;">
                        <a href=""> Contacto </a>
                    </td>

                    <td style="padding: 10px 46px 10px 10px; width: 50%;">
                        <a href=""> Recursos </a>
                    </td>
                </tr>
            </table>
        </nav>
    </header>

Ese es el header, contiene un nav con una tabla donde tengo los links, la tabla ocupa 100% de la pagina y 2 filas con 50% en cada celda. La tabla contiene los 4 links, si me da tiempo crearé páginas simples para linkearlas internamente. Tuve problemas para alinearlas asi que ocupé padding 46 y 24 px respectivamente para que se alinearan.

CSS (Header):
.titulo {
    /* header */
    background-color: rgb(0, 0, 0);
    border: 5px solid rgb(90, 0, 0);
    border-radius: 10px;
    color: white;
    display: flex;
    flex-direction: column;
    height: 125px;
    text-align: center;
}

Fondo color negro
Borde rojo oscuro 5px estilo solido con curvatura en las esquinas de 10px
Display: flex
flex direction: column
Alto definido en 125px
Color del texto blanco y alineado al centro

.secciones {
    /* nav */
    display: flex;
    justify-content: space-between;
    margin: 0 100 0 100;
}

display: flex;
justify content: space-between; Espaciado entre elementos
Margen de 100px a la izquierda y a la derecha de elementos para que se agrupen de mejor manera



Parte 2 26/04/2024


    <section>
        <div class="parrafo">
            <p> Esta página recopila una lista con los juegos más influyentes de su respectiva epoca, conocerás la
                historia,
                especificaciones, información y alcance de cada juego. Esta lista está ordenada cronologicamente, si
                deseas
                ver una epoca especifica revisar:<br> </p>
        </div>

        <br>

        <div class="contenedor">
            <div class="lista1">
                <ol>
                    <li>
                        <p> 1980 - 1990 </p>
                    </li>

                    <li>
                        <p> 1990 - 2000 </p>
                    </li>

                    <li>
                        <p> 2000 - 2010 </p>
                    </li>

                    <li>
                        <p> 2010 - 2020 </p>
                    </li>

                    <li>
                        <p> 2020 - Actualidad </p>
                    </li>
                </ol>

                <aside class="nota">
                    <p> Nota: La lista que verás se ha elaborado de manera imparcial y objetiva, basada
                        en información recopilada y sintetizada de diversas fuentes. </p>
                </aside>
            </div>

            <figure class="figura1">
                <img src="https://i.blogs.es/4d650a/gogga/1366_2000.jpeg" alt="juegos" class="img1">
            </figure>
        </div>
    </section>
    
Luego del header usé <section> para envolver un div con un parrafo, tiene una descripción de la página, a continuación hay otro div con una lista ordenada con las decadas que se tendrán presentes en la realización de la página, una nota con una aclaración sobre la web, y una imagen. En pc la imagen se verá al lado de la lista, en teléfono se verá abajo.

CSS (Section): 
.parrafo {
    /* Primer parrafo */
    background-color: black;
    border: 5px solid rgb(90, 0, 0);
    border-radius: 10px;
    color: white;
    text-align: center;
}

Fondo negro, borde rojo oscuro
Color del texto blanco y alineado al centro

.contenedor {
    /* Contenedor de imagen 1 */
    display: flex;
}

.lista1 {
    /* ol */
    background-color: black;
    border: 5px solid rgb(90, 0, 0);
    border-radius: 10px;
    width: 318px;
    justify-content: flex-start;
    text-align: center;
    /* width: 318px; en teléfono - width: 334px; en pc */
}

Lista ordenada
Fondo negro, borde rojo oscuro
Ancho fijo de 318px
Justify content: flex-start; Contenido alineado al principio del contenedor
Texto centrado de la lista

.nota {
    background-color: orangered;
    border: 3px solid rgb(90, 0, 0);
    border-radius: 10px;
    color: black;
    font-weight: 550;
    margin: 5px;
    text-align: center;
}

Fondo color naranja rojizo, borde rojo oscuro
Tamaño de fuente 550 para que se remarque un poco el texto 
Margen del borde de 5px
Texto alineado al centro

.figura1 {
    /* Primera figura */
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
}

Contenedor de la imagen
Ancho del 100%
Display: flex;
Justify content: center; Alinear horizontalmente la imagen
Align items: center; Alinear verticalmente la imagen

.img1 {
    width: 750px;
}

Ancho de la imagen a 750px

.........................................




 
