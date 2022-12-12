# VIEWS 
> Una vista es la definición de una Query.
## Tipos de Opciones en Views
> 1. **Schemabinding:** Evita que se altere los campos de una tabla si una vista utiliza dicha columna.
> 2. **ENCRYPTION:** Agrega un nivel de seguridad donde solo los usuarios con los permisos pertinentes puedan acceder al codigo fuente de la vista.
> 3. **CHECK OPTION:** Evita la actualizacion sobre la tabla a la que la vista apunta.

## Vistas indexadas.
### Tipos de Indices
>  **No indice: ** Los registros se guardan segun el orden de insercion.
>  **Unique Clostered Index: ** Los registros respetan la secuencia de la primary key y acomoda el indice si es necesario.
>  **No clustered Index: ** Crea una especie de talas para cada indice en un orden logico para cuestion de filtrado.<br/>
> ***Nota*** SQL SERVER tiene algo llamado refresh view, que hace que se actualice automaticamente los indices ya sea cuando se modifican e insertan registros en la vista o en la tabla.

## Restricciones
> 1. No se puede agregar la clausula order by solo si tiene la clausula top, offset o for xml
> 2. No se pueden pasar parametros.

# INLINE-FUNCTION

> Resive un solo select (solo se ejecuta un solo select) - Cumple las mismas condiciones que las vistas con la diferencia que admite parametros. Admiten valores por defecto en los parametros de la funcion.

## Tipos de Opciones en las inline-function
> 1. **Schemabinding:** Evita que se altere los campos de una tabla si una vista utiliza dicha columna.
> 2. **ENCRYPTION:** Agrega un nivel de seguridad donde solo los usuarios con los permisos pertinentes puedan acceder al codigo fuente de la vista.

# Pasar multiples valores a una funcion
> Sql tiene la bondad de permitirnos definir nuestros propios tipos. Y definimos que el paremtros de la funcion reciba un parametro de ese tipo (que realmente es una tabla temporal parecido a una enumeracion).

```
CREATE TYPE ProductCategory AS TABLE (categoria int);
```
