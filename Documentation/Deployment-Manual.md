# Deployment Manual
## Resources
- Azure
  - Permissions to be passed on directly
  - Resource Group: Capstone
    - Storage Account: brstrayer
      - Used for blob storage, GeoJSON data located in container "geojson"
      - Keys located in Settings -> Access keys
    - App Service: dltas
      - Communicates with the actual app
      - Tables located in "Easy Tables" in menu
      - Any changes to schema should be done in here except for adding Foreign Keys, which should be done through SQL in the SQL Database
      - The service can be started and stopped by selecting start/stop on the home page of the service
    - SQL Database: Device Location Tracking and Sharing
      - Changes to be made in Query Editor
      - SQL credentials to be passed on directly
- Firebase
  - Permissions to be passed on directly
  - Authenticated users can be added in the Authentication -> Users page
  - In order for a user to sign in through Google, their SHA certificate must be entered into the page accessed by clicking the gear next to the "Project Overview" button and selecting "Project Settings"
  
## Troubleshooting
- In the case of a 500 server error with the Azure service, restart the app service before trying any of the fixes in the development manual to make sure that the problem did not just require a simple fix.
