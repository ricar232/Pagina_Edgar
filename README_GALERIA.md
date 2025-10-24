# 📸 Galería de Antes y Después - Instrucciones

## 🎯 **Sistema Bilingüe Implementado**

Tu página web ahora funciona en **inglés por defecto** con opción de **cambiar a español**.

### **Selector de Idioma:**
- **Ubicación**: Esquina superior derecha
- **Banderas**: 🇺🇸 (Inglés) y 🇪🇸 (Español)
- **Persistencia**: El idioma elegido se guarda en el navegador

---

## 📷 **Cómo Agregar Fotos de Antes y Después**

### **1. Ubicación de las Fotos**
Guarda tus fotos en la misma carpeta que `index.html` con estos nombres:

#### **Cocina:**
- `kitchen-before.jpg` (foto de antes)
- `kitchen-after.jpg` (foto de después)

#### **Baño:**
- `bathroom-before.jpg` (foto de antes)
- `bathroom-after.jpg` (foto de después)

#### **Sala/Living:**
- `living-before.jpg` (foto de antes)
- `living-after.jpg` (foto de después)

#### **Electricidad:**
- `electrical-before.jpg` (foto de antes)
- `electrical-after.jpg` (foto de después)

### **2. Formatos Recomendados**
- **Formato**: JPG, PNG, WebP
- **Tamaño**: 1200x800 píxeles (proporción 3:2)
- **Peso**: Máximo 2MB por foto
- **Calidad**: Alta resolución para mostrar detalles

### **3. Funcionalidad de Deslizamiento**
- **Deslizador**: Los usuarios pueden arrastrar la línea blanca
- **Click**: Hacer click mueve el deslizador a esa posición
- **Móvil**: Compatible con touch/swipe en dispositivos móviles
- **Etiquetas**: "BEFORE/AFTER" en inglés, "ANTES/DESPUÉS" en español

---

## 🔧 **Cómo Agregar Más Proyectos**

Para agregar un nuevo proyecto (ej: "Deck Renovation"):

### **1. Agrega las Fotos:**
- `deck-before.jpg`
- `deck-after.jpg`

### **2. Agrega el HTML:**
```html
<div class="project-item">
  <h3 data-translate="project5-title">Deck Renovation</h3>
  <div class="before-after-container">
    <div class="before-after-slider">
      <div class="before-image">
        <img src="deck-before.jpg" alt="Deck before renovation" />
        <span class="image-label" data-translate="before-label">BEFORE</span>
      </div>
      <div class="after-image">
        <img src="deck-after.jpg" alt="Deck after renovation" />
        <span class="image-label" data-translate="after-label">AFTER</span>
      </div>
      <div class="slider-handle">
        <div class="slider-line"></div>
        <div class="slider-button">
          <i class="fas fa-chevron-left"></i>
          <i class="fas fa-chevron-right"></i>
        </div>
      </div>
    </div>
  </div>
  <p class="project-description" data-translate="project5-desc">Beautiful deck renovation with new materials.</p>
</div>
```

### **3. Agrega las Traducciones:**
En el archivo `index.html`, encuentra la sección `translations` y agrega:

```javascript
// En la sección 'en':
'project5-title': 'Deck Renovation',
'project5-desc': 'Beautiful deck renovation with new materials.',

// En la sección 'es':
'project5-title': 'Renovación de Terraza',
'project5-desc': 'Hermosa renovación de terraza con nuevos materiales.',
```

---

## 📤 **Sistema de Subida de Fotos**

### **Funcionalidad Actual:**
- **4 Categorías**: Cocina, Baño, Áreas de Estar, Trabajo Eléctrico
- **Drag & Drop**: Arrastra fotos directamente a las áreas
- **Click Upload**: Haz click para explorar archivos
- **Feedback Visual**: Muestra confirmación al subir

### **Para Implementación Completa:**
El sistema actual simula la subida. Para funcionalidad real necesitarías:
1. **Servidor backend** (PHP, Node.js, Python, etc.)
2. **Base de datos** para guardar referencias
3. **Carpeta de uploads** en el servidor
4. **Sistema de administración** para organizar fotos

---

## 🎨 **Personalización de Estilos**

### **Colores del Deslizador:**
```css
.slider-handle {
  background: white; /* Color de la línea */
}

.slider-button {
  background: white; /* Color del botón circular */
  color: var(--primary-color); /* Color de las flechas */
}
```

### **Tamaño de la Galería:**
```css
.before-after-container {
  height: 300px; /* Cambiar altura */
}

.before-after-gallery {
  grid-template-columns: repeat(auto-fit, minmax(500px, 1fr)); /* Cambiar ancho mínimo */
}
```

---

## 🌍 **Traducciones Disponibles**

### **Secciones Traducidas:**
- ✅ Header y navegación
- ✅ Galería de antes/después
- ✅ Sistema de subida de fotos
- ✅ Etiquetas y descripciones
- ⏳ Servicios (parcial)
- ⏳ Resto de secciones (pendiente)

### **Para Completar Traducciones:**
1. Agrega `data-translate="clave"` a elementos HTML
2. Agrega las traducciones en el objeto `translations`
3. Las traducciones se aplicarán automáticamente

---

## 📱 **Responsive Design**

- **Desktop**: Galería en 2 columnas
- **Tablet**: Galería en 1-2 columnas
- **Móvil**: Galería en 1 columna
- **Touch**: Funcionalidad táctil para deslizador

¡Tu galería de antes/después está lista para impresionar a tus clientes! 🚀