# Docker Net7 Demo . net7 comes with new feature that you don't need a dockerfile anymore instead you can install Package and build your immage and run 
follow this steps

#Step One
Install Package using the following command

dotnet add package Microsoft.NET.Build.Containers

#step two 

Build your immage using the following command 

dotnet publish --os linux --arch x64 -p:publishProfile=DefaultContainer

your image will be built taking your projectname by default and version tag 1.0.0
eg. demoproject1.0.0

# step three

Run your Immage using comand

docker run --name yourcontainername -p 8085:80 -d yourimagename:1.0.0  

that is it!!
