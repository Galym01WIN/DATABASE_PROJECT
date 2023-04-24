# DATABASE_PROJECT

CREATE TABLE BOOK_SHOP(
BOOK_SHOP_ID NUMBER(1) PRIMARY KEY,
BOOK_SHOP_NAME VARCHAR(50),
BOOK_SHOP_ADDRESS VARCHAR(50),
BOOK_SHOP_PHONE VARCHAR(50) 
);

INSERT INTO BOOK_SHOP(BOOK_SHOP_ID,  BOOK_SHOP_NAME,  BOOK_SHOP_ADDRESS,  BOOK_SHOP_PHONE)
VALUES(1,'MIRO_BOOK_SHOP','ABAY-140','87076195677')

CREATE TABLE BOOKS_ASAN(
BOOK_ID NUMBER(1) PRIMARY KEY,
BOOK_TITLE VARCHAR(50),
BOOK_PRICE NUMBER(8),
BOOK_STATUS VARCHAR(50),
AUTHOR_ID NUMBER(1) REFERENCES AUTHOR(AUTHOR_ID),
PUBLISHER_ID NUMBER(1) REFERENCES PUBLISHER_AS(PUBLISHER_ID)
);

INSERT INTO BOOKS_ASAN(BOOK_ID, BOOK_TITLE, BOOK_PRICE, BOOK_STATUS, AUTHOR_ID, PUBLISHER_ID)
VALUES(1,'The Catcher in the Rye ',5000,'Available',1,2)

INSERT INTO BOOKS_ASAN(BOOK_ID, BOOK_TITLE, BOOK_PRICE, BOOK_STATUS, AUTHOR_ID, PUBLISHER_ID)
VALUES(2,'1984',3700,'Available',2,1)

INSERT INTO BOOKS_ASAN(BOOK_ID, BOOK_TITLE, BOOK_PRICE, BOOK_STATUS, AUTHOR_ID, PUBLISHER_ID )
VALUES(3,'To Kill a Mockingbird',4500,'Available',3,3)

INSERT INTO BOOKS_ASAN(BOOK_ID, BOOK_TITLE, BOOK_PRICE, BOOK_STATUS, AUTHOR_ID, PUBLISHER_ID )
VALUES(4,'The Great Gatsby',2800,'Damaged',4,1)

INSERT INTO BOOKS_ASAN(BOOK_ID, BOOK_TITLE, BOOK_PRICE, BOOK_STATUS, AUTHOR_ID, PUBLISHER_ID )
VALUES(5,'Pride and Prejudice',3600,'Available',5,3)

INSERT INTO BOOKS_ASAN(BOOK_ID, BOOK_TITLE, BOOK_PRICE, BOOK_STATUS, AUTHOR_ID, PUBLISHER_ID)
VALUES(6,'Crime and Punishment',6200,'Available',6,1)

INSERT INTO BOOKS_ASAN(BOOK_ID, BOOK_TITLE, BOOK_PRICE, BOOK_STATUS, AUTHOR_ID, PUBLISHER_ID )
VALUES(7,'The Hobbit',4800,'Available',7,2)


CREATE TABLE AUTHOR(
AUTHOR_ID NUMBER(1) PRIMARY KEY,
AUTHOR_NAME VARCHAR(50),
AUTHOR_SUBJECT VARCHAR(50)
);

INSERT INTO AUTHOR(AUTHOR_ID,AUTHOR_NAME,AUTHOR_SUBJECT)
VALUES(1,'J.D. Salinger','Psychology')

INSERT INTO AUTHOR(AUTHOR_ID,AUTHOR_NAME,AUTHOR_SUBJECT)
VALUES(2,'George Orwell','Literature')

INSERT INTO AUTHOR(AUTHOR_ID,AUTHOR_NAME,AUTHOR_SUBJECT)
VALUES(3,'Harper Lee','Literature')

INSERT INTO AUTHOR(AUTHOR_ID,AUTHOR_NAME,AUTHOR_SUBJECT)
VALUES(4,'F. Scott Fitzgerald','Psychology')

INSERT INTO AUTHOR(AUTHOR_ID,AUTHOR_NAME,AUTHOR_SUBJECT)
VALUES(5,'Jane Austen','Literature')

INSERT INTO AUTHOR(AUTHOR_ID,AUTHOR_NAME,AUTHOR_SUBJECT)
VALUES(6,'Fyodor Dostoevsky','Literature')

INSERT INTO AUTHOR(AUTHOR_ID,AUTHOR_NAME,AUTHOR_SUBJECT)
VALUES(7,'J.R.R. Tolkien','Psychology')

