# CrudJSFPesitenciaprimefaces
#SQL
create table departamento(
id_dep serial primary key,
nombre varchar(20) 

);
create table empleado (
id_emp serial primary key ,
nombre varchar(50),
  id_dep int REFERENCES departamento(id_dep)
);

-- Insertar departamentos
INSERT INTO departamento (nombre) VALUES ('Ventas');
INSERT INTO departamento (nombre) VALUES ('Marketing');
INSERT INTO departamento (nombre) VALUES ('Recursos Humanos');

-- Insertar empleados
INSERT INTO empleado (nombre, id_dep) VALUES ('Ana López', 1);
INSERT INTO empleado (nombre, id_dep) VALUES ('Carlos Ramírez', 1);
INSERT INTO empleado (nombre, id_dep) VALUES ('María González', 2);
INSERT INTO empleado (nombre, id_dep) VALUES ('Luis Torres', 3);
INSERT INTO empleado (nombre, id_dep) VALUES ('Abel Gomez', 3);
