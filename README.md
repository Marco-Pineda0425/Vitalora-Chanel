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

        /* Estilo para los campos automáticos deshabilitados */
        .form-group input[readonly] {
            background-color: #F3F4F6;
            color: #6B7280;
            cursor: not-allowed;
        }

        /* Movimiento y enfoque de los inputs activos */
        .form-group input:not([readonly]):focus {
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

        .btn-submit:disabled {
            background-color: #9CA3AF;
            cursor: not-allowed;
            box-shadow: none;
            transform: none;
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

    <!-- BARRA DE NAVEGACIÓN -->
    <nav class="navbar">
        <div class="brand">Vita<span>lora</span></div>
        <ul class="nav-links">
            <li><a href="#inicio">Inicio</a></li>
            <li><a href="#productos">Suplementos</a></li>
            <li><a href="#contacto">Contacto</a></li>
        </ul>
    </nav>

    <!-- CONTENEDOR PRINCIPAL -->
    <div class="container">
        <div class="hero-text">
            <h1>Bienvenido a Vitalora</h1>
            <p>Conecta con tu bienestar integral y comparte tu contenido</p>
        </div>

        <div class="form-card" id="contacto">
            <form id="vitaloraForm">
                
                <!-- Nombre -->
                <div class="form-group">
                    <label for="nombre">Nombre</label>
                    <input type="text" id="nombre" name="Nombre" placeholder="Tu nombre completo" required>
                </div>

                <!-- Fecha de hoy (Autocompletada por JavaScript) -->
                <div class="form-group">
                    <label for="fechaHoy">Fecha de hoy</label>
                    <input type="text" id="fechaHoy" name="Fecha de hoy" readonly>
                </div>

                <!-- Día de la Semana (Autocompletado por JavaScript) -->
                <div class="form-group">
                    <label for="diaSemana">Día de la Semana</label>
                    <input type="text" id="diaSemana" name="Día de la Semana" readonly>
                </div>

                <!-- Evangelio Video -->
                <div class="form-group">
                    <label for="evangelioVideo">Evangelio Video (Enlace / Comentario)</label>
                    <input type="url" id="evangelioVideo" name="Evangelio Video" placeholder="https://ejemplo.com/video" required>
                </div>

                <!-- Evangelio Audio -->
                <div class="form-group">
                    <label for="evangelioAudio">Evangelio Audio (Enlace / Comentario)</label>
                    <input type="url" id="evangelioAudio" name="Evangelio Audio" placeholder="https://ejemplo.com/audio" required>
                </div>

                <!-- Botón de Envío -->
                <button type="submit" class="btn-submit" id="btnEnviar">Enviar Registro</button>
            </form>
        </div>
    </div>

    <!-- SCRIPT DE INTERACTIVIDAD AUTOMÁTICA Y CONEXIÓN WEBHOOK -->
    <script>
        document.addEventListener("DOMContentLoaded", function() {
            
            // 1. ASIGNACIÓN AUTOMÁTICA DE FECHA Y DÍA
            const opcionesFecha = { year: 'numeric', month: 'long', day: 'numeric' };
            const opcionesDia = { weekday: 'long' };
            const hoy = new Date();
            
            const fechaFormateada = hoy.toLocaleDateString('es-MX', opcionesFecha);
            let diaFormateada = hoy.toLocaleDateString('es-MX', opcionesDia);
            
            // Capitalizar la primera letra del día
            diaFormateada = diaFormateada.charAt(0).toUpperCase() + diaFormateada.slice(1);

            // Inyectar valores iniciales fijos
            document.getElementById("fechaHoy").value = fechaFormateada;
            document.getElementById("diaSemana").value = diaFormateada;

            // 2. EFECTOS VISUALES DE MOVIMIENTO EN LOS INPUTS ACTIVOS
            const inputs = document.querySelectorAll(".form-group input:not([readonly])");
            inputs.forEach(input => {
                input.addEventListener("focus", () => {
                    input.parentElement.style.transform = "translateX(5px)";
                    input.parentElement.style.transition = "transform 0.3s ease";
                });
                input.addEventListener("blur", () => {
                    input.parentElement.style.transform = "translateX(0px)";
                });
            });

            // 3. ENVÍO LÓGICO DE LOS DATOS HACIA EL WEBHOOK
            const formulario = document.getElementById("vitaloraForm");
            const botonEnviar = document.getElementById("btnEnviar");

            formulario.addEventListener("submit", function(e) {
                e.preventDefault(); // Detiene el refresco de página involuntario

                // Modificar estado del botón durante la carga
                botonEnviar.textContent = "Procesando envío...";
                botonEnviar.disabled = true;

                // Creación de la estructura JSON idéntica a la solicitada
                const resultadoJSON = {
                    "Nombre": document.getElementById("nombre").value,
                    "Fecha de hoy": document.getElementById("fechaHoy").value,
                    "Día de la Semana": document.getElementById("diaSemana").value,
                    "Evangelio Video": document.getElementById("evangelioVideo").value,
                    "Evangelio Audio": document.getElementById("evangelioAudio").value
                };

                // URL del Webhook de Make (Reemplaza con el tuyo propio)
                const urlWebhook = "AQUÍ_PEGA_TU_URL_DE_WEBHOOK"; 

                // Ejecución del envío mediante Fetch API
                fetch(urlWebhook, {
                    method: "POST",
                    headers: {
                        "Content-Type": "application/json"
                    },
                    body: JSON.stringify(resultadoJSON)
                })
                .then(respuesta => {
                    if(respuesta.ok || respuesta.status === 200) {
                        alert("¡Datos enviados con éxito al Webhook de Make!");
                        formulario.reset();
                    } else {
                        alert("El servidor Webhook recibió los datos pero devolvió un error de procesamiento.");
                    }
                })
                .catch(error => {
                    console.error("Error al enviar:", error);
                    alert("Hubo un error de conexión al enviar al Webhook. Revisa la URL asignada.");
                })
                .finally(() => {
                    // Restablecer el estado del botón y recuperar campos de fecha/día automáticos
                    botonEnviar.textContent = "Enviar Registro";
                    botonEnviar.disabled = false;
                    document.getElementById("fechaHoy").value = fechaFormateada;
                    document.getElementById("diaSemana").value = diaFormateada;
                });
            });
        });
    </script>
</body>
</html>