CREATE TABLE PUBLISHER_AS(
PUBLISHER_ID NUMBER(1) PRIMARY KEY,
PUBLISHER_NAME VARCHAR(50),
PUBLISHER_PHONE VARCHAR(50)
CONSTRAINT phone_check CHECK (LENGTH(PUBLISHER_PHONE) = 11)
);

INSERT INTO PUBLISHER_AS(PUBLISHER_ID, PUBLISHER_NAME, PUBLISHER_PHONE)
VALUES(1,'Atamura','87074767894')

INSERT INTO PUBLISHER_AS(PUBLISHER_ID, PUBLISHER_NAME, PUBLISHER_PHONE)
VALUES(2,'Almaty','87077847921')

INSERT INTO PUBLISHER_AS(PUBLISHER_ID, PUBLISHER_NAME, PUBLISHER_PHONE)
VALUES(3,'Daik-Press','87077867121')


CREATE TABLE EMPLOYEE_A(
EMPLOYEE_ID NUMBER(1) PRIMARY KEY,
EMPLOYEE_NAME VARCHAR(50),
EMPLOYEE_EMAIL VARCHAR(51),
EMPLOYEE_PASSWORD VARCHAR(50),
EMPLOYEE_SALARY NUMBER(8)
);

INSERT INTO EMPLOYEE_A (EMPLOYEE_ID, EMPLOYEE_NAME, EMPLOYEE_EMAIL, EMPLOYEE_PASSWORD, EMPLOYEE_SALARY)
VALUES(1, 'John Smith', 'johnsmith@example.com', 'password123', 50000)

INSERT INTO EMPLOYEE_A (EMPLOYEE_ID, EMPLOYEE_NAME, EMPLOYEE_EMAIL, EMPLOYEE_PASSWORD, EMPLOYEE_SALARY)
VALUES(2, 'Jane Doe', 'janedoe@example.com', 'password456', 60000)

INSERT INTO EMPLOYEE_A (EMPLOYEE_ID, EMPLOYEE_NAME, EMPLOYEE_EMAIL, EMPLOYEE_PASSWORD, EMPLOYEE_SALARY)
VALUES(3, 'Bob Johnson', 'bjohnson@example.com', 'password789', 55000)

INSERT INTO EMPLOYEE_A (EMPLOYEE_ID, EMPLOYEE_NAME, EMPLOYEE_EMAIL, EMPLOYEE_PASSWORD, EMPLOYEE_SALARY)
VALUES(4, 'Sarah Lee', 'sarahlee@example.com', 'passwordabc', 65000)

INSERT INTO EMPLOYEE_A (EMPLOYEE_ID, EMPLOYEE_NAME, EMPLOYEE_EMAIL, EMPLOYEE_PASSWORD, EMPLOYEE_SALARY)
VALUES(5, 'David Kim', 'davidkim@example.com', 'passworddef', 70000)

INSERT INTO EMPLOYEE_A (EMPLOYEE_ID, EMPLOYEE_NAME, EMPLOYEE_EMAIL, EMPLOYEE_PASSWORD, EMPLOYEE_SALARY)
VALUES(6, 'Karen Wong', 'kwong@example.com', 'passwordghi', 75000)

galym, [24.04.2023 20:15]
galym, [24.04.2023 17:18]
INSERT INTO EMPLOYEE_A (EMPLOYEE_ID, EMPLOYEE_NAME, EMPLOYEE_EMAIL, EMPLOYEE_PASSWORD, EMPLOYEE_SALARY)
VALUES(7, 'Tom Baker', 'tbaker@example.com', 'passwordjkl', 80000)

INSERT INTO EMPLOYEE_A (EMPLOYEE_ID, EMPLOYEE_NAME, EMPLOYEE_EMAIL, EMPLOYEE_PASSWORD, EMPLOYEE_SALARY)
VALUES(8, 'Emily Chen', 'echen@example.com', 'passwordmno', 85000)

INSERT INTO EMPLOYEE_A (EMPLOYEE_ID, EMPLOYEE_NAME, EMPLOYEE_EMAIL, EMPLOYEE_PASSWORD, EMPLOYEE_SALARY)
VALUES(9, 'Mark Davis', 'mdavis@example.com', 'passwordpqr', 90000)


CREATE TABLE CLIENT_AS(
CLIENT_ID NUMBER(20) PRIMARY KEY,
CLIENT_NAME VARCHAR(50),
CLIENT_ADDRESS VARCHAR(50),
CLIENT_PHONE VARCHAR(50)
);

INSERT INTO CLIENT_AS(CLIENT_ID, CLIENT_NAME, CLIENT_ADDRESS, CLIENT_PHONE) 
VALUES(1001,'Sabina','Kyzylorda','87074567891')

