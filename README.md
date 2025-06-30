<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Clientiia Agencia de IA para Inmobiliarias</title>
    <!-- Enlace a Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Configuración de Tailwind para usar la fuente Inter -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        inter: ['Inter', 'sans-serif'],
                    },
                }
            }
        }
    </script>
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f8f8f8; /* Un fondo suave */
        }
        /* Estilos personalizados para el CTA */
        .cta-button {
            transition: all 0.3s ease;
        }
        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }
    </style>
</head>
<body class="text-gray-800">
    <!-- Sección de Cabecera (Header) -->
    <header class="bg-white shadow-md py-4 px-6 flex justify-between items-center fixed top-0 left-0 w-full z-10">
        <div class="text-2xl font-bold text-indigo-700">
            Agencia IA Inmobiliaria
        </div>
        <nav class="hidden md:flex space-x-6">
            <a href="#servicios" class="text-gray-600 hover:text-indigo-700 font-medium">Servicios</a>
            <a href="#testimonios" class="text-gray-600 hover:text-indigo-700 font-medium">Testimonios</a>
            <a href="#nosotros" class="text-gray-600 hover:text-indigo-700 font-medium">Nosotros</a>
            <a href="#contacto" class="text-gray-600 hover:text-indigo-700 font-medium">Contacto</a>
            <a href="#agenda" class="bg-indigo-600 text-white px-4 py-2 rounded-lg hover:bg-indigo-700 transition duration-300">Agenda una Sesión</a>
        </nav>
        <!-- Menú móvil (oculto por defecto) -->
        <div class="md:hidden">
            <button id="menu-button" class="text-gray-600 hover:text-indigo-700 focus:outline-none">
                <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path>
                </svg>
            </button>
        </div>
    </header>

    <!-- Menú móvil desplegable -->
    <nav id="mobile-menu" class="fixed top-0 left-0 w-full h-full bg-white z-20 transform -translate-x-full transition-transform duration-300 ease-in-out md:hidden">
        <div class="flex justify-end p-4">
            <button id="close-menu-button" class="text-gray-600 hover:text-indigo-700 focus:outline-none">
                <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
                </svg>
            </button>
        </div>
        <ul class="flex flex-col items-center space-y-6 text-xl mt-10">
            <li><a href="#servicios" class="text-gray-800 hover:text-indigo-700 font-medium" onclick="toggleMobileMenu()">Servicios</a></li>
            <li><a href="#testimonios" class="text-gray-800 hover:text-indigo-700 font-medium" onclick="toggleMobileMenu()">Testimonios</a></li>
            <li><a href="#nosotros" class="text-gray-800 hover:text-indigo-700 font-medium" onclick="toggleMobileMenu()">Nosotros</a></li>
            <li><a href="#contacto" class="text-gray-800 hover:text-indigo-700 font-medium" onclick="toggleMobileMenu()">Contacto</a></li>
            <li><a href="#agenda" class="bg-indigo-600 text-white px-6 py-3 rounded-lg hover:bg-indigo-700 transition duration-300" onclick="toggleMobileMenu()">Agenda una Sesión Gratuita</a></li>
        </ul>
    </nav>


    <!-- Sección Principal (Hero) -->
    <section class="bg-gradient-to-r from-indigo-600 to-purple-700 text-white py-24 md:py-32 px-6 flex items-center justify-center min-h-screen-70 mt-16 md:mt-0">
        <div class="container mx-auto flex flex-col md:flex-row items-center justify-between text-center md:text-left gap-10">
            <div class="md:w-1/2">
                <h1 class="text-4xl md:text-5xl lg:text-6xl font-extrabold leading-tight mb-6">
                    Duplica tus <span class="text-yellow-300">Leads Inmobiliarios</span> con IA
                </h1>
                <p class="text-lg md:text-xl mb-8 opacity-90">
                    Implementamos y gestionamos Asistentes Virtuales IA personalizados.
                    <br class="hidden md:inline">**Pagas solo por los resultados que te generamos.**
                </p>
                <a href="#agenda" class="cta-button bg-yellow-400 text-indigo-900 font-bold py-4 px-8 rounded-full text-lg shadow-lg hover:bg-yellow-300 inline-block transition duration-300 transform hover:scale-105">
                    Agenda una Sesión Estratégica Gratuita
                </a>
            </div>
            <div class="md:w-1/2 flex justify-center md:justify-end">
                <!-- Placeholder para imagen o ilustración -->
                <img src="https://placehold.co/500x350/667EEA/FFFFFF?text=Asistente+IA+Inmobiliario" alt="Ilustración de asistente IA inmobiliario" class="rounded-xl shadow-2xl max-w-full h-auto">
            </div>
        </div>
    </section>

    <!-- Sección de Nuestros Servicios / Cómo Funciona -->
    <section id="servicios" class="py-16 md:py-24 px-6 bg-white">
        <div class="container mx-auto text-center max-w-4xl">
            <h2 class="text-3xl md:text-4xl font-bold mb-12 text-indigo-800">
                ¿Cómo funciona tu Agente Virtual de IA?
            </h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-10 text-left">
                <!-- Beneficio 1 -->
                <div class="p-8 bg-gray-50 rounded-xl shadow-lg border border-gray-100">
                    <div class="text-indigo-600 mb-4 text-5xl">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-12 w-12 mx-auto" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M13 7h8m0 0v8m0-8L11 2m7 5l-7 7m0 0a9 9 0 11-9-9m9 9L2 11" />
                        </svg>
                    </div>
                    <h3 class="text-2xl font-semibold mb-4 text-gray-900">Captación de Leads 24/7</h3>
                    <p class="text-gray-600">
                        Tu agente IA nunca duerme. Responde al instante a consultas, califica a los interesados y capta datos cruciales, 
                        asegurando que ninguna oportunidad se pierda, en cualquier momento del día o de la noche.
                    </p>
                </div>
                <!-- Beneficio 2 -->
                <div class="p-8 bg-gray-50 rounded-xl shadow-lg border border-gray-100">
                    <div class="text-indigo-600 mb-4 text-5xl">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-12 w-12 mx-auto" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.003 12.003 0 002.944 12c0 3.037 1.157 5.82 3.04 8.618A11.955 11.955 0 0112 21.056a11.955 11.955 0 018.618-3.04A12.003 12.003 0 0021.056 12c0-3.037-1.157-5.82-3.04-8.618z" />
                        </svg>
                    </div>
                    <h3 class="text-2xl font-semibold mb-4 text-gray-900">Calificación Automática</h3>
                    <p class="text-gray-600">
                        El Agente Virtual filtra a los curiosos, identificando solo a los leads realmente cualificados y motivados,
                        ahorrándote tiempo y esfuerzo en búsquedas infructuosas.
                    </p>
                </div>
                <!-- Beneficio 3 -->
                <div class="p-8 bg-gray-50 rounded-xl shadow-lg border border-gray-100">
                    <div class="text-indigo-600 mb-4 text-5xl">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-12 w-12 mx-auto" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
                        </svg>
                    </div>
                    <h3 class="text-2xl font-semibold mb-4 text-gray-900">Respuestas Instantáneas</h3>
                    <p class="text-gray-600">
                        De días a segundos. Tu IA responde a preguntas comunes, envía información de propiedades y gestiona citas 
                        al instante, mejorando la experiencia del cliente y la eficiencia.
                    </p>
                </div>
                <!-- Beneficio 4 -->
                <div class="p-8 bg-gray-50 rounded-xl shadow-lg border border-gray-100">
                    <div class="text-indigo-600 mb-4 text-5xl">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-12 w-12 mx-auto" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M8 12h.01M12 12h.01M16 12h.01M21 12c0 4.418-4.03 8-9 8a9.863 9.863 0 01-4.255-.949L3 20l1.395-3.72C3.512 15.042 3 13.574 3 12c0-4.418 4.03-8 9-8s9 3.582 9 8z" />
                        </svg>
                    </div>
                    <h3 class="text-2xl font-semibold mb-4 text-gray-900">Seguimiento Automatizado</h3>
                    <p class="text-gray-600">
                        El Agente Virtual se encarga del seguimiento de leads a través de email, SMS y llamadas inteligentes, 
                        asegurando que cada potencial cliente reciba la atención necesaria en el momento oportuno.
                    </p>
                </div>
                <!-- Beneficio 5 -->
                <div class="p-8 bg-gray-50 rounded-xl shadow-lg border border-gray-100">
                    <div class="text-indigo-600 mb-4 text-5xl">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-12 w-12 mx-auto" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M12 6V4m0 2a2 2 0 100 4m0-4a2 2 0 110 4m-6 8a2 2 0 100-4m0 4a2 2 0 110-4m0 4v2m0-6V4m6 6v10m6-2a2 2 0 100-4m0 4a2 2 0 110-4m0 4v2m0-6V4" />
                        </svg>
                    </div>
                    <h3 class="text-2xl font-semibold mb-4 text-gray-900">Libera tu Tiempo</h3>
                    <p class="text-gray-600">
                        Al automatizar tareas repetitivas, el Agente IA te permite a ti y a tu equipo de ventas
                        enfocaros en lo que realmente importa: cerrar propiedades y maximizar vuestra rentabilidad.
                    </p>
                </div>
                <!-- Beneficio 6 -->
                <div class="p-8 bg-gray-50 rounded-xl shadow-lg border border-gray-100">
                    <div class="text-indigo-600 mb-4 text-5xl">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-12 w-12 mx-auto" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M9 14l6-6m-6 6l6 6M5 18H3a2 2 0 01-2-2V8a2 2 0 012-2h3.5l2-2h4.914a1 1 0 01.707.293l4.086 4.086a1 1 0 01.293.707V18a2 2 0 01-2 2h-3.5l-2 2H9c-1.104 0-2-.896-2-2v-2" />
                        </svg>
                    </div>
                    <h3 class="text-2xl font-semibold mb-4 text-gray-900">Pagas por Resultados</h3>
                    <p class="text-gray-600">
                        Nuestro modelo es justo: solo pagas por los leads cualificados y las conversiones que tu Agente Virtual te ayuda a generar. 
                        Tu éxito es nuestro éxito.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Sección de Casos de Éxito / Testimonios -->
    <section id="testimonios" class="py-16 md:py-24 px-6 bg-indigo-50">
        <div class="container mx-auto text-center max-w-4xl">
            <h2 class="text-3xl md:text-4xl font-bold mb-12 text-indigo-800">
                Lo Que Dicen Nuestros Clientes
            </h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-10">
                <!-- Testimonio 1 -->
                <div class="bg-white p-8 rounded-xl shadow-lg border border-indigo-100">
                    <p class="text-lg italic text-gray-700 mb-6">
                        "¡Increíble! Desde que implementamos el Agente Virtual de IA, nuestras citas con leads cualificados se han duplicado. La automatización es clave y nos ha liberado muchísimo tiempo."
                    </p>
                    <p class="font-semibold text-indigo-700">- María G., Directora de Ventas, Inmobiliaria Estrella</p>
                </div>
                <!-- Testimonio 2 -->
                <div class="bg-white p-8 rounded-xl shadow-lg border border-indigo-100">
                    <p class="text-lg italic text-gray-700 mb-6">
                        "No más tiempo perdido. El asistente IA responde al instante y califica a los clientes por nosotros. Nuestra eficiencia ha mejorado drásticamente. ¡Altamente recomendado!"
                    </p>
                    <p class="font-semibold text-indigo-700">- Juan P., Agente Inmobiliario Independiente</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Sección Sobre Nosotros -->
    <section id="nosotros" class="py-16 md:py-24 px-6 bg-white">
        <div class="container mx-auto text-center max-w-4xl">
            <h2 class="text-3xl md:text-4xl font-bold mb-12 text-indigo-800">
                Quiénes Somos
            </h2>
            <p class="text-lg text-gray-700 leading-relaxed mb-6">
                Somos un equipo apasionado por la **innovación y la eficiencia** en el sector inmobiliario. Fundamos esta agencia
                con la visión de transformar la forma en que los profesionales del sector captan y gestionan sus leads,
                aprovechando el poder de la **Inteligencia Artificial**.
            </p>
            <p class="text-lg text-gray-700 leading-relaxed">
                Nuestra misión es empoderar a agentes y agencias inmobiliarias, ofreciéndoles soluciones "Done-For-You" que les
                permitan **escalar sus operaciones, reducir sus cargas de trabajo y, lo más importante, cerrar más propiedades**
                sin la complejidad de gestionar tecnologías avanzadas. Nos encargamos de todo para que tú te enfoques en tus clientes.
            </p>
        </div>
    </section>

    <!-- Sección de Contacto / CTA Final -->
    <section id="contacto" class="bg-gradient-to-r from-purple-700 to-indigo-600 text-white py-16 md:py-24 px-6">
        <div class="container mx-auto text-center max-w-3xl">
            <h2 class="text-3xl md:text-4xl font-bold mb-8">
                ¿Listo para Duplicar Tus Leads?
            </h2>
            <p class="text-lg md:text-xl mb-10 opacity-90">
                Contáctanos hoy para una sesión estratégica gratuita y descubre cómo la IA puede transformar tu negocio inmobiliario.
            </p>
            <a id="agenda" href="#" class="cta-button bg-yellow-400 text-indigo-900 font-bold py-4 px-10 rounded-full text-xl shadow-lg hover:bg-yellow-300 inline-block transition duration-300 transform hover:scale-105">
                Agenda Tu Sesión Gratuita Ahora
            </a>
            <p class="text-sm mt-8 opacity-80">
                (Este enlace te llevará a nuestro calendario para que elijas el mejor momento)
            </p>
            <!-- Formulario de Contacto (alternativa si no quieren agendar directamente) -->
            <div class="mt-12 p-8 bg-white text-gray-800 rounded-xl shadow-2xl">
                <h3 class="text-2xl font-bold mb-6 text-indigo-800">O Envíanos un Mensaje Directo</h3>
                <form action="#" method="POST" class="space-y-6">
                    <div>
                        <label for="nombre" class="sr-only">Nombre Completo</label>
                        <input type="text" name="nombre" id="nombre" autocomplete="name" required
                               class="w-full px-5 py-3 border border-gray-300 rounded-lg placeholder-gray-500 focus:ring-indigo-500 focus:border-indigo-500"
                               placeholder="Tu Nombre Completo">
                    </div>
                    <div>
                        <label for="email" class="sr-only">Correo Electrónico</label>
                        <input id="email" name="email" type="email" autocomplete="email" required
                               class="w-full px-5 py-3 border border-gray-300 rounded-lg placeholder-gray-500 focus:ring-indigo-500 focus:border-indigo-500"
                               placeholder="Tu Correo Electrónico">
                    </div>
                    <div>
                        <label for="telefono" class="sr-only">Número de Teléfono</label>
                        <input type="tel" name="telefono" id="telefono" autocomplete="tel"
                               class="w-full px-5 py-3 border border-gray-300 rounded-lg placeholder-gray-500 focus:ring-indigo-500 focus:border-indigo-500"
                               placeholder="Número de Teléfono (opcional)">
                    </div>
                    <div>
                        <label for="mensaje" class="sr-only">Tu Mensaje</label>
                        <textarea id="mensaje" name="mensaje" rows="4" required
                                  class="w-full px-5 py-3 border border-gray-300 rounded-lg placeholder-gray-500 focus:ring-indigo-500 focus:border-indigo-500"
                                  placeholder="Cuéntanos más sobre tu negocio inmobiliario y cómo podemos ayudarte..."></textarea>
                    </div>
                    <button type="submit"
                            class="w-full bg-indigo-600 text-white font-bold py-3 px-6 rounded-lg text-lg shadow-md hover:bg-indigo-700 transition duration-300">
                        Enviar Mensaje
                    </button>
                </form>
            </div>
        </div>
    </section>

    <!-- Sección de Pie de Página (Footer) -->
    <footer class="bg-gray-900 text-gray-300 py-8 px-6 text-center">
        <div class="container mx-auto">
            <p>&copy; 2025 Agencia IA Inmobiliaria. Todos los derechos reservados.</p>
            <div class="mt-4 space-x-4">
                <a href="#" class="hover:text-white">Política de Privacidad</a>
                <span class="text-gray-600">|</span>
                <a href="#" class="hover:text-white">Términos de Servicio</a>
            </div>
        </div>
    </footer>

    <script>
        // Smooth scrolling para los enlaces de navegación
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();

                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Funcionalidad del menú móvil
        const menuButton = document.getElementById('menu-button');
        const closeMenuButton = document.getElementById('close-menu-button');
        const mobileMenu = document.getElementById('mobile-menu');

        function toggleMobileMenu() {
            mobileMenu.classList.toggle('-translate-x-full');
        }

        menuButton.addEventListener('click', toggleMobileMenu);
        closeMenuButton.addEventListener('click', toggleMobileMenu);
    </script>
</body>
</html>
