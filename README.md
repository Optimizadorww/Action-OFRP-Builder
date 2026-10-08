# 🦊 Action-Ofox-Builder

GitHub Actions para compilar **OrangeFox Recovery** para el **TECNO BG7**.

Este proyecto automatiza la compilación de OrangeFox Recovery utilizando GitHub Actions y el árbol de dispositivo específico para el TECNO BG7.

---

## 📱 Dispositivo

| Información      | Detalle            |
| ---------------- | ------------------ |
| Fabricante       | TECNO              |
| Modelo           | BG7                |
| Recovery         | OrangeFox Recovery |
| Versión          | R12.1 / OrangeFox  |
| Arquitectura     | ARM64              |
| Plataforma       | MediaTek MT6765    |
| Tipo de recovery | `vendor_boot`      |
| Android base     | Android 12.1       |

---

## ✨ Características

* 🦊 Compilación automática de OrangeFox.
* ⚙️ GitHub Actions totalmente automatizado.
* 📦 Generación de `vendor_boot.img`.
* 📦 Generación de `OrangeFox-R12.0-Unofficial-BG7.zip`.
* 💾 Generación de `OrangeFox-R12.0-Unofficial-BG7.img`.
* 🔧 Soporte para `fastbootd`.
* 🚀 Compilación reproducible desde GitHub Actions.
* 📋 Publicación automática de los archivos generados como artefactos/releases.

---

## 🏗️ Compilación

El proyecto utiliza GitHub Actions para realizar la compilación.

### 1. Clonar el repositorio

```bash
git clone https://github.com/Optimizadorww/Action-OFRP-Builder.git
cd Action-OFRP-Builder
```

### 2. Ejecutar GitHub Actions

Desde GitHub:

**Actions → Recovery Build → Run workflow**

Selecciona los parámetros disponibles y ejecuta el workflow.

La compilación se realizará automáticamente en los servidores de GitHub Actions.

---

## 📦 Archivos generados

Al finalizar correctamente la compilación, se generan archivos similares a:

```text
OrangeFox-R12.0-Unofficial-BG7.img
OrangeFox-R12.0-Unofficial-BG7.zip
ramdisk.img
vendor_boot.img
```

Los archivos pueden encontrarse en los **Artifacts** de GitHub Actions o en la **Release** generada por el workflow.

---

## ⚠️ Advertencia

Este recovery es **no oficial** y está destinado al **TECNO BG7**.

No flashees imágenes destinadas a otro dispositivo.

Antes de modificar el dispositivo, asegúrate de:

* Tener una copia de seguridad de tus datos.
* Conocer el procedimiento de recuperación de tu dispositivo.
* Verificar que el archivo corresponde exactamente a tu modelo.
* Comprobar el hash SHA-256 de los archivos descargados cuando esté disponible.

El uso de este proyecto es bajo tu propia responsabilidad.

**Ni el autor del proyecto ni los colaboradores se responsabilizan por daños, pérdida de datos, bootloops o dispositivos inutilizados.**

---

## 🔧 Estructura del proyecto

```text
Action-OFRP-Builder/
├── .github/
│   └── workflows/
│       └── Recovery_Build.yml
├── README.md
└── ...
```

El árbol del dispositivo utilizado durante la compilación se encuentra en:

```text
device/tecno/BG7
```

---

## 🧩 Device Tree

El proyecto utiliza un device tree específico para:

```text
TECNO BG7
```

Configuración principal:

```text
TARGET_ARCH := arm64
TARGET_BOARD_PLATFORM := mt6765
TARGET_BOOTLOADER_BOARD_NAME := BG7
```

OrangeFox se integra como recovery dentro de `vendor_boot`.

---

## 🤖 GitHub Actions

La compilación se realiza automáticamente mediante GitHub Actions.

El workflow se encarga de:

1. Preparar el entorno de compilación.
2. Descargar el código necesario.
3. Preparar el device tree.
4. Configurar OrangeFox.
5. Compilar el recovery.
6. Generar las imágenes correspondientes.
7. Calcular hashes SHA-256.
8. Publicar los archivos generados.

---

## 📜 Créditos

Gracias a todos los desarrolladores y proyectos de código abierto que hacen posible este proyecto.

### OrangeFox Recovery

Proyecto de recovery utilizado como base.

### Android Open Source Project

Base del sistema de compilación Android.

### TeamWin Recovery Project

Parte importante del ecosistema de recovery personalizado utilizado como base tecnológica.

### GitHub Actions

Infraestructura utilizada para automatizar las compilaciones.

---

## ❤️ Autor

**Ryuu**

Proyecto mantenido para el:

**TECNO BG7**

---

## 📄 Licencia

Este proyecto contiene componentes provenientes de diferentes proyectos de código abierto.

Consulta las licencias correspondientes de cada componente antes de redistribuirlo.

---

## ⭐ Si este proyecto te resulta útil

Si este proyecto te ayudó a compilar OrangeFox para tu dispositivo, puedes darle una ⭐ al repositorio.

También puedes reportar problemas mediante **Issues** proporcionando:

* Log completo de GitHub Actions.
* Modelo exacto del dispositivo.
* Versión de Android.
* Archivo utilizado.
* Error reproducible.
* Información relevante del recovery.
