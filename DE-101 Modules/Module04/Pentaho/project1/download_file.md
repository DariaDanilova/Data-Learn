## Job to download a file

Create a 'temp' folder and a 'work' folder.
Save the paths in temporary variables.
* HOME – the path to the folder where the files we are working with are located.
* WORKFOLDER - the path to the folder where transformations, jobs and scripts are located.

![image](https://user-images.githubusercontent.com/61746700/166154055-fa400919-50d6-4346-8333-c498502bfad5.png)

Let's create a job that downloads a file from the github and saves it on the computer.

![image](https://user-images.githubusercontent.com/61746700/166154064-28d9bf57-229f-4a9d-bc12-7cf1812981d6.png)

There are two options for downloading – via HTTP step and via shell script.

### Via HTTP

Drag the Start and HTTP steps on the canvas.

![image](https://user-images.githubusercontent.com/61746700/166154097-d4b85ee9-d373-4231-bace-052c0d08dfd6.png)

Click on HTTP, and enter a link to the file to download in the *URL* field. In the *Target file* field, enter the location where to save the downloaded file.

![image](https://user-images.githubusercontent.com/61746700/166154182-bd2abdb2-63ec-47ef-bee2-759b8aa2218b.png)

Connect the steps via hop.

![image](https://user-images.githubusercontent.com/61746700/166154192-a039a9ba-70b9-4c59-b66f-a169916d17c2.png)
 
Save the job.

![image](https://user-images.githubusercontent.com/61746700/166154199-eadb8375-99e0-46c2-84e9-573bbcb84473.png)

Execute it.

![image](https://user-images.githubusercontent.com/61746700/166154207-68f15643-4ee8-41a5-95a9-8f7423074f03.png)

Check - the file is downloaded.

![image](https://user-images.githubusercontent.com/61746700/166154211-92c8e857-dff2-4a75-8b91-4a4326814bff.png)

### Via shell script

Script content:
```
curl -O D:/temp/superstore_shell.xls https://github.com/Data-Learn/data-engineering/raw/master/DE-101%20Modules/Module01/DE%20-%20101%20Lab%201.1/Sample%20-%20Superstore.xls
```
Drag the Shell step into the workspace.
 
![image](https://user-images.githubusercontent.com/61746700/166154228-cb013c4a-f24b-4524-a2ab-9849f85c0794.png)

Click on Shell and enter the path where the script lies in the *Script file name* field.

![image](https://user-images.githubusercontent.com/61746700/166154240-100f5d15-cd22-4c69-9f48-8412cd18d3c1.png)

Connect the steps, and run the job.

![image](https://user-images.githubusercontent.com/61746700/166154250-663300c6-135b-4dfc-9126-b5f7e83aa33d.png)
