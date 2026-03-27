# Generador de Taxonomías - Nissan México 🚗

Este repositorio contiene los archivos necesarios para limpiar, filtrar y formatear la información de los vehículos de Nissan. El archivo final alimenta la herramienta online que utilizamos para generar las taxonomías del sitio web.

## 📁 ¿Qué hace cada archivo?

En este repositorio encontrarás dos archivos principales de Excel:

1. **`taxo-nissan-formulas.xlsm` (El Motor):** Este archivo contiene las fórmulas y la macro. Se encarga de recibir la información cruda, eliminar textos repetitivos (como la palabra "NEW" o el modelo duplicado en la versión) y generar una tabla limpia. 
2. **`archivo_nissan_taxo.xlsx` (El Resultado Final):** Este es el archivo de texto plano. Es el único que lee la herramienta online a través de GitHub. **Solo se debe modificar pegando los valores limpios que arroja el archivo intermedio.**

---

## 🚀 Paso 1: Duplicar (Clonar) el repositorio en tu computadora

Si es la primera vez que vas a actualizar las taxonomías, necesitas descargar esta carpeta a tu Mac/PC.

1. Abre la **Terminal** (Mac) o **Símbolo del sistema / Git Bash** (Windows).
2. Ve a la carpeta donde quieres guardar los archivos (por ejemplo, Documentos):
   ```bash
   cd ~/Documentos
   ```
3. Ejecuta el siguiente comando para clonar el repositorio:
   ```bash
   git clone [https://github.com/Charlyenlaweb/taxonomias-nissan.git](https://github.com/Charlyenlaweb/taxonomias-nissan.git)
   ```
4. Entra a la carpeta que se acaba de crear:
   ```bash
   cd taxonomias-nissan
   ```

---

## 🛠️ Paso 2: Proceso de actualización de datos

Cuando recibas el archivo original de Nissan con el nuevo inventario, sigue estos pasos:

### A. Preparar los datos
Abre el archivo original de Nissan y copia **únicamente** estas 5 columnas en este orden exacto:
1. Año / Cuota
2. Vehículo / Modelo
3. Versión / Descripción
4. Color Interior / Interior
5. Color Exterior / Exterior

*(Nota: Con ayuda de los filtros Ignora los vehículos de Infiniti o columnas adicionales que no sean estas 5).*

> 📸 *<img width="1679" height="993" alt="archivo-cabeceras-y-tipificaciones" src="https://github.com/user-attachments/assets/3009d088-5c65-48ad-acc4-7df4c5e8defc" />
*
> `![Selección de columnas](ruta-de-tu-imagen1.jpg)`

### B. Limpiar los datos
1. Abre el archivo **`taxo-nissan-formulas.xlsm`**. *(Asegúrate de habilitar las macros si Excel te lo pregunta).*
2. Ve a la hoja **"Pegar Datos"**.
3. Pega la información que copiaste a partir de la celda **A2** (debajo de los encabezados).
4. Haz clic en el botón **"Generar Texto Plano"** que se encuentra en esa misma hoja.

> 📸 *<img width="1679" height="994" alt="archivo-taxo-nissan-formulas" src="https://github.com/user-attachments/assets/806a41be-22f6-45d0-9dfd-85f128060d4e" />
*
> `![Pegar datos y botón de macro](ruta-de-tu-imagen2.jpg)`

Al presionar el botón, la macro automáticamente procesará las fórmulas y te llevará a la hoja **"Texto Plano"** con la información ya filtrada y lista.

### C. Guardar el resultado final
1. Copia toda la información resultante de la hoja "Texto Plano".
2. Abre el archivo **`archivo_nissan_taxo.xlsx`**.
3. Pega la información **como Valores** para no arrastrar ningún formato raro.
4. Guarda y cierra ambos archivos de Excel.

> 📸 *<img width="1678" height="1018" alt="archivo-nissan-taxo" src="https://github.com/user-attachments/assets/b39da541-4363-43c6-a1df-67ac56c46936" />
*
>  `![Pegar datos y botón de macro](ruta-de-tu-imagen3.jpg)`
---

## ☁️ Paso 3: Subir los cambios a GitHub

Para que la herramienta online lea los datos nuevos, hay que subir la actualización. Abre tu Terminal en la carpeta del repositorio y ejecuta estos comandos uno por uno:

1. Prepara los archivos modificados:
   ```bash
   git add .
   ```
2. Crea un punto de guardado con un mensaje descriptivo:
   ```bash
   git commit -m "Actualización de inventario y taxonomías Nissan 'Fecha DD/MM/YYYY' "
   ```
3. Sube los cambios a la nube:
   ```bash
   git push
   ```

¡Listo! La URL cruda de GitHub se actualizará automáticamente y la herramienta online ya tendrá la información más reciente.
