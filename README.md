# apodNasa
Note: assuming this is the requirement: " NASA APOD API availability for a public consumption, with parameters - date, hd, concept_tags, & api_key 

https://api.nasa.gov/planetary/apod



Certification of NASA APOD API service for public consumption through API calls:

       Test Case 1 (API): Verify user access to the site with generated token (api_key)
                    Steps:
                         1. Generate Token based on user name  //api_key=hAdnK2o8MFeL8D7WR1VYm8TahKUjPwlKETFQO5GQ
                         2. Post with generated tolen
                         3. Assert on respond code 200
      Test Case 2 (UI): Verify user can navigate to the url + token and render the page
                     Steps:
                     1. Generate Token based on user name
                     2. build url + hd
                     3. Open browser and navigate to the url.  //test with multiple browsers - Chrome, IE, Firefox and Edge
                     4. Get value of the title
                     5. Assert on page randering by checking image name - LighthouseJupSat_Saragozza_4480.jpg
   
       
   
       Test Case 3 (API): Verify date on the application is the same as today date and a version of the site - data and service_version
                 Steps: 
                 1. Get today date value
                 2. Get date from the url
                 3. Assert dates
   
       Test Case 4 (API): Verify version of the application - service_version
                 Steps: 
                 1. Get setvice_version value
                 2. Assert on expected service_version = v1
                 
       Test Case 5(API): Verify correct content of the page
                Steps:
                1. Get value of explanation
                2. Verify it's text
   
       Test Case 6(API): Verify correct concept_tags  - explanation and image_type
                1. Get value of media_type
                2. Asset it to expected "image"
