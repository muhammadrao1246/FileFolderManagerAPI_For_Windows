
# FileFolderManagerAPI_For_Windows
File Folder Manager API primarily Focused to assist c++ programmer in deal with File System Structure of Windows in the simplest way possible.  Built on Visual Studio 2012. A high performance API in C++ With Easy Debugging Facility.  

## Installtion Guidelines
The Both Files are the only files of this API.
You can use this API by just adding the Header File and CPP File in its respective project directory Like in
### In Visual Studio Project:

 1. Open the project that you have created as console application
 2. Then Just drag FileManager.cpp into "Source Files" visible directory inside project
 3. And then drag **FileManager.h** into "***Header Files***" visible directory inside project
 4. At Last Just Include the header inside your main cpp file as #include **FileManager.h**
 5. Now you're ready to go enjoy and for more information read the MD file.


## Documentation For Implementation
In this you just have to call the built-in static functions of the API to do the file handling.
### File Handling

 - **Creating A File:**
 ```c++
      std::string filename = "D:\example.txt\\";
			if ( FileManager::createFile(filename) ) 
			{
				std::cout << "Created file: " << filename << std::endl;
			}
```
 - **Writing To A File:**
```c++
      std::string filename = "D:\example.txt\\";
			if (FileManager::fileExists(filename)) 
			{
				std::cout << "Writing Into the File: \t" <<filename<< std::endl;
				std::vector<std::string> newLines ;
				newLines.push_back("Hello");
				newLines.push_back("world!");
				if (FileManager::writeLines(filename, newLines)) {
					std::cout << "Wrote new lines to file: " << filename << std::endl;
				}
			}
```
 - **Reading From A File:**
```c++  
      std::string filename = "D:\example.txt\\";
			if (FileManager::fileExists(filename)) 
			{
				std::cout << "Reading the File: \t" <<filename<< std::endl;
				std::vector<std::string> lines = FileManager::readLines(filename);
				for (const auto& line : lines) {
					std::cout << line << std::endl;
				}
			}
```
 - **Copying A File:**
```c++  
      std::string filename = "D:\example.txt\\";
			if (FileManager::fileExists(filename)) 
			{
				std::cout << "Copying the File: \t" <<filename<< std::endl;
				if (FileManager::copyFile(filename, "D:\\np\\")) 
				{
				std::cout << "File Copied: " << filename << std::endl;
				}
			}
```
			
### Folder Handling

 - **Creating A Folder:**
```c++
      std::string dir = "D:\\meetha\\";
			if (FileManager::createDirectory(dir))
			{
				std::cout << "Directory Created : "<<dir << std::endl;
			}
```
 - **Copying A Folder:**
```c++
		  std::string dir = "D:\\meetha\\";
			std::string source = "D:\\np\\";
			if( FileManager::copyDirectory(source,dir))
			{
				std::cout << "Directory D:\\np\\ Copied to: "<<dir << std::endl;
			}
```
 - **Deleting A Folder:**
 
```c++
		std::string dir = "D:\\meetha\\";
		if (FileManager::deleteDirectory(dir))
		{
			std::cout << "Directory Deleted : "<<dir << std::endl;
		}
```


 
            
> #### **Your Suggestions and Contributions will be highly appreciated!**