INSERT INTO CLIENT_AS(CLIENT_ID, CLIENT_NAME, CLIENT_ADDRESS, CLIENT_PHONE) 
VALUES(1002, 'Nursultan', 'Almaty', '89876543210')

INSERT INTO CLIENT_AS(CLIENT_ID, CLIENT_NAME, CLIENT_ADDRESS, CLIENT_PHONE)
VALUES(1003, 'Amina', 'Aktau', '89216745328')

INSERT INTO CLIENT_AS(CLIENT_ID, CLIENT_NAME, CLIENT_ADDRESS, CLIENT_PHONE) 
VALUES(1004, 'Temirlan', 'Karaganda', '89891234567')

INSERT INTO CLIENT_AS(CLIENT_ID, CLIENT_NAME, CLIENT_ADDRESS, CLIENT_PHONE) 
VALUES(1005, 'Aizere', 'Shymkent', '89357902134')

INSERT INTO CLIENT_AS(CLIENT_ID, CLIENT_NAME, CLIENT_ADDRESS, CLIENT_PHONE) 
VALUES(1006, 'Daniyar', 'Aktobe', '87075634129')

INSERT INTO CLIENT_AS(CLIENT_ID, CLIENT_NAME, CLIENT_ADDRESS, CLIENT_PHONE)
VALUES(1007, 'Ayaz', 'Kostanay', '87772107890')

INSERT INTO CLIENT_AS(CLIENT_ID, CLIENT_NAME, CLIENT_ADDRESS, CLIENT_PHONE)
VALUES(1008, 'Gulmira', 'Taraz', '87078765432')

INSERT INTO CLIENT_AS(CLIENT_ID, CLIENT_NAME, CLIENT_ADDRESS, CLIENT_PHONE)
VALUES(1009, 'Zhanar', 'Atyrau', '89123456789')

INSERT INTO CLIENT_AS(CLIENT_ID, CLIENT_NAME, CLIENT_ADDRESS, CLIENT_PHONE)
VALUES(1010, 'Talgat', 'Pavlodar', '89678901234')

CREATE TABLE ORDER_AS(
ORDER_ID NUMBER(1) PRIMARY KEY,
CLIENT_ID NUMBER(20) REFERENCES CLIENT_AS(CLIENT_ID),
EMPLOYEE_ID NUMBER(20) REFERENCES EMPLOYEE_A(EMPLOYEE_ID),
ORDER_TOTAL NUMBER(8),
ORDER_DATE VARCHAR(50),
ORDER_ADDRESS VARCHAR(50)
);

INSERT INTO ORDER_AS(ORDER_ID, CLIENT_ID, EMPLOYEE_ID, ORDER_TOTAL, ORDER_DATE, ORDER_ADDRESS)
VALUES(1,1001,1,4000,'APRIL-2','ABAY-145')

INSERT INTO ORDER_AS(ORDER_ID, CLIENT_ID, EMPLOYEE_ID, ORDER_TOTAL, ORDER_DATE, ORDER_ADDRESS)
VALUES(2,1002,2,2000,'APRIL-12','ABAY-105')

INSERT INTO ORDER_AS(ORDER_ID, CLIENT_ID, EMPLOYEE_ID, ORDER_TOTAL, ORDER_DATE, ORDER_ADDRESS)
VALUES(3,1003,3,1500,'MAY-2','SAKEN-115')

INSERT INTO ORDER_AS(ORDER_ID, CLIENT_ID, EMPLOYEE_ID, ORDER_TOTAL, ORDER_DATE, ORDER_ADDRESS)
VALUES(4,1004,4,6200,'DECEMBER-13','WEST-115')

INSERT INTO ORDER_AS(ORDER_ID, CLIENT_ID, EMPLOYEE_ID, ORDER_TOTAL, ORDER_DATE, ORDER_ADDRESS)
VALUES(5,1005,5,5000,'MAY-5','MERU-145')

INSERT INTO ORDER_AS(ORDER_ID, CLIENT_ID, EMPLOYEE_ID, ORDER_TOTAL, ORDER_DATE, ORDER_ADDRESS)
VALUES(6,1006,5,6500,'JUNE-6','GALA-146')

INSERT INTO ORDER_AS(ORDER_ID, CLIENT_ID, EMPLOYEE_ID, ORDER_TOTAL, ORDER_DATE, ORDER_ADDRESS)
VALUES(7,1007,7,7600,'JULY-7','SABA-147')

INSERT INTO ORDER_AS(ORDER_ID, CLIENT_ID, EMPLOYEE_ID, ORDER_TOTAL, ORDER_DATE, ORDER_ADDRESS)
VALUES(8,1008,8,8200,'AUGUST-8','DONY-148')

