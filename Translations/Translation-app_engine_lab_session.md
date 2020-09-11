#LAB: Google Cloud Fundamentals: Getting Started with App Engine

## Objectives:

In this lab, you learn how to perform the following tasks:

    -Initialize App Engine.

    -Preview an App Engine application running locally in Cloud Shell.

    -Deploy an App Engine application, so that others can reach it.

    -Disable an App Engine application, when you no longer want it to be visible.

##Steps:

1. Activate Google Cloud Shell using the Google Cloud Platform (GCP) Console.

        gcloud auth list

        Result:

            The terminal should authenticate your account credentials allowing you to further as to list the project ID using the command:

                gcloud config list project


2. Initialize App Engine.

    -Initialize your App Engine app with your project and choose its region:

        gcloud app create --project=$DEVSHELL_PROJECT_ID

    -Clone the source code repository for a sample application in the hello_world directory:

        git clone https://github.com/GoogleCloudPlatform/python-docs-samples
    
    -Navigate to the source directory:

        cd python-docs-samples/appengine/standard_python3/hello_world


3. Run Hello World application locally.

    A. Execute the following command to download and update the packages list:

            sudo apt-get update

        -Set up a virtual environment in which you will run your application, using the command:

            sudo apt-get install virtualenv

        (If prompted [Y/n], press Y and then Enter)

        -Activate the virtual environment, using the command:

            source venv/bin/activate
    
        -Navigate to your project directory and install dependencies and run the apllication using commands:

            pip install  -r requirements.txt

            python main.py

    B. In Cloud Shell, click Web preview (Web Preview) > Preview on port 8080 to preview the application and end test using Ctrl+C to abort deployed services.


4. Deploy and run Hello World on App Engine.
    
    A. Navigate to the source directory:

            cd ~/python-docs-samples/appengine/standard_python3/hello_world

        -Deploy your Hello World application with the command:

            gcloud app deploy

        (If prompted [Y/n], press Y and then Enter)

    B. Launch your browser to view the app at http://YOUR_PROJECT_ID.appspot.com using:

            gcloud app browse

        -Copy and paste the URL into a new browser window.
    
             -Result:
            
                A webapge with the "Hello world message".


5. Exit terminal and end Lab session.