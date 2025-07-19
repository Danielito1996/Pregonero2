#**PREGONERO**

**Pregonero** es una aplicación móvil Android que conecta a usuarios en una ciudad cubana, permitiendo localizar y publicar bienes (*comida, ropa, productos de higiene*), servicios (*reparaciones, transporte*) y eventos (*fiestas, actividades culturales*) en un entorno comunitario. Diseñada para operar en un contexto de conectividad limitada, la app ofrece soporte offline con algunas limitaciones . Los negocios pueden publicar hasta 5 publicaciones gratis (*10 para el top 3% basado en calificaciones de usuarios*), con opciones pagadas de 10-50 CUP, mientras que los usuarios generales buscan contenidos y crean anuncios rápidos (*2 horas de persistencia*). Un sistema de puntuación basado en calificaciones fomenta la calidad y la confianza en la comunidad.

##**Propósito:**
*Aborda la escasez de bienes y servicios en Cuba, facilitando el acceso a productos, servicios y eventos locales a través de una plataforma comunitaria. Los usuarios pueden descubrir ofertas cercanas usando mapas offline, publicar anuncios rápidos para necesidades urgentes y calificar negocios para promover calidad y confianza. La app está optimizada para dispositivos Android de gama baja-media, con soporte offline y precios accesibles (10-50 CUP por publicación pagada), adaptándose al contexto cubano de conectividad limitada.FuncionalidadesTipos de usuarios:Negocios (personas naturales o establecimientos): Publican bienes, servicios o eventos. Hasta 5 publicaciones gratis (10 para el top 3% basado en calificaciones). Publicaciones pagadas: 10 CUP (1 día), 20 CUP (2 días), 30 CUP (5 días), 50 CUP (2 semanas).
Usuarios generales: Buscan publicaciones, crean anuncios rápidos (gratis, 2 horas de persistencia) y califican negocios (1-5 estrellas).*

##**Sistema de puntuación:** 
*Los usuarios generales califican negocios tras interacciones. El top 3% recibe 5 publicaciones gratis adicionales y prioridad alta (visibilidad destacada en búsquedas y mapas).
Búsqueda y filtros: Por categoría (bienes, servicios, eventos), precio, distancia o ciudad/barrio, con soporte offline.
Mapas offline: Integración con **Google Maps Compose** para mostrar ubicaciones, con datos cacheados parPagos: Integración con QvaPay para pagos en USDT (TRC-20), CUP o MLC, con códigos QR cacheados.
Soporte offline: Publicaciones, calificaciones y anuncios se almacenan localmente, sincronizando en puntos Wi-Fi (ETECSA).
Tutoriales offline: Guías en imágenes o **animaciones Lottie** para enseñar a usar la app.*

##**Tecnologías** 
Lenguaje: **Kotlin**
Interfaz de usuario: **Jetpack Compose** para una UI moderna y reactiva
Red: **Ktor** para consumir APIs externas
Inyección de dependencias: **Dagger Hilt** para gestionar dependencias
Animaciones: **Lottie** para animaciones fluidas en tutoriales y transiciones
Íconos: IconExtended para íconos personalizados (*por ejemplo, estrellas para negocios top 3%*)
Mapas: **Google Maps Compose** para geolocalización, con soporte offline
Backend: **Firebase** para:Autenticación: Google Sign-In, correo/contraseña y autenticación anónima
Almacenamiento: **Cloud Firestore** (*Spark Plan*) para publicaciones, calificaciones y pagos
Almacenamiento de archivos: **Firebase Storage** para imágenes (*complementa GitHub Pages*)

Imágenes: *Hospedadas en GitHub Pages, cacheadas con Coil para Jetpack Compose*

##**Arquitectura:**
La aplicación sigue una arquitectura MVVM (*Model-View-ViewModel*) con Jetpack Compose:Model: Datos almacenados en Firestore (*publicaciones, calificaciones, pagos*) y cacheados localmente para soporte offline.
View: Pantallas en Compose para Inicio, Búsqueda, Detalles, Creación de publicación, Anuncios rápidos, Calificación, Perfil y Tutoriales.
ViewModel: Gestiona la lógica de negocio, inyectada con Dagger Hilt.
Red: Ktor maneja integraciones externas.
Offline: Firestore y Google Maps Compose usan caché local. Imágenes se cachean con Coil desde GitHub Pages.

##**Instalación**
Clona el repositorio:bash

```git clone https://github.com/Danielito1996/Pregonero2.git```

Abre en Android Studio:Usa Android Studio (*versión Dolphin o superior*).
Sincroniza el proyecto con Gradle.

Configura dependencias:Asegúrate de tener las siguientes dependencias en build.gradle (*módulo app*):gradle


```// Jetpack Compose
   implementation "androidx.compose.ui:ui:$compose_version"
   implementation "androidx.compose.material3:material3:$compose_version"```
