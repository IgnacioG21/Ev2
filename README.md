# Ev2
Ignacio Garrido
21.559.162-k
TI2031/V-B50-N3-P12-C1/V La Granja B5


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




CODIGO FINAL (VERSION CELULAR CODIGO CSS INTEGRADO)
<!DOCTYPE html>
<html>

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title> Review Juegos Clasicos - Modernos </title>
    <link rel="stylesheet" href="Estilo1-1.css">
    <script> /* Formulario */
        function selectRadio(inputId) {
            document.getElementById(inputId).checked = true;
        }
    </script>
    <style>
        /* Links */
        a:hover {
            color: red;
        }

        /* Cuerpo */
        body {
            background-color: red;
            color: white;
            font-family: sans-serif;
        }

        h1 {
            margin: 5px 0px 0px 0px;
        }

        img {
            border: 5px solid rgb(90, 0, 0);
            border-radius: 10px;
        }


        /* Clases */
        .center {
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .contenedor {
            /* ol 1     -       img 1 */
            display: grid;
            grid-template-columns: 1fr 1fr;
            justify-content: space-between;
            gap: 8px;
            width: 100%;
        }

        .contenedor-imagen-indice {
            /* Primera figura */
            display: flex;
            justify-content: center;
            align-items: center;
            width: 100%;
            margin: 0px;
        }



        /* Seccion de información */
        .contenedor-img {
            display: flex;
            justify-content: center;
            align-items: center;
            width: 100%;
            text-align: center;
        }

        .contenedor-seccion {
            display: grid;
            grid-template-columns: 1fr 1fr;
            justify-content: space-between;
            gap: 10px;
            width: 100%;
            margin: 10px 0px 0px 0px;
        }

        .contenedor-parrafo {
            background-color: rgb(0, 0, 0);
            border: 5px solid rgb(90, 0, 0);
            border-radius: 10px;
            display: flex;
            justify-content: center;
            padding: 15px;
            width: 90%;

        }

        .img-seccion {
            width: 700px;
        }


        /* */
        .contenedor-lista {
            /* ol 1*/
            width: 100%;
            /* width: 318px; en teléfono - width: 334px; en pc */
        }

        /* Footer */
        .footer {
            display: inline-block;
            background-color: black;
            border: 5px solid blue;
            border-radius: 10px;
            text-align: center;
            margin-bottom: 10px;
            padding: 5px;
        }

        .link-footer {
            background-color: white;
            border: 2px solid blue;
            border-radius: 10px;
            color: black;
            font-weight: 550;
            font-family: monospace;
            text-decoration: none;
            padding: 5px;
        }

        /* Formulario */
        .form {
            border: 5px solid rgb(90, 0, 0);
            border-radius: 10px;
            margin-top: 10px;
            width: 80%;
        }

        #Tabla,
        #Tabla th,
        #Tabla td {
            border: 2px solid white;
            background-color: black;
            text-align: center;
            padding: 10px;
        }

        .input {
            border: 5px solid black;
            border-radius: 10px;
            margin-top: 5px;
            margin-bottom: 5px;
        }




        .header-inicio {
            /* header */
            background-color: rgb(0, 0, 0);
            border: 5px solid rgb(90, 0, 0);
            border-radius: 10px;
            color: white;
            display: flex;
            flex-direction: column;
            text-align: center;
        }

        .img1 {
            max-width: 700px;
            height: auto;
        }

        .lista {
            background-color: black;
            border: 5px solid rgb(90, 0, 0);
            border-radius: 10px;
            text-align: center;
            margin-top: 0px;
            padding-top: 10px;
            padding-bottom: 10px;
        }

        .link-lista {
            text-decoration: none;
            color: white;
        }


        .link {
            background-color: white;
            border: 1px solid red;
            border-radius: 10px;
            color: black;
            font-weight: 550;
            font-family: monospace;
            text-decoration: none;
            padding: 5px;
        }

        .nota {
            background-color: orangered;
            border: 3px solid rgb(90, 0, 0);
            border-radius: 10px;
            color: black;
            font-weight: 550;
            padding: 5px;
            text-align: center;
        }

        .parrafo {
            background-color: black;
            border: 5px solid rgb(90, 0, 0);
            border-radius: 10px;
            color: white;
            padding: 15px;
        }

        .secciones {
            /* nav */
            display: flex;
            justify-content: space-between;
            margin: 0 100 0 100;
        }

        .seccion-pacman {
            background-color: yellow;
            padding: 10px;
            border: 2px solid black;
            border-radius: 10px;
        }

        .seccion-dk {
            background-color: rgb(139, 80, 11);
            padding: 10px;
            border: 2px solid black;
            border-radius: 10px;
        }

        .seccion-1942 {
            background-color: lightseagreen;
            padding: 10px;
            border: 2px solid black;
            border-radius: 10px;
        }

        .seccion-dd {
            background-color: rgb(15, 168, 15);
            padding: 10px;
            border: 2px solid black;
            border-radius: 10px;
        }

        .seccion-mario {
            background-color: rgb(180, 15, 15);
            padding: 10px;
            border: 2px solid black;
            border-radius: 10px;
        }

        .sub {
            color: red;
            font-weight: 549;
        }

        .titulo {
            display: inline-block;
            background-color: black;
            border: 5px solid rgb(90, 0, 0);
            border-radius: 10px;
            text-align: center;
            margin-bottom: 10px;
            padding: 5px;
        }

        .tituloizq {
            display: inline-block;
            background-color: black;
            border: 5px solid rgb(90, 0, 0);
            border-radius: 10px;
            margin-bottom: 10px;
            padding: 5px;
        }

        /* Media Querys */

        /* 375px    -   400px */
        @media screen and (min-width: 375px) and (max-width: 400px) {
            .contenedor {
                display: flex;
                flex-direction: column;
            }

            .contenedor-seccion {
                display: flex;
                flex-direction: column;
            }

            .img-seccion {
                width: 90%;
            }

            /* */
            .img1 {
                width: 320px;
            }

            .contenedor-imagen-indice {
                width: 100%;
                margin: 20px 0px 0px 0px;
                display: flex;
                justify-content: center;
                align-items: center;
            }

            .form {
                width: 100%;
                margin-bottom: 10px;
            }

            #Tabla th {
                padding: 10px 0px 10px 0px;
            }

            #Tabla td {
                padding: 0px 10px 0px 10px;
            }
        }

        /* 400px */
        /* Usado de ejemplo */
        @media screen and (min-width: 400px) and (max-width: 415px) {
            .contenedor {
                display: flex;
                flex-direction: column;
            }

            /* Pacman */
            .contenedor-seccion {
                display: flex;
                flex-direction: column;
            }

            .img-seccion {
                width: 90%;
            }

            /* */
            .img1 {
                width: 375px;
            }

            .contenedor-imagen-indice {
                width: 100%;
                margin: 20px 0px 0px 0px;
                display: flex;
                justify-content: center;
                align-items: center;
            }

            .form {
                width: 100%;
                margin-bottom: 10px;
            }

            #Tabla th {
                padding: 10px 0px 10px 0px;
            }

            #Tabla td {
                padding: 0px 10px 0px 10px;
            }
        }

        /* 415px    -   455px */
        @media screen and (min-width: 415px) and (max-width: 455px) {
            .contenedor {
                display: flex;
                flex-direction: column;
            }

            /* Pacman */
            .contenedor-seccion {
                display: flex;
                flex-direction: column;
            }

            .img-seccion {
                width: 90%;
            }

            /* */
            .img1 {
                width: 380px;
            }

            .contenedor-imagen-indice {
                /* Primera figura */
                width: 100%;
                margin: 20px 0px 0px 0px;
                display: flex;
                justify-content: center;
                align-items: center;
            }

            .form {
                width: 100%;
                margin-bottom: 10px;
            }

            #Tabla th {
                padding: 10px 0px 10px 0px;
            }

            #Tabla td {
                padding: 0px 10px 0px 10px;
            }

        }

        /* 455px    -   495px */
        @media screen and (min-width: 455px) and (max-width: 495px) {
            .contenedor {
                display: flex;
                flex-direction: column;
            }

            /* Pacman */
            .contenedor-seccion {
                display: flex;
                flex-direction: column;
            }

            .img-seccion {
                width: 90%;
            }

            .img1 {
                width: 420px;
            }

            .contenedor-imagen-indice {
                /* Primera figura */
                width: 100%;
                margin: 20px 0px 0px 0px;
                display: flex;
                justify-content: center;
                align-items: center;
            }

            .form {
                width: 100%;
                margin-bottom: 10px;
            }

            #Tabla th {
                padding: 10px 0px 10px 0px;
            }

            #Tabla td {
                padding: 0px 10px 0px 10px;
            }

        }

        /* 495px    -   535px */
        @media screen and (min-width: 495px) and (max-width: 535px) {
            .contenedor {
                display: flex;
                flex-direction: column;
            }

            /* Pacman */
            .contenedor-seccion {
                display: flex;
                flex-direction: column;
            }

            .img-seccion {
                width: 90%;
            }

            .img1 {
                width: 440px;
            }

            .contenedor-imagen-indice {
                /* Primera figura */
                width: 100%;
                margin: 20px 0px 0px 0px;
                display: flex;
                justify-content: center;
                align-items: center;
            }

            .form {
                width: 100%;
                margin-bottom: 10px;
            }

            #Tabla th {
                padding: 10px 0px 10px 0px;
            }

            #Tabla td {
                padding: 0px 10px 0px 10px;
            }

        }

        /* 535px    -   575px */
        @media screen and (min-width: 535px) and (max-width: 575px) {
            .contenedor {
                display: flex;
                flex-direction: column;
            }

            /* Pacman */
            .contenedor-seccion {
                display: flex;
                flex-direction: column;
            }

            .img-seccion {
                width: 90%;
            }

            .img1 {
                width: 480px;
            }

            .contenedor-imagen-indice {
                /* Primera figura */
                width: 100%;
                margin: 20px 0px 0px 0px;
                display: flex;
                justify-content: center;
                align-items: center;
            }

            .form {
                width: 90%;
                margin-bottom: 10px;
            }

            #Tabla th {
                padding: 10px 0px 10px 0px;
            }

            #Tabla td {
                padding: 0px 10px 0px 10px;
            }

        }

        /* 575px    -   615px */
        @media screen and (min-width: 575px) and (max-width: 615px) {
            .contenedor {
                display: flex;
                flex-direction: column;
            }

            /* Pacman */
            .contenedor-seccion {
                display: flex;
                flex-direction: column;
            }

            .img-seccion {
                width: 90%;
            }

            .img1 {
                width: 520px;
            }

            .contenedor-imagen-indice {
                /* Primera figura */
                width: 100%;
                margin: 20px 0px 0px 0px;
                display: flex;
                justify-content: center;
                align-items: center;
            }

            .form {
                width: 90%;
                margin-bottom: 10px;
            }

            #Tabla th {
                padding: 10px 0px 10px 0px;
            }

            #Tabla td {
                padding: 0px 10px 0px 10px;
            }
        }

        /* 615px    -   655px */
        @media screen and (min-width: 615px) and (max-width: 655px) {
            .contenedor {
                display: flex;
                flex-direction: column;
            }

            /* Pacman */
            .contenedor-seccion {
                display: flex;
                flex-direction: column;
            }

            .img-seccion {
                width: 90%;
            }

            .img1 {
                width: 560px;
            }

            .contenedor-imagen-indice {
                /* Primera figura */
                width: 100%;
                margin: 20px 0px 0px 0px;
                display: flex;
                justify-content: center;
                align-items: center;
            }

            .form {
                width: 90%;
                margin-bottom: 10px;
            }

            #Tabla th {
                padding: 10px 0px 10px 0px;
            }

            #Tabla td {
                padding: 0px 10px 0px 10px;
            }
        }

        /* 655px    -   695px */
        @media screen and (min-width: 655px) and (max-width: 695px) {
            .contenedor {
                display: flex;
                flex-direction: column;
            }

            /* Pacman */
            .contenedor-seccion {
                display: flex;
                flex-direction: column;
            }

            .img-seccion {
                width: 90%;
            }

            .img1 {
                width: 600px;
            }

            .contenedor-imagen-indice {
                /* Primera figura */
                width: 100%;
                margin: 20px 0px 0px 0px;
                display: flex;
                justify-content: center;
                align-items: center;
            }
        }

        /* 695px    -   735px */
        @media screen and (min-width: 695px) and (max-width: 735px) {
            .contenedor {
                display: flex;
                flex-direction: column;
            }

            /* Pacman */
            .contenedor-seccion {
                display: flex;
                flex-direction: column;
            }

            .img-seccion {
                width: 90%;
            }

            .img1 {
                width: 640px;
            }

            .contenedor-imagen-indice {
                /* Primera figura */
                width: 100%;
                margin: 20px 0px 0px 0px;
                display: flex;
                justify-content: center;
                align-items: center;
            }
        }

        /* 735px    -   775px */
        @media screen and (min-width: 735px) and (max-width: 775px) {
            .contenedor {
                display: flex;
                flex-direction: column;
            }

            /* Pacman */
            .contenedor-seccion {
                display: flex;
                flex-direction: column;
            }

            .img-seccion {
                width: 90%;
            }

            .img1 {
                width: 700px;
            }

            .contenedor-imagen-indice {
                /* Primera figura */
                width: 100%;
                margin: 20px 0px 0px 0px;
                display: flex;
                justify-content: center;
                align-items: center;
            }
        }

        /* 800px    -   860px */
        @media screen and (min-width: 775px) and (max-width: 860px) {
            .img1 {
                width: 350px;
                height: 230px;
                margin: 5px 0px 15px 0px;
            }

            /* Pacman */
            .contenedor-seccion {
                display: flex;
                flex-direction: column;
            }

            .img-seccion {
                width: 80%;
            }
        }

        /* 860px    -   900px */
        @media screen and (min-width: 860px) and (max-width: 900px) {
            .img1 {
                width: 400px;
                height: 260px;
            }

            /* Pacman */
            .contenedor-seccion {
                display: flex;
                flex-direction: column;
            }

            .img-seccion {
                width: 80%;
            }
        }

        /* 900px    -   940px */
        @media screen and (min-width: 900px) and (max-width: 940px) {
            .img1 {
                width: 450px;
                height: 270px;
            }

            /* Pacman */
            .contenedor-seccion {
                display: flex;
                flex-direction: column;
            }

            .img-seccion {
                width: 80%;
            }
        }

        /* 940px    -   980px */
        @media screen and (min-width: 940px) and (max-width: 980px) {
            .img1 {
                width: 500px;
                height: 280px;
            }

            /* Pacman */
            .contenedor-seccion {
                display: flex;
                flex-direction: column;
            }

            .img-seccion {
                width: 80%;
            }
        }

        /* 980px    -   1020px */
        @media screen and (min-width: 980px) and (max-width: 1020px) {
            .img1 {
                width: 550px;
                height: 290px;
            }

            /* Pacman */
            .contenedor-seccion {
                display: flex;
                flex-direction: column;
            }

            .img-seccion {
                width: 75%;
            }
        }

        /* 1020px    -   1060px */
        @media screen and (min-width: 1020px) and (max-width: 1060px) {
            .img1 {
                width: 600px;
                height: 300px;
            }

            /* Pacman */
            .contenedor-seccion {
                display: flex;
                flex-direction: column;
            }

            .img-seccion {
                width: 75%;
            }
        }

        /* 1060px    -   1100px */
        @media screen and (min-width: 1060px) and (max-width: 1100px) {
            .img1 {
                width: 650px;
                height: 300px;
            }

            /* Pacman */
            .contenedor-seccion {
                display: flex;
                flex-direction: column;
            }

            .img-seccion {
                width: 70%;
            }
        }

        @media screen and (min-width: 1100px) and (max-width: 1300px) {

            /* Pacman */
            .contenedor-seccion {
                display: flex;
                flex-direction: column;
            }

            .img-seccion {
                width: 70%;
            }
        }

        /* 1100px    -   1439px */
        @media screen and (min-width: 1100px) and (max-width: 1439px) {
            .img1 {
                width: 660px;
                height: 300px;
            }
        }
    </style>
