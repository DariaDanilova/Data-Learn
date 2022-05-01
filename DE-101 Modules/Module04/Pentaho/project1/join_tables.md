## Transformation: join 3 tables into 1

Choose *Microsoft Excel input* step.

![image](https://user-images.githubusercontent.com/61746700/166154512-50c460a9-1925-4aee-a618-d13a73aa0234.png)

In the *File or directory* field write path to the xls file and press *Add*.

![image](https://user-images.githubusercontent.com/61746700/166154530-f257a045-2101-4c83-a7ba-1994dd65dc7a.png)

In the *!Sheet* tab, select the *Orders* table.

![image](https://user-images.githubusercontent.com/61746700/166154579-f49d064f-cc57-41d3-b2c5-b49c8078d63f.png)

In the *Fields* tab, select the required fields and make changes if necessary.

![image](https://user-images.githubusercontent.com/61746700/166154588-23084185-6512-4420-b9b6-0728ce5fbd67.png)

Since it is needed to combine data from three sheets, you need three components.

![image](https://user-images.githubusercontent.com/61746700/166154596-b8a3db6f-ed2e-43dc-b680-9ad4d00030ce.png)

![image](https://user-images.githubusercontent.com/61746700/166154599-f1374ea5-e116-49e7-9db2-4b1c1d3104e7.png)

![image](https://user-images.githubusercontent.com/61746700/166154605-7a9d58b3-4960-438a-9f4a-50af88a3a03b.png)

![image](https://user-images.githubusercontent.com/61746700/166154611-448fa16f-1de5-49b9-962c-578e5df88ba8.png)

![image](https://user-images.githubusercontent.com/61746700/166154616-ef6211d7-c888-4a79-9ef2-0964d94ade81.png)

Now we need to join this data. The *Merge join* will be used. But before performing joining, PDI requires sorting ascending the fields by which tables will be joining.

![image](https://user-images.githubusercontent.com/61746700/166154644-464d2e28-7168-4529-b137-a849762b2b48.png)

Choose *Sort rows*, rename it and choose fields by which to join.

![image](https://user-images.githubusercontent.com/61746700/166154656-83e72aeb-8efd-4efb-8227-7baad3ff0ff4.png)

Check the box *Only pass unique rows*, since there are duplicate rows in the *Returns* table.

![image](https://user-images.githubusercontent.com/61746700/166154673-c41fb365-fa2b-48f7-a067-80d897d01d55.png)

Define the necessary fields and the type of join.

![image](https://user-images.githubusercontent.com/61746700/166154678-a1adb4a0-cb0c-4caa-bf0a-2b33ed5cde34.png)

Make the same for *People* table.

![image](https://user-images.githubusercontent.com/61746700/166154704-3a24f6f7-4537-4cb5-9c24-9b267b097613.png)

![image](https://user-images.githubusercontent.com/61746700/166154708-6cd412b3-557b-4b0d-8b4d-6b64eeefdbd7.png)

And sort the result of *Orders* and *Returns* joining.

![image](https://user-images.githubusercontent.com/61746700/166154718-1d9ceaf2-db76-4e0b-95ca-f2bdb3da3a17.png)

![image](https://user-images.githubusercontent.com/61746700/166154730-a02aecf8-0a1d-40a9-9b8d-1b2f004bbd07.png)

Now the transformation looks like this.

![image](https://user-images.githubusercontent.com/61746700/166154739-154c997d-ffef-49f5-989d-22d5ee49f698.png)

Define fields for second left join.

![image](https://user-images.githubusercontent.com/61746700/166154745-4f4849f1-5ecf-4d18-a6c5-c676e38d1c89.png)

Run the transformation. Everything looks fine.

![image](https://user-images.githubusercontent.com/61746700/166154764-cc49f0a4-5f83-4f24-9b15-efd49f998750.png)

But let’s delete some repeated columns.

![image](https://user-images.githubusercontent.com/61746700/166154768-af54f327-9756-432e-8dd0-fd56a1c6be90.png)

For this use *Select values* step. In the *Remove* tab choose columns to delete.

![image](https://user-images.githubusercontent.com/61746700/166154779-fcab9b1c-f484-49bb-bc00-9b53bdd883da.png)

![image](https://user-images.githubusercontent.com/61746700/166154784-2bf7ae21-844e-448b-8bed-de955c4838d5.png)

The last step is to save the results into csv file (use *Text file output*).

![image](https://user-images.githubusercontent.com/61746700/166154796-27a76343-95cc-4167-847e-b307169341dc.png)

Fill the *Filename* field and choose the extension.

![image](https://user-images.githubusercontent.com/61746700/166154802-bc01d245-0eea-4afa-93fc-2be82eea0629.png)

The file is created.

![image](https://user-images.githubusercontent.com/61746700/166154806-9109f67d-ad49-4224-951a-5f320bb6754d.png)

![image](https://user-images.githubusercontent.com/61746700/166154807-3f52f787-477e-4101-a142-86c22da6393a.png)


