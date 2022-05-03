## Final Job

Now let's create a final job that will run all previously created tasks.

![image](https://user-images.githubusercontent.com/61746700/166462334-3a16371e-40d4-4059-bcf0-0d0945623af0.png)

Create variables using *Set variables* step with paths to which scripts and files will be saved. 

![image](https://user-images.githubusercontent.com/61746700/166462361-fe25be6b-1127-44e9-a9eb-872046bb5f23.png)

*Download dataset* job uses job which downloads csv file from github.

![image](https://user-images.githubusercontent.com/61746700/166462423-e6e244dd-6d07-4bf5-8a33-f5c3ca7512e5.png)

Checking whether the file was downloaded successfully.

![image](https://user-images.githubusercontent.com/61746700/166462447-1c012f67-3141-4af2-9592-cd795539b7f2.png)

Do a transformation to merge Orders, Returns and People tables.

![image](https://user-images.githubusercontent.com/61746700/166462473-80a77fdb-5093-459d-be5a-fee986bf57c5.png)

*Create a folder* step creates *returns* folder because *XML output* step does not allow to do this.

![image](https://user-images.githubusercontent.com/61746700/166462531-df6e86de-634a-4c1e-bfa5-26c2deb52551.png)

*Save to files* executes transformation which saves data to different file formats.

![image](https://user-images.githubusercontent.com/61746700/166462593-a70aadad-3341-4d7c-91c7-a04903f9b2d6.png)
