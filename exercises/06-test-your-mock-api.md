# Test Your Mock API


Update your OpenAPI definition to support Mocks and run your SRT script to test your API

 * Turn on mocking for your OpenAPI in Swagger Editor
 * Edit your copy of the SRT list to include your mock URL
 * Run the SRT script to confirm your mosk is up and running

_Optionally, add more URLs to your SRT script to create additional tests for your API mock._


**NOTE:** You will need to install and run a custom bash script to complete this exercise. See the github repo for details:
`https://github.com/mamund/simple-request-testing`

## Steps
Here are the steps for this exercise:

 
### Turn on Mocking for your OpenAPI in the Swagger Editor
 * Hover over the title of your API in the top left of the editor
 * Click on the down arrow to show the dialog box
 * Click on the word "Integrations" in the dialog
 * You should see the "API Auto Mocking" option
 * Click on the arrow to start the mock server
 * If prompted, save any changes
 * You should see a status message on the screen indicating your Mock server is running

### Edit your copy of the SRT list to include your mock URL
  * While the mock server is running, find the `servers:` section in the document
  * Find the Auto Mocking URL. You'll need this for your script
  * For example: `url: https://virtserver.swaggerhub.com/amundsen/simple-api/1.0`
  * Save the `srt-list.txt` script to disk.
  
### Run the SRT script to confirm your mosk is up and running
  * After running the mock server and editing your srt-list script, you are ready to run your test
  * Be sure to edit the SRT script to include at least one existing endpoint from your OpenAPI document
  * For example: `https://virtserver.swaggerhub.com/amundsen/simple-api/1.0/collection/`
  * To run the test, type `./srt.sh` and press [enter]
  * You should see a valid resonse from the Mock server.
  
### Optional additional work
Feel free to add more URLs to your SRT script to test other aspects of your API




