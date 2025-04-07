<!-- 
Nombre: Sergio Morales 
Curso: ASIR1 
Fecha: 06/04/2025 
Ejercicio: DTD5 
-->

<!-- 
 Documento XML con DTD interna corregida.
 En este caso, los errores estaban en la DTD (no en el contenido del XML).
 Se han corregido para que el documento sea válido.
-->

<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE curso [
  <!-- 
   Definición general:
  Un curso contiene uno o más alumnos. Cada alumno tiene nombre, edad y grupo.
  -->

  <!ELEMENT curso (alumno+)>

  <!--  Un alumno tiene nombre, edad y grupo en ese orden -->
  <!ELEMENT alumno (nombre, edad, grupo)>
  <!ELEMENT nombre (#PCDATA)>
  <!ELEMENT edad (#PCDATA)>
  <!ELEMENT grupo (#PCDATA)>
]>

<!--  Listado de alumnos del curso -->
<curso>
  <!--  Alumno 1 -->
  <alumno>
    <nombre>Lucía Ramírez</nombre>
    <edad>19</edad>
    <grupo>A</grupo>
  </alumno>

  <!--  Alumno 2 -->
  <alumno>
    <nombre>Carlos Pérez</nombre>
    <edad>20</edad>
    <grupo>B</grupo>
  </alumno>
</curso>
