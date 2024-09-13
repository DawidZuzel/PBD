3.CREATE DATABASE Imie_Nazwisko;

4.CREATE TABLE Uczniowie(
Id_Ucznia INT AUTO_INCREMENT PRIMARY KEY,
Nazwisko VARCHAR(40),
Imie VARCHAR(25),
Ulica VARCHAR(25)
);
CREATE TABLE TelefonyUczniow(
Id_Ucznia INT,
Telefon INT,
PRIMARY KEY(Id_Ucznia, Telefon)
);

5.CREATE USER 'DZ'@'localhost' IDENTIFIED BY 'your_password';


GRANT ALL PRIVILEGES ON Imie_Nazwisko.* TO 'DZ'@'localhost';


FLUSH PRIVILEGES;
6.
ALTER USER 'DZ'@'localhost' IDENTIFIED BY 'new_password';


FLUSH PRIVILEGES;
7.
CREATE USER 'D_Z'@'localhost' IDENTIFIED BY 'new_password';


GRANT ALL PRIVILEGES ON Imie_Nazwisko.* TO 'D_Z'@'localhost';


FLUSH PRIVILEGES;

8.
DROP USER 'D_Z'@'localhost';


FLUSH PRIVILEGES;

9.
CREATE USER 'Dawid_Zuzel'@'localhost' IDENTIFIED BY 'your_password';


GRANT ALL PRIVILEGES ON Imie_Nazwisko.* TO 'Dawid_Zuzel'@'localhost';


FLUSH PRIVILEGES;

10.
CREATE USER 'Dawid_Zuzel'@'localhost' IDENTIFIED BY 'your_password';
GRANT ALL PRIVILEGES ON Imie_Nazwisko.* TO 'Dawid_Zuzel'@'localhost';
FLUSH PRIVILEGES;

DROP USER 'DawidZuzel'@'localhost';
FLUSH PRIVILEGES;

11.
ALTER USER 'Dawid_Zuzel'@'localhost' IDENTIFIED BY 'Abc123!@#';
FLUSH PRIVILEGES;
12.
SHOW GRANTS FOR 'Dawid_Zuzel'@'localhost';

13.
GRANT SELECT ON Imie_Nazwisko.* TO 'Dawid_Zuzel'@'localhost';
FLUSH PRIVILEGES;

14.SELECT * FROM Uczniowie;

15.GRANT INSERT ON Imie_Nazwisko.Uczniowie TO 'Dawid_Zuzel'@'localhost';
FLUSH PRIVILEGES;

16.SHOW GRANTS FOR Dawid_Zuzel;
17.GRANT DELETE, UPDATE ON Imie_Nazwisko.TelefonyUczniow TO 'Dawid_Zuzel'@'localhost';
FLUSH PRIVILEGES;

19.GRANT CREATE ON Imie_Nazwisko.* TO 'Dawid_Zuzel'@'localhost';
FLUSH PRIVILEGES;

22.REVOKE DELETE ON Imie_Nazwisko.TelefonyUczniow FROM 'Dawid_Zuzel'@'localhost';
FLUSH PRIVILEGES;