</head>

<body>
    <header class="header-inicio">
        <h1> Juegos Iconicos </h1>
        <nav class="secciones">
            <table style="width: 100%;">
                <tr>
                    <td style="padding: 10px 31px 10px 10px; width: 50%;">
                        <a href="https://vimm.net" target="_blank" class="link"> Jugar </a>
                    </td>

                    <td style="padding: 10px; width: 50%;">
                        <a href="Quienes.html" class="link"> Quienes Somos </a>
                    </td>
                </tr>
                <tr>
                    <td style="padding: 10px; width: 50%;">
                        <a href="Contacto.html" class="link"> Contacto </a>
                    </td>

                    <td style="padding: 10px 46px 10px 10px; width: 50%;">
                        <a href="Recursos.html" class="link"> Recursos </a>
                    </td>
                </tr>
            </table>
        </nav>
    </header>

    <hr>

    <section>
        <div class="parrafo">
            <p> Esta página recopila una lista con los juegos más influyentes de su respectiva epoca, conocerás la
                historia,
                especificaciones, información y alcance de cada juego. Esta lista está ordenada cronologicamente, si
                deseas
                ver una epoca especifica revisar el índice:<br> </p>
        </div>

        <br>

        <div class="contenedor">
            <div>
                <div class="contenedor-lista">
                    <ol class="lista">
                        <li>
                            <a href="#1980-1990" class="link-lista">1980 - 1990</a>
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
                </div>
                <aside class="nota">
                    <p> Nota: La lista se ha elaborado sin precedencia, es una sintesis basada
                        en información recopilada y sintetizada de diversas fuentes. </p>
                </aside>

            </div>
            <figure class="contenedor-imagen-indice">
                <img src="https://i.blogs.es/4d650a/gogga/1366_2000.jpeg" alt="juegos" class="img1">
            </figure>
        </div>
    </section>
    <hr>
    <!--                                                                                                                                                                        -->
    <!-- 1980 - 1990-->
    <article>
        <div>
            <span style="display: flex; justify-content: center; align-items: center;">
                <h1 class="titulo" id="1980-1990"> 1980 - 1990 </h1>
            </span>
            <div class="parrafo">
                <p>
                    En la década de los 80, surgieron los videojuegos, una forma nueva de entretenimiento que cautivó a
                    millones de personas. Época marcada por los graficos pixelados y los sonidos sintetizados. Los
                    videojuegos de los 80 definieron el panorama de la cultura pop, con personajes icónicos como
                    Mario,
                    Pac-Man, Donkey Kong, Mega Man, entre otros. <br> <br>

                    En esta sección veremos los 5 juegos que más influencia tuvieron entre 1980 y 1990:<br>
                </p>
            </div>
        </div>

        <br>

        <!-- Pac-Man -->
        <section class="seccion-pacman">
            <h2 class="tituloizq"> Pac-Man </h2>

            <div class="parrafo">
                <p> Creado por el diseñador de videojuegos <span class="sub">Toru Iwatani</span> de la empresa de Namco,
                    distribuido por Midway
                    Games
                    al mercado de Estados Unidos a mediados de el año 1980. Pac-Man fué lanzado el 22 de Mayo de 1980 y
                    fue todo un éxito, convirtiendose en un fenómeno mundial
                    en la
                    industria de los videojuegos. <br> <br> Pac-Man vendió
                    un
                    total de 293.822 máquinas desde 1981 hasta 1987 dominando parcialmente el mundo virtual y de paso
                    consiguiendo un récord Guiness del "Videojuego de arcade más exitoso de todos los tiempos", sin duda
                    uno de los juegos más emblemáticos de los 80.
                </p>
            </div>

            <!-- Info Pac-man-->
            <figure class="contenedor-seccion">
                <div class="contenedor-img">
                    <a href="https://pacman.com/en/games/" target="_blank" title="Sitio Oficial de Pac-man">
                        <img src="https://cdn.hobbyconsolas.com/sites/navi.axelspringer.es/public/media/image/2022/04/pac-man-2682107.jpg?tf=3840x"
                            alt="Pacman" class="img-seccion">
                    </a>
                </div>

                <div class="center">
                    <div class="contenedor-parrafo">
                        <p style="margin-top: 0px; margin-bottom: 0px;">
                        <ul style="padding: 0px 0px 0px 10px;">
                            <p style="margin: 0px;">
                                El objetivo del juego es simple, controlar a <span
                                    style="color: yellow;">Pac-Man</span>, un
                                personaje amarillo redondo
                                con una boca
                                grande, y comer todas las <span class="sub">píldoras</span> o "puntos" dispersos por el
                                laberinto mientras evitas ser
                                atrapado por cuatro fantasmas. <br> <br>
                            </p>

                            <li>
                                <p style="margin: 0px;">
                                    Puedes mover a Pac-Man hacia arriba, abajo, izquierda y derecha para navegar por el
                                    laberinto.
                                    <br> <br>
                                </p>
                            </li>

                            <li>
                                <p style="margin: 0px;">
                                    Además de los puntos normales, también hay <span class="sub">frutas</span> que
                                    aparecen
                                    periódicamente en el
                                    laberinto y
                                    valen más puntos si Pac-Man las come. También hay <span class="sub">puntos
                                        grandes</span> o "píldoras de poder"
                                    que,
                                    cuando Pac-Man los come, le dan temporalmente la capacidad de comer a los fantasmas.
                                    <br> <br>
                                </p>
                            </li>

                            <li>
                                <p style="margin: 0px;">
                                    Cuando Pac-Man come un punto grande, los fantasmas se vuelven azules y Pac-Man puede
                                    comerlos temporalmente para ganar puntos adicionales. Sin embargo, los fantasmas
                                    eventualmente se recuperarán y <span class="sub">volverán a su estado normal</span>.
                                    <br> <br>
                                </p>
                            </li>

                            <li>
                                <p style="margin: 0px;">
                                    En el laberinto hay cuatro fantasmas, cada uno con su propio nombre y color (<span
                                        style="color: red;">Blinky</span>,
                                    <span style="color: violet;">Pinky</span>, <span style="color: aqua;">Inky</span> y
                                    <span style="color: orangered;"> Clyde </span>). Estos fantasmas intentarán
                                    atrapar a Pac-Man. Si Pac-Man es
                                    atrapado por un fantasma, pierde una <span class="sub"> vida </span>. <br> <br>
                                </p>
                            </li>

                            <li>
                                <p style="margin: 0px;">
                                    Pac-Man tiene un número <span class="sub">limitado</span> de vidas, generalmente
                                    tres, y
                                    el juego termina cuando
                                    todas las vidas se <span class="sub">agotan</span>. A medida que avanzas en el
                                    juego,
                                    los laberintos se vuelven
                                    más <span class="sub">complicados</span> y los fantasmas se vuelven más <span
                                        class="sub">rápidos</span> y
                                    <span class="sub">astutos</span>.
                                </p>
                            </li>
                        </ul>
                        </p>
                    </div>
                </div>
            </figure>

            <span class="center">
                <h4 class="titulo" style="margin: 10px 0px 0px 0px; padding: 5px;">

                    <nav class="secciones">
                        <table style="width: 100%;">
                            <tr>
                                <td>
                                    <a href="https://vimm.net/vault/91396" target="_blank" class="link"> Jugar </a>
                                </td>

                                <td>
                                    <a href="https://www.youtube.com/watch?v=Z9kP-Dk9t8Y" target="_blank" class="link">
                                        GamePlay </a>
                                </td>
                            </tr>
                        </table>
                    </nav>

                </h4>
            </span>
        </section>

        <br>

        <!-- Donkey Kong -->
        <section class="seccion-dk">
            <h2 class="tituloizq"> Donkey Kong </h2>

            <div class="parrafo">
                <p>
                    Creado por <span class="sub"> Shigeru Miyamoto </span> y desarrollado por Nintendo, lanzado en 1981,
                    Donkey Kong es otro juego clásico que ha dejado una huella en la historia de los videojuegos. <br>
                    <br>
                    El juego presenta a dos personajes principales: <span class="sub"> Jumpman </span>(más tarde
                    conocido como Mario) y <span class="sub">Donkey Kong</span>. Miyamoto eligió el nombre
                    "Donkey" ("Burro") para reflejar la estupidez del personaje, mientras que "Kong" se consideraba un
                    término genérico para los grandes simios en Japón. Donkey Kong fue el primer gran éxito de
                    Nintendo
                    en Norteamérica, comenzando a hacerse famoso y marcando el comienzo de las franquicias Super Mario y
                    Donkey Kong.
                </p>
            </div>

            <!-- Info DK-->
            <figure class="contenedor-seccion">
                <div class="contenedor-img">
                    <a href="https://www.nintendo.com/en-gb/Games/Characters-hub/Donkey-Kong-Hub/Donkey-Kong-Hub-846642.html"
                        target="_blank" title="Sitio Oficial de Donkey Kong">
                        <img src="https://www.nintendo.com/eu/media/images/10_share_images/games_15/virtual_console_nintendo_3ds_7/SI_3DSVC_DonkeyKong_image1600w.jpg"
                            alt="Donkey" class="img-seccion">
                    </a>
                </div>

                <div class="center">
                    <div class="contenedor-parrafo">
                        <p style="margin-top: 0px; margin-bottom: 0px;">
                        <ul style="padding: 0px 0px 0px 10px;">
                            <p style="margin: 0px;">
                                En Donkey Kong interpretas el papel de <span
                                    style="color: rgb(46, 46, 241)">Mario</span>
                                (Jumpman), quien debe rescatar a <span style="color: violet;">Peach</span>,
                                la princesa, de <span style="color: rgb(139, 80, 11);">Donkey Kong</span>. El objetivo
                                principal es llegar a la <span class="sub">parte
                                    superior</span> de la
                                estructura donde se encuentra Peach, evitando los <span class="sub">obstáculos</span>
                                y <span class="sub">enemigos</span> en
                                el camino. <br> <br>
                            </p>

                            <li>
                                <p style="margin: 0px;">
                                    Puedes mover a Mario hacia la derecha, izquierda, subir y bajar escaleras, tomar y
                                    usar objetos, y saltar
                                    para evitar los obstáculos, así subir la estructura para rescatar a la princesa.
                                    <br>
                                    <br>
                                </p>
                            </li>

                            <li>
                                <p style="margin: 0px;">
                                    El juego consta de <span class="sub">varios niveles</span>, cada uno con su propio
                                    diseño y desafíos. En cada
                                    nivel, debes esquivar obstáculos como <span class="sub">barriles</span> que Donkey
                                    Kong arroja, <span class="sub">fuego</span> y otros
                                    peligros mientras subes por las escaleras. <br> <br>
                                </p>
                            </li>

                            <li>
                                <p style="margin: 0px;">
                                    Obtienes puntos por recoger objetos como <span class="sub">martillos</span> y por
                                    <span class="sub">rescatar</span> a la Princesa
                                    Peach. También puedes ganar <span class="sub">vidas extra</span> al alcanzar ciertos
                                    puntajes. Además de los obstáculos, hay <span class="sub">enemigos</span> que
                                    intentarán detenerte, como los
                                    <span class="sub">pequeños fuegos</span> o los <span class="sub">carros de
                                        minas</span> que se deslizan por
                                    las plataformas.<br> <br>
                                </p>
                            </li>

                            <li>
                                <p style="margin: 0px;">
                                    En <span class="sub">algunos</span> niveles, Mario puede recoger un martillo que le
                                    permite destruir
                                    <span class="sub">temporalmente</span> a los enemigos y ganar <span
                                        class="sub">puntos adicionales</span> al golpear barriles. Sin
                                    embargo, Mario <span class="sub">no puede</span> saltar mientras sostiene un
                                    martillo. <br> <br>
                                </p>
                            </li>

                            <li>
                                <p style="margin: 0px;">
                                    Los enemigos y obstáculos en Donkey Kong siguen <span class="sub">patrones de
                                        movimiento predecibles</span>
                                    en cada nivel. Aprender estos patrones puede ayudarte a <span
                                        class="sub">anticipar</span> los movimientos de
                                    los enemigos y a <span class="sub">planificar</span> tu estrategia en consecuencia.
                                </p>
                            </li>
                        </ul>
                        </p>
                    </div>
                </div>
            </figure>

            <span class="center">
                <h4 class="titulo" style="margin: 10px 0px 0px 0px; padding: 5px;">

                    <nav class="secciones">
                        <table style="width: 100%;">
                            <tr>
                                <td>
                                    <a href="https://vimm.net/vault/91476" target="_blank" class="link"> Jugar </a>
                                </td>

                                <td>
                                    <a href="https://www.youtube.com/watch?v=jWiLt3BSJp0" target="_blank" class="link">
                                        GamePlay </a>
                                </td>
                            </tr>
                        </table>
                    </nav>
                </h4>
            </span>
        </section>

        <br>

        <!-- 1942 -->
        <section class="seccion-1942">
            <h2 class="tituloizq"> 1942</h2>

            <div class="parrafo">
                <p>
                    El videojuego "1942" se estrenó en 1984. Fue creado por la empresa japonesa <span
                        class="sub">Capcom</span>, que
                    es conocida por desarrollar muchos juegos icónicos en la historia de los videojuegos.
                    <br><br>1942 tuvo un impacto significativo en los años 80, fue uno de los primeros
                    <span class="sub">juegos de disparos</span> de <span class="sub">desplazamiento
                        vertical</span> que se convirtió
                    en un éxito comercial,
                    estableciendo un formato que sería ampliamente imitado en los años siguientes. Además,
                    su <span class="sub">jugabilidad adictiva</span> y <span class="sub">desafiante</span>
                    lo convirtió en un
                    favorito entre los jugadores de
                    la época, contribuyendo a su popularidad duradera y a su estatus como un clásico de los
                    videojuegos.
                </p>
            </div>

            <!-- Info -->
            <figure class="contenedor-seccion">
                <div class="contenedor-img">
                    <a href="https://capcom.fandom.com/es/wiki/1942" target="_blank" title=""> <!---->
                        <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiv29wQb4fC5L1YUimieRxklQr3J5Bk7WXj1ClWNficu1Gt3Jgt0mD8bhStRRnZQlQQNC91mmSL5sJ-LBMCEqwPtBjS6PWa-pPR5h5tUsi6n2_-VeerpMEUc7aQLS-Pw64dvI6oMKt6_p0/s1600/1942.jpg"
                            alt="1942" class="img-seccion"> <!---->
                    </a>
                </div>

                <div class="center">
                    <div class="contenedor-parrafo">
                        <p style="margin-top: 0px; margin-bottom: 0px;">
                        <ul style="padding: 0px 0px 0px 10px;">
                            <p style="margin: 0px;">
                                En 1942, asumes el papel de un piloto de avión durante la Segunda Guerra Mundial. El
                                objetivo
                                principal del juego es <span class="sub">destruir aviones enemigos</span> y otras
                                <span class="sub">fuerzas hostiles</span> mientras se
                                avanza a través de niveles que representan diferentes <span class="sub">etapas de la
                                    guerra</span>. <br> <br>
                            </p>

                            <li>
                                <p style="margin: 0px;">
                                    El avión puede moverse hacia arriba, abajo, izquierda y derecha en la pantalla para
                                    <span class="sub">esquivar disparos enemigos y obstáculos</span>. El avión también
                                    puede <span class="sub">disparar</span> una serie
                                    de <span class="sub">proyectiles</span> para destruir <span class="sub">aviones
                                        enemigos</span> y otros
                                    objetivos, como <span class="sub">barcos</span> y
                                    <span class="sub">fortalezas terrestres</span>. <br><br>
                                </p>
                            </li>

                            <li>
                                <p style="margin: 0px;">
                                    El juego se complica a medida que avanza, con <span class="sub">enemigos más
                                        difíciles</span> y una <span class="sub">mayor
                                        cantidad de disparos</span> y <span class="sub">obstáculos</span> en pantalla.
                                    Además, hay
                                    enfrentamientos con <span class="sub">jefes</span>
                                    al final de ciertos niveles que requieren <span class="sub">estrategia</span> y
                                    <span class="sub">habilidad</span> para ser
                                    derrotados. <br> <br>

                                </p>
                            </li>

                            <li>
                                <p style="margin: 0px;">
                                    El jugador tiene un número <span class="sub">limitado</span> de vidas, y el juego
                                    termina cuando todas las
                                    vidas se <span class="sub">agotan</span>. Sin embargo, el jugador puede <span
                                        class="sub">ganar vidas
                                        extra</span> al alcanzar <span class="sub">ciertos
                                        puntajes</span> o al recoger <span class="sub">power-ups especiales</span> que
                                    aparecen ocasionalmente. <br><br>
                                </p>
                            </li>

                            <li>
                                <p style="margin: 0px;">
                                    Los power-ups mejoran las <span class="sub">capacidades</span> del avión. Estos
                                    pueden incluir mejoras en el
                                    armamento, como <span class="sub">balas más potentes</span> o <span
                                        class="sub">misiles guiados</span>, así
                                    como <span class="sub">mejoras en la
                                        defensa</span>, como escudos temporales que protegen al avión de los ataques
                                    enemigos.
                                    <br><br>
                                </p>
                            </li>

                            <li>
                                <p style="margin: 0px;">
                                    A lo largo del juego, el jugador se enfrenta a una variedad de <span
                                        class="sub">escenarios</span> que
                                    representan diferentes <span class="sub">ubicaciones</span> y situaciones de la
                                    Segunda Guerra Mundial. Esto
                                    incluye enfrentamientos sobre el <span class="sub">océano</span>, <span
                                        class="sub">batallas en tierra</span>
                                    y ataques aéreos sobre
                                    <span class="sub">ciudades enemigas</span>.
                                </p>
                            </li>
                        </ul>
                        </p>
                    </div>
                </div>
            </figure>

            <span class="center">
                <h4 class="titulo" style="margin: 10px 0px 0px 0px; padding: 5px;">

                    <nav class="secciones">
                        <table style="width: 100%;">
                            <tr>
                                <td>
                                    <a href="https://vimm.net/vault/4" target="_blank" class="link"> Jugar </a>
                                </td>

                                <td>
                                    <a href="https://www.youtube.com/watch?v=1yMGtlNjcMY" target="_blank" class="link">
                                        GamePlay </a>
                                </td>
                            </tr>
                        </table>
                    </nav>

                </h4>
            </span>
        </section>

        <br>

        <!-- Double Dragon -->
        <section class="seccion-dd">
            <h2 class="tituloizq"> Double Dragon </h2>

            <div class="parrafo">
                <p>
                    Double Dragon es un videojuego <span class="sub"> beat 'em up </span> de desplazamiento <span
                        class="sub"> lateral </span> lanzado en 1987, desarrollado por Technōs Japan y distribuido en
                    América del Norte y Europa por Taito Corporation. Double Dragon se considera uno de los primeros
                    ejemplares exitosos del género, lo que resultó en la creación de <span class="sub">dos
                        secuelas</span>
                    arcade y varios
                    spin-offs, además de inspirar a otras compañías a crear sus propios beat 'em ups. <br><br>
                    El juego tuvo grandes influencias de películas de artes marciales, especialmente con <span
                        class="sub">Bruce Lee</span>, como
                    <span class="sub">Operación Dragón</span>; y una ambientación <span
                        class="sub">postapocalíptica</span> basada en el popular
                    anime
                    <span class="sub">El Puño de la Estrella del Norte</span>. Double Dragon fue notable por su
                    jugabilidad <span class="sub">cooperativa multijugador</span>, que permitía a los amigos unirse y
                    jugar juntos. También introdujo varias
                    características innovadoras para su época, como la capacidad de <span class="sub">agarrar</span> y
                    <span class="sub">lanzar</span> enemigos, así como
                    peligros ambientales que podían ser usados contra los oponentes.
                </p>
            </div>

            <!-- Info -->
            <figure class="contenedor-seccion">
                <div class="contenedor-img">
                    <a href="" target="_blank" title=""> <!---->
                        <img src="https://i.ytimg.com/vi/OI_ZsgCgDNM/maxresdefault.jpg" alt="DoubleDragon"
                            class="img-seccion"> <!---->
                    </a>
                </div>

                <div class="center">
                    <div class="contenedor-parrafo">
                        <p style="margin-top: 0px; margin-bottom: 0px;">
                        <ul style="padding: 0px 0px 0px 10px;">
                            <p style="margin: 0px;">
                                El jugador toma el control del artista marcial <span class="sub">Billy Lee</span>
                                "Hammer", o de su hermano
                                gemelo <span class="sub">Jimmy Lee</span> "Spike", quienes están en una
                                misión para rescatar a la novia de <span class="sub">Billy</span>, <span
                                    class="sub">Marian</span>, quien ha sido secuestrada por la
                                pandilla <span class="sub">Black Warriors</span>. El jugador controla a Billy o Jimmy (o
                                a ambos en modo de
                                dos jugadores) mientras luchan contra oleadas de enemigos
                                usando <span class="sub">puñetazos</span>, <span class="sub">patadas</span> y
                                varios <span class="sub">objetos</span> encontrados a lo largo de los niveles. <br> <br>
                            </p>

                            <li>
                                <p style="margin: 0px;">
                                    Puedes moverte hacia la izquierda o derecha para <span class="sub">avanzar</span> o
                                    <span class="sub">retroceder</span>, y hacia
                                    arriba o abajo para <span class="sub">esquivar ataques</span> o <span
                                        class="sub">recoger objetos</span>. Cada personaje emplea
                                    puñetazos y patadas para luchar contra los enemigos. Cada golpe tiene su propio
                                    alcance y velocidad, así que experimenta para encontrar la <span
                                        class="sub">combinación</span> más efectiva.
                                    <br> <br>
                                </p>
                            </li>

                            <li>
                                <p style="margin: 0px;">
                                    <span class="sub">Acércate</span> a los enemigos y utiliza la función de agarre para
                                    <span class="sub">sujetarlos</span>. Una vez
                                    agarrados, puedes <span class="sub">lanzarlos</span> en la dirección que elijas, lo
                                    que puede ser útil para
                                    <span class="sub">despejar</span> el camino o <span class="sub">golpear</span> a
                                    otros enemigos. <br> <br>
                                </p>
                            </li>

                            <li>
                                <p style="margin: 0px;">
                                    A lo largo del juego, encontrarás armas como <span class="sub">palos</span>, <span
                                        class="sub">cuchillos</span> y <span class="sub">látigos</span>. Recoge
                                    estas armas para aumentar tu <span class="sub">poder de ataque</span> y usa su <span
                                        class="sub">alcance</span> y <span class="sub">capacidad de daño</span>
                                    para tu ventaja. <br> <br>
                                </p>
                            </li>

                            <li>
                                <p style="margin: 0px;">
                                    Cada nivel presenta su propio conjunto de <span class="sub">desafíos</span> y <span
                                        class="sub">enemigos únicos</span>, y los
                                    jugadores deben superarlos para avanzar en la historia y finalmente rescatar a
                                    Marian. <br> <br>
                                </p>
                            </li>

                            <li>
                                <p style="margin: 0px;">
                                    El jugador comienza el juego con una cierta cantidad de <span class="sub">vidas
                                        extra</span> y un <span class="sub">indicador de vida</span> que se agota a
                                    medida que el jugador <span class="sub">recibe golpes</span> de los enemigos. Si el
                                    indicador de vida se agota o el <span class="sub">límite de tiempo</span> llega a
                                    cero, el jugador <span class="sub">perderá</span> una vida.
                                </p>
                            </li>
                        </ul>
                        </p>
                    </div>
                </div>
            </figure>

            <span class="center">
                <h4 class="titulo" style="margin: 10px 0px 0px 0px; padding: 5px;">

                    <nav class="secciones">
                        <table style="width: 100%;">
                            <tr>
                                <td>
                                    <a href="https://vimm.net/vault/91481" target="_blank" class="link"> Jugar </a>
                                </td>

                                <td>
                                    <a href="https://www.youtube.com/watch?v=rTy6NS7Bciw" target="_blank" class="link">
                                        GamePlay </a>
                                </td>
                            </tr>
                        </table>
                    </nav>

                </h4>
            </span>
        </section>

        <br>

        <!-- Mario Bros -->
        <section class="seccion-mario">
            <h2 class="tituloizq"> Mario Bros</h2>

            <div class="parrafo">
                <p>
                    Mario Bros es un videojuego arcade desarrollado por <span class="sub"> Nintendo </span> y lanzado
                    el 21
                    de junio de 1983. Fue creado por <span class="sub">Shigeru Miyamoto</span> y <span
                        class="sub">Gunpei Yokoi</span>, el ingeniero jefe de Nintendo. Fue la <span class="sub">tercera
                        aparición</span> de
                    Mario además de la <span class="sub">primera aparición</span> con su <span class="sub">nombre
                        definitivo</span>, ya que en <span style="color: rgb(139, 80, 11);">Donkey Kong</span> (1981)
                    aparecía
                    bajo el seudónimo de <span style="color: rgb(46, 46, 241);">Jumpman</span>. <br><br>
                    Los elementos introducidos en Mario Bros como las <span class="sub">tuberías</span>, <span
                        class="sub">monedas de bonificación giratorias</span>,
                    <span class="sub">tortugas</span> que se pueden voltear sobre sus espaldas y <span
                        style="color: green;">Luigi</span>, se trasladaron a <span class="sub">Super Mario Bros</span>
                    (1985),
                    y se convirtieron en elementos básicos de la franquicia.
                </p>
            </div>

            <!-- Info -->
            <figure class="contenedor-seccion">
                <div class="contenedor-img">
                    <a href="" target="_blank" title=""> <!---->
                        <img src="https://static.euronews.com/articles/stories/07/75/00/94/1440x810_cmsv2_c6b7f87c-e7d0-5737-9fe1-a94668aea9c2-7750094.jpg"
                            alt="Mario" class="img-seccion"> <!---->
                    </a>
                </div>

                <div class="center">
                    <div class="contenedor-parrafo">
                        <p style="margin-top: 0px; margin-bottom: 0px;">
                        <ul style="padding: 0px 0px 0px 10px;">
                            <p style="margin: 0px;">
                                Asumes el papel de <span class="sub">Mario</span> (o <span
                                    style="color: green;">Luigi</span> en
                                modo de <span class="sub">dos jugadores</span>) mientras trabajan en un
                                alcantarillado, enfrentándose a diversas criaturas, como <span
                                    class="sub">tortugas</span> y <span class="sub">cangrejos</span>, conocidas
                                como "Koopas" y "Sidesteppers", respectivamente. <br><br>
                            </p>

                            <li>
                                <p style="margin: 0px;">
                                    El objetivo principal es eliminar a <span class="sub">todas las criaturas</span> de
                                    cada nivel golpeando el suelo <span class="sub">debajo de ellas</span> y luego
                                    recogiendo los <span class="sub">objetos</span> que dejan caer, como <span
                                        class="sub">monedas</span> o <span class="sub">puntos</span>. El juego
                                    también presenta obstáculos
                                    en forma de <span class="sub">tuberías</span> y <span class="sub">bloques</span>,
                                    algunos de los cuales contienen sorpresas como <span class="sub">monedas
                                        adicionales</span> o <span class="sub">enemigos</span>. <br> <br>
                                </p>
                            </li>

                            <li>
                                <p style="margin: 0px;">
                                    Puedes moverte de <span class="sub">izquierda</span> a <span
                                        class="sub">derecha</span> en la pantalla. También puedes <span
                                        class="sub">saltar</span>, los
                                    enemigos se desplazarán por las <span class="sub">plataformas</span>, y tu objetivo
                                    es <span class="sub">eliminarlos</span>. Para
                                    hacerlo, debes <span class="sub">golpear el suelo debajo de ellos</span>. Una vez
                                    que estén sobre una
                                    plataforma, <span class="sub">golpéala desde abajo</span> para
                                    <span class="sub">voltearlos</span>. Luego, corre hacia ellos y toca el enemigo
                                    volteado para <span class="sub">eliminarlo</span>.
                                    <br> <br>
                                </p>
                            </li>

                            <li>
                                <p style="margin: 0px;">
                                    Después de <span class="sub">eliminar a un enemigo</span>, dejará caer un <span
                                        class="sub">objeto</span>.
                                    Corre hacia él para
                                    <span class="sub">recogerlo</span>. Los objetos pueden ser <span
                                        class="sub">monedas</span>, que te otorgan
                                    <span class="sub">puntos</span>, o bonus como las
                                    <span class="sub">estrellas</span>, que te proporcionan pequeños tiempos de
                                    <span class="sub">invulnerabilidad</span>. <br><br>
                                </p>
                            </li>

                            <li>
                                <p style="margin: 0px;">
                                    Cada nivel tiene un <span class="sub">límite de tiempo</span>. Debes eliminar a
                                    todos los enemigos antes de
                                    que el <span class="sub">tiempo se agote</span>. Si no lo haces, aparecerá un
                                    <span class="sub">enemigo rojo</span> más <span class="sub">rápido</span> y
                                    <span class="sub">agresivo</span>, lo que complica la tarea. <br><br>
                                </p>
                            </li>

                            <li>
                                <p style="margin: 0px;">
                                    Después de completar ciertos niveles, puedes acceder a <span class="sub">niveles
                                        bonus</span> donde tienes la
                                    oportunidad de ganar <span class="sub">puntos extra</span>. En el modo de <span
                                        class="sub">dos jugadores</span>, el segundo jugador
                                    controlará a <span style="color: green;">Luigi</span>. Ambos jugadores pueden
                                    trabajar juntos
                                    para eliminar enemigos y
                                    completar niveles.
                                </p>
                            </li>
                        </ul>
                        </p>
                    </div>
                </div>
            </figure>

            <span class="center">
                <h4 class="titulo" style="margin: 10px 0px 0px 0px; padding: 5px;">

                    <nav class="secciones">
                        <table style="width: 100%;">
                            <tr>
                                <td>
                                    <a href="https://vimm.net/vault/91511" target="_blank" class="link"> Jugar </a>
                                </td>

                                <td>
                                    <a href="https://www.youtube.com/watch?v=ly8DofqCuOs" target="_blank" class="link">
                                        GamePlay </a>
                                </td>
                            </tr>
                        </table>
                    </nav>

                </h4>
            </span>
        </section>

        <div class="center">
            <h2 class="titulo"> ¿Que tanto te gustaron estos juegos? </h2>
        </div>
        <section class="center">
            <form class="form">
                <table id="Tabla" style="width: 100%;">
                    <tr>
                        <th></th>
                        <th> 1.0 <br>-<br> 3.0 </th>
                        <th> 3.0 <br>-<br> 5.0 </th>
                        <th> 5.0 <br>-<br> 7.0 </th>
                    </tr>
                    <tr>
                        <th>Pac-Man</th>
                        <td onclick="selectRadio('Pacman1.0-3.0')">
                            <input id="Pacman1.0-3.0" name="Pacman" type="radio">
                        </td>

                        <td onclick="selectRadio('Pacman3.0-5.0')">
                            <input id="Pacman3.0-5.0" name="Pacman" type="radio">
                        </td>

                        <td onclick="selectRadio('Pacman5.0-7.0')">
                            <input id="Pacman5.0-7.0" name="Pacman" type="radio">
                        </td>
                    </tr>

                    <tr>
                        <th>Donkey Kong</th>
                        <td onclick="selectRadio('DK1.0-3.0')">
                            <input id="DK1.0-3.0" name="DK" type="radio">
                        </td>

                        <td onclick="selectRadio('DK3.0-5.0')">
                            <input id="DK3.0-5.0" name="DK" type="radio">
                        </td>

                        <td onclick="selectRadio('DK5.0-7.0')">
                            <input id="DK5.0-7.0" name="DK" type="radio">
                        </td>
                    </tr>

                    <tr>
                        <th>1942</th>
                        <td onclick="selectRadio('19421.0-3.0')">
                            <input id="19421.0-3.0" name="1942" type="radio">
                        </td>

                        <td onclick="selectRadio('19423.0-5.0')">
                            <input id="19423.0-5.0" name="1942" type="radio">
                        </td>

                        <td onclick="selectRadio('19425.0-7.0')">
                            <input id="19425.0-7.0" name="1942" type="radio">
                        </td>
                    </tr>

                    <tr>
                        <th>Double Dragon</th>
                        <td onclick="selectRadio('DD1.0-3.0')">
                            <input id="DD1.0-3.0" name="DD" type="radio">
                        </td>

                        <td onclick="selectRadio('DD3.0-5.0')">
                            <input id="DD3.0-5.0" name="DD" type="radio">
                        </td>

                        <td onclick="selectRadio('DD5.0-7.0')">
                            <input id="DD5.0-7.0" name="DD" type="radio">
                        </td>
                    </tr>

                    <tr>
                        <th>Mario Bros</th>
                        <td onclick="selectRadio('Mario1.0-3.0')">
                            <input id="Mario1.0-3.0" name="Mario" type="radio">
                        </td>

                        <td onclick="selectRadio('Mario3.0-5.0')">
                            <input id="Mario3.0-5.0" name="Mario" type="radio">
                        </td>

                        <td onclick="selectRadio('Mario5.0-7.0')">
                            <input id="Mario5.0-7.0" name="Mario" type="radio">
                        </td>
                    </tr>
                </table>

                <div class="center">
                    <input type="submit" value="Enviar" class="input"
                        onclick="alert('Gracias calificar los juegos vistos, los datos serán procesados y se hará una lista más sintetizada con los resultados obtenidos.')">
                </div>
            </form>
        </section>
    </article>


    <hr style="margin-bottom: 10px;">
    <div class="center">
        <footer class="footer" style="padding-left: 100px; padding-right: 100px;">
            <table style="width: 100%;">
                <tr style="font-size: 15px;">
                    <td class="center">
                        <a href="" class="link-footer"> Home </a>
                    </td>
                </tr>
            </table>
        </footer>
    </div>
</body>



</html>




 
