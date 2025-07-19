<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pregonero (EN DESARROLLO)</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 0 auto;
            max-width: 800px;
            padding: 20px;
            background-color: #f9f9f9;
        }
        h1, h2, h3 {
            color: #333;
        }
        h1 {
            font-size: 2.5em;
        }
        h2 {
            font-size: 1.8em;
        }
        h3 {
            font-size: 1.4em;
        }
        strong {
            font-weight: bold;
        }
        em {
            font-style: italic;
        }
        code {
            background-color: #f4f4f4;
            padding: 2px 4px;
            border-radius: 4px;
            font-family: 'Courier New', Courier, monospace;
        }
        pre {
            background-color: #f4f4f4;
            padding: 10px;
            border-radius: 4px;
            overflow-x: auto;
            font-family: 'Courier New', Courier, monospace;
        }
        a {
            color: #0077B5;
            text-decoration: none;
        }
        a:hover {
            text-decoration: underline;
        }
        img {
            vertical-align: middle;
        }
        table {
            border-collapse: collapse;
            width: 100%;
            margin: 20px 0;
        }
        th, td {
            border: 1px solid #ddd;
            padding: 8px;
            text-align: left;
        }
        th {
            background-color: #f2f2f2;
        }
        .badge {
            margin-right: 10px;
        }
        .right-align {
            float: right;
            margin-left: 20px;
        }
        .tech-icons img {
            margin-right: 12px;
        }
    </style>
