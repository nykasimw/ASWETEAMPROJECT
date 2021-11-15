# ASWETEAMPROJECT
ASWE Fall 2021 Group Project  

In order to build our service, you will need to ensure that the following files are in the same directory:  scraper.py, db.py, evaluation.py. Scraper.py creates the csv file for the culpa data which the database will be populated with. Db.py creates the database from the culpa data and contains functions for accessing specific information in the database such as get_entry_class(). Evaluation provides the API endpoints for the service. Note that upon running scraper.py, a csv file will be created which also needs to be in the same directory. Note that all imports listed on the top of each file must be downloaded in order for the code to successfully run. For example, one would need to make sure sqlite3, Error and csv are imported before running db.py. Run the code by first running scraper.py and ensuring that a csv file is produced and is then saved in the same directory as the other files. Then, run db.py followed by evaluation.py. One can test the endpoints by using Postman (make sure evaluation.py is running in order for Postman to connect), following the comments within evaluation.py for each endpoint. The comments will specify the name of the endpoint, information required and what the endpoint should output (we used localhost for the base URL on Postman). Additionally, if one wishes to run the unit tests ensure that test_db.py and test_evaluation.py are in the same directory as the aforementioned files - they can simply be run by pressing the play button in the IDE.
 
There are 7 (out of 9) operational entry points to our service: GET: ‘/’, ‘/professor’, ‘/easy’, ‘/final’, ‘/extensions’, ‘/difficulty’ and ‘/total_reviews’. ‘/’ is the entry point for the service and outputs a hello message letting the accesser know they are using the right service. ‘/professor’ requires a professor name in the request URL and outputs a single review for the desired professor. ‘/easy’ requires a professor name in the request URL and outputs a message with the number of occurrences found in the reviews regarding topics like lenient grading and recommendation. ‘/final’ requires a course title in the request URL and outputs a message with the number of occurrences found in the reviews regarding topics like take home final and final paper. ‘/extensions’ requires a professor name in the request URL and outputs a message with the number of occurrences found in the reviews regarding extensions. ‘/difficulty’ requires a course title in the request URL and outputs a message with the number of occurrences found in the reviews regarding topics harsh grading and hard. ‘/total_reviews’ requires a professor name in the request URL and outputs a message with the total number of reviews for a professor. 

No third party code