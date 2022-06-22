### Issue Background

On Google Play, CP uses multiple Firebase projects to send push notifications to a single app - `app1-package-name`. With that configuration they can test features and send the push notification to test users only. Unfortunately Huawei Push Notifications are linked to single app. 

### Question
Is it possible to have multiple app IDs for single package name (e.g.  `app1-package-name`)? 

### Server Configuration

Current server side configuration: 

Settings("`app1-package-name`", "`app1-app-id`", "xxxSECRETxxx"); 
Settings("`app2-package-name`", "`app2-app-id`", "xxxSECRETxxx"); 

Desired server side configuration: 
Settings("`app1-package-name`", "`app1-app-id`", "xxxSECRETxxx"); 
Settings("`app1-package-name`", "newIdForTest", "xxxSECRETxxx"); 
Settings("`app2-package-name`", "`app2-app-id`", "xxxSECRETxxx"); 
Settings("`app2-package-name`", "newIdForTest", "xxxSECRETxxx");