INSERT INTO ORDER_AS(ORDER_ID, CLIENT_ID, EMPLOYEE_ID, ORDER_TOTAL, ORDER_DATE, ORDER_ADDRESS)
VALUES(9,1009,9,9800,'SEPTEMBER-9','ALAN-148')

CREATE TABLE PAYMENT_AS(
PAYMENT_ID NUMBER(1) PRIMARY KEY,
PAYMENT_METHOD VARCHAR(50),
CONSTRAINT METHOD_CHECK CHECK (PAYMENT_METHOD IN ('CASH' , 'CARD'))
);

INSERT INTO PAYMENT_AS(PAYMENT_ID, PAYMENT_METHOD)
VALUES(1,'CASH')

INSERT INTO PAYMENT_AS(PAYMENT_ID, PAYMENT_METHOD)
VALUES(2,'CARD')

INSERT INTO PAYMENT_AS(PAYMENT_ID, PAYMENT_METHOD)
VALUES(3,'CARD')

INSERT INTO PAYMENT_AS(PAYMENT_ID, PAYMENT_METHOD)
VALUES(4,'CASH')


CREATE TABLE CASH_PAYMENTSA(
CASH_PAYMENT_ID NUMBER(2),
PAYMENT_ID NUMBER(1) REFERENCES PAYMENT_AS(PAYMENT_ID),
CASH_AMOUNT NUMBER(10),
CASH_CHANGE_GIVEN NUMBER(10),
PRIMARY KEY(CASH_PAYMENT_ID)
);

galym, [24.04.2023 20:15]
INSERT INTO CASH_PAYMENTSA(CASH_PAYMENT_ID,PAYMENT_ID, CASH_AMOUNT, CASH_CHANGE_GIVEN) VALUES(10,1, 500, 100)
INSERT INTO CASH_PAYMENTSA(CASH_PAYMENT_ID,PAYMENT_ID, CASH_AMOUNT, CASH_CHANGE_GIVEN) VALUES(11,4, 780, 230)


CREATE TABLE CARD_PAYMENTS(
CASH_PAYMENT_ID NUMBER(2),
PAYMENT_ID NUMBER(1) REFERENCES PAYMENT_AS(PAYMENT_ID),
CARD_NAME VARCHAR(10),
CARD_NUMBER NUMBER(30),
CARD_EXPIRES VARCHAR(30),
CARD_AMOUNT NUMBER(10),
CARD_CVV NUMBER(4),
PRIMARY KEY(CASH_PAYMENT_ID)
); 


INSERT INTO CARD_PAYMENTS(CASH_PAYMENT_ID, PAYMENT_ID, CARD_NAME, CARD_NUMBER, CARD_EXPIRES, CARD_AMOUNT, CARD_CVV)
VALUES (21,2,'John Smith', 1234567890123456, '12/25', 100.00, 123)

INSERT INTO CARD_PAYMENTS(CASH_PAYMENT_ID, PAYMENT_ID, CARD_NAME, CARD_NUMBER, CARD_EXPIRES, CARD_AMOUNT, CARD_CVV)
VALUES (22,3,'Jane Doe', 9876543210987654, '06/24', 50.00, 456)






CREATE OR REPLACE PROCEDURE UPDATE_BOOK_PRICE(BOOK_STATUS IN VARCHAR2, BOOK_PRICE IN NUMBER) AS 
  ROWS_UPDATED NUMBER;
BEGIN 
  UPDATE BOOKS_ASAN SET PRICE = BOOK_PRICE WHERE BOOK_STATUS = BOOK_STATUS;
  ROWS_UPDATED:= SQL%ROWCOUNT;
  DBMS_OUTPUT.PUT_LINE('Number of rows updated: '|| ROWS_UPDATED);
EXCEPTION
  WHEN OTHERS THEN
    DBMS_OUTPUT.PUT_LINE('Error occurred: ' || SQLERRM);
END;


CREATE OR REPLACE TRIGGER COUNT_CARD_PAYMENT_AMOUNT
BEFORE INSERT ON CARD_PAYMENTS
FOR EACH ROW
DECLARE
  COUNT_CARD_PAYMENT_AMOUNT NUMBER;
BEGIN
  SELECT COUNT(*) INTO client_order_amount FROM order WHERE CASH_PAYMENT_ID_id = :new.CASH_PAYMENT_ID;
  DBMS_OUTPUT.PUT_LINE('Current number of orders from  '  :new.CASH_PAYMENT_ID  ' is : ' || COUNT_CARD_PAYMENT_AMOUNT);
END;
