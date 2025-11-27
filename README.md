<div align="center">

# 🐾 Animall Forrajería - Legacy System

<img src="https://img.shields.io/badge/Estado-Legacy%20%2F%20Archivado-orange?style=for-the-badge&logo=archive&logoColor=white" alt="Estado Badge"/>
<img src="https://img.shields.io/badge/Versión-Old-grey?style=for-the-badge" alt="Version Badge"/>

<br/>

<a href="https://github.com/martin-ratti" target="_blank" style="text-decoration: none;">
    <img src="https://img.shields.io/badge/👤%20Martín%20Ratti-martin--ratti-000000?style=for-the-badge&logo=github&logoColor=white" alt="Martin"/>
</a>

<br/>

<p>
    <img src="https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white" alt="CSharp Badge"/>
    <img src="https://img.shields.io/badge/.NET-Framework-512BD4?style=for-the-badge&logo=dotnet&logoColor=white" alt="DotNet Badge"/>
    <img src="https://img.shields.io/badge/UI-Windows%20Forms-0078D4?style=for-the-badge&logo=windows&logoColor=white" alt="WinForms Badge"/>
    <img src="https://img.shields.io/badge/IDE-Visual%20Studio-5C2D91?style=for-the-badge&logo=visual-studio&logoColor=white" alt="VS Badge"/>
</p>

</div>

---

## 🎯 Objetivo y Alcance

Este repositorio contiene el código fuente de la **versión original (Legacy)** del sistema de gestión para **Animall Forrajería**. Es una aplicación de escritorio robusta diseñada para administrar las operaciones diarias del local, desde la apertura de caja hasta la emisión de tickets.

Aunque ha sido sucedida por versiones más nuevas, este código sirve como referencia histórica de la lógica de negocio y la estructura base sobre la cual operaba la forrajería.

---

## ⚙️ Stack Tecnológico & Arquitectura

El proyecto sigue una arquitectura clásica de Windows Forms separada en capas lógicas.

| Capa / Proyecto | Tecnología | Descripción |
| :--- | :--- | :--- |
| **Animall.app** | Windows Forms (.NET) | La interfaz gráfica de usuario. Contiene todos los formularios (`MainForm`, `TicketForm`), gestión de eventos y controles de usuario. |
| **Animall.Core** | C# Class Library | Biblioteca de clases base. Contiene lógica compartida, utilidades y gestión de recursos tipográficos (Fuentes). |
| **Recursos** | Embedded Resources | Gestión interna de imágenes (iconos, logos) y fuentes personalizadas (Arial, Courier) embebidas en el ensamblado. |

---

## 🚀 Características Funcionales

* **🏪 Punto de Venta (POS):** Interfaz principal (`MainForm`) para la carga y procesamiento de ventas.
* **💰 Gestión de Caja:**
    * **Apertura:** Módulo `DineroInicialForm` para declarar el fondo de caja al inicio del turno.
    * **Cierre y Arqueo:** Funcionalidad para el control de ingresos.
* **💳 Métodos de Pago:** Módulo `SeleccionarMetodos` para procesar cobros en efectivo, tarjetas o billeteras virtuales.
* **🧾 Emisión de Comprobantes:** Sistema de generación de tickets (`TicketForm`) diseñado para impresoras térmicas, utilizando fuentes monoespaciadas (Courier) para una alineación perfecta.
* **🛡️ Seguridad Operativa:** Confirmaciones críticas (`ConfirmacionReinicioForm`) para evitar cierres accidentales del sistema.

---

## 🛠️ Modo de Uso (Desarrollo)

Al ser una aplicación de escritorio .NET, se requiere un entorno Windows para su ejecución nativa.

```text
/AnimallForrajeria
├── Animall.sln            <-- Solución principal
├── Animall.app/           <-- Proyecto de Interfaz
│   ├── MainForm.cs        <-- Pantalla Principal
│   └── TicketForm.cs      <-- Diseño de Tickets
└── Animall.Core/          <-- Lógica de Negocio
````

### Pasos para Ejecutar

1.  **Prerrequisitos:** Instalar Visual Studio (2019 o superior) con la carga de trabajo ".NET Desktop Development".
2.  **Clonar:** Descarga este repositorio en tu máquina local.
3.  **Abrir:** Ejecuta el archivo `Animall.Core.sln` (o la solución principal si está unificada).
4.  **Restaurar:** Visual Studio restaurará automáticamente los paquetes NuGet necesarios.
5.  **Compilar:** Presiona `F5` o el botón "Iniciar" para compilar y ejecutar en modo Debug.

-----

## 📦 Despliegue

El proyecto incluye perfiles de publicación configurados (`FolderProfile.pubxml`) para generar ejecutables portables o instalables en entornos Windows.

-----

## ⚖️ Créditos

Desarrollado por **Martín Ratti**.
*Este software es propietario y fue desarrollado específicamente para las necesidades de Animall Forrajería.*
