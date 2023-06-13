# Pertemuan12
## ERD Karyawan

 Nama: Inayatus Sholekhawati
 
 NIM: 312210200
 
 Kelas: TI.22.A.2

## membuat tabel

```
CREATE TABLE departemen (
    ->     id_departemen INT PRIMARY KEY,
    ->     nama_departemen VARCHAR(50);
CREATE TABLE Karyawan (
    ->     id_karyawan INT PRIMARY KEY,
    ->     nama_karyawan VARCHAR(50),
    ->     id_departemen INT,
    ->     id_manager INT);
 CREATE TABLE supervisor (
    ->     id_supervisor INT PRIMARY KEY,
    ->     id_departemen INT,
    ->     id_karyawan INT);
CREATE TABLE project (
    ->     id_project INT PRIMARY KEY,
    ->     nama_project VARCHAR(50),
    ->     id_departemen INT);
 CREATE TABLE karyawan_project (
    ->     id_karyawan INT,
    ->     id_project INT); 
```

<img width="799" alt="image" src="https://github.com/inayy12/Pertemuan12/assets/115867315/4dcaa3a7-a24d-4247-ab60-b5cff8172338">

# Menyambungkan Tabel

```
 ALTER TABLE supervisor ADD CONSTRAINT FOREIGN KEY (id_departemen) REFERENCES departemen (id_departemen);
 ALTER TABLE supervisor ADD CONSTRAINT FOREIGN KEY (id_karyawan) REFERENCES karyawan (id_karyawan);
 ALTER TABLE project ADD CONSTRAINT FOREIGN KEY (id_departemen) REFERENCES departemen (id_departemen);
 ALTER TABLE karyawan_project ADD CONSTRAINT FOREIGN KEY (id_karyawan) REFERENCES karyawan (id_karyawan);
 ALTER TABLE karyawan ADD CONSTRAINT FOREIGN KEY (id_manager) REFERENCES karyawan (id_karyawan);
```
<img width="941" alt="ruto3" src="https://github.com/inayy12/Pertemuan12/assets/115867315/006b6d47-b2c5-4123-bdea-49c5f70de1de">

<img width="930" alt="ruto1" src="https://github.com/inayy12/Pertemuan12/assets/115867315/376ff669-63e7-48c0-a0aa-4fda9cf45dce">
