# LumbraTech

Aplicación móvil desarrollada con Expo Router y React Native, con integración de autenticación en la nube mediante Supabase.

## Estado del Proyecto

**Base de desarrollo** - Proyecto inicial con:
- Sistema de autenticación con Supabase
- Pantalla de login y registro
- Contexto global de autenticación
- Navegación por pestañas
- Listo para implementar nuevas características

## Requisitos

- Node.js 18 o superior
- npm o yarn
- Expo CLI: `npm install -g expo-cli`

## Inicio Rápido

### 1. Instalar Dependencias
```bash
npm install
```

### 2. Configurar Variables de Entorno
Crea un archivo `.env` con tus credenciales de Supabase:

```env
EXPO_PUBLIC_SUPABASE_URL=https://tu-proyecto.supabase.co
EXPO_PUBLIC_SUPABASE_ANON_KEY=tu-anon-key-aqui
```

Referencia: Usa `.env.example` como plantilla.

### 3. Iniciar Servidor de Desarrollo
```bash
npm start
```

Selecciona la opción apropiada:
- `w` - Navegador web
- `a` - Emulador de Android
- `i` - Simulador de iOS (requiere macOS)

## Estructura del Proyecto

```
app/
  ├── _layout.tsx              Configuración de rutas y autenticación
  ├── login.tsx                Pantalla de autenticación
  ├── modal.tsx                Ejemplo de componente modal
  └── (tabs)/
      ├── _layout.tsx          Configuración de navegación por pestañas
      ├── index.tsx            Pantalla de inicio
      └── explore.tsx          Pantalla de exploración

contexts/
  └── auth-context.tsx         Contexto global de autenticación

lib/
  └── supabase.ts              Cliente de Supabase configurado

components/
  ├── themed-text.tsx          Componente de texto con tema
  ├── themed-view.tsx          Componente de vista con tema
  └── ui/                      Librería de componentes de interfaz
```

## Autenticación

La aplicación implementa autenticación con Supabase con las siguientes características:

- Login con correo electrónico y contraseña
- Registro de usuario con confirmación de email
- Gestión persistente de sesiones
- Hook personalizado `useAuth()` para acceder al estado de autenticación

### Configurar Usuario de Prueba

1. Accede a tu proyecto en supabase.com
2. Ve a la sección Authentication > Users
3. Crea un nuevo usuario con correo electrónico y contraseña

## Dependencias Principales

| Paquete | Propósito |
|---------|-----------|
| expo | Framework para desarrollo multiplataforma |
| expo-router | Sistema de enrutamiento basado en archivos |
| react-native | Framework nativo para móviles |
| @supabase/supabase-js | Librería cliente de Supabase |
| react-navigation | Navegación nativa |

## Scripts Disponibles

| Comando | Descripción |
|---------|------------|
| `npm start` | Inicia el servidor de desarrollo |
| `npm run web` | Ejecuta en navegador web |
| `npm run android` | Ejecuta en Android |
| `npm run ios` | Ejecuta en iOS |
| `npm run lint` | Valida el código |
| `npm run reset-project` | Reinicia la estructura del proyecto |

## Soporte de Tema

La aplicación se adapta automáticamente al modo claro u oscuro según las preferencias del sistema.

## Documentación

- [Documentación de Expo](https://docs.expo.dev)
- [Documentación de Supabase](https://supabase.com/docs)
- [Documentación de React Native](https://reactnative.dev)
- [Guía de Expo Router](https://docs.expo.dev/router/introduction)

## Consideraciones de Seguridad

- No hagas commit de archivos `.env` con credenciales de producción
- Las claves públicas se almacenan solo en `.env.example`
- Las claves de servicio nunca deben exponerse en aplicaciones cliente
- Todas las credenciales deben gestionarse mediante variables de entorno

## Licencia

Propietario - LumbraTech
