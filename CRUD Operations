

/*   03   CRUD  OPERATIONS   */

/* ADDING NEW PRODUCT*/
/*  Query */				
Insert Into Product
values
('JBL CHARGE MINI 3+ BLUETOOTH SPEAKER','6',1500,800),
('Mi Power Bank 2 10000Mah with 2USB  (Black)','7',5000,1000);

/*PROCEDURE*/
	CREATE PROCEDURE INSERTPRODUCT
  @Value1 varchar,
  @Value2 int,
  @Value3 int,
  @Value4 int
AS
BEGIN
  INSERT INTO Product(ProductName, CategoryID,Price,Stock_quantity)
  VALUES (@Value1, @Value2, @Value3,@Value4);
END;

EXEC INSERTPRODUCT 'JBL 3+ BLUETOOTH SPEAKER','6',1200,500;
EXEC INSERTPRODUCT 'Mi Power Bank 30000Mah with 2USB  (Black)','7',15000,800;






/* UPDATING PRODUCT DETAILS */
/*  Query */	
update Product set price=3500,stock_quantity=40 where productid=12;
update product set price=1500,stock_quantity=0 where productid=13;
/*PROCEDURE*/
CREATE PROCEDURE UpdateProduct
  @SearchValue int,
  @NewValue1 int,
  @NewValue2 int
AS
BEGIN
  UPDATE Product
  SET Price = @NewValue1,
      Stock_quantity = @NewValue2
  WHERE ProductID = @SearchValue;
END;

EXEC UpdateProduct '17', '2500', '1200';


					/* Viewing customer detals */
/*METHOD 1 QUERY*/
select customerid,firstname,lastname,email,Contact,Email, DOB from customer;
/*METHOD 2 VIEW */
CREATE VIEW CustomerDetails
AS
SELECT customerid,firstname,lastname,Contact,Email, DOB
FROM  customer;

Select * from CustomerDetails;


/* DELETEING  ORDERS */

CREATE PROCEDURE DeleteOrder
  @SearchValue int
AS
BEGIN
  DELETE FROM OrderedProduct
  WHERE ProductID = @SearchValue;
END;

EXEC DeleteOrder 7;