```// Google Maps Compose```
```implementation "com.google.maps.android:maps-compose:2.11.0"```
```implementation "com.google.android.gms:play-services-maps:18.1.0"```
```// Dagger Hilt```
```implementation "com.google.dagger:hilt-android:$hilt_version"```
```kapt "com.google.dagger:hilt-compiler:$hilt_version"```
```// Ktor```
```implementation "io.ktor:ktor-client-core:$ktor_version"```
```implementation "io.ktor:ktor-client-okhttp:$ktor_version"```
```implementation "io.ktor:ktor-client-content-negotiation:$ktor_version"```
```implementation "io.ktor:ktor-serialization-kotlinx-json:$ktor_version"```
```// Lottie```
```implementation "com.airbnb.android:lottie-compose:$lottie_version"```
```// IconExtended (ajusta según la fuente)```
```implementation "com.malinskiy:materialicons:1.0.0" // Ejemplo```
```// Firebase```
```implementation platform('com.google.firebase:firebase-bom:32.0.0')```
```implementation 'com.google.firebase:firebase-auth'```
```implementation 'com.google.firebase:firebase-firestore'```
```implementation 'com.google.firebase:firebase-storage'```
```// Coil para imágenes```
```implementation "io.coil-kt:coil-compose:2.4.0" ```

Configura Firebase:Crea un proyecto en Firebase Console.
Agrega las claves SHA-1/SHA-256 (*debug y release*) en Project Settings > Your Apps:bash

`./gradlew signingReport`

Descarga google-services.json y colócalo en `app/.`

Configura Google Maps:Obtén una clave API en Google Cloud Console.
Agrega la clave en AndroidManifest.xml:xml

```xml``
<meta-data```
```    android:name="com.google.android.geo.API_KEY" ```
```    android:value="TU_CLAVE_API"/>```

*ConfiguraciónDagger Hilt:* Anota la clase Application con `@HiltAndroidApp:kotlin`

```kotlin @HiltAndroidApp```
```class MainApplication : Application()```

Define módulos para inyectar dependencias:kotlin

```kotlin @Module```
```@InstallIn(SingletonComponent::class)```
```object AppModule {```
```    @Provides```
```    @Singleton```
```    fun provideFirestore() = FirebaseFirestore.getInstance()```
```    @Provides```
```    @Singleton```
```   fun provideKtorClient() = HttpClient(OkHttp) {```
```        install(ContentNegotiation) { json() }```
```    }```
```    @Provides```
```    @Singleton```
```    fun provideQvaPayClient(@Named("ktorClient") client: HttpClient) = QvaPayClient(client)```
```}```

**Ktor:** Configura el cliente Ktor para consumir la APIs.

*/Configura autenticación (Google, correo/contraseña, anónima)**:
```kotlin val auth = FirebaseAuth.getInstance()```
```val gso = GoogleSignInOptions.Builder(GoogleSignInOptions.DEFAULT_SIGN_IN)```
```    .requestIdToken(getString(R.string.default_web_client_id))```
```    .requestEmail()```
```    .build()```
    
**Google Maps Compose:** Usa mapas offline con caché local:

```kotlin @Composable```
```fun MapScreen() {```
```    val cameraPositionState = rememberCameraPositionState {```
```        position = CameraPosition.fromLatLngZoom(LatLng(23.113, -82.366), 10f)```
```    }```
```    GoogleMap(```
```        modifier = Modifier.fillMaxSize(),```
```        cameraPositionState = cameraPositionState```
```    ) {```
```        // Pines para publicaciones (bienes, servicios, eventos)```
```    }```
```}```

**Lottie:** Usa animaciones para tutoriales offline:

```kotlin @Composable```
```fun TutorialScreen() {```
```    val composition by rememberLottieComposition(LottieCompositionSpec.RawRes(R.raw.tutorial_animation))```
```    LottieAnimation(```
```        composition = composition,```
```        iterations = LottieConstants.IterateForever```
```    )```
```}```

**Uso offline:** Publicaciones, calificaciones y anuncios rápidos se almacenan en Firestore cache. Imágenes se cachean con Coil desde GitHub Pages o Firebase Storage.
Distribución: APK y datos iniciales (*imágenes, publicaciones, tutoriales*) se distribuyen vía Apklis o "paquete semanal" (USB) para minimizar descargas.

##**Contribuir**
¡Bienvenidos a contribuir! Sigue estos pasos:Fork el repositorio.
Crea una rama (`git checkout -b feature/nueva-funcionalidad`).
Realiza tus cambios y haz commit (`git commit -m "Añade nueva funcionalidad"`).
Sube los cambios (`git push origin feature/nueva-funcionalidad`).
Abre un Pull Request en GitHub.

Por favor, revisa el Código de Conducta (*CODE_OF_CONDUCT.md*) antes de contribuir.LicenciaEste proyecto está bajo la licencia MIT (*LICENSE*). Consulta el archivo LICENSE para más detalles.
