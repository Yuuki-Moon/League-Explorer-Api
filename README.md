# League Explorer Api
**A C# .NET library for interacting with League Of Legends LCU and Web Api.**

## About this Project
This library is being developed alongside another project of mine and it's original goal was to provide the data I would need for said project. At some point I decided to make this a standalone library and release it separately, so here it is.

This library aims to interact both with the LCU League Api and the Riot's Web Api endpoints related to League of Legends.

The base code I started with and the inspiration for the came from <a href="https://github.com/Skinz3/League-of-Legends-Bot">Skinz3/League-of-Legends-Bot</a>.

### Features

  - Easy access to the LCU API to Control and Retrieve information from the League Client.
  - Live data from the current League match.
  - Direct acces to the Web API from a personal and production Key.
  - Automatic limits and manages the ammount of request to the Web Api per key type.


## Sample Usage
The library is used by instantiating the **LeagueExplorer** class from the **LeagueExplorerApi** Namespace:
```
LeagueExplorerApi.LeagueExplorer league = new LeagueExplorerApi.LeagueExplorer(
                    LeagueFolderPath: @"C:\Riot Games\League of Legends\",
                    WebApiEnable: false,
                    WebApiKey: "",
                    WebApiLicence: WebApiLicences.PERSONAL
                );
```
There are some parameters that should be passed to the constructor, more information about them and their default values are available in the <a href="https://github.com/Yuuki-Moon/League-Explorer-Api/wiki">Documentation/Wiki</a>.

From the LeagueExplorer Object, you have access to three separeate objects that give you access to diffents areas of the Api's. They are:
 - **Client** gives you access to the LCU methods related to the League Client and is only available when the Client is open.
 - **Game** gives you access to the LCU methods related to the Current League Match and is only available when the Game is open and a Match is currently in place.
 - **Web** gives you access to the Web Api methods is only available if **WebApiEnable** is set to **true** in the object constructor and an Api Key Is provided.


