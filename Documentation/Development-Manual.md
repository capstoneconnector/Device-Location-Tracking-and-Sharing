# Development Manual
## Tech Aspects
- The project is coded in Java for Android using Android Studio.
- It uses four key "services":
  - Google Sign-In
    - Used to allow the user to sign in with Google
  - Firebase
    - Handles Google Sign-In results and authentication
  - Microsoft Azure
    - Our database and GeoJSON service
  - Google Maps
    - Used to track user location during tracks
## Replication
- Software Requirements
  - Java Development Kit
  - Android Studio
- The project code is located on the DeviceLocationTrackingSharing-NBC repository linked in the README file of this repository.
- The code can be accessed through any of the following four methods, ordered by (subjective) convenience:
  - Copy the repository url into a third-party git client (eg: GitKraken, Sourcetree, GitHub Desktop) and open the project in Android Studio
  - In Android Studio, select the "VCS" tab, click on "Checkout from version control", and select "git". Paste the url for the repository.
  - In terminal, provided git is installed on your machine, type "git clone X" where X is the repository url.
  - Download the ZIP from the repository's main page and open it in Android Studio. (Not recommended for production, mostly for local testing)
## Folder structure
- Aside from the default Android project folder layout (manifests, java, res folders) the .java files are separated into four packages:
  - activities
    - All of the activities, or pages, of the project are listed here. This package contains most of the source code and the vast majority of the functionality.
  - adapters
    - This package contains the AzureServiceAdapter for accessing the Azure blob GeoJSON data, as well as Group and Person adapters for the RecyclerViews
  - interfaces
    - This package contains the interfaces for dealing with the responses from database calls
  - models
    - This package contains model classes for all of the database tables
## Important files
- Keys for the four services (listed above) should be received from the maintainer and added to LoginActivity (Google Sign-In), MapsActivity and PreviousToursActivity (Azure), and google_maps_api.xml (Google Maps)
## Future Improvements
- Will be updated over time
