# Kakebo
...
## 1. Fundamentos del sistema
El objetivo principal es contar con una app que contabilice todos y cada uno de los gastos e ingresos de una persona. Y que con un analisis de gastos, posible ahorros, e inversiones, se le sugiera al usuario, una serie de acciones para que se pueda lleagar a una estabilidad/libertad, financiera/económica.

## 2. Análisis y especificación de requisitiso
Requisitos Funcionales
Se dividen entre las funcionalidades base (gratuitas) y las avanzadas (suscripción de pago).

Módulo Base (Freeware)

Consolidación Financiera Temporal:
La aplicación calculará automáticamente el balance neto (ingresos menos gastos) abarcando estrictamente desde el primer día hasta el último día del mes en curso (día 28, 30 o 31 según corresponda).

Categorización Automática y Agregación:
El sistema clasificará de forma inteligente cada transacción saliente en categorías predefinidas y personalizables (ej. Vivienda, Alimentación, Ocio, Transporte) mediante algoritmos de procesamiento del lenguaje natural, mostrando subtotales desglosados por categoría.

Proyección de Capacidad de Ahorro a 6 Meses:
Con base en el historial de ingresos estables y variables (incluyendo transferencias de Bizum y plataformas de movilidad), la app proyectará un modelo predictivo a 6 meses de la capacidad real de ahorro del usuario, sugiriendo estrategias de redistribución de saldo.

Optimización de Gasto Prescindible:
El sistema analizará los patrones de consumo para identificar gastos hormiga o suscripciones recurrentes no esenciales, sugiriendo recortes concretos orientados a cumplir con un objetivo de ahorro mensual estandarizado.

Módulo Premium (Suscripción de Pago)

Asistente de Inversión Anti-Inflación:
Análisis patrimonial: Generará un informe del ahorro acumulado.

Recomendación de cartera: Propondrá vehículos de inversión (fondos indexados, ETFs, etc.) orientados a superar la tasa de inflación anual para preservar el poder adquisitivo.

Onboarding guiado: Proveerá un tutorial interactivo paso a paso para simplificar los trámites iniciales de inversión.

Canal de Consulta Directa con Expertos (Broker Chat):
Ofrecerá acceso temporal (durante 7 días a elección por cada usuario) a un chat integrado con asesores financieros certificados de la entidad bancaria asociada para resolver dudas de perfil de riesgo y operativa de mercado.

Requisitos No Funcionales

Seguridad y Cumplimiento Normativo:
Cifrado de datos: Todo el tráfico de datos y almacenamiento local/en nube deberá utilizar cifrado de extremo a extremo.

El acceso a las cuentas y tarjetas de la entidad asociada y terceros deberá cumplir rigurosamente con los protocolos de autenticación de clientes.

Rendimiento y Disponibilidad:

Tiempos de respuesta: La sincronización y actualización de movimientos de tarjetas y pasarelas de pago (Bizum, BlaBlaCar) no puede superar 1 minuto desde la apertura de la app.

Disponibilidad del servicio: El servidor backend deberá garantizar un tiempo de actividad (uptime) mínimo del 99.5% anual. Es decir, que no se pase del tiempo estimado de mantenimiento. 
Modelo de Licenciamiento y Distribución:

Freeware Privado: El software se distribuirá de forma totalmente gratuita al usuario final, pero mantendrá el código fuente bajo estricta propiedad privativa (cerrado), prohibiendo de forma nativa la ingeniería inversa, descompilación o redistribución de modificaciones.
Colaboración y Perfiles de Desarrollo (Equipo Mixto):
El proyecto se desarrollará bajo un modelo de co-creación con la entidad bancaria aliada (ej. BBVA), integrando perfiles especializados: un Desarrollador Backend/API, un Analista de Datos (Data Scientist) para los modelos de predicción de ahorro, y un Especilista en Marketing Digital y UX para la conversión del modelo Freemium.
Mantenimiento Automatizado y Auditoría de Errores:
El sistema ejecutará una batería de pruebas de integración y diagnóstico automatizadas todos los domingos a las 00:00 h, generando un informe de incidencias (log de errores) en formato de texto estructurado para facilitar la revisión del equipo de desarrollo cada lunes a primera hora.

