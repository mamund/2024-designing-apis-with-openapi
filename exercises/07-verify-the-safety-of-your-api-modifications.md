# Verify the Safety of Your API Modifications

Modify your existing OpenAPI design and re-run your tests
 * Start with your existing OpenAPI document
 * Make sure your SRT script passes all tests
 * Add a new URL resource, method, or parameter to your API
 * Update your SRT script to test the new design element
 * Re-run the tests (both existing and new) to confirm safe modifications


## Steps
Below are the steps to complete this exercisse

### Start with your existing OpenAPI document

 * Open up your OpenAPI document in the SwaggerHub editor
 * Activate the Mock Server

### Make sure your SRT script passes all tests
   
 * Open a command-line on your computer
 * Navigate to the folder that holds your SRT script
 * With the Mock Server running, execute your SRT script and confirm all tests pass

### Add a new URL resource, method, or parameter to your API

 * In the SwaggerHub editor, modify your API design
 * Add a new resource/URL or
 * Add an additional method to an existing resource/URL or
 * Add an additional *query parameter* to an existing resoruce/URL method or
 * Add an additional optional argument to an existing *requestBody* 
 * Save your updated design in SwaggerHub and fix any errors, if needed
 
### Update your SRT script to test the new design element
 * Open your *srt-list.txt* test script in your local text editor
 * Without changing any existing tests, add one or more new tests for the new API features
 * Save your *srt-list.txt* to disk and close your editor

### Re-run the tests (both existing and new) to confirm safe modifications
 * Open a command-line on your computer
 * Navigate to the folder that holds your SRT script
 * With the Mock Server running, execute your SRT script and confirm all tests pass


