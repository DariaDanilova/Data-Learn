# Transformation: split data into different file formats

Let's split the data into different formats.
* save the product information in JSON format.
* information about refunds save in XML format.
* Information about orders will be divided by region.
  * CENTRAL – 1 file in xls format
  * WEST – several files divided by state in csv format
  * SOUTH - 1 file in csv format in a zip archive
  * EAST - a text file with the .dat extension

## Product information in JSON format

Use *Text file input* step to read csv file. Don’t forget to press *Get fields* on the *Fields* tab.

![image](https://user-images.githubusercontent.com/61746700/166297527-2203155a-2893-4cd4-a384-433491309ecd.png)

![image](https://user-images.githubusercontent.com/61746700/166297540-88c50317-81bb-408a-aa4d-71a3864fc34c.png)

Before saving to JSON, let’s remove duplicate rows using *Sort rows* step.

![image](https://user-images.githubusercontent.com/61746700/166297573-a0f614a5-953e-4b6e-8c2c-8490ac6f3b1b.png)

On JSON output step choose path, where result will be saved and check the box *Create Parent folder* to create folder product if it will not exist.
Put 10000 in the *Nr rows in a block* field so that all records are in one file, and not in several different ones.

![image](https://user-images.githubusercontent.com/61746700/166297678-6422a0d0-b0d6-401b-8463-ee029ae29d0e.png)

Select the fields to be written to the output file.

![image](https://user-images.githubusercontent.com/61746700/166297709-90529958-43e7-40af-b743-fb16f9e4d71d.png)

Run the transformation. File is created.

![image](https://user-images.githubusercontent.com/61746700/166297761-7bf4075b-9eb5-481c-a7af-979f6b66a819.png)

![image](https://user-images.githubusercontent.com/61746700/166297772-2823cd47-f1a8-4d2a-b43e-cd0baad5b218.png)

## Refunds information in XML format

Now add necessary steps.

![image](https://user-images.githubusercontent.com/61746700/166297843-ef497264-01d9-4270-9e7d-56b75351e2ee.png)

*Sort rows* to remove duplicates.

![image](https://user-images.githubusercontent.com/61746700/166297861-d0fd6b33-04bc-46ab-8c5e-cdde60e7d70a.png)

*Filter rows* to leave rows for which there would be a return.

![image](https://user-images.githubusercontent.com/61746700/166297929-925ce045-0137-4b7d-9ba8-f0ce96baf025.png)

On *XML output* step choose path, where result will be saved. There is no way to create a folder in advance. So it will be done in the job.

![image](https://user-images.githubusercontent.com/61746700/166297976-311059a5-e68c-4bfe-974a-5a1bfc362c14.png)

Leave two fields for output.

![image](https://user-images.githubusercontent.com/61746700/166298002-319576d1-45bb-4acd-a34b-cbe42f7bc78c.png)

Run transformation.

![image](https://user-images.githubusercontent.com/61746700/166298027-83e20cb3-351e-478f-920d-51c1aeb2caaa.png)

Check the results.

![image](https://user-images.githubusercontent.com/61746700/166298041-e9e4e956-6011-4b26-a16a-df11737a7c40.png)

![image](https://user-images.githubusercontent.com/61746700/166298054-931a0220-47b0-4838-a74b-fdce680f98e8.png)

## Divide orders information by region

The necessary steps have been added.

![image](https://user-images.githubusercontent.com/61746700/166298135-f6f12d92-5feb-401c-a99b-a8c74726925a.png)

Filter rows to leave only with the CENTRAL region.

![image](https://user-images.githubusercontent.com/61746700/166298157-64d3fa21-2e7f-42b2-8c29-359c793f27b6.png)

Define path to save results and select fields.

![image](https://user-images.githubusercontent.com/61746700/166298193-b5db41e6-110f-49f9-a9bb-aa55e530331c.png)

![image](https://user-images.githubusercontent.com/61746700/166298203-0429181f-a899-4e42-ba7e-6c3f5bb85214.png)

Run transformation. The central_orders.xls has been created.

![image](https://user-images.githubusercontent.com/61746700/166298230-1e978250-4d0e-41c1-9cbe-6932ffa84df4.png)

Now do for South region. Choose *Filter rows* step and *Text file output* step.

![image](https://user-images.githubusercontent.com/61746700/166298282-b05004d7-ad26-46b6-975f-bf91cbf770a9.png)

Set the value to South.

![image](https://user-images.githubusercontent.com/61746700/166298299-06c93cb6-f91d-4e0b-8034-935bec94d033.png)

Define path and extension.

![image](https://user-images.githubusercontent.com/61746700/166298316-7765bd14-3e15-4f08-829a-d642b4c438b2.png)

Select zip in the compression field.

![image](https://user-images.githubusercontent.com/61746700/166298342-8fb41c41-0a9c-4b64-ba9e-ea57ca944a10.png)

Select fields.

![image](https://user-images.githubusercontent.com/61746700/166298363-6c13064e-c348-42bb-9d65-d9485bad66b3.png)

Check the results.

![image](https://user-images.githubusercontent.com/61746700/166298399-0cc92489-9f36-4645-a6fb-34c4bca0588b.png)

For East region everything looks almost the same.

![image](https://user-images.githubusercontent.com/61746700/166298482-c2079318-bdba-4f23-b3c7-65a2c025fba6.png)

![image](https://user-images.githubusercontent.com/61746700/166298502-ab250d7b-82ea-4805-81e4-659396719fee.png)

![image](https://user-images.githubusercontent.com/61746700/166298513-cf641587-6501-4560-876a-257135777d83.png)

![image](https://user-images.githubusercontent.com/61746700/166298548-55487ffe-d146-43f3-969d-733ba076bc38.png)

The last region is West.
For Arizona, fill in the fields as follows.

![image](https://user-images.githubusercontent.com/61746700/166298585-5b0c581e-215e-467c-a672-51d26e3032a8.png)

![image](https://user-images.githubusercontent.com/61746700/166298592-37de98b6-f568-4c61-a424-2357924c51d3.png)

For the rest, do the same.

Run the transformation.

![image](https://user-images.githubusercontent.com/61746700/166298638-15633a1d-d0b1-436c-92a8-98b66724862b.png)

Check the results in the west folder.

![image](https://user-images.githubusercontent.com/61746700/166298670-bc4c0ecb-20a7-4ec8-a8ee-27f1b68e0217.png)



