### Bloque 1

##### Consultas

1. Listar los nombres de los usuarios

   ```sql
   SELECT nombre FROM tblUsuarios;
   ```

2. Calcular el saldo máximo de los usuarios de sexo “Mujer”

     ```sql
     SELECT MAX(saldo) FROM tblUsuarios WHERE sexo = "M";
     ```

3. Listar nombre y teléfono de los usuarios con teléfono NOKIA, BLACKBERRY o SONY

     ```sql
     SELECT nombre, telefono FROM tblUsuarios WHERE marca IN ("NOKIA", "BLACKBERRY", "SONY");
     ```

4. Contar los usuarios sin saldo o inactivos

     ```sql
     SELECT COUNT(idx) as sin_saldo_inactivos FROM tblUsuarios WHERE (saldo = 0) OR (activo = 0);
     ```

5. Listar el login de los usuarios con nivel 1, 2 o 3

     ```sql
     SELECT nombre, email FROM tblUsuarios WHERE NOT nivel = 0;
     ```

6. Listar los números de teléfono con saldo menor o igual a 300

     ```sql
     SELECT telefono FROM tblUsuarios WHERE (saldo <= 300);
     ```

7. Calcular la suma de los saldos de los usuarios de la compañia telefónica NEXTEL

     ```sql
     SELECT SUM(saldo) FROM tblUsuarios WHERE (compañia = "NEXTEL");
     ```

8. Contar el número de usuarios por compañía telefónica

     ```sql
     SELECT compañia, COUNT(idx) AS cantidad FROM tblUsuarios GROUP BY compañia;
     ```

9. Contar el número de usuarios por nivel

     ```sql
     SELECT nivel, COUNT(idx) AS cantidad FROM tblUsuarios GROUP BY nivel ORDER BY nivel ASC;
     ```

10. Listar el login de los usuarios con nivel 2

       ```sql
       SELECT nombre, email FROM tblUsuarios WHERE nivel = 2;
       ```

11. Mostrar el email de los usuarios que usan gmail

      ```sql
      SELECT email FROM tblUsuarios WHERE email LIKE ("%gmail%");
      ```

12. Listar nombre y teléfono de los usuarios con teléfono LG, SAMSUNG o MOTOROLA

      ```sql
      SELECT nombre, telefono FROM tblUsuarios WHERE marca IN ("LG", "SAMSUNG", "MOTOROLA");
      ```

------

### Bloque 2

##### Consultas

1. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca LG o SAMSUNG

     ```sql
     SELECT nombre, telefono FROM tblUsuarios WHERE marca NOT IN ("LG", "SAMSUNG");
     ```

2. Listar el login y teléfono de los usuarios con compañia telefónica IUSACELL

     ```sql
     SELECT nombre, email, telefono FROM tblUsuarios WHERE compañia = "IUSACELL";
     ```

3. Listar el login y teléfono de los usuarios con compañia telefónica que no sea TELCEL

     ```sql
     SELECT nombre, email, telefono FROM tblUsuarios WHERE NOT compañia = "IUSACELL";
     ```

4. Calcular el saldo promedio de los usuarios que tienen teléfono marca NOKIA

     ```sql
     SELECT compañia, AVG(saldo) AS saldo_promedio FROM tblUsuarios GROUP BY compañia;
     ```

5. Listar el login y teléfono de los usuarios con compañia telefónica IUSACELL o AXEL

     ```sql
     SELECT nombre, email, telefono FROM tblUsuarios WHERE compañia IN ("IUSACELL", "AXEL");
     ```

6. Mostrar el email de los usuarios que no usan yahoo

     ```sql
     SELECT email FROM tblUsuarios WHERE email NOT LIKE ("%yahoo%");
     ```

7. Listar el login y teléfono de los usuarios con compañia telefónica que no sea TELCEL o IUSACELL

     ```sql
     SELECT nombre, email, telefono FROM tblUsuarios WHERE compañia NOT IN ("TELCEL", "IUSACELL");
     ```

8. Listar el login y teléfono de los usuarios con compañia telefónica UNEFON

     ```sql
     SELECT nombre, email, telefono FROM tblUsuarios WHERE compañia ="UNEFON";
     ```

9. Listar las diferentes marcas de celular en orden alfabético descendentemente

     ```sql
     SELECT DISTINCT marca FROM tblUsuarios ORDER BY marca DESC;
     ```

10. Listar las diferentes compañias en orden alfabético aleatorio

      ```sql
      SELECT DISTINCT marca FROM tblUsuarios;
      ```

11. Listar el login de los usuarios con nivel 0 o 2

      ```sql
      SELECT nivel, nombre, email FROM tblUsuarios WHERE nivel IN (0,2) ORDER BY nivel;
      ```

