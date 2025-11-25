<h1 align="center">🐾 Animall Forrajería - Legacy System</h1>

<div align="center">
    <img src="https://img.shields.io/badge/Estado-Legacy%20%2F%20Archivado-orange?style=for-the-badge&logo=archive&logoColor=white" alt="Estado Badge"/>
    <img src="https://img.shields.io/badge/Versión-Old-grey?style=for-the-badge" alt="Version Badge"/>
</div>

<p align="center">
    <a href="https://github.com/martin-ratti" target="_blank" style="text-decoration: none;">
        <img src="https://img.shields.io/badge/👤%20Martín%20Ratti-martin--ratti-000000?style=for-the-badge&logo=github&logoColor=white" alt="Martin"/>
    </a>
</p>

<p align="center">
    <img src="https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white" alt="CSharp Badge"/>
    <img src="https://img.shields.io/badge/.NET-Framework-512BD4?style=for-the-badge&logo=dotnet&logoColor=white" alt="DotNet Badge"/>
    <img src="https://img.shields.io/badge/UI-Windows%20Forms-0078D4?style=for-the-badge&logo=windows&logoColor=white" alt="WinForms Badge"/>
    <img src="https://img.shields.io/badge/IDE-Visual%20Studio-5C2D91?style=for-the-badge&logo=visual-studio&logoColor=white" alt="VS Badge"/>
</p>

<hr>

<h2>🎯 Objetivo y Alcance</h2>

<p>
    Este repositorio contiene el código fuente de la <strong>versión original (Legacy)</strong> del sistema de gestión para <strong>Animall Forrajería</strong>. 
    Es una aplicación de escritorio robusta diseñada para administrar las operaciones diarias del local, desde la apertura de caja hasta la emisión de tickets.
</p>

<p>
    Aunque ha sido sucedida por versiones más nuevas, este código sirve como referencia histórica de la lógica de negocio y la estructura base sobre la cual operaba la forrajería.
</p>

<hr>

<h2>⚙️ Stack Tecnológico & Arquitectura</h2>

<p>El proyecto sigue una arquitectura clásica de Windows Forms separada en capas lógicas.</p>

<table>
 <thead>
  <tr>
   <th>Capa / Proyecto</th>
   <th>Tecnología</th>
   <th>Descripción</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><strong>Animall.app</strong></td>
   <td>Windows Forms (.NET)</td>
   <td>La interfaz gráfica de usuario. Contiene todos los formularios (<code>MainForm</code>, <code>TicketForm</code>), gestión de eventos y controles de usuario.</td>
  </tr>
  <tr>
   <td><strong>Animall.Core</strong></td>
   <td>C# Class Library</td>
   <td>Biblioteca de clases base. Contiene lógica compartida, utilidades y gestión de recursos tipográficos (Fuentes).</td>
  </tr>
  <tr>
   <td><strong>Recursos</strong></td>
   <td>Embedded Resources</td>
   <td>Gestión interna de imágenes (iconos, logos) y fuentes personalizadas (Arial, Courier) embebidas en el ensamblado.</td>
  </tr>
 </tbody>
</table>

<hr>

<h2>🚀 Características Funcionales</h2>

<ul>
    <li><strong>🏪 Punto de Venta (POS)</strong>: Interfaz principal (<code>MainForm</code>) para la carga y procesamiento de ventas.</li>
    <li><strong>💰 Gestión de Caja</strong>:
        <ul>
            <li><strong>Apertura:</strong> Módulo <code>DineroInicialForm</code> para declarar el fondo de caja al inicio del turno.</li>
            <li><strong>Cierre y Arqueo:</strong> Funcionalidad para el control de ingresos.</li>
        </ul>
    </li>
    <li><strong>💳 Métodos de Pago</strong>: Módulo <code>SeleccionarMetodos</code> para procesar cobros en efectivo, tarjetas o billeteras virtuales.</li>
    <li><strong>🧾 Emisión de Comprobantes</strong>: Sistema de generación de tickets (<code>TicketForm</code>) diseñado para impresoras térmicas, utilizando fuentes monoespaciadas (Courier) para una alineación perfecta.</li>
    <li><strong>🛡️ Seguridad Operativa</strong>: Confirmaciones críticas (<code>ConfirmacionReinicioForm</code>) para evitar cierres accidentales del sistema.</li>
</ul>

<hr>

<h2>🛠️ Modo de Uso (Desarrollo)</h2>

Al ser una aplicación de escritorio .NET, se requiere un entorno Windows para su ejecución nativa.

<pre>
/AnimallForrajeria
├── Animall.sln            <-- Solución principal
├── Animall.app/           <-- Proyecto de Interfaz
│   ├── MainForm.cs        <-- Pantalla Principal
│   └── TicketForm.cs      <-- Diseño de Tickets
└── Animall.Core/          <-- Lógica de Negocio
</pre>

<h3>Pasos para Ejecutar</h3>
<ol>
    <li><strong>Prerrequisitos:</strong> Instalar Visual Studio (2019 o superior) con la carga de trabajo ".NET Desktop Development".</li>
    <li><strong>Clonar:</strong> Descarga este repositorio en tu máquina local.</li>
    <li><strong>Abrir:</strong> Ejecuta el archivo <code>Animall.Core.sln</code> (o la solución principal si está unificada).</li>
    <li><strong>Restaurar:</strong> Visual Studio restaurará automáticamente los paquetes NuGet necesarios.</li>
    <li><strong>Compilar:</strong> Presiona <code>F5</code> o el botón "Iniciar" para compilar y ejecutar en modo Debug.</li>
</ol>

<hr>

<h2>📦 Despliegue</h2>

El proyecto incluye perfiles de publicación configurados (<code>FolderProfile.pubxml</code>) para generar ejecutables portables o instalables en entornos Windows.

<hr>

<h2>⚖️ Créditos</h2>

<p>
    Desarrollado por <strong>Martín Ratti</strong>. 
    <em>Este software es propietario y fue desarrollado específicamente para las necesidades de Animall Forrajería.</em>
</p>
