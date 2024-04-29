# Google cloud Functions Course
## Starting a project
to start a new project in google cloud , we can go to the Firebase Console(http://console.firebase.google.com) or 
create it form [Google cloud platform console](http://console.cloud.google.com)

## Creating a virtual environment                      ( so all other project can work together with the same version of Python)
First we have to install python3-venv with the following command:
sudo apt install python3-venv       - copy this command and pasted to terminal 
then we execute the following command:
'''
python3 -m venv venv
'''
to activate the virtual environmen we do:
source venv/bin/activate

''''''
in order to add new packages to our new virtual environment
we create a file called 'requirements.txt' and execute the following commands:
''''''
pip install -r requirements.txt
'''
## Deploying our functions
First, we have to set our project ID with the following command:
'''''''
gcloud config set project [YOUR_PROJECT_ID]  e.g $gcloud config set project cloud-function-course-f1109
'''''
Then we deploy our function with this command
$gcloud functions deploy [function_name] -- runtime python37 --trigger-http

## Deploying cloud functions with environment variables and other dependencies
we have to create a .env.yaml file and a requirements.txt file in the same directory of our main.py under emails folder
and run the following command:
'''
gcloud functions deploy [function name] --env-vars-file .env.yaml --runtime python37 --trigger-http
 after deploy then copy url and paste to PostMan
 