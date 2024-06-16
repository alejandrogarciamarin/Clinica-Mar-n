<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Clínica Dental - Actividades y Servicios</title>
    <style>
        body { font-family: Arial, sans-serif; margin: 0; padding: 0; }
        header { background-color: #4CAF50; color: white; padding: 1em; text-align: center; }
        nav ul { list-style-type: none; margin: 0; padding: 0; overflow: hidden; }
        nav ul li { float: left; }
        nav ul li a { display: block; color: white; text-align: center; padding: 14px 16px; text-decoration: none; }
        nav ul li a:hover { background-color: #3e8e41; }
        section { padding: 20px; }
        footer { background-color: #4CAF50; color: white; text-align: center; padding: 10px; position: fixed; bottom: 0; width: 100%; }
        form { margin-top: 20px; }
        label { display: block; margin-bottom: 5px; }
        input, textarea { width: 100%; padding: 10px; margin-bottom: 10px; }
        button { background-color: #4CAF50; color: white; border: none; padding: 10px 20px; cursor: pointer; }
        button:hover { background-color: #45a049; }
        .comentario { border-top: 1px solid #ccc; padding-top: 10px; margin-top: 10px; }
    </style>
</head>
<body>
    <header>
        <h1>Clínica Dental</h1>
        <nav>
            <ul>
                <li><a href="#servicios">Servicios</a></li>
                <li><a href="#galeria">Galería</a></li>
                <li><a href="#formulario">Contacto</a></li>
                <li><a href="#comentarios">Comentarios</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section id="servicios">
            <h2>Servicios</h2>
            <p>Descripción de los servicios que ofrece la clínica dental.</p>
            <ul>
                <li>Ortodoncia</li>
                <li>Implantes Dentales</li>
                <li>Blanqueamiento Dental</li>
                <li>...</li>
            </ul>
            <img src="https://via.placeholder.com/400" alt="Ortodoncia">
        </section>

        <section id="galeria">
            <h2>Galería</h2>
            <p>Imágenes de la clínica dental y del equipo médico en acción.</p>
            <img src="https://via.placeholder.com/400" alt="Galería 1">
            <img src="https://via.placeholder.com/400" alt="Galería 2">
        </section>

        <section id="formulario">
            <h2>Contacto</h2>
            <p>Complete el siguiente formulario para más información:</p>
            <form>
                <label for="nombre">Nombre:</label>
                <input type="text" id="nombre" name="nombre" required>
                <label for="apellidos">Apellidos:</label>
                <input type="text" id="apellidos" name="apellidos" required>
                <label for="telefono">Teléfono:</label>
                <input type="tel" id="telefono" name="telefono" required>
                <label for="correo">Correo electrónico:</label>
                <input type="email" id="correo" name="correo" required>
                <button type="submit">Enviar</button>
            </form>
        </section>

        <section id="comentarios">
            <h2>Comentarios</h2>
            <div id="comentarios-lista">
                <!-- Aquí se mostrarán los comentarios dinámicamente -->
            </div>
            <form id="form-comentario">
                <label for="nombre-comentario">Nombre:</label>
                <input type="text" id="nombre-comentario" name="nombre-comentario" required>
                <label for="mensaje-comentario">Comentario:</label>
                <textarea id="mensaje-comentario" name="mensaje-comentario" rows="3" required></textarea>
                <button type="submit">Enviar Comentario</button>
            </form>
        </section>
    </main>

    <footer>
        <p>&copy; 2024 Clínica Dental. Todos los derechos reservados.</p>
    </footer>

    <script>
        // Script JavaScript para manejar el envío de comentarios
        document.getElementById('form-comentario').addEventListener('submit', function(event) {
            event.preventDefault(); // Prevenir envío del formulario por defecto
            let nombre = document.getElementById('nombre-comentario').value;
            let mensaje = document.getElementById('mensaje-comentario').value;
            let comentariosLista = document.getElementById('comentarios-lista');
            let nuevoComentario = document.createElement('div');
            nuevoComentario.classList.add('comentario');
            nuevoComentario.innerHTML = `<p><strong>${nombre}</strong>: ${mensaje}</p>`;
            comentariosLista.appendChild(nuevoComentario);
            document.getElementById('form-comentario').reset();
        });
    </script>
</body>
</html>

