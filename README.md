# 🚀 Portfolio Denilson - IT Security Specialist & Developer

Portafolio profesional completo con navegación interactiva, submenús organizados y evidencias de proyectos en desarrollo, instalaciones, ciberseguridad y soporte.

---

## 📁 Estructura del Proyecto

```
portfolio/
│
├── index.html              # Página principal con navegación completa
│
├── css/
│   └── styles.css          # Estilos modernos y responsive
│
├── javascript/
│   └── main.js             # Funcionalidades interactivas y animaciones
│
├── php/
│   └── security_utils.php  # Utilidades PHP para backend y APIs
│
├── python/
│   └── security_utils.py   # Utilidades Python para seguridad y análisis
│
└── assets/
    └── images/             # Carpeta para imágenes del portafolio
```

---

## 🎯 Características Principales

### ✨ Diseño y UI/UX
- **Navegación fija** con efecto blur y sombra al hacer scroll
- **Menú responsive** con hamburger menu para móviles
- **Submenús dropdown** organizados por categorías
- **Animaciones suaves** con CSS y JavaScript
- **Tema oscuro profesional** con acentos en cyan y morado
- **Tarjetas interactivas** con efectos hover y ripple

### 📱 Navegación Organizada

#### 🏠 Inicio
- Hero section con estadísticas animadas
- Presentación profesional

#### 💻 Desarrollos
Submenú con:
- **Python Projects**: ML, análisis de datos, automatización
- **JavaScript/React**: Dashboards, herramientas web
- **PHP Backend**: APIs REST, sistemas de gestión
- **PowerShell Scripts**: Automatización Windows, administración

#### 🔧 Instalaciones
Submenú con:
- **FortiGate/FortiDLP**: Implementaciones enterprise
- **Sistemas de Cámaras**: CCTV y videovigilancia
- **Infraestructura de Red**: VLANs, segmentación
- **Servidores**: Active Directory, Docker

#### 🔐 Ciberseguridad
Submenú con:
- **DLP Policies**: Data Loss Prevention
- **Firewall Config**: Reglas y políticas
- **Security Monitoring**: SIEM y análisis
- **ML DDoS Detection**: Machine Learning aplicado

#### 🎯 Soporte
Submenú con:
- **Active Directory**: Gestión de usuarios y OUs
- **Group Policy**: GPOs y configuraciones
- **Ticket Resolution**: Helpdesk y soporte
- **Automatización**: Scripts y workflows

#### 📬 Contacto
- Email con enlace directo
- WhatsApp con mensaje predefinido
- LinkedIn profesional

---

## 🛠️ Archivos de Utilidades

### Python (python/security_utils.py)

**Clases incluidas:**

#### `NetworkScanner`
```python
# Escaneo de puertos
scanner = NetworkScanner()
open_ports = scanner.scan_common_ports("192.168.1.1")
local_ip = scanner.get_local_ip()
```

#### `SecurityUtils`
```python
# Análisis de seguridad
utils = SecurityUtils()
file_hash = utils.hash_file("document.pdf")
password_strength = utils.check_password_strength("MyPassword123")
```

#### `LogAnalyzer`
```python
# Análisis de logs
analyzer = LogAnalyzer()
failed_logins = analyzer.find_failed_logins("auth.log")
suspicious_ips = analyzer.detect_port_scan("access.log")
```

#### `ReportGenerator`
```python
# Generación de reportes
generator = ReportGenerator()
report = generator.generate_security_report(data)
generator.export_to_json(data, "report.json")
```

### PHP (php/security_utils.php)

**Clases incluidas:**

#### `SecureDatabase`
```php
// Conexión segura con PDO
$db = new SecureDatabase('localhost', 'dbname', 'user', 'pass');
$users = $db->select('users', 'active = :active', ['active' => 1]);
$id = $db->insert('logs', ['event' => 'login', 'user_id' => 1]);
```

#### `JWTAuth`
```php
// Autenticación JWT
$jwt = new JWTAuth('secret_key');
$token = $jwt->createToken(['user_id' => 1, 'role' => 'admin']);
$payload = $jwt->verifyToken($token);
```

#### `InputValidator`
```php
// Validación de entrada
$clean = InputValidator::sanitizeString($_POST['input']);
$valid = InputValidator::validateEmail($email);
$strength = InputValidator::validatePasswordStrength($password);
```

#### `RESTApi`
```php
// Manejo de API REST
$api = new RESTApi();
$method = $api->getMethod();
$params = $api->getParams();
$api->sendResponse(['success' => true, 'data' => $data]);
```

#### `SecurityLogger`
```php
// Logging de seguridad
$logger = new SecurityLogger('security.log');
$logger->info('User logged in', ['user_id' => 1]);
$logger->warning('Failed login attempt');
$logger->error('Database connection failed');
```

---

## 🚀 Cómo Usar

### Instalación Local

1. **Clonar o descargar** la carpeta `portfolio/`

2. **Abrir con un servidor local:**

   **Opción 1 - Python:**
   ```bash
   cd portfolio
   python -m http.server 8000
   ```
   
   **Opción 2 - PHP:**
   ```bash
   cd portfolio
   php -S localhost:8000
   ```
   
   **Opción 3 - Node.js:**
   ```bash
   npx http-server portfolio -p 8000
   ```

3. **Acceder en el navegador:**
   ```
   http://localhost:8000
   ```

### Personalización

#### 1. Datos de Contacto
Editar en `index.html` líneas 545-570:
```html
<a href="mailto:TU_EMAIL@ejemplo.com">
<a href="https://wa.me/TU_NUMERO">
```

