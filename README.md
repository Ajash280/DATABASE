# DATABASE
use atom;
CREATE TABLE suppliers(supplier_id int NOT NULL, supplier_name char(50) NOT NULL, contact_name char(50), address char(50), city char(50), category_type char(50));
desc suppliers;

INSERT into suppliers VALUES (101,'HCL', 'HCL PVT Ltd', 'Grant Road, Mumbai', 'Mumbai', 'Hardware'), (102,'EA', 'EA Games Ltd.', 'Andheri Mumbai', 'Mumbai', 'Software'), (103, 'IBM', 'IBM PVT Itd', 'Chandni Chowk Delhi', 'Delhi', 'Hardware'), (101, 'LENOVO', 'LEN PVT Itd.', 'Pune Maharashtra ','Pune', 'Hardware');
select * from suppliers;

CREATE VIEW hardware_suppliers AS SELECT supplier_id, supplier_name FROM suppliers WHERE category_type = 'Hardware';

ALTER VIEW hardware_suppliers AS SELECT supplier_id, supplier_name, address, city FROM suppliers WHERE category_type = 'Hardware';
SELECT * FROM hardware_suppliers;
