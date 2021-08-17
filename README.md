# SQL_prb
 import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="yourusername",
  password="yourpassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

#for creating Database


mycursor.execute("CREATE TABLE Customers
                 (CustomerName VARCHAR(255),
                 CustomerID int,
                 CutomerOpenDate int,
                 LastConsultedDate int,
                 VacclinationType VARCHAR(5),
                 DocterConsulted VARCHAR(255),
                 State VARCHAR(5),
                 Country VARCHAR(5),
                 PostCode int,
                 DateOfBirth int,
                 ActiveCutomer VARCHAR(1)
                  ")


INSERT INTO Customers (CustomerName, CustomerID, CutomerOpenDate, LastConsultedDate, VacclinationType, DocterConsulted,
                       State,Country,PostCode,DateOfBirth,ActiveCutomer)
VALUES ('Alex', '123457', '20101012', '20101013',' MVD', 'Paul', 'SA','USA','6031987','A')
VALUES ('John', '123458', '20101013', '20101013',' MVD', '  ', 'TN','IND','6031987','A')
VALUES ('Mathew', '123459', '20101013', '20101013',' MVD', '  ', 'WAS','PHIL','6031987','A')
VALUES ('Matt', '12345', '20101013', '20101013',' MVD', '  ', 'BOS','NYC','6031987','A')
VALUES ('Jacob', '1256', '20101013', '20101013',' MVD', '  ', 'VIC','AU','6031987','A')

#for Reading Database

SELECT * FROM Customers ;
                  

