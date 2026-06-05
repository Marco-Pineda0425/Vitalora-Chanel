# Vitalora-Chanel
Creación de la comunidad Vitalora
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vitalora - Suplementos Inteligentes</title>
    <style>
        /* --- ESTILOS GENERALES Y PALETA CÁLIDA --- */
        :root {
            --primary: #D97706; /* Ámbar / Naranja cálido */
            --primary-light: #FEF3C7; /* Crema suave */
            --secondary: #78350F; /* Marrón terracota oscuro */
            --accent: #EF4444; /* Coral vibrante */
            --bg-gradient: linear-gradient(135deg, #FFFBEB 0%, #FDE68A 100%);
            --text-dark: #1F2937;
            --white: #FFFFFF;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background: var(--bg-gradient);
            color: var(--text-dark);
            min-height: 100vh;
            overflow-x: hidden;
        }

        /* --- BARRA DE NAVEGACIÓN --- */
        .navbar {
            background-color: var(--white);
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 5%;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .brand {
            font-size: 1.8rem;
            font-weight: bold;
            color: var(--secondary);
            letter-spacing: 1px;
        }

        .brand span {
            color: var(--primary);
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--text-dark);
            font-weight: 600;
            transition: color 0.3s ease;
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        /* --- CONTENEDOR PRINCIPAL --- */
        .container {
            max-width: 800px;
            margin: 3rem auto;
            padding: 0 2rem;
        }

        .hero-text {
            text-align: center;
            margin-bottom: 2.5rem;
            opacity: 0;
            transform: translateY(30px);
            animation: fadeInUp 1s ease forwards;
        }

        .hero-text h1 {
            color: var(--secondary);
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
        }

        /* --- FORMULARIO CON MOVIMIENTO --- */
        .form-card {
            background: var(--white);
            padding: 2.5rem;
            border-radius: 15px;
            box-shadow: 0 10px 25px rgba(120, 53, 15, 0.15);
            opacity: 0;
            transform: translateY(40px);
            animation: fadeInUp 1s ease 0.3s forwards;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        /* Efecto Hover interactivo en la tarjeta */
        .form-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(120, 53, 15, 0.2);
        }

        .form-group {
            margin-bottom: 1.5rem;
            position: relative;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            color: var(--secondary);
            font-weight: 600;
            font-size: 0.95rem;
        }

        .form-group input, .form-group textarea {
            width: 100%;
            padding: 0.8rem 1rem;
            border: 2px solid #E5E7EB;
            border-radius: 8px;
            outline: none;
            font-size: 1rem;
            transition: all 0.3s ease;
            background-color: #FAFAFA;
        }

        /* Movimiento y enfoque de los inputs */
        .form-group input:focus, .form-group textarea:focus {
            border-color: var(--primary);
            background-color: var(--white);
            box-shadow: 0 0 8px rgba(217, 119, 6, 0.2);
            transform: scale(1.01);
        }

        .btn-submit {
            width: 100%;
            background-color: var(--primary);
            color: var(--white);
            border: none;
            padding: 1rem;
            font-size: 1.1rem;
            font-weight: bold;
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 4px 10px rgba(217, 119, 6, 0.3);
        }

        .btn-submit:hover {
            background-color: var(--secondary);
            box-shadow: 0 6px 15px rgba(120, 53, 15, 0.4);
            transform: translateY(-2px);
        }

        .btn-submit:active {
            transform: translateY(1px);
        }

        /* --- ANIMACIONES --- */
        @keyframes fadeInUp {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* --- RESPONSIVO --- */
        @media (max-width: 600px) {
            .navbar {
                flex-direction: column;
                gap: 1rem;
            }
            .nav-links {
                gap: 1.5rem;
            }
            .form-card {
                padding: 1.5rem;
            }
        }
    </style>
</head>
<body>

    <nav class="navbar">
        <div class="brand">Vita<span>lora</span></div>
        <ul class="nav-links">
            <li><a href="#inicio">Inicio</a></li>
            <li><a href="#productos">Suplementos</a></li>
            <li><a href="#contacto">Contacto</a></li>
        </ul>
    </nav>

    <div class="container">
        <div class="hero-text">
            <h1>Bienvenido a Vitalora</h1>
            <p>Conecta con tu bienestar integral y comparte tu contenido</p>
        </div>

        <div class="form-card" id="contacto">
            <form id="vitaloraForm">
                
                <div class="form-group">
                    <label for="nombre">Nombre</label>
                    <input type="text" id="nombre" name="Nombre" placeholder="Tu nombre completo" required>
                </div>

                <div class="form-group">
                    <label for="fechaHoy">Fecha de hoy</label>
                    <input type="text" id="fechaHoy" name="Fecha de hoy" readonly>
                </div>

                <div class="form-group">
                    <label for="diaSemana">Día de la Semana</label>
                    <input type="text" id="diaSemana" name="Día de la Semana" readonly>
                </div>

                <div class="form-group">
                    <label for="evangelioVideo">Evangelio Video (Enlace / Comentario)</label>
                    <input type="url" id="evangelioVideo" name="Evangelio Video" placeholder="https://ejemplo.com/video" required>
                </div>

                <div class="form-group">
                    <label for="evangelioAudio">Evangelio Audio (Enlace / Comentario)</label>
                    <input type="url" id="evangelioAudio" name="Evangelio Audio" placeholder="https://ejemplo.com/audio" required>
                </div>

                <button type="submit" class="btn-submit">Enviar Registro</button>
            </form>
        </div>
    </div>

    <script>
        document.addEventListener("DOMContentLoaded", function() {
            // 1. OBTENER FECHA Y DÍA ACTUAL AUTOMÁTICAMENTE
            const opcionesFecha = { year: 'numeric', month: 'long', day: 'numeric' };
            const opcionesDia = { weekday: 'long' };
            
            const hoy = new Date();
            
            // Formatear en español de México
            const fechaFormateada = hoy.toLocaleDateString('es-MX', opcionesFecha);
            let diaFormateada = hoy.toLocaleDateString('es-MX', opcionesDia);
            
            // Capitalizar la primera letra del día (ej: "jueves" -> "Jueves")
            diaFormateada = diaFormateada.charAt(0).toUpperCase() + diaFormateada.slice(1);

            // Asignar valores a los campos correspondientes del JSON
            document.getElementById("fechaHoy").value = fechaFormateada;
            document.getElementById("diaSemana").value = diaFormateada;

            // 2. INTERACTIVIDAD DE ENTRADA EN LOS INPUTS (Efecto focus dinámico adicional)
            const inputs = document.querySelectorAll(".form-group input");
            inputs.forEach(input => {
                input.addEventListener("focus", () => {
                    input.parentElement.style.transform = "translateX(5px)";
                    input.parentElement.style.transition = "transform 0.3s ease";
                });
                input.addEventListener("blur", () => {
                    input.parentElement.style.transform = "translateX(0px)";
                });
            });

            // 3. CAPTURA DEL FORMULARIO EN FORMATO JSON
            const formulario = document.getElementById("vitaloraForm");
            formulario.addEventListener("submit", function(e) {
                e.preventDefault(); // Evita la recarga de página

                // Creación del objeto final según la estructura solicitada
                const resultadoJSON = {
                    "Nombre": document.getElementById("nombre").value,
                    "Fecha de hoy": document.getElementById("fechaHoy").value,
                    "Día de la Semana": document.getElementById("diaSemana").value,
                    "Evangelio Video": document.getElementById("evangelioVideo").value,
                    "Evangelio Audio": document.getElementById("evangelioAudio").value
                };

                // Mostrar resultado en consola con animación de éxito
                console.log("%c¡Datos capturados exitosamente en JSON!", "color: #D97706; font-weight: bold; font-size: 1.2rem;");
                console.log(JSON.stringify(resultadoJSON, null, 4));
                
                alert("¡Datos enviados correctamente! Revisa la consola del navegador para ver la estructura JSON generada.");
                formulario.reset();
                
                // Mantener los campos automáticos fijos después del reset
                document.getElementById("fechaHoy").value = fechaFormateada;
                document.getElementById("diaSemana").value = diaFormateada;
            });
        });
    </script>
</body>
</html>