</head>
<body>
    <h2 align="left">Hola 👋! Mi nombre es Daniel ...soy desarrollador de aplicaciones móviles y multiplataforma</h2>

    <div align="right">
        <img src="https://avatars.githubusercontent.com/u/129673020?v=4" height="150" alt="Daniel's avatar" class="right-align">
    </div>

    <div align="left" class="tech-icons">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/kotlin/kotlin-original.svg" height="30" alt="kotlin logo">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/csharp/csharp-original.svg" height="30" alt="csharp logo">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" height="30" alt="javascript logo">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" height="30" alt="python logo">
    </div>

    <div align="left">
        <a href="mailto:daniel.imbert96@gmail.com" target="_blank">
            <img src="https://img.shields.io/static/v1?message=Gmail&logo=gmail&label=&color=D14836&logoColor=white&labelColor=&style=for-the-badge" height="35" alt="gmail logo" class="badge">
        </a>
        <a href="https://www.linkedin.com/in/daniel-imbert-68b4952b4" target="_blank">
            <img src="https://img.shields.io/static/v1?message=LinkedIn&logo=linkedin&label=&color=0077B5&logoColor=white&labelColor=&style=for-the-badge" height="35" alt="linkedin logo" class="badge">
        </a>
    </div>

    <h1>Pregonero</h1>
    <p><strong>Pregonero</strong> es una aplicación móvil Android que conecta a usuarios en una ciudad cubana, permitiendo localizar y publicar <em>bienes</em> (comida, ropa, productos de higiene), <em>servicios</em> (reparaciones, transporte) y <em>eventos</em> (fiestas, actividades culturales) en un entorno comunitario. Diseñada para operar en un contexto de <em>conectividad limitada</em>, la app ofrece soporte offline y se distribuye vía <a href="https://www.apklis.cu/">Apklis</a> o <em>paquete semanal</em> (USB). Los <strong>negocios</strong> publican hasta 5 publicaciones gratis (10 para el top 3% basado en calificaciones), con opciones pagadas de 10-50 CUP. Los <strong>usuarios generales</strong> buscan contenidos y crean <em>anuncios rápidos</em> (2 horas, gratis). Un <em>sistema de puntuación</em> fomenta calidad y confianza.</p>
    <img src="https://username.github.io/pregonero/screenshots/home.png" alt="Pantalla de Inicio" width="300">

    <h2>Propósito</h2>
    <p><strong>Pregonero</strong> resuelve la escasez de bienes y servicios en Cuba, conectando comunidades locales mediante una plataforma accesible. Los usuarios descubren ofertas cercanas con mapas offline, publican anuncios urgentes y califican negocios para promover calidad, todo optimizado para dispositivos Android de gama baja-media.</p>

    <h2>Funcionalidades</h2>
    <ul>
        <li><strong>Negocios</strong>: Publican bienes, servicios o eventos. 5 publicaciones gratis (10 para el <em>top 3%</em>). Pagadas: <code>10 CUP</code> (1 día), <code>20 CUP</code> (2 días), <code>30 CUP</code> (5 días), <code>50 CUP</code> (2 semanas).</li>
        <li><strong>Usuarios generales</strong>: Buscan, crean <em>anuncios rápidos</em> (2 horas, gratis) y califican negocios (1-5 estrellas).</li>
        <li><strong>Sistema de puntuación</strong>: El <em>top 3%</em> recibe publicaciones gratis adicionales y <em>prioridad alta</em> (visibilidad destacada).</li>
        <li><strong>Mapas offline</strong>: Usando <strong>Google Maps Compose</strong>, con caché local.</li>
        <li><strong>Pagos</strong>: <strong>QvaPay</strong> para USDT, CUP o MLC, con códigos QR cacheados.</li>
        <li><strong>Soporte offline</strong>: Cacheo de datos con <strong>Firebase</strong> y <strong>Coil</strong>.</li>
        <li><strong>Tutoriales</strong>: Animaciones <strong>Lottie</strong> y guías offline para autenticación y uso.</li>
    </ul>

    <h2>Tecnologías</h2>
    <table>
        <tr>
            <th>Tecnología</th>
            <th>Propósito</th>
        </tr>
        <tr>
            <td><strong>Kotlin</strong></td>
            <td>Lenguaje de programación</td>
        </tr>
        <tr>
            <td><strong>Jetpack Compose</strong></td>
            <td>Interfaz de usuario moderna</td>
        </tr>
        <tr>
            <td><strong>Ktor</strong></td>
            <td>Consumo de APIs (QvaPay)</td>
        </tr>
        <tr>
            <td><strong>Dagger Hilt</strong></td>
            <td>Inyección de dependencias</td>
        </tr>
        <tr>
            <td><strong>Lottie</strong></td>
            <td>Animaciones en tutoriales</td>
        </tr>
        <tr>
            <td><strong>IconExtended</strong></td>
            <td>Íconos personalizados</td>
        </tr>
        <tr>
            <td><strong>Google Maps Compose</strong></td>
            <td>Mapas offline para geolocalización</td>
        </tr>
        <tr>
            <td><strong>Firebase</strong></td>
            <td>Autenticación (<em>Google Sign-In</em>, correo/contraseña, anónima) y almacenamiento (<em>Firestore</em>, <em>Storage</em>)</td>
        </tr>
        <tr>
            <td><strong>QvaPay</strong></td>
            <td>Pagos en USDT, CUP, MLC</td>
        </tr>
        <tr>
            <td><strong>Coil</strong></td>
            <td>Cacheo de imágenes</td>
        </tr>
    </table>

    <h2>Arquitectura</h2>
    <p><strong>Pregonero</strong> usa <strong>MVVM</strong> con <strong>Jetpack Compose</strong>:</p>
    <ul>
        <li><strong>Model</strong>: Datos en <strong>Firestore</strong>, cacheados para uso offline.</li>
        <li><strong>View</strong>: Pantallas en <strong>Compose</strong> (Inicio, Búsqueda, Calificación).</li>
        <li><strong>ViewModel</strong>: Lógica inyectada con <strong>Dagger Hilt</strong>.</li>
        <li><strong>Red</strong>: <strong>Ktor</strong> para APIs externas (<strong>QvaPay</strong>).</li>
        <li><strong>Offline</strong>: Cacheo con <strong>Firestore</strong>, <strong>Coil</strong>, y <strong>Google Maps Compose</strong>.</li>
    </ul>

    <h2>Instalación</h2>
    <ol>
        <li>Clona el repositorio:
            <pre><code>git clone https://github.com/tu_usuario/pregonero.git</code></pre>
        </li>
        <li>Abre en <strong>Android Studio</strong> (Dolphin o superior) y sincroniza Gradle.</li>
        <li>Agrega dependencias en <code>app/build.gradle</code>:
            <pre><code>def compose_version = "1.5.0"
def hilt_version = "2.48"
def ktor_version = "2.3.0"
def lottie_version = "6.0.0"

