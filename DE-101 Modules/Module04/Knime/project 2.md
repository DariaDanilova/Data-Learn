
# Knime Workflow
This project is a transformation of Project 1. In the context of each country and each month of 1998, the number of orders made by citizens of these countries is calculated.

![image](https://user-images.githubusercontent.com/61746700/167297384-bbd0e031-7e24-401e-b073-4cd38003b293.png)

#
This part of the pipeline reads the data, converts the Freight column from the String type to the Number type, then deletes unnecessary columns and renames some columns in order to concatenate tables later.

![image](https://user-images.githubusercontent.com/61746700/167297311-57ca9d4d-7720-4cca-97be-27f75e4bbe8c.png)

After that, the lines with undelivered orders are deleted. Next, the data is combined with the Employees table and the Clients table. Then year and month are extracted from date, and only orders made in 1998 should be left.

![image](https://user-images.githubusercontent.com/61746700/167297319-200b9c78-1939-49b1-822e-22e6000c30e2.png)

Now the total number of orders is calculated for each country and for each month.  Missing values are replaced with 0. The result is written to an xlsx file.

![image](https://user-images.githubusercontent.com/61746700/167297321-c2dbadaf-38ff-4ec7-b79e-2037f1ee2d72.png)

The result looks like this.

![image](https://user-images.githubusercontent.com/61746700/167297331-301c148e-e313-4ec9-a0d5-9d8dae29d21d.png)
