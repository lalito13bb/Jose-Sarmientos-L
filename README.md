# Jose-Sarmientos-L
aqui creo los roles
CREATE ROLE 'admin';
CREATE ROLE 'editor';
CREATE ROLE 'lector';

Asignar privilegios
GRANT ALL PRIVILEGES ON mi_empresa.* TO 'admin';
GRANT SELECT, INSERT, UPDATE ON mi_empresa.* TO 'editor';
GRANT SELECT ON mi_empresa.* TO 'lector';

se crea los usuarios y asignar roles
CREATE USER 'ana'@'localhost' IDENTIFIED BY 'claveAna';
GRANT 'admin' TO 'ana'@'localhost';
SET DEFAULT ROLE 'admin' TO 'ana'@'localhost';

CREATE USER 'juan'@'localhost' IDENTIFIED BY 'claveJuan';
GRANT 'editor' TO 'juan'@'localhost';
SET DEFAULT ROLE 'editor' TO 'juan'@'localhost';

CREATE USER 'sofia'@'localhost' IDENTIFIED BY 'claveSofia';
GRANT 'lector' TO 'sofia'@'localhost';
SET DEFAULT ROLE 'lector' TO 'sofia'@'localhost';