12. Calcular el saldo promedio de los usuarios que tienen teléfono marca LG

      ```sql
      SELECT marca, AVG(saldo) AS saldo_promedio FROM tblUsuarios WHERE marca = "LG" GROUP BY marca;
      ```

------

### Bloque 3

##### Consultas

1. Listar el login de los usuarios con nivel 1 o 3

     ```sql
     SELECT nivel, nombre, email FROM tblUsuarios WHERE nivel IN (1,3) ORDER BY nivel;
     ```

2. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca BLACKBERRY

     ```sql
     SELECT nombre, telefono FROM tblUsuarios WHERE NOT marca = "BLACKBERRY";
     ```

3. Listar el login de los usuarios con nivel 3

     ```sql
     SELECT nivel, nombre, email FROM tblUsuarios WHERE nivel = 3;
     ```

4. Listar el login de los usuarios con nivel 0

     ```sql
     SELECT nivel, nombre, email FROM tblUsuarios WHERE nivel = 0;
     ```

5. Listar el login de los usuarios con nivel 1

     ```sql
     SELECT nivel, nombre, email FROM tblUsuarios WHERE nivel = 1;
     ```

6. Contar el número de usuarios por sexo

     ```sql
     SELECT sexo, COUNT(idx) AS cantidad FROM tblUsuarios GROUP BY sexo;
     ```

7. Listar el login y teléfono de los usuarios con compañia telefónica AT&T

     ```sql
     SELECT nombre, email, telefono FROM tblUsuarios WHERE compañia ="AT&T";
     ```

8. Listar las diferentes compañias en orden alfabético descendentemente

     ```sql
     SELECT DISTINCT compañia FROM tblUsuarios ORDER BY compañia DESC;
     ```

9. Listar el logn de los usuarios inactivos

     ```sql
     SELECT nombre, email FROM tblUsuarios WHERE activo = 0;
     ```

10. Listar los números de teléfono sin saldo

       ```sql
       SELECT telefono, saldo FROM tblUsuarios WHERE saldo = 0;
       ```

11. Calcular el saldo mínimo de los usuarios de sexo “Hombre”

      ```sql
      SELECT nombre, saldo FROM tblUsuarios WHERE sexo = "H" ORDER BY saldo ASC LIMIT 1;
      ```

12. Listar los números de teléfono con saldo mayor a 300

      ```sql
      SELECT telefono, saldo FROM tblUsuarios WHERE saldo >= 300;
      ```

------

### Bloque 4

##### Consultas

1. Contar el número de usuarios por marca de teléfono

     ```sql
     SELECT marca, COUNT(idx) AS cantidad FROM tblUsuarios GROUP BY marca;
     ```

2. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca LG

     ```sql
     SELECT nombre, telefono, marca FROM tblUsuarios WHERE NOT marca ="LG";
     ```

3. Listar las diferentes compañias en orden alfabético ascendentemente

     ```sql
     SELECT DISTINCT compañia FROM tblUsuarios ORDER BY compañia ASC;
     ```

4. Calcular la suma de los saldos de los usuarios de la compañia telefónica UNEFON

     ```sql
     SELECT compañia, SUM(saldo) AS saldo_total FROM tblUsuarios WHERE compañia = "UNEFON" GROUP BY compañia;
     ```

5. Mostrar el email de los usuarios que usan hotmail

     ```sql
     SELECT usuario, email FROM tblUsuarios WHERE email LIKE ("%hotmail%");
     ```

6. Listar los nombres de los usuarios sin saldo o inactivos

     ```sql
     SELECT nombre, saldo, activo FROM tblUsuarios WHERE (saldo = 0) OR (activo = 0);
     ```

7. Listar el login y teléfono de los usuarios con compañia telefónica IUSACELL o TELCEL

     ```sql
     SELECT nombre, email, telefono FROM tblUsuarios WHERE compañia IN ("TELCEL", "IUSACELL");
     ```

8. Listar las diferentes marcas de celular en orden alfabético ascendentemente

     ```sql
     SELECT DISTINCT marca FROM tblUsuarios ORDER BY marca ASC;
     ```

9. Listar las diferentes marcas de celular en orden alfabético aleatorio

     ```sql
     SELECT DISTINCT marca FROM tblUsuarios;
     ```

10. Listar el login y teléfono de los usuarios con compañia telefónica IUSACELL o UNEFON

      ```sql
      SELECT nombre, email, telefono FROM tblUsuarios WHERE compañia IN ("UNEFON", "IUSACELL");
      ```

11. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca MOTOROLA o NOKIA

      ```sql
      SELECT nombre, telefono FROM tblUsuarios WHERE marca NOT IN ("MOTOROLA", "NOKIA");
      ```

12. Calcular la suma de los saldos de los usuarios de la compañia telefónica TELCEL

      ```sql
      SELECT compañia, SUM(saldo) AS saldo_total FROM tblUsuarios WHERE compañia = "TELCEL" GROUP BY compañia;
      ```
