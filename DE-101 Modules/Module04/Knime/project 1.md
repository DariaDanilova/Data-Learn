# Knime workflow
In this project, I will upload data from several sources: xlsx and csv files. And then I will calculate the total weight of orders in the context of each employee and each year by making a pivot table.

![image](https://user-images.githubusercontent.com/61746700/167296930-622017b0-bce1-4b08-800b-094eef283ecf.png)
##

This part of the pipeline reads the data, converts the Freight column from the String type to the Number type, then deletes unnecessary columns and renames some columns in order to concatenate tables later.

![image](https://user-images.githubusercontent.com/61746700/167296867-a06e535d-6bc9-4d1b-994c-0a3d0d4c71de.png)

After that, the lines with undelivered orders are deleted. Next, the data is combined with the Employees table. Then the year is extracted from the date, the order weight is converted into kilograms, and the columns with the customer's name and surname are combined into one.

![image](https://user-images.githubusercontent.com/61746700/167296874-13e252b4-93f2-490c-a4a1-4cd3650533e8.png)

Now the total weight of orders is calculated for each employee and for each year. The order of the columns is determined, and the values of the columns 1998 are sorted. The result is written to an xlsx file.

![image](https://user-images.githubusercontent.com/61746700/167296895-248626b5-2933-4dc4-b234-acd9311c0fdb.png)

The result looks like this.

![image](https://user-images.githubusercontent.com/61746700/167296898-595daff4-5fe7-4183-b3cc-2fd2c6677a3a.png)
