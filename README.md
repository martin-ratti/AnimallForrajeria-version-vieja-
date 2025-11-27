<div align="center">

# 🐾 Animall Forrajería - Legacy System

<img src="https://img.shields.io/badge/Estado-Legacy%20%2F%20Archivado-orange?style=for-the-badge&logo=archive&logoColor=white" alt="Estado Legacy"/>
<img src="https://img.shields.io/badge/Versión-Final_v1.0-grey?style=for-the-badge" alt="Version"/>

<br/>

<a href="https://github.com/martin-ratti" target="_blank" style="text-decoration: none;">
    <img src="https://img.shields.io/badge/👤%20Martín%20Ratti-martin--ratti-000000?style=for-the-badge&logo=github&logoColor=white" alt="Martin"/>
</a>

<br/>

<p>
    <img src="https://img.shields.io/badge/Lenguaje-C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white" alt="C# Badge"/>
    <img src="https://img.shields.io/badge/Framework-.NET%20Framework%204.x-512BD4?style=for-the-badge&logo=dotnet&logoColor=white" alt=".NET Badge"/>
    <img src="https://img.shields.io/badge/UI-Windows%20Forms-0078D4?style=for-the-badge&logo=windows&logoColor=white" alt="WinForms Badge"/>
    <img src="https://img.shields.io/badge/DB-Microsoft%20Access-A4373A?style=for-the-badge&logo=microsoftaccess&logoColor=white" alt="Access Badge"/>
</p>

</div>

---

## 🎯 Objetivo y Contexto Histórico

Este repositorio contiene el código fuente de la **versión original (Legacy)** del sistema de gestión para **Animall Forrajería**. Fue la primera solución digital implementada para administrar las operaciones diarias del local, reemplazando procesos manuales.

Aunque ha sido sucedida por versiones modernas (Web/Cloud), este código se mantiene como referencia de la lógica de negocio fundamental y los algoritmos de facturación originales.

---

## 🏛️ Arquitectura del Sistema

El proyecto sigue una arquitectura clásica de escritorio en capas, típica del desarrollo en .NET Framework de la época.

### Diagrama de Dependencias

| Componente | Tecnología | Responsabilidad |
| :--- | :--- | :--- |
| **Animall.app** | Windows Forms | Interfaz gráfica (MDI), gestión de eventos de usuario y validación visual. |
| **Animall.Core** | Class Library (C\#) | Contiene los modelos (`Venta`, `Producto`), la lógica de conexión `OleDb` y la generación de strings para tickets. |
| **Recursos** | Embedded Resources | Gestión de fuentes tipográficas (Arial, Courier) e imágenes incrustadas en el ensamblado. |

-----

## 🚀 Características Funcionales

  * **🏪 Punto de Venta (POS):** Interfaz optimizada para teclado (`MainForm`) para carga rápida de productos.
  * **💰 Gestión de Tesorería:**
      * **Apertura de Caja:** Declaración de fondos iniciales (`DineroInicialForm`).
      * **Arqueo y Cierre:** Control de ingresos diarios.
  * **💳 Métodos de Pago:** Soporte para efectivo, tarjetas y billeteras virtuales (`SeleccionarMetodos`).
  * **🧾 Motor de Impresión:** Generación de tickets de texto plano formateados para impresoras térmicas ESC/POS.
  * **🛡️ Seguridad Operativa:** Prevención de cierres accidentales mediante `ConfirmacionReinicioForm`.

-----

## 🛠️ Modo de Uso (Entorno de Desarrollo)

### Requisitos Previos

1.  **Visual Studio 2019/2022** con la carga de trabajo ".NET Desktop Development".
2.  **Microsoft Access Database Engine 2010/2016** (Driver OLEDB) instalado para permitir la conexión a `.accdb`.

### Estructura del Proyecto

```text
/AnimallForrajeria
├── Animall.sln            <-- Solución de Visual Studio
├── Animall.app/           <-- Proyecto de UI (Ejecutable)
│   ├── MainForm.cs        <-- Pantalla Principal de Ventas
│   ├── TicketForm.cs      <-- Previsualización de Tickets
│   └── Resources/         <-- Iconos y Assets
└── Animall.Core/          <-- Librería de Clases
    └── Class1.cs          <-- Lógica central (Conexión DB y Modelos)
```

### Pasos para Ejecutar

1.  Clonar el repositorio.
2.  Abrir `Animall.Core.sln` (o la solución unificada).
3.  Verificar que la cadena de conexión en `Animall.Core` apunte correctamente al archivo `.accdb` (por defecto `./Animall_db.accdb`).
4.  Compilar y ejecutar con **F5**.

> ⚠️ **Nota Legacy:** Es posible que sea necesario ejecutar Visual Studio como Administrador si la aplicación intenta escribir logs o acceder a puertos de impresión directos.

-----

## 📦 Despliegue

El proyecto incluye perfiles de publicación (`FolderProfile.pubxml`) configurados para generar un ejecutable portable para Windows (x86/x64).

-----

## ⚖️ Créditos y Licencia

Desarrollado por **Martín Ratti**.
*Software propietario desarrollado exclusivamente para Animall Forrajería. No apto para uso público sin autorización.*