#### 2. Contenido de Proyectos
Cada tarjeta de proyecto puede editarse en `index.html`:
- **Título**: `<h4 class="card-title">`
- **Descripción**: `<p class="card-description">`
- **Tags**: `<span class="tag">`
- **Enlace**: `<a href="..." class="btn-view">`

#### 3. Colores y Tema
Editar variables CSS en `css/styles.css` líneas 1-12:
```css
:root {
    --primary: #0a0e27;
    --accent: #00d9ff;
    /* ... más colores */
}
```

#### 4. Añadir Nuevos Proyectos
Copiar una tarjeta existente y modificar:
```html
<div class="portfolio-card">
    <div class="card-header python">
        <span class="card-icon">🎯</span>
        <span class="card-badge">Python</span>
    </div>
    <h4 class="card-title">Tu Proyecto</h4>
    <p class="card-description">Descripción del proyecto...</p>
    <div class="card-tags">
        <span class="tag">Tag1</span>
        <span class="tag">Tag2</span>
    </div>
    <div class="card-footer">
        <a href="ruta/proyecto.html" class="btn-view">Ver Proyecto</a>
    </div>
</div>
```

---

## 📊 Proyectos Destacados Incluidos

### Desarrollos
- ✅ DDoS Detection ML System (99.8% accuracy)
- ✅ Port Scanner Avanzado
- ✅ Big Data Analytics Bot-IoT
- ✅ Security Dashboard React
- ✅ Sistema de Tickets PHP
- ✅ FortiDLP Agent Manager PowerShell
- ✅ Firewall Analyzer
- ✅ Windows Backup System

### Instalaciones
- ✅ FortiGate 200E Implementation
- ✅ FortiDLP Enterprise Deployment
- ✅ Sistema CCTV Hikvision
- ✅ Red Empresarial Segmentada
- ✅ Active Directory Domain
- ✅ Servidor Docker Monitoring

### Ciberseguridad
- ✅ 15+ Políticas DLP
- ✅ 100+ Reglas de Firewall
- ✅ Sistema IPS/IDS
- ✅ Dashboard SIEM
- ✅ ML DDoS Detection
- ✅ Análisis de Tráfico Anómalo

### Soporte
- ✅ Gestión Masiva AD Users
- ✅ GPOs de Seguridad
- ✅ 500+ Tickets Resueltos
- ✅ Scripts de Diagnóstico
- ✅ Workflows Automatizados

---

## 🎨 Tecnologías Utilizadas

### Frontend
- HTML5 Semántico
- CSS3 con Variables y Animaciones
- JavaScript ES6+ Vanilla
- Google Fonts (Outfit, JetBrains Mono)

### Backend (Utilities)
- Python 3.x
- PHP 8.x
- PowerShell 5.1+

### Seguridad
- JWT Authentication
- Password Hashing (Argon2)
- Prepared Statements (PDO)
- Input Validation
- Security Logging

---

## 📱 Responsive Design

El portafolio está optimizado para:
- 📱 **Móviles**: 320px - 480px
- 📱 **Tablets**: 481px - 768px
- 💻 **Laptops**: 769px - 1024px
- 🖥️ **Desktop**: 1025px+

---

## ⚡ Funcionalidades JavaScript

### Navegación
- Menú hamburguesa responsive
- Dropdowns animados
- Smooth scroll
- Active state en secciones

### Animaciones
- Fade in al hacer scroll
- Contador animado de estadísticas
- Efecto ripple en botones
- Parallax en hero section
- Hover effects en tarjetas

### Interactividad
- Filtrado de proyectos
- Búsqueda de portafolio
- Intersection Observer
- Lazy loading de imágenes

---

## 🔒 Seguridad

### Implementaciones de Seguridad
- ✅ Sanitización de inputs
- ✅ Prepared statements
- ✅ Password hashing (Argon2ID)
- ✅ JWT para autenticación
- ✅ HTTPS-ready
- ✅ CSP headers compatible
- ✅ XSS protection
- ✅ CSRF tokens (en PHP)

---

## 📝 Notas de Desarrollo

### Para Añadir Páginas de Proyectos
1. Crear archivo HTML en la carpeta correspondiente
2. Usar la misma estructura de estilos
3. Actualizar el enlace en `index.html`

### Para Añadir Imágenes
1. Colocar imágenes en `assets/images/`
2. Usar lazy loading:
   ```html
   <img data-src="assets/images/proyecto.png" alt="Proyecto">
   ```

### Para Personalizar Animaciones
Editar en `css/styles.css`:
```css
@keyframes tuAnimacion {
    from { /* estado inicial */ }
    to { /* estado final */ }
}
```

---

## 🤝 Contacto

**Denilson**  
IT Security Specialist & Developer  
Practicante TISec @ SiiX EMS Mexico

📧 Email: denilson.dev@siixems.com  
💬 WhatsApp: +52 1 444 123 4567  
💼 LinkedIn: /in/denilson-dev

---

## 📄 Licencia

Este portafolio es de código abierto para uso personal y educativo.

---

## 🎯 Próximas Mejoras

- [ ] Sistema de búsqueda avanzada
- [ ] Filtros por tecnología
- [ ] Modo claro/oscuro toggle
- [ ] Blog integrado
- [ ] Formulario de contacto con backend
- [ ] Integración con GitHub API
- [ ] Analytics dashboard
- [ ] Certificaciones section

---

**Hecho con 💙 por Denilson | 2026**
