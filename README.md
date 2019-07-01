# AppPreferences-Library
# Usage
To get a Git project into your build:

Step 1. Add the JitPack repository to your build file

Add jitpack in your root build.gradle at the end of repositories:

         allprojects {
	             repositories {
		            maven { url 'https://jitpack.io' }
	                           }
                      }
                      
                      
Step 2. Add the dependency

            dependencies {
                  implementation 'com.github.harishpadmanabh-HP:AppPreferences-Library:1.5'
                       }

Step 3 : Declare AppPrefernces.

            AppPreferences appPreferences;
            
Step 4 : Trigger an instance of AppPrefernces with context and appname string from resources inside your onCreate()

                    appPreferences = AppPreferences.getInstance(this, getResources().getString(R.string.app_name));
                    
Step 5 : Now you can use appPreferences methods to store and retrieve data in key - value pairs. 

                            String data = "Data to be stored ";
                            appPreferences.saveData("keynamefordata",data);//to store data.
                            appPreferences.getData("keynamefordata");
                            
In this way you can avoid usage of sharedPrefernces to store data . 
The main advantage of this library is that the stored data will not be lost even the app is killed .
You can store int,string and booleans values in appPreferences.
The methods for storing these values are listed below.

                           appPreferences.saveData("key","Testing app preferences"); //stores a string 
                           appPreferences.getData("key"); //retrieves  string in "key"
                           
                           appPreferences.saveInt("key",3201); //stores an int 
                           appPreferences.getInt("key"); //retrieves  int in "key"
                           
                           appPreferences.saveDataBoolean("key",true); //stores a boolean 
                           appPreferences.getDataBoolean("key"); //retrieves  boolean in "key"
                           
                           appPreferences.clearData(); // clear all data in    appPreferences.
                           
                           appPreferences.removeKey("key") //remove data in specified key
                           
                           
# Happy Coding !!!
                           
                           
                           
                           