implementation "androidx.compose.ui:ui:$compose_version"
implementation "androidx.compose.material3:material3:$compose_version"
implementation "com.google.maps.android:maps-compose:2.11.0"
implementation "com.google.android.gms:play-services-maps:18.1.0"
implementation "com.google.dagger:hilt-android:$hilt_version"
kapt "com.google.dagger:hilt-compiler:$hilt_version"
implementation "io.ktor:ktor-client-core:$ktor_version"
implementation "io.ktor:ktor-client-okhttp:$ktor_version"
implementation "io.ktor:ktor-client-content-negotiation:$ktor_version"
implementation "io.ktor:ktor-serialization-kotlinx-json:$ktor_version"
implementation "com.airbnb.android:lottie-compose:$lottie_version"
implementation "com.malinskiy:materialicons:1.0.0" // IconExtended
implementation platform('com.google.firebase:firebase-bom:32.0.0')
implementation 'com.google.firebase:firebase-auth'
implementation 'com.google.firebase:firebase-firestore'
implementation 'com.google.firebase:firebase-storage'
implementation "io.coil-kt:coil-compose:2.4.0"</code></pre>
        </li>
    </ol>

    <h2>Configuración</h2>
    <h3>Firebase</h3>
    <ul>
        <li>Crea un proyecto en <a href="https://console.firebase.google.com/">Firebase Console</a>.</li>
        <li>Agrega claves SHA-1/SHA-256:
            <pre><code>./gradlew signingReport</code></pre>
        </li>
        <li>Descarga <code>google-services.json</code> y colócalo en <code>app/</code>.</li>
        <li>Habilita <strong>Firestore</strong> offline:
            <pre><code class="language-kotlin">FirebaseFirestore.getInstance().firestoreSettings = FirebaseFirestoreSettings.Builder()
    .setPersistenceEnabled(true)
    .build()</code></pre>
        </li>
        <li>Configura autenticación:
            <pre><code class="language-kotlin">val auth = FirebaseAuth.getInstance()
val gso = GoogleSignInOptions.Builder(GoogleSignInOptions.DEFAULT_SIGN_IN)
    .requestIdToken(getString(R.string.default_web_client_id))
    .requestEmail()
    .build()</code></pre>
        </li>
    </ul>

    <h3>Google Maps</h3>
    <ul>
        <li>Obtén una clave API en <a href="https://console.cloud.google.com/">Google Cloud Console</a>.</li>
        <li>Agrega en <code>AndroidManifest.xml</code>:
            <pre><code class="language-xml">&lt;meta-data
    android:name="com.google.android.geo.API_KEY"
    android:value="TU_CLAVE_API"/&gt;</code></pre>
        </li>
    </ul>

    <h3>QvaPay</h3>
    <ul>
        <li>Regístrate en <a href="https://qvapay.com/">QvaPay</a> para obtener <code>app_id</code> y <code>app_secret</code>.</li>
        <li>Configura <strong>Ktor</strong>:
            <pre><code class="language-kotlin">@Inject
class QvaPayClient(private val client: HttpClient) {
    suspend fun createInvoice(amount: Double, description: String, postId: String): Invoice {
        return client.post("https://qvapay.com/api/invoice") {
            contentType(ContentType.Application.Json)
            setBody(mapOf("amount" to amount * 1.01, "description" to description, "postId" to postId))
        }.body()
    }
}</code></pre>
        </li>
    </ul>

    <h2>Uso en Cuba</h2>
    <ul>
        <li><strong>Offline</strong>: Datos cacheados con <strong>Firestore</strong>, imágenes con <strong>Coil</strong>, y mapas con <strong>Google Maps Compose</strong>.</li>
        <li><strong>Distribución</strong>: APK y datos iniciales vía <a href="https://www.apklis.cu/">Apklis</a> o <em>paquete semanal</em> (USB).</li>
        <li><strong>Pagos</strong>: <strong>QvaPay</strong> para transacciones en USDT, CUP o MLC, con códigos QR cacheados.</li>
        <li><strong>Tutoriales</strong>: Animaciones <strong>Lottie</strong> y guías offline para autenticación y uso.</li>
    </ul>

    <h2>Contribuir</h2>
    <ol>
        <li>Fork el repositorio.</li>
        <li>Crea una rama: <code>git checkout -b feature/nueva-funcionalidad</code>.</li>
        <li>Haz commit: <code>git commit -m "Añade nueva funcionalidad"</code>.</li>
        <li>Sube cambios: <code>git push origin feature/nueva-funcionalidad</code>.</li>
        <li>Abre un Pull Request.</li>
    </ol>
    <p>Consulta el <a href="CODE_OF_CONDUCT.html">Código de Conducta</a>.</p>

    <h2>Licencia</h2>
    <p><a href="LICENSE">MIT</a></p>
</body>
</html>