## 3. Diseño
https://viewer.diagrams.net/?tags=%7B%7D&lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&title=Mi_empresa.drawio&dark=auto#R%3Cmxfile%3E%3Cdiagram%20name%3D%22P%C3%A1gina-1%22%20id%3D%22yFOmNwyrJ4fZHQxHq2fi%22%3E7Vxfd6I4FP80njP7UA8hgvCISrucVeyKzkznjQpVdpR0EFudT79BgkqgFDURpjMP0yGXEML9%2B7s3iQ3YXW7uAvt5PkCOu2iIgrNpwF5DFIGsyvi%2FiLIlFCDAmDILPIfQDgTL%2B%2BkSokCoa89xV6mOIUKL0HtOE6fI991pmKLZQYBe092e0CL91md75mYI1tReZKlfPCecx1RFbB%2Fof7vebJ68GX9yfGdpJ53Jl6zmtoNej0hQb8BugFAYXy03XXcRcS%2FhS%2Fzc7Rt39xMLXD8s88Dq24%2F57eBf8atvr79D%2B3Hzr3l7kzMKIa3CbcKDVRig7%2FvPxxPvzMPlAl8CfIk%2F6znqt9zMIhVoPi3Q63RuB2EzdIOl59shCnC317kXutazPY36vuKemBa%2F6MVerMmLbg2T0NwgdDdH8yGfdOeipRsGW9xlfsR1mbD49SAhIBAaGQVKpJ0ootAiBJtoyGw%2F9oGJ%2BILw8QSetuJxXSejWVkmo3UwdQvGEjPCiIa1SBMF4RzNkG8v9AO1E6C177jRDAXcOvTpI%2FRMhPafG4ZbYmz2OkRpkRIzs4OZGxbMDWbkly%2BpwF3YofeSZgZzrou10mTDNLrG8FrKzE2VZYaqDGusylJVqvxDkL6YM2iihzt0%2F9nR%2FLY6vUmHNPsx4ZeQZX6R1ChO9%2B1HHJxT3LEX3szH11M8nhvpdqSqHg5%2BGrmx9BwnFoS78n6SmUSieEaeH%2B6%2BW%2Bo0pB6mPCE%2FJGIAYp5JQPwGUTDMsW6Oy1tGLsfJIzdCE0AJvi0FMtx9NNmjLujpaYXVgRbT%2Fq3n2wss44TyHMixG8r4qBzvMh4Ne5OuMcL0iTXRRpGvER7wv%2B4Q39MsvdGFDRVozDyQSHmgFhVOubkghaELkmrsgtq1iqbgUh%2BkVOGDMiy0DCaORmgKAminFF6skddJcqVf10bwLIPt1%2BPGQzRYU0qavQ0ZPG5tSaukbWWRqjm80Lp2j2pBYG%2BPOhCNzOoA0aOWkvaakE7Z3ukP2gKlP%2FEM8p%2BWxPy37acb8408xV4tpTLBMJij5eN69QauptG54a88xy0fKLvD0UjvjnEYlBd4Ch3He8GXs3DXNyY9BtGHU0RMSnU9I4juMfsJOF5sM4iiuZCSJZBvF3oIH%2FmRS5iug5edRwAZ%2F7C7ddCvXY8zfAYNOFdYnROCsvMUzlEr6yly%2BVRZIlDEaf5wMk5WhZ6O%2F1iGNdYH3JAjkCmdV3npvHiCzh%2Fpsu9oUd0wgiQLe7Xypml%2BpnX5NCVMGcU%2B5glNRU2HPbC%2F%2F0bc27Xu3cDDnIpA0ynBEJRU8WO5Jn4qV%2B2PhC2lZY1xUysdwJpqi3FMlRSY1idQHFNVSv9k6ZSY2oLU2yClvbH3zMTU7EAgPRAQJMwtClWyC9C5BnJmalXkOD9kUKgsNcuvDp2J9n87san1Etsp4eh3FhsoG6CuI7caZDHWsI8B2njS062zUBkAWVimUqgMULmizAuVgTOXx4o888e0g8rW1%2FLRNEu0UBO5HSB4Cn%2B%2FA765SFuULhTueQUpIW32klAAhlnBzqtltbfD0UDDma2ZpLbdiW6OuWW2IlXNgfwy2zPLOUUwqXJb3Hjh16Prh6PrgyFGjVQS%2FEGs9yJ1UEtBlL3QQAmY8r55DSa6NR5hYxIM826kW8PzsEkJu1KltI%2BSJF5m1WZoViCntPQnxlWZgJUq%2F7E2k47W18yunkSgwZkQvkz4oSB8i1v4ARJLOyneF3R9O6GWIMX31iA5JsGVmQpLfFEbAROAQVaVT4MYJ65L86tnXT1DoLyK1LpChpB8xcfSv9xA%2FN5KDx%2Fv0q7Su4gsK6H1lm5FngIolcoX%2FpEvZ%2FleGgouky%2FLCm7N5VtJmiRUKV1Qag8z3wWP%2B5E%2BMCbnnQVSspmSkk6UJGrv8n5TK3teXqnUOdKtyUCPypza4L5vaD12J0%2BoJFNW6CSTVzEGslzmBvnbkX%2BBhaJL8X4W0FNVapnewcJ500kiCt420RkN%2F9FH3KottCFAVeFlCEyToZpU%2B%2F8Ywl4U1wsOlj7QTK0f1%2Bw%2FY%2BMwhia%2FeqSspvkLFG7LYTmHUnhw8n5oGZ1%2BxLEq%2BAcFXvyDLOu5Yk32JuWX%2B%2FYVvhPKfbxLNG9v%2Fb56sY9SuVbReRNWfhCSYnOZo2aF6luz867m8JM5JJnMX6WdxDvnXQVFTu8bvinA35SQmR5Ey5cEywXU2jiSSpxCQW5%2Bba%2FQFvKBEl%2BvoFzqFfL3mFXvFXD7U3QuVYh9w4Cdb2inj6gmB2Bq4RrEUvtoL8dotwZGuMY3bbTDu9Zu8xcffEavtyv8tnupDN0qqN3ey6Z8WGOPXGukyjvjOfkE1AfctQJFliFVqJ3so%2BNbJxTcfxuxs1xDqx2SOlo2q0zob5%2BNrEzmrUshT%2F5aWtWQh92PcKiyfBVIg5uH3%2BWLux9%2B3hDq%2FwM%3D%3C%2Fdiagram%3E%3C%2Fmxfile%3E

