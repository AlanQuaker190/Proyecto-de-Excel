📊 Bakery Shopping List - Excel Automation Project
🥐 Proyecto: Lista de Compras para Panadería
Este proyecto simula la gestión de pedidos de ingredientes para una panadería con 5 empleados: Abby, Bill, Cathy, Derek y Emily. A lo largo del tiempo, cada empleado realiza pedidos para diferentes recetas, registrando las cantidades necesarias de diversos ingredientes. La finalidad es automatizar y facilitar la dispersión de estos ingredientes, asegurando un control claro y eficiente del inventario.

📝 Descripción del Proyecto
El archivo principal contiene una hoja de cálculo donde se registran las fechas, nombres de los empleados y las cantidades de ingredientes solicitados. A partir de esta información, el proyecto solicita implementar una sección dinámica que permita:

1. Seleccionar un empleado desde una lista desplegable.
2. Seleccionar un ingrediente desde una lista desplegable.
3. Mostrar automáticamente la cantidad total solicitada por ese empleado para dicho ingrediente.
4. Mostrar la unidad de medida correcta del ingrediente seleccionado (cups, tsp, etc.).
5. Importante: El sistema debe ser lo suficientemente robusto para actualizarse automáticamente si se añade una nueva fila con un pedido adicional.

✅ Requerimientos Clave
-Validación de datos en la celda E17: Solo permitir los nombres Abby, Bill, Cathy, Derek, Emily mediante lista desplegable.
-Validación de datos en la celda E18: Solo permitir los ingredientes Flour, Sugar, Baking powder, Baking soda, Salt, Milk, Butter, Vanilla, Eggs, Bananas mediante lista 
 desplegable.
-Cálculo automático en E20: Mostrar la suma total acumulada del ingrediente seleccionado por el empleado seleccionado.
-Unidad de medida mostrada en F20: Visualizar automáticamente la unidad correcta del ingrediente (cups, tsp, etc.).
-Actualización automática: El sistema debe actualizar resultados correctamente cuando se agreguen nuevas filas de datos.

🔧 Funcionalidades y Fórmulas Usadas
Este proyecto aplica y refuerza los siguientes conceptos y herramientas de Excel:

-Data Validation (Validación de Datos): Para restringir las entradas a valores específicos y facilitar selección desde listas desplegables.

-SUMA(SI()): Fórmula clave para sumar condicionalmente, combinando el nombre del empleado y el ingrediente seleccionado para obtener el total acumulado.

 Ejemplo:
 En E20: 
 =SUMA(SI((Name=ShoppingTable[Name])*(Ingredient=ShoppingTable[[#Encabezados];[Flour]:[Bananas]]);ShoppingTable[[Flour]:[Bananas]];""))

-INDICE() / COINCIDIR(): Para buscar la unidad de medida correspondiente al ingrediente seleccionado.

 Ejemplo:

 En F20:
 =SI(INDICE(C2:L2;COINCIDIR(E18;C3:L3;0))=0;"";INDICE(C2:L2;COINCIDIR(E18;C3:L3;0)))

-Tablas Dinámicas y Rango de Datos Expansible: Aunque no estrictamente necesario, el diseño permite fácilmente convertir el registro en una tabla para que se expanda 
 automáticamente con nuevas entradas.

-Referencias Absolutas y Nombres Definidos: Para mayor claridad y robustez al momento de manejar los rangos.

📚 Conceptos Reforzados:
-Gestión avanzada de listas desplegables.
-Uso efectivo de funciones condicionales.
-Aplicación de búsqueda y referencias cruzadas.
-Automatización en la actualización de cálculos ante nuevos datos.
-Diseño limpio y práctico de una hoja de cálculo interactiva.

🚀 Cómo Usar
-Abre el archivo Excel.
-En las celdas verdes (E17 y E18), selecciona un empleado y un ingrediente.
-Automáticamente verás en la celda amarilla (E20) la cantidad total acumulada, y en la celda a la derecha (F20) la unidad de medida correspondiente.
-Puedes agregar nuevas filas de pedidos y todo se actualizará sin intervención manual.