## 4. Implementación
package com.mycompany.corrigiendo_codificacion_fea;
public class Hola {
public static void main(String[] args) {
System.out.println("Hola mundo");
if (true) {
System.out.println("Condición verdadera");
} else {
System.out.println("Condición falsa");
}
}
}

-----------------------------------------------------------------

package com.mycompany.corrigiendo_codificacion_fea;
public class Area {
public static void main(String[] args) {
double r = 5;
double area = Math.PI * r * r;
System.out.println("El área es " + area);
}
}

-----------------------------------------------------------------


public class OperacionesMatematicas {
public static int sumarNumeros(int numeroUno, int numeroDos) {
return numeroUno + numeroDos;
}
public static int restar(int a, int b) {
return a - b;
}
public static int multiplicacion(int num1, int num2) {
return num1 * num2;
}
public static int divisionDeEnteros(int dividendo, int divisor) {
return dividendo / divisor;
}
public static void main(String[] args) {
System.out.println(sumarNumeros(3, 4));
System.out.println(restar(5, 2));
System.out.println(multiplicacion(2, 6));
System.out.println(divisionDeEnteros(8, 2));
}
}

-----------------------------------------------------------------


// Este método suma dos números
public int sumar(int x, int y) {
return x + y;
}
// Este método resta dos números
public int restar(int x, int y) {
return x - y;
}
// Este método multiplica dos números
public int multiplicar(int x, int y) {
return x * y;
}
// Este método divide dos números
public int dividir(int x, int y) {
return x / y;
}
public static void main(String[] args) {
Calculadora c = new Calculadora();
System.out.println("resultado:" + c.sumar(5, 3));
}
}

-----------------------------------------------------------------


/ Clase de alumno
public class alumno {
private String nombre;
private int edad;
private double NotaFinal;
public alumno(String n, int e, double nf) {
nombre = n;
edad = e;
NotaFinal = nf;
}
public void Mostrardatos() {
System.out.println("Alumno: " + nombre + ", Edad:" + edad + ", Nota Final:" +
NotaFinal);
}
public boolean aprobado() {
if (NotaFinal >= 5.0) {
return true;
} else {
return false;
}
}
public void mensajeFinal() {
if (aprobado()) {
System.out.println("felicidades " + nombre + " aprobaste!");
} else {
System.out.println("Lo siento " + nombre + " no aprobaste");
}
}
}
class curso {
private String nombre_curso;
private alumno[] lista;
public curso(String n, alumno[] l) {
nombre_curso = n;
lista = l;
}
public void mostrarTodo() {
System.out.println("curso: " + nombre_curso);
for (alumno a : lista) {
a.Mostrardatos();
a.mensajeFinal();
}
}
public static void main(String[] args) {
alumno a1 = new alumno("ana", 18, 6.5);
alumno a2 = new alumno("PEDRO", 19, 4.3);
alumno a3 = new alumno("Lucia", 17, 8.7);
alumno[] lista = {a1, a2, a3};
curso c1 = new curso("programacion", lista);
c1.mostrarTodo();
}
}



## 5. Plan de pruebas del sistema
Añade aquí lo que hicimos para diseñar las pruebas
Nada por aquí

### 5.1. Pruebas de aceptación
Nada por aquí 

## 7. Los diccionarios de datos
